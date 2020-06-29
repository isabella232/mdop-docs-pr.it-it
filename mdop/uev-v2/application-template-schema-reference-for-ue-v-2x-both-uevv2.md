---
title: Riferimento allo schema modello applicazione per UE-V 2. x
description: Riferimento allo schema modello applicazione per UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827406"
---
# Riferimento allo schema modello applicazione per UE-V 2. x


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 usano i modelli di posizione delle impostazioni XML per definire le impostazioni dell'applicazione desktop e le impostazioni di Windows acquisite e applicate da UE-V. UE-V include un set di modelli di posizione predefiniti per le impostazioni. È anche possibile creare modelli di posizione delle impostazioni personalizzate con il generatore UE-V.

Un utente avanzato può personalizzare il file XML per un modello di posizione delle impostazioni. Questo argomento descrive in dettaglio la struttura XML dei modelli di posizione delle impostazioni UE-V 2,1 (SP1) e 2,0 e fornisce indicazioni per la modifica di questi file.

## Informazioni di riferimento sullo schema del modello di applicazione UE-V 2,1 e 2,1 SP1


Questa sezione descrive in dettaglio la struttura XML del modello di posizione delle impostazioni dell'UE-V 2,1 e 2,1 SP1 e fornisce indicazioni per la modifica di questo file.

### In questa sezione

