---
title: Come aggiornare i server e i componenti del sistema
description: Come aggiornare i server e i componenti del sistema
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816425"
---
# Come aggiornare i server e i componenti del sistema


Usare la procedura seguente per aggiornare i componenti software installati in tutti i computer di sistema per la virtualizzazione delle applicazioni. I servizi di sistema di virtualizzazione delle applicazioni verranno riavviati automaticamente in ogni computer dopo l'aggiornamento.

**Nota**  
-   Il processo di aggiornamento Arresta tutti i servizi di sistema di virtualizzazione delle applicazioni, eliminando così il sistema dal servizio. Le sessioni utente devono essere interrotte prima di iniziare il processo di aggiornamento ed è consigliabile arrestare tutti i servizi Application Virtualization Server nell'ambiente.

-   Se si hanno più server che condividono l'accesso al database di virtualizzazione dell'applicazione, è necessario che tutti questi server vengano disattivati durante l'aggiornamento del database. È consigliabile seguire le normali procedure aziendali per l'aggiornamento del database, ma è consigliabile testare l'aggiornamento del database usando una copia di backup del database per la prima volta in un server di test. Devi quindi selezionare uno dei server per il primo aggiornamento, che aggiornerà lo schema del database. Dopo che il database di produzione è stato aggiornato correttamente, è possibile aggiornare gli altri server.

-   È possibile eseguire l'aggiornamento a Microsoft Application Virtualization (App-V) 4.5 solo da Microsoft Application Virtualization (App-V) 4.1 o 4.1 SP1. App-V 4.0 e versioni precedenti devono essere disinstallate o aggiornate in 4.1 o 4.1 SP1 prima di eseguire l'aggiornamento a App-V 4.5.

 

**Per aggiornare i componenti software nei computer dei sistemi di virtualizzazione delle applicazioni**

1.  Passare al percorso del programma di installazione nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic sul file Setup.exe.

2.  Nella pagina di **benvenuto** dell'installazione guidata fare clic su **Avanti**.

3.  Nella pagina **contratto di licenza** leggere il contratto di licenza, verificare **di accettare i termini del contratto di licenza**e fare clic su **Avanti**.

4.  Quando si apre la pagina **software installata** e viene visualizzato un elenco dei componenti del sistema di virtualizzazione delle applicazioni installati e della versione di ogni componente, fare clic su **Avanti**.

5.  Nella pagina **avviso di perdita della sessione** leggere il messaggio visualizzato e fare clic su **Avanti**.

6.  Nella pagina **Connetti a database di configurazione** esaminare il contenuto della pagina e fare clic su **Avanti**.

7.  Se viene visualizzata la pagina di **aggiornamento del database** , è necessario un aggiornamento del database. Immettere le credenziali amministrative del database e quindi fare clic su **Avanti**. Se questa pagina non è visualizzata, passare al passaggio 9.

8.  Nella pagina **Database Configuration backup** selezionare le caselle appropriate per eseguire il backup ed esportarlo in una posizione esistente e quindi fare clic su **Avanti**.

    **Importante**  Per poter eseguire il rollback alla versione precedente in caso di errore di aggiornamento, verificare di aver **eseguito il backup della casella database di configurazione oppure di** perdere i dati di configurazione.

    Quando si vuole ripristinare un database con VSS, è necessario prima di tutto arrestare il servizio App-V Server nel server di gestione. Questa operazione deve essere eseguita in ogni server di gestione se sono presenti più server connessi allo stesso database.

     

9.  Nella prima pagina di **convalida del pacchetto** leggere il contenuto e quindi fare clic su **Avanti**.

10. Nella seconda pagina di **convalida del pacchetto** è possibile visualizzare i dettagli della convalida del pacchetto in una finestra del blocco note. Per visualizzare i dettagli, fare clic su **Dettagli**; in caso contrario, fare clic su **Avanti**.

11. Nella pagina **pronto per l'aggiornamento della programmazione** fare clic su **Avanti**.

12. Nella pagina **installazione guidata completare** fare clic su **fine**.

13. Ripetere i passaggi da 1 a 12 in tutti gli altri computer in cui è stata installata l'Application Virtualization Management Console o il componente software Application Virtualization Server.

    Dopo l'aggiornamento dell'archivio dati, è possibile riprendere il normale funzionamento. L'aggiornamento dell'archivio dati viene aggiornato quando si aggiorna un server o il servizio Web di gestione App-V.

## Argomenti correlati


[Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





