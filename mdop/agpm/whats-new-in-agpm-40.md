---
title: Novità di Gestione avanzata Criteri di gruppo 4.0
description: Novità di Gestione avanzata Criteri di gruppo 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820105"
---
# Novità di Gestione avanzata Criteri di gruppo 4.0


Gestione avanzata Criteri di gruppo di Microsoft (Advanced Group Policy Management) 4.0 include nuove funzionalità che consentono di cercare oggetti Criteri di gruppo, filtrare l'elenco dei GPO visualizzati, esportare e importare un GPO in un'altra foresta e installare Advanced Group Policy Manager nei computer che eseguono Windows7 e Windows Server2008R2.

## Cercare e filtrare gli oggetti Criteri di ricerca


In Advanced Group Policy Management 4,0 è possibile eseguire una ricerca nell'elenco di GPO per individuare attributi specifici per filtrare l'elenco dei GPO visualizzati. Ad esempio, puoi cercare gli oggetti Criteri di ricerca con un nome, uno stato o un commento specifico. È anche possibile cercare gli oggetti Criteri di gruppo modificati per l'ultima volta da un determinato amministratore dei criteri di raggruppamento o in una data specifica.

Puoi creare una stringa di ricerca complessa usando il formato *attributo GPO 1: ricerca testo 1 attributo GPO 2: ricerca testo 2...*, dove un attributo GPO è qualsiasi intestazione di colonna nell'elenco di GPO in Advanced Group Policy Management. Ad esempio, per cercare tutti i GPO con nomi che includono il testo "MioGPO" che sono stati archiviati e modificati per l'ultima volta dall'utente Editor03, digitare quanto segue nella casella di ricerca: **Nome: MioGPO stato:****archiviato****modificato da: Editor03**. La ricerca restituisce le corrispondenze parziali in modo che sia possibile immettere parte di un nome di oggetto o di un nome utente e visualizzare un elenco di tutti i GPO che includono il testo nel nome.

Inoltre, puoi usare gli stessi termini speciali disponibili durante la ricerca in Windows per cercare gli oggetti Criteri di ricerca modificati in una data o un intervallo di date specifico. Ad esempio, **Cambia Data:****lastmonth** o **modifica data:****ThisWeek**.

## Esportare e importare GPO in foreste diverse


Usando Advanced Group Policy Management 4,0, è possibile copiare un oggetto Criteri di campo controllato da un dominio in una foresta in un dominio in una seconda foresta. Ad esempio, è possibile esportare un oggetto Criteri di stato da un dominio in una foresta in un file CAB tramite Advanced Group Policy Management, copiare il file CAB in un'unità USB, collegare l'unità USB a un computer di un dominio in una seconda foresta e importare l'oggetto Criteri di ricerca in Advanced Group Policy in un dominio della seconda foresta. Puoi importare l'oggetto Criteri di controllo come nuovo GPO controllato oppure importarlo per sostituire le impostazioni di un oggetto Criteri di controllo esistente Estratto.

## Supporto per Windows Server 2008 R2 e Windows 7


Advanced Group Policy Management 4,0 supporta Windows Server2008R2 e Windows7, ma supporta ancora Windows Server2008 e WindowsVista® con Service Pack1 (SP1). Esistono tuttavia limitazioni in un ambiente misto che include sia i sistemi operativi più recenti che quelli più vecchi, come indicato nella tabella seguente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo in cui viene eseguito Advanced Server Group Policy Management 4,0</th>
<th align="left">Sistema operativo in cui viene eseguito il client Advanced Group Policy Management 4,0</th>
<th align="left">Stato del supporto per Advanced Group Policy Management 4,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>File modifiche disco non supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</p></td>
</tr>
</tbody>
</table>

 

 

 





