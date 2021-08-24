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
ms.openlocfilehash: 4dffe2e2dcb82866b86a3ac281aca8a0dcaab686
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910661"
---
# <a name="how-to-install-and-configure-mbam-on-a-single-server"></a>Come installare e configurare MBAM in un server singolo


Le procedure descritte in questo argomento descrivono come installare Microsoft BitLocker Administration and Monitoring (MBAM) nella topologia autonoma in un singolo server. Utilizzare la configurazione a server singolo solo in un ambiente di testing. Per gli ambienti di produzione, utilizzare due o più server. Se si installa Amministrazione e monitoraggio di Microsoft BitLocker utilizzando la topologia di Configuration Manager, vedere [Deploying MBAM with Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Il diagramma seguente mostra un esempio di architettura a server singolo. Per una descrizione dei database e delle funzionalità, vedere [High-Level Architecture for MBAM 2.0.](high-level-architecture-for-mbam-20-mbam-2.md)

![Topologia di distribuzione a server singolo mbam 2.](images/mbam2-1-server.gif)

Ogni funzionalità del server dispone di alcuni prerequisiti. Per verificare di aver soddisfatto i prerequisiti e i requisiti hardware e software, vedere [MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) e [MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md). Inoltre, alcune funzionalità dispongono anche di informazioni che devono essere fornite durante il processo di installazione per distribuire correttamente la funzionalità. È inoltre consigliabile esaminare [Preparazione dell'ambiente per MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md) prima di avviare la distribuzione di MBAM.

**Nota**  
Per ottenere i file di registro dell'installazione, è necessario utilizzare il pacchetto Msiexec e l'opzione **/L** &lt; location per installare &gt; MBAM. I file di registro vengono creati nel percorso specificato.

Ulteriori file di registro dell'installazione vengono creati nella cartella %temp% nel server dell'utente che installa MBAM.



## <a name="to-install-mbam-server-features-on-a-single-server"></a>Per installare le funzionalità del server MBAM in un singolo server


I passaggi seguenti descrivono come installare le funzionalità generali di MBAM.

**Per avviare l'installazione delle funzionalità del server MBAM**

1.  Nel server in cui si desidera installare MBAM, eseguireMBAMSetup.exe** per ** avviare l'installazione guidata di MBAM.

2.  Nella pagina **iniziale,** facoltativamente, selezionare il programma Analisi utilizzo **software**e quindi fare clic su **Avvia.**

3.  Leggere e accettare il Contratto di licenza software Microsoft, quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** selezionare **** la topologia autonoma e quindi fare clic su **Avanti.**

5.  Nella pagina **Seleziona funzionalità da installare** selezionare le funzionalità che si desidera installare. Per impostazione predefinita, tutte le funzionalità di MBAM sono selezionate per l'installazione. Le funzionalità che devono essere installate nello stesso computer devono essere installate contemporaneamente. Deselezionare le caselle di controllo per tutte le funzionalità che si desidera installare altrove. È necessario installare le funzionalità di MBAM nell'ordine seguente:

    -   Database di ripristino

    -   Database di conformità e controllo

    -   Report di conformità e controllo

    -   Self-Service Server

    -   Amministrazione e Monitoring Server

    -   Modello Criteri di gruppo MBAM

    **Nota**  
    L'installazione guidata controlla i prerequisiti per l'installazione e visualizza i prerequisiti mancanti. Se vengono soddisfatti tutti i prerequisiti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.



6.  Nella pagina **Configura sicurezza comunicazioni di** rete scegliere se crittografare la comunicazione tra i servizi Web nell'amministrazione e monitoring server e i client. Se si decide di crittografare la comunicazione, selezionare il certificato di cui è stato effettuato il provisioning dell'autorità di certificazione da utilizzare per la crittografia. Il certificato deve essere creato prima di questo passaggio per consentirti di selezionarlo in questa pagina.

    **Nota**  
    Questa pagina viene visualizzata solo se è stata selezionata la funzionalità Self-Service Portal o Amministrazione e Monitoring Server nella **pagina Selezione funzionalità da** installare.



7.  Fare **clic**su Avanti e quindi passare al set di passaggi successivo per configurare le funzionalità del server MBAM.

**Per configurare le funzionalità del server MBAM**

1.  Nella pagina **Configura database di ripristino** specificare il nome dell SQL Server e il nome del database in cui verranno archiviati i dati di ripristino. È inoltre necessario specificare la posizione dei file di database e la posizione delle informazioni di registro.

2.  Fai clic su **Next** per continuare.

3.  Nella pagina **Configura database di conformità** e controllo specificare il nome dell'istanza SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo. È inoltre necessario specificare la posizione dei file di database e la posizione delle informazioni di registro.

4.  Fai clic su **Next** per continuare.

5.  Nella pagina **Configura** report di conformità e controllo specificare l'istanza di SQL Server Reporting Services in cui verranno installati i report conformità e controllo e specificare un account utente di dominio e una password per accedere al database di conformità e controllo. Configurare la password per questo account in modo che non scada mai. L'account utente deve essere in grado di accedere a tutti i dati disponibili per il gruppo MbAM Reports Users.

6.  Fai clic su **Next** per continuare.

7.  Nella pagina **Configure the Self-Service Portal** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per Self-Service Portal.

    **Nota**  
    Il numero di porta specificato deve essere un numero di porta inutilizzato in Administration and Monitoring Server, a meno che non si specifica un nome di intestazione host univoco. Se si utilizza Windows Firewall, la porta verrà aperta automaticamente.



8.  Fai clic su **Next** per continuare.

9.  Specificare se utilizzare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti.** In questo modo non viene attivata la funzionalità Aggiornamenti automatici Windows.

10. Nella pagina **Configure the Administration and Monitoring Server** immettere il numero di porta, il nome host, il nome della directory virtuale e il percorso di installazione per il sito Web help desk.

    **Nota**  
    Il numero di porta specificato deve essere un numero di porta inutilizzato in Administration and Monitoring Server, a meno che non si specifica un nome di intestazione host univoco. Se si utilizza Windows Firewall, la porta verrà aperta automaticamente.



11. Nella pagina **Riepilogo installazione** esaminare l'elenco delle funzionalità che verranno installate e fare clic su **Installa** per avviare l'installazione delle funzionalità di MBAM. Fare **clic su** Indietro per tornare alla procedura guidata se è necessario rivedere o modificare le impostazioni di installazione oppure fare clic su **Annulla** per uscire dall'installazione. Il programma di installazione installa le funzionalità di MBAM e avvisa l'utente che l'installazione è stata completata.

12. Fare **clic su** Fine per uscire dalla procedura guidata. Dopo aver installato le funzionalità di Amministrazione e Monitoring Server di Microsoft BitLocker, passare alla sezione successiva e completare i passaggi necessari per aggiungere utenti ai ruoli di amministrazione e monitoraggio di Microsoft BitLocker. Per ulteriori informazioni sui ruoli, vedere [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).

**Per eseguire la configurazione post-installazione**

1.  In Administration and Monitoring Server, aggiungere gli utenti ai gruppi locali seguenti per consentire loro l'accesso alle funzionalità del sito Web dell'Help Desk di MBAM:

    -   **Utenti dell'helpdesk MBAM**: i membri di questo gruppo locale possono accedere alle funzionalità Di ripristino unità e Gestione TPM nel sito Web Amministrazione e monitoraggio di MBAM. Tutti i campi in Ripristino unità e Gestione TPM sono campi obbligatori per un utente dell'helpdesk.

    -   **MbAM Advanced Helpdesk Users**: i membri di questo gruppo locale hanno accesso avanzato alle funzionalità di ripristino delle unità e gestione del TPM nel sito Web Amministrazione e monitoraggio di MBAM. Per gli utenti dell'helpdesk avanzato, solo il campo **ID** chiave è obbligatorio in Ripristino unità. In Gestisci TPM sono obbligatori solo il **campo Dominio computer** e il campo **Nome** computer.

2.  In Administration and Monitoring Server, aggiungere gli utenti al gruppo locale seguente per consentire loro di accedere alla funzionalità Report nel sito Web Amministrazione e monitoraggio di MBAM:

    -   **Utenti report MBAM**: i membri di questo gruppo locale possono accedere alle funzionalità report nel sito Web Amministrazione e monitoraggio di MBAM.

    -   Brand the Self-Service Portal with your company name, notice text, and other company-specific information. Per istruzioni, vedere [Come brandire il portale Self-Service.](how-to-brand-the-self-service-portal.md)

    **Nota**  
    Appartenenza a utenti o gruppi identici del gruppo locale **MBAM Report Gli** utenti devono essere mantenuti in tutti i computer in cui sono installate le funzionalità di Amministrazione e Monitoring Server di MBAM, Database di conformità e controllo e Report di conformità e controllo. A tale scopo, è consigliabile creare un gruppo di sicurezza di dominio e aggiungere tale gruppo di dominio a ogni gruppo locale di utenti di report MBAM. Quando si utilizza questo processo, gestire le appartenenze ai gruppi tramite il gruppo di dominio.



## <a name="validating-the-mbam-server-feature-installation"></a>Convalida dell'installazione delle funzionalità del server MBAM


Al termine dell'installazione di Amministrazione e monitoraggio di Microsoft BitLocker, verificare che l'installazione abbia configurato correttamente tutte le funzionalità MBAM necessarie per la gestione di BitLocker. Utilizzare la procedura seguente per verificare che il servizio MBAM sia funzionante.

**Per convalidare l'installazione delle funzionalità del server MBAM**

1. In ogni server in cui è distribuita una funzionalità MBAM, aprire Pannello **di controllo.** Selezionare **Programmi**e quindi **Programmi e funzionalità.** Verificare che **Microsoft BitLocker Administration and Monitoring** sia visualizzato nell'elenco Programmi **e** funzionalità.

   **Nota**  
   Per convalidare l'installazione, è necessario utilizzare un account di dominio con credenziali amministrative del computer locale in ogni server.



2. Nel server in cui è installato il database di ripristino, aprire SQL Server Management Studio e verificare che il database di ripristino e hardware di **MBAM** sia installato.

3. Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il database dello stato di conformità **MBAM.**

4. Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con credenziali amministrative e passare alla "Home" del sito SQL Server Reporting Services sito.

   La posizione iniziale predefinita di SQL Server Reporting Services'istanza del sito è http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports. Per trovare l'URL effettivo, utilizzare lo strumento Gestione configurazione Reporting Services e selezionare le istanze specificate durante l'installazione.

   Verificare che una cartella Reports denominata Microsoft BitLocker Administration and Monitoring contenga un'origine dati denominata **MaltaDataSource** e che una cartella **en-us** contenga quattro report.

   **Nota**  
   Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Nel server in cui è installata la funzionalità amministrazione e monitoraggio, eseguire **Server Manager** e passare a **Ruoli**. Selezionare **Server Web (IIS)** e quindi fare clic su Gestione Internet Information Services **(IIS).**

6. In **Connessioni passare** a * &lt; nomecomputer &gt; *, selezionare **Siti**e quindi Selezionare Amministrazione e monitoraggio di **Microsoft BitLocker**. Verificare che **MBAMAdministrationService,** **MBAMUserSupportService,** **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.

7. Nel server in cui sono installate le funzionalità di amministrazione e monitoraggio e il portale di Self-Service, aprire un Web browser con credenziali amministrative e individuare i percorsi seguenti per verificare che il caricamento sia stato eseguito correttamente:

   -   *http:// &lt; hostname &gt; /HelpDesk/default.aspx* e confermare ognuno dei collegamenti per lo spostamento e i report

   -   *http:// &lt; hostname &gt; /SelfService&gt;/*

   -   *http:// &lt; computername &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; hostname &gt; /MBAMUserSupportService/UserSupportService.svc*

   -   *http:// &lt; computername &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; computername &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Nota**  
   Si presuppone che le funzionalità del server siano state installate sulla porta predefinita senza crittografia di rete. Se le funzionalità del server sono installate in una porta o in una directory virtuale diversa, modificare gli URL in modo da includere la porta appropriata, ad esempio *nomehost http:// &lt; : porta &gt; &lt; &gt; /HelpDesk/default.asp*x o nome*host http:// : port &lt; &gt; &lt; &gt; / &lt; virtualdirectory &gt; /default.aspx*

   Se le funzionalità del server sono state installate con la crittografia di rete, modificare http:// in https://.



## <a name="related-topics"></a>Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









