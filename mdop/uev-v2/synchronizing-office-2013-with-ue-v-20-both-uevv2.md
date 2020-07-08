---
title: Sincronizzazione di Office 2013 con UE-V 2,0
description: Sincronizzazione di Office 2013 con UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826886"
---
# Sincronizzazione di Office 2013 con UE-V 2,0


Microsoft User Experience Virtualization (UE-V) 2,0 supporta la sincronizzazione dell'impostazione delle applicazioni di Microsoft Office 2013 usando un modello disponibile nella raccolta modelli di UE-V. La combinazione di supporto di UE-V 2 e App-V 5,0 SP2 di Office 2013 Professional Plus consente di ottenere la stessa esperienza su un'istanza virtualizzata di Office 2013 da qualsiasi dispositivo abilitato per la versione UE o desktop virtualizzato.

Per attivare il supporto delle impostazioni dell'applicazione UE-V di Office 2013, è possibile scaricare i modelli ufficiali UE-V Office 2013 dalla [raccolta modelli di Microsoft User Experience Virtualization (UE-v) 2](https://go.microsoft.com/fwlink/p/?LinkId=246589). Questa risorsa include i modelli di posizione delle impostazioni della community-V creati da Microsoft e i modelli di posizione delle impostazioni sviluppati dalla Comunità.

## Supporto di Microsoft Office in UE-V


UE-V 1,0 e UE-V 2 includono i modelli di posizione delle impostazioni per Microsoft Office 2010. Questi modelli vengono distribuiti e registrati nell'ambito del processo di installazione dell'agente UE-V. Questi modelli aiutano a sincronizzare l'esperienza di Office degli utenti tra i dispositivi. I modelli UE-V per Office 2013 garantiscono un'esperienza di impostazioni molto simile ai modelli per Office 2010. Le impostazioni di Microsoft Office 2013 in roaming con l'esperienza di Office 365 non sono incluse in queste impostazioni. Per un elenco delle impostazioni specifiche di Office 365, vedere [Panoramica delle impostazioni utente e roaming per office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).

## Impostazioni di Office 2013 sincronizzate


Le tabelle seguenti contengono i dettagli per il supporto di Office 2013 in UE-V:

### Modelli UE-V supportati per Microsoft Office

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Modelli di Office 2013 (UE-V 2,0, disponibili nella raccolta UE-V):</th>
<th align="left">Modelli di Office 2010 (UE-V 1,0 &amp; 1,0 SP1):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftOffice2013Win32.xml</p>
<p>MicrosoftOffice2013Win64.xml</p>
<p>MicrosoftLync2013Win32.xml</p>
<p>MicrosoftLync2013Win64.xml</p></td>
<td align="left"><p>MicrosoftOffice2010Win32.xml</p>
<p>MicrosoftOffice2010Win64.xml</p>
<p>MicrosoftLync2010.xml</p>
<p></p></td>
</tr>
</tbody>
</table>

 

### Applicazioni di Microsoft Office supportate dai modelli UE-V

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Access 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft Word 2013</p>
<p>Microsoft Office Upload Manager</p></td>
<td align="left"><p>Microsoft Access 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft SharePoint Designer 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft Word 2010</p>
<p></p></td>
</tr>
</tbody>
</table>

 

## Distribuzione dei modelli di Office 2013


È possibile distribuire il modello di posizione delle impostazioni di UE-V con i metodi seguenti:

-   **Registrazione di un modello tramite PowerShell**. Se si usa Windows PowerShell per gestire i computer, eseguire il comando di Windows PowerShell seguente aperto come amministratore per registrare il modello di posizione delle impostazioni:

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    Per altre informazioni sull'uso di UE-V e Windows PowerShell, vedere [gestione dei modelli di posizione delle impostazioni di UE-v 2. x tramite Windows PowerShell e WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

-   **Registrazione del modello tramite il percorso Catalogo modelli**. Se si usa il percorso catalogo delle impostazioni per gestire i modelli nei computer degli utenti, copiare il modello di Office 2013 nella cartella definita nell'agente UE-V. La volta successiva che viene eseguita l'attività programmata per l'aggiornamento automatico del modello (ApplySettingsCatalog.exe), il modello di posizione delle impostazioni verrà registrato nel dispositivo. Per altre informazioni, vedere [distribuzione del catalogo di modelli di impostazioni per UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).

-   **Registrazione di un modello tramite Configuration Manager**. Se si usa Configuration Manager per gestire i modelli di archiviazione delle impostazioni di UE-V, ricreare il modello CAB Baseline, importarlo in Configuration Manager e quindi distribuire la linea di base ai client. Per altre informazioni, vedere le indicazioni fornite nella documentazione relativa al [pacchetto di configurazione di System Center 2012 per Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).






 

 





