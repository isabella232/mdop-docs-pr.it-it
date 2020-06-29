---
title: Uso dei modelli Custom UE-V 2. x e del generatore UE-V 2. x
description: Uso dei modelli Custom UE-V 2. x e del generatore UE-V 2. x
author: dansimp
ms.assetid: f0bb4920-0132-472c-a564-abf06a884275
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a8d863896e4ccfa92161f8a8f5e2b8955f139872
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819295"
---
# Uso dei modelli Custom UE-V 2. x e del generatore UE-V 2. x


Per sincronizzare le impostazioni delle applicazioni tra i computer degli utenti, Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usano i *modelli di posizione delle impostazioni*. Alcuni modelli di posizione delle impostazioni sono inclusi nella virtualizzazione dell'esperienza utente. È anche possibile creare, modificare o convalidare i modelli di posizione delle impostazioni personalizzate usando il generatore UE-V.

Il generatore di UE-V monitora le applicazioni desktop di Windows per individuare e acquisire le posizioni in cui vengono archiviate le impostazioni dell'applicazione. L'applicazione monitorata deve essere un'applicazione desktop. Il generatore UE-V non può creare un modello di posizione delle impostazioni per i tipi di applicazione seguenti:

-   Applicazioni virtualizzate

-   Applicazioni offerte tramite Servizi terminal

-   Applicazioni Java

-   App di Windows  

Questo argomento

**Posizioni delle impostazioni standard e non standard:** Il generatore UE-V consente di identificare la posizione in cui le applicazioni cercano file di impostazioni e impostazioni del registro di sistema che le applicazioni usano per archiviare le informazioni sulle impostazioni. Il generatore individua solo le impostazioni in posizioni accessibili a un utente standard. Le impostazioni archiviate in altre posizioni sono escluse. Le impostazioni individuate sono raggruppate in due categorie: **standard** e **non standard**. Le impostazioni standard sono consigliate per la sincronizzazione e l'opzione UE-V può acquisirle e applicarle facilmente. Le impostazioni non standard possono potenzialmente sincronizzare le impostazioni, ma, a causa delle regole usate da UE-V, queste impostazioni potrebbero non essere coerenti o in modo affidabile per sincronizzare le impostazioni. Queste impostazioni possono dipendere da file temporanei, causare la sincronizzazione non affidabile o potrebbero non essere utili. Questi percorsi delle impostazioni sono presentati nel generatore di UE-V. È possibile scegliere di includerli o escluderli caso per caso.

Il generatore UE-V apre l'applicazione come parte del processo di individuazione. Il generatore può acquisire le impostazioni nei percorsi seguenti:

-   **Impostazioni del registro** di sistema-posizioni del registro di sistema in **HKEY \ _CURRENT \ _USER**

-   **File di impostazioni applicazione** : file archiviati in \ \ **Users** \ \ \ [nome utente \] \ \ **AppData**  \\  **roaming**

Il generatore UE-V esclude le posizioni, che in genere archiviano i file del software dell'applicazione, ma non si sincronizzano correttamente tra i computer degli utenti o gli ambienti. Il generatore UE-V esclude queste posizioni. I percorsi esclusi sono i seguenti:

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file a cui l'utente connesso non può scrivere valori

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file associati alle funzionalità di base di Windows

-   Tutte le chiavi del registro di sistema situate in HKEY \ _LOCAL \ _MACHINE hive, che richiedono diritti di amministratore e potrebbero richiedere l'impostazione di un contratto di controllo dell'account utente

-   File che si trovano nelle directory Program Files, che richiedono diritti di amministratore e che potrebbero richiedere l'impostazione di un contratto UAC

-   File che si trovano in utenti \ \ \ [nome utente \] \ \ AppData \ \ LocalLow

-   I file di sistema operativo Windows che si trovano in% SystemRoot%, che richiedono diritti di amministratore e potrebbero richiedere l'impostazione di un contratto UAC

Se le chiavi del registro di sistema e i file archiviati in queste posizioni sono necessari per sincronizzare le impostazioni dell'applicazione, è possibile aggiungere manualmente i percorsi esclusi al modello della posizione delle impostazioni durante il processo di creazione del modello (ad eccezione delle voci del registro di sistema in HKEY \ _LOCAL \ _MACHINE hive).