-   [Attributo di codifica e dichiarazione XML](#xml21)

-   [Spazio dei nomi e elemento radice](#namespace21)

-   [Tipi di dati](#data21)

-   [Elemento Name](#name21)

-   [Elemento ID](#id21)

-   [Elemento version](#version21)

-   [Elemento Author](#author21)

-   [Processi ed elementi process](#processes21)

-   [Elemento Application](#application21)

-   [Elemento comune](#common21)

-   [Elemento SettingsLocationTemplate](#settingslocationtemplate21)

-   [Appendice: SettingsLocationTemplate. xsd](#appendix21)

### <a href="" id="xml21"></a>Attributo di codifica e dichiarazione XML

**Obbligatorio: vero**

**Digitare: stringa**

La dichiarazione XML deve specificare l'attributo XML version 1,0 ( &lt; ? XML version = "1.0" &gt; ). I modelli di posizione delle impostazioni creati dal generatore UE-V vengono salvati nella codifica UTF-8, anche se la codifica non è specificata in modo esplicito. È consigliabile includere l'attributo encoding = "UTF-8" in questo elemento come procedura consigliata. Tutti i modelli inclusi nel prodotto specificano anche questo tag (Vedi i documenti in%ProgramFiles%\\Microsoft User Experience Virtualization\\Templates per riferimento). Ad esempio:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a>Spazio dei nomi e elemento radice

**Obbligatorio: vero**

**Digitare: stringa**

UE-V usa lo https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate spazio dei nomi per tutte le applicazioni. SettingsLocationTemplate è l'elemento radice e contiene tutti gli altri elementi. Fare riferimento a SettingsLocationTemplate in tutti i modelli usando questo tag:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a>Tipi di dati

Questi sono i tipi di dati per lo schema del modello di applicazione UE-V.

<a href="" id="guid"></a>**GUID** GUID descrive un'espressione regolare dell'identificatore univoco globale standard nel formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \ \}". Viene usato nell'elemento Filesetting\\Root\\KnownFolder per verificare la formattazione delle cartelle note.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString si riferisce al nome del file di un processo da monitorare. I relativi valori sono limitati dall'espressione Regex \ [^ \ &lt; &gt; \ \ \ \ \ /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i caratteri del colon.

<a href="" id="idstring"></a>**IdString** IDString fa riferimento al valore ID di elementi Application, SettingsLocationTemplate e elementi comuni (usati per descrivere i gruppi di applicazioni che condividono le impostazioni comuni). È limitato dalla stessa Regex di FilenameString (\ [^ \ \ \ \ \ \? \ \ \ \ &lt; &gt; \ \ \ \ \ \ \ \ \ \ /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion è un valore intero usato per descrivere la revisione del modello di posizione delle impostazioni. Il valore può essere compreso tra 0 e 2147483647.

<a href="" id="empty"></a>**Empty** Empty fa riferimento a un valore null. Viene usato in Process\\ShellProcess per indicare che non esiste un processo da monitorare. Questo valore non deve essere usato nei modelli di applicazione.

<a href="" id="author"></a>**Autore** Il tipo di dati Author è un tipo complesso che identifica l'autore di un modello. Contiene due elementi figlio: **nome** e **posta elettronica**. All'interno del tipo di dati Author, l'elemento Name è obbligatorio mentre l'elemento di posta elettronica è facoltativo. Questo tipo è descritto in modo più dettagliato sotto l'elemento SettingsLocationTemplate.

<a href="" id="range"></a>**Intervallo** Range definisce una classe integer costituita da due elementi figlio: **Minimum** e **Maximum**. Questo tipo di dati viene implementato nel tipo di dati ProcessVersion. Se specificato, è necessario includere i valori minimo e massimo.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion definisce un tipo con quattro elementi figlio: **Major**, **minor**, **Build**e **patch**. Questo tipo di dati viene usato dall'elemento Process per popolare i relativi valori ProductVersion e fileversion. I dati per questo tipo sono un valore di intervallo. L'elemento figlio principale è obbligatorio e gli altri sono facoltativi.

<a href="" id="architecture"></a>**Architettura** L'architettura enumera due valori possibili: **Win32** e **Win64**. Questi valori vengono usati per specificare l'architettura di processo.

<a href="" id="process"></a>**Processo** Il tipo di dati processo è un contenitore usato per descrivere i processi da monitorare da UE-V. Contiene sei elementi figlio: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**. Questa tabella descrive in dettaglio i rispettivi tipi di dati di ogni elemento:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Elemento</strong></p></td>
<td align="left"><p><strong>Tipo di dati</strong></p></td>
<td align="left"><p><strong>Mandatory</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome file</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Architettura</p></td>
<td align="left"><p>Architettura</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Processi** Il tipo di dati processes rappresenta un contenitore per una raccolta di uno o più elementi Process. Nel tipo di sequenza processi sono supportati due elementi figlio: **Process** e **ShellProcess**. Process è un elemento di tipo Process e ShellProcess è di tipo dati vuoto. Nella sequenza devono essere identificati almeno un elemento.

<a href="" id="path"></a>**Percorso** Path viene usato da RegistrySetting e filesetting per fare riferimento ai percorsi del registro di sistema e dei file. Questo elemento supporta due attributi facoltativi: **ricorsive** e **DeleteIfNotFound**. Entrambi i valori sono impostati su default = "false".

Ricorsive indica che il percorso e tutte le sottocartelle sono incluse per le impostazioni dei file o che tutte le chiavi del registro di sistema figlio sono incluse per le impostazioni del registro di sistema. In entrambi i casi, tutti gli elementi a livello corrente sono inclusi nei dati acquisiti. Per un oggetto fileSettings, tutti i file all'interno della cartella specificata sono inclusi nei dati acquisiti da UE-V, ma le cartelle non sono incluse. Per i percorsi del registro di sistema, vengono acquisiti tutti i valori nel percorso corrente, ma le chiavi del registro di sistema figlio non vengono acquisite. In entrambi i casi, è necessario prestare attenzione per evitare l'acquisizione di set di dati di grandi dimensioni o un numero elevato di elementi.

L'attributo DeleteIfNotFound rimuove l'impostazione dai dati del percorso di archiviazione delle impostazioni dell'utente. Questo potrebbe essere utile nei casi in cui la rimozione di queste impostazioni dal pacchetto salverà una grande quantità di spazio su disco nel file server del percorso di archiviazione delle impostazioni.

<a href="" id="filemask"></a>**FileMask** FileMask specifica solo determinati tipi di file per la cartella definita da path. Ad esempio, Path può essere `C:\users\username\files` e FileMask può `*.txt` includere solo file di testo.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting rappresenta un contenitore per le chiavi del registro di sistema e i valori e il comportamento desiderato associato da parte dell'agente UE-V. In questo tipo sono definiti quattro elementi figlio: **path**, **Name**, **Exclude**e una sequenza di valori **path** e **Name**.

<a href="" id="filesetting"></a>**Impostazione Filesetting** Filesetting contiene i parametri associati ai percorsi di file e file. Vengono definiti quattro elementi figlio: **root**, **path**, **FileMask**ed **Exclude**. Root è obbligatorio e gli altri sono facoltativi.

<a href="" id="settings"></a>**Impostazioni** Settings è un contenitore per tutte le impostazioni che si applicano a un determinato modello. Contiene le istanze delle impostazioni del registro di sistema, file, SystemParameter e CustomAction descritte in precedenza. Inoltre, può contenere anche gli elementi figlio seguenti con i comportamenti descritti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Elemento</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Asincrona</p></td>
<td align="left"><p>I pacchetti di impostazioni asincrone vengono applicati senza bloccare l'avvio dell'applicazione in modo che l'avvio dell'applicazione proceda mentre le impostazioni sono ancora applicate. Questa operazione è utile per le impostazioni che possono essere applicate in modo asincrono, ad esempio quelle <code>get/set</code> tramite un'API, come SystemParameterSetting.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Per impostazione predefinita, UE-V Salva solo le impostazioni per un'applicazione quando viene chiusa l'ultima istanza di un'applicazione che usa il modello. Quando questo elemento è impostato su "false", UE-V Esporta le impostazioni anche se sono in uso altre istanze di un'applicazione. Modelli adatti: quelli che includono una sezione elemento comune, forniti con UE-V, usano questo contrassegno per consentire alle impostazioni condivise di esportare sempre in prossimità dell'applicazione, impedendo l'esportazione di impostazioni specifiche dell'applicazione finché non viene chiusa l'ultima istanza.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AlwaysApplySettings</p></td>
<td align="left"><p>(introdotta in 2,1)</p>
<p>Questo parametro impone l'applicazione di un pacchetto di impostazioni importato anche se non ci sono differenze tra il pacchetto e lo stato corrente dell'applicazione. Questo parametro deve essere usato solo in casi particolari perché può rallentare l'importazione delle impostazioni.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a>Elemento Name

**Obbligatorio: vero**

**Digitare: stringa**

Nome specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. In generale, evita di fare riferimento alle informazioni sulla versione, perché questo può essere obiettato dall'elemento ProductVersion. Ad esempio, specificare `<Name>My Application</Name>` invece di `<Name>My Application 1.1</Name>` .

**Nota**  UE-V non fa riferimento a DTD esterni, quindi non è possibile usare le entità denominate in un modello di posizione delle impostazioni. Ad esempio, non usare per &reg; fare riferimento al segno di firma del marchio registrato®. USA invece i riferimenti numerati canonici per includere questi tipi di caratteri speciali, ad esempio & \ #174 per il carattere®. Questa regola si applica a tutti i valori stringa in questo documento.

Vedere <http://www.w3.org/TR/xhtml1/dtds.html> per un elenco completo delle entità di caratteri. I documenti con codifica UTF-8 possono includere direttamente i caratteri Unicode. Il salvataggio dei modelli tramite il generatore UE-V converte automaticamente le entità di caratteri nelle rappresentazioni Unicode.

 

### <a href="" id="id21"></a>Elemento ID

**Obbligatorio: vero**

**Digitare: stringa**

ID popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione, ad esempio, Vedi l'output dei cmdlet di PowerShell Get-UevTemplate e Get-UevTemplateProgram. Per convenzione, questo tag non deve contenere spazi, che semplificano lo scripting. I numeri di versione delle applicazioni devono essere specificati in questo elemento per consentire una facile identificazione del modello, ad esempio `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version21"></a>Elemento version

**Obbligatorio: vero**

**Digitare: integer**

**Valore minimo: 0**

**Valore massimo: 2147483647**

La versione identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche. Il generatore UE-V incrementa automaticamente questo numero per uno ogni volta che il modello viene salvato. Si noti che questo campo deve essere un numero intero Integer; i valori frazionari, ad esempio `<Version>2.5</Version>` non sono consentiti.

**Suggerimento:** È possibile salvare le note sulle modifiche della versione usando i tag di commento XML `<!-- -->` , ad esempio:

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

**Importante**  Questo valore viene interrogato per determinare se una nuova versione di un modello deve essere applicata a un modello esistente in queste istanze:

-   Quando viene eseguita l'attività di aggiornamento automatico del modello programmato

-   Quando viene eseguito il cmdlet di PowerShell Update-UevTemplate

-   Quando viene chiamato il metodo di aggiornamento microsoft\\uev: SettingsLocationTemplate tramite WMI

 

### <a href="" id="author21"></a>Elemento Author

**Obbligatorio: falso**

**Digitare: stringa**

Autore identifica il creatore del modello di posizione delle impostazioni. Sono supportati due elementi figlio facoltativi: **nome** e **posta elettronica**. Entrambi gli attributi sono facoltativi, ma, se l'elemento figlio del messaggio di posta elettronica viene specificato, deve essere accompagnato dall'elemento Name. Autore fa riferimento al nome completo del contatto per il modello di posizione delle impostazioni e la posta elettronica deve fare riferimento a un indirizzo di posta elettronica per l'autore. È consigliabile includere queste informazioni nei modelli pubblicati pubblicamente, ad esempio nella [raccolta modelli di UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes21"></a>Processi ed elementi process

**Obbligatorio: vero**

**Digitare: elemento**

I processi contengono almeno un `<Process>` elemento, che a sua volta contiene gli elementi figlio seguenti: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**. L'elemento figlio filename è obbligatorio e gli altri sono facoltativi. Un elemento completamente popolato contiene tag simili a questo esempio:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Nome file

**Obbligatorio: vero**

**Digitare: stringa**

Filename si riferisce al nome effettivo del file eseguibile visualizzato nel file System. Questo elemento specifica il criterio principale usato da UE-V per valutare se un modello si applica o meno a un processo. Questo elemento deve essere specificato nel codice XML del modello di posizione delle impostazioni.

I nomi file validi non devono corrispondere all'espressione regolare \ [^ \ \ \ \ \ \ \ &lt; &gt; /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i due punti (il \ \? \* | &lt; &gt; /o: caratteri.).

**Suggerimento:** Per testare una stringa con questa regex, usare una finestra di comando di PowerShell e sostituire il nome dell'eseguibile per **nomefile**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Il valore **true** indica che la stringa contiene caratteri non validi. Ecco alcuni esempi di valori illegali:

-   \\\\server\\share\\program.exe

-   Program \ *. exe

-   ram.exe Pro?

-   Programma &lt; 1 &gt; . exe

**Nota**  Il generatore UE-V codifica i caratteri maggiore di e minore di e &gt; &lt; rispettivamente.

 

In rari casi, il valore FileName non include necessariamente l'estensione exe, ma deve essere specificato come parte del valore. Ad esempio, `<Filename>MyApplictication.exe</Filename>` deve essere specificato al posto di `<Filename>MyApplictication</Filename>` . Il secondo esempio non applica il modello al processo se il nome effettivo del file eseguibile è "MyApplication.exe".

### Architettura

**Obbligatorio: falso**

**Digitare: Architecture (String)**

L'architettura si riferisce all'architettura del processore per cui è stato compilato l'eseguibile di destinazione. I valori validi sono Win32 per le applicazioni a 32 bit o Win64 per le applicazioni a 64 bit. Se presente, questo tag limita l'applicabilità del modello di posizione delle impostazioni a una particolare architettura dell'applicazione. Per un esempio, confronta l'esperienza utente di%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e MicrosoftOffice2010Win64.xml file inclusi in UE-V. Questa operazione è utile quando i percorsi relativi cambiano tra versioni diverse di un file eseguibile o se le impostazioni sono state aggiunte o rimosse quando si spostano da un'architettura del processore a un'altra.

Se questo elemento è assente, il modello di posizione delle impostazioni ignora l'architettura del processo e si applica ai processi di 32 e 64 bit se il nome file e gli altri attributi si applicano.

**Nota**  UE-V non supporta i processori ARM in questa versione.

 

### ProductName

**Obbligatorio: falso**

**Digitare: stringa**

ProductName è un elemento facoltativo usato per identificare un prodotto per scopi amministrativi o per la creazione di report. ProductName è diverso dal nome del file, in quanto il relativo valore non contiene restrizioni per le espressioni regolari. In questo modo è possibile comprendere più facilmente le descrizioni di un processo in cui il nome eseguibile potrebbe non essere ovvio. Ad esempio:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obbligatorio: falso**

**Digitare: stringa**

FileDescription è un tag facoltativo che consente di avere una descrizione amministrativa del file eseguibile. Si tratta di un campo di testo gratuito e può essere utile per distinguere più eseguibili in un pacchetto software in cui è necessario identificare la funzione dell'eseguibile.

Ad esempio, in un'applicazione appropriata può essere utile specificare i promemoria relativi alla funzione di due eseguibili (MyApplication.exe e MyApplicationHelper.exe), come illustrato di seguito:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obbligatorio: falso**

**Digitare: stringa**

ProductVersion si riferisce alle versioni di prodotto principali e secondarie di un file, oltre a una build e a un livello di patch. ProductVersion è un elemento facoltativo, ma se specificato deve contenere almeno l'elemento figlio principale. Il valore deve esprimere un intervallo nella forma Minimum = "X" Maximum = "Y" dove X e Y sono numeri interi. I valori minimo e massimo possono essere identici.

Gli elementi della versione del prodotto e del file possono essere lasciati non specificati. In questo modo il modello si applica a "versione agnostica", ovvero il modello verrà applicato a tutte le versioni del file eseguibile specificato.

**Esempio 1:**

Versione del prodotto: 1,0 specificato nel generatore di UE-V produce il codice XML seguente:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Esempio 2:**

Versione file: 5.0.2.1000 specificato nel generatore UE-V produce il codice XML seguente:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Esempio errato 1-intervallo incompleto:**

È presente solo l'attributo Minimum. Anche il valore massimo deve essere incluso in un intervallo.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Esempio errato 2-secondario specificato senza elemento principale:**

Solo l'elemento secondario è presente. Anche Major deve essere incluso.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obbligatorio: falso**

**Digitare: stringa**

FileVersion differenzia la versione finale di un'applicazione pubblicata e i dettagli di compilazione interni di un eseguibile del componente. Per la maggior parte delle applicazioni commerciali, questi numeri sono identici. Dove variano, la versione del prodotto di un file indica l'identificazione di una versione generica di un file, mentre la versione del file indica una build specifica di un file, come nel caso di un hotfix o di un aggiornamento. Questo identifica in modo univoco i file senza interrompere la logica di rilevamento.

Per determinare la versione del prodotto e la versione del file di un determinato eseguibile, fare clic con il pulsante destro del mouse sul file in Esplora risorse, scegliere Proprietà e quindi fare clic sulla scheda Dettagli.

L'inclusione di un elemento FileVersion per un'applicazione consente di definire una logica di rilevamento più granulare, ma non è necessaria per la maggior parte delle applicazioni. Le impostazioni dell'elemento ProductVersion sono controllate per prime e quindi viene selezionata la versione Fileversion. Verrà applicata l'impostazione più restrittiva.

Gli elementi figlio e le regole di sintassi per fileversion sono identici a quelli di ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a>Elemento Application

Application è un contenitore per le impostazioni che si applicano a una particolare applicazione. Si tratta di una raccolta dei campi/tipi seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. Per altre informazioni, Vedi <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione. Per altre informazioni, Vedi <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione facoltativa del modello.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Versione</p></td>
<td align="left"><p>Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche. Per altre informazioni, vedere la <a href="#version21" data-raw-source="[Version](#version21)"> versione </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controlla se il modello è abilitato in combinazione con un account Microsoft. Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365. Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (introdotta in 2,1)</p></td>
<td align="left"><p>Specifica che questo modello può essere associato solo al profilo specificato in questo elemento e non può essere modificato tramite WMI o PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Processi</p></td>
<td align="left"><p>Un contenitore per una raccolta di uno o più elementi Process. Per altre informazioni, vedere <a href="#processes21" data-raw-source="[Processes](#processes21)"> processi </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Impostazioni</p></td>
<td align="left"><p>Un contenitore per tutte le impostazioni che si applicano a un determinato modello. Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction. Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data21" data-raw-source="[Data types](#data21)"> tipi di dati </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a>Elemento comune

Common è simile a un elemento Application, ma è sempre associato a due o più elementi Application. La sezione comune rappresenta il set di impostazioni condivise tra le istanze dell'applicazione. Si tratta di una raccolta dei campi/tipi seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. Per altre informazioni, Vedi <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione. Per altre informazioni, Vedi <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione facoltativa del modello.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Versione</p></td>
<td align="left"><p>Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche. Per altre informazioni, vedere la <a href="#version21" data-raw-source="[Version](#version21)"> versione </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controlla se il modello è abilitato in combinazione con un account Microsoft. Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365. Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (introdotta in 2,1)</p></td>
<td align="left"><p>Specifica che questo modello può essere associato solo al profilo specificato in questo elemento e non può essere modificato tramite WMI o PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni</p></td>
<td align="left"><p>Un contenitore per tutte le impostazioni che si applicano a un determinato modello. Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction. Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data21" data-raw-source="[Data types](#data21)"> tipi di dati </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a>Elemento SettingsLocationTemplate

Questo elemento definisce le impostazioni per una singola applicazione o una famiglia di applicazioni.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. Per altre informazioni, Vedi <a href="#name21" data-raw-source="[Name](#name21)"> nome </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione. Per altre informazioni, Vedi <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione facoltativa del modello.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a>Appendice: SettingsLocationTemplate. xsd

Ecco il file SettingsLocationTemplate. xsd che Mostra gli elementi, gli elementi figlio, gli attributi e i parametri:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## Informazioni di riferimento sullo schema del modello di applicazione UE-V 2,0


Questa sezione descrive in dettaglio la struttura XML del modello di posizione delle impostazioni di 2,0 UE-V e fornisce indicazioni per la modifica di questo file.

### In questa sezione

-   [Attributo di codifica e dichiarazione XML](#xml)

-   [Spazio dei nomi e elemento radice](#namespace)

-   [Tipi di dati](#data)

-   [Elemento Name](#name)

-   [Elemento ID](#id)

-   [Elemento version](#version)

-   [Elemento Author](#author)

-   [Processi ed elementi process](#processes)

-   [Elemento Application](#application)

-   [Elemento comune](#common)

-   [Elemento SettingsLocationTemplate](#settingslocationtemplate)

-   [Appendice: SettingsLocationTemplate. xsd](#appendix)

### <a href="" id="xml"></a>Attributo di codifica e dichiarazione XML

**Obbligatorio: vero**

**Digitare: stringa**

La dichiarazione XML deve specificare l'attributo XML version 1,0 ( &lt; ? XML version = "1.0" &gt; ). I modelli di posizione delle impostazioni creati dal generatore UE-V vengono salvati nella codifica UTF-8, anche se la codifica non è specificata in modo esplicito. È consigliabile includere l'attributo encoding = "UTF-8" in questo elemento come procedura consigliata. Tutti i modelli inclusi nel prodotto specificano anche questo tag (Vedi i documenti in%ProgramFiles%\\Microsoft User Experience Virtualization\\Templates per riferimento). Ad esempio:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a>Spazio dei nomi e elemento radice

**Obbligatorio: vero**

**Digitare: stringa**

UE-V usa lo https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate spazio dei nomi per tutte le applicazioni. SettingsLocationTemplate è l'elemento radice e contiene tutti gli altri elementi. Fare riferimento a SettingsLocationTemplate in tutti i modelli usando questo tag:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a>Tipi di dati

Questi sono i tipi di dati per lo schema del modello di applicazione UE-V.

<a href="" id="guid"></a>**GUID** GUID descrive un'espressione regolare dell'identificatore univoco globale standard nel formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {4} -\ [a-fa-F0-9 \] {12} \ \}". Viene usato nell'elemento Filesetting\\Root\\KnownFolder per verificare la formattazione delle cartelle note.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString si riferisce al nome del file di un processo da monitorare. I relativi valori sono limitati dall'espressione Regex \ [^ \ &lt; &gt; \ \ \ \ \ /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i caratteri del colon.

<a href="" id="idstring"></a>**IdString** IDString fa riferimento al valore ID di elementi Application, SettingsLocationTemplate e elementi comuni (usati per descrivere i gruppi di applicazioni che condividono le impostazioni comuni). È limitato dalla stessa Regex di FilenameString (\ [^ \ \ \ \ \ \? \ \ \ \ &lt; &gt; \ \ \ \ \ \ \ \ \ \ /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion è un valore intero usato per descrivere la revisione del modello di posizione delle impostazioni. Il valore può essere compreso tra 0 e 2147483647.

<a href="" id="empty"></a>**Empty** Empty fa riferimento a un valore null. Viene usato in Process\\ShellProcess per indicare che non esiste un processo da monitorare. Questo valore non deve essere usato nei modelli di applicazione.

<a href="" id="author"></a>**Autore** Il tipo di dati Author è un tipo complesso che identifica l'autore di un modello. Contiene due elementi figlio: **nome** e **posta elettronica**. All'interno del tipo di dati Author, l'elemento Name è obbligatorio mentre l'elemento di posta elettronica è facoltativo. Questo tipo è descritto in modo più dettagliato sotto l'elemento SettingsLocationTemplate.

<a href="" id="range"></a>**Intervallo** Range definisce una classe integer costituita da due elementi figlio: **Minimum** e **Maximum**. Questo tipo di dati viene implementato nel tipo di dati ProcessVersion. Se specificato, è necessario includere i valori minimo e massimo.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion definisce un tipo con quattro elementi figlio: **Major**, **minor**, **Build**e **patch**. Questo tipo di dati viene usato dall'elemento Process per popolare i relativi valori ProductVersion e fileversion. I dati per questo tipo sono un valore di intervallo. L'elemento figlio principale è obbligatorio e gli altri sono facoltativi.

<a href="" id="architecture"></a>**Architettura** L'architettura enumera due valori possibili: **Win32** e **Win64**. Questi valori vengono usati per specificare l'architettura di processo.

<a href="" id="process"></a>**Processo** Il tipo di dati processo è un contenitore usato per descrivere i processi da monitorare da UE-V. Contiene sei elementi figlio: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**. Questa tabella descrive in dettaglio i rispettivi tipi di dati di ogni elemento:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Tipo di dati</th>
<th align="left">Mandatory</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome file</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>True</p></td>
</tr>
<tr class="even">
<td align="left"><p>Architettura</p></td>
<td align="left"><p>Architettura</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>False</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Processi** Il tipo di dati processes rappresenta un contenitore per una raccolta di uno o più elementi Process. Nel tipo di sequenza processi sono supportati due elementi figlio: **Process** e **ShellProcess**. Process è un elemento di tipo Process e ShellProcess è di tipo dati vuoto. Nella sequenza devono essere identificati almeno un elemento.

<a href="" id="path"></a>**Percorso** Path viene usato da RegistrySetting e filesetting per fare riferimento ai percorsi del registro di sistema e dei file. Questo elemento supporta due attributi facoltativi: **ricorsive** e **DeleteIfNotFound**. Entrambi i valori sono impostati su default = "false".

Ricorsive indica che il percorso e tutte le sottocartelle sono incluse per le impostazioni dei file o che tutte le chiavi del registro di sistema figlio sono incluse per le impostazioni del registro di sistema. In entrambi i casi, tutti gli elementi a livello corrente sono inclusi nei dati acquisiti. Per un oggetto fileSettings, tutti i file all'interno della cartella specificata sono inclusi nei dati acquisiti da UE-V, ma le cartelle non sono incluse. Per i percorsi del registro di sistema, vengono acquisiti tutti i valori nel percorso corrente, ma le chiavi del registro di sistema figlio non vengono acquisite. In entrambi i casi, è necessario prestare attenzione per evitare l'acquisizione di set di dati di grandi dimensioni o un numero elevato di elementi.

L'attributo DeleteIfNotFound rimuove l'impostazione dai dati del percorso di archiviazione delle impostazioni dell'utente. Questo potrebbe essere utile nei casi in cui la rimozione di queste impostazioni dal pacchetto salverà una grande quantità di spazio su disco nel file server del percorso di archiviazione delle impostazioni.

<a href="" id="filemask"></a>**FileMask** FileMask specifica solo determinati tipi di file per la cartella definita da path. Ad esempio, Path può essere `C:\users\username\files` e FileMask può `*.txt` includere solo file di testo.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting rappresenta un contenitore per le chiavi del registro di sistema e i valori e il comportamento desiderato associato da parte dell'agente UE-V. In questo tipo sono definiti quattro elementi figlio: **path**, **Name**, **Exclude**e una sequenza di valori **path** e **Name**.

<a href="" id="filesetting"></a>**Impostazione Filesetting** Filesetting contiene i parametri associati ai percorsi di file e file. Vengono definiti quattro elementi figlio: **root**, **path**, **FileMask**ed **Exclude**. Root è obbligatorio e gli altri sono facoltativi.

<a href="" id="settings"></a>**Impostazioni** Settings è un contenitore per tutte le impostazioni che si applicano a un determinato modello. Contiene le istanze delle impostazioni del registro di sistema, file, SystemParameter e CustomAction descritte in precedenza. Inoltre, può contenere anche gli elementi figlio seguenti con i comportamenti descritti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Asincrona</p></td>
<td align="left"><p>I pacchetti di impostazioni asincrone vengono applicati senza bloccare l'avvio dell'applicazione in modo che l'avvio dell'applicazione proceda mentre le impostazioni sono ancora applicate. Questa operazione è utile per le impostazioni che possono essere applicate in modo asincrono, ad esempio quelle <code>get/set</code> tramite un'API, come SystemParameterSetting.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>Per impostazione predefinita, UE-V Salva solo le impostazioni per un'applicazione quando viene chiusa l'ultima istanza di un'applicazione che usa il modello. Quando questo elemento è impostato su "false", UE-V Esporta le impostazioni anche se sono in uso altre istanze di un'applicazione. Modelli adatti: quelli che includono una sezione elemento comune, forniti con UE-V, usano questo contrassegno per consentire alle impostazioni condivise di esportare sempre in prossimità dell'applicazione, impedendo l'esportazione di impostazioni specifiche dell'applicazione finché non viene chiusa l'ultima istanza.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a>Elemento Name

**Obbligatorio: vero**

**Digitare: stringa**

Nome specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. In generale, evita di fare riferimento alle informazioni sulla versione, perché questo può essere obiettato dall'elemento ProductVersion. Ad esempio, specificare `<Name>My Application</Name>` invece di `<Name>My Application 1.1</Name>` .

**Nota**  UE-V non fa riferimento a DTD esterni, quindi non è possibile usare le entità denominate in un modello di posizione delle impostazioni. Ad esempio, non usare per &reg; fare riferimento al segno di firma del marchio registrato®. USA invece i riferimenti numerati canonici per includere questi tipi di caratteri speciali, ad esempio & \ #174 per il carattere®. Questa regola si applica a tutti i valori stringa in questo documento.

Vedere <http://www.w3.org/TR/xhtml1/dtds.html> per un elenco completo delle entità di caratteri. I documenti con codifica UTF-8 possono includere direttamente i caratteri Unicode. Il salvataggio dei modelli tramite il generatore UE-V converte automaticamente le entità di caratteri nelle rappresentazioni Unicode.

 

### <a href="" id="id"></a>Elemento ID

**Obbligatorio: vero**

**Digitare: stringa**

ID popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione, ad esempio, Vedi l'output dei cmdlet di PowerShell Get-UevTemplate e Get-UevTemplateProgram. Per convenzione, questo tag non deve contenere spazi, che semplificano lo scripting. I numeri di versione delle applicazioni devono essere specificati in questo elemento per consentire una facile identificazione del modello, ad esempio `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version"></a>Elemento version

**Obbligatorio: vero**

**Digitare: integer**

**Valore minimo: 0**

**Valore massimo: 2147483647**

La versione identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche. Il generatore UE-V incrementa automaticamente questo numero per uno ogni volta che il modello viene salvato. Si noti che questo campo deve essere un numero intero Integer; i valori frazionari, ad esempio `<Version>2.5</Version>` non sono consentiti.

**Suggerimento:** È possibile salvare le note sulle modifiche della versione usando i tag di commento XML `<!-- -->` , ad esempio:

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

**Importante**  Questo valore viene interrogato per determinare se una nuova versione di un modello deve essere applicata a un modello esistente in queste istanze:

-   Quando viene eseguita l'attività di aggiornamento automatico del modello programmato

-   Quando viene eseguito il cmdlet di PowerShell Update-UevTemplate

-   Quando viene chiamato il metodo di aggiornamento microsoft\\uev: SettingsLocationTemplate tramite WMI

 

### <a href="" id="author"></a>Elemento Author

**Obbligatorio: falso**

**Digitare: stringa**

Autore identifica il creatore del modello di posizione delle impostazioni. Sono supportati due elementi figlio facoltativi: **nome** e **posta elettronica**. Entrambi gli attributi sono facoltativi, ma, se l'elemento figlio del messaggio di posta elettronica viene specificato, deve essere accompagnato dall'elemento Name. Autore fa riferimento al nome completo del contatto per il modello di posizione delle impostazioni e la posta elettronica deve fare riferimento a un indirizzo di posta elettronica per l'autore. È consigliabile includere queste informazioni nei modelli pubblicati pubblicamente, ad esempio nella [raccolta modelli di UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes"></a>Processi ed elementi process

**Obbligatorio: vero**

**Digitare: elemento**

I processi contengono almeno un `<Process>` elemento, che a sua volta contiene gli elementi figlio seguenti: **filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**e **fileversion**. L'elemento figlio filename è obbligatorio e gli altri sono facoltativi. Un elemento completamente popolato contiene tag simili a questo esempio:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### Nome file

**Obbligatorio: vero**

**Digitare: stringa**

Filename si riferisce al nome effettivo del file eseguibile visualizzato nel file System. Questo elemento specifica il criterio principale usato da UE-V per valutare se un modello si applica o meno a un processo. Questo elemento deve essere specificato nel codice XML del modello di posizione delle impostazioni.

I nomi file validi non devono corrispondere all'espressione regolare \ [^ \ \ \ \ \ \ \ &lt; &gt; /: \] +, ovvero potrebbero non contenere caratteri barra rovesciata, asterischi o caratteri jolly del punto interrogativo, il carattere della pipe, il segno maggiore o minore di, la barra o i due punti (il \ \? \* | &lt; &gt; /o: caratteri.).

**Suggerimento:** Per testare una stringa con questa regex, usare una finestra di comando di PowerShell e sostituire il nome dell'eseguibile per **nomefile**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Il valore **true** indica che la stringa contiene caratteri non validi. Ecco alcuni esempi di valori illegali:

-   \\\\server\\share\\program.exe

-   Program \ *. exe

-   ram.exe Pro?

-   Programma &lt; 1 &gt; . exe

**Nota**  Il generatore UE-V codifica i caratteri maggiore di e minore di e &gt; &lt; rispettivamente.

 

In rari casi, il valore FileName non include necessariamente l'estensione exe, ma deve essere specificato come parte del valore. Ad esempio, `<Filename>MyApplictication.exe</Filename>` deve essere specificato al posto di `<Filename>MyApplictication</Filename>` . Il secondo esempio non applica il modello al processo se il nome effettivo del file eseguibile è "MyApplication.exe".

### Architettura

**Obbligatorio: falso**

**Digitare: Architecture (String)**

L'architettura si riferisce all'architettura del processore per cui è stato compilato l'eseguibile di destinazione. I valori validi sono Win32 per le applicazioni a 32 bit o Win64 per le applicazioni a 64 bit. Se presente, questo tag limita l'applicabilità del modello di posizione delle impostazioni a una particolare architettura dell'applicazione. Per un esempio, confronta l'esperienza utente di%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml e MicrosoftOffice2010Win64.xml file inclusi in UE-V. Questa operazione è utile quando i percorsi relativi cambiano tra versioni diverse di un file eseguibile o se le impostazioni sono state aggiunte o rimosse quando si spostano da un'architettura del processore a un'altra.

Se questo elemento è assente, il modello di posizione delle impostazioni ignora l'architettura del processo e si applica ai processi di 32 e 64 bit se il nome file e gli altri attributi si applicano.

**Nota**  UE-V non supporta i processori ARM in questa versione.

 

### ProductName

**Obbligatorio: falso**

**Digitare: stringa**

ProductName è un elemento facoltativo usato per identificare un prodotto per scopi amministrativi o per la creazione di report. ProductName è diverso dal nome del file, in quanto il relativo valore non contiene restrizioni per le espressioni regolari. In questo modo è possibile comprendere più facilmente le descrizioni di un processo in cui il nome eseguibile potrebbe non essere ovvio. Ad esempio:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obbligatorio: falso**

**Digitare: stringa**

FileDescription è un tag facoltativo che consente di avere una descrizione amministrativa del file eseguibile. Si tratta di un campo di testo gratuito e può essere utile per distinguere più eseguibili in un pacchetto software in cui è necessario identificare la funzione dell'eseguibile.

Ad esempio, in un'applicazione appropriata può essere utile specificare i promemoria relativi alla funzione di due eseguibili (MyApplication.exe e MyApplicationHelper.exe), come illustrato di seguito:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obbligatorio: falso**

**Digitare: stringa**

ProductVersion si riferisce alle versioni di prodotto principali e secondarie di un file, oltre a una build e a un livello di patch. ProductVersion è un elemento facoltativo, ma se specificato deve contenere almeno l'elemento figlio principale. Il valore deve esprimere un intervallo nella forma Minimum = "X" Maximum = "Y" dove X e Y sono numeri interi. I valori minimo e massimo possono essere identici.

Gli elementi della versione del prodotto e del file possono essere lasciati non specificati. In questo modo il modello si applica a "versione agnostica", ovvero il modello verrà applicato a tutte le versioni del file eseguibile specificato.

**Esempio 1:**

Versione del prodotto: 1,0 specificato nel generatore di UE-V produce il codice XML seguente:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Esempio 2:**

Versione file: 5.0.2.1000 specificato nel generatore UE-V produce il codice XML seguente:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Esempio errato 1-intervallo incompleto:**

È presente solo l'attributo Minimum. Anche il valore massimo deve essere incluso in un intervallo.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Esempio errato 2-secondario specificato senza elemento principale:**

Solo l'elemento secondario è presente. Anche Major deve essere incluso.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obbligatorio: falso**

**Digitare: stringa**

FileVersion differenzia la versione finale di un'applicazione pubblicata e i dettagli di compilazione interni di un eseguibile del componente. Per la maggior parte delle applicazioni commerciali, questi numeri sono identici. Dove variano, la versione del prodotto di un file indica l'identificazione di una versione generica di un file, mentre la versione del file indica una build specifica di un file, come nel caso di un hotfix o di un aggiornamento. Questo identifica in modo univoco i file senza interrompere la logica di rilevamento.

Per determinare la versione del prodotto e la versione del file di un determinato eseguibile, fare clic con il pulsante destro del mouse sul file in Esplora risorse, scegliere Proprietà e quindi fare clic sulla scheda Dettagli.

L'inclusione di un elemento FileVersion per un'applicazione consente di definire una logica di rilevamento più granulare, ma non è necessaria per la maggior parte delle applicazioni. Le impostazioni dell'elemento ProductVersion sono controllate per prime e quindi viene selezionata la versione Fileversion. Verrà applicata l'impostazione più restrittiva.

Gli elementi figlio e le regole di sintassi per fileversion sono identici a quelli di ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a>Elemento Application

Application è un contenitore per le impostazioni che si applicano a una particolare applicazione. Si tratta di una raccolta dei campi/tipi seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. Per altre informazioni, Vedi <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione. Per altre informazioni, Vedi <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione facoltativa del modello.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versione</p></td>
<td align="left"><p>Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche. Per altre informazioni, vedere la <a href="#version" data-raw-source="[Version](#version)"> versione </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controlla se il modello è abilitato in combinazione con un account Microsoft. Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365. Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Processi</p></td>
<td align="left"><p>Un contenitore per una raccolta di uno o più elementi Process. Per altre informazioni, vedere <a href="#processes" data-raw-source="[Processes](#processes)"> processi </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Impostazioni</p></td>
<td align="left"><p>Un contenitore per tutte le impostazioni che si applicano a un determinato modello. Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction. Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data" data-raw-source="[Data types](#data)"> tipi di dati </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a>Elemento comune

Common è simile a un elemento Application, ma è sempre associato a due o più elementi Application. La sezione comune rappresenta il set di impostazioni condivise tra le istanze dell'applicazione. Si tratta di una raccolta dei campi/tipi seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. Per altre informazioni, Vedi <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione. Per altre informazioni, Vedi <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione facoltativa del modello.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versione</p></td>
<td align="left"><p>Identifica la versione del modello di posizione delle impostazioni per il rilevamento amministrativo delle modifiche. Per altre informazioni, vedere la <a href="#version" data-raw-source="[Version](#version)"> versione </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controlla se il modello è abilitato in combinazione con un account Microsoft. Se la sincronizzazione di MSA è abilitata per un utente in un computer, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>Analogamente a MSA, controlla se questo modello è abilitato in combinazione con Office365. Se si usa Office 365 per sincronizzare le impostazioni, il modello verrà disabilitato automaticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni</p></td>
<td align="left"><p>Un contenitore per tutte le impostazioni che si applicano a un determinato modello. Contiene istanze delle impostazioni registro di sistema, file, SystemParameter e CustomAction. Per altre informazioni, vedere <strong> impostazioni </strong> nei <a href="#data" data-raw-source="[Data types](#data)"> tipi di dati </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a>Elemento SettingsLocationTemplate

Questo elemento definisce le impostazioni per una singola applicazione o una famiglia di applicazioni.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Specifica un nome univoco per il modello di posizione delle impostazioni. Viene usato per scopi di visualizzazione quando si fa riferimento al modello in WMI, PowerShell, Visualizzatore eventi e registri di debug. Per altre informazioni, Vedi <a href="#name" data-raw-source="[Name](#name)"> nome </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Popola un identificatore univoco per un determinato modello. Questo tag diventa l'identificatore principale usato dall'agente UE-V per fare riferimento al modello in fase di esecuzione. Per altre informazioni, Vedi <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione facoltativa del modello.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nome facoltativo visualizzato nell'interfaccia utente, localizzato da una lingua locale.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descrizione del modello facoltativa localizzata in base alle impostazioni locali della lingua.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a>Appendice: SettingsLocationTemplate. xsd

Ecco il file SettingsLocationTemplate. xsd che Mostra gli elementi, gli elementi figlio, gli attributi e i parametri:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## Argomenti correlati


[Uso dei modelli Custom UE-V 2. x e del generatore UE-V 2. x](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





