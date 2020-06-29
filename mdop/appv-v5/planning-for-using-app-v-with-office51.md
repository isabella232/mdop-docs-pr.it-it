---
title: Pianificazione per l'uso di App-V con Office
description: Pianificazione per l'uso di App-V con Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804959"
---
# Pianificazione per l'uso di App-V con Office


Usare le informazioni seguenti per pianificare la distribuzione di Office tramite Microsoft Application Virtualization (App-V) 5,1. Questo articolo include:

-   [Supporto di App-V per i Language Pack](#bkmk-lang-pack)

-   [Versioni supportate di Microsoft Office](#bkmk-office-vers-supp-appv)

-   [Pianificazione dell'uso di App-V con le versioni coesistenti di Office](#bkmk-plan-coexisting)

-   [Modalità di integrazione di Office con Windows quando si distribuisce USA App-V per distribuire Office](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a>Supporto di App-V per i Language Pack


Puoi usare il sequencer App-V 5,1 per creare pacchetti plug-in per Language Pack, Language Interface Pack, strumenti di correzione e lingue delle descrizioni comandi. Puoi quindi includere i pacchetti plug-in in un gruppo di connessioni, insieme al pacchetto di Office 2013 creato tramite Office Deployment Toolkit. Le applicazioni di Office e i Language Pack plug-in interagiscono perfettamente nello stesso gruppo di connessioni, come tutti gli altri pacchetti raggruppati in un gruppo di connessioni.

>**Nota**  Microsoft Visio e Microsoft Project non consentono di supportare il Language Pack tailandese.

 

## <a href="" id="bkmk-office-vers-supp-appv"></a>Versioni supportate di Microsoft Office

Vedere [ID prodotto Microsoft Office supportati da App-V](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) per un elenco di prodotti Office compatibili.
>**Note** &nbsp; Nota &nbsp; Devi usare lo strumento di distribuzione di Office per creare pacchetti App-V per le app Microsoft 365 per le aziende. La creazione di pacchetti per le versioni con contratto multilicenza di Office Professional Plus o Office standard non è supportata. Non è possibile usare l'App-V Sequencer.

 

## <a href="" id="bkmk-plan-coexisting"></a>Pianificazione dell'uso di App-V con le versioni coesistenti di Office


È possibile installare più di una versione di Microsoft Office affiancata nello stesso computer usando "coesistenza di Microsoft Office". Puoi implementare la coesistenza di Office con le combinazioni di tutte le versioni principali di Office e con i metodi di installazione, se applicabile, usando la versione di Office basata su Windows Installer (MSi), a portata di clic e App-V 5,1. Tuttavia, l'uso della coesistenza di Office non è consigliato da Microsoft.

La procedura consigliata di Microsoft è quella di evitare completamente la coesistenza di Office per evitare problemi di compatibilità. Tuttavia, quando si esegue la migrazione a una versione più recente di Office, si verificano occasionalmente problemi che non possono essere risolti immediatamente, in modo da poter implementare temporaneamente la coesistenza per facilitare una migrazione più rapida alla versione più recente del prodotto. L'uso della coesistenza di Office a lungo termine non è mai consigliato e l'organizzazione dovrebbe avere un piano per la transizione completa nell'immediato futuro.

### Prima di implementare la coesistenza di Office

Prima di implementare la coesistenza di Office, esaminare la documentazione di Office seguente. Scegliere l'articolo che corrisponde alla versione più recente di Office per cui si intende implementare la coesistenza.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di Office</th>
<th align="left">Collegamento alle indicazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)">Informazioni su come usare le suite e i programmi di Office 2013 (distribuzione MSI) in un computer in cui è in esecuzione un'altra versione di Office</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)">Informazioni sull'uso di Office 2010 Suites e programmi in un computer in cui è in esecuzione un'altra versione di Office</a></p></td>
</tr>
</tbody>
</table>

 

La documentazione di Office offre indicazioni esaustive sulla coesistenza per le installazioni di Office basate su Windows Installer (MSi) e a portata di clic. Questo argomento App-V sulla coesistenza integra le indicazioni di Office con le informazioni più specifiche per le distribuzioni di App-V.

### Scenari di coesistenza di Office supportati

Le tabelle seguenti riepilogano gli scenari di coesistenza supportati. Sono organizzati in base al metodo di versione e distribuzione a cui si sta iniziando e al metodo di versione e distribuzione a cui si sta eseguendo la migrazione. Assicurarsi di testare completamente tutte le soluzioni di coesistenza prima di distribuirle a un gruppo di destinatari.

>**Nota**  Microsoft non supporta l'uso di più versioni di Office in ambienti Windows Server in cui è abilitato il servizio ruolo Host sessione Desktop remoto. Per eseguire scenari di coesistenza di Office, è necessario disabilitare questo servizio ruolo.

 

### Integrazioni di Windows & coesistenza di Office

I metodi di installazione di Office basati su Windows Installer e a portata di clic vengono integrati con alcuni punti del sistema operativo Windows sottostante. Quando si usa la coesistenza, le integrazioni comuni dei sistemi operativi tra due versioni di Office possono essere in conflitto, causando problemi di compatibilità e esperienza utente. Con App-V puoi sequenziare alcune versioni di Office per escludere le integrazioni, quindi "isolarle" dal sistema operativo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Modalità in cui App-V può sequenziare questa versione di Office</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2007</p></td>
<td align="left"><p>Sempre non integrati. App-V non offre integrazioni di sistemi operativi con una versione virtualizzata di Office 2007.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p>Modalità integrata e non integrata.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p>Sempre integrata. Le integrazioni dei sistemi operativi Windows non possono essere disabilitate.</p></td>
</tr>
</tbody>
</table>

 

Microsoft consiglia di distribuire la coesistenza di Office con una sola istanza di Office integrata. Ad esempio, se si usa App-V per distribuire Office 2010 e Office 2013, è necessario sequenziare Office 2010 in modalità non integrata. Per altre informazioni sulla sequenziazione di Office in modalità non di integrazione (isolata), vedere [come sequenziare Microsoft office 2010 in Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).

### Limitazioni note degli scenari di coesistenza di Office

Le sezioni seguenti descrivono alcuni problemi che potresti riscontrare quando usi App-V per implementare la coesistenza con Office.

### Limitazioni comuni agli scenari di coesistenza di Windows Installer e a portata di clic e App-V Office

Quando si installano le versioni seguenti di Office nello stesso computer, è possibile che siano presenti le limitazioni seguenti:

-   Office 2010 tramite la versione basata su Windows Installer

-   Office 2013 tramite App-V

Dopo aver pubblicato Office 2013 tramite App-V affiancata a una versione precedente di Office 2010 basato su Windows Installer, potrebbe essere necessario avviare Windows Installer. Il motivo è che la versione basata su Windows Installer o a portata di clic di Office 2010 sta provando a eseguire automaticamente la registrazione nel computer.

Per ignorare l'operazione di registrazione automatica per Word 2010 nativo, eseguire le operazioni seguenti:

1.  Uscire da Word 2010.

2.  Avviare l'editor del registro di sistema eseguendo le operazioni seguenti:

    -   In Windows 7: fare clic sul pulsante **Start**, digitare **Regedit** nella casella Inizia ricerca e quindi premere INVIO.

    -   In Windows 8,1 o Windows 10 digitare **Regedit** premere INVIO nella pagina iniziale e quindi premere INVIO.

    Se viene richiesta una password di amministratore o per una conferma, digitare la password oppure fare clic su **continua**.

3.  Individuare e quindi selezionare la sottochiave del registro di sistema seguente:

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  Scegliere **nuovo**dal menu **modifica** e quindi fare clic su **valore DWORD**.

5.  Digitare **NoReReg**e quindi premere INVIO.

6.  Fare clic con il pulsante destro del mouse su **NoReReg** e quindi scegliere **modifica**.

7.  Nella casella **Dativalore** Digitare **1**e quindi fare clic su **OK**.

8.  Nel menu file fare clic su **Esci** per chiudere l'editor del registro di sistema.

## <a href="" id="bkmk-office-integration-win"></a>Modalità di integrazione di Office con Windows quando si usa App-V per distribuire Office


Quando si distribuisce Office 2013 tramite App-V, Office è completamente integrato con il sistema operativo, che fornisce agli utenti finali le stesse funzionalità e funzionalità di Office quando viene distribuita senza App-V.

Il pacchetto Office 2013 App-V supporta i punti di integrazione seguenti con il sistema operativo Windows:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Punto di estensione</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plug-in di Lync meeting join per Firefox e Chrome</p></td>
<td align="left"><p>L'utente può partecipare a riunioni Lync da Firefox e Chrome</p></td>
</tr>
<tr class="even">
<td align="left"><p>Inviato al driver di stampa di OneNote</p></td>
<td align="left"><p>L'utente può stampare in OneNote</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Note collegate in OneNote</p></td>
<td align="left"><p>Note collegate in OneNote</p></td>
</tr>
<tr class="even">
<td align="left"><p>Inviare al componente aggiuntivo OneNote Internet Explorer</p></td>
<td align="left"><p>L'utente può inviare a OneNote da IE</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eccezione del firewall per Lync e Outlook</p></td>
<td align="left"><p>Eccezione del firewall per Lync e Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client MAPI</p></td>
<td align="left"><p>Le app e i componenti aggiuntivi nativi possono interagire con Outlook virtuale tramite MAPI</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plug-in di SharePoint per Firefox</p></td>
<td align="left"><p>L'utente può usare le caratteristiche di SharePoint in Firefox</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet del pannello di controllo posta</p></td>
<td align="left"><p>L'utente ottiene l'applet del pannello di controllo della posta in Outlook</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Assembly di interoperabilità primari</p></td>
<td align="left"><p>Supportare i componenti aggiuntivi gestiti</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore della cache dei documenti di Office</p></td>
<td align="left"><p>Consente la cache dei documenti per le applicazioni di Office</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore ricerca protocollo di Outlook</p></td>
<td align="left"><p>L'utente può eseguire ricerche in Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlli Active X:</p></td>
<td align="left"><p>Per altre informazioni sui controlli ActiveX, vedere <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> riferimenti alle API dei controlli ActiveX </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect. PersonalSite</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenXMLDocuments</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld. CopyCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Controllo Active X</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Helper del browser OneDrive Pro</p></td>
<td align="left"><p>Controllo Active X]</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sovrapposizioni di icone di OneDrive Pro</p></td>
<td align="left"><p>L'icona della shell di Windows Explorer si sovrappone quando gli utenti esaminano le cartelle di OneDrive Pro</p></td>
</tr>
<tr class="even">
<td align="left"><p>Estensioni della shell</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scorciatoie</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Search</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





