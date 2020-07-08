---
title: Come installare e configurare MBAM su server distribuiti
description: Come installare e configurare MBAM su server distribuiti
author: dansimp
ms.assetid: 67b91e6b-ae2e-4e47-9ef2-6819aba95976
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 841b894430d14604f0fd923703708d7a3f588c07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824056"
---
# Come installare e configurare MBAM su server distribuiti


Le procedure descritte in questo argomento descrivono come installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 nella topologia autonoma nei server distribuiti. Per visualizzare un diagramma dell'architettura consigliata, insieme a una descrizione dei database e delle caratteristiche, vedere [distribuzione dell'infrastruttura del server MBAM 2,0](deploying-the-mbam-20-server-infrastructure-mbam-2.md). Per installare l'amministrazione e il monitoraggio di Microsoft BitLocker con la topologia di Configuration Manager, vedere [distribuzione di mbam con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).

Ogni funzionalità del server ha alcuni prerequisiti. Per verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). Alcune funzionalità richiedono inoltre di specificare determinate informazioni durante il processo di installazione per la distribuzione corretta della funzionalità. Devi anche rivedere la [pianificazione per la distribuzione di mbam 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md) prima di avviare la distribuzione di mbam.

**Nota**  
Per ottenere i file di log della configurazione, è necessario usare il pacchetto msiexec e **/L** l' &lt; &gt; opzione di posizione/l per installare mbam. I file di log vengono creati nella posizione specificata.

I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% nel server dell'utente che sta installando MBAM.



## <a href="" id="deploying-mbam-server-features-"></a>Distribuzione delle funzionalità di MBAM server


I passaggi seguenti descrivono come installare le caratteristiche generali di MBAM.

**Per avviare l'installazione guidata di MBAM server**

1.  Nel server in cui si vuole installare l'amministrazione e il monitoraggio di Microsoft BitLocker, eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.

2.  Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** **selezionare la topologia autonoma** e quindi fare clic su **Avanti**.

    **Nota**  
    Se si vuole installare MBAM con la topologia integrata di Configuration Manager, vedere la pagina relativa alla [distribuzione di mbam con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md).



5.  Selezionare le caratteristiche che si desidera installare. Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione. Deselezionare le caratteristiche che si desidera installare altrove. Le caratteristiche che verranno installate nello stesso computer devono essere installate contemporaneamente. È necessario installare le caratteristiche di MBAM nell'ordine seguente:

    -   Database di ripristino

    -   Database di conformità e controllo

    -   Report di conformità e controllo

    -   Portale self-service

    -   Server di amministrazione e monitoraggio

    -   Modello di criteri di gruppo di MBAM

    **Nota**  
    La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti. Se tutti i prerequisiti sono soddisfatti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.



~~~
The MBAM Setup wizard displays installation pages for the features that you select. The following sections describe the installation procedures for each feature.

**Note**  
For the following instructions, it is assumed that each feature is to be installed on a separate server. If you install multiple features on a single server, you can change or eliminate some steps.
~~~



**Per installare il database di ripristino**

1.  Nella pagina **Configura database di ripristino** specificare i nomi dei computer in cui verrà eseguita la funzionalità di amministrazione e monitoraggio Server. Dopo la distribuzione della funzionalità di amministrazione e monitoraggio del server, usa il proprio account di dominio per connettersi al database.

2.  Fai clic su **Next** per continuare.

3.  Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino. È inoltre necessario specificare sia la posizione in cui si trova il database, sia dove verranno individuate le informazioni sul log.

4.  Fare clic su **Avanti** per continuare con la configurazione guidata di mbam.

**Per installare il database di conformità e controllo**

1.  Nella pagina **Configura il database di conformità e controllo** specificare l'account utente che verrà usato per accedere al database per i report.

2.  Specificare i nomi di computer dei computer in cui verranno eseguiti il server di amministrazione e monitoraggio e i report di conformità e controllo. Una volta distribuiti l'amministrazione e il monitoraggio e il server dei report di conformità e controllo, questi usano gli account di dominio per connettersi ai database.

    **Nota**  
    Se si sta installando il database di conformità e controllo senza la caratteristica conformità e rapporti di controllo, è necessario aggiungere un'eccezione nel computer di database di conformità e controllo per abilitare il traffico in ingresso nella porta di Microsoft SQL Server. Il numero di porta predefinito è 1433.



