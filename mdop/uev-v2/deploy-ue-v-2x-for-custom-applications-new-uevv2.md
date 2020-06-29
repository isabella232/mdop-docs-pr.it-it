---
title: Distribuire UE-V 2. x per le applicazioni personalizzate
description: Distribuire UE-V 2. x per le applicazioni personalizzate
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824405"
---
# Distribuire UE-V 2. x per le applicazioni personalizzate


Microsoft User Experience Virtualization (UE-V) 2,0. 2,1 e 2,1 SP1 usano i file XML denominati **modelli di posizione delle impostazioni** per monitorare e sincronizzare le impostazioni delle applicazioni desktop e le impostazioni desktop di Windows tra i computer degli utenti. Per impostazione predefinita, alcuni modelli di percorsi impostazioni sono inclusi in UE-V. Se invece si vogliono sincronizzare le impostazioni per le applicazioni desktop diverse da quelle incluse nei modelli predefiniti, è possibile creare modelli di posizione personalizzati con il generatore di impostazioni personalizzate.

Dopo aver letto il materiale per la pianificazione in [preparare una distribuzione di UE-v 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) e aver deciso di sincronizzare le impostazioni per le applicazioni personalizzate (di terze parti, line-of-business e così via), verranno distribuite le caratteristiche di UE-v come descritto in questo argomento. Per iniziare, ecco i passaggi principali necessari per sincronizzare le impostazioni per le applicazioni personalizzate:

