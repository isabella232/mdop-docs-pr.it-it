---
title: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 3.0
description: Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 3.0
author: dansimp
ms.assetid: d067f465-d7c8-4f6d-b311-66b9b06874f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f3f31808be82ec07d63bd0a9a2a402c9d7b693ea
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910491"
---
# <a name="step-by-step-guide-for-microsoft-advanced-group-policy-management-30"></a>Guida dettagliata per Gestione avanzata Criteri di gruppo Microsoft 3.0


Questa guida dettagliata illustra le tecniche avanzate per la gestione di Criteri di gruppo tramite Console Gestione Criteri di gruppo (GPMC) e Microsoft Advanced Group Policy Management (AGPM). AGPM aumenta le funzionalità della Console Gestione Criteri di gruppo, fornendo:

-   Ruoli standard per la delega delle autorizzazioni per gestire gli oggetti Criteri di gruppo (GPO) a più amministratori di Criteri di gruppo, nonché la possibilità di delegare l'accesso agli oggetti Criteri di gruppo nell'ambiente di produzione.

-   Archivio per consentire agli amministratori di Criteri di gruppo di creare e modificare gli oggetti Criteri di gruppo offline prima di distribuirli in un ambiente di produzione.

-   Possibilità di eseguire il rollback a qualsiasi versione precedente di un oggetto Criteri di gruppo nell'archivio e di limitare il numero di versioni archiviate nell'archivio.

-   Funzionalità di archiviazione/estrazione per gli oggetti Criteri di gruppo per garantire che gli amministratori di Criteri di gruppo non sovrascrivono inavvertitamente il lavoro dell'altro.

## <a name="agpm-scenario-overview"></a>Panoramica dello scenario AGPM


Per questo scenario, si utilizzerà un account utente separato per ogni ruolo in AGPM per dimostrare come è possibile gestire Criteri di gruppo in un ambiente con più amministratori di Criteri di gruppo con livelli di autorizzazioni diversi. In particolare, verranno eseguite le attività seguenti:

-   Utilizzando un account membro del gruppo Domain Admins, installare il server AGPM e assegnare il ruolo amministratore di AGPM a un account o a un gruppo.

-   Utilizzando gli account a cui verranno assegnati i ruoli di AGPM, installare il client AGPM.

-   Utilizzando un account con il ruolo di amministratore di AGPM, configurare AGPM e delegare l'accesso agli oggetti Criteri di gruppo assegnando ruoli ad altri account.

-   Utilizzando un account con il ruolo Editor, richiedere la creazione di un oggetto Criteri di gruppo, che viene quindi approvato utilizzando un account con il ruolo Responsabile approvazione. Con l'account Editor, estrarre l'oggetto Criteri di gruppo dall'archivio, modificare l'oggetto Criteri di gruppo, archiviare l'oggetto Criteri di gruppo nell'archivio e richiedere la distribuzione.

-   Utilizzando un account con il ruolo Responsabile approvazione, esaminare l'oggetto Criteri di gruppo e distribuirlo nell'ambiente di produzione.

-   Usando un account con il ruolo Editor, crea un modello di oggetto Criteri di gruppo e usalo come punto di partenza per creare un nuovo oggetto Criteri di gruppo.

-   Utilizzando un account con il ruolo Responsabile approvazione, eliminare e ripristinare un oggetto Criteri di gruppo.

![processo di sviluppo di oggetti Criteri di gruppo.](images/ab77a1f3-f430-4e7d-be58-ee8f9bd1140e.gif)

## <a name="requirements"></a>Requisiti


I computer in cui si desidera installare AGPM devono soddisfare i requisiti seguenti ed è necessario creare account da utilizzare in questo scenario.

**Nota**  
Se è installato AGPM 2.5 e si esegue l'aggiornamento da Windows Server® 2003 a Windows Server 2008 o Windows Vista® senza service pack installati Windows Vista con Service Pack 1, è necessario aggiornare il sistema operativo prima di eseguire l'aggiornamento a AGPM 3.0.

 

### <a name="agpm-server-requirements"></a>Requisiti del server AGPM

AGPM Server 3.0 richiede Windows Server 2008 o Windows Vista con Service Pack 1 e la Console Gestione Criteri di gruppo da Strumenti di amministrazione remota del server (RSAT) è installata. Sono supportate entrambe le versioni a 32 bit e a 64 bit.

Prima di installare il server AGPM, è necessario essere membri del gruppo Domain Admins e devono essere presenti le seguenti funzionalità di Windows se non diversamente specificato:

-   Console Gestione Criteri di gruppo

    -   Windows Server 2008: La Console Gestione Criteri di gruppo viene installata automaticamente da AGPM se non è presente.

    -   Windows Vista: è necessario installare la Console Gestione Criteri di gruppo da RSAT prima di installare AGPM. Per altre informazioni, vedi <https://go.microsoft.com/fwlink/?LinkID=116179>.

-   .NET Framework 3.5

Le seguenti Windows sono richieste dal server AGPM e verranno installate automaticamente se non presenti:

-   Attivazione WCF; Attivazione non HTTP

-   Servizio Attivazione dei processi Windows

    -   Modello di processo

    -   Ambiente .NET

    -   API di configurazione

