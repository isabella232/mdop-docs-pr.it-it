---
title: Distribuzione di MBAM 2.5 in una configurazione autonoma
description: Introduzione alla distribuzione di MBAM 2.5 in una configurazione autonoma.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 1ceccf3973bb131484f91917c2b80cd676d1c31b
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910471"
---
# <a name="deploying-mbam-25-in-a-standalone-configuration"></a>Distribuzione di MBAM 2.5 in una configurazione autonoma

In questo articolo vengono fornite istruzioni dettagliate per l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in una configurazione autonoma. In questa guida verrà utilizzata una configurazione a due server. Uno dei due server sarà un server di database che esegue Microsoft SQL Server 2012. Questo server ospiterà i database e i report MBAM. Il server aggiuntivo sarà un Windows Server 2012 Web che ospita "Administration and Monitoring Server" e "Self-Service Portal".

## <a name="preparation-steps-before-installing-mbam-25-server-software"></a>Passaggi di preparazione prima di installare il software server MBAM 2.5

### <a name="step-1-installation-and-configuration-of-servers"></a>Passaggio 1: installazione e configurazione dei server

Prima di iniziare a configurare MBAM 2.5, è necessario verificare che entrambi i server siano configurati in base ai requisiti di sistema di MBAM. Vedere i requisiti minimi di sistema di [MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements)e selezionare una configurazione che soddisfi questi requisiti. 

#### <a name="step-11-deploying-prerequisites-for-database-and-reporting-server"></a>Passaggio 1.1: Distribuzione dei prerequisiti per database e server di report

1. Installare e configurare un server che esegue Windows Server 2008 R2 (o versione successiva).

2. Installare Windows PowerShell 3.0.

3. Installare Microsoft SQL Server 2008 R2 o versione successiva che include il Service Pack più recente. Se si installa una nuova istanza di SQL Server per MBAM, verificare che il SQL Server installato includa le regole di confronto SQL_Latin1_General_CP1_CI_AS. Dovrai installare le seguenti funzionalità SQL Server seguenti:

    * motore di database
    * Reporting Services
    * Connettività degli strumenti client
    * Strumenti di gestione - Completa

    > [!Note]
    > Facoltativamente, è anche possibile installare la [funzionalità Transparent Data Encryption (TDE) in SQL Server](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations).

    SQL Server Reporting Services deve essere installato e configurato in modalità "nativa" e non in modalità non configurata o "SharePoint".

    ![Le funzionalità SQL Server necessarie.](images/deploying-MBAM-1.png)

