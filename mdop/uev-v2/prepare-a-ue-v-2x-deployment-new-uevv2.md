---
title: Preparare una UE-V 2.x
description: Preparare una UE-V 2.x
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
ms.openlocfilehash: 3e4d4b69975deda473372345733d8e8593a4775d
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910531"
---
# <a name="prepare-a-ue-v-2x-deployment"></a>Preparare una UE-V 2.x


Prima di distribuire Microsoft User Experience Virtualization (UE-V) 2.0 o 2.1 come soluzione per la sincronizzazione delle impostazioni tra dispositivi a cui gli utenti accedono nell'organizzazione, è necessario eseguire alcune operazioni di pianificazione e preparazione. Questo argomento consente di determinare il tipo di distribuzione da eseguire e la preparazione che è possibile eseguire in precedenza in modo che la distribuzione venga eseguita correttamente.

Prima di tutto, esamini le attività che dovrai eseguire per distribuire UE-V:

-   Pianificare la distribuzione UE-V distribuzione

    Prima di distribuire qualsiasi elemento, un buon primo passaggio consiste nell'eseguire un po' di pianificazione in modo da poter determinare UE-V funzionalità da distribuire. Pertanto, se si esce da questa pagina, assicurarsi di tornare a leggere le informazioni sulla pianificazione riportate di seguito.