### <a name="agpm-client-requirements"></a>Requisiti del client AGPM

AgPM Client 3.0 richiede Windows Server 2008 o Windows Vista con Service Pack 1 e la Console Gestione Criteri di gruppo da Strumenti di amministrazione remota del server (RSAT) installato. Sono supportate entrambe le versioni a 32 bit e a 64 bit. Il client AGPM può essere installato in un computer che esegue il server AGPM.

Le seguenti Windows sono richieste dal client AGPM e verranno installate automaticamente se non presenti se non diversamente specificato:

-   Console Gestione Criteri di gruppo

    -   Windows Server 2008: La Console Gestione Criteri di gruppo viene installata automaticamente da AGPM se non è presente.

    -   Windows Vista: è necessario installare la Console Gestione Criteri di gruppo da RSAT prima di installare AGPM. Per altre informazioni, vedi <https://go.microsoft.com/fwlink/?LinkID=116179>.

-   .NET Framework 3.0

### <a name="scenario-requirements"></a>Requisiti dello scenario

Prima di iniziare questo scenario, creare quattro account utente. Durante lo scenario, verrà assegnato uno dei ruoli agPM seguenti a ognuno di questi account: Amministratore DI AGPM (controllo completo), Responsabile approvazione, Editor e Revisore. Questi account devono essere in grado di inviare e ricevere messaggi di posta elettronica. Assegnare **l'autorizzazione Collega** oggetti Criteri di gruppo agli account con i ruoli amministratore, responsabile approvazione e (facoltativamente) editor di AGPM.

**Nota**  
**L'autorizzazione Collega oggetti** Criteri di gruppo viene assegnata ai membri di Domain Administrators e Enterprise Administrators per impostazione predefinita. Per **** assegnare l'autorizzazione Collega oggetti Criteri di gruppo ad altri utenti o gruppi (ad esempio account **** con i ruoli di amministratore o responsabile approvazione agPM), fare clic sul nodo relativo al dominio e quindi fare clic sulla scheda Delega, selezionare **Collega**oggetti Criteri di gruppo, fare clic su **Aggiungi**e selezionare gli utenti o i gruppi a cui assegnare l'autorizzazione.

 

## <a name="steps-for-installing-and-configuring-agpm"></a>Passaggi per l'installazione e la configurazione di AGPM


Per installare e configurare AGPM, è necessario completare la procedura seguente.

