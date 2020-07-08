---
title: Elenco di controllo per valutare le applicazioni line-of-business per UE-V 1.0
description: Elenco di controllo per valutare le applicazioni line-of-business per UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826456"
---
# Elenco di controllo per valutare le applicazioni line-of-business per UE-V 1.0


Per valutare le applicazioni line-of-business da includere nella distribuzione UE-V, tenere presente quanto segue:

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
<td align="left"><p>È importante per l'utente che queste impostazioni si aggirano?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Queste impostazioni utente sono già gestite da una soluzione dei criteri di gestione o impostazioni delle applicazioni? UE-V applica le impostazioni dell'applicazione all'avvio dell'applicazione e alle impostazioni di Windows agli eventi logon, Unlock o Connect remoto. Se si usa UE-V con altre soluzioni per i criteri di impostazioni, gli utenti potrebbero riscontrare incongruenze tra le impostazioni in roaming.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Le impostazioni dell'applicazione sono specifiche per il computer? Le preferenze e le personalizzazioni delle applicazioni associate all'hardware o alle configurazioni di computer specifiche non si aggirano in modo coerente tra le sessioni e possono causare un'esperienza di applicazione insufficiente.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Le impostazioni dell'archivio applicazioni si trovano nella directory Program Files o nella directory di file che si trova nella <strong> Directory Users </strong> \ [user name] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ? I dati dell'applicazione archiviati in uno di questi percorsi in genere non devono essere spostati con l'utente, perché questi dati sono specifici del computer o perché i dati sono troppo grandi per spostarsi in roaming.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>L'applicazione archivia le impostazioni in un file che contiene altri dati dell'applicazione che non devono essere spostati? UE-V sincronizza i file come unità singola. Se le impostazioni sono archiviate in file che includono dati dell'applicazione diversi dalle impostazioni, la sincronizzazione di questi dati aggiuntivi può causare un'esperienza di applicazione insufficiente.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Dimensioni dei file che contengono le impostazioni Le prestazioni della sincronizzazione delle impostazioni possono essere influenzate da file di grandi dimensioni. L'inclusione di file di grandi dimensioni può influire sulle prestazioni della sincronizzazione delle impostazioni.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Pianificazione per i metodi di configurazione di UE-V](planning-for-ue-v-configuration-methods.md)

[Pianificazione di UE-V 1.0](planning-for-ue-v-10.md)

 

 