3.  Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di conformità e controllo. Devi anche specificare la posizione in cui verranno individuate le informazioni sul database e sul log.

4.  Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

**Per installare i report di conformità e controllo**

1.  Nella pagina **configura report di conformità e controllo** specificare il nome dell'istanza di SQL Server remoto, ad esempio nomeserver, in &lt; &gt; cui è stato installato il database di conformità e controllo.

    **Nota**  
    Se si installano i report di conformità e controllo senza il server di amministrazione e monitoraggio, è necessario aggiungere un'eccezione nel computer del report di conformità e controllo per abilitare il traffico in ingresso nella porta del server di report (la porta predefinita è 80).



2.  Specificare il nome del database di conformità e controllo. Per impostazione predefinita, il nome del database è lo stato di conformità di MBAM, anche se è possibile modificare il nome quando si installa il database di conformità e controllo.

3.  Fai clic su **Next** per continuare.

4.  Selezionare l'istanza di SQL Server Reporting Services in cui verranno installati i report di conformità e controllo. Specificare un account utente di dominio e una password per accedere al database di conformità e controllo. Configurare la password per l'account per non scadere mai. L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.

5.  Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

**Per installare il portale self-service**

1.  Nella pagina **Configura il portale self-service** è possibile facoltativamente crittografare la comunicazione tra il portale self-service e i server di amministrazione e monitoraggio. Se si sceglie l'opzione per crittografare la comunicazione, viene chiesto di selezionare il certificato di provisioning dell'autorità di certificazione da usare per la crittografia.

2.  Fai clic su **Next** per continuare.

3.  Specificare l'istanza remota di SQL Server, ad esempio * &lt; NomeServer &gt; *, in cui è stato installato il database di conformità e controllo.

4.  Specificare il nome del database di conformità e controllo. Per impostazione predefinita, il nome del database è lo stato di conformità di MBAM. È tuttavia possibile modificare il nome quando si installa il database di conformità e controllo.

5.  Fai clic su **Next** per continuare.

6.  Specificare l'istanza remota di SQL Server, ad esempio * &lt; NomeServer &gt; *, in cui è stato installato il database di ripristino.

7.  Specificare il nome del database di ripristino. Per impostazione predefinita, il nome del database è **mbam Recovery and hardware**. È tuttavia possibile modificare il nome durante l'installazione della caratteristica del database di ripristino.

8.  Fai clic su **Next** per continuare.

9.  Immettere il **numero di porta**, il **nome host** (facoltativo) e il **percorso di installazione** per l'amministrazione e il server di monitoraggio di mbam.

    **Nota**  
    Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco. Se si usa Windows Firewall, la porta verrà aperta automaticamente.



10. Per registrare facoltativamente un nome dell'entità servizio (SPN) per il portale self-service, selezionare **registra SPN (Service Principal Name) di questo computer con Active Directory (obbligatorio per l'autenticazione di Windows)**. Se si seleziona questa casella di controllo, MBAM Setup non tenterà di registrare i nomi SPN esistenti ed è possibile registrare manualmente l'SPN prima o dopo l'installazione di MBAM. Per istruzioni su come registrare manualmente l'SPN, vedere [registrazione manuale di SPN](https://go.microsoft.com/fwlink/?LinkId=286758).

11. Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

12. Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.

13. Quando le informazioni della caratteristica MBAM selezionato sono completate, si è pronti per avviare l'installazione di MBAM usando la configurazione guidata. Fare clic su **Torna** per spostarsi nella procedura guidata se è necessario rivedere o modificare le impostazioni di installazione. Fare clic su **Installa** per avviare l'installazione. Fare clic su **Annulla** per chiudere la procedura guidata. Il programma di installazione installa le caratteristiche di MBAM selezionate e informa che l'installazione è terminata.

