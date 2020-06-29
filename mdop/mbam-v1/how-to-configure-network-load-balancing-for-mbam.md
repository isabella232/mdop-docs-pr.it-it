---
title: Come configurare Bilanciamento carico di rete per MBAM
description: Come configurare Bilanciamento carico di rete per MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825515"
---
# Come configurare Bilanciamento carico di rete per MBAM


Per verificare che siano stati soddisfatti i prerequisiti e i requisiti hardware e software per installare la caratteristica server di amministrazione e monitoraggio, vedere [prerequisiti per la distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).

**Nota**  Per ottenere i file di log della configurazione, è necessario installare Microsoft BitLocker Administration and Monitoring (MBAM) tramite il pacchetto **msiexec** e l'opzione di posizione **/l** &lt; &gt; . I file di log vengono creati nella posizione specificata.

I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% dell'utente che installa MBAM.

 

I cluster di bilanciamento del carico di rete (NLB) per l'amministrazione e il server di monitoraggio offrono la scalabilità in MBAM e dovrebbe supportare più di 55.000 computer client MBAM.

**Nota**  Il bilanciamento del carico di rete di Windows Server distribuisce le richieste client in un set di server configurati in un singolo cluster di server. Quando il bilanciamento del carico di rete viene installato in ognuno dei server (host) in un cluster, il cluster presenta un indirizzo IP virtuale o un nome di dominio completo (FQDN) alle richieste del cliente. Le richieste client iniziali vengono inviate a tutti gli host del cluster, ma solo un host accetta e gestisce la richiesta.

Tutti i computer che faranno parte di un cluster NLB avranno i requisiti seguenti:

-   Tutti i computer nel cluster NLB devono essere nello stesso dominio.

-   Ogni computer nel cluster NLB deve usare un indirizzo IP statico.

-   Ogni computer nel cluster NLB deve avere il bilanciamento del carico di rete abilitato.

-   Il cluster NLB richiede un indirizzo IP statico e un record host deve essere creato manualmente nel DNS (Domain Name System).

 

## Configurazione del bilanciamento del carico di rete per i server di amministrazione e monitoraggio di MBAM


I passaggi seguenti descrivono come configurare un nome virtuale del cluster NLB e un indirizzo IP per due server di amministrazione e monitoraggio di MBAM e come configurare i client MBAM per l'uso del cluster NLB.

Prima di iniziare le procedure descritte in questo argomento, è necessario che la funzionalità MBAM Administration e Monitoring Server sia stata installata correttamente usando lo stesso binding della porta di IIS in due computer server distinti che soddisfano i prerequisiti per l'installazione delle funzionalità di MBAM server e la configurazione del cluster NLB.

**Nota**  Questo argomento descrive il processo di base dell'uso di Gestione bilanciamento carico di rete per creare un cluster NLB. La procedura esatta per configurare un server Windows come parte di un cluster NLB dipende dalla versione di Windows Server in uso. Per altre informazioni su come creare NLBs in WindowsServer2008, vedere [creazione di cluster di bilanciamento del carico di rete](https://go.microsoft.com/fwlink/?LinkId=197176) nella raccolta TechNet di Windows Server2008.

 

**Per configurare un nome virtuale del cluster NLB e un indirizzo IP per due server di amministrazione e monitoraggio di MBAM**

1.  Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **strumenti di amministrazione**e quindi fare clic su **Gestione bilanciamento carico di rete**.

    **Nota**  Se il gestore NLB non è presente, è possibile installarlo come caratteristica WindowsServer. È necessario installare questa funzionalità sia in amministrazione MBAM che in server di monitoraggio se si vuole configurarla nel cluster NLB.

     

2.  Sulla barra dei menu fare clic su **cluster**e quindi su **nuovo** per aprire la finestra di dialogo **parametri cluster** .