## <a href="" id="edit"></a>Modificare i modelli di posizione delle impostazioni con il generatore UE-V


Usare il generatore UE-V per modificare i modelli di posizione delle impostazioni. Quando le impostazioni modificate vengono aggiunte ai modelli tramite il generatore UE-V, le informazioni sulla versione all'interno del modello vengono aggiornate automaticamente per verificare che i modelli esistenti distribuiti nell'organizzazione vengano aggiornati correttamente.

**Nota**  Se si modifica un modello UE-V 1,0 tramite il generatore UE-V 2, il modello viene convertito automaticamente in un modello UE-V 2. Gli agenti UE-V 1,0 non possono più usare il modello modificato.

 

**Per modificare un modello di posizione delle impostazioni di UE-V con il generatore UE-V**

1.  Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.

2.  Fare clic su **modifica modello posizione impostazioni**.

3.  Nell'elenco dei modelli usati di recente selezionare il modello da modificare. In alternativa, fare clic su **Sfoglia** per cercare il file del modello di impostazioni. Fai clic su **Next** per continuare.

4.  Esaminare le **Proprietà**, le posizioni **del registro di sistema** e i percorsi dei **file** per il modello di impostazioni. Modifica come richiesto.

    -   Nella scheda **Proprietà** è possibile visualizzare e modificare le proprietà seguenti:

        -   **Nome applicazione**: il nome dell'applicazione scritto nella descrizione delle proprietà del file di programma.

        -   **Nome programma**: il nome del programma che viene ricavato dalle proprietà del file di programma. Il nome in genere ha l'estensione exe.

        -   **Versione del prodotto**: il numero di versione del prodotto del file exe dell'applicazione. Questa proprietà, insieme alla **versione del file**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni si applica a tutte le versioni del prodotto.

        -   **Versione file**: il numero di versione del file exe dell'applicazione. Questa proprietà, insieme alla **versione del prodotto**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni si applica a tutte le versioni del programma.

        -   **Nome autore modello** (facoltativo): nome dell'autore del modello di impostazioni.

        -   **Autore** di un modello (facoltativo): l'indirizzo di posta elettronica dell'autore del modello di posizione delle impostazioni.

    -   La scheda **Registro di sistema** elenca la **chiave** e l' **ambito** delle posizioni del registro di sistema incluse nel modello di posizione delle impostazioni. È possibile modificare le posizioni del registro di sistema usando il menu a discesa **attività** . Nel menu attività è possibile aggiungere nuove chiavi, modificare il nome o l'ambito delle chiavi esistenti, eliminare le chiavi e cercare il registro di sistema in cui si trovano le chiavi. Quando si definisce l'ambito per il registro di sistema, è possibile usare l'ambito **tutte le impostazioni** per includere tutte le impostazioni del registro di sistema sotto la chiave specificata. Usare **tutte le impostazioni** e le **sottochiavi** per includere tutte le impostazioni del registro di sistema sotto la chiave, le sottochiavi e le impostazioni della sottochiave specificati.

    -   Nella scheda **file** sono elencati il percorso del file e la maschera di file delle posizioni di file incluse nel modello di posizione delle impostazioni. È possibile modificare i percorsi dei file usando il menu a discesa **attività** . Nel menu **attività** per i percorsi dei file è possibile aggiungere nuovi file o posizioni delle cartelle, modificare l'ambito di file o cartelle esistenti, eliminare file o cartelle e aprire la posizione selezionata in Esplora risorse. Per includere tutti i file nella cartella specificata, lascia vuota la maschera di file.

5.  Fare clic su **Salva** per salvare le modifiche apportate al modello posizione impostazioni.

6.  Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni. Uscire dall'applicazione Generator UE-V.

    Dopo aver modificato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello. Distribuire il modello di posizione delle impostazioni modificate in un ambiente lab prima di inserirlo nella produzione nell'organizzazione.

**Come modificare manualmente un modello di posizione delle impostazioni**

