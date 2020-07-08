---
title: Come installare e configurare MBAM in un server singolo
description: Come installare e configurare MBAM in un server singolo
author: dansimp
ms.assetid: 45e6a012-6c8c-4d90-902c-d09de9a0cbea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53e170f421bdce8dd6f771af3902af627a15a085
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824066"
---
# Come installare e configurare MBAM in un server singolo


Le procedure descritte in questo argomento descrivono come installare Microsoft BitLocker Administration and Monitoring (MBAM) nella topologia autonoma in un singolo server. Usare la configurazione a server singolo solo in un ambiente di test. Per gli ambienti di produzione, usa due o più server. Se si sta installando l'amministrazione e il monitoraggio di Microsoft BitLocker tramite la topologia di Configuration Manager, vedere [distribuzione di mbam con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Il diagramma seguente mostra un esempio di architettura a server singolo. Per una descrizione dei database e delle caratteristiche, vedere [architettura di alto livello per MBAM 2,0](high-level-architecture-for-mbam-20-mbam-2.md).

![singola topologia di distribuzione di MBAM 2 server](images/mbam2-1-server.gif)

Ogni funzionalità del server ha alcuni prerequisiti. Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). Inoltre, alcune caratteristiche includono anche informazioni che devono essere fornite durante il processo di installazione per la distribuzione corretta della funzionalità. Dovresti anche rivedere [la preparazione dell'ambiente per mbam 2,0 prima di iniziare la distribuzione di](preparing-your-environment-for-mbam-20-mbam-2.md) mbam.

**Nota**  
Per ottenere i file di log della configurazione, è necessario usare il pacchetto msiexec **/L** e l' &lt; &gt; opzione di posizione/l per installare mbam. I file di log vengono creati nella posizione specificata.

I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% nel server dell'utente che sta installando MBAM.



## Per installare le funzionalità di MBAM server in un singolo server


I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.

**Per avviare l'installazione delle funzionalità di MBAM server**

1.  Nel server in cui si vuole installare MBAM eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.

2.  Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** **selezionare la topologia autonoma** e quindi fare clic su **Avanti**.

5.  Nella pagina **selezionare le caratteristiche da installare** selezionare le caratteristiche che si desidera installare. Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione. Le caratteristiche da installare nello stesso computer devono essere installate contemporaneamente. Deselezionare le caselle di controllo relative a tutte le funzionalità che si desidera installare altrove. È necessario installare le caratteristiche di MBAM nell'ordine seguente:

    -   Database di ripristino

    -   Database di conformità e controllo

    -   Report di conformità e controllo

    -   Server self-service

    -   Server di amministrazione e monitoraggio

    -   Modello di criteri di gruppo di MBAM

    **Nota**  
    La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti. Se tutti i prerequisiti sono soddisfatti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.



6.  Nella pagina **Configura sicurezza comunicazioni di rete** scegliere se crittografare la comunicazione tra i servizi Web nel server di amministrazione e monitoraggio e nei client. Se si decide di crittografare la comunicazione, selezionare il certificato di provisioning dell'autorità di certificazione da usare per la crittografia. Il certificato deve essere creato prima di questo passaggio per consentire di selezionarlo in questa pagina.

    **Nota**  
    Questa pagina viene visualizzata solo se è stata selezionata la caratteristica portale self-service o amministrazione e monitoraggio server nella pagina **selezionare le caratteristiche da installare** .



7.  Fare clic su **Avanti**e quindi passare al set di passaggi successivo per configurare le caratteristiche del server mbam.

**Per configurare le caratteristiche del server MBAM**

1.  Nella pagina **Configura database di ripristino** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino. È inoltre necessario specificare sia la posizione in cui si trovano i file di database che le informazioni sul log.

2.  Fai clic su **Next** per continuare.

3.  Nella pagina **Configura il database di conformità e controllo** specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo. Devi anche specificare la posizione in cui si trovano i file di database e dove verranno individuate le informazioni sul log.

4.  Fai clic su **Next** per continuare.

5.  Nella pagina **configurare i report di conformità e controllo** specificare l'istanza di SQL Server Reporting Services in cui verranno installati i report di conformità e controllo e specificare un account utente di dominio e una password per accedere al database di conformità e controllo. Configurare la password per l'account per non scadere mai. L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.

6.  Fai clic su **Next** per continuare.

7.  Nella pagina **Configura il portale self-service** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per il portale self-service.

    **Nota**  
    Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco. Se si usa Windows Firewall, la porta verrà aperta automaticamente.



8.  Fai clic su **Next** per continuare.

9.  Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**. Ciò non consente di attivare gli aggiornamenti automatici in Windows.

10. Nella pagina **Configura il server di amministrazione e monitoraggio** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per il sito Web dell'help desk.

    **Nota**  
    Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco. Se si usa Windows Firewall, la porta verrà aperta automaticamente.



11. Nella pagina **Riepilogo installazione** esaminare l'elenco delle caratteristiche che verranno installate e fare clic su **Installa** per avviare l'installazione delle funzionalità di mbam. Fare clic su **Torna** per tornare alla procedura guidata se è necessario rivedere o modificare le impostazioni di installazione oppure fare clic su **Annulla** per uscire dalla configurazione. Il programma di installazione installa le caratteristiche di MBAM e informa che l'installazione è stata completata.

12. Fare clic su **fine** per chiudere la procedura guidata. Dopo aver installato le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker, passare alla sezione successiva e completare la procedura per aggiungere utenti ai ruoli di amministrazione e monitoraggio di Microsoft BitLocker. Per altre informazioni sui ruoli, vedere [pianificazione dei ruoli di amministratore di MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

**Per eseguire la configurazione post-installazione**

1.  Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti per consentire l'accesso alle funzionalità del sito Web di MBAM help desk:

    -   **Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere al recupero delle unità e gestire le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam. Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.

    -   **Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam. Per gli utenti di helpdesk avanzati, è necessario solo il campo **ID chiave** in recupero unità. In Manage TPM sono necessari solo il campo **computer Domain** e il **nome computer** .

2.  Nel server di amministrazione e monitoraggio aggiungere utenti al gruppo locale seguente per consentire loro di accedere alla funzionalità report nel sito Web amministrazione e monitoraggio di MBAM:

    -   **Utenti di report mbam**: i membri di questo gruppo locale possono accedere alle funzionalità report nel sito Web amministrazione e monitoraggio di mbam.

    -   Marca il portale self-service con il nome della società, il testo dell'avviso e altre informazioni specifiche della società. Per istruzioni, Vedi [come personalizzare il portale self-service](how-to-brand-the-self-service-portal.md).

    **Nota**  
    L'appartenenza a un utente o un gruppo identico al gruppo locale degli **utenti del report mbam** deve essere mantenuta in tutti i computer in cui sono installate le funzionalità mbam Administration e Monitoring Server, la conformità e il database di audit e i report di conformità e controllo. Il modo consigliato per eseguire questa operazione consiste nel creare un gruppo di sicurezza del dominio e aggiungere il gruppo di dominio a ogni gruppo di utenti del report MBAM locale. Quando si usa questo processo, gestire le appartenenze ai gruppi tramite il gruppo di domini.



## Convalida dell'installazione della funzionalità di MBAM server


Dopo aver completato l'installazione di amministrazione e monitoraggio di Microsoft BitLocker, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM necessarie per la gestione di BitLocker. Usare la procedura seguente per verificare che il servizio MBAM sia funzionante.

**Per convalidare l'installazione delle funzionalità di MBAM server**

1. In ogni server in cui è distribuita una caratteristica di MBAM aprire il **Pannello di controllo**. Selezionare **programmi**e quindi selezionare **programmi e funzionalità**. Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .

   **Nota**  
   Per convalidare l'installazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.



2. Nel server in cui è installato il database di ripristino, aprire SQL Server Management Studio e verificare che il database **di ripristino e hardware di mbam** sia installato.

3. Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il **database dello stato di conformità di mbam** .

4. Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con credenziali amministrative e passare alla Home page del sito di SQL Server Reporting Services.

   La posizione iniziale predefinita di un'istanza del sito di SQL Server Reporting Services si trova in http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.

   Verificare che una cartella report denominata amministrazione e monitoraggio di Microsoft BitLocker contenga un'origine dati denominata **MaltaDataSource** e che una cartella **en-US** contenga quattro report.

   **Nota**  
   Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**. Selezionare **server Web (IIS)** e quindi fare clic su **Gestione Internet Information Services (IIS).**

6. In **connessioni** passare a * &lt; nomecomputer &gt; *, selezionare **siti**e quindi selezionare **amministrazione e monitoraggio di Microsoft BitLocker**. Verificare che **MBAMAdministrationService**, **MBAMUserSupportService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.

7. Nel server in cui sono installate le funzionalità di amministrazione e monitoraggio e il portale self-service aprire un Web browser con credenziali amministrative e individuare le posizioni seguenti per verificare che vengano caricate correttamente:

   -   *http:// &lt; hostname &gt; /helpdesk/default.aspx* e confermare tutti i collegamenti per l'esplorazione e i report

   -   *http:// &lt; hostname &gt; /selfservice&gt;/*

   -   *http:// &lt; nomecomputer &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; nomecomputer &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nomecomputer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Nota**  
   Si presuppone che le funzionalità del server siano installate nella porta predefinita senza crittografia di rete. Se sono state installate le funzionalità del server in una porta o una directory virtuale diversa, modificare gli URL per includere la porta appropriata, ad esempio *http:// &lt; hostname &gt; : &lt; Port &gt; /helpdesk/default.asp*x o*http:// &lt; hostname &gt; : &lt; Port &gt; / &lt; VirtualDirectory &gt; /default.aspx*

   Se le funzionalità del server sono state installate con la crittografia di rete, cambiare http://in https://.



## Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