4. Se si prevede di utilizzare SSL per il sito Web amministrazione e monitoraggio, assicurarsi di configurare SQL Server Reporting Services (SSRS) per l'utilizzo del protocollo SSL (Secure Sockets Layer) prima di configurare il sito Web amministrazione e monitoraggio. In caso contrario, la funzionalità Report utilizzerà il trasporto dati non crittografato (HTTP) anziché crittografato (HTTPS).

    È possibile seguire [Configure SSL Connections](https://docs.microsoft.com/sql/reporting-services/security/configure-ssl-connections-on-a-native-mode-report-server?view=sql-server-2017) on a Native Mode Report Server per configurare SSL nel server di report.
    
    > [!Note]
    > È possibile seguire la guida all SQL Server installazione per la propria versione di SQL Server installare SQL Server. I collegamenti sono i seguenti:
        > * [SQL Server 2014](https://docs.microsoft.com/sql/sql-server/install/planning-a-sql-server-installation?view=sql-server-2014)
        > * [SQL Server 2012](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))
        > * [SQL Server 2008 R2](https://docs.microsoft.com/previous-versions/sql/sql-server-2012/bb500442(v=sql.110))

5. Nella post-installazione di SQL Server, assicurarsi di effettuare il provisioning dell'account utente in SQL Server e assegnare le autorizzazioni seguenti all'utente che configurerà il database MBAM e i ruoli di creazione di report nel server database.

    Ruoli per l'istanza di SQL Server:
        
    * dbcreator
    * processadmin

    Diritti per l'istanza di SQL Server Reporting Services:
    
    * Creare cartelle
    * Pubblicare report

Il server di database è pronto per la configurazione dei ruoli di MBAM 2.5. Passiamo al server successivo.

#### <a name="step-12-deploying-prerequisites-for-administration-and-monitoring-server"></a>Passaggio 1.2: Distribuzione dei prerequisiti per il server di amministrazione e monitoraggio

Scegliere un server che soddisfi la configurazione hardware, come illustrato nel documento [mbam system requirements .](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-supported-configurations#-mbam-server-system-requirements) Deve essere in esecuzione Windows Server 2008 R2 o versione successiva con service pack e aggiornamenti più recenti. Dopo aver pronto il server, installare i ruoli e le funzionalità seguenti:

##### <a name="roles"></a>Ruoli

* Strumenti di gestione server Web (IIS) (selezionare Strumenti e script di gestione IIS).

* Servizi ruolo server Web

    * Funzionalità HTTP comuni<br />
      Contenuto statico<br />
      Documento predefinito

    * Sviluppo di applicazioni<br />
      ASP.NET<br />
      Estendibilità .NET<br />
      Estensioni ISAPI<br />
      Filtri ISAPI<br />
      Sicurezza<br />
      Autenticazione di Windows<br />
      Filtro richieste

    * Strumenti di gestione IIS del servizio Web

##### <a name="feature"></a>Funzionalità

* .NET Framework 4.5
  
  * Microsoft .NET Framework 4.5
  
    Per Windows Server 2012 o Windows Server 2012 R2, .NET Framework 4.5 è già installato per queste versioni di Windows Server. Tuttavia, è necessario abilitarlo.
  
    Per Windows Server 2008 R2, .NET Framework 4.5 non è incluso in Windows Server 2008 R2. È quindi necessario scaricare .NET Framework 4.5 e installarlo separatamente.
  
  * Attivazione WCF<br />
    Attivazione HTTP<br />
    Attivazione non HTTP
  
  * Attivazione TCP
  
  * Windows Process Activation Service:<br />
    Modello di processo<br />
    .NET Framework Ambiente<br />
    API di configurazione

Per il funzionamento del portale self-service, è inoltre consigliabile scaricare e installare [ASP.NET MVC 4.0.](https://go.microsoft.com/fwlink/?linkid=392271)

Il passaggio successivo consiste nel creare gli utenti e i gruppi MBAM necessari in Active Directory.

### <a name="step-2-creating-users-and-groups-in-active-directory-domain-services"></a>Passaggio 2: Creazione di utenti e gruppi in Servizi di dominio Active Directory
 
Come parte dei prerequisiti, è necessario definire determinati ruoli e account utilizzati in MBAM per fornire diritti di sicurezza e accesso a server e funzionalità specifici, ad esempio i database in esecuzione nell'istanza di SQL Server e le applicazioni Web in esecuzione in Administration and Monitoring Server.

Creare i gruppi e gli utenti seguenti in Active Directory. È possibile utilizzare qualsiasi nome per i gruppi e gli utenti. Gli utenti non devono disporre di diritti utente maggiori. Un account utente di dominio è sufficiente. Dovrai specificare il nome di questi gruppi durante la configurazione di MBAM 2.5:

* **MBAMAppPool**  

  **Tipo**: Utente di dominio

  **Descrizione:** utente di dominio che dispone dell'autorizzazione di lettura o scrittura per il database di conformità e controllo e il database di ripristino per consentire alle applicazioni Web di accedere ai dati e ai report in questi database. Verrà inoltre utilizzato dal pool di applicazioni per le applicazioni Web.

  **Ruoli account (durante la configurazione di MBAM)**:

  1. Account di dominio del pool di applicazioni del servizio Web

  2. Compliance and Audit Database and Recovery Database read/write user for reports

* **MBAMROUser**

  **Tipo**: Utente di dominio

  **Descrizione:** utente di dominio che Read-Only accesso al database di conformità e controllo per consentire ai report di accedere ai dati di conformità e controllo in questo database. Sarà anche l'account utente di dominio utilizzato dall'istanza SQL Server Reporting Services locale per accedere al database di conformità e controllo.

  **Ruoli account (durante la configurazione di MBAM)**:

  1. Utente di sola lettura del database di conformità e controllo per i report

  2. Account utente di dominio del database di conformità e controllo

* **MBAMAdvHelpDsk**

  **Tipo**: Gruppo di dominio

  **Descrizione:** gruppo di accesso utenti del supporto avanzato MBAM: gruppo di utenti di dominio i cui membri hanno accesso a tutte le aree del sito Web amministrazione e monitoraggio. Gli utenti che dispongono di questo ruolo devono immettere solo la chiave di ripristino, non il dominio e il nome utente dell'utente, quando aiutano gli utenti a ripristinare le unità. Se un utente è membro sia del gruppo MbAM Helpdesk Users che del gruppo MbAM Advanced Helpdesk Users, le autorizzazioni del gruppo MbAM Advanced Helpdesk Users hanno la precedenza sulle autorizzazioni del gruppo helpdesk MBAM.

  **Ruoli account (durante la configurazione di MBAM):** utenti del supporto avanzato MBAM

* **MBAMHelpDsk**

  **Tipo**: Gruppo di dominio

  **Descrizione:** gruppo di accesso utenti helpdesk MBAM: gruppo di utenti di dominio i cui membri hanno accesso alle aree Gestione TPM e Ripristino unità del sito Web Amministrazione e monitoraggio MBAM. Gli utenti con questo ruolo devono compilare tutti i campi quando utilizzano entrambe le opzioni. Sono inclusi il dominio e il nome dell'account dell'utente.

  **Ruoli account (durante la configurazione di MBAM):** utenti del supporto di MBAM

* **MBAMRUGrp**

  **Tipo**: Gruppo di dominio

  **Descrizione:** gruppo di utenti di dominio i cui membri hanno accesso in sola lettura ai report nell'area Report del sito Web amministrazione e monitoraggio.

  **Ruoli account (durante la configurazione di MBAM)**:

  1. Segnala il gruppo di accesso al dominio di sola lettura

  2. Gruppo di accesso utenti report MBAM

### <a name="step-3-optional-configure-and-install-ssl-certificate-on-administration-and-monitoring-server"></a>Passaggio 3 (facoltativo): configurare e installare il certificato SSL nel server di amministrazione e monitoraggio

Sebbene sia facoltativo, è consigliabile utilizzare un certificato per proteggere la comunicazione tra il client MBAM e il sito Web amministrazione e monitoraggio e i siti Web Self-Service Portal. Non è consigliabile utilizzare certificati autofirmati per ovvi motivi di sicurezza. È consigliabile utilizzare un certificato di tipo server Web da un'Autorità di certificazione attendibile. A tale scopo, è possibile fare riferimento alla sezione "Utilizzo del certificato approvato dall'autorità di certificazione" da [KB 2754259](https://support.microsoft.com/help/2754259).

Dopo l'emissione del certificato, è necessario aggiungere il certificato all'archivio personale di Administration and Monitoring Server. Per aggiungere il certificato, aprire l'archivio certificati nel computer locale. A tale scopo, procedere come segue:

1. Fare clic con il pulsante destro del mouse su Start e quindi scegliere Esegui.

   ![Selezionare.](images/deploying-MBAM-2.png)

2. Digitare "MMC.EXE" (senza virgolette) e quindi selezionare **OK**.

   ![Casella Esegui.](images/deploying-MBAM-3.png) 

3. Selezionare **File** nella nuova console MMC aperta, quindi **scegliere Aggiungi/Rimuovi snap-in.**
   
   ![Selezionare.](images/deploying-MBAM-4.png)

4. Evidenziare **lo** snap-in Certificati e quindi selezionare **Aggiungi**.

   ![Finestra Aggiungi o rimuovi snap-in.](images/deploying-MBAM-5.png)

5. Selezionare **l'opzione Account computer** e quindi fare clic su **Avanti.**
   
   ![Finestra snap-in Certificati.](images/deploying-MBAM-6.png)

6. Selezionare **Computer locale** nella schermata successiva e quindi fare clic su **Fine.**
   
   ![Seleziona Finestra computer.](images/deploying-MBAM-7.png)

7. A questo punto è stato aggiunto lo snap-in Certificati. In questo modo sarà possibile utilizzare tutti i certificati nell'archivio certificati del computer.

   ![Finestra Aggiungi o rimuovi snap-in.](images/deploying-MBAM-8.png)

8. Importare il certificato del server Web nell'archivio certificati del computer.

   Ora che si ha accesso alla snap-in Certificati, è possibile importare il certificato del server Web nell'archivio certificati del computer. A tale scopo, seguire i passaggi successivi.

9. Aprire lo snap-in Certificati (computer locale) e passare a **Personale** e quindi **Certificati**.
   
   ![Finestra snap-in Certificati (computer locale).](images/deploying-MBAM-9.png)

   > [!Note]
   > Lo snap-in Certificati potrebbe non essere elencato. In caso contrario, non verrà installato alcun certificato.

10. Fare clic con il **pulsante destro del**mouse su Certificati , scegliere Tutte **le**attività e quindi **Importa**.

    ![Finestra snap-in Certificati (computer locale).](images/deploying-MBAM-10.png)

11. All'avvio della procedura guidata, selezionare **Avanti**. Passare al file creato contenente il certificato server e la chiave privata e quindi selezionare **Avanti.**

    ![Finestra Importazione guidata certificati.](images/deploying-MBAM-11.png)

12. Immettere la password se è stata specificata una per il file al momento della creazione.

   ![Finestra immettere la password.](images/deploying-MBAM-12.png)

   > [!Note]
   > Assicurati che **l'opzione** Contrassegna la chiave come esportabile sia selezionata se vuoi poter esportare di nuovo la coppia di chiavi da questo computer. Come misura di sicurezza aggiunta, è possibile lasciare deselezionata questa opzione per assicurarsi che nessuno possa eseguire un backup della chiave privata.
 
13. Selezionare **Avanti**e quindi selezionare l'archivio **certificati** in cui si desidera salvare il certificato.

    ![Finestra Importazione guidata certificati.](images/deploying-MBAM-13.png)

    > [!Note]
    > È consigliabile **selezionare Personale**perché si tratta di un certificato del server Web. Se il certificato è stato incluso nella gerarchia di certificazione, verrà aggiunto anche a questo archivio.
 
14. Selezionare **Avanti**e quindi **fine.**

    ![Finestra Importazione guidata certificati.](images/deploying-MBAM-14.png)

Il certificato server per il server Web verrà ora visualizzato nell'elenco Certificati personali. Verrà denotato dal nome comune del server. È possibile trovarlo nella sezione dell'oggetto del certificato.

Per ulteriori informazioni di riferimento:

[Considerazioni sulla sicurezza per MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/mbam-25-security-considerations)

[Pianificazione di come proteggere i siti Web di MBAM](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Il passaggio successivo consiste nel registrare un nome di principio del servizio per l'account del pool di applicazioni.

### <a name="step-4-configuring-ssl-certificate-for-mbam-web-server"></a>Passaggio 4: Configurazione del certificato SSL per il server Web MBAM

Se si utilizza la comunicazione SSL tra il client e il server, assicurarsi che il certificato abbia OID di utilizzo chiavi avanzato (1.3.6.1.5.5.7.3.1) e (1.3.6.1.5.5.7.3.2). Ciò significa che è necessario assicurarsi che l'autenticazione server e l'autenticazione client siano state aggiunte.

Se viene visualizzato un errore di certificato quando si tenta di esplorare gli URL del servizio, si utilizza un certificato emesso con un nome diverso oppure si sta esplorando utilizzando un URL non corretto.

Anche se il browser potrebbe richiedere un messaggio di errore del certificato ma consentire di continuare, il servizio Web MBAM non ignorerà gli errori del certificato e blocterà la connessione. Si noteranno errori relativi ai certificati nel registro eventi di amministrazione MBAM del client MBAM. Se si utilizza un alias per connettersi al server di amministrazione e monitoraggio, è necessario emettere un certificato al nome dell'alias. In altre informazioni, il nome soggetto del certificato deve essere il nome alias e il nome DNS del server locale deve essere aggiunto al campo **Subject Alternative Name** del certificato.

Esempio:

Se il nome virtuale è "bitlocker.contoso.com" e il nome del server di amministrazione e monitoraggio di MBAM è "adminserver.contoso.com", il certificato deve essere rilasciato a bitlocker.contoso.com (nome soggetto) e adminserver.contoso.com deve essere aggiunto al campo **Nome** soggetto alternativo del certificato.

Analogamente, se sono installati più server di amministrazione e monitoraggio per bilanciare il carico tramite un servizio di bilanciamento del carico, è consigliabile emettere il certificato SSL al nome virtuale. In altre informazioni, il campo del nome soggetto del certificato deve avere il nome virtuale e i nomi di tutti i server locali devono essere aggiunti nel campo Nome soggetto **alternativo** del certificato.

Esempio:

Se il nome virtuale è "bitlocker.contoso.com" e i server sono "adminserver1.contoso.com" e "adminiserver2.contoso.com", il certificato deve essere rilasciato a bitlocker.contoso.com (nome soggetto) e adminserver1.contoso.com e adminiserver2.contoso.com deve essere aggiunto al campo **Subject Alternative Name** del certificato.

I passaggi per configurare la comunicazione SSL tramite MBAM sono descritti nel seguente articolo della Knowledge Base: [KB 2754259](https://support.microsoft.com/help/2754259).

### <a name="step-5-register-spns-for-the-application-pool-account-and-configure-constrained-delegation"></a>Passaggio 5: registrare SPN per l'account del pool di applicazioni e configurare la delega vincolata

> [!Note]
> La delega vincolata è necessaria solo per la versione 2.5 e non per 2.5 Service Pack 1 e versioni successive.

Per consentire ai server MBAM di autenticare le comunicazioni dal sito Web di amministrazione e monitoraggio e dal portale di Self-Service, è necessario registrare un nome dell'entità servizio (SPN) per il nome host nell'account di dominio utilizzato per il pool di applicazioni Web. L'articolo seguente contiene istruzioni dettagliate per registrare gli SPN: [Planning How to Secure the MBAM Websites](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites)

Dopo aver configurato l'SPN, è necessario impostare la delega vincolata nell'SPN. A tale scopo, procedere come segue:

1. Passare ad Active Directory e trovare le credenziali del pool di app configurate per i siti Web MBAM nei passaggi precedenti.

2. Fare clic con il pulsante destro del mouse sulle credenziali e quindi scegliere **proprietà**.

3. Selezionare la **scheda delega.**

4. Selezionare l'opzione per l'autenticazione Kerberos.

5. Seleziona **Sfoglia**e cerca di nuovo le credenziali del pool di app. Verranno quindi visualizzati tutti gli SPN impostati nell'account creds del pool di app. (Il nome SPN deve essere simile a "http/bitlocker.fqdn.com"). Evidenziare l'SPN che corrisponde al nome host specificato durante l'installazione di MBAM.

6. Selezionare **OK**.

A questo punto è possibile utilizzare i prerequisiti. Nei passaggi successivi, il software MBAM verrà installato nei server e configurato.

## <a name="installing-and-configuring-mbam-25-server-software"></a>Installazione e configurazione del software server MBAM 2.5

### <a name="step-6-install-mbam-25-server-software"></a>Passaggio 6: Installare il software server MBAM 2.5 

Per installare il software del server MBAM utilizzando l'installazione guidata di Amministrazione e monitoraggio di Microsoft BitLocker sia nel server di database che in Amministrazione e Monitoring Server, attenersi alla seguente procedura.

1. Nel server in cui si desidera installare MBAM, eseguire MBAMserversetup.exe per avviare l'installazione guidata di Amministrazione e monitoraggio di Microsoft BitLocker.

2. Nella pagina iniziale selezionare **Avanti**.

3. Leggere e accettare il Contratto di licenza software Microsoft, quindi selezionare **Avanti** per continuare l'installazione.

4. Decidere se utilizzare Microsoft Update quando si verifica la disponibilità di aggiornamenti e quindi selezionare **Avanti**.

5. Decidere se partecipare al programma Analisi utilizzo software e quindi selezionare **Avanti.**

6. Per avviare l'installazione, selezionare **Installa**.

7. Per configurare le funzionalità del server al termine dell'installazione del software del server MBAM, selezionare la casella di controllo Esegui configurazione **server MBAM** dopo la chiusura della procedura guidata. In caso contrario, è possibile configurare MBAM in un secondo momento utilizzando il collegamento **Configurazione server MBAM** creato dall'installazione del server nel menu **Start.**

8. Selezionare **Fine.**

Per ulteriori informazioni, vedere [Installing the MBAM 2.5 Server Software](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/installing-the-mbam-25-server-software).

### <a name="step-7-configure-mbam-25-database-and-reports-role"></a>Passaggio 7: Configurare il ruolo di database e report di MBAM 2.5

In questo passaggio verrà configurato il componente di creazione dei report e dei database di MBAM 2.5 utilizzando la procedura guidata MBAM:

1. Configurare il database di conformità e controllo e il database di ripristino tramite la procedura guidata:
   
   1. Nel server in cui si desidera configurare i database avviare la Configurazione **guidata server MBAM.** È possibile selezionare **Configurazione server MBAM** dal menu **Start** per aprire la procedura guidata.

   2. Selezionare **Aggiungi nuove funzionalità,** selezionare **Conformità e controllo database,** **Database**e report di ripristino e quindi fare clic su **Avanti.** La procedura guidata verifica che tutti i prerequisiti per i database siano soddisfatti.

   3. Se il controllo dei prerequisiti ha esito positivo, selezionare **Avanti** per continuare. In caso contrario, risolvere eventuali prerequisiti mancanti e quindi selezionare **Controlla di nuovo i prerequisiti.**
   
   4. Utilizzando le descrizioni seguenti, immettere i valori dei campi nella procedura guidata:

2. Database di conformità e controllo

   |Campo   |Descrizione|
   |-------|-------|
   |SQL Server nome |Nome del server in cui si sta configurando il database di conformità e controllo. <br /> È necessario aggiungere un'eccezione nel computer del database di conformità e controllo per abilitare il traffico in ingresso sulla porta SQL Server controllo. Il numero di porta predefinito è 1433.|
   |SQL Server istanza del database    |Nome dell'istanza del database in cui verranno archiviati i dati di conformità e controllo. Se si utilizza l'istanza predefinita, è necessario lasciare vuoto questo campo. È inoltre necessario specificare la posizione delle informazioni del database.|
   |Nome database   |Nome del database in cui verranno archiviati i dati di conformità. È necessario prendere nota del nome del database specificato qui perché sarà necessario fornire queste informazioni nei passaggi successivi.|
   |Utente o gruppo del dominio di autorizzazione di lettura/scrittura  |Specificare il nome dell'utente MBAMAppPool come configurato nel passaggio 2.|
   |Utente o gruppo di dominio di accesso di sola lettura   |Specificare il nome dell'utente MBAMROUser come configurato nel passaggio 2.|

3. Database di ripristino.

   |Campo   |Descrizione|
   |-----|-----|
   |SQL Server nome |Nome del server in cui si sta configurando il database di ripristino. È necessario aggiungere un'eccezione nel computer del database di ripristino per abilitare il traffico in ingresso sulla SQL Server locale. Il numero di porta predefinito è 1433.|
   |SQL Server istanza del database    |Nome dell'istanza del database in cui verranno archiviati i dati di ripristino. Se si utilizza l'istanza predefinita, è necessario lasciare vuoto questo campo. È inoltre necessario specificare la posizione delle informazioni del database.|
   |Nome database   |Nome del database in cui verranno archiviati i dati di ripristino.|
   |Utente o gruppo del dominio di autorizzazione di lettura/scrittura  |Utente o gruppo di dominio che dispone dell'autorizzazione di lettura/scrittura per il database per consentire alle applicazioni Web di accedere ai dati e ai report in questo database. <br />Se si immette un utente in questo campo, deve corrispondere al valore del campo Account di dominio del pool di applicazioni del servizio **Web** nella pagina Configura **applicazioni Web.** <br />Se si immette un gruppo in questo campo, il valore nel campo Account di dominio del pool di applicazioni del servizio **Web** nella pagina Configura applicazioni **Web** deve essere un membro del gruppo immesso in questo campo.|
   
   Al termine delle voci, selezionare **Avanti**. La procedura guidata verifica che tutti i prerequisiti per i database siano soddisfatti.
   
   Se il controllo dei prerequisiti ha esito positivo, selezionare **Avanti** per continuare. In caso contrario, risolvere eventuali prerequisiti mancanti e quindi selezionare **di nuovo Avanti.**

4. Report.

   |Campo   |Descrizione|
   |----|----|
   |SQL Server Reporting Services istanza  |Istanza di SQL Server Reporting Services in cui verranno configurati i report. Se si utilizza l'istanza predefinita, è necessario lasciare vuoto questo campo.|
   |Gruppo di dominio del ruolo Reporting |Specificare il nome di MBAMRUGrp come indicato nel passaggio 2.|
   |SQL Server nome |Nome del server in cui è configurato il database di conformità e controllo.|
   |SQL Server istanza del database    |Nome dell'istanza del database in cui sono configurati i dati di conformità e controllo. Se si utilizza l'istanza predefinita, è necessario lasciare vuoto questo campo. <br />È necessario aggiungere un'eccezione nel computer Report per abilitare il traffico in ingresso sulla porta del server di report. La porta predefinita è 80.|
   |Nome database|  Nome del database di conformità e controllo. Per impostazione predefinita, il nome del database è MBAM Compliance Status.|
   |Account di dominio del database di conformità e controllo    |Specificare il nome dell'utente MBAMROUser come configurato nel passaggio 2.|
   
   Al termine delle voci, selezionare **Avanti**. La procedura guidata verifica che tutti i prerequisiti per la funzionalità Report siano soddisfatti. Seleziona Avanti per continuare. Nella pagina **Riepilogo** esaminare le funzionalità che verranno aggiunte.
   
   Per ulteriori informazioni, vedere l'articolo seguente: [How to Configure the MBAM 2.5 Databases](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-mbam-25-databases).

### <a name="step-8-configure-the-mbam-25-web-applications-role"></a>Passaggio 8: Configurare il ruolo applicazioni Web MBAM 2.5

1. Nel server in cui si desidera configurare le applicazioni Web avviare la Configurazione guidata server MBAM. È possibile selezionare **Configurazione server MBAM** dal menu **Start** per aprire la procedura guidata.

2. Selezionare **Aggiungi nuove funzionalità,** selezionare **Sito Web di amministrazione** e monitoraggio e **Portale self-service**e quindi fare clic su **Avanti.** La procedura guidata verifica che tutti i prerequisiti per i database siano soddisfatti.

3. Se il controllo dei prerequisiti ha esito positivo, selezionare **Avanti** per continuare. In caso contrario, risolvere eventuali prerequisiti mancanti e quindi selezionare **Controlla di nuovo i prerequisiti.**

4. Utilizzare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata.

   |Campo   |Descrizione|
   |-----|-----|
   |Certificato di sicurezza    |Selezionare un certificato creato in precedenza nel passaggio 3 per crittografare facoltativamente la comunicazione tra i servizi Web e il server in cui si sta configurando il sito Web di amministrazione e monitoraggio. Se si seleziona Non utilizzare un certificato, la comunicazione Web potrebbe non essere sicura.|
   |Nome dell'host   |Nome del computer host in cui si sta configurando il sito Web di amministrazione e monitoraggio. <br />Non deve essere il nome host del computer, ma può essere qualsiasi cosa. Tuttavia, se il nome host è diverso dal nome netbios del computer, è necessario creare un record A e assicurarsi che l'SPN utilizzi il nome host personalizzato, non il nome netbios. Ciò è comune negli scenari di bilanciamento del carico.|
   |Percorso di installazione   |Percorso in cui si sta installando il sito Web di amministrazione e monitoraggio.|
   |Port    |Numero di porta da utilizzare per la comunicazione del sito Web. <br /> È necessario impostare un'eccezione del firewall per abilitare la comunicazione tramite la porta specificata.|
   |Account di dominio e password del pool di applicazioni del servizio Web    |Specificare l'account utente e la password dell'utente MBAMAppPool come configurato nel passaggio 2. <br /> Per una maggiore sicurezza, impostare l'account specificato nelle credenziali in modo che abbia diritti utente limitati. Impostare inoltre la password dell'account in modo che non scada mai.|

5. Verificare che l'account IIS_IUSRS predefinito o l'account del pool di applicazioni sia stato aggiunto alle impostazioni di protezione locale Rappresenta un **client** dopo l'autenticazione e Accedi come processo **batch.**

   Per verificare se l'account è stato aggiunto alle impostazioni di **** protezione locali, aprire **** **l'editor**criteri di sicurezza locali, espandere il nodo Criteri locali, selezionare il nodo Assegnazione diritti utente e quindi fare doppio clic su Rappresenta un **client** dopo l'autenticazione e Accedere come processo **batch** nel riquadro a destra.

6. Utilizzare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di conformità e controllo.
   |Campo   |Descrizione|
   |------|------|
   |SQL Server nome |Nome del server in cui è configurato il database di conformità e controllo.|
   |SQL Server istanza del database    |Nome dell'istanza di SQL Server (ad esempio, ) in cui è configurato il database di conformità \<Server Name\> e controllo. Lasciare vuoto questo campo se si utilizza l'istanza predefinita.|
   |Nome database   |Nome del database di conformità e controllo. Per impostazione predefinita, è "Stato conformità MBAM".|

7. Utilizzare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di ripristino.
   |Campo   |Descrizione|
   |----|----|
   |SQL Server nome |Nome del server in cui è configurato il database di ripristino.|
   |SQL Server istanza del database    |Nome dell'istanza di SQL Server (ad esempio, \<Server Name\> ) in cui è configurato il database di ripristino. Lasciare vuoto questo campo se si utilizza l'istanza predefinita.|
   |Nome database   |Nome del database di ripristino. Per impostazione predefinita, è "MBAM Recovery and Hardware".|

8. Utilizzare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata per configurare il sito Web amministrazione e monitoraggio.
   |Campo   |Descrizione|
   |----|----|
   |Gruppo di dominio del ruolo Helpdesk avanzato |Specificare il nome del gruppo MBAMAdvHelpDsk come configurato nel passaggio 2.|
   |Gruppo di dominio del ruolo Helpdesk  |Specificare il nome del gruppo MBAMHelpDsk come configurato nel passaggio 2.|
   |Usare System Center Configuration Manager integration |Selezionare questa casella di controllo per deselezionare questa casella di controllo.     |
   |Gruppo di dominio del ruolo Reporting |Specificare il nome del gruppo MBAMRUGrp come configurato nel passaggio 2.    |
   |SQL Server Reporting Services URL   |Specificare l'URL del servizio Web per il server SSRS in cui sono configurati i report MBAM. È possibile trovare queste informazioni accedendo a Gestione configurazione Reporting Services nel server di database. <br /> Esempio di nome di dominio completo: https://MyReportServer.Contoso.com/ReportServer <br />Esempio di nome host personalizzato: https://MyReportServer/ReportServer|
   |Directory virtuale   |Directory virtuale del sito Web di amministrazione e monitoraggio. Questo nome corrisponde alla directory fisica del sito Web nel server e viene aggiunto al nome host del sito Web. Ad esempio: <br />http(s):// *\<host name\>* : *\<port\>* /HelpDesk/ <br />Se non si specifica una directory virtuale, verrà utilizzato il valore HelpDesk.     |

9. Utilizzare la descrizione seguente per immettere i valori dei campi nella procedura guidata per configurare il Self-Service Portal.

   |Campo   |Descrizione|
   |----|----|
   |Directory virtuale   |Directory virtuale dell'applicazione Web. Questo nome corrisponde alla directory fisica del sito Web nel server e viene aggiunto al nome host del sito Web. Ad esempio:<br />http(s):// *\<host name\>* : *\<port\>* /SelfService/<br /> Se non si specifica una directory virtuale, verrà utilizzato il valore "SelfService".|

10. Al termine delle voci, selezionare **Avanti**. La procedura guidata verifica che tutti i prerequisiti per le applicazioni Web siano soddisfatti.

11. Selezionare **Avanti** per continuare.

12. Nella pagina **Riepilogo** esaminare le funzionalità che verranno aggiunte.

13. Selezionare **Aggiungi** per aggiungere le applicazioni Web al server e quindi selezionare **Chiudi.**

## <a name="customizing-and-validating-steps-after-installing-mbam-25-server-software"></a>Personalizzazione e convalida dei passaggi dopo l'installazione del software server MBAM 2.5

### <a name="step-9-customizing-the-self-server-portal-for-your-organization"></a>Passaggio 9: Personalizzazione del portale self-server per l'organizzazione

Per personalizzare il portale di Self-Service aggiungendo testo di avviso personalizzato, il nome della società, i puntatori a ulteriori informazioni e così via, vedere [Customizing the Self-Service Portal for Your Organization](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/customizing-the-self-service-portal-for-your-organization).
 
### <a name="step-10-configure-the-self-server-portal-if-client-computers-cannot-access-the-cdn"></a>Passaggio 10: Configurare il portale self-server se i computer client non possono accedere al rete CDN 

Determinare se i computer client hanno accesso a Microsoft AJAX rete per la distribuzione di contenuti (rete CDN). Il rete CDN fornisce al Self-Service portal l'accesso necessario a determinati file JavaScript. Se non si configura il portale di Self-Service quando i computer client non possono accedere al rete CDN, verranno visualizzati solo il nome della società e l'account con cui l'utente ha eseguito l'accesso. Non verrà visualizzato alcun messaggio di errore.

Effettua una delle seguenti operazioni:

* Se i computer client hanno accesso al rete CDN, non eseguire alcuna operazione. La configurazione Self-Service Portal è stata completata.

* Se i computer client non hanno accesso al rete CDN, seguire la procedura descritta in [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft rete per la distribuzione di contenuti](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network).

### <a name="step-11-validate-the-mbam-25-server-feature-configuration"></a>Passaggio 11: Convalidare la configurazione delle funzionalità del server MBAM 2.5 

Per convalidare la distribuzione del server MBAM per l'utilizzo della topologia autonoma, eseguire la procedura seguente.

1. In ogni server in cui viene distribuita una funzionalità MBAM, selezionare Programmi e funzionalità del **Pannello**  >  ****  >  **di controllo.** Verificare che **Microsoft BitLocker Administration and Monitoring** sia visualizzato nell'elenco Programmi **e** funzionalità.
   > [!Note]
   > Per eseguire la convalida, è necessario utilizzare un account di dominio con credenziali amministrative del computer locale in ogni server.

2. Nel server in cui è configurato il database di ripristino, aprire SQL Server Management Studio e verificare che il database di ripristino e hardware di **MBAM** sia configurato.

3. Nel server om in cui è configurato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che il database dello stato di conformità MBAM sia configurato.

4. Nel server in cui è configurata la funzionalità Report, aprire un Web browser utilizzando le credenziali amministrative e passare alla home page del sito SQL Server Reporting Services sito.
   
   Il percorso predefinito della home page di SQL Server Reporting Services'istanza del sito è il seguente: http(s):// *\<MBAM Reports Server Name\>* : *\<port\>* /Reports.aspx
   
   Per trovare l'URL effettivo, utilizzare lo strumento Gestione configurazione Reporting Services e selezionare le istanze specificate durante l'installazione.
   
5. Verificare che una cartella dei report denominata Amministrazione e monitoraggio di Microsoft BitLocker contenga un'origine dati denominata MaltaDataSource. Questa origine dati contiene cartelle con nomi che rappresentano le impostazioni locali della lingua, ad esempio en-us. I report sono nelle cartelle della lingua.

   > [!Note]
   > Se SQL Server Reporting Services (SSRS) è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http(s):// \<MBAM Reports Server Name\> : \<port\> /Reports_\<SSRS Instance Name\>
   >
   > Se SSRS non è stato configurato per l'utilizzo di SSL (Secure Socket Layer), l'URL per i report verrà impostato su "HTTP" anziché su "HTTPS" quando si installa il server MBAM. Se quindi si passa al sito Web di amministrazione e monitoraggio (noto anche come Helpdesk) e si seleziona un report, viene visualizzato il messaggio seguente: "Viene visualizzato solo il contenuto protetto". Per visualizzare il report, selezionare **Mostra tutto il contenuto.**

6. Nel server in cui è configurata la funzionalità Sito Web di amministrazione e monitoraggio, eseguire Server Manager, passare a Ruoli **e**quindi selezionare Gestione server **Web (IIS)**  >  **Internet Information Services (IIS).**

7. In **Connessioni**passare a e quindi selezionare Siti Amministrazione e monitoraggio \<computer name\> di Microsoft ****  >  **BitLocker.** Verificare che siano elencati i seguenti elementi:

   * MBAMAdministrationService
   * MBAMComplianceStatusService
   * MBAMRecoveryAndHardwareService

8. Nel server in cui sono configurati il sito Web di amministrazione e monitoraggio e Self-Service Portal, aprire un Web browser utilizzando le credenziali amministrative.

9. Accedere ai siti Web seguenti per verificare che il caricamento sia stato eseguito correttamente:
   * https(s):// \<MBAM Administration Server Name\> : \<port\> /HelpDesk/ (confermare ogni collegamento per lo spostamento e i report)
   * http(s):// \<MBAM Administration Server Name\> : \<port\> /SelfService/

   > [!Note]
   > Si presuppone che le funzionalità del server siano configurate sulla porta predefinita senza crittografia di rete. Se le funzionalità del server sono configurate su una porta o una directory virtuale diversa, modificare gli URL in modo da includere la porta appropriata. Ad esempio: http(s):// \<host name\> : \<port\> /HelpDesk/ http(s):// : / Se le funzionalità del server sono state configurate per l'utilizzo della crittografia di rete, modificare \<host name\> http:// in \<port\> / \<virtualdirectory\> https://.
   
10. Passare ai servizi Web seguenti per verificare che il caricamento sia stato eseguito correttamente. Verrà visualizzata una pagina per indicare che il servizio è in esecuzione. Tuttavia, la pagina non visualizza metadati.

    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMAdministrationService/AdministrationService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMUserSupportService/UserSupportService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMComplianceStatusService/StatusReportingService.svc
    * http(s):// \<MBAM Administration Server Name> : \<port> /MBAMRecoveryAndHardwareService/CoreService.svc

### <a name="step-12-configure-the-mbam-group-policy-templates"></a>Passaggio 12: Configurare i modelli di Criteri di gruppo MBAM

Per distribuire MBAM, è necessario impostare le impostazioni di Criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per Crittografia unità BitLocker. Per completare questa attività, è necessario copiare i modelli di Criteri di gruppo MBAM in un server o una workstation in grado di eseguire Console Gestione Criteri di gruppo (GPMC) o Gestione avanzata Criteri di gruppo (AGPM), quindi modificare le impostazioni.

> [!Important]
> Non modificare le impostazioni di Criteri di gruppo nel nodo Crittografia unità **BitLocker** o MBAM non funzionerà correttamente. Quando si configurano le impostazioni di Criteri di gruppo nel nodo **MDOP MBAM (Gestione BitLocker),** MBAM configura automaticamente le impostazioni di Crittografia unità **BitLocker** automaticamente.
 
#### <a name="copying-the-mbam-25-group-policy-templates"></a>Copia dei modelli di Criteri di gruppo di MBAM 2.5

Prima di installare il client MBAM, è necessario copiare oggetti Criteri di gruppo specifici di MBAM nella workstation di gestione. Questi oggetti Criteri di gruppo definiscono le impostazioni di implementazione di MBAM per BitLocker. È possibile copiare i modelli di Criteri di gruppo in qualsiasi server o workstation che sia un server o un computer client basato su Windows supportato e che possa eseguire Console Gestione Criteri di gruppo o Gestione avanzata Criteri di gruppo.

Per ulteriori informazioni, vedere [Copying the MBAM 2.5 Group Policy Templates](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/copying-the-mbam-25-group-policy-templates).
 
#### <a name="editing-mbam-25-gpo-settings"></a>Modifica delle impostazioni degli oggetti Criteri di gruppo di MBAM 2.5

Dopo aver creato gli oggetti Criteri di gruppo necessari, è necessario distribuire le impostazioni di Criteri di gruppo MBAM nei computer client dell'organizzazione. Per visualizzare e creare oggetti Criteri di gruppo, è necessario avere installato Console Gestione Criteri di gruppo (GPMC) o Gestione avanzata Criteri di gruppo (AGPM).

Per ulteriori informazioni, vedere [Editing the MBAM 2.5 Group Policy Impostazioni](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/editing-the-mbam-25-group-policy-settings) and Planning for [MBAM 2.5 Group Policy Requirements](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements).
 
### <a name="step-13-deploying-the-mbam-25-client"></a>Passaggio 13: Distribuzione del client MBAM 2.5

A seconda di quando si distribuisce il software Client di amministrazione e monitoraggio di Microsoft BitLocker, è possibile abilitare BitLocker in un computer dell'organizzazione prima che l'utente riceva il computer o successivamente configurando Criteri di gruppo e distribuendo il software client MBAM utilizzando un sistema di distribuzione del software aziendale.
 
#### <a name="deploy-the-mbam-client-to-desktop-or-portable-computers"></a>Distribuire il client MBAM in computer desktop o portatili

Dopo aver configurato le impostazioni di Criteri di gruppo, è possibile utilizzare un prodotto del sistema di distribuzione software aziendale, ad esempio Microsoft System Center 2012 Configuration Manager o Servizi di dominio Active Directory per distribuire i file di installazione del programma di installazione del client MBAM Windows nei computer di destinazione. È possibile utilizzare i file MbamClientSetup.exe a 32 bit o a 64 bit o i file MBAMClient.msi a 32 o 64 bit. Questi vengono forniti insieme al software del client MBAM.

Per ulteriori informazioni, vedere [How to Deploy the MBAM Client to Desktop or Laptop Computers](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25).
 
#### <a name="deploy-the-mbam-client-as-part-of-a-windows-deployment"></a>Distribuire il client MBAM come parte di una Windows distribuzione

Nelle organizzazioni in cui i computer vengono ricevuti e configurati centralmente, è possibile installare il client MBAM per gestire Crittografia unità BitLocker in ogni computer prima della scrittura dei dati degli utenti. Il vantaggio di questo processo è che ogni computer è quindi conforme a BitLocker. Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer. Un presupposto fondamentale per questo scenario è che il criterio dell'organizzazione consiste nell'installare un'immagine Windows aziendale prima che il computer venga recapitato all'utente. Se le impostazioni di Criteri di gruppo sono configurate per richiedere un PIN, agli utenti viene richiesto di impostare un PIN dopo aver ricevuto il criterio.

Per ulteriori informazioni, vedere [How to Deploy the MBAM Client as Part of a Windows Deployment](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25).
 
#### <a name="how-to-deploy-the-mbam-client-by-using-a-command-line"></a>Come distribuire il client MBAM tramite una riga di comando

Per ulteriori informazioni, [vedere How to Deploy the MBAM Client by Using a Command Line](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/how-to-deploy-the-mbam-client-by-using-a-command-line).

#### <a name="post-deployment-of-clients"></a>Post-distribuzione dei client

Dopo aver completato l'attività di distribuzione, è necessario esaminare i log seguenti e determinare se i client stanno segnalando correttamente al database MBAM.

## <a name="faq"></a>Domande frequenti

### <a name="how-to-create-a-load-balanced-iis-servers"></a>Come creare un server IIS con bilanciamento del carico

* L'SPN deve essere registrato solo con il nome descrittivo (ad esempio: bitlocker.corp.net) e non deve essere registrato nei singoli server IIS.

* Se si usa un certificato, il certificato deve avere nomi FQDN e NetBIOS immessi nel campo **Nome** alternativo soggetto per tutti i server IIS nel gruppo di bilanciamento del carico e anche come nome descrittivo (ad esempio: bitlocker.corp.net). In caso contrario, il certificato verrà segnalato come non attendibile dal browser quando si esplorano gli indirizzi con bilanciamento del carico.

Per ulteriori informazioni, vedere [Bilanciamento carico di rete IIS](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-high-availability#a-href-idbkmk-load-balanceaiis-network-load-balancing) e Registrazione degli [SPN per l'account del pool di applicazioni.](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-how-to-secure-the-mbam-websites#registering-spns-for-the-application-pool-account)

### <a name="how-to-configure-a-certificate"></a>Come configurare un certificato

* Sarà necessario disporre di due certificati. Un certificato viene utilizzato per SQL server e l'altro per IIS. Devono essere installati prima di avviare l'installazione di MBAM.

* È consigliabile utilizzare il programma di installazione per aggiungere il certificato alla configurazione di IIS anziché modificare manualmente il file web.config file.

* Il certificato non verrà accettato dal configuratore MBAM se il campo "Rilasciato a" nel certificato non corrisponde al nome del server. In questo caso, creare temporaneamente un certificato autofirmato dalla console di IIS e usarlo nel Configurator. In questo modo si assicura che le app Web siano installate per SSL e HTTPS. Successivamente, è possibile modificare il certificato in uno dai binding IIS per il sito Web MBAM.

### <a name="the-sql-permissions-requirement-for-installation"></a>Requisiti SQL autorizzazioni per l'installazione

Creare un account per il pool di app MBAM e assegnargli solo le autorizzazioni SecurityAdmin, Public e DBCreator.

Per [ulteriori informazioni, vedere Configurazione del database MBAM - Autorizzazioni](https://blogs.technet.microsoft.com/dubaisec/2016/02/02/mbam-database-configuration-minimum-permissions/) minime.

> [!Note]
> * In alcuni casi, sono necessarie ulteriori autorizzazioni per le operazioni di installazione e aggiornamento iniziali.
> * Utilizzare un account con sa temporanea per l'installazione.
> * Non avviare configuratore nel contesto di un account utente (RunAs) che non dispone di autorizzazioni sufficienti per apportare modifiche a SQL Server perché ciò causerà errori di installazione.
> * È necessario eseguire l'accesso utilizzando un account che dispone delle autorizzazioni per SQL Server. Solo SQL Server database possono essere creati o aggiornati eseguendo il Configuratore MBAM in remoto. Per il server SSRS, è necessario installare MBAM ed eseguire Configurator in locale per installare o aggiornare i report SSRS di MBAM.

### <a name="the-permission-required-for-spn-registration"></a>Autorizzazione necessaria per la registrazione SPN

Un account utilizzato per l'installazione del portale IIS deve disporre delle autorizzazioni SPN Write ServicePrincipalName e Write Validated. Senza queste autorizzazioni, l'installazione restituirà un messaggio di avviso che indica che non è possibile registrare l'SPN.

> [!Note]
> Questo messaggio di avviso verrà visualizzato due volte. Ciò non significa che all'SPN devono essere registrati due oggetti.

Per ulteriori informazioni, vedere [MbAM Setup fails with "Register SPN Deferred" error message](https://support.microsoft.com/help/2754138/).

### <a name="did-i-have-to-update-the-admx-templates-to-the-latest-version"></a>È stato necessario aggiornare i modelli ADMX alla versione più recente?

Vedrai più opzioni del sistema operativo nel nodo radice MBAM per l'oggetto Criteri di gruppo dopo aver aggiornato i modelli ADMX alle versioni più recenti. Ad esempio, Windows 7, Windows 8.1 e Windows 10 versione 1511 e versioni successive.

Per ulteriori informazioni su come aggiornare i modelli ADMX, vedere gli articoli seguenti:
* [Come scaricare e distribuire i modelli Criteri di gruppo MDOP (con estensione admx)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates)
* [Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/planning-for-mbam-25-group-policy-requirements)
* [Modelli amministrativi di Criteri di gruppo di Microsoft Desktop Optimization Pack](https://www.microsoft.com/en-us/download/details.aspx?id=55531)
