---
title: Come installare e configurare MBAM su server distribuiti
description: Come installare e configurare MBAM su server distribuiti
author: dansimp
ms.assetid: 9ee766aa-6339-422a-8d00-4f58e4646a5e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51f56a12d4e59226f834c7e474af0f1e96c1e8e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825656"
---
# Come installare e configurare MBAM su server distribuiti


Le procedure descritte in questo argomento descrivono l'installazione completa delle funzionalità di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker nei server distribuiti.

Ogni funzionalità del server ha alcuni prerequisiti. Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md). Alcune funzionalità richiedono inoltre di specificare determinate informazioni durante il processo di installazione per la distribuzione corretta della funzionalità.

**Nota**  
Per ottenere i file di log della configurazione, è necessario installare MBAM usando il pacchetto **msiexec** e l'opzione di ** &lt; posizione &gt; /l** . I file di log vengono creati nella posizione specificata.

I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% dell'utente che esegue l'installazione di MBAM.



## <a href="" id="deploy-the-mbam-server-features-"></a>Distribuire le caratteristiche del server MBAM


I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.

**Nota**  
Verificare di usare la configurazione a 32 bit nei server a 32 bit e la configurazione a 64 bit nei server a 64 bit.



**Per distribuire le caratteristiche del server MBAM**

1.  Avviare l'installazione guidata di MBAM e fare clic su **Installa** nella pagina di benvenuto.

2.  Leggere e accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

3.  Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione. Deselezionare le caratteristiche che si desidera installare altrove. Le caratteristiche che si desidera installare nello stesso computer devono essere installate tutte contemporaneamente. Le caratteristiche di MBAM devono essere installate nell'ordine seguente:

    -   Database di ripristino e hardware

    -   Database di conformità e controllo

    -   Audit e report di conformità

    -   Server di amministrazione e monitoraggio

    -   Modello di criteri di gruppo di MBAM

    **Nota**  
    La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti. Se tutti i prerequisiti sono soddisfatti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Se sono soddisfatte tutte le condizioni preliminari, verrà ripresa l'installazione.



4.  La configurazione guidata MBAM visualizzerà le pagine di installazione per le caratteristiche selezionate. Nelle sezioni seguenti vengono descritte le procedure di installazione per ogni funzionalità.

    **Nota**  
    In genere, ogni funzionalità viene installata in un server separato. Se si vogliono installare più funzionalità in un singolo server, è possibile modificare o eliminare alcuni dei passaggi seguenti.



~~~
**To install the Recovery and Hardware Database**

1.  Choose an option for MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the names of the computers that will be running the Administration and Monitoring Server feature, to configure access to the Recovery and Hardware Database.. Once the Administration and Monitoring Server feature is deployed, it connects to the database by using its domain account.

4.  Click **Next** to continue.

5.  Specify the **Database Configuration** for the SQL Server instance that stores the recovery and hardware data. You must also specify where the database will be located and where the log information will be located.

6.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Database**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Compliance and Audit Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that will be used for encryption.

2.  Click **Next** to continue.

3.  Specify the user account that will be used to access the database for reports.

4.  Click **Next** to continue.

5.  Specify the computer names of the computers that you want to run the Administration and Monitoring Server and the Compliance and Audit Reports, to configure the access to the Compliance and Audit Database.. After the Administration and Monitoring and the Compliance and Audit Reports Server are deployed, they will connect to the databases by using their domain accounts.

6.  Specify the **Database Configuration** for the SQL Server instance that will store the compliance and audit data. You must also specify where the database will be located and where the log information will be located.

7.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Compliance and Audit Reports**

1.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Compliance and Audit Database are installed.

2.  Specify the name of the Compliance and Audit Database. By default, the database name is “MBAM Compliance Status”, but you can change the name when you install the Compliance and Audit Database.

3.  Click **Next** to continue.

4.  Select the SQL Server Reporting Services instance where the Compliance and Audit Reports will be installed. Provide the username and password used to access the compliance database.

5.  Click **Next** to continue with the MBAM Setup wizard.

**To install the Administration and Monitoring Server feature**

1.  Choose an option for the MBAM communication encryption. MBAM can encrypt the communication between the Recovery and Hardware Database and the Administration and Monitoring servers. If you choose the option to encrypt communication, you are asked to select the authority-provisioned certificate that is used for encryption.

2.  Click **Next** to continue.

3.  Specify the remote SQL Server instance, For example, *&lt;ServerName&gt;*, where the Compliance and Audit Database are installed.

4.  Specify the name of the Compliance and Audit Database. By default, the database name is MBAM Compliance Status, but, you can change the name when you install the Compliance and Audit Database.

5.  Click **Next** to continue.

6.  Specify the remote SQL Server instance. For example, *&lt;ServerName&gt;*,where the Recovery and Hardware Database are installed.

7.  Specify the name of the Recovery and Hardware Database. By default, the database name is **MBAM Recovery and Hardware**, but you can change the name when you install the Recovery and Hardware Database feature.

8.  Click **Next** to continue.

9.  Specify the URL for the “Home” of the SQL Server Reporting Services (SRS) site. The default Home location of a SQL Server Reporting Services site instance is at:

    http://*&lt;NameofMBAMReportsServer&gt;/*ReportServer

    **Note**  
    If you configured the SQL Server Reporting Services as a named instance, the URL resembles the following:http://*&lt;NameofMBAMReportsServer&gt;*/ReportServer\_*&lt;SRSInstanceName&gt;*



