---
title: Distribuzione di MBAM 2.5 in una configurazione autonoma
description: Introduzione alla distribuzione di MBAM 2,5 in una configurazione autonoma.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 905eb7a40483a7a7b499d6dced8472331c87b838
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826435"
---
# Distribuzione di MBAM 2,5 in una configurazione autonoma

Questo articolo fornisce istruzioni dettagliate per l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 in una configurazione autonoma. In questa guida verrà usata una configurazione a due server. Uno dei due server sarà un server di database che utilizza Microsoft SQL Server 2012. Questo server ospiterà i database e i report di MBAM. Il server aggiuntivo sarà un server Web di Windows Server 2012 che ospita "Administration and Monitoring Server" e "Self-Service Portal".

## Procedura per la preparazione prima di installare il software MBAM 2,5 Server

### Passaggio 1: installazione e configurazione dei server

Prima di iniziare a configurare MBAM 2,5, dobbiamo assicurarci che entrambi i server siano configurati secondo i requisiti di sistema di MBAM. Vedere i [requisiti di sistema di mbam Minimum](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)e selezionare una configurazione che soddisfi questi requisiti. 

#### Passaggio 1,1: distribuzione dei prerequisiti per il database e il server di report

1. Installare e configurare un server che utilizza il sistema operativo Windows Server 2008 R2 (o versioni successive).

2. Installare Windows PowerShell 3,0.

3. Installare Microsoft SQL Server 2008 R2 o una versione successiva che include il Service Pack più recente. Se si sta installando una nuova istanza di SQL Server per MBAM, verificare che l'installazione di SQL Server includa le regole di confronto SQL_Latin1_General_CP1_CI_AS. È necessario installare le funzionalità di SQL Server seguenti:

    * Motore di database
    * Reporting Services
    * Connettività degli strumenti client
    * Strumenti di gestione-completamento

    > [!Note]
    > Facoltativamente, è anche possibile installare la [funzionalità di crittografia dati trasparente (Transparent Data Encryption) in SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).

    SQL Server Reporting Services deve essere installato e configurato in modalità "nativa" e non in modalità non configurata o "SharePoint".

    ![Funzionalità di SQL Server necessarie](images/deploying-MBAM-1.png)

4. Se si prevede di usare SSL per il sito Web di amministrazione e monitoraggio, verificare di aver configurato SQL Server Reporting Services (SSRS) in modo da usare il protocollo SSL (Secure Sockets Layer) prima di configurare il sito Web di amministrazione e monitoraggio. In caso contrario, la caratteristica report utilizzerà il trasporto dati non crittografato (HTTP) anziché crittografato (HTTPS).

    È possibile seguire la [configurazione delle connessioni SSL](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) in un server di report in modalità nativa per configurare SSL nel server di report.
    
    > [!Note]
    > Per installare SQL Server, è possibile seguire la Guida all'installazione di SQL Server per la rispettiva versione di SQL Server. I collegamenti sono i seguenti:
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Nella post-installazione di SQL Server verificare che l'account utente venga provisionato in SQL Server e assegnare le autorizzazioni seguenti all'utente che configurerà il database MBAM e i ruoli di segnalazione nel server di database.

    Ruoli per l'istanza di SQL Server:
        
    * dbcreator
    * processadmin

    Diritti per l'istanza di SQL Server Reporting Services:
    
    * Creare cartelle
    * Pubblicare report

Il server di database è pronto per la configurazione dei ruoli di MBAM 2,5. Passiamo al server successivo.

#### Passaggio 1,2: distribuzione dei prerequisiti per l'amministrazione e il server di monitoraggio

Scegliere un server che soddisfi la configurazione hardware, come spiegato nel [documento dei requisiti di sistema di mbam](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements). Deve eseguire Windows Server 2008 R2 o un sistema operativo successivo insieme al Service Pack e agli aggiornamenti più recenti. Dopo aver completato il server, installare i ruoli e le caratteristiche seguenti:

##### Ruoli

* Strumenti di gestione di Web Server (IIS) (selezionare script e strumenti per la gestione di IIS).

* Servizi ruolo server Web

    * Funzionalità HTTP comuni<br />
      Contenuto statico<br />
      Documento predefinito

    * Sviluppo di applicazioni<br />
      ASP.NET<br />
      Estensibilità .NET<br />
      Estensioni ISAPI<br />
      Filtri ISAPI<br />
      Sicurezza<br />
      Autenticazione di Windows<br />
      Filtro delle richieste

    * Strumenti di gestione di IIS per servizi Web

##### Funzionalità

* Caratteristiche di .NET Framework 4,5
  
  * Microsoft .NET Framework 4,5
  
    Per Windows Server 2012 o Windows Server 2012 R2, .NET Framework 4,5 è già installato per queste versioni di Windows Server. Devi tuttavia abilitarlo.
  
    Per Windows Server 2008 R2, .NET Framework 4,5 non è incluso in Windows Server 2008 R2. È quindi necessario scaricare .NET Framework 4,5 e installarlo separatamente.
  
  * Attivazione di WCF<br />
    Attivazione HTTP<br />
    Attivazione non HTTP
  
  * Attivazione TCP
  
  * Servizio Attivazione processo Windows:<br />
    Modello di processo<br />
    Ambiente .NET Framework<br />
    API di configurazione

