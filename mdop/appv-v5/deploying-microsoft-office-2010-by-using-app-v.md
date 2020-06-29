---
title: Distribuzione di Microsoft Office 2010 con App-V
description: Distribuzione di Microsoft Office 2010 con App-V
author: dansimp
ms.assetid: 0a9e496e-82a1-4dc0-a496-7b21eaa00f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 303a44d921e40a411a4c4ea4622f06a76b8ed9c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805877"
---
# Distribuzione di Microsoft Office 2010 con App-V


È possibile creare pacchetti di Office 2010 per Application Virtualization 5,0 usando uno dei metodi seguenti:

-   Application Virtualization (App-V) Sequencer

-   Acceleratore pacchetto Application Virtualization (App-V)

## Supporto di App-V per Office 2010


Nella tabella seguente sono illustrate le versioni di App-V, i metodi di creazione di pacchetti di Office, le licenze supportate e le distribuzioni supportate per Office 2010.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento supportato</th>
<th align="left">Livello di supporto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versioni App-V supportate</p></td>
<td align="left"><ul>
<li><p>4,6</p></li>
<li><p>5.0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Creazione di pacchetti</p></td>
<td align="left"><ul>
<li><p>Sequenziamento</p></li>
<li><p>Acceleratore pacchetto</p></li>
<li><p>Office Deployment Kit</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Licenze supportate</p></td>
<td align="left"><p>Contratti multilicenza</p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribuzioni supportate</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>VDI personale</p></li>
<li><p>RDS</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Creazione di Office 2010 App-V 5,0 con il sequencer


La sequenziazione di Office 2010 è uno dei metodi principali per la creazione di un pacchetto di Office 2010 in App-V 5,0. Microsoft ha fornito una ricetta dettagliata tramite un articolo della Knowledge base. Per creare un pacchetto di Office 2010 in App-V 5,0, vedere il collegamento seguente per istruzioni dettagliate:

[Come sequenziare Microsoft Office 2010 in Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## Creazione di pacchetti di Office 2010 App-V 5,0 con gli acceleratori pacchetto


I pacchetti di Office 2010 App-V 5,0 possono essere creati tramite acceleratori pacchetto. Microsoft ha fornito gli acceleratori pacchetto per la creazione di Office 2010 in Windows 8 e Windows 7. Per creare pacchetti di Office 2010 in App-V con gli acceleratori pacchetto, fare riferimento alle pagine seguenti per accedere all'Acceleratore pacchetto appropriato:

-   [Acceleratore pacchetto App-V 5,0 per Office Professional Plus 2010-Windows 8](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [Acceleratore pacchetto App-V 5,0 per Office Professional Plus 2010-Windows 7](https://go.microsoft.com/fwlink/p/?LinkId=330678)

Per istruzioni dettagliate su come creare pacchetti di applicazioni virtuali con gli acceleratori di pacchetti App-V, vedere [come creare un pacchetto di applicazione virtuale usando un Acceleratore pacchetto App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).

## Distribuzione del pacchetto Microsoft Office per App-V 5,0


È possibile distribuire i pacchetti di Office 2010 usando uno dei metodi di distribuzione di App-V seguenti:

-   System Center Configuration Manager

-   App-V Server

-   Autonomo tramite i comandi di PowerShell

## Gestione e personalizzazione dei pacchetti di Office App-V


I pacchetti di Office 2010 possono essere gestiti come qualsiasi altro pacchetto App-V 5,0 attraverso i meccanismi di gestione dei pacchetti noti. Non sono necessarie istruzioni speciali, ad esempio per aggiungere, pubblicare, annullare la pubblicazione o rimuovere i pacchetti di Office.

## Integrazione di Microsoft Office con Windows


La tabella seguente include un elenco completo dei punti di integrazione supportati per Office 2010.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Punto di estensione</th>
<th align="left">Descrizione</th>
<th align="left">Office 2010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plug-in di Lync meeting join per Firefox e Chrome</p></td>
<td align="left"><p>L'utente può partecipare a riunioni Lync da Firefox e Chrome</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Inviato al driver di stampa di OneNote</p></td>
<td align="left"><p>L'utente può stampare in OneNote</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Note collegate in OneNote</p></td>
<td align="left"><p>Note collegate in OneNote</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Inviare al componente aggiuntivo OneNote Internet Explorer</p></td>
<td align="left"><p>L'utente può inviare a OneNote da IE</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eccezione del firewall per Lync e Outlook</p></td>
<td align="left"><p>Eccezione del firewall per Lync e Outlook</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Client MAPI</p></td>
<td align="left"><p>Le app e i componenti aggiuntivi nativi possono interagire con Outlook virtuale tramite MAPI</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Plug-in di SharePoint per Firefox</p></td>
<td align="left"><p>L'utente può usare le caratteristiche di SharePoint in Firefox</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet del pannello di controllo posta</p></td>
<td align="left"><p>L'utente ottiene l'applet del pannello di controllo della posta in Outlook</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Assembly di interoperabilità primari</p></td>
<td align="left"><p>Supportare i componenti aggiuntivi gestiti</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestore della cache dei documenti di Office</p></td>
<td align="left"><p>Consente la cache dei documenti per le applicazioni di Office</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestore ricerca protocollo di Outlook</p></td>
<td align="left"><p>L'utente può eseguire ricerche in Outlook</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlli Active X:</p></td>
<td align="left"><p>Per altre informazioni sui controlli ActiveX, vedere <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> riferimenti alle API dei controlli ActiveX </a> .</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect. PersonalSite</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Sharpoint. OpenXMLDocuments</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld. CopyCtl</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Controllo Active X</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Helper del browser OneDrive Pro</p></td>
<td align="left"><p>Controllo Active X]</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sovrapposizioni di icone di OneDrive Pro</p></td>
<td align="left"><p>L'icona della shell di Windows Explorer si sovrappone quando gli utenti esaminano le cartelle di OneDrive Pro</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Risorse aggiuntive


**Office 2013 App-V 5,0 packages 5,0 risorse aggiuntive**

[Scenari supportati per la distribuzione di Microsoft Office come pacchetto di App-V sequenziato](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Pacchetti app di Office 2010-V 5,0**

[Microsoft Office 2010-Kit di sequenziazione per Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Problemi noti quando si crea o si usa un pacchetto di App-V 5,0 Office 2010](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Come sequenziare Microsoft Office 2010 in Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Gruppi di connessioni**

[Distribuzione di gruppi di connessioni in Microsoft App-V v5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Gestione dei gruppi di connessione](managing-connection-groups.md)

**Configurazione dinamica**

[Informazioni sulla configurazione dinamica di App-V 5.0](about-app-v-50-dynamic-configuration.md)






 

 