10. Click **Next** to continue.

11. Enter the **Port Number**, the **Host Name** (optional), and the **Installation Path** for the MBAM Administration and Monitoring server

    **Warning**  
    The port number that you specify must be an unused port number on the Administration and Monitoring server, unless you specify a unique host header name.



12. Click **Next** to continue with the MBAM Setup wizard.
~~~

5. 

   Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.

6. Quando le informazioni della caratteristica MBAM selezionato sono completate, si è pronti per avviare l'installazione di MBAM usando la configurazione guidata. Fare clic su **Torna** per spostarsi nella procedura guidata se è necessario rivedere o modificare le impostazioni di installazione. Fare clic su **Installa** per avviare l'installazione. Fare clic su **Annulla** per chiudere la procedura guidata. Il programma di installazione installa le caratteristiche di MBAM selezionate e informa che l'installazione è terminata.

7. Fare clic su **fine** per chiudere la procedura guidata.

8. Aggiungere utenti ai ruoli appropriati di MBAM, dopo aver installato le funzionalità del server MBAM. Per altre informazioni, Vedi [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

**Configurazione post-installazione**

1.  Dopo aver completato la configurazione di MBAM, è necessario aggiungere ruoli utente prima che gli utenti possano accedere alle funzionalità nel sito Web di amministrazione di MBAM. Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti.

    -   **Utenti di hardware MBAM**: i membri di questo gruppo locale possono accedere alla funzionalità hardware nel sito Web di amministrazione di mbam.

    -   **Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere alle funzionalità TPM (Trusted Platform Modules) nel sito Web di amministrazione di mbam. Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.

    -   **Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le funzionalità TPM nel sito Web di amministrazione di mbam. Per gli utenti di helpdesk avanzati, è necessario solo il campo ID chiave in recupero unità. In Manage TPM sono necessari solo il campo computer Domain e il nome computer.

2.  Nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita i report di conformità e controllo aggiungere utenti al gruppo locale seguente per consentire l'accesso alla funzionalità report nel sito Web di amministrazione di MBAM.

    -   **Utenti di report mbam**: i membri di questo gruppo locale possono accedere ai report nel sito Web di amministrazione di mbam.

    **Nota**  
    L'appartenenza a un utente o un gruppo identico al gruppo locale degli **utenti del report mbam** deve essere mantenuta in tutti i computer in cui sono installate le funzionalità mbam Administration e Monitoring Server, la conformità e il database di audit e i report di conformità e controllo.



## Convalidare l'installazione delle funzionalità di MBAM server


Quando l'installazione della funzionalità di MBAM server è completa, devi verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM. Usare la procedura seguente per verificare che il servizio MBAM sia funzionante.

**Per convalidare un'installazione di MBAM**

1. In ogni server, in cui è distribuita una caratteristica di MBAM, aprire il **Pannello di controllo**, fare clic su **programmi**e quindi su **programmi e funzionalità**. Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .

   **Nota**  
   Per convalidare l'installazione di MBAM, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.



2. Nel server in cui è installato il database di ripristino e hardware, aprire SQL Server Management Studio e verificare che il database **hardware e ripristino di mbam** sia installato.

3. Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il database **dello stato di conformità di mbam** .

4. Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con privilegi amministrativi e passare alla Home page del sito di SQL Server Reporting Services.

   La posizione principale predefinita di un'istanza del sito di SQL Server Reporting Services è disponibile in http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx. Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.

   Verificare che sia elencata una cartella denominata **report di conformità Malta** e che contenga cinque report e un'origine dati.

   **Nota**  
   Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



5. Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**, selezionare **server Web (IIS)** e quindi fare clic su **Gestione Internet Information Services (IIS)**. In **connessioni** passare a * &lt; nomecomputer &gt; *, fare clic su **siti**e quindi su **amministrazione e monitoraggio di Microsoft BitLocker**. Verificare che **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.

6. Nel server in cui è installata la funzionalità di amministrazione e monitoraggio aprire un Web browser con privilegi amministrativi e passare alle posizioni seguenti nel sito Web di MBAM per verificare che vengano caricati correttamente:

   -   *http:// &lt; nomecomputer &gt; /default.aspx* e confermare ognuno dei collegamenti per gli spostamenti e i report

   -   *http:// &lt; nomecomputer &gt; /MBAMAdministrationService/AdministrationService.svc*

   -   *http:// &lt; nomecomputer &gt; /MBAMComplianceStatusService/StatusReportingService.svc*

   -   *http:// &lt; nomecomputer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc*

   **Nota**  
   In genere, i servizi vengono installati nella porta predefinita 80 senza crittografia di rete. Se i servizi sono installati in una porta diversa, modificare gli URL in modo da includere la porta appropriata. Ad esempio, http://* &lt; nomecomputer &gt; : &lt; porta &gt; */default.aspx o http:// <em> &lt; HostHeaderName &gt; / </em> default. aspx

   Se i servizi sono stati installati con la crittografia di rete, cambiare http://in https://.



~~~
Verify that each web page loads successfully.
~~~

## Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)