14. Fare clic su **fine** per chiudere la procedura guidata.

    **Nota**  
    Per configurare il portale self-service dopo averlo installato, personalizzare il portale self-service con il nome della società e altre informazioni specifiche della società, vedere [come personalizzare il portale self-service](how-to-brand-the-self-service-portal.md) per le istruzioni.



15. Se i computer client hanno accesso alla rete di distribuzione dei contenuti Microsoft (CDN), che fornisce al portale self-service l'accesso necessario a determinati file JavaScript, è stata completata l'installazione del portale self-service. Se i computer client non hanno accesso alla rete CDN Microsoft, completare i passaggi della sezione successiva per configurare il portale self-service in modo che faccia riferimento ai file JavaScript da un'origine accessibile.

**Per configurare il portale self-service quando gli utenti finali non riescono ad accedere alla rete di distribuzione dei contenuti Microsoft**

1. Se i computer client hanno accesso alla rete di distribuzione dei contenuti Microsoft (CDN), che fornisce al portale self-service l'accesso necessario a determinati file JavaScript, viene completata l'installazione del portale self-service. Se i computer client non hanno accesso alla rete CDN Microsoft, completare i passaggi rimanenti in questa sezione per configurare il portale self-service in modo che faccia riferimento ai file JavaScript da un'origine accessibile.