[Passaggio 1: Installare il server AGPM](#bkmk-config1)

[Passaggio 2: Installare il client AGPM](#bkmk-config2)

[Passaggio 3: Configurare una connessione al server AGPM](#bkmk-config3)

[Passaggio 4: Configurare la notifica tramite posta elettronica](#bkmk-config4)

[Passaggio 5: Delegare l'accesso](#bkmk-config5)

### <a name="step-1-install-agpm-server"></a><a href="" id="bkmk-config1"></a>Passaggio 1: Installare il server AGPM

In questo passaggio, si installa il server AGPM nel server membro o nel controller di dominio che eseguirà il servizio AGPM e si configura l'archivio. Tutte le operazioni di AGPM vengono gestite tramite questo Windows e vengono eseguite con le credenziali del servizio. L'archivio gestito da un server AGPM può essere ospitato in tale server o in un altro server nella stessa foresta.

**Per installare il server AGPM nel computer che ospiterà il servizio AGPM**

1.  Accedere con un account membro del gruppo Domain Admins.

2.  Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione avanzata Criteri di gruppo - Server.**

3.  Nella finestra **di dialogo** Benvenuto fare clic su **Avanti.**

4.  Nella finestra **di dialogo Condizioni di licenza** software Microsoft accettare le condizioni e fare clic su **Avanti.**

5.  Nella finestra **di dialogo Percorso** applicazione selezionare un percorso in cui installare il server AGPM. Il computer in cui è installato il server AGPM ospiterà il servizio AGPM e gestirà l'archivio. Fai clic su **Avanti**.

6.  Nella finestra **di dialogo Percorso** archivio selezionare un percorso per l'archivio relativo al server AGPM. Il percorso di archiviazione può puntare a una cartella nel server AGPM o altrove, ma è consigliabile selezionare un percorso con spazio sufficiente per archiviare tutti gli oggetti Criteri di gruppo e i dati della cronologia gestiti da questo server AGPM. Fai clic su **Avanti**.

7.  Nella finestra **di dialogo Account servizio AGPM** selezionare un account di servizio con cui verrà eseguito il servizio AGPM e quindi fare clic su **Avanti.**

8.  Nella finestra **di dialogo Proprietario** archivio selezionare un account o un gruppo a cui assegnare inizialmente il ruolo amministratore di AGPM (controllo completo). Questo amministratore di AGPM può assegnare ruoli e autorizzazioni di AGPM ad altri amministratori di Criteri di gruppo (incluso il ruolo di amministratore di AGPM). Per questo scenario, selezionare l'account da utilizzare nel ruolo di amministratore di AGPM. Fai clic su **Avanti**.

9.  Nella finestra **di dialogo Configurazione** porta digitare una porta su cui il servizio AGPM deve restare in attesa. Non deselezionare la casella di controllo Aggiungi eccezione porta **al firewall** a meno che non si configurano manualmente le eccezioni di porta o si utilizzino regole per configurare le eccezioni di porta. Fai clic su **Avanti**.

10. Nella finestra **di dialogo** Lingue selezionare una o più lingue di visualizzazione da installare per il server AGPM.

11. Fare **clic su**Installa e quindi su **Fine** per uscire dall'Installazione guidata.

    **Attenzione**  
    Non modificare le impostazioni per il servizio AGPM tramite **Strumenti di** amministrazione **e servizi** nel sistema operativo. Questa operazione può impedire l'avvio del servizio AGPM. Per informazioni su come modificare le impostazioni per il servizio, vedere la Guida per Gestione avanzata Criteri di gruppo.

     

### <a name="step-2-install-agpm-client"></a><a href="" id="bkmk-config2"></a>Passaggio 2: Installare il client AGPM

Ogni amministratore di Criteri di gruppo, ovvero chiunque crei, modifica, distribuisca, rivede o elimini oggetti Criteri di gruppo, deve disporre di Client AGPM installato nei computer utilizzati per gestire gli oggetti Criteri di gruppo. Per questo scenario, si installa il client AGPM in almeno un computer. Non è necessario installare il client AGPM nei computer degli utenti finali che non eseguono l'amministrazione di Criteri di gruppo.

**Per installare il client AGPM nel computer di un amministratore di Criteri di gruppo**

1.  Avviare il CD di Microsoft Desktop Optimization Pack e seguire le istruzioni visualizzate per selezionare **Gestione avanzata Criteri di gruppo - Client.**

2.  Nella finestra **di dialogo** Benvenuto fare clic su **Avanti.**

3.  Nella finestra **di dialogo Condizioni di licenza** software Microsoft accettare le condizioni e fare clic su **Avanti.**

4.  Nella finestra **di dialogo Percorso** applicazione selezionare un percorso in cui installare il client AGPM. Fai clic su **Avanti**.

5.  Nella finestra **di dialogo Server AGPM** digitare il nome computer completo per il server AGPM e la porta a cui connettersi. La porta predefinita per il servizio AGPM è 4600. Non deselezionare la casella di controllo **Consenti Microsoft Management Console** attraverso il firewall a meno che non si configurano manualmente le eccezioni alle porte o si utilizzino regole per configurare le eccezioni di porta. Fai clic su **Avanti**.

6.  Nella finestra **di dialogo** Lingue selezionare una o più lingue di visualizzazione da installare per il client AGPM.

7.  Fare **clic su**Installa e quindi su **Fine** per uscire dall'Installazione guidata.

### <a name="step-3-configure-an-agpm-server-connection"></a><a href="" id="bkmk-config3"></a>Passaggio 3: Configurare una connessione al server AGPM

AGPM archivia tutte le versioni di ogni oggetto Criteri di gruppo controllato , ovvero un oggetto Criteri di gruppo per il quale AGPM fornisce il controllo delle modifiche, in un archivio centrale, in modo che gli amministratori di Criteri di gruppo possano visualizzare e modificare gli oggetti Criteri di gruppo offline senza influire immediatamente sulla versione distribuita di ogni oggetto Criteri di gruppo.

In questo passaggio si configura una connessione al server AGPM e si garantisce che tutti gli amministratori di Criteri di gruppo si connettono allo stesso server AGPM. Per informazioni sulla configurazione di più server AGPM, vedere la Guida di Gestione avanzata Criteri di gruppo.

**Per configurare una connessione al server AGPM per tutti gli amministratori di Criteri di gruppo**

1.  In un computer in cui è stato installato il client AGPM, accedere con l'account utente selezionato come proprietario dell'archivio. Questo utente ha il ruolo di amministratore di AGPM (controllo completo).

2.  Fare clic sul pulsante **Start,** **scegliere Strumenti di**amministrazione e quindi Gestione Criteri di **gruppo** per aprire la Console Gestione Criteri di gruppo.

3.  Modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori di Criteri di gruppo.

4.  Nella finestra **Editor Gestione Criteri** di gruppo fare doppio clic su **Configurazione** **utente,** **Criteri,** Modelli amministrativi, **Windows componenti**e **AGPM.**

5.  Nel riquadro dei dettagli fare doppio clic su **AGPM: Specificare il server AGPM predefinito (tutti i domini).**

6.  Nella finestra **Proprietà** selezionare **Abilitato** e digitare il nome completo del computer e la porta (ad esempio, **server.contoso.com:4600**) per il server che ospita l'archivio. Per impostazione predefinita, il servizio AGPM utilizza la porta 4600.

7.  Fare **clic su OK**e quindi chiudere la finestra Editor Gestione Criteri **di** gruppo. Quando Criteri di gruppo viene aggiornato, la connessione al server AGPM viene configurata per ogni amministratore di Criteri di gruppo.

### <a name="step-4-configure-e-mail-notification"></a><a href="" id="bkmk-config4"></a>Passaggio 4: Configurare la notifica tramite posta elettronica

L'amministratore di AGPM (controllo completo) designa gli indirizzi di posta elettronica dei responsabili approvazione e degli amministratori di AGPM a cui viene inviato un messaggio di posta elettronica contenente una richiesta quando un editor tenta di creare, distribuire o eliminare un oggetto Criteri di gruppo. È inoltre possibile determinare l'alias da cui vengono inviati questi messaggi.

**Per configurare la notifica tramite posta elettronica per AGPM**

1.  Nel riquadro dei dettagli fare clic sulla **scheda Delega** dominio.

2.  Nel campo **Indirizzo di posta elettronica mittente** digitare l'alias di posta elettronica per AGPM da cui inviare le notifiche.

3.  Nel campo **A indirizzo di posta** elettronica digitare l'indirizzo di posta elettronica dell'account utente a cui si desidera assegnare il ruolo responsabile approvazione.

4.  Nel campo **Server SMTP** digitare un server di posta SMTP valido.

5.  Nei campi **Nome utente** **e Password** digitare le credenziali di un utente con accesso al servizio SMTP. Fai clic su **Applica**.

### <a name="step-5-delegate-access"></a><a href="" id="bkmk-config5"></a>Passaggio 5: Delegare l'accesso

In quanto amministratore di AGPM (controllo completo), si delega l'accesso a livello di dominio agli oggetti Criteri di gruppo, assegnando ruoli all'account di ogni amministratore di Criteri di gruppo.

**Nota**  
È inoltre possibile delegare l'accesso a livello di oggetto Criteri di gruppo anziché a livello di dominio. Per informazioni dettagliate, vedere la Guida per Gestione avanzata Criteri di gruppo.

 

**Importante**  
È consigliabile limitare l'appartenenza al gruppo Proprietari creatori criteri di gruppo, in modo che non possa essere utilizzata per aggirare la gestione agPM dell'accesso agli oggetti Criteri di gruppo. In Console Gestione Criteri di **** gruppo **fare**clic su Oggetti Criteri di gruppo nella **** foresta e nel dominio in cui si desidera gestire gli oggetti Criteri di gruppo, fare clic su Delega e quindi configurare le impostazioni per soddisfare le esigenze dell'organizzazione.

 

**Per delegare l'accesso a tutti gli oggetti Criteri di gruppo in un dominio**

1.  Nella scheda **Delega dominio** **** fare clic sul pulsante Aggiungi, selezionare l'account utente dell'amministratore di Criteri di gruppo da utilizzare come responsabile approvazione e quindi fare clic su **OK.**

2.  Nella finestra **di dialogo Aggiungi gruppo** o utente selezionare il ruolo **Responsabile** approvazione per assegnare tale ruolo all'account e quindi fare clic su **OK.** Questo ruolo include il ruolo Revisore.

3.  Fare clic **sul pulsante** Aggiungi, selezionare l'account utente dell'amministratore di Criteri di gruppo da utilizzare come editor e quindi fare clic su **OK.**

4.  Nella finestra **di dialogo Aggiungi gruppo o** utente selezionare il ruolo **Editor** per assegnare il ruolo all'account e quindi fare clic su **OK.** Questo ruolo include il ruolo Revisore.

5.  Fare clic **sul** pulsante Aggiungi, selezionare l'account utente dell'amministratore di Criteri di gruppo da utilizzare come revisore e quindi fare clic su **OK.**

6.  Nella finestra **di dialogo Aggiungi gruppo o** utente selezionare il ruolo **Revisore** per assegnare solo tale ruolo all'account.

## <a name="steps-for-managing-gpos"></a>Passaggi per la gestione degli oggetti Criteri di gruppo


È necessario completare i passaggi seguenti per creare, modificare, rivedere e distribuire oggetti Criteri di gruppo tramite AGPM. Inoltre, verrà creato un modello, verrà eliminato un oggetto Criteri di gruppo e verrà ripristinato un oggetto Criteri di gruppo eliminato.

[Passaggio 1: Creare un oggetto Criteri di gruppo](#bkmk-manage1)

[Passaggio 2: Modificare un oggetto Criteri di gruppo](#bkmk-manage2)

[Passaggio 3: Esaminare e distribuire un oggetto Criteri di gruppo](#bkmk-manage3)

[Passaggio 4: Utilizzare un modello per creare un oggetto Criteri di gruppo](#bkmk-manage4)

[Passaggio 5: Eliminare e ripristinare un oggetto Criteri di gruppo](#bkmk-manage5)

### <a name="step-1-create-a-gpo"></a><a href="" id="bkmk-manage1"></a>Passaggio 1: Creare un oggetto Criteri di gruppo

In un ambiente con più amministratori di Criteri di gruppo, gli utenti con il ruolo Editor hanno la possibilità di richiedere la creazione di nuovi oggetti Criteri di gruppo, ma tale richiesta deve essere approvata da un utente con il ruolo responsabile approvazione perché la creazione di un nuovo oggetto Criteri di gruppo influisce sull'ambiente di produzione.

In questo passaggio si utilizza un account con il ruolo Editor per richiedere la creazione di un nuovo oggetto Criteri di gruppo. L'utilizzo di un account con il ruolo Responsabile approvazione consente di approvare questa richiesta e completare la creazione di un oggetto Criteri di gruppo.

**Per richiedere la creazione di un nuovo oggetto Criteri di gruppo gestito tramite AGPM**

1.  In un computer in cui è stato installato il client AGPM, accedere con un account utente a cui è stato assegnato il ruolo Editor in AGPM.

2.  **Nell'albero della Console Gestione Criteri** di gruppo fare clic su **Cambia** controllo nella foresta e nel dominio in cui si desidera gestire gli oggetti Criteri di gruppo.

3.  Fare clic con il pulsante destro **del mouse sul** nodo Cambia controllo e quindi scegliere Nuovo oggetto Criteri di gruppo **controllato.**

4.  Nella finestra **di dialogo Nuovo oggetto Criteri** di gruppo controllato:

    1.  Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel **campo Cc.**

    2.  Digitare **MyGPO** come nome per il nuovo oggetto Criteri di gruppo.

    3.  Digitare un commento per il nuovo oggetto Criteri di gruppo.

    4.  Fare **clic su Crea in** tempo reale in modo che il nuovo oggetto Criteri di gruppo verrà distribuito nell'ambiente di produzione subito dopo l'approvazione. Fai clic su **Invia**.

5.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** Il nuovo oggetto Criteri di gruppo viene visualizzato nella **scheda In** sospeso.

**Per approvare la richiesta in sospeso per creare un oggetto Criteri di gruppo**

1.  In un computer in cui è stato installato il client AGPM, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione in AGPM.

2.  Aprire la posta in arrivo per l'account e notare che è stato ricevuto un messaggio di posta elettronica dall'alias di AGPM con la richiesta dell'editor di creare un oggetto Criteri di gruppo.

3.  **Nell'albero della Console Gestione Criteri** di gruppo fare clic su **Cambia** controllo nella foresta e nel dominio in cui si desidera gestire gli oggetti Criteri di gruppo.

4.  Nella scheda **Contenuto** fare clic sulla scheda **In** sospeso per visualizzare gli oggetti Criteri di gruppo in sospeso.

5.  Fare clic con il **pulsante destro del mouse su MyGPO**e quindi scegliere **Approva**.

6.  Fare **clic su Sì** per confermare l'approvazione della creazione dell'oggetto Criteri di gruppo. L'oggetto Criteri di gruppo viene spostato nella **scheda** Controllato.

### <a name="step-2-edit-a-gpo"></a><a href="" id="bkmk-manage2"></a>Passaggio 2: Modificare un oggetto Criteri di gruppo

È possibile utilizzare gli oggetti Criteri di gruppo per configurare le impostazioni del computer o degli utenti e distribuirli a molti computer o utenti. In questo passaggio si utilizza un account con il ruolo Editor per estrarre un oggetto Criteri di gruppo dall'archivio, modificare l'oggetto Criteri di gruppo offline, archiviare l'oggetto Criteri di gruppo modificato nell'archivio e richiedere la distribuzione dell'oggetto Criteri di gruppo nell'ambiente di produzione. Per questo scenario, si configura un'impostazione nell'oggetto Criteri di gruppo per richiedere che la password sia lunga almeno otto caratteri.

**Per estrarre l'oggetto Criteri di gruppo dall'archivio per la modifica**

1.  In un computer in cui è stato installato il client AGPM, accedere con un account utente a cui è stato assegnato il ruolo di Editor in AGPM.

2.  **Nell'albero della Console Gestione Criteri** di gruppo fare clic su **Cambia** controllo nella foresta e nel dominio in cui si desidera gestire gli oggetti Criteri di gruppo.

3.  Nella scheda **Contenuto** del riquadro dei dettagli fare clic sulla **scheda Controllato** per visualizzare gli oggetti Criteri di gruppo controllati.

4.  Fare clic con il pulsante destro del mouse su **MyGPO**e **quindi scegliere Estrai**.

5.  Digitare un commento da visualizzare nella cronologia dell'oggetto Criteri di gruppo durante l'estrazione e quindi fare clic su **OK.**

6.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** Nella scheda **Controllato** lo stato dell'oggetto Criteri di gruppo è identificato come **Estratto.**

**Per modificare l'oggetto Criteri di gruppo offline e configurare la lunghezza minima della password**

1.  Nella scheda **Controllato** fare clic con il pulsante **** destro del mouse su **MyGPO**e quindi scegliere Modifica per aprire la finestra **Editor** Gestione Criteri di gruppo e apportare modifiche a una copia offline dell'oggetto Criteri di gruppo. Per questo scenario, configurare la lunghezza minima della password:

    1.  In **Configurazione computer**fare doppio clic su **Criteri**, **Windows Impostazioni**, Sicurezza **Impostazioni** **,** Criteri account e Criteri **password**.

    2.  Nel riquadro dei dettagli fare doppio clic su **Lunghezza minima password**.

    3.  Nella finestra delle proprietà selezionare la casella **di** controllo Definisci questo criterio, impostare il numero di caratteri su **8**e quindi fare clic su **OK.**

2.  Chiudere la **finestra Editor Gestione Criteri di** gruppo.

**Per archiviare l'oggetto Criteri di gruppo nell'archivio**

1.  Nella scheda **Controllato** fare clic con il pulsante destro del mouse su **MyGPO** e quindi **scegliere Archivia**.

2.  Digitare un commento e quindi fare clic su **OK.**

3.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** Nella scheda **Controllato** lo stato dell'oggetto Criteri di gruppo è identificato come **Archiviato.**

**Per richiedere la distribuzione dell'oggetto Criteri di gruppo nell'ambiente di produzione**

1.  Nella scheda **Controllato** fare clic con il pulsante destro del mouse su **MyGPO** e quindi scegliere **Distribuisci**.

2.  Poiché questo account non è un responsabile approvazione o un amministratore di AGPM, è necessario inviare una richiesta per la distribuzione. Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel **campo Cc.** Digitare un commento da visualizzare nella cronologia dell'oggetto Criteri di gruppo e quindi fare clic su **Invia.**

3.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** **MyGPO** viene visualizzato nell'elenco degli oggetti Criteri di gruppo nella **scheda In** sospeso.

### <a name="step-3-review-and-deploy-a-gpo"></a><a href="" id="bkmk-manage3"></a>Passaggio 3: Esaminare e distribuire un oggetto Criteri di gruppo

In questo passaggio, si agisce come responsabile approvazione, creando report e analizzando le impostazioni e le modifiche alle impostazioni nell'oggetto Criteri di gruppo per determinare se approvarle. Dopo aver valutato l'oggetto Criteri di gruppo, è possibile distribuirlo nell'ambiente di produzione e collegarlo a un dominio o a un'unità organizzativa in modo che sia effettiva quando i Criteri di gruppo vengono aggiornati per i computer in tale dominio o unità organizzativa.

**Per esaminare le impostazioni nell'oggetto Criteri di gruppo**

1. In un computer in cui è stato installato il client AGPM, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione in AGPM. Qualsiasi amministratore di Criteri di gruppo con il ruolo Revisore, incluso in tutti gli altri ruoli, può esaminare le impostazioni in un oggetto Criteri di gruppo.

2. Aprire la posta in arrivo per l'account e notare che è stato ricevuto un messaggio di posta elettronica dall'alias di AGPM con una richiesta dell'editore per distribuire un oggetto Criteri di gruppo.

3. **Nell'albero della Console Gestione Criteri** di gruppo fare clic su **Cambia** controllo nella foresta e nel dominio in cui si desidera gestire gli oggetti Criteri di gruppo.

4. Nella scheda **Contenuto** del riquadro dei dettagli fare clic sulla **scheda In** sospeso.

5. Fare doppio clic **su MyGPO per** visualizzarne la cronologia.

6. Esaminare le impostazioni nella versione più recente di MyGPO:

   1.  Nella finestra **Cronologia** fare clic con il pulsante destro del mouse sulla versione dell'oggetto Criteri di gruppo con il timestamp più recente, scegliere **Impostazioni**e quindi report **HTML** per visualizzare un riepilogo delle impostazioni dell'oggetto Criteri di gruppo.

   2.  Nel Web browser fare clic su **Mostra tutto** per visualizzare tutte le impostazioni nell'oggetto Criteri di gruppo. Chiudi il browser.

7. Confrontare la versione più recente di MyGPO con la prima versione archiviata nell'archivio:

   1. Nella finestra **Cronologia** fare clic sulla versione dell'oggetto Criteri di gruppo con il timestamp più recente. Premere CTRL e fare clic sulla versione meno recente dell'oggetto Criteri di gruppo per cui la versione **computer** non è **\\***.

   2. Fare clic **sul pulsante** Differenze. La **sezione Criteri account/Criteri password** è evidenziata in verde e preceduta da **\[+\]**, a indicare che questa impostazione è configurata solo nell'ultima versione dell'oggetto Criteri di gruppo.

   3. Fare **clic su Criteri account/Criteri password.** L'impostazione Lunghezza **minima password** è evidenziata anche in verde e preceduta da **\[+\]**, a indicare che è configurata solo nell'ultima versione dell'oggetto Criteri di gruppo.

   4. Chiudere il Web browser.

**Per distribuire l'oggetto Criteri di gruppo nell'ambiente di produzione**

1.  Nella scheda **In** sospeso fare clic con il pulsante destro del mouse su **MyGPO** e quindi scegliere **Approva**.

2.  Digitare un commento da includere nella cronologia dell'oggetto Criteri di gruppo.

3.  Fai clic su **Sì**. Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** L'oggetto Criteri di gruppo viene distribuito nell'ambiente di produzione.

**Per collegare l'oggetto Criteri di gruppo a un dominio o a un'unità organizzativa**

1.  Nella Console Gestione Criteri di gruppo fare clic con il pulsante destro del mouse sul dominio o su un'unità organizzativa a cui applicare l'oggetto Criteri di gruppo configurato e quindi scegliere Collega un oggetto Criteri **di gruppo esistente.**

2.  Nella finestra **di dialogo Seleziona oggetto Criteri** di gruppo fare clic su **MyGPO**e quindi su **OK.**

### <a name="step-4-use-a-template-to-create-a-gpo"></a><a href="" id="bkmk-manage4"></a>Passaggio 4: Utilizzare un modello per creare un oggetto Criteri di gruppo

In questo passaggio si utilizza un account con il ruolo Editor per creare un modello, ovvero una versione statica non modificabile di un oggetto Criteri di gruppo da utilizzare come punto di partenza per la creazione di nuovi oggetti Criteri di gruppo, e quindi creare un nuovo oggetto Criteri di gruppo basato su tale modello. I modelli sono utili per creare rapidamente più oggetti Criteri di gruppo che includono molte delle stesse impostazioni.

**Per creare un modello basato su un oggetto Criteri di gruppo esistente**

1.  In un computer in cui è stato installato il client AGPM, accedere con un account utente a cui è stato assegnato il ruolo di Editor in AGPM.

2.  **Nell'albero della Console Gestione Criteri** di gruppo fare clic su **Cambia** controllo nella foresta e nel dominio in cui si desidera gestire gli oggetti Criteri di gruppo.

3.  Nella scheda **Contenuto** del riquadro dei dettagli fare clic sulla **scheda** Controllato.

4.  Fare clic con il pulsante **** destro del mouse su **MyGPO**e quindi scegliere Salva come modello per creare un modello che incorpora tutte le impostazioni attualmente in MyGPO.

5.  Digitare **MyTemplate** come nome per il modello e un commento e quindi fare clic su **OK.**

6.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** Il nuovo modello viene visualizzato nella **scheda** Modelli.

**Per richiedere la creazione di un nuovo oggetto Criteri di gruppo gestito tramite AGPM**

1.  Fare clic **sulla scheda** Controllato.

2.  Fare clic con il pulsante destro **del mouse sul** nodo Cambia controllo e quindi scegliere Nuovo oggetto Criteri di gruppo **controllato.**

3.  Nella finestra **di dialogo Nuovo oggetto Criteri** di gruppo controllato:

    1.  Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel **campo Cc.**

    2.  Digitare **MyOtherGPO** come nome per il nuovo oggetto Criteri di gruppo.

    3.  Digitare un commento per il nuovo oggetto Criteri di gruppo.

    4.  Fare **clic su Crea live,** in modo che il nuovo oggetto Criteri di gruppo verrà distribuito nell'ambiente di produzione subito dopo l'approvazione.

    5.  Per **Da modello oggetto Criteri di**gruppo, selezionare **MyTemplate.** Fai clic su **Invia**.

4.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** Il nuovo oggetto Criteri di gruppo viene visualizzato nella **scheda In** sospeso.

Utilizzare un account a cui è stato assegnato il ruolo di responsabile approvazione per approvare la richiesta in sospeso per creare l'oggetto Criteri di gruppo come nel [passaggio 1:](#bkmk-manage1)creare un oggetto Criteri di gruppo. MyTemplate incorpora tutte le impostazioni configurate in MyGPO. Poiché MyOtherGPO è stato creato con MyTemplate, inizialmente contiene tutte le impostazioni contenute in MyGPO al momento della creazione di MyTemplate. Puoi confermarlo generando un report delle differenze per confrontare MyOtherGPO con MyTemplate.

**Per estrarre l'oggetto Criteri di gruppo dall'archivio per la modifica**

1.  In un computer in cui è stato installato il client AGPM, accedere con un account utente a cui è stato assegnato il ruolo di Editor in AGPM.

2.  Fare clic con il **pulsante destro del mouse su MyOtherGPO**e quindi scegliere **Estrai**.

3.  Digitare un commento da visualizzare nella cronologia dell'oggetto Criteri di gruppo durante l'estrazione e quindi fare clic su **OK.**

4.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** Nella scheda **Controllato** lo stato dell'oggetto Criteri di gruppo è identificato come **Estratto.**

**Per modificare l'oggetto Criteri di gruppo offline e configurare la durata del blocco dell'account**

1.  Nella scheda **Controllato** fare clic con il pulsante destro **** del mouse su **MyOtherGPO**e quindi scegliere Modifica per aprire la finestra **Editor** Gestione Criteri di gruppo e apportare modifiche a una copia offline dell'oggetto Criteri di gruppo. Per questo scenario, configurare la lunghezza minima della password:

    1.  In **Configurazione computer**fare doppio clic su **Criteri** **, Windows Impostazioni**, Sicurezza **Impostazioni** **,** Criteri account e Criteri di **blocco account**.

    2.  Nel riquadro dei dettagli fare doppio clic su **Durata blocco account.**

    3.  Nella finestra delle proprietà seleziona Definisci **questa impostazione di criterio,** imposta la durata **su 30** minuti e quindi fai clic su **OK.**

2.  Chiudere la **finestra Editor Gestione Criteri di** gruppo.

Archiviare MyOtherGPO nell'archivio e richiedere la distribuzione come per MyGPO nel [passaggio 2: modificare un oggetto Criteri di gruppo.](#bkmk-manage2) Puoi confrontare MyOtherGPO con MyGPO o Con MyTemplate usando i rapporti sulle differenze. Qualsiasi account che includa il ruolo Revisore (Amministratore AGPM \[Controllo completo\], Responsabile approvazione, Editor o Revisore) può generare report.

**Per confrontare un oggetto Criteri di gruppo con un altro oggetto Criteri di gruppo e con un modello**

1.  Per confrontare MyGPO e MyOtherGPO:

    1.  Nella scheda **Controllato** fare clic su **MyGPO.** Premere CTRL e quindi fare clic **su MyOtherGPO.**

    2.  Fare clic con il pulsante destro del mouse su **MyOtherGPO,** scegliere **Differenze**e fare clic su **Report HTML.**

2.  Per confrontare MyOtherGPO e MyTemplate:

    1.  Nella scheda **Controllato** fare clic **su MyOtherGPO.**

    2.  Fare clic con il pulsante destro del mouse su **MyOtherGPO,** scegliere **Differenze**e fare clic su **Modello.**

    3.  Selezionare **MyTemplate** e **Report HTML**e quindi fare clic su **OK.**

### <a name="step-5-delete-and-restore-a-gpo"></a><a href="" id="bkmk-manage5"></a>Passaggio 5: Eliminare e ripristinare un oggetto Criteri di gruppo

In questo passaggio si agisce come responsabile approvazione per eliminare un oggetto Criteri di gruppo.

**Per eliminare un oggetto Criteri di gruppo**

1.  In un computer in cui è stato installato il client AGPM, accedere con un account utente a cui è stato assegnato il ruolo di responsabile approvazione.

2.  **Nell'albero della Console Gestione Criteri** di gruppo fare clic su **Cambia** controllo nella foresta e nel dominio in cui si desidera gestire gli oggetti Criteri di gruppo.

3.  Nella scheda **Contenuto** fare clic sulla **scheda Controllato** per visualizzare gli oggetti Criteri di gruppo controllati.

4.  Fare clic con il **pulsante destro del mouse su MyGPO**e quindi scegliere **Elimina.** Fare **clic su Elimina oggetto** Criteri di gruppo dall'archivio e dalla produzione per eliminare sia la versione nell'archivio che la versione distribuita dell'oggetto Criteri di gruppo nell'ambiente di produzione.

5.  Digitare un commento da visualizzare nell'audit trail per l'oggetto Criteri di gruppo e quindi fare clic su **OK.**

6.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** L'oggetto Criteri di gruppo viene rimosso **dalla** scheda Controllato e visualizzato nella scheda **Cestino,** dove può essere ripristinato o eliminato.

In alcuni casi è possibile che dopo l'eliminazione di un oggetto Criteri di gruppo sia ancora necessario. In questo passaggio, si agisce come responsabile approvazione per ripristinare un oggetto Criteri di gruppo che è stato eliminato.

**Per ripristinare un oggetto Criteri di gruppo eliminato**

1.  Nella scheda **Contenuto** fare clic sulla scheda **Cestino** per visualizzare gli oggetti Criteri di gruppo eliminati.

2.  Fare clic con il **pulsante destro del mouse su MyGPO**e quindi scegliere **Ripristina**.

3.  Digitare un commento da visualizzare nella cronologia dell'oggetto Criteri di gruppo e quindi fare clic su **OK.**

4.  Quando la **finestra Stato agPM** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** L'oggetto Criteri di gruppo viene rimosso **dalla scheda Cestino** e visualizzato nella **scheda** Controllato.

    **Nota**  
    Il ripristino di un oggetto Criteri di gruppo nell'archivio non lo ridistribuisce automaticamente nell'ambiente di produzione. Per restituire l'oggetto Criteri di gruppo all'ambiente di produzione, distribuire l'oggetto Criteri di gruppo come nel [passaggio 3: esaminare e distribuire un oggetto Criteri di gruppo.](#bkmk-manage3)

     

Dopo aver modificato e distribuito un oggetto Criteri di gruppo, è possibile che le modifiche recenti all'oggetto Criteri di gruppo causano un problema. In questo passaggio si funge da responsabile approvazione per eseguire il rollback a una versione precedente dell'oggetto Criteri di gruppo. È possibile eseguire il rollback a qualsiasi versione nella cronologia dell'oggetto Criteri di gruppo. È possibile utilizzare commenti ed etichette per identificare le versioni buone note e quando sono state apportate modifiche specifiche.

**Per eseguire il rollback a una versione precedente di un oggetto Criteri di gruppo**

1.  Nella scheda **Contenuto** fare clic sulla **scheda Controllato** per visualizzare gli oggetti Criteri di gruppo controllati.

2.  Fare doppio clic **su MyGPO per** visualizzarne la cronologia.

3.  Fare clic con il pulsante destro del mouse sulla versione da distribuire, **scegliere Distribuisci**e quindi fare clic su **Sì.**

4.  Quando la **finestra Stato** indica che l'avanzamento complessivo è stato completato, fare clic su **Chiudi.** Nella finestra **Cronologia** fare clic su **Chiudi.**

    **Nota**  
    Per verificare che la versione ridistribuito sia quella prevista, esaminare un report delle differenze per le due versioni. Nella finestra **Cronologia** dell'oggetto Criteri di gruppo selezionare le due versioni, fare clic con il pulsante destro del mouse su di esse, scegliere **Differenza**e quindi report **HTML** o **Report XML.**

     

 

 





