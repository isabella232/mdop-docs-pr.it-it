---
title: Come installare e configurare MBAM in un server singolo
description: Come installare e configurare MBAM in un server singolo
author: dansimp
ms.assetid: 55841c63-bad9-44e7-b7fd-ea7037febbd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 225f66493ceafce5461df3fcc6f701e9a2922a5f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824096"
---
# Come installare e configurare MBAM in un server singolo


Le procedure descritte in questo argomento descrivono l'installazione completa delle funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in un singolo server.

Ogni funzionalità del server ha alcuni prerequisiti. Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md). Inoltre, alcune caratteristiche includono anche informazioni che devono essere fornite durante il processo di installazione per la distribuzione corretta della funzionalità. Dovresti anche rivedere la [preparazione dell'ambiente per mbam 1,0 prima di](preparing-your-environment-for-mbam-10.md) iniziare la distribuzione di mbam.

**Nota**  Per ottenere i file di log della configurazione, è necessario installare MBAM usando il pacchetto **msiexec** e l'opzione di posizione **/l** &lt; &gt; . I file di log vengono creati nella posizione specificata.

I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% dell'utente che sta installando MBAM.

 

## Per installare le funzionalità di MBAM server in un singolo server


I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.

**Nota**  Verificare di usare la configurazione a 32 bit nei server a 32 bit e la configurazione a 64 bit nei server a 64 bit.

 

**Per avviare l'installazione delle funzionalità di MBAM server**

1.  Avviare l'installazione guidata di MBAM. Fare clic su **Installa** nella pagina di benvenuto.

2.  Leggere e accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

3.  Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione. Le caratteristiche che verranno installate nello stesso computer devono essere installate contemporaneamente. Deselezionare le caratteristiche che si desidera installare altrove. È necessario installare le caratteristiche di MBAM nell'ordine seguente:

    -   Database di ripristino e hardware

    -   Database di conformità e controllo

    -   Audit e report di conformità

    -   Server di amministrazione e monitoraggio

    -   Modello di criteri di gruppo di MBAM

    **Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti. Se tutti i prerequisiti sono soddisfatti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Dopo aver soddisfatto tutti i prerequisiti, l'installazione riprende.

     

4.  Viene richiesto di configurare la sicurezza delle comunicazioni di rete. MBAM può crittografare la comunicazione tra il database di ripristino e hardware, il server di amministrazione e monitoraggio e i client. Se si decide di crittografare la comunicazione, viene chiesto di selezionare il certificato di provisioning dell'autorità che verrà usato per la crittografia.

5.  Fai clic su **Next** per continuare.

6.  La configurazione guidata MBAM visualizzerà le pagine di installazione per le caratteristiche selezionate.

**Per distribuire le caratteristiche del server MBAM**

1.  Nella finestra **Configura database hardware e ripristino** specificare l'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino e hardware. È inoltre necessario specificare sia la posizione dei file di database che il percorso delle informazioni del log.

2.  Fai clic su **Next** per continuare.

3.  Nella finestra **Configura database di conformità e controllo** specificare l'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo. Specificare quindi la posizione dei file di database e il percorso delle informazioni del log.

4.  Fai clic su **Next** per continuare.

5.  Nella finestra **report conformità e controllo** specificare l'istanza del servizio report che verrà usata e fornirà un account utente di dominio per l'accesso al database. Dovrebbe trattarsi di un account utente a cui viene effettuato il provisioning specifico per questo uso. L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.

6.  Fai clic su **Next** per continuare.

7.  Nella finestra **Configura il server di amministrazione e monitoraggio** immettere il **Binding della porta**, il **nome host** (facoltativo) e il **percorso di installazione** per l'amministrazione e il server di monitoraggio di mbam.

    **Avviso**  Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco.

     

8.  Fai clic su **Next** per continuare.

9.  Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**. L'opzione Microsoft Updates non attiva gli aggiornamenti automatici in Windows.

10. Quando la configurazione guidata ha raccolto le informazioni necessarie sulle caratteristiche, l'installazione di MBAM è pronta per iniziare. Fare clic su **Torna** per tornare alla procedura guidata se si vogliono rivedere o modificare le impostazioni di installazione. Fare clic su **Installa** per avviare l'installazione. Fare clic su **Annulla** per uscire dalla configurazione. Il programma di installazione installa le caratteristiche di MBAM e informa che l'installazione è stata completata.

11. Fare clic su **fine** per chiudere la procedura guidata.

12. Dopo aver installato le funzionalità di MBAM server, è necessario aggiungere utenti ai ruoli di MBAM. Per altre informazioni, Vedi [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Per eseguire la configurazione post-installazione**

1.  Al termine della configurazione, è necessario aggiungere ruoli utente in modo da consentire agli utenti di accedere alle funzionalità nel sito Web di amministrazione di MBAM. Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti:

    -   **Utenti di hardware MBAM**: i membri di questo gruppo locale possono accedere alla funzionalità hardware nel sito Web di amministrazione di mbam.

    -   **Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere al recupero delle unità e gestire le funzionalità TPM nel sito Web di amministrazione di mbam. Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.

    -   **Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le funzionalità TPM nel sito Web di amministrazione di mbam. Per gli utenti di helpdesk avanzati, è necessario solo il campo ID chiave in recupero unità. Per gestire gli utenti TPM, sono necessari solo il campo computer Domain e il nome computer.

2.  Nel database di amministrazione e monitoraggio Server, conformità e controllo e nel computer che ospita i report di conformità e controllo aggiungere utenti al gruppo locale seguente per consentire loro di accedere alla funzionalità report nel sito Web di amministrazione di MBAM:

    -   **Utenti di report mbam**: i membri di questo gruppo locale possono accedere alle funzionalità report nel sito Web di amministrazione di mbam.

    **Nota**  L'appartenenza a un utente o un gruppo di membri identici del gruppo di **utenti del report mbam** deve essere mantenuto in tutti i computer in cui sono installate le funzionalità di amministrazione e monitoraggio del server, il database di conformità e controllo e i report di conformità e controllo.

    Per mantenere le appartenenze identiche in tutti i computer, è necessario creare un gruppo di sicurezza del dominio e aggiungere il gruppo di dominio a ogni gruppo di utenti del report MBAM locale. Quando si esegue questa operazione, è possibile gestire le appartenenze ai gruppi usando il gruppo Domain.

     

## Convalida dell'installazione della funzionalità di MBAM server


Dopo aver completato l'installazione di MBAM, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM necessarie per la gestione di BitLocker. Usare la procedura seguente per verificare che il servizio MBAM sia funzionante:

**Per convalidare l'installazione delle funzionalità di MBAM server**

1. In ogni server in cui è distribuita una caratteristica di MBAM aprire il **Pannello di controllo**. Fare clic su **programmi**e quindi su **programmi e funzionalità**. Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .

   **Nota**  
   Per convalidare l'installazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.

     

2. Nel server in cui è installato il database di ripristino e hardware, aprire SQL Server Management Studio e verificare che il database **hardware e ripristino di mbam** sia installato.

3. Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il **database di verifica e conformità di mbam** .

4. Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con privilegi amministrativi e passare alla Home page del sito di SQL Server Reporting Services.

   La posizione iniziale predefinita di un'istanza del sito di SQL Server Reporting Services si trova in http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.

   Verificare che sia elencata una cartella denominata **report di conformità Malta** e che contenga cinque report e un'origine dati.

   **Nota**  
   Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *

     

5. Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**, selezionare **server Web (IIS)** e fare clic su **Gestione Internet Information Services (IIS)**

6. In **connessioni**passare a * &lt; nomecomputer &gt; *, selezionare **siti**e selezionare **amministrazione e monitoraggio di Microsoft BitLocker**. Verificare che **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.

7. Nel server in cui è installata la funzionalità di amministrazione e monitoraggio aprire un Web browser con privilegi amministrativi e quindi passare alle posizioni seguenti nel sito Web di MBAM per verificare che vengano caricati correttamente:

   -   *http:// &lt; nomecomputer &gt; /default.aspx* e confermare ognuno dei collegamenti per gli spostamenti e i report

   -   *http:// &lt; nomecomputer &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; nomecomputer &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nomecomputer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Nota**  
   In genere, i servizi vengono installati nella porta predefinita 80 senza crittografia di rete. Se i servizi sono installati in una porta diversa, modificare gli URL in modo da includere la porta appropriata. Ad esempio, http://* &lt; nomecomputer &gt; : &lt; Port &gt; */default.aspx o http:// <em> &lt; HostHeaderName &gt; / </em> default. aspx.

   Se i servizi sono installati con la crittografia di rete, cambiare http://in https://.

     

## Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