2. Scaricare i quattro file JavaScript da Microsoft CDN:

   -   jQuery-1.7.2.min.js-[https://go.microsoft.com/p/fwlink/?LinkID=271736](https://go.microsoft.com/fwlink/p/?LinkID=271736)

   -   MicrosoftAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272283](https://go.microsoft.com/fwlink/p/?LinkId=272283)

   -   MicrosoftMvcAjax.js-[https://go.microsoft.com/p/fwlink/?LinkId=272284](https://go.microsoft.com/fwlink/p/?LinkId=272284)

   -   MicrosoftMvcValidation.js- <https://go.microsoft.com/fwlink/p/?LinkId=272285>

3. Copiare i file JavaScript nella directory **Scripts** del portale self-service. Questa directory si trova in <em> &lt; mbam self-service install directory &gt; \\ </em> self service Website\\Scripts.

4. Aprire **Gestione Internet Information Services (IIS)**.

5. Espandere i **siti** &gt; **di amministrazione e monitoraggio di Microsoft BitLocker**ed evidenziare **selfservice**.

   **Nota**  
   *Selfservice* è il nome della directory virtuale predefinita. Se si è scelto un nome diverso per questa directory durante l'installazione, ricordarsi di sostituire *selfservice* nelle rimanenti istruzioni con il nome scelto.



6. Nel riquadro centrale fare doppio clic su **Impostazioni applicazione**.

7. Per ogni elemento dell'elenco seguente modificare le impostazioni dell'applicazione per fare riferimento alla nuova posizione sostituendo &lt; directory virtuale &gt; con/selfservice/(o il nome scelto durante l'installazione). Il percorso della directory virtuale, ad esempio, sarà simile a/selfservice/scripts/jquery-1.7.2.min.js.

   -   jQueryPath:/ &lt; directory virtuale &gt; /script/jQuery-1.7.2.min.js

   -   MicrosoftAjaxPath:/ &lt; directory virtuale &gt; /script/MicrosoftAjax.js

   -   MicrosoftMvcAjaxPath:/ &lt; directory virtuale &gt; /script/MicrosoftMvcAjax.js

   -   MicrosoftMvcValidationPath:/ &lt; directory virtuale &gt; /script/MicrosoftMvcValidation.js

**Per installare la funzionalità di amministrazione e monitoraggio del server**

1. MBAM può crittografare le comunicazioni tra i servizi Web e i server di amministrazione e monitoraggio. Se si sceglie l'opzione per crittografare la comunicazione, viene chiesto di selezionare il certificato di provisioning dell'autorità di certificazione da usare per la crittografia.

2. Fai clic su **Next** per continuare.

3. Specificare l'istanza remota di SQL Server, ad esempio * &lt; NomeServer &gt; *, in cui è stato installato il database di conformità e controllo.

4. Specificare il nome del database di conformità e controllo. Per impostazione predefinita, il nome del database è lo stato di conformità di MBAM. È tuttavia possibile modificare il nome quando si installa il database di conformità e controllo.

5. Fai clic su **Next** per continuare.

6. Specificare l'istanza remota di SQL Server, ad esempio * &lt; NomeServer &gt; *, in cui è stato installato il database di ripristino.

7. Specificare il nome del database di ripristino. Per impostazione predefinita, il nome del database è **mbam Recovery and hardware**. È tuttavia possibile modificare il nome durante l'installazione della caratteristica del database di ripristino.

8. Fai clic su **Next** per continuare.

9. Specificare l'URL per la "Home" del sito di SQL Server Reporting Services (SRS). La posizione principale predefinita di un'istanza del sito di SQL Server Reporting Services è:

   http:// <em> &lt; NameofMBAMReportsServer &gt; / </em> ReportServer

   **Nota**  
   Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL è simile al seguente: http://* &lt; NameofMBAMReportsServer &gt; */ReportServer\_* &lt; SRSInstanceName &gt; *.



10. Fai clic su **Next** per continuare.

11. Immettere il **numero di porta**, il **nome host** (facoltativo) e il **percorso di installazione** per l'amministrazione e il server di monitoraggio di mbam.

    **Nota**  
    Il numero di porta specificato deve essere un numero di porta non usato nel server di amministrazione e monitoraggio, a meno che non venga specificato un nome di intestazione host univoco. Se si usa Windows Firewall, la porta verrà aperta automaticamente.



12. Per registrare facoltativamente un nome dell'entità servizio (SPN) per il portale self-service, selezionare **registra SPN (Service Principal Name) di questo computer con Active Directory (obbligatorio per l'autenticazione di Windows)**. Se si seleziona questa casella di controllo, MBAM Setup non tenterà di registrare i nomi SPN esistenti ed è possibile registrare manualmente l'SPN prima o dopo l'installazione di MBAM. Per istruzioni su come registrare manualmente l'SPN, vedere [registrazione manuale di SPN](https://go.microsoft.com/fwlink/?LinkId=286758).

13. Fare clic su **Avanti** per continuare con la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

14. Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**.

15. Quando le informazioni della caratteristica MBAM selezionato sono completate, si è pronti per avviare l'installazione di MBAM usando la configurazione guidata. Fare clic su **Torna** per spostarsi nella procedura guidata se è necessario rivedere o modificare le impostazioni di installazione. Fare clic su **Installa** per eseguire l'installazione. Fare clic su **Annulla** per chiudere la procedura guidata. Il programma di installazione installa le caratteristiche di MBAM selezionate e informa che l'installazione è terminata.

16. Fare clic su **fine** per chiudere la procedura guidata.

**Per eseguire la configurazione post-installazione**

1.  Nel server di amministrazione e monitoraggio aggiungere utenti ai gruppi locali seguenti per consentire loro di accedere alle funzionalità del sito Web di amministrazione e monitoraggio di MBAM.

    -   **Utenti di mbam helpdesk**: i membri di questo gruppo locale possono accedere al recupero delle unità e gestire le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam. Tutti i campi in recupero unità e Gestisci TPM sono campi obbligatori per un utente dell'helpdesk.

    -   **Mbam Advanced helpdesk utenti**: i membri di questo gruppo locale hanno accesso avanzato al ripristino delle unità e gestiscono le caratteristiche del TPM nel sito Web di amministrazione e monitoraggio di mbam. Per gli utenti di helpdesk avanzati, è necessario solo il campo ID chiave in recupero unità. In **Manage TPM**sono necessari solo il campo **computer Domain** e il **nome computer** .

2.  Nel server che ospita il server di amministrazione e monitoraggio e il database di conformità e controllo e nel server che ospita i report di conformità e controllo, aggiungere utenti al gruppo locale seguente per consentire loro l'accesso alla funzionalità report nel sito Web di amministrazione e monitoraggio di MBAM.

    -   **Utenti di report mbam**: i membri di questo gruppo locale possono accedere ai report nel sito Web di amministrazione e monitoraggio di mbam.

    **Nota**  
    L'appartenenza a un utente o un gruppo identico al gruppo locale degli **utenti del report mbam** deve essere mantenuta in tutti i computer in cui sono installate le funzionalità mbam Administration e Monitoring Server, la conformità e il database di audit e i report di conformità e controllo.



## Convalida dell'installazione della funzionalità di MBAM server


Quando l'installazione delle funzionalità di amministrazione e monitoraggio di Microsoft BitLocker è stata completata, è consigliabile verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM. Usare la procedura seguente per verificare che il servizio di amministrazione e monitoraggio di Microsoft BitLocker sia funzionale.

**Per convalidare un'installazione di MBAM server**

1. In ogni server in cui è distribuita una caratteristica di MBAM, aprire il **Pannello di controllo**, selezionare **programmi**e quindi selezionare **programmi e funzionalità**. Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .

   **Nota**  
   Per convalidare l'installazione di MBAM, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.



2. Nel server in cui è installato il database di ripristino, aprire SQL Server Management Studio e verificare che il database **di ripristino e hardware di mbam** sia installato.

3. Nel server in cui è installato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia installato il **database dello stato di conformità di mbam** .

4. Nel server in cui sono installati i report di conformità e controllo, aprire un Web browser con credenziali amministrative e passare alla Home page del sito di SQL Server Reporting Services.

   La posizione Home predefinita di un'istanza del sito di SQL Server Reporting Services è disponibile all'indirizzo http:// <em> &lt; NameofMBAMReportsServer &gt; </em> /Reports.aspx. Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.

   Verificare che una cartella report denominata **amministrazione e monitoraggio di Microsoft BitLocker** contenga un'origine dati denominata **MaltaDataSource** e che una cartella **en-US** contenga quattro report.

   **Nota**  
   Se SQL Server Reporting Services è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http://* &lt; NameofMBAMReportsServer &gt; */Reports\_* &lt; SRSInstanceName &gt; *



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring website and select a report, the following message appears: “Only Secure Content is Displayed.” To show the report, click **Show All Content**.
~~~



5. Nel server in cui è installata la funzionalità di amministrazione e monitoraggio eseguire **Server Manager** e passare a **ruoli**. Selezionare **server Web (IIS)** e quindi fare clic su **Gestione Internet Information Services (IIS)**.

6. In **connessioni**passare a * &lt; nomecomputer &gt; *, selezionare **siti**e selezionare **amministrazione e monitoraggio di Microsoft BitLocker**. Verificare che **MBAMAdministrationService**, **MBAMComplianceStatusService**e **MBAMRecoveryAndHardwareService** siano elencati.

7. Nel server in cui sono installate le funzionalità di amministrazione e monitoraggio e il portale self-service, aprire un Web browser con credenziali amministrative e individuare le posizioni seguenti per verificare che vengano caricate correttamente.

   **Nota**  
   Gli URL che terminano con ". svc" non visualizzano un sito Web. Il successo è indicato dal messaggio "la pubblicazione dei metadati per questo servizio è attualmente disabilitata" o dal codice simile alle informazioni. Se viene visualizzato un altro messaggio di errore o se non è possibile trovare la pagina, la pagina non è stata caricata correttamente.



~~~
-   *http://&lt;hostname&gt;/HelpDesk/default.aspx* and confirm each of the links for navigation and reports

-   *http://&lt;hostname&gt;/SelfService&gt;/*

-   *http://&lt;computername&gt;/MBAMAdministrationService/AdministrationService.svc*

-   *http://&lt;hostname&gt;/MBAMUserSupportService/UserSupportService.svc*

-   *http://&lt;computername&gt;/MBAMComplianceStatusService/StatusReportingService.svc*

-   *http://&lt;computername&gt;/MBAMRecoveryAndHardwareService/CoreService.svc*

**Note**  
It is assumed that the server features were installed on the default port without network encryption. If you installed the server features on a different port or virtual directory, change the URLs to include the appropriate port, for example, *http://&lt;hostname&gt;:&lt;port&gt;/HelpDesk/default.aspx* or*http://&lt;hostname&gt;:&lt;port&gt;/&lt;virtualdirectory&gt;/default.aspx*

If the server features were installed with network encryption, change http:// to https://.
~~~



8. Verificare che ogni pagina venga caricata correttamente.

## Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