-   [Installare il generatore di UEV](#uevgen)

    Usa il generatore UEV per creare modelli di posizione delle impostazioni XML personalizzati.

-   [Configurare un catalogo di modelli di impostazioni UE-V](#deploycatalogue)

    Puoi definire questo percorso in cui vengono archiviati i modelli di posizione delle impostazioni personalizzate.

-   [Creare modelli di posizione delle impostazioni personalizzate](#createcustomtemplates)

    Questi modelli personalizzati consentono agli utenti di sincronizzare le impostazioni per le applicazioni personalizzate.

-   [Distribuire i modelli di posizione delle impostazioni personalizzate](#deploycustomtemplates)

    Dopo aver testato il modello personalizzato per verificare che le impostazioni vengano sincronizzate correttamente, è possibile distribuire questi modelli in uno dei modi seguenti:

    -   Tramite l'infrastruttura di distribuzione esistente, ad esempio Configuration Manager

    -   Usando le preferenze di criteri di gruppo

    -   [Distribuire un catalogo di modelli di impostazioni UE-V](#deploycatalogue)

    **Nota**  I modelli distribuiti tramite ESD o criteri di gruppo devono essere registrati con Strumentazione gestione Windows (WMI) di UE-V o Windows PowerShell.

     

## Preparare la distribuzione di UE-V 2. x per le applicazioni personalizzate


Prima di iniziare a distribuire le funzionalità UE-V che gestiscono le applicazioni personalizzate, è possibile esaminare solo un paio di elementi.

### Generatore UE-V

Il generatore di UE-V monitora un'applicazione per individuare e acquisire le posizioni in cui vengono archiviate le impostazioni dell'applicazione. L'applicazione monitorata deve essere un'applicazione tradizionale. Si usa il generatore UE-V per creare modelli di posizione delle impostazioni, ma non è possibile creare un modello di posizione delle impostazioni da questi tipi di applicazione:

-   Applicazioni virtualizzate

-   Applicazioni offerte tramite Servizi terminal

-   Applicazioni Java

-   App di Windows  

**Nota**  Non è possibile creare modelli di posizione delle impostazioni di UE-V da applicazioni virtualizzate o Servizi terminal. Tuttavia, le impostazioni sincronizzate con i modelli possono essere applicate a tali applicazioni. Per creare modelli che supportano le applicazioni VDI (Virtual Desktop Infrastructure) e Servizi terminal, aprire una versione del pacchetto di Windows Installer (con estensione msi) dell'applicazione usando il generatore UE-V. Per altre informazioni sulla sincronizzazione delle impostazioni per le applicazioni virtuali, vedere [uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).

 

**Percorsi esclusi:** Il processo di individuazione esclude le posizioni che in genere archiviano i file software dell'applicazione che non sincronizzano correttamente le impostazioni tra i computer degli utenti o gli ambienti di elaborazione. Per impostazione predefinita, questi sono esclusi:

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file a cui l'utente connesso non può scrivere valori

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file associati alle funzionalità di base di Windows

-   Tutte le chiavi del registro di sistema che si trovano nell'HKEY \ _LOCAL \ _MACHINE hive

-   File che si trovano nelle directory dei file di programma

-   File che si trovano in utenti \ \ \ [nome utente \] \ \ AppData \ \ LocalLow

-   File di sistema operativo Windows che si trovano in% SystemRoot%

Se le chiavi del registro di sistema e i file archiviati in percorsi esclusi sono necessari per sincronizzare le impostazioni dell'applicazione, è possibile aggiungere manualmente le posizioni al modello di percorso delle impostazioni durante il processo di creazione del modello.
Tuttavia, solo le modifiche apportate all'HKEY \ _CURRENT \ _USER hive verranno sincronizzate.

### Sostituire i modelli Microsoft predefiniti

L'agente UE-V installa un gruppo predefinito di modelli di posizione delle impostazioni per le comuni applicazioni Microsoft e le impostazioni di Windows. Se si personalizzano questi modelli o si creano modelli di posizione delle impostazioni per la sincronizzazione delle impostazioni per le applicazioni personalizzate, l'agente UE-V può essere configurato per l'uso di un catalogo di modelli di impostazioni per l'archiviazione. In questo caso dovrai includere i modelli predefiniti insieme ai modelli personalizzati nel catalogo dei modelli di impostazioni.

Quando si [distribuisce un agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), è possibile usare il parametro della riga `RegisterMSTemplates` di comando per disabilitare la registrazione dei modelli Microsoft predefiniti.

Quando si usano criteri di gruppo per configurare il percorso del catalogo dei modelli di impostazioni, è possibile scegliere di sostituire i modelli Microsoft predefiniti. Se si configurano le impostazioni dei criteri per sostituire i modelli Microsoft predefiniti, tutti i modelli Microsoft predefiniti installati dall'agente UE-V vengono eliminati e vengono usati solo i modelli presenti nel catalogo dei modelli di impostazioni. Il parametro dell'impostazione di configurazione dell'agente UE-V `RegisterMSTemplates` deve essere impostato su *true* per eseguire l'override del modello Microsoft predefinito.

**Nota**  Se si disabilita questa impostazione dei criteri dopo che è stata abilitata, l'agente UE-V non ripristinerà i modelli Microsoft predefiniti.

 

Se sono presenti modelli personalizzati nel catalogo di modelli di impostazioni che usano lo stesso ID dei modelli Microsoft predefiniti e l'agente UE-V non è configurato per sostituire i modelli Microsoft predefiniti, i modelli Microsoft vengono ignorati.

È anche possibile sostituire i modelli predefiniti usando le caratteristiche di Windows PowerShell di UE-V. Per sostituire il modello Microsoft predefinito con Windows PowerShell, annullare la registrazione di tutti i modelli Microsoft predefiniti e quindi registrare i modelli personalizzati.

**Nota**  I pacchetti di impostazioni precedenti rimangono nella posizione di archiviazione delle impostazioni anche se si distribuiscono i nuovi modelli di posizione delle impostazioni per un'applicazione. Questi pacchetti non vengono letti dall'agente, ma non vengono eliminati automaticamente.

 

## <a href="" id="uevgen"></a>Installare il generatore UEV 2. x


Installare il generatore di Microsoft User Experience Virtualization (UE-V) 2,0 in un computer che può essere usato per creare un modello di posizione delle impostazioni personalizzato. Questo computer dovrebbe avere le applicazioni installate per cui devono essere generati i modelli di posizione delle impostazioni personalizzate.

**Per installare il generatore UE-V**

1.  Come utente con diritti di amministratore locale, individuare il file di installazione del generatore di UE-V **ToolSetup.exe** fornito con il software UE-v. In alternativa, se si conosce l'architettura del computer, è possibile eseguire il file di Windows Installer (MSI) appropriato, **ToolsSetupx64.msi** o **ToolsSetupx86.msi**.

2.  Fare doppio clic sul file di installazione. Verrà visualizzata la configurazione guidata generatore di virtualizzazione dell'esperienza utente. Fai clic su **Next** per continuare.

3.  Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.

4.  Fare clic sulle opzioni per gli aggiornamenti Microsoft e sul programma Analisi utilizzo software.

5.  Selezionare la cartella di destinazione in cui installare il generatore UE-V e quindi fare clic su **Avanti**.

6.  Fare clic su **Installa** per avviare l'installazione.

    **Nota**  Prima dell'installazione dell'applicazione viene visualizzato un prompt per il **controllo dell'account utente** . Per installare il generatore UE-V è necessaria l'autorizzazione.

     

7.  Fare clic su **fine** per chiudere la procedura guidata al termine dell'installazione. È necessario riavviare il computer prima di poter eseguire il generatore di UE-V.

    Per verificare che l'installazione sia stata eseguita correttamente, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Microsoft User Experience Virtualization**e quindi fare clic su **Microsoft User Experience Virtualization Generator**.

    **Nota**  Il generatore UE-V 2 può essere usato solo per creare modelli per gli agenti UE-V 2. In una distribuzione mista di agenti UE-V 1,0 e di agenti UE-V 2, è necessario continuare a usare il generatore UE-V 1,0 fino a quando non sono stati aggiornati tutti gli agenti di UE-v.

     

## <a href="" id="deploycatalogue"></a>Distribuire un catalogo di modelli di impostazioni


Il catalogo dei modelli di impostazioni di virtualizzazione dell'esperienza utente è un percorso di cartella nei computer UE-V o in una condivisione di rete SMB (Server Message Block) in cui sono archiviati tutti i modello di posizione delle impostazioni personalizzate. Un'attività pianificata nell'agente UE-V controlla questa posizione una volta al giorno e aggiorna il comportamento di sincronizzazione, in base ai modelli in questa cartella.

L'agente UE-V registra i modelli che sono stati aggiunti o aggiornati in questa cartella dopo l'ultima volta che la cartella è stata selezionata e Annulla la registrazione dei modelli rimossi. Per impostazione predefinita, i modelli sono registrati e non registrati una volta al giorno alle 3:30 A.M. ora locale dall'utilità di pianificazione e dall'avvio del sistema. Per personalizzare la frequenza di questa attività pianificata, vedere [modifica della frequenza delle attività pianificate di UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

È possibile configurare il percorso del catalogo dei modelli di impostazioni usando le opzioni della riga di comando per l'installazione, criteri di gruppo, WMI o Windows PowerShell. I modelli archiviati nel percorso del catalogo dei modelli di impostazioni vengono registrati e annullati automaticamente da un'attività pianificata.

**Per configurare il catalogo dei modelli di impostazioni per UE-V 2. x**

1.  Creare una nuova cartella nel computer in cui è archiviato il catalogo dei modelli di impostazioni UE-V.

2.  Impostare le seguenti autorizzazioni SMB per la cartella del catalogo dei modelli di impostazioni.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Account utente</strong></th>
    <th align="left"><strong>Autorizzazioni consigliate</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tutti</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computer di dominio</p></td>
    <td align="left"><p>Livelli di autorizzazione di lettura</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Livelli di autorizzazione di lettura/scrittura</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Impostare le autorizzazioni di file system NTFS seguenti per la cartella del catalogo dei modelli di impostazioni.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Account utente</th>
    <th align="left">Autorizzazioni consigliate</th>
    <th align="left">Applica a</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creatore/proprietario</p></td>
    <td align="left"><p>Controllo completo</p></td>
    <td align="left"><p>Questa cartella, le sottocartelle e i file</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computer di dominio</p></td>
    <td align="left"><p>Contenuto della cartella di elenco e lettura</p></td>
    <td align="left"><p>Questa cartella, le sottocartelle e i file</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Tutti</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Controllo completo</p></td>
    <td align="left"><p>Questa cartella, le sottocartelle e i file</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Fare clic su **OK** per chiudere le finestre di dialogo.

La condivisione di rete deve almeno concedere le autorizzazioni per il gruppo Domain Computers. Concedere inoltre le autorizzazioni di accesso per la cartella di condivisione di rete agli amministratori che gestiscono i modelli archiviati.

## <a href="" id="createcustomtemplates"></a>Creare modelli di posizione delle impostazioni personalizzate


Usa il generatore UE-V per creare modelli di posizione delle impostazioni per le applicazioni line-of-business o altre applicazioni personalizzate. Dopo aver creato il modello per un'applicazione, è possibile distribuirlo nei computer in modo che le impostazioni vengano sincronizzate per l'applicazione.

**Per creare un modello di posizione delle impostazioni di UE-V con il generatore UE-V**

1.  Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.

2.  Fare clic su **Crea modello posizione impostazioni**.

3.  Specifica l'applicazione. Individuare il percorso del file dell'applicazione (con estensione exe) o il collegamento all'applicazione (con estensione lnk) per cui si vuole creare un modello di posizione delle impostazioni. Specificare gli argomenti della riga di comando, se presenti, e la directory di lavoro, se presenti. Fai clic su **Next** per continuare.

    **Nota**  Prima che l'applicazione venga avviata, il sistema Visualizza un prompt per il **controllo dell'account utente**. È necessaria l'autorizzazione per monitorare il registro di sistema e i percorsi dei file usati dall'applicazione per archiviare le impostazioni.

     

4.  Dopo l'avvio dell'applicazione, chiudere l'applicazione. Il generatore UE-V registra le posizioni in cui vengono archiviate le impostazioni dell'applicazione.

5.  Al termine del processo, fare clic su **Avanti** per continuare.

6.  Esaminare e selezionare le caselle di controllo accanto alle posizioni appropriate per la sincronizzazione delle impostazioni del registro di sistema e dei file di impostazioni da sincronizzare per l'applicazione. L'elenco include le due categorie seguenti per i percorsi delle impostazioni:

    -   **Standard**: impostazioni dell'applicazione archiviate nel registro di sistema in HKEY \ _CURRENT \ _USER i tasti o nelle cartelle file in \ \ **Users** \ \ \ [nome utente \] \ \ **AppData**  \\  **roaming**. Il generatore UE-V include queste impostazioni per impostazione predefinita.

    -   Non **standard**: le impostazioni dell'applicazione archiviate all'esterno delle posizioni vengono specificate nelle procedure consigliate per l'archiviazione dei dati delle impostazioni (facoltativo). Questi includono file e cartelle in **utenti** \ \ \ [nome utente \] \ \ **AppData**  \\  **local**. Esaminare queste posizioni per determinare se includerle nel modello di posizione delle impostazioni. Selezionare le caselle di controllo percorsi per includerle.

    Fai clic su **Next** per continuare.

7.  Rivedere e modificare le **Proprietà**, le posizioni **del registro di sistema** e i percorsi dei **file** per il modello di posizione delle impostazioni.

    -   Modificare le proprietà seguenti nella scheda **Proprietà** :

        -   **Nome applicazione**: il nome dell'applicazione scritto nella descrizione delle proprietà dei file di programma.

        -   **Nome programma**: il nome del programma che viene ricavato dalle proprietà del file di programma. Il nome in genere ha l'estensione exe.

        -   **Versione del prodotto**: il numero di versione del prodotto del file exe dell'applicazione. Questa proprietà, insieme alla versione del **file**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni si applica a tutte le versioni del prodotto.

        -   **Versione file**: il numero di versione del file exe dell'applicazione. Questa proprietà, insieme alla versione del **prodotto**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni si applica a tutte le versioni del programma.

        -   **Nome autore modello** (facoltativo): nome dell'autore del modello di posizione delle impostazioni.

        -   **Autore** di un modello (facoltativo): l'indirizzo di posta elettronica dell'autore del modello di posizione delle impostazioni.

    -   La scheda **Registro di sistema** elenca la **chiave** e l' **ambito** delle posizioni del registro di sistema incluse nel modello di posizione delle impostazioni. Modificare i percorsi del registro di sistema usando il menu a discesa **attività** . Le attività consentono di aggiungere nuove chiavi, modificare il nome o l'ambito delle chiavi esistenti, eliminare le chiavi e passare al registro di sistema in cui si trovano le chiavi. Usare l'ambito **tutte le impostazioni** per includere tutte le impostazioni del registro di sistema sotto la chiave specificata. Usare **tutte le impostazioni e le sottochiavi** per includere tutte le impostazioni del registro di sistema sotto la chiave, le sottochiavi e le impostazioni della sottochiave specificati.

    -   Nella scheda **file** sono elencati il percorso del file e la maschera di file delle posizioni di file incluse nel modello di posizione delle impostazioni. Modificare i percorsi dei file usando il menu a discesa **attività** . Le attività per i percorsi dei file consentono di aggiungere nuovi file o posizioni delle cartelle, modificare l'ambito di file o cartelle esistenti, eliminare file o cartelle e aprire la posizione selezionata in Esplora risorse. Lascia vuota la maschera di file per includere tutti i file nella cartella specificata.

8.  Fare clic su **Crea**e quindi su **Salva** per salvare il modello posizione impostazioni nel computer.

9.  Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni. Uscire dall'applicazione Generator UE-V.

    Dopo aver creato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello. Distribuire il modello in un ambiente lab prima di inserirlo nella produzione aziendale.

Guida di [riferimento allo schema del modello di applicazione per la direttiva UE-v](https://technet.microsoft.com/library/dn763947.aspx) descrive la struttura XML del modello di posizione delle impostazioni di UE-v e fornisce indicazioni per la modifica di questi file.

## <a href="" id="deploycustomtemplates"></a>Distribuire i modelli di posizione delle impostazioni personalizzate


Dopo aver creato un modello di posizione delle impostazioni con il generatore UE-V, è consigliabile testarlo per verificare che le impostazioni dell'applicazione vengano sincronizzate correttamente. Puoi quindi distribuire il modello di posizione delle impostazioni in modo sicuro ai computer dell'organizzazione.

I modelli di posizione delle impostazioni possono essere distribuiti usando uno di questi metodi:

-   Sistema ESD (Enterprise Software Distribution), ad esempio System Center Configuration Manager

-   Preferenze di Criteri di gruppo

-   Catalogo di modelli di impostazioni UE-V

I modelli distribuiti tramite un sistema ESD o gli oggetti Criteri di gruppo devono essere registrati tramite Strumentazione gestione Windows (WMI) di UE-V o Windows PowerShell. I modelli archiviati nella posizione del catalogo dei modelli di impostazioni vengono automaticamente registrati dall'agente UE-V.

**Per usare il percorso del catalogo di modelli di impostazioni per distribuire i modelli di posizione delle impostazioni di UE-V**

1.  Passare alla cartella della condivisione di rete definita come catalogo dei modelli di impostazioni.

2.  Aggiungere, rimuovere o aggiornare i modelli di posizione delle impostazioni nel catalogo dei modelli di impostazioni per riflettere la configurazione del modello di agente UE-V desiderata per i computer UE-V.

    **Nota**  I modelli nei computer vengono aggiornati giornalmente. L'aggiornamento si basa sulle modifiche apportate al catalogo dei modelli di impostazioni.

     

3.  Per aggiornare manualmente i modelli in un computer che esegue l'agente UE-V, aprire un prompt dei comandi con privilegi elevati e passare a **% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 o x64 &gt; **, quindi eseguire **ApplySettingsTemplateCatalog.exe**.

    **Nota**  Questo programma viene eseguito automaticamente durante l'avvio del computer e ogni giorno in 3:30 a. M. per raccogliere tutti i nuovi modelli aggiunti di recente al catalogo.

     






## Argomenti correlati


[Preparare una distribuzione UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Distribuire le funzionalità necessarie per UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