Per il funzionamento del portale self-service, devi anche [scaricare e installare ASP.NET MVC 4,0](https://go.microsoft.com/fwlink/?linkid=392271).

Il passaggio successivo consiste nel creare gli utenti e i gruppi di MBAM necessari in Active Directory.

### Passaggio 2: creazione di utenti e gruppi in servizi di dominio Active Directory
 
Come parte dei prerequisiti, è necessario definire determinati ruoli e account usati in MBAM per specificare i diritti di sicurezza e di accesso a server e funzionalità specifici, ad esempio i database in uso nell'istanza di SQL Server e le applicazioni Web in uso nel server di amministrazione e monitoraggio.

Creare i gruppi e gli utenti seguenti in Active Directory. Puoi usare qualsiasi nome per i gruppi e gli utenti. Gli utenti non devono avere diritti utente più grandi. Un account utente di dominio è sufficiente. È necessario specificare il nome di questi gruppi durante la configurazione di MBAM 2,5:

* **MBAMAppPool**  

  **Tipo**: utente di dominio

  **Descrizione**: utente di dominio che ha l'autorizzazione di lettura o scrittura per il database di conformità e controllo e il database di ripristino per consentire alle applicazioni Web di accedere ai dati e ai report in questi database. Verrà usato anche dal pool di applicazioni per le applicazioni Web.

  **Ruoli account (durante la configurazione di mbam)**:

  1. Account di dominio del pool di applicazioni Web Service

  2. Utente per la lettura e la scrittura del database di conformità e controllo e ripristino per i report

* **MBAMROUser**

  **Tipo**: utente di dominio

  **Descrizione**: utente di dominio che avrà accesso di sola lettura al database di conformità e controllo per consentire ai report di accedere ai dati di conformità e controllo in questo database. Sarà anche l'account utente di dominio usato dall'istanza di SQL Server Reporting Services locale per accedere al database di conformità e controllo.

  **Ruoli account (durante la configurazione di mbam)**:

  1. Utente di sola lettura del database di conformità e controllo per i report

  2. Account utente del dominio del database di conformità e audit

* **MBAMAdvHelpDsk**

  **Tipo**: gruppo di domini

  **Descrizione**: mbam Advanced helpdesk utenti Access Group: gruppo di utenti del dominio i cui membri hanno accesso a tutte le aree del sito Web di amministrazione e monitoraggio. Gli utenti che hanno questo ruolo devono immettere solo la chiave di ripristino, non il dominio dell'utente e il nome utente, quando aiutano gli utenti a recuperare le proprie unità. Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti dell'helpdesk avanzato MBAM eseguono l'override delle autorizzazioni di MBAM Group helpdesk.

  **Ruoli account (durante la configurazione di mbam)**: utenti di helpdesk avanzati di mbam

* **MBAMHelpDsk**

  **Tipo**: gruppo di domini

  **Descrizione**: mbam helpdesk utenti gruppo di Access: gruppo di utenti del dominio i cui membri hanno accesso alle aree di gestione TPM e unità di ripristino del sito Web di amministrazione e monitoraggio di mbam. Le persone che hanno questo ruolo devono compilare tutti i campi quando usano un'opzione qualsiasi. Questo include il dominio e il nome dell'account dell'utente.

  **Ruoli account (durante la configurazione di mbam)**: utenti dell'helpdesk di mbam

* **MBAMRUGrp**

  **Tipo**: gruppo di domini

  **Descrizione**: gruppo di utenti del dominio i cui membri hanno accesso in sola lettura ai report nell'area report del sito Web amministrazione e monitoraggio.

  **Ruoli account (durante la configurazione di mbam)**:

  1. Report di gruppo di Access per il dominio di sola lettura

  2. Gruppo di Access report MBAM utenti

### Passaggio 3 (facoltativo): configurare e installare il certificato SSL nel server di amministrazione e monitoraggio

Anche se è facoltativo, ti consigliamo vivamente di usare un certificato per proteggere la comunicazione tra il client MBAM e il sito Web di amministrazione e monitoraggio e i siti Web portale self-service. Non è consigliabile usare i certificati autofirmati a causa di ovvi motivi di sicurezza. Ti consigliamo di usare un certificato di tipo server Web da un'autorità di certificazione attendibile. A questo scopo, è possibile fare riferimento alla sezione "utilizzo di certificato approvato da autorità di certificazione" da [KB 2754259](https://support.microsoft.com/help/2754259).

Dopo l'emissione del certificato, è necessario aggiungere il certificato allo Store personale del server di amministrazione e monitoraggio. Per aggiungere il certificato, aprire l'archivio certificati nel computer locale. A tale scopo, effettua quanto segue:

1. Fare clic con il pulsante destro del mouse su Start, quindi scegliere Esegui.

   ![Selezionare ](images/deploying-MBAM-2.png)

2. Digitare "MMC.EXE" (senza virgolette) e quindi scegliere **OK**.

   ![Casella Esegui](images/deploying-MBAM-3.png) 

3. Selezionare **file** nella nuova console MMC aperta e quindi selezionare **Aggiungi/Rimuovi snap-in**.
   
   ![Selezionare](images/deploying-MBAM-4.png)

4. Evidenziare lo snap-in **certificati** e quindi fare clic su **Aggiungi**.

   ![Finestra Aggiungi o Rimuovi snap-in](images/deploying-MBAM-5.png)

5. Selezionare l'opzione **account computer** e quindi selezionare **Avanti**.
   
   ![Finestra di snap-in certificati](images/deploying-MBAM-6.png)

6. Selezionare **computer locale** nella schermata successiva e quindi selezionare **fine**.
   
   ![Selezionare finestra del computer](images/deploying-MBAM-7.png)

7. Ora è stato aggiunto lo snap-in certificati. In questo modo potrai usare qualsiasi certificato nell'archivio certificati del computer.

   ![Finestra Aggiungi o Rimuovi snap-in](images/deploying-MBAM-8.png)

8. Importare il certificato del server Web nell'archivio certificati del computer.

   Ora che si ha accesso allo snap-in certificati, è possibile importare il certificato del server Web nell'archivio certificati del computer. Per eseguire questa operazione, seguire i passaggi successivi.

9. Aprire lo snap-in certificati (computer locale) e passare a **personale** e quindi **certificati**.
   
   ![Finestra degli snap-in certificati (computer locale)](images/deploying-MBAM-9.png)

   > [!Note]
   > Lo snap-in certificati potrebbe non essere elencato. In caso contrario, non vengono installati certificati.

10. Fare clic con il pulsante destro del mouse su **certificati**, selezionare **tutte le attività**e quindi **Importa**.

    ![Finestra degli snap-in certificati (computer locale)](images/deploying-MBAM-10.png)

11. Quando viene avviata la procedura guidata, selezionare **Avanti**. Passare al file creato contenente il certificato del server e la chiave privata e quindi selezionare **Avanti**.

    ![Finestra di importazione guidata certificati](images/deploying-MBAM-11.png)

12. Immettere la password se è stata specificata una per il file al momento della creazione.

   ![Finestra Immetti password](images/deploying-MBAM-12.png)

   > [!Note]
   > Verificare che l'opzione **contrassegna la chiave come esportabile** sia selezionata se si vuole esportare di nuovo la coppia di chiavi dal computer in cui si trova. Come misura di sicurezza aggiunta, potresti voler cancellare questa opzione per verificare che nessuno possa eseguire un backup della tua chiave privata.
 
13. Selezionare **Avanti**e quindi selezionare l' **archivio certificati** a cui si vuole salvare il certificato.

    ![Finestra di importazione guidata certificati](images/deploying-MBAM-13.png)

    > [!Note]
    > È necessario selezionare **personale**, perché si tratta di un certificato del server Web. Se è stato incluso il certificato nella gerarchia di certificazione, verrà aggiunto anche allo Store.
 
14. Selezionare **Avanti**, quindi selezionare **fine**.

    ![Finestra di importazione guidata certificati](images/deploying-MBAM-14.png)

Si vedrà ora il certificato server per il server Web nell'elenco certificati personali. Verrà indicato con il nome comune del server. Puoi trovarlo nella sezione oggetto del certificato.

Per altre informazioni di riferimento:

[Considerazioni sulla sicurezza per MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Pianificazione di come proteggere i siti Web di MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Il passaggio successivo consiste nel registrare un nome di principio del servizio per l'account del pool di applicazioni.

### Passaggio 4: configurazione del certificato SSL per MBAM Web Server

Se si usa la comunicazione SSL tra il client e il server, è necessario assicurarsi che il certificato disponga di OID (1.3.6.1.5.5.7.3.1) e (1.3.6.1.5.5.7.3.2). Occorre quindi verificare che l'autenticazione del server e l'autenticazione del client vengano aggiunte.

Se si riceve un errore di certificato quando si tenta di esplorare gli URL del servizio, si usa un certificato emesso con un nome diverso oppure si sta navigando usando un URL non corretto.

Anche se il browser può richiedere un messaggio di errore del certificato ma consente di continuare, il servizio Web MBAM non ignorerà gli errori del certificato e bloccherà la connessione. Noterai gli errori relativi ai certificati nel log eventi dell'amministratore del client MBAM. Se si usa un alias per connettersi al server di amministrazione e monitoraggio, è necessario emettere un certificato per il nome dell'alias. Il nome dell'oggetto del certificato deve quindi essere il nome dell'alias e il nome DNS del server locale deve essere aggiunto al campo **nome alternativo oggetto** del certificato.

Esempio:

Se il nome virtuale è "bitlocker.contoso.com" e il nome del server di amministrazione e monitoraggio di MBAM è "adminserver.contoso.com", il certificato deve essere emesso in bitlocker.contoso.com (nome soggetto) e adminserver.contoso.com deve essere aggiunto al campo **nome alternativo soggetto** del certificato.

Analogamente, se sono installati più server di amministrazione e monitoraggio per bilanciare il carico usando un bilanciamento del carico, è necessario emettere il certificato SSL nel nome virtuale. Il campo nome oggetto del certificato deve avere il nome virtuale e i nomi di tutti i server locali devono essere aggiunti nel campo **nome alternativo oggetto** del certificato.

Esempio:

Se il nome virtuale è "bitlocker.contoso.com" e i server sono "adminserver1.contoso.com" e "adminiserver2.contoso.com", il certificato deve essere emesso in bitlocker.contoso.com (nome soggetto) e adminserver1.contoso.com e adminiserver2.contoso.com deve essere aggiunto al campo **nome alternativo oggetto** del certificato.

I passaggi per configurare la comunicazione SSL tramite MBAM sono descritti nell'articolo della Knowledge Base seguente: [KB 2754259](https://support.microsoft.com/help/2754259).

### Passaggio 5: registrare i nomi SPN per l'account del pool di applicazioni e configurare la delega vincolata

> [!Note]
> La delega vincolata è necessaria solo per 2,5 e non è obbligatoria per 2,5 Service Pack 1 e versioni successive.

Per consentire ai server MBAM di autenticare le comunicazioni dal sito Web di amministrazione e monitoraggio e dal portale self-service, è necessario registrare un nome dell'entità servizio (SPN) per il nome host sotto l'account di dominio in uso per il pool di applicazioni Web. L'articolo seguente contiene istruzioni dettagliate per la registrazione dei nomi SPN: [pianificare come proteggere i siti Web di mbam](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Dopo avere configurato l'SPN, è necessario configurare la delega vincolata per l'SPN. A tale scopo, effettua quanto segue:

1. Passa a Active Directory e trova le credenziali del pool di app configurate per i siti Web di MBAM nei passaggi precedenti.

2. Fare clic con il pulsante destro del mouse sulle credenziali e quindi scegliere **Proprietà**.

3. Selezionare la scheda **delega** .

4. Selezionare l'opzione per l'autenticazione Kerberos.

5. Selezionare **Sfoglia**e cercare di nuovo le credenziali del pool di app. Dovresti quindi vedere tutti i nomi SPN configurati nell'account del pool di app creds. (L'SPN deve essere simile a "http/BitLocker. FQDN. com"). Evidenziare l'SPN che corrisponde al nome host specificato durante l'installazione di MBAM.

6. Seleziona **OK**.

Ora sei bravo con i prerequisiti. Nei passaggi successivi verrà installato il software MBAM nei server e configurarlo.

## Installazione e configurazione di MBAM 2,5 Server software

### Passaggio 6: installare il software MBAM 2,5 Server 

Per installare il software MBAM server utilizzando la configurazione guidata di amministrazione e monitoraggio di Microsoft BitLocker sia nel server di database che in Administration and Monitoring Server, eseguire la procedura seguente.

1. Nel server in cui si vuole installare MBAM eseguire MBAMserversetup.exe per avviare la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.

2. Nella pagina di benvenuto selezionare **Avanti**.

3. Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4. Decidere se usare Microsoft Update quando si verificano gli aggiornamenti e quindi selezionare **Avanti**.

5. Decidere se partecipare al programma Analisi utilizzo software e quindi selezionare **Avanti**.

6. Per avviare l'installazione, selezionare **Installa**.

7. Per configurare le caratteristiche del server dopo l'installazione del software MBAM server, selezionare la casella di controllo **Esegui la configurazione del server mbam dopo la chiusura della procedura guidata** . In alternativa, è possibile configurare MBAM in seguito usando il collegamento di **configurazione del server mbam** creato dall'installazione del server nel menu **Start** .

8. Selezionare **fine**.

Per altre informazioni, vedere [installazione del software server MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

### Passaggio 7: configurare il database MBAM 2,5 e il ruolo report

In questo passaggio verranno configurati i database di MBAM 2,5 e il componente di Reporting tramite MBAM Wizard:

1. Configurare il database di conformità e controllo e il database di ripristino tramite la procedura guidata:
   
   1. Nel server in cui si vogliono configurare i database avviare la **Configurazione guidata del server mbam**. Per aprire la procedura guidata, è possibile selezionare la **configurazione di mbam server** nel menu **Start** .

   2. Selezionare **Aggiungi nuove funzionalità**, selezionare **database di conformità e controllo**, **database di ripristino e report**e quindi selezionare **Avanti**. La procedura guidata controlla che siano soddisfatti tutti i prerequisiti per i database.

   3. Se il controllo dei prerequisiti è riuscito, selezionare **Avanti** per continuare. In caso contrario, risolvere i prerequisiti mancanti e quindi selezionare di **nuovo Controlla prerequisiti**.
   
   4. Usando le descrizioni seguenti, immettere i valori dei campi nella procedura guidata:

2. Database di conformità e controllo

   |Campo   |Descrizione|
   |-------|-------|
   |Nome di SQL Server |Nome del server in cui si sta configurando il database di conformità e controllo. <br /> È necessario aggiungere un'eccezione nel computer di database di conformità e controllo per abilitare il traffico in ingresso in ingresso nella porta di SQL Server. Il numero di porta predefinito è 1433.|
   |Istanza di database di SQL Server    |Nome dell'istanza del database in cui verranno archiviati i dati di conformità e controllo. Se si usa l'istanza predefinita, è necessario lasciarlo vuoto. Devi anche specificare la posizione in cui verranno individuate le informazioni sul database.|
   |Nome database   |Nome del database in cui verranno archiviati i dati di conformità. È necessario prendere nota del nome del database che si sta specificando qui, perché sarà necessario specificare queste informazioni nei passaggi successivi.|
   |Utente o gruppo di dominio delle autorizzazioni di lettura/scrittura  |Specificare il nome dell'utente di MBAMAppPool configurato nel passaggio 2.|
   |Utente o gruppo di dominio di Access di sola lettura   |Specificare il nome dell'utente di MBAMROUser configurato nel passaggio 2.|

3. Database di ripristino.

   |Campo   |Descrizione|
   |-----|-----|
   |Nome di SQL Server |Nome del server in cui si sta configurando il database di ripristino. È necessario aggiungere un'eccezione nel computer del database di ripristino per abilitare il traffico in ingresso in ingresso nella porta di SQL Server. Il numero di porta predefinito è 1433.|
   |Istanza di database di SQL Server    |Nome dell'istanza del database in cui verranno archiviati i dati di ripristino. Se si usa l'istanza predefinita, è necessario lasciarlo vuoto. Devi anche specificare la posizione in cui verranno individuate le informazioni sul database.|
   |Nome database   |Nome del database in cui verranno archiviati i dati di ripristino.|
   |Utente o gruppo di dominio delle autorizzazioni di lettura/scrittura  |Utente o gruppo di dominio che ha l'autorizzazione di lettura/scrittura per il database per consentire alle applicazioni Web di accedere ai dati e ai report in questo database. <br />Se si immette un utente in questo campo, deve essere lo stesso valore del campo account del pool di **applicazioni Web Service** nella pagina **Configura applicazioni Web** . <br />Se si immette un gruppo in questo campo, il valore nel campo **account di dominio del pool di applicazioni del servizio Web** nella pagina **Configura applicazioni Web** deve essere un membro del gruppo immesso in questo campo.|
   
   Dopo aver completato le voci, selezionare **Avanti**. La procedura guidata controlla che siano soddisfatti tutti i prerequisiti per i database.
   
   Se il controllo dei prerequisiti è riuscito, selezionare **Avanti** per continuare. In caso contrario, risolvere eventuali prerequisiti mancanti e quindi fare di nuovo clic su **Avanti** .

4. Rapporti.

   |Campo   |Descrizione|
   |----|----|
   |Istanza di SQL Server Reporting Services  |Istanza di SQL Server Reporting Services in cui verranno configurati i report. Se si usa l'istanza predefinita, è necessario lasciarlo vuoto.|
   |Gruppo di Domain Role Reporting |Specificare il nome del MBAMRUGrp come indicato nel passaggio 2.|
   |Nome di SQL Server |Nome del server in cui è configurato il database di conformità e controllo.|
   |Istanza di database di SQL Server    |Nome dell'istanza del database in cui sono configurati i dati di conformità e controllo. Se si usa l'istanza predefinita, è necessario lasciarlo vuoto. <br />È necessario aggiungere un'eccezione nel computer report per abilitare il traffico in ingresso nella porta del server di report. (La porta predefinita è 80).|
   |Nome database|  Nome del database di conformità e controllo. Per impostazione predefinita, il nome del database è lo stato di conformità di MBAM.|
   |Account di dominio del database di conformità e audit    |Specificare il nome dell'utente di MBAMROUser configurato nel passaggio 2.|
   
   Dopo aver completato le voci, selezionare **Avanti**. La procedura guidata controlla che siano soddisfatti tutti i prerequisiti per la caratteristica report. Seleziona Avanti per continuare. Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.
   
   Per altre informazioni, vedere l'articolo seguente: [come configurare i database di MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### Passaggio 8: configurare il ruolo delle applicazioni Web MBAM 2,5

1. Nel server in cui si vogliono configurare le applicazioni Web, avviare la configurazione guidata di MBAM server. Per aprire la procedura guidata, è possibile selezionare la **configurazione di mbam server** nel menu **Start** .

2. Selezionare **Aggiungi nuove funzionalità**, selezionare **amministrazione e monitoraggio sito Web** e **portale self-service**, quindi scegliere **Avanti**. La procedura guidata controlla che siano soddisfatti tutti i prerequisiti per i database.

3. Se il controllo dei prerequisiti è riuscito, selezionare **Avanti** per continuare. In caso contrario, risolvere i prerequisiti mancanti e quindi selezionare di **nuovo Controlla prerequisiti**.

4. Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata.

   |Campo   |Descrizione|
   |-----|-----|
   |Certificato di sicurezza    |Selezionare un certificato creato in precedenza nel passaggio 3 per crittografare facoltativamente la comunicazione tra i servizi Web e il server in cui si sta configurando il sito Web di amministrazione e monitoraggio. Se si seleziona non usare un certificato, la comunicazione web potrebbe non essere sicura.|
   |Nome dell'host   |Nome del computer host in cui si sta configurando il sito Web di amministrazione e monitoraggio. <br />Non deve essere il nome host della macchina, ma potrebbe essere qualsiasi cosa. Tuttavia, se l'hostname è diverso dal nome NetBIOS del computer, è necessario creare un record A e verificare che l'SPN usi il nome host personalizzato, non quello NetBIOS. Questa operazione è comune sugli scenari di bilanciamento del carico.|
   |Percorso di installazione   |Percorso in cui si sta installando il sito Web di amministrazione e monitoraggio.|
   |Port    |Numero di porta da usare per la comunicazione tramite sito Web. <br /> Per abilitare le comunicazioni tramite la porta specificata, è necessario impostare un'eccezione del firewall.|
   |Account di dominio e password del pool di applicazioni Web Service    |Specificare l'account utente e la password dell'utente di MBAMAppPool come configurato nel passaggio 2. <br /> Per una maggiore sicurezza, imposta l'account specificato nelle credenziali per avere diritti utente limitati. Imposta inoltre la password dell'account su non scadono mai.|

5. Verificare che l'account predefinito IIS_IUSRS o l'account del pool di applicazioni sia stato aggiunto al **client** di rappresentazioni dopo l'autenticazione e le impostazioni di sicurezza locali del **processo di accesso come batch** .

   Per verificare se l'account è stato aggiunto alle impostazioni di sicurezza locali, aprire l' **Editor criteri di sicurezza locali**, espandere il nodo **criteri locali** , selezionare il nodo **assegnazione diritti utente** e fare doppio clic su **rappresenta un client dopo l'autenticazione** e **accedere come criteri processo batch** nel riquadro di destra.

6. Usare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di conformità e controllo.
   |Campo   |Descrizione|
   |------|------|
   |Nome di SQL Server |Nome del server in cui è configurato il database di conformità e controllo.|
   |Istanza di database di SQL Server    |Nome dell'istanza di SQL Server, ad esempio, \<Server Name\> e in cui è configurato il database di conformità e controllo. Se si usa l'istanza predefinita, lasciarlo vuoto.|
   |Nome database   |Nome del database di conformità e controllo. Per impostazione predefinita, è "stato di conformità di MBAM".|

7. Usare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di ripristino.
   |Campo   |Descrizione|
   |----|----|
   |Nome di SQL Server |Nome del server in cui è configurato il database di ripristino.|
   |Istanza di database di SQL Server    |Nome dell'istanza di SQL Server, ad esempio, \<Server Name\> in cui è configurato il database di ripristino. Se si usa l'istanza predefinita, lasciarlo vuoto.|
   |Nome database   |Nome del database di ripristino. Per impostazione predefinita, è "MBAM Recovery and hardware".|

8. Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata per configurare il sito Web di amministrazione e monitoraggio.
   |Campo   |Descrizione|
   |----|----|
   |Gruppo di domini del ruolo Advanced helpdesk |Specificare il nome del gruppo MBAMAdvHelpDsk configurato nel passaggio 2.|
   |Gruppo di domini del ruolo helpdesk  |Specificare il nome del gruppo MBAMHelpDsk configurato nel passaggio 2.|
   |Usare l'integrazione di System Center Configuration Manager |Selezionare questa casella di controllo per deselezionarla.     |
   |Gruppo di Domain Role Reporting |Specificare il nome del gruppo MBAMRUGrp configurato nel passaggio 2.    |
   |URL di SQL Server Reporting Services   |Specificare l'URL del servizio Web per il server SSRS in cui sono configurati i report MBAM. Queste informazioni possono essere trovate accedendo a Gestione configurazione di Reporting Services nel server di database. <br /> Esempio di un nome di dominio completo:https://MyReportServer.Contoso.com/ReportServer <br />Esempio di nome host personalizzato:https://MyReportServer/ReportServer|
   |Directory virtuale   |Directory virtuale del sito Web di amministrazione e monitoraggio. Questo nome corrisponde alla directory fisica del sito Web del server e viene accodato al nome host del sito Web. Ad esempio: <br />http (s):// *\<host name\>* : *\<port\>* /helpdesk/ <br />Se non si specifica una directory virtuale, verrà usato l'HelpDesk per il valore.     |

9. Usare la descrizione seguente per immettere i valori dei campi nella procedura guidata per configurare il portale self-service.

   |Campo   |Descrizione|
   |----|----|
   |Directory virtuale   |Directory virtuale dell'applicazione Web. Questo nome corrisponde alla directory fisica del sito Web del server e viene accodato al nome host del sito Web. Ad esempio:<br />http (s):// *\<host name\>* : *\<port\>* /selfservice/<br /> Se non specifichi una directory virtuale, verrà usato il valore "SelfService".|

10. Dopo aver completato le voci, selezionare **Avanti**. La procedura guidata controlla che siano soddisfatti tutti i prerequisiti per le applicazioni Web.

11. Selezionare **Avanti** per continuare.

12. Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.

13. Selezionare **Aggiungi** per aggiungere le applicazioni Web al server e quindi selezionare **Chiudi**.

## Personalizzazione e convalida delle procedure dopo l'installazione di MBAM 2,5 Server software

### Passaggio 9: personalizzazione del portale self-server per l'organizzazione

Per personalizzare il portale self-service con l'aggiunta di testo di avviso personalizzato, il nome della società, i puntatori a altre informazioni e così via, vedere [personalizzazione del portale self-service per l'organizzazione](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization).
 
### Passaggio 10: configurare il portale self-server se i computer client non riescono ad accedere alla rete CDN 

Determinare se i computer client hanno accesso alla rete CDN (Microsoft AJAX Content Delivery Network). La rete CDN offre al portale self-service l'accesso necessario a determinati file JavaScript. Se non si configura il portale self-service quando i computer client non riescono ad accedere alla rete CDN, verranno visualizzati solo il nome della società e l'account in cui l'utente ha eseguito l'accesso. Nessun messaggio di errore verrà visualizzato.

Effettua una delle seguenti operazioni:

* Se i computer client hanno accesso alla rete CDN, non eseguire alcuna operazione. La configurazione del portale self-service è completa.

* Se i computer client non hanno accesso alla rete CDN, seguire la procedura descritta in [come configurare il portale self-service quando i computer client non riescono ad accedere a Microsoft Content Delivery Network](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### Passaggio 11: convalidare la configurazione della funzionalità del server MBAM 2,5 

Per convalidare la distribuzione di MBAM server per usare la topologia autonoma, seguire questa procedura.

1. In ogni server in cui è distribuita una caratteristica di mbam **Control Panel**selezionare  >  **Programs**  >  **programmi e funzionalità**del pannello di controllo. Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .
   > [!Note]
   > Per eseguire la convalida, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.

2. Nel server in cui è configurato il database di ripristino, aprire SQL Server Management Studio e verificare che il database di **mbam Recovery e hardware** sia configurato.

3. Nel server om che è configurato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che sia configurato il database di stato della conformità MBAM.

4. Nel server ONM in cui è configurata la caratteristica report, aprire un Web browser usando le credenziali amministrative e passare alla Home page del sito di SQL Server Reporting Services.
   
   La posizione iniziale predefinita di un'istanza del sito di SQL Server Reporting Services è la seguente: http (s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.
   
5. Verificare che una cartella report denominata amministrazione e monitoraggio di Microsoft BitLocker contenga un'origine dati denominata MaltaDataSource. Questa origine dati contiene le cartelle che contengono nomi che rappresentano le impostazioni locali della lingua, ad esempio en-US. I report si trovano nelle cartelle della lingua.

   > [!Note]
   > Se SQL Server Reporting Services (SSRS) è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http (s):// \<MBAM Reports Server Name\> : \<port\> /reports_\<SSRS Instance Name\>
   >
   > Se SSRS non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL per i report verrà impostato su "HTTP" invece di "HTTPS" quando si installa il server MBAM. Se si passa al sito Web di amministrazione e monitoraggio (noto anche come helpdesk) e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto". Per visualizzare il report, selezionare **Mostra tutto il contenuto**.

6. Nel server in cui è configurata la caratteristica sito Web amministrazione e monitoraggio eseguire Server Manager, passare a **ruoli**e quindi selezionare **Web Server (IIS)**  >  gestione**Internet Information Services (IIS)** .

7. In **connessioni**individuare \<computer name\> e selezionare i **siti**  >  **amministrazione e monitoraggio di Microsoft BitLocker**. Verificare che siano elencati i seguenti elementi:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. Nel server in cui sono configurati il sito Web di amministrazione e monitoraggio e il portale self-service, aprire un Web browser utilizzando le credenziali amministrative.

9. Individuare i siti Web seguenti per verificare che vengano caricati correttamente:
   * HTTPS (s):// \<MBAM Administration Server Name\> : \<port\> /helpdesk/(confermare ogni collegamento per gli spostamenti e i report)
   * http (s):// \<MBAM Administration Server Name\> : \<port\> /selfservice/

   > [!Note]
   > Si presuppone che siano state configurate le caratteristiche del server nella porta predefinita senza crittografia di rete. Se sono state configurate le caratteristiche del server in una porta o una directory virtuale diversa, cambiare gli URL in modo da includere la porta appropriata. Ad esempio: http (s):// \<host name\> : \<port\> /helpdesk/http (s):// \<host name\> : \<port\> / \<virtualdirectory\> /se le caratteristiche del server sono state configurate per l'uso della crittografia di rete, cambiare http://in https://.
   
10. Individuare i servizi Web seguenti per verificare che vengano caricati correttamente. Verrà visualizzata una pagina per indicare che il servizio è in funzione. Tuttavia, la pagina non Visualizza metadati.

    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http (s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### Passaggio 12: configurare i modelli dei criteri di gruppo di MBAM

Per distribuire MBAM, è necessario impostare le impostazioni dei criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per la crittografia unità BitLocker. Per completare questa attività, è necessario copiare i modelli di criteri di gruppo di MBAM in un server o una workstation in grado di eseguire la console Gestione criteri di gruppo o gestione avanzata Criteri di gruppo e quindi modificare le impostazioni.

> [!Important]
> Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** o mbam non funziona correttamente. Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di **crittografia unità BitLocker** .
 
#### Copia dei modelli di criteri di gruppo di MBAM 2,5

Prima di installare il client MBAM, devi copiare oggetti Criteri di gruppo specifici per MBAM nella workstation di gestione. Questi GPO definiscono le impostazioni di implementazione di MBAM per BitLocker. È possibile copiare i modelli di criteri di gruppo in qualsiasi server o workstation supportato da un server basato su Windows o da un computer client che può eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.

Per altre informazioni, vedere [copiare i modelli di criteri di gruppo di MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).
 
#### Modifica delle impostazioni GPO di MBAM 2,5

Dopo aver creato i GPO necessari, è necessario distribuire le impostazioni dei criteri di gruppo di MBAM ai computer client dell'organizzazione. Per visualizzare e creare oggetti Criteri di gruppo, è necessario che sia installata la console di gestione dei criteri di raggruppamento o Advanced Group Policy Management.

Per altre informazioni, vedere [modifica delle impostazioni dei criteri di gruppo di mbam 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) e [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### Passaggio 13: distribuzione del client MBAM 2,5

A seconda di quando si distribuisce il software di amministrazione e monitoraggio di Microsoft BitLocker, è possibile abilitare BitLocker in un computer dell'organizzazione prima che l'utente riceva il computer o in seguito configurando criteri di gruppo e distribuendo il software del client MBAM usando un sistema di distribuzione del software aziendale.
 
#### Distribuire il client MBAM in computer desktop o portatili

Dopo aver configurato le impostazioni dei criteri di gruppo, è possibile usare un prodotto del sistema di distribuzione del software aziendale, ad esempio Microsoft System Center 2012 Configuration Manager o Active Directory Domain Services (AD DS) per distribuire i file di installazione di Windows Installer di MBAM client in computer di destinazione. È possibile usare i file di MbamClientSetup.exe a 32 bit o a 64 bit oppure i file di MBAMClient.msi a 32 bit o 64 bit. Questi sono forniti insieme al software client MBAM.

Per altre informazioni, vedere [come distribuire il client mbam in computer desktop o portatili](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).
 
#### Distribuire il client MBAM come parte di una distribuzione di Windows

Nelle organizzazioni in cui i computer vengono ricevuti e configurati in modo centralizzato, è possibile installare il client MBAM per gestire la crittografia unità BitLocker in ogni computer prima che vengano scritti i dati degli utenti. Il vantaggio di questo processo è che ogni computer è quindi conforme a BitLocker. Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer. Un presupposto chiave per questo scenario è che il criterio dell'organizzazione consiste nell'installare un'immagine Windows aziendale prima che il computer venga recapitato all'utente. Se le impostazioni dei criteri di gruppo sono configurate per richiedere un PIN, viene chiesto agli utenti di impostare un PIN dopo la ricezione del criterio.

Per altre informazioni, vedere [come distribuire il client mbam come parte di una distribuzione di Windows](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### Come distribuire il client MBAM usando una riga di comando

Per altre informazioni [, vedere come distribuire il client mbam usando una riga di comando](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### Post-distribuzione dei client

Dopo aver completato l'attività di distribuzione, è necessario rivedere i registri seguenti e determinare se i client segnalano correttamente il database MBAM.

## Domande frequenti

### Come creare un server IIS con bilanciamento del carico

* L'SPN deve essere registrato solo per il nome descrittivo (ad esempio: bitlocker.corp.net) e non deve essere registrato nei singoli server IIS.

* Se viene usato un certificato, il certificato deve avere nomi FQDN e NetBIOS immessi nel campo **nome alternativo oggetto** per tutti i server IIS nel gruppo bilanciamento del carico e anche come nome descrittivo (ad esempio: BitLocker.Corp.NET). In caso contrario, il certificato verrà segnalato come non considerato attendibile dal browser quando si esplorano gli indirizzi con bilanciamento del carico.

Per altre informazioni, vedere [bilanciamento del carico di rete di IIS](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) e [registrazione di nomi SPN per l'account del pool di applicazioni](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account).

### Come configurare un certificato

* Dovrai avere due certificati. Viene usato un certificato per SQL Server e l'altro viene usato per IIS. Devono essere installati prima di avviare l'installazione di MBAM.

* È consigliabile usare il programma di installazione per aggiungere il certificato alla configurazione di IIS invece di modificare manualmente il file web.config.

* Il certificato non verrà accettato da MBAM Configurator se il campo "rilasciato a" del certificato non corrisponde al nome del server. In questo caso, creare temporaneamente un certificato autofirmato dalla console IIS e usarlo nel configuratore. In questo modo Nsure che le app Web siano installate per SSL e HTTPS. In seguito, puoi cambiare il certificato in uno dei binding di IIS per il sito Web di MBAM.

### Requisito di autorizzazioni SQL per l'installazione

Crea un account per il pool di MBAM app e assegna solo le autorizzazioni SecurityAdmin, Public e DBCreator.

Vedi la [configurazione del database mbam-autorizzazioni minime](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) per altre informazioni.

> [!Note]
> * In alcuni casi sono necessarie più autorizzazioni per le operazioni di installazione e aggiornamento iniziali.
> * Usare un account con SA temporanea per l'installazione.
> * Non avviare il configuratore nel contesto di un account utente (Esegui come) che non disponga di autorizzazioni sufficienti per apportare modifiche a SQL Server, in quanto ciò causerà errori di installazione.
> * È necessario avere effettuato l'accesso con un account che disponga delle autorizzazioni per SQL Server. È possibile creare o aggiornare solo i database di SQL Server eseguendo MBAM Configurator in remoto. Per il server SSRS, è necessario installare MBAM ed eseguire Configurator localmente per installare o aggiornare i report di MBAM SSRS.

### Autorizzazione necessaria per la registrazione di SPN

Un account usato per l'installazione del portale IIS deve avere le autorizzazioni Write ServicePrincipalName e Write convalidated SPN. Senza queste autorizzazioni, l'installazione restituirà un messaggio di avviso che indica che non può registrare il nome SPN.

> [!Note]
> Questo messaggio di avviso verrà visualizzato due volte. Questo non significa che il nome SPN debba avere due oggetti registrati.

Per altre informazioni, vedere [errore di configurazione di mbam con "Register SPN Deferred"](https://support.microsoft.com/help/2754138/).

### È necessario aggiornare i modelli ADMX alla versione più recente?

Vedrai più opzioni del sistema operativo nel nodo radice di MBAM per l'oggetto Criteri di gruppo dopo l'aggiornamento dei modelli ADMX alle versioni più recenti. Ad esempio, Windows 7, Windows 8,1 e Windows 10, versione 1511 e versioni successive.

Per altre informazioni su come aggiornare i modelli ADMX, vedere gli articoli seguenti:
* [Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Modelli amministrativi di criteri di gruppo di Microsoft Desktop Optimization Pack](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