-   [Distribuire le funzionalità necessarie per UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Ogni UE-V di distribuzione richiede queste attività:

    -   [Definire un percorso di archiviazione delle impostazioni](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Decidere come distribuire l'agente UE-V e gestire le UE-V predefinite](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Installare l'UE-V in](https://technet.microsoft.com/library/dn458891.aspx#agent) ogni computer utente che necessita di impostazioni sincronizzate

-   Facoltativamente, è possibile [distribuire UE-V 2.x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    La pianificazione consente di stabilire se si desidera che UE-V supporti la sincronizzazione delle impostazioni per le applicazioni personalizzate (di terze parti o line-of-business), che richiedono queste funzionalità di UE-V:

    -   [Installare il generatore UEV in](https://technet.microsoft.com/library/dn458942.aspx#uevgen) modo da poter creare, modificare e convalidare i modelli di percorso delle impostazioni personalizzate necessari per sincronizzare le impostazioni personalizzate dell'applicazione

    -   [Creare modelli di percorso delle](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) impostazioni personalizzate tramite il generatore UE-V personalizzato

    -   [Distribuire un UE-V di modelli di](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) impostazioni personalizzate da usare per archiviare i modelli di percorso delle impostazioni personalizzate

Questo diagramma del flusso di lavoro offre una conoscenza di alto livello di una distribuzione UE-V e delle decisioni che determinano la modalità di UE-V nell'organizzazione.

![deploymentworkflow.](images/deploymentworkflow.png)

**Pianificazione di una UE-V distribuzione:** Prima di tutto, si desidera eseguire un po' di pianificazione in modo da poter determinare UE-V componenti da distribuire. La pianificazione di UE-V una distribuzione implica le operazioni seguenti:

-   [Decidere se sincronizzare le impostazioni per le applicazioni personalizzate](#deciding)

    Questo determina se verrà installato il generatore di UE-V durante la distribuzione, che consente di creare modelli di percorso delle impostazioni personalizzate. Implica quanto segue:

    Esaminare le [impostazioni sincronizzate automaticamente in una UE-V distribuzione](#autosyncsettings).

    [Determinare se sono necessarie impostazioni sincronizzate per altre applicazioni](#determinesettingssync).

-   Esaminare [altre considerazioni per la distribuzione di UE-V](#considerations), ad esempio la pianificazione della disponibilità elevata e della capacità.

-   [Verificare i prerequisiti e le configurazioni supportate per UE-V](#prereqs)

## <a name="decide-whether-to-synchronize-settings-for-custom-applications"></a><a href="" id="deciding"></a>Decidere se sincronizzare Impostazioni applicazioni personalizzate


In una UE-V, molte impostazioni vengono sincronizzate automaticamente. Tuttavia, puoi anche personalizzare UE-V per sincronizzare le impostazioni per altre applicazioni, ad esempio le app line-of-business e di terze parti.

Decidere se si desidera UE-V le impostazioni per le applicazioni personalizzate è probabilmente la parte più importante della pianificazione della UE-V distribuzione. Gli argomenti di questa sezione ti aiuteranno a prendere questa decisione.

### <a name="settings-that-are-automatically-synchronized-in-a-ue-v-deployment"></a><a href="" id="autosyncsettings"></a>Impostazioni sincronizzati automaticamente in una UE-V distribuzione

In questa sezione vengono fornite informazioni sulle impostazioni sincronizzate per impostazione predefinita in UE-V, tra cui:

Applicazioni desktop le cui impostazioni sono sincronizzate per impostazione predefinita

Windows desktop sincronizzate per impostazione predefinita

Dichiarazione di supporto per la sincronizzazione Windows'impostazione dell'app

Per scaricare un elenco completo delle impostazioni specifiche di Microsoft Office 2013, Microsoft Office 2010 e Microsoft Office 2007 sincronizzate da UE-V, vedere [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.

### <a name="desktop-applications-synchronized-by-default-in-ue-v-21-and-ue-v-21-sp1"></a>Applicazioni desktop sincronizzate per impostazione predefinita in UE-V 2.1 e UE-V 2.1 SP1

Quando si installa l'UE-V 2.1 o 2.1 SP1 Agent, viene registrato un gruppo predefinito di modelli di percorso delle impostazioni che acquisiscono i valori delle impostazioni per queste applicazioni Microsoft comuni.

**Suggerimento**  
**Microsoft Office 2007 Impostazioni Synchronization** : in UE-V 2.1 e 2.1 SP1, un modello di percorso delle impostazioni non è più incluso per impostazione predefinita per le applicazioni Office 2007. Tuttavia, è comunque possibile utilizzare i modelli Office 2007 di UE-V 2.0 o versioni precedenti ed è possibile ottenere i modelli dalla raccolta modelli [UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589).



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
<td align="left"><p>Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scarica un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
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
<td align="left"><p>Microsoft Office 2013</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scarica un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
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
<p>I modelli UE-V 2.1 e 2.1 SP1 Microsoft Office 2013 includono un supporto migliorato Outlook firme. È stata aggiunta la sincronizzazione delle impostazioni di firma predefinite per i messaggi di posta elettronica nuovi, di risposta e inoltrati.</p>
<div class="alert">
<strong>Nota</strong><br/><p>È Outlook deve essere creato un profilo per qualsiasi dispositivo in cui un utente desidera sincronizzare la propria Outlook firma. Se il profilo non è già stato creato, l'utente può crearne uno e quindi riavviare Outlook sul dispositivo per abilitare la sincronizzazione delle firme.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Opzioni del browser: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</p></td>
<td align="left"><p>Preferiti, home page, schede e barre degli strumenti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>UE-V non esegue il roaming delle impostazioni per i cookie di Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows accessori</p></td>
<td align="left"><p>Calcolatrice Microsoft, Blocco note, WordPad.</p></td>
</tr>
</tbody>
</table>



**Nota**  
UE-V 2.1 SP1 non sincronizza le impostazioni tra il Calcolatrice Microsoft in Windows 10 e Calcolatrice Microsoft nei sistemi operativi precedenti.



### <a name="desktop-applications-synchronized-by-default-in-ue-v-20"></a>Applicazioni desktop sincronizzate per impostazione predefinita in UE-V 2.0

Quando si installa l'UE-V 2.0 Agent, viene registrato un gruppo predefinito di modelli di percorso delle impostazioni che acquisiscono i valori delle impostazioni per queste applicazioni Microsoft comuni.

**Suggerimento**  
**Microsoft Office 2013 Impostazioni Synchronization** : in UE-V 2.0, un modello di percorso delle impostazioni non è incluso per impostazione predefinita per le applicazioni di Office 2013, ma è disponibile per il download dalla raccolta [modelli di UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589). [La sincronizzazione Office 2013 con UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) fornisce informazioni dettagliate sui modelli supportati per la sincronizzazione Office 2013.



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
<td align="left"><p>Microsoft Office 2007</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scarica un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
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
<td align="left"><p>Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Scarica un elenco di tutte le impostazioni sincronizzate </a> )</p></td>
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
<td align="left"><p>Preferiti, home page, schede e barre degli strumenti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>UE-V non esegue il roaming delle impostazioni per i cookie di Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows accessori</p></td>
<td align="left"><p>Calcolatrice Microsoft, Blocco note, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a name="windows-settings-synchronized-by-default"></a><a href="" id="autosyncsettings2"></a>Windows sincronizzate per impostazione predefinita

UE-V include modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per Windows impostazioni.

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
<th align="left">Applica su</th>
<th align="left">Esportare il</th>
<th align="left">Stato predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sfondo del desktop</p></td>
<td align="left"><p>Sfondo o sfondo del desktop attualmente attivo.</p></td>
<td align="left"><p>Accesso, sblocco, connessione remota, eventi attività pianificate.</p></td>
<td align="left"><p>Disconnessione, blocco, disconnessione remota, clic utente su Sincronizza ora in Centro Impostazioni <strong> aziendale o intervallo attività </strong> pianificato</p></td>
<td align="left"><p>Abilitato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accessibilità</p></td>
<td align="left"><p>Impostazioni di accessibilità e input, Microsoft Lente di ingrandimento, Assistente vocale e tastiera su schermo.</p></td>
<td align="left"><p>Solo accesso.</p></td>
<td align="left"><p>Disconnessione, utente che fa <strong> clic su Sincronizza ora nel Centro Impostazioni aziendale o intervallo attività </strong> pianificate</p></td>
<td align="left"><p>Abilitato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostazioni desktop</p></td>
<td align="left"><p>menu Start e della barra delle applicazioni, Opzioni cartella, Icone predefinite del desktop, Orologi aggiuntivi e Impostazioni paese e lingua.</p></td>
<td align="left"><p>Solo accesso.</p></td>
<td align="left"><p>Disconnessione, utente che fa <strong> clic su Sincronizza ora nel Centro Impostazioni aziendale o attività </strong> pianificata</p></td>
<td align="left"><p>Abilitato</p></td>
</tr>
</tbody>
</table>



**Nota**  
A partire Windows 8, UE-V non esegue il roaming delle impostazioni relative alla schermata Start, ad esempio elementi e posizioni. Inoltre, UE-V non supporta la sincronizzazione degli elementi della barra delle applicazioni aggiunti o dei collegamenti Windows file.



**Importante**  
UE-V 2.1 SP1 roaming delle impostazioni della barra delle applicazioni tra Windows 10 dispositivi. Tuttavia, UE-V non sincronizza le impostazioni della barra delle applicazioni tra Windows 10 dispositivi e dispositivi che eseguono sistemi operativi precedenti.



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
<th align="left">Acquisizione</th>
<th align="left">Applica</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Applicazione Impostazioni</strong></p></td>
<td align="left"><p>App di Windows  </p></td>
<td align="left"><p>Chiudere l'app</p>
<p>Windows evento di modifica delle impostazioni dell'app</p></td>
<td align="left"><p>Avviare il monitoraggio UE-V app all'avvio</p>
<p>Apri app</p>
<p>Windows Evento di Impostazioni app</p>
<p>Arrivo di un pacchetto di impostazioni</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Applicazioni desktop</p></td>
<td align="left"><p>L'applicazione viene chiusa</p></td>
<td align="left"><p>L'applicazione viene aperta e chiusa</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Impostazioni desktop</strong></p></td>
<td align="left"><p>Sfondo del desktop</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso, sblocco, connessione remota, notifica dell'arrivo di un nuovo pacchetto, clic su Sincronizza ora nel Centro Impostazioni aziendale o esecuzione <strong> </strong> di attività pianificate.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Accessibilità (comune- Accessibilità, Assistente vocale, Lente di ingrandimento, Tastiera su schermo)</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Accessibilità (Shell - Audio, Accessibilità, Tastiera, Mouse)</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso, sblocco, connessione remota, notifica dell'arrivo di un nuovo pacchetto, clic su Sincronizza ora nel Centro Impostazioni aziendale o esecuzione <strong> </strong> di attività pianificate</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Impostazioni desktop</p></td>
<td align="left"><p>Blocco o disconnessione</p></td>
<td align="left"><p>Accesso</p></td>
</tr>
</tbody>
</table>



### <a name="ue-v-support-for-windows-apps"></a>UE-V supporto per Windows app

Per Windows app, lo sviluppatore dell'app specifica le impostazioni sincronizzate. Puoi specificare quali app Windows abilitate per la sincronizzazione delle impostazioni.

Per visualizzare un elenco di app Windows che possono sincronizzare le impostazioni in un computer con il nome della famiglia di pacchetti, lo stato abilitato e l'origine abilitata, al prompt dei comandi di Windows PowerShell immettere: `Get-UevAppxPackage`

**Nota**  
A Windows 8, UE-V non sincronizza le impostazioni dell'app Windows se l'utente di dominio collega le credenziali di accesso all'account Microsoft. Questo collegamento sincronizza le impostazioni con Microsoft OneDrive in modo UE-V, che disabilita la sincronizzazione delle impostazioni Windows'app.



### <a name="ue-v-support-for-roaming-printers"></a>UE-V supporto per stampanti mobili

UE-V 2.1 SP1 consente alle stampanti di rete di eseguire il roaming tra dispositivi in modo che un utente abbia accesso alle proprie stampanti di rete quando è connesso a qualsiasi dispositivo in rete. Ciò include il roaming della stampante impostata come predefinita.

Il roaming delle stampanti UE-V uno di questi scenari:

-   Il server di stampa può scaricare il driver necessario durante il roaming in un nuovo dispositivo.

-   Il driver per la stampante di rete mobile è preinstallato in qualsiasi dispositivo che deve accedere a tale stampante di rete.

-   Il driver della stampante può essere ottenuto da Windows Update.

**Nota**  
La UE-V roaming della stampante non **esegue** il roaming delle impostazioni o delle preferenze della stampante, ad esempio la stampa fronte retro.



### <a name="determine-whether-you-need-settings-synchronized-for-other-applications"></a><a href="" id="determinesettingssync"></a>Determinare se sono necessarie impostazioni sincronizzate per altre applicazioni

Dopo aver esaminato le impostazioni sincronizzate automaticamente in una distribuzione di UE-V, è necessario decidere se sincronizzare le impostazioni per altre applicazioni in quanto ciò determina la modalità di distribuzione di UE-V in tutta l'organizzazione.

In quanto amministratore, quando si valutano le applicazioni desktop da includere nella soluzione UE-V, considerare quali impostazioni possono essere personalizzate dagli utenti e come e dove l'applicazione archivia le impostazioni. Non tutte le applicazioni desktop dispongono di impostazioni che possono essere personalizzate o personalizzate di routine dagli utenti. Inoltre, non tutte le impostazioni delle applicazioni desktop possono essere sincronizzate in modo sicuro in più computer o ambienti.

In generale, è possibile sincronizzare le impostazioni che soddisfano i criteri seguenti:

-   Impostazioni archiviati in posizioni accessibili dall'utente. Ad esempio, non sincronizzare le impostazioni archiviate in System32 o all'esterno della sezione HKEY\_CURRENT\_USER (HKCU) del Registro di sistema.

-   Impostazioni che non sono specifiche del computer specifico. Ad esempio, escludere le configurazioni hardware o di rete.

-   Impostazioni che possono essere sincronizzati tra computer senza rischio di dati danneggiati. Ad esempio, non utilizzare le impostazioni archiviate in un file di database.

### <a name="checklist-for-evaluating-custom-applications"></a><a href="" id="checklistsettingssync"></a>Elenco di controllo per la valutazione delle applicazioni personalizzate

Se si è deciso di sincronizzare le impostazioni per altre applicazioni, è possibile utilizzare questo elenco di controllo per determinare quali applicazioni includere.

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
<td align="left"><p>Questa applicazione contiene impostazioni che l'utente può personalizzare?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>È importante per l'utente che queste impostazioni siano sincronizzate?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Queste impostazioni utente sono già gestite da una soluzione di criteri per la gestione o le impostazioni delle applicazioni? UE-V le impostazioni dell'applicazione all'avvio dell'applicazione e Windows eventi di accesso, sblocco o connessione remota. Se si utilizza un UE-V con altre soluzioni di condivisione delle impostazioni, gli utenti potrebbero verificarsi incoerenza tra le impostazioni sincronizzate.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Le impostazioni dell'applicazione sono specifiche del computer? Le preferenze e le personalizzazioni delle applicazioni associate all'hardware o a configurazioni di computer specifiche non vengono sincronizzate in modo coerente tra le sessioni e possono causare un'esperienza di applicazione scarsa.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L'applicazione archivia le impostazioni nella directory Programmi o nella directory dei file che si trova nella <strong> directory Utenti </strong> [nome utente] appData forte &lt; &gt; </strong> &lt; &gt; </strong> LocalLow? I dati dell'applicazione archiviati in una di queste posizioni in genere non devono essere sincronizzati con l'utente, perché questi dati sono specifici del computer o perché i dati sono troppo grandi per la sincronizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L'applicazione archivia le impostazioni in un file contenente altri dati dell'applicazione che non devono essere sincronizzati? UE-V i file vengono sincronizzati come una singola unità. Se le impostazioni vengono archiviate in file che includono dati dell'applicazione diversi da impostazioni, la sincronizzazione di questi dati aggiuntivi può causare un'esperienza di applicazione scarsa.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Quanto sono grandi i file che contengono le impostazioni? Le prestazioni della sincronizzazione delle impostazioni possono essere influenzate da file di grandi dimensioni. L'inclusione di file di grandi dimensioni può influire sulle prestazioni della sincronizzazione delle impostazioni.</p></td>
</tr>
</tbody>
</table>



## <a name="other-considerations-when-preparing-a-ue-v-deployment"></a><a href="" id="considerations"></a>Altre considerazioni sulla preparazione di una UE-V distribuzione


È inoltre consigliabile tenere in considerazione questi aspetti quando si prepara la distribuzione UE-V:

-   [Gestione della sincronizzazione delle credenziali](#creds)

-   [Windows sincronizzazione delle impostazioni dell'app](#appxsettings)

-   [Modelli di percorso UE-V impostazioni personalizzate](#custom)

-   [Configurazioni non intenzionali delle impostazioni utente](#prevent)

-   [Prestazioni e capacità](#capacity)

-   [Disponibilità elevata](#high)

-   [Sincronizzazione orologio computer](#clocksync)

### <a name="managing-credentials-synchronization-in-ue-v-21-and-ue-v-21-sp1"></a><a href="" id="creds"></a>Gestione della sincronizzazione delle credenziali in UE-V 2.1 e UE-V 2.1 SP1

Molte applicazioni aziendali, tra cui Microsoft Outlook e Lync, richiede agli utenti le credenziali di dominio all'accesso. Gli utenti hanno la possibilità di salvare le credenziali su disco per evitare di doverle immettere ogni volta che aprono queste applicazioni. L'abilitazione della sincronizzazione delle credenziali mobili consente agli utenti di salvare le credenziali in un computer ed evitare di immetterle nuovamente in ogni computer utilizzato nel proprio ambiente. Gli utenti possono sincronizzare alcune credenziali di dominio con UE-V 2.1 e 2.1 SP1.

**Importante**  
La sincronizzazione delle credenziali è disabilitata per impostazione predefinita. Per implementare questa funzionalità, è necessario abilitare esplicitamente la sincronizzazione delle credenziali durante la distribuzione.



UE-V 2.1 e 2.1 SP1 possono sincronizzare le credenziali aziendali, ma non eseguire il roaming delle credenziali destinate solo all'utilizzo nel computer locale.

Le credenziali sono impostazioni sincrone, ovvero vengono applicate al profilo al primo accesso al computer dopo UE-V sincronizzazione.

La sincronizzazione delle credenziali è gestita dal proprio modello di percorso delle impostazioni, disabilitato per impostazione predefinita. È possibile abilitare o disabilitare questo modello tramite gli stessi metodi utilizzati per altri modelli. L'identificatore del modello per questa funzionalità è RoamingCredentialSettings.

**Importante**  
Se si utilizza Il roaming delle credenziali di Active Directory nell'ambiente, è consigliabile non abilitare il modello UE-V roaming delle credenziali.



Utilizzare uno di questi metodi per abilitare la sincronizzazione delle credenziali:

-   Company Impostazioni Center

-   PowerShell

-   Criteri di gruppo

**Nota**  
Le credenziali vengono crittografate durante la sincronizzazione.



[Company Impostazioni Center](https://technet.microsoft.com/library/dn458903.aspx)**: selezionare** la casella di controllo Roaming Credential Impostazioni in Windows Impostazioni per abilitare la sincronizzazione delle credenziali. Deseleziona la casella per disabilitarla. Questa casella di controllo viene visualizzata solo in Company Impostazioni Center se l'account non è configurato per sincronizzare le impostazioni con un account Microsoft.

[PowerShell:](https://technet.microsoft.com/library/dn458937.aspx)**questo** cmdlet di PowerShell consente la sincronizzazione delle credenziali:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Questo cmdlet di PowerShell disabilita la sincronizzazione delle credenziali:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Criteri di gruppo:](https://technet.microsoft.com/library/dn458893.aspx)**è** necessario distribuire il modello [ADMX MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) più recente per abilitare la sincronizzazione delle credenziali tramite Criteri di gruppo. La sincronizzazione delle credenziali viene gestita con le Windows predefinite. Per gestire questa funzionalità con Criteri di gruppo, abilitare il criterio Sincronizza Windows impostazioni.

1.  Aprire Editor Criteri di gruppo e passare a **Configurazione utente – Modelli amministrativi – Windows componenti – Microsoft User Experience Virtualization**.

2.  Fare doppio clic su **Sincronizza Windows impostazioni**.

3.  Se questo criterio è abilitato, è possibile **** abilitare la sincronizzazione delle credenziali selezionando la casella di controllo Credenziali mobili o disabilitare la sincronizzazione delle credenziali deselezionando l'opzione.

4.  Fai clic su **OK**.

### <a name="credential-locations-synchronized-by-ue-v"></a>Percorsi delle credenziali sincronizzati da UE-V

I file delle credenziali salvati dalle applicazioni nei percorsi seguenti vengono sincronizzati:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

Le credenziali salvate in altri percorsi non vengono sincronizzate da UE-V.

### <a name="windows-app-settings-synchronization"></a><a href="" id="appxsettings"></a>Windows delle impostazioni dell'app

UE-V gestisce la Windows delle impostazioni dell'app in tre modi:

-   **Sincronizza Windows app:** Consentire o negare qualsiasi sincronizzazione Windows'app

-   **Windows app:** Sincronizzare un elenco di Windows app

-   **Comportamento di sincronizzazione predefinito non in elenco:** Determinare il comportamento di sincronizzazione Windows app non presenti nell'elenco Windows app.

Per altre informazioni, vedi [l'elenco Windows app.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

### <a name="custom-ue-v-settings-location-templates"></a><a href="" id="custom"></a>Modelli di percorso UE-V impostazioni personalizzate

Se si distribuisce un UE-V per sincronizzare le impostazioni per le applicazioni personalizzate, si utilizzerà il generatore di UE-V per creare modelli di percorso delle impostazioni personalizzate per tali applicazioni desktop. Dopo aver creato e testato un modello di percorso delle impostazioni personalizzato in un ambiente di testing, è possibile distribuire i modelli di percorso delle impostazioni nei computer dell'organizzazione.

I modelli di percorso delle impostazioni personalizzate devono essere distribuiti con un'infrastruttura di distribuzione esistente, ad esempio un metodo ESD (Enterprise Software Distribution), ad esempio System Center Configuration Manager, con preferenze o configurando un catalogo di modelli di impostazioni di UE-V. I modelli distribuiti con Configuration Manager o Criteri di gruppo devono essere registrati UE-V WMI o Windows PowerShell.

Per ulteriori informazioni sui modelli di percorso delle impostazioni personalizzate, vedere [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Per ulteriori informazioni sull'UE-V con Configuration Manager, vedere [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a name="prevent-unintentional-user-settings-configuration"></a><a href="" id="prevent"></a>Impedire la configurazione involontaria delle impostazioni utente

UE-V scarica nuove informazioni sulle impostazioni utente da un percorso di archiviazione delle impostazioni e applica le impostazioni al computer locale in questi casi:

-   Ogni volta che viene avviata un'applicazione con un modello UE-V registrato.

-   Quando un utente accede a un computer.

-   Quando un utente sblocca un computer.

-   Quando viene stabilita una connessione a un computer desktop remoto UE-V installato.

-   Quando viene eseguita l'attività pianificata Dell'applicazione controller di sincronizzazione.

Se UE-V è installato nel computer A e nel computer B e le impostazioni desiderate per l'applicazione si trova nel computer A, il computer A dovrebbe aprire e chiudere prima l'applicazione. Se l'applicazione viene aperta e chiusa prima nel computer B, le impostazioni dell'applicazione nel computer A vengono configurate in base alle impostazioni dell'applicazione nel computer B. Impostazioni vengono sincronizzate tra i computer in base all'applicazione. Nel tempo, le impostazioni diventano coerenti tra i computer quando vengono aperte e chiuse con le impostazioni preferite.

Questo scenario si applica anche alle Windows predefinite. Se le Windows del computer B devono essere le stesse di Windows nel computer A, l'utente deve prima accedere e disconnettersi dal computer A.

Se le impostazioni utente che l'utente desidera applicare vengono applicate nell'ordine errato, possono essere ripristinate eseguendo un'operazione di ripristino per l'applicazione specifica o la configurazione di Windows nel computer in cui le impostazioni sono state sovrascritte. Per ulteriori informazioni, vedere [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a name="performance-and-capacity-planning"></a><a href="" id="capacity"></a>Pianificazione delle prestazioni e della capacità

Specificare i requisiti per l'UE-V con capacità del disco standard e monitoraggio dell'integrità della rete.

UE-V utilizza una condivisione SMB (Server Message Block) per l'archiviazione dei pacchetti di impostazioni. Le dimensioni dei pacchetti di impostazioni variano a seconda delle informazioni sulle impostazioni per ogni applicazione. Anche se la maggior parte dei pacchetti di impostazioni è di piccole dimensioni, la sincronizzazione di file potenzialmente di grandi dimensioni, ad esempio immagini desktop, può comportare prestazioni scarse, in particolare nelle reti più lente.

Per ridurre i problemi di latenza di rete, creare percorsi di archiviazione delle impostazioni sulle stesse reti locali in cui risiedono i computer degli utenti. È consigliabile 20 MB di spazio su disco per utente per il percorso di archiviazione delle impostazioni.

Per impostazione predefinita, UE-V timeout della sincronizzazione dopo 2 secondi per evitare un ritardo eccessivo a causa di un pacchetto di impostazioni di grandi dimensioni. È possibile configurare l'impostazione SyncMethod=SyncProvider utilizzando [Oggetti Criteri di gruppo.](https://technet.microsoft.com/library/dn458893.aspx)

### <a name="high-availability-for-ue-v"></a><a href="" id="high"></a>Disponibilità elevata per UE-V

Il UE-V di archiviazione delle impostazioni e il catalogo dei modelli di impostazioni supportano l'archiviazione dei dati utente in qualsiasi condivisione scrivibile. Per garantire la disponibilità elevata, seguire questi criteri:

-   Formattare il volume di archiviazione con un file system NTFS.

-   La condivisione può utilizzare DFS (Distributed File System), ma esistono restrizioni.
In particolare, è supportata la configurazione di destinazione singola DFS-R (Distributed File System Replication) con o senza uno spazio dei nomi del file system distribuito (DFS-N).
Analogamente, con DFS-N è supportata una sola configurazione di destinazione.
Per informazioni dettagliate, vedere La dichiarazione di supporto di [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=313991) sui dati dei profili utente replicati e informazioni sui criteri di supporto Microsoft per uno scenario di distribuzione [DFS-R e DFS-N.](https://support.microsoft.com/kb/2533009)

    Inoltre, poiché SYSVOL utilizza DFS-R per la replica, non è possibile utilizzare SYSVOL per la replica UE-V file di dati.

-   Configurare le autorizzazioni di condivisione e gli elenchi di controllo di accesso NTFS come specificato in [Deploying the Impostazioni Archiviazione Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Utilizzare il clustering di file server insieme all'UE-V agent per fornire l'accesso alle copie dei dati sullo stato utente in caso di errori di comunicazione.

-   È possibile archiviare i dati del percorso di archiviazione (dati utente) e i modelli di catalogo dei modelli di impostazioni in condivisioni cluster, in condivisioni DFS-N o in entrambi.

### <a name="synchronize-computer-clocks-for-ue-v-settings-synchronization"></a><a href="" id="clocksync"></a>Sincronizzare gli orologi del computer per UE-V sincronizzazione delle impostazioni

I computer che eseguono l UE-V agent devono utilizzare un server di tempo per mantenere un'esperienza di impostazioni coerente. UE-V usa timestamp per determinare se le impostazioni devono essere sincronizzate dal percorso di archiviazione delle impostazioni. Se l'orologio del computer non è accurato, le impostazioni precedenti possono sovrascrivere le impostazioni più recenti oppure le nuove impostazioni potrebbero non essere salvate nel percorso di archiviazione delle impostazioni.

## <a name="confirm-prerequisites-and-supported-configurations-for-ue-v"></a><a href="" id="prereqs"></a>Verificare i prerequisiti e le configurazioni supportate per UE-V


Prima di procedere, verificare che l'ambiente includa questi requisiti per l'esecuzione UE-V.

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
<td align="left"><p>Windows PowerShell 3.0 o versione successiva</p></td>
<td align="left"><p>.NET Framework 4.5 o versione successiva per UE-V 2.1.</p>
<p>.NET Framework 4 o versione successiva per UE-V 2.0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o Server Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 o versione successiva</p></td>
<td align="left"><p>.NET Framework 4.5 o versione successiva per UE-V 2.1.</p>
<p>.NET Framework 4 o versione successiva per UE-V 2.0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 e Windows 8.1</p></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 o versione successiva</p></td>
<td align="left"><p>.NET Framework 4.5 o versione successiva</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, versione precedente alla 1607</p>
<div class="alert">
<strong>Nota</strong><br/><p>Solo UE-V 2.1 SP1 supporta Windows 10 versione precedente alla 1607</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 o versione successiva</p></td>
<td align="left"><p>.NET framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 e Windows Server 2012 R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 o versione successiva</p></td>
<td align="left"><p>.NET Framework 4.5 o versione successiva</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>Windows PowerShell 3.0 o versione successiva</p></td>
<td align="left"><p>.NET Framework 4.6 o versione successiva</p></td>
</tr>
</tbody>
</table>



Inoltre...

-   **Licenza MDOP:** Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP). Enterprise clienti possono ottenere MDOP con Microsoft Software Assurance. Per ulteriori informazioni sull Microsoft Software Assurance e sull'acquisizione di MDOP, vedere How Do I Get MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenziali amministrative** per qualsiasi computer in cui verrà installato

**Nota**  

-   A partire da WIndows 10 versione 1607, UE-V è incluso in [Windows 10 per Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) e non fa più parte di Microsoft Desktop Optimization Pack.

-   La UE-V Windows PowerShell dell'agente UE-V richiede .NET Framework 4 o versione successiva e Windows PowerShell 3.0 o versione successiva per essere abilitata. Scaricare Windows PowerShell 3.0 [qui](https://go.microsoft.com/fwlink/?LinkId=309609).

-   Installare .NET Framework 4 o .NET Framework 4.5 nei computer che eseguono il sistema operativo Windows 7 o Windows Server 2008 R2. I Windows 8, Windows 8.1 e Windows Server 2012 sono .NET Framework 4.5 installati. Il Windows 10 viene fornito con .NET Framework 4.6 installato.
-   Il criterio "Elimina cache roaming" per i profili obbligatori non è supportato con UE-V e non deve essere utilizzato.



Non esistono requisiti speciali di memoria ad accesso casuale (RAM) specifici per UE-V.

### <a name="synchronization-of-settings-through-the-sync-provider"></a>Sincronizzazione di Impostazioni tramite il provider di sincronizzazione

Provider di sincronizzazione è l'impostazione predefinita per gli utenti, che sincronizza una cache locale con il percorso di archiviazione delle impostazioni in questi casi:

-   Accesso/disconnessione

-   Blocco/sblocco

-   Connessione/disconnessione desktop remoto

-   Applicazione aperta/chiusa

Un'attività pianificata gestisce questa sincronizzazione delle impostazioni ogni 30 minuti o tramite determinati eventi trigger per determinate applicazioni. Per ulteriori informazioni, vedere [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

L'agente UE-V sincronizza le impostazioni utente per i computer che non sono sempre connessi alla rete aziendale (computer remoti e portatili) e i computer sempre connessi alla rete (computer che eseguono sessioni VDI (Virtual Desktop Interface) Windows Server e host).

**Sincronizzazione per computer con connessioni sempre disponibili:** Quando si utilizza UE-V nei computer sempre connessi alla rete, è necessario configurare l'agente UE-V per sincronizzare le impostazioni utilizzando il parametro *SyncMethod=None,* che considera il server di archiviazione delle impostazioni come una condivisione di rete standard. In questa configurazione, il UE-V può essere configurato per notificare se l'importazione delle impostazioni dell'applicazione viene ritardata.

Abilita questa configurazione tramite uno dei metodi seguenti:

-   Durante l UE-V installazione, al prompt dei comandi o in un file batch, impostare il parametro *AgentSetup.exe SyncMethod = None*. [La distribuzione dell'UE-V 2.x fornisce](https://technet.microsoft.com/library/dn458891.aspx#agent) ulteriori informazioni.

-   Dopo l UE-V installazione, utilizzare la funzionalità gestione Impostazioni in System Center 2012 Configuration Manager o i modelli MDOP ADMX per eseguire il push della configurazione *SyncMethod = None.*

-   Utilizzare Windows PowerShell o Windows Management Instrumentation (WMI) per impostare *syncMethod = None* configuration.

    **Nota**  
    Questi ultimi due metodi non funzionano per gli ambienti VDI (Virtual Desktop Infrastructure) in pool.



È necessario riavviare il computer prima che le impostazioni inizino a sincronizzarsi.

**Nota**  
Se si imposta *SyncMethod = None*, le modifiche alle impostazioni vengono salvate direttamente nel server. Se la connessione di rete al percorso di archiviazione delle impostazioni non viene trovata, le modifiche alle impostazioni vengono memorizzate nella cache del dispositivo e sincronizzate alla successiva esecuzione del provider di sincronizzazione. Se il percorso di archiviazione delle impostazioni non viene trovato e il profilo utente viene rimosso da un ambiente VDI in pool alla disconnessione, le modifiche apportate alle impostazioni andranno perse e l'utente dovrà riapplicare la modifica quando il computer viene riconnesso al percorso di archiviazione delle impostazioni.



**Sincronizzazione per motori di sincronizzazione esterni:** Il parametro *SyncMethod=External* consente di specificare che se le impostazioni di UE-V vengono scritte in una cartella locale del computer utente, è possibile utilizzare qualsiasi motore di sincronizzazione esterno (ad esempio OneDrive for Business, Cartelle di lavoro, Sharepoint o Dropbox) per applicare queste impostazioni ai diversi computer a cui gli utenti accedono.

**Supporto per sessioni VDI condivise:** UE-V 2.1 e 2.1 SP1 forniscono supporto per le sessioni VDI condivise tra gli utenti finali. È possibile registrare e configurare uno speciale modello VDI, che garantisce che UE-V tutte le relative funzionalità siano intatte per le sessioni VDI non persistenti.

**Nota**  
Se non abiliti la modalità VDI per le sessioni VDI non persistenti, alcune funzionalità non funzionano, ad esempio backup/ripristino e last [known good (LKG).](https://technet.microsoft.com/library/dn878331.aspx)



Il modello VDI viene fornito con UE-V 2.1 e 2.1 SP1 ed è in genere disponibile qui dopo l'installazione: C:\\Programmi\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml

### <a name="prerequisites-for-ue-v-generator-support"></a>Prerequisiti per il UE-V Generator

Installare il generatore UE-V nel computer utilizzato per creare modelli di percorso delle impostazioni personalizzate. Questo computer dovrebbe essere in grado di eseguire le applicazioni le cui impostazioni sono sincronizzate. È necessario essere membri del gruppo Administrators nel computer che esegue il software UE-V Generator.

Il UE-V deve essere installato in un computer che utilizza un file system NTFS. Il software UE-V Generator richiede .NET Framework 4. Per ulteriori informazioni, vedere [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a name="other-resources-for-this-product"></a>Altre risorse per questo prodotto


-   [Microsoft User Experience Virtualization (UE-V) 2.x](index.md)

-   [Introduzione a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Amministrazione di UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Risoluzione dei UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