3.  Nella finestra di dialogo **parametri cluster** immettere le informazioni per la configurazione IP del cluster NLB:

    -   **Indirizzo IP:** Indirizzo IP del cluster NLB registrato nel DNS

    -   **Subnet mask:** Subnet mask dell'indirizzo IP del cluster NLB registrato nel DNS

    -   **Nome Internet completo:** FQDN del nome del cluster NLB registrato in DNS

4.  Verificare che l'opzione **unicast** sia selezionata in **modalità operazione cluster**e quindi fare clic su **Avanti**.

5.  Nella pagina **indirizzi IP del cluster** fare clic su **Avanti**.

6.  Nella pagina **regole porta** fare clic su **modifica** per definire le porte a cui il cluster NLB risponderà e configurare le porte usate per la comunicazione del sistema da client a sito mentre sono definite per il sito oppure fare clic su **Avanti** per abilitare l'indirizzo IP del cluster NLB per rispondere a tutte le porte TCP/IP.

    **Nota**  Verificare che l' **affinità** sia impostata su **Single**.

     

7.  Nella pagina **Connect** immettere un nome host dell'istanza di amministrazione e monitoraggio di mbam che farà parte del cluster NLB in **host**e quindi fare clic su **Connetti**.

8.  Nelle **interfacce disponibili per la configurazione di un nuovo cluster**selezionare l'interfaccia di rete che verrà configurata per rispondere alla comunicazione cluster NLB e quindi fare clic su **Avanti**.

9.  Nella pagina **Host Parameters** esaminare le informazioni visualizzate per verificare che le impostazioni di **configurazione IP dedicate** VISUALIZZino la configurazione IP dell'host dedicato per l'host del cluster NLB corretto, verificare che lo stato dell'host iniziale sia quello **predefinito:** viene **avviato**e quindi fare clic su **fine**.

    **Nota**  Nella pagina **parametri host** viene visualizzata anche la priorità dell'host del cluster NLB, che è da 1 a 32. Man mano che i nuovi host vengono aggiunti al cluster NLB, la priorità dell'host deve essere diversa dagli host aggiunti in precedenza. La priorità viene incrementata automaticamente quando si usa Gestione bilanciamento carico di rete.

     

10. Fare clic su ** &lt; nome &gt; cluster NLB** e verificare che lo **stato** dell'interfaccia host NLB venga visualizzato **convergente** prima di continuare. Questo passaggio può richiedere che il cluster NLB venga aggiornato come configurazione TCP/IP dell'host che viene modificata da gestione NLB.

11. Per aggiungere altri host al cluster NLB, fare clic con il pulsante destro del mouse su ** &lt; nome &gt; cluster NLB**, scegliere **Aggiungi host a cluster** e quindi ripetere i passaggi da 7 a 10 per ogni sistema di sito che farà parte del cluster NLB.

12. In un computer in cui è installato MBAM modello di criteri di gruppo, modificare le impostazioni dei criteri di gruppo di mbam per configurare gli endpoint di servizi di MBAM per usare il nome del cluster NLB e il binding della porta IIS appropriato per accedere alle funzionalità di amministrazione e monitoraggio di MBAM che vengono installate nei computer del cluster NLB. Per altre informazioni su come modificare le impostazioni dei GPO di MBAM, Vedi [come modificare le impostazioni di gpo 1,0](how-to-edit-mbam-10-gpo-settings.md). Se i server di amministrazione e monitoraggio di MBAM sono nuovi per l'ambiente, verificare che le appartenenze del gruppo di sicurezza locale richiesto siano state configurate correttamente. Per altre informazioni sui requisiti per il gruppo di sicurezza, vedere [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

13. Una volta completata la configurazione del cluster NLB, è consigliabile verificare che il cluster NLB di amministrazione e monitoraggio sia funzionale. A questo scopo, aprire un Web browser in un computer diverso dai server configurati in NLB e verificare che sia possibile accedere al sito Web di amministrazione e monitoraggio di MBAM tramite il nome di dominio completo NLB.

## Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





