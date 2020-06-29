---
title: Scheda Delega dominio
description: Scheda Delega dominio
author: dansimp
ms.assetid: 5be5841e-92fb-4af6-aa68-0ae50f8d5141
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c5f3b5c3b7d8799b383ab48870fcccad0b0c3f73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818636"
---
# Scheda Delega dominio


La scheda **delega del dominio** nel riquadro **Cambia controllo** fornisce un elenco di amministratori dei criteri di gruppo con accesso a livello di dominio all'archivio e indica i ruoli di ognuno. Questa scheda consente inoltre agli amministratori della gestione avanzata Criteri di amministrazione (controllo completo) di configurare le autorizzazioni a livello di dominio per editor, responsabili approvazione, revisori e altri amministratori della gestione avanzata Criteri di gruppo. Nella scheda **delega del dominio** sono presenti due sezioni, ovvero la configurazione della notifica tramite posta elettronica e la delega basata sui ruoli per Advanced Group Policy Management a livello di dominio.

## Configurazione della notifica tramite posta elettronica


La sezione notifica tramite posta elettronica di questa scheda identifica i responsabili approvazione che riceveranno una notifica quando le operazioni sono in sospeso in Advanced Group Policy Management.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Impostazione</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Dall'indirizzo di posta elettronica</strong></p></td>
<td align="left"><p>L'alias Advanced Group Policy Management da cui viene inviata una notifica agli approvatori. In un ambiente con più domini può essere lo stesso alias nell'ambiente o in un altro alias per ogni dominio.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>A indirizzo di posta elettronica</strong></p></td>
<td align="left"><p>Elenco delimitato da virgole di indirizzi di posta elettronica degli approvatori a cui inviare la notifica</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Server SMTP</strong></p></td>
<td align="left"><p>Nome del server di posta elettronica, ad esempio mail.contoso.com</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nome utente</strong></p></td>
<td align="left"><p>Un utente con accesso al server SMTP</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Password</strong></p></td>
<td align="left"><p>Password dell'utente per l'autenticazione nel server SMTP</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Conferma password</strong></p></td>
<td align="left"><p>Confermare la password dell'utente</p></td>
</tr>
</tbody>
</table>

 

## Delega basata sui ruoli a livello di dominio


La sezione delega basata sui ruoli di questa scheda Visualizza e consente a un amministratore Advanced Group Policy Management di delegare le autorizzazioni consentite, negate e ereditate per ogni gruppo e utente nel dominio con accesso all'archivio. Un amministratore della gestione avanzata Criteri di amministrazione può configurare le autorizzazioni a livello di dominio usando i ruoli Advanced Group Policy Management (editor, approvatore, revisore e amministratore della gestione avanzata) o una combinazione personalizzata di autorizzazioni per ogni amministratore dei criteri di gruppo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Button</th>
<th align="left">Effetto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Aggiungi</strong></p></td>
<td align="left"><p>Aggiungere una nuova voce al descrittore di sicurezza. Gli utenti o i gruppi di Active Directory possono essere aggiunti come amministratori dei criteri di gruppo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Rimuovi</strong></p></td>
<td align="left"><p>Rimuovere gli amministratori dei criteri di gruppo selezionati dall'elenco di controllo di Access.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Proprietà</strong></p></td>
<td align="left"><p>Visualizzare le proprietà per gli amministratori dei criteri di gruppo selezionati.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Avanzate</strong></p></td>
<td align="left"><p>Aprire l' <strong> Editor elenco di controllo di Access </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Considerazioni aggiuntive

-   Per informazioni su ruoli e autorizzazioni correlati a specifiche attività, vedere le attività in [esecuzione di attività di amministratore della gestione avanzata Criteri di amministrazione](performing-agpm-administrator-tasks-agpm40.md), esecuzione di attività dell' [Editor](performing-editor-tasks-agpm40.md), esecuzione di [attività di approvazione](performing-approver-tasks-agpm40.md)ed esecuzione di [attività del revisore](performing-reviewer-tasks-agpm40.md).

### Riferimenti aggiuntivi

-   [Interfaccia utente: Gestione avanzata Criteri di gruppo](user-interface-advanced-group-policy-management-agpm40.md)

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks-agpm40.md)

 

 