1.  Creare una copia locale del file modello. XML della posizione delle impostazioni. I modelli di posizione delle impostazioni di UE-V sono file XML che identificano le posizioni in cui i valori delle impostazioni dell'archivio applicazioni.

    **Nota**  Un modello di posizione delle impostazioni è univoco a causa dell' **ID**modello. Se si copia il modello e si rinomina il file con estensione XML, la registrazione del modello non riesce perché UE-V legge il tag **ID** modello nel file XML per determinare il nome e non il nome del file XML. UE-V legge anche il numero di **versione** per sapere se è cambiato qualcosa. Se il numero di versione è più alto, UE-V aggiorna il modello.

     

2.  Aprire il file del modello di posizione delle impostazioni con un editor XML.

3.  Modificare il file del modello di posizione delle impostazioni. Tutte le modifiche devono essere conformi al file di schema UE-V definito in [SettingsLocationTempate. xsd](https://technet.microsoft.com/library/dn763947.aspx). Per impostazione predefinita, una copia del file con estensione xsd si trova in \\ProgramData\\Microsoft\\UEV\\Templates.

4.  Incrementare il numero di **versione** per il modello posizione impostazioni.

5.  Salvare il file del modello di posizione delle impostazioni e quindi chiudere l'editor XML.

6.  Convalidare il file del modello di posizione delle impostazioni modificate usando il generatore UE-V.

7.  È necessario registrare il modello di posizione delle impostazioni UE-V modificato prima che possa sincronizzare le impostazioni tra i computer client. Per registrare un modello, aprire Windows PowerShell e quindi eseguire il cmdlet seguente: `update-uevtemplate [templatefilename]` . È quindi possibile copiare il file nel catalogo dello spazio di archiviazione delle impostazioni. L'agente UE-V nei computer degli utenti dovrebbe quindi essere aggiornato come programmato nell'attività pianificata.

## <a href="" id="validate"></a>Convalida dei modelli di posizione delle impostazioni con il generatore UE-V


È possibile creare o modificare i modelli di posizione delle impostazioni in un editor XML senza usare il generatore UE-V. In questo caso, puoi usare il generatore UE-V per verificare che il codice XML nuovo o modificato corrisponda allo schema definito per il modello.

**Per convalidare un modello di posizione delle impostazioni di UE-V con il generatore UE-V**

1.  Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.

2.  Fare clic su **convalida modello posizione impostazioni**.

3.  Nell'elenco dei modelli usati di recente selezionare il modello da modificare. In alternativa, è possibile **passare** al file del modello di impostazioni. Fai clic su **Next** per continuare.

4.  Fare clic su **convalida** per continuare.

5.  Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni. Uscire dall'applicazione Generator UE-V.

    Dopo aver convalidato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello. Distribuire il modello in un ambiente lab prima di inserirlo in un ambiente di produzione aziendale.

## <a href="" id="share"></a>Condividere i modelli di posizione delle impostazioni con la raccolta modelli


La raccolta modelli di Microsoft User Experience Virtualization (UE-V) 2,0 consente agli amministratori di condividere i modelli di posizione delle impostazioni di UE-V. Nella raccolta è possibile caricare i modelli di posizione delle impostazioni per consentire ad altri utenti di usarli ed è possibile scaricare i modelli creati da altri utenti. La raccolta modelli UE-V si trova in [Microsoft TechNet.](https://go.microsoft.com/fwlink/p/?LinkId=246589)

Prima di condividere un modello di posizione delle impostazioni nella raccolta modelli UE-V, verificare che non contenga informazioni personali o aziendali. È possibile usare qualsiasi visualizzatore XML per aprire e visualizzare il contenuto di un file del modello di posizione delle impostazioni. I valori di modello seguenti devono essere esaminati prima di condividere un modello con chiunque all'esterno della società.

-   Nome autore modello: specificare un nome generale non Identificativo per il nome dell'autore del modello o escludere questi dati dal modello.

-   Autore di un modello-specificare un modello di messaggio di posta elettronica non identificante o escludere i dati dal modello.

Prima di distribuire un modello di posizione delle impostazioni scaricato dalla raccolta UE-V, è consigliabile prima di tutto testare il modello per verificare che le impostazioni dell'applicazione vengano sincronizzate correttamente in un ambiente di test.






## Argomenti correlati


[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





