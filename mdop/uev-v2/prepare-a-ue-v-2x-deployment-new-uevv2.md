---
title: Preparare una distribuzione UE-V 2. x
description: Preparare una distribuzione UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826425"
---
# Preparare una distribuzione UE-V 2. x


La pianificazione e la preparazione da eseguire prima di distribuire Microsoft User Experience Virtualization (UE-V) 2,0 o 2,1 è una soluzione per la sincronizzazione delle impostazioni tra i dispositivi a cui gli utenti accedono nell'organizzazione. Questo argomento consente di determinare il tipo di distribuzione che si sta eseguendo e la preparazione che è possibile eseguire in anticipo in modo che la distribuzione abbia successo.

Prima di tutto, esaminiamo le attività da eseguire per distribuire UE-V:

-   Pianificare la distribuzione di UE-V

    Prima di distribuire qualsiasi elemento, un buon primo passaggio consiste nell'eseguire un po' di pianificazione in modo da determinare quali funzionalità di UE-V verranno distribuite. Quindi, se si lascia questa pagina, assicurarsi di tornare e leggere le informazioni di pianificazione seguenti.

-   [Distribuire le funzionalità necessarie per UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Ogni distribuzione UE-V richiede queste attività:

    -   [Definire una posizione di archiviazione delle impostazioni](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Decidere come distribuire l'agente UE-V e gestire le configurazioni di UE-V](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Installare l'agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) in tutti i computer degli utenti che necessitano di impostazioni sincronizzate

-   Facoltativamente, è possibile [distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    La pianificazione consentirà di capire se si vuole che UE-V supporti la sincronizzazione delle impostazioni per le applicazioni personalizzate (di terze parti o line-of-business), che richiede queste funzionalità di UE-V:

    -   [Installare il generatore di UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) in modo da poter creare, modificare e convalidare i modelli di posizione delle impostazioni personalizzati necessari per sincronizzare le impostazioni delle applicazioni personalizzate

    -   [Creare modelli di posizione delle impostazioni personalizzate](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) usando il generatore UE-V

    -   [Distribuire un catalogo di modelli di impostazioni UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) che si usa per archiviare i modelli di posizione delle impostazioni personalizzate

Questo diagramma flusso di lavoro offre una comprensione di alto livello di una distribuzione UE-V e delle decisioni che determinano la modalità di distribuzione di UE-V nell'organizzazione.

![deploymentworkflow](images/deploymentworkflow.png)

**Pianificazione di una distribuzione di UE-V:** Prima di tutto, devi pianificare la pianificazione in modo da determinare i componenti UE-V che dovrai distribuire. La pianificazione di una distribuzione UE-V implica questi elementi:

-   [Decidere se sincronizzare le impostazioni per le applicazioni personalizzate](#deciding)

    In questo modo viene determinato se si installerà il generatore UE-V durante la distribuzione, che consente di creare modelli di posizione delle impostazioni personalizzati. Si tratta delle operazioni seguenti:

    Esaminare le [Impostazioni sincronizzate automaticamente in una distribuzione di UE-V](#autosyncsettings).

    [Determinare se sono necessarie impostazioni sincronizzate per altre applicazioni](#determinesettingssync).

-   Esaminare [altre considerazioni per la distribuzione di UE-V](#considerations), ad esempio disponibilità elevata e pianificazione della capacità.

-   [Confermare i prerequisiti e le configurazioni supportate per la versione UE-V](#prereqs)

## <a href="" id="deciding"></a>Decidere se sincronizzare le impostazioni per le applicazioni personalizzate


In una distribuzione di UE-V vengono sincronizzate automaticamente molte impostazioni. Ma è anche possibile personalizzare UE-V per sincronizzare le impostazioni per altre applicazioni, ad esempio le app line-of-business e di terze parti.

Decidere se si vuole che la sincronizzazione delle impostazioni per le applicazioni personalizzate da parte di UE-V sia probabilmente la parte più importante della pianificazione della distribuzione di UE-V. Gli argomenti di questa sezione ti aiuteranno a prendere questa decisione.

### <a href="" id="autosyncsettings"></a>Impostazioni sincronizzate automaticamente in una distribuzione di UE-V

In questa sezione vengono fornite informazioni sulle impostazioni sincronizzate per impostazione predefinita in UE-V, incluse le seguenti:

Applicazioni desktop le cui impostazioni sono sincronizzate per impostazione predefinita

Impostazioni desktop di Windows sincronizzate per impostazione predefinita

Dichiarazione di supporto per la sincronizzazione delle impostazioni dell'app Windows

Vedere [modelli di impostazioni per la virtualizzazione dell'esperienza utente (UE-v) per Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) per scaricare un elenco completo delle impostazioni specifiche di microsoft Office 2013, microsoft Office 2010 e microsoft Office 2007 sincronizzate da UE-v.

### Applicazioni desktop sincronizzate per impostazione predefinita in UE-V 2,1 e UE-V 2,1 SP1

Quando si installa l'agente UE-V 2,1 o 2,1 SP1, viene registrato un gruppo predefinito di modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per queste applicazioni Microsoft comuni.

**Suggerimento**  
**Sincronizzazione delle impostazioni di Microsoft Office 2007** -in UE-V 2,1 e 2,1 SP1, un modello di posizione delle impostazioni non è più incluso per impostazione predefinita per le applicazioni di Office 2007. Tuttavia, è comunque possibile usare i modelli di Office 2007 da UE-V 2,0 o versioni precedenti e ottenere i modelli dalla [raccolta modelli di UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoria applicazione</strong></th>
<th align="left"><strong>Descrizione</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Applicazioni di Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applicazioni di Microsoft Office 2013</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Office 2013 Upload Center</p>
<p>Microsoft OneDrive for Business 2013</p>
<p>I modelli di posizione delle impostazioni di Microsoft Office 2013 della versione UE-V 2,1 e 2,1 SP1 includono il supporto per la firma di Outlook migliorato. È stata aggiunta la sincronizzazione delle impostazioni predefinite della firma per i messaggi di posta elettronica nuovi, di risposta e inoltrati.</p>
<div class="alert">
<strong>Nota</strong><br/><p>È necessario creare un profilo di Outlook per qualsiasi dispositivo in cui un utente vuole sincronizzare la firma di Outlook. Se il profilo non è già stato creato, l'utente può crearne uno e quindi riavviare Outlook in tale dispositivo per abilitare la sincronizzazione della firma.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Opzioni del browser: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</p></td>
<td align="left"><p>Preferiti, Home page, schede e barre degli strumenti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>UE-V non esegue la roaming delle impostazioni per i cookie di Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Accessori per Windows</p></td>
<td align="left"><p>Microsoft Calculator, blocco note, WordPad.</p></td>
</tr>
</tbody>
</table>



**Nota**  
UE-V 2,1 SP1 non sincronizza le impostazioni tra la calcolatrice Microsoft in Windows 10 e la calcolatrice Microsoft nei sistemi operativi precedenti.



### Applicazioni desktop sincronizzate per impostazione predefinita in UE-V 2,0

Quando si installa l'agente UE-V 2,0, viene registrato un gruppo predefinito di modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per queste applicazioni Microsoft comuni.

**Suggerimento**  
**Sincronizzazione delle impostazioni di Microsoft office 2013** -in UE-v 2,0 un modello di posizione delle impostazioni non è incluso per impostazione predefinita per le applicazioni di Office 2013, ma è disponibile per il download dalla [raccolta modelli di UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589). La [sincronizzazione di office 2013 con UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fornisce informazioni dettagliate sui modelli supportati che sincronizzano le impostazioni di Office 2013.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoria applicazione</strong></th>
<th align="left"><strong>Descrizione</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Applicazioni di Microsoft Office 2007</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
<td align="left"><p>Microsoft Access 2007</p>
<p>Microsoft Communicator 2007</p>
<p>Microsoft Excel 2007</p>
<p>Microsoft InfoPath 2007</p>
<p>Microsoft OneNote 2007</p>
<p>Microsoft Outlook 2007</p>
<p>Microsoft PowerPoint 2007</p>
<p>Microsoft Project 2007</p>
<p>Microsoft Publisher 2007</p>
<p>Microsoft SharePoint Designer 2007</p>
<p>Microsoft Visio 2007</p>
<p>Microsoft Word 2007</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applicazioni di Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scaricare un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Opzioni del browser: Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10</p></td>
<td align="left"><p>Preferiti, Home page, schede e barre degli strumenti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>UE-V non esegue la roaming delle impostazioni per i cookie di Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Accessori per Windows</p></td>
<td align="left"><p>Microsoft Calculator, blocco note, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a>Impostazioni di Windows sincronizzate per impostazione predefinita

UE-V include i modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per queste impostazioni di Windows.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">impostazioni di Windows</th>
<th align="left">Descrizione</th>
<th align="left">Applicare il</th>
<th align="left">Esporta in</th>
<th align="left">Stato predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sfondo del desktop</p></td>
<td align="left"><p>Sfondo del desktop attualmente attivo o sfondo.</p></td>
<td align="left"><p>Eventi attività pianificati per l'accesso, l'apertura, la connessione remota.</p></td>
<td align="left"><p>Disconnessione, blocco, disconnessione remota, utente che fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o nell'intervallo di attività pianificato</p></td>
<td align="left"><p>Abilitato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accessibilità</p></td>
<td align="left"><p>Impostazioni di accessibilità e input, Microsoft Magnifier, Assistente vocale e tastiera su schermo.</p></td>
<td align="left"><p>Solo accesso.</p></td>
<td align="left"><p>Disconnessione, utente che fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o nell'intervallo di attività pianificato</p></td>
<td align="left"><p>Abilitato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni desktop</p></td>
<td align="left"><p>Menu Start e impostazioni della barra delle applicazioni, Opzioni cartella, icone desktop predefinite, clock aggiuntivi e impostazioni area geografica e lingua.</p></td>
<td align="left"><p>Solo accesso.</p></td>
<td align="left"><p>Disconnessione, utente che fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o in un'attività pianificata</p></td>
<td align="left"><p>Abilitato</p></td>
</tr>
</tbody>
</table>



**Nota**  
A partire da Windows 8, UE-V non esegue la roaming delle impostazioni relative alla schermata Start, ad esempio gli elementi e le posizioni. Inoltre, UE-V non supporta la sincronizzazione di elementi della barra delle applicazioni bloccati o di collegamenti di file di Windows.



**Importante**  
UE-V 2,1 SP1 si aggira sulle impostazioni della barra delle applicazioni tra i dispositivi Windows 10. Tuttavia, UE-V non sincronizza le impostazioni della barra delle applicazioni tra dispositivi e dispositivi Windows 10 in cui sono in uso sistemi operativi precedenti.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gruppo di impostazioni</th>
<th align="left">Categoria</th>
<th align="left">Catturare</th>
<th align="left">Applica</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Impostazioni applicazione</strong></p></td>
<td align="left"><p>App di Windows  </p></td>
<td align="left"><p>Chiudi app</p>
<p>Evento di modifica delle impostazioni dell'app Windows</p></td>
<td align="left"><p>Avviare l'app UE-V monitor all'avvio</p>
<p>Aprire l'app</p>
<p>Evento di modifica delle impostazioni dell'app Windows</p>
<p>Arrivo di un pacchetto di impostazioni</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Applicazioni desktop</p></td>
<td align="left"><p>Applicazione chiusa</p></td>
<td align="left"><p>L'applicazione si apre e si chiude</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Impostazioni desktop</strong></p></td>
<td align="left"><p>Sfondo del desktop</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso, sblocco, connessione remota, notifica del nuovo arrivo del pacchetto, l'utente fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o viene eseguita un'attività pianificata.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Accesso facilitato (comune-accessibilità, Assistente vocale, lente di ingrandimento, tastiera su schermo)</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Accesso facilitato (Shell-audio, accessibilità, tastiera, mouse)</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso, sblocco, connessione remota, notifica del nuovo arrivo del pacchetto, l'utente fa clic su <strong> Sincronizza ora </strong> nel centro impostazioni società o viene eseguita un'attività pianificata</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Impostazioni desktop</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso</p></td>
</tr>
</tbody>
</table>



### UE-V-supporto per le app di Windows

Per le app di Windows, lo sviluppatore di app specifica le impostazioni sincronizzate. Puoi specificare quali app di Windows sono abilitate per la sincronizzazione delle impostazioni.

Per visualizzare un elenco di app di Windows che possono sincronizzare le impostazioni in un computer con il nome della famiglia di pacchetti, lo stato abilitato e l'origine abilitata, al prompt dei comandi di Windows PowerShell immettere: `Get-UevAppxPackage`

**Nota**  
A partire da Windows 8, UE-V non sincronizza le impostazioni delle app di Windows se l'utente del dominio collega le proprie credenziali di accesso al proprio account Microsoft. Questo collegamento sincronizza le impostazioni con Microsoft OneDrive in modo da UE-V, che disabilita la sincronizzazione delle impostazioni delle app di Windows.



### UE-V-supporto per le stampanti mobili

UE-V 2,1 SP1 consente alle stampanti di rete di spostarsi tra i dispositivi in modo che l'utente abbia accesso alle stampanti di rete quando si è connessi a qualsiasi dispositivo della rete. Questo include il roaming della stampante impostata come predefinita.

La stampante in roaming in UE-V richiede uno di questi scenari:

-   Il server di stampa può scaricare il driver necessario quando si sposta in roaming su un nuovo dispositivo.

-   Il driver per la stampante di rete mobile è preinstallato in qualsiasi dispositivo che deve accedere alla stampante di rete.

-   Il driver della stampante può essere ottenuto da Windows Update.

**Nota**  
La funzionalità di roaming della stampante UE-V **non** esegue la roaming delle impostazioni o delle preferenze della stampante, ad esempio la stampa fronte-retro.



### <a href="" id="determinesettingssync"></a>Determinare se sono necessarie impostazioni sincronizzate per altre applicazioni

Dopo aver esaminato le impostazioni sincronizzate automaticamente in una distribuzione di UE-V, si vuole decidere se sincronizzare le impostazioni per altre applicazioni, perché determina la modalità di distribuzione di UE-V in tutta l'organizzazione.

In qualità di amministratore, quando si considerano le applicazioni desktop da includere nella soluzione UE-V, valutare quali impostazioni possono essere personalizzate dagli utenti e come e dove l'applicazione archivia le proprie impostazioni. Non tutte le applicazioni desktop hanno impostazioni che possono essere personalizzate o che sono personalizzate in routine dagli utenti. Inoltre, non tutte le impostazioni delle applicazioni desktop possono essere sincronizzate in modo sicuro in più computer o ambienti.

In generale, è possibile sincronizzare le impostazioni che soddisfano i criteri seguenti:

-   Impostazioni archiviate in percorsi accessibili dall'utente. Ad esempio, non sincronizzare le impostazioni archiviate in system32 o all'esterno della sezione HKEY \ _CURRENT \ _USER (HKCU) del registro di sistema.

-   Impostazioni non specifiche per il computer specifico. Ad esempio, Escludi configurazioni di rete o hardware.

-   Impostazioni che è possibile sincronizzare tra computer senza rischio di dati danneggiati. Ad esempio, non usare le impostazioni archiviate in un file di database.

### <a href="" id="checklistsettingssync"></a>Elenco di controllo per la valutazione delle applicazioni personalizzate

Se si è deciso di usare le impostazioni sincronizzate per altre applicazioni, è possibile utilizzare questo elenco di controllo per individuare le applicazioni che si vogliono includere.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Questa applicazione contiene le impostazioni che l'utente può personalizzare?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>È importante per l'utente che queste impostazioni siano sincronizzate?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Queste impostazioni utente sono già gestite da una soluzione dei criteri di gestione o impostazioni delle applicazioni? UE-V applica le impostazioni dell'applicazione all'avvio dell'applicazione e alle impostazioni di Windows agli eventi logon, Unlock o Connect remoto. Se si usa UE-V con altre soluzioni di condivisione delle impostazioni, gli utenti potrebbero riscontrare incongruenze tra le impostazioni sincronizzate.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Le impostazioni dell'applicazione sono specifiche per il computer? Le preferenze e le personalizzazioni dell'applicazione associate all'hardware o a configurazioni di computer specifiche non vengono sincronizzate in modo coerente tra le sessioni e possono causare un'esperienza di applicazione insufficiente.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Le impostazioni dell'archivio applicazioni si trovano nella directory Program Files o nella directory di file che si trova nella directory Users <strong> </strong> [nome utente] &lt; Strong &gt; AppData </strong> &lt; Strong &gt; LocalLow </strong> ? I dati dell'applicazione archiviati in uno di questi percorsi in genere non devono essere sincronizzati con l'utente, perché questi dati sono specifici del computer o perché i dati sono troppo grandi per la sincronizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L'applicazione archivia le impostazioni in un file che contiene altri dati dell'applicazione che non devono essere sincronizzati? UE-V sincronizza i file come unità singola. Se le impostazioni sono archiviate in file che includono dati dell'applicazione diversi dalle impostazioni, la sincronizzazione di questi dati aggiuntivi può causare un'esperienza di applicazione insufficiente.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Dimensioni dei file che contengono le impostazioni Le prestazioni della sincronizzazione delle impostazioni possono essere influenzate da file di grandi dimensioni. L'inclusione di file di grandi dimensioni può influire sulle prestazioni della sincronizzazione delle impostazioni.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a>Altre considerazioni durante la preparazione di una distribuzione UE-V


È consigliabile considerare questi elementi anche quando si sta preparando la distribuzione di UE-V:

-   [Gestione della sincronizzazione delle credenziali](#creds)

-   [Sincronizzazione delle impostazioni dell'app Windows](#appxsettings)

-   [Modelli di posizione delle impostazioni UE-V personalizzati](#custom)

-   [Configurazioni delle impostazioni utente non intenzionali](#prevent)

-   [Prestazioni e capacità](#capacity)

-   [Disponibilità elevata](#high)

-   [Sincronizzazione di un orologio del computer](#clocksync)

### <a href="" id="creds"></a>Gestione della sincronizzazione delle credenziali in UE-V 2,1 e UE-V 2,1 SP1

Molte applicazioni aziendali, tra cui Microsoft Outlook e Lync, richiedono agli utenti le credenziali di dominio all'accesso. Gli utenti hanno la possibilità di salvare le credenziali su disco per evitare di dover immetterle ogni volta che aprono queste applicazioni. Abilitazione della sincronizzazione delle credenziali mobili consente agli utenti di salvare le proprie credenziali in un computer ed evitare di reimmetterle in tutti i computer usati nell'ambiente. Gli utenti possono sincronizzare alcune credenziali di dominio con UE-V 2,1 e 2,1 SP1.

**Importante**  
La sincronizzazione delle credenziali è disabilitata per impostazione predefinita. Per implementare questa funzionalità, è necessario abilitare esplicitamente la sincronizzazione delle credenziali durante la distribuzione.



UE-V 2,1 e 2,1 SP1 possono sincronizzare le credenziali aziendali, ma non le credenziali di roaming destinate solo all'uso nel computer locale.

Le credenziali sono impostazioni sincrone, ovvero vengono applicate al profilo la prima volta che si accede al computer dopo la sincronizzazione di UE-V.

La sincronizzazione delle credenziali è gestita dal modello di posizione delle impostazioni, che è disabilitato per impostazione predefinita. Puoi abilitare o disabilitare questo modello con gli stessi metodi usati per altri modelli. L'identificatore di modello per questa caratteristica è RoamingCredentialSettings.

**Importante**  
Se si usano le credenziali di Active Directory in roaming nell'ambiente, è consigliabile non abilitare il modello di credenziali comuni UE-V.



Usare uno di questi metodi per abilitare la sincronizzazione delle credenziali:

-   Centro impostazioni società

-   PowerShell

-   Criteri di gruppo

**Nota**  
Le credenziali vengono crittografate durante la sincronizzazione.



[Centro impostazioni società](https://technet.microsoft.com/library/dn458903.aspx)**:** Selezionare la casella di controllo impostazioni credenziali comuni in impostazioni di Windows per abilitare la sincronizzazione delle credenziali. Deselezionare la casella di controllo per disattivarla. Questa casella di controllo viene visualizzata solo nel centro impostazioni società se l'account non è configurato per la sincronizzazione delle impostazioni con un account Microsoft.

[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** questo cmdlet di PowerShell consente la sincronizzazione delle credenziali:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Questo cmdlet di PowerShell Disabilita la sincronizzazione delle credenziali:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)**:** è necessario [distribuire il modello ADMX più recente di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) per abilitare la sincronizzazione delle credenziali tramite criteri di gruppo. La sincronizzazione delle credenziali viene gestita con le impostazioni di Windows. Per gestire questa caratteristica con criteri di gruppo, abilitare la sincronizzazione dei criteri delle impostazioni di Windows.

1.  Aprire Editor criteri di gruppo e passare a **Configurazione utente-modelli amministrativi-Componenti di Windows-virtualizzazione dell'esperienza utente Microsoft**.

2.  Fare doppio clic su **Sincronizza impostazioni di Windows**.

3.  Se questo criterio è abilitato, è possibile abilitare la sincronizzazione delle credenziali controllando la casella di controllo **credenziali mobili** o disabilitare la sincronizzazione delle credenziali deselezionando.

4.  Fai clic su **OK**.

### Percorsi delle credenziali sincronizzati da UE-V

I file di credenziali salvati dalle applicazioni nei percorsi seguenti vengono sincronizzati:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

Le credenziali salvate in altre posizioni non vengono sincronizzate da UE-V.

### <a href="" id="appxsettings"></a>Sincronizzazione delle impostazioni dell'app Windows

UE-V gestisce la sincronizzazione delle impostazioni delle app di Windows in tre modi:

-   **Sincronizzare le app di Windows:** Consentire o negare qualsiasi sincronizzazione delle app di Windows

-   **Elenco delle app di Windows:** Sincronizzare un elenco di app di Windows

-   **Comportamento di sincronizzazione predefinito non elenco:** Determinare il comportamento di sincronizzazione delle app di Windows non presenti nell'elenco delle app di Windows.

Per altre informazioni, Vedi l' [elenco delle app di Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

### <a href="" id="custom"></a>Modelli di posizione delle impostazioni UE-V personalizzati

Se si sta distribuendo UE-V per sincronizzare le impostazioni per le applicazioni personalizzate, si utilizzerà il generatore UE-V per creare modelli di posizione personalizzati per le applicazioni desktop. Dopo aver creato e testato un modello di posizione delle impostazioni personalizzato in un ambiente di test, è possibile distribuire i modelli di posizione delle impostazioni ai computer nell'organizzazione.

I modelli di posizione delle impostazioni personalizzate devono essere distribuiti con un'infrastruttura di distribuzione esistente, ad esempio un metodo ESD (Enterprise Software Distribution), come System Center Configuration Manager, con preferenze o configurando un catalogo di modelli di impostazioni UE-V. I modelli distribuiti con Configuration Manager o criteri di gruppo devono essere registrati usando WMI-V di UE o Windows PowerShell.

Per altre informazioni sui modelli di posizione delle impostazioni personalizzate, vedere [distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Per altre informazioni sull'uso di UE-V con Configuration Manager, vedere [configurazione di UE-v 2. x con System Center Configuration manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a href="" id="prevent"></a>Impedire la configurazione delle impostazioni utente non intenzionale

UE-V Scarica le nuove informazioni sulle impostazioni utente da una posizione di archiviazione delle impostazioni e applica le impostazioni al computer locale in queste istanze:

-   Ogni volta che viene avviata un'applicazione con un modello UE-V registrato.

-   Quando un utente accede a un computer.

-   Quando un utente sblocca un computer.

-   Quando viene effettuata una connessione a un computer desktop remoto in cui è installata la versione UE-V.

-   Quando viene eseguita l'attività programmata del controller di sincronizzazione.

Se UE-V è installato nel computer A e nel computer B e le impostazioni desiderate per l'applicazione si trovano nel computer A, il computer A dovrebbe aprire e chiudere prima l'applicazione. Se l'applicazione viene aperta e chiusa nel computer B, le impostazioni dell'applicazione nel computer A sono configurate per le impostazioni dell'applicazione nel computer B. le impostazioni vengono sincronizzate tra i computer per ogni singola applicazione. Nel tempo le impostazioni diventano coerenti tra i computer quando vengono aperte e chiuse con le impostazioni preferite.

Questo scenario si applica anche alle impostazioni di Windows. Se le impostazioni di Windows nel computer B devono essere le stesse delle impostazioni di Windows nel computer A, l'utente deve eseguire l'accesso e disconnettersi il computer per primo.

Se le impostazioni utente desiderate dall'utente vengono applicate nell'ordine errato, possono essere recuperate eseguendo un'operazione di ripristino per l'applicazione specifica o la configurazione di Windows nel computer in cui sono state sovrascritte le impostazioni. Per altre informazioni, vedere [gestire il backup e il ripristino amministrativi in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a href="" id="capacity"></a>Pianificazione delle prestazioni e della capacità

Specificare i requisiti per UE-V con capacità disco standard e monitoraggio dell'integrità della rete.

UE-V usa una condivisione SMB (Server Message Block) per l'archiviazione dei pacchetti di impostazioni. La dimensione dei pacchetti di impostazioni varia in base alle informazioni sulle impostazioni per ogni applicazione. Mentre la maggior parte dei pacchetti di impostazioni è di piccole dimensioni, la sincronizzazione di file potenzialmente di grandi dimensioni, ad esempio immagini desktop, può causare scarse prestazioni, in particolare sulle reti più lente.

Per ridurre i problemi relativi alla latenza della rete, creare posizioni di archiviazione delle impostazioni nelle stesse reti locali in cui risiedono i computer degli utenti. È consigliabile 20 MB di spazio su disco per ogni utente per la posizione di archiviazione delle impostazioni.

Per impostazione predefinita, la sincronizzazione UE-V viene riattivata dopo 2 secondi per evitare eccessivi ritardi dovuti a un pacchetto di impostazioni di grandi dimensioni. Puoi configurare l'impostazione SyncMethod = SyncProvider usando [gli oggetti Criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx).

### <a href="" id="high"></a>Disponibilità elevata per UE-V

Il catalogo della posizione e del modello di impostazioni di archiviazione delle impostazioni UE-V supporta l'archiviazione dei dati degli utenti in qualsiasi condivisione modificabile. Per garantire una disponibilità elevata, seguire questi criteri:

-   Formattare il volume di archiviazione con un file system NTFS.

-   La condivisione può usare il file System distribuito (DFS), ma esistono restrizioni.
In particolare, è supportata la replica di file System Distributed (DFS-R), con o senza uno spazio dei nomi di file System distribuito (DFS-N).
Analogamente, è supportata solo la configurazione di una singola destinazione con DFS-N.
Per informazioni dettagliate, vedere [l'istruzione del supporto Microsoft intorno ai dati di profilo utente replicati](https://go.microsoft.com/fwlink/p/?LinkId=313991) e anche [informazioni sui criteri di supporto Microsoft per uno scenario di distribuzione DFS-R e DFS-N](https://support.microsoft.com/kb/2533009).

    Inoltre, poiché SYSVOL USA DFS-R per la replica, non è possibile usare SYSVOL per la replica di file di dati UE-V.

-   Configurare le autorizzazioni di condivisione e gli elenchi di controllo di accesso (ACL) NTFS specificati in [distribuzione della posizione di archiviazione delle impostazioni per UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Usa il clustering di file server insieme all'agente UE-V per consentire l'accesso alle copie dei dati sullo stato dell'utente in caso di errori di comunicazione.

-   È possibile archiviare i dati del percorso di archiviazione delle impostazioni (dati utente) e modelli di catalogo delle impostazioni in condivisioni in cluster, in condivisioni DFS-N o in entrambe.

### <a href="" id="clocksync"></a>Sincronizzare gli orologi del computer per la sincronizzazione delle impostazioni UE-V

I computer che eseguono l'agente UE-V devono usare un server temporale per mantenere un'esperienza di impostazioni coerente. UE-V usa i timestamp per determinare se le impostazioni devono essere sincronizzate dalla posizione di archiviazione delle impostazioni. Se l'orologio del computer non è accurato, le impostazioni precedenti possono sovrascrivere le impostazioni più recenti o le nuove impostazioni potrebbero non essere salvate nella posizione di archiviazione delle impostazioni.

## <a href="" id="prereqs"></a>Confermare i prerequisiti e le configurazioni supportate per la versione UE-V


Prima di procedere, verificare che l'ambiente contenga questi requisiti per l'uso di UE-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Sistema operativo</strong></th>
<th align="left"><strong>Edizione</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Architettura di sistema</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate, Enterprise o Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5 o versione successiva per la versione UE-V 2,1.</p>
<p>.NET Framework 4 o versione successiva per la versione UE-V 2,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o server Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5 o versione successiva per la versione UE-V 2,1.</p>
<p>.NET Framework 4 o versione successiva per la versione UE-V 2,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 e Windows 8,1</p></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5 o versione successiva</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, versione pre-1607</p>
<div class="alert">
<strong>Nota</strong><br/><p>Solo UE-V 2,1 SP1 supporta Windows 10, versione pre-1607</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 e Windows Server 2012 R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,5 o versione successiva</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3,0 o versioni successive</p></td>
<td align="left"><p>.NET Framework 4,6 o versione successiva</p></td>
</tr>
</tbody>
</table>



Inoltre...

-   **Licenza MDOP:** Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP). I clienti aziendali possono ottenere MDOP con Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere come si ottiene MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenziali amministrative** per qualsiasi computer in cui verrà installato

**Nota**  

-   A partire da WIndows 10, versione 1607, UE-V è incluso in [Windows 10 per le aziende](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e non fa più parte del Microsoft Desktop Optimization Pack.

-   La caratteristica UE-V Windows PowerShell dell'agente UE-V richiede .NET Framework 4 o versione successiva e Windows PowerShell 3,0 o versioni successive per essere abilitate. Scaricare Windows PowerShell 3,0 [qui](https://go.microsoft.com/fwlink/?LinkId=309609).

-   Installare .NET Framework 4 o .NET Framework 4,5 nei computer che eseguono Windows 7 o il sistema operativo Windows Server 2008 R2. I sistemi operativi Windows 8, Windows 8,1 e Windows Server 2012 sono installati in .NET Framework 4,5. Il sistema operativo Windows 10 include .NET Framework 4,6 installato.
-   Il criterio "Elimina cache roaming" per i profili obbligatori non è supportato con UE-V e non deve essere usato.



Non sono previsti particolari requisiti RAM (Random Access Memory) specifici di UE-V.

### Sincronizzazione delle impostazioni tramite il provider di sincronizzazione

Il provider di sincronizzazione è l'impostazione predefinita per gli utenti, che sincronizza una cache locale con la posizione di archiviazione delle impostazioni in queste istanze:

-   Accesso/fine sessione

-   Bloccare/sbloccare

-   Connessione/disconnessione desktop remoto

-   Apertura/chiusura dell'applicazione

Un'attività pianificata gestisce questa sincronizzazione delle impostazioni ogni 30 minuti o tramite determinati eventi trigger per alcune applicazioni. Per altre informazioni, vedere [modifica della frequenza delle attività pianificate di UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

L'agente UE-V consente di sincronizzare le impostazioni utente per i computer che non sono sempre connessi alla rete aziendale (computer remoti e laptop) e computer sempre connessi alla rete (computer che eseguono Windows Server e ospitano sessioni di Virtual Desktop Interface (VDI)).

**Sincronizzazione per i computer con connessioni sempre disponibili:** Quando si usa UE-V in computer sempre connessi alla rete, è necessario configurare l'agente UE-V per sincronizzare le impostazioni usando il parametro *SyncMethod = None* , che tratta il server di archiviazione delle impostazioni come condivisione di rete standard. In questa configurazione, l'agente UE-V può essere configurato per segnalare se l'importazione delle impostazioni dell'applicazione è ritardata.

Abilitare questa configurazione tramite uno di questi metodi:

-   Durante l'installazione di UE-V, al prompt dei comandi o in un file batch, imposta il parametro AgentSetup.exe *SyncMethod = None*. [La distribuzione dell'agente UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) fornisce ulteriori informazioni.

-   Dopo l'installazione di UE-V, usare la caratteristica di gestione delle impostazioni in System Center 2012 Configuration Manager o i modelli ADMX di MDOP per spingere la configurazione *SyncMethod = None* .

-   Usare Windows PowerShell o Strumentazione gestione Windows (WMI) per impostare la configurazione *SyncMethod = None* .

    **Nota**  
    Questi ultimi due metodi non funzionano per gli ambienti VDI (Virtual Desktop Infrastructure) in pool.



È necessario riavviare il computer prima che le impostazioni inizino a essere sincronizzate.

**Nota**  
Se si imposta *SyncMethod = None*, le eventuali modifiche apportate alle impostazioni vengono salvate direttamente nel server. Se la connessione di rete al percorso di archiviazione delle impostazioni non viene trovata, le modifiche apportate alle impostazioni vengono memorizzate nella cache del dispositivo e vengono sincronizzate alla successiva esecuzione del provider di sincronizzazione. Se il percorso di archiviazione delle impostazioni non viene trovato e il profilo utente viene rimosso da un ambiente VDI in pool durante la disconnessione, le modifiche alle impostazioni vengono perse e l'utente deve riapplicare la modifica quando il computer viene riconnesso al percorso di archiviazione delle impostazioni.



**Sincronizzazione per motori di sincronizzazione esterni:** Il parametro *SyncMethod = External* specifica che se le impostazioni di UE-V vengono scritte in una cartella locale nel computer utente, qualsiasi motore di sincronizzazione esterno, ad esempio OneDrive for business, work Folders, SharePoint o Dropbox, può essere usato per applicare queste impostazioni ai diversi computer a cui gli utenti accedono.

**Supporto per le sessioni VDI condivise:** UE-V 2,1 e 2,1 SP1 consentono di supportare le sessioni VDI condivise tra gli utenti finali. È possibile registrare e configurare uno speciale modello VDI, garantendo che UE-V mantenga intatte tutte le sue funzionalità per le sessioni VDI non persistenti.

**Nota**  
Se non si Abilita la modalità VDI per le sessioni VDI non persistenti, alcune caratteristiche non funzionano, ad esempio [backup/ripristino e ultimo bene noto (LKG)](https://technet.microsoft.com/library/dn878331.aspx).



Il modello VDI è provvisto di UE-V 2,1 e 2,1 SP1 ed è in genere disponibile qui dopo l'installazione: C:\\Programmi \\Programmi\\microsoft User Experience Virtualization\\Templates\\VdiState.xml

### Prerequisiti per il supporto del generatore di UE-V

Installare il generatore UE-V nel computer usato per creare modelli di posizione delle impostazioni personalizzate. Questo computer dovrebbe essere in grado di eseguire le applicazioni le cui impostazioni sono sincronizzate. È necessario essere un membro del gruppo Administrators nel computer in cui è in esecuzione il software Generator UE-V.

Il generatore UE-V deve essere installato in un computer che usa un file system NTFS. Il software Generator UE-V richiede .NET Framework 4. Per altre informazioni, vedere [distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## Altre risorse per questo prodotto


-   [Microsoft User Experience Virtualization (UE-V) 2. x](index.md)

-   [Introduzione a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Risoluzione dei problemi relativi a UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














