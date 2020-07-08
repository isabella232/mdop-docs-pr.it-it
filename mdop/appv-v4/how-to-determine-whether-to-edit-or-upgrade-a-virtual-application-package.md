---
title: Come scegliere se modificare o aggiornare un pacchetto applicazione virtuale
description: Come scegliere se modificare o aggiornare un pacchetto applicazione virtuale
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817505"
---
# Come scegliere se modificare o aggiornare un pacchetto applicazione virtuale


Usare la tabella seguente per determinare se un pacchetto di applicazione virtuale può essere aperto per la modifica, se è necessario creare una nuova versione del pacchetto o se è disponibile un'opzione, usando l'App-V Sequencer.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Azione</th>
<th align="left">Apri per la modifica</th>
<th align="left">Apri per l'aggiornamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Visualizzare le proprietà del pacchetto.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Visualizzare la cronologia delle modifiche del pacchetto.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Visualizzare i file di pacchetto associati.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modificare le impostazioni del registro di sistema.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rivedere le impostazioni aggiuntive del pacchetto (ad eccezione delle proprietà del file di sistema operativo).</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Creare Windows Installer (MSI) associato.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modificare il file OSD.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Comprimere e decomprimere il pacchetto.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aggiungere associazioni di tipi di file.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Rinominare i tasti di scelta rapida.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostare lo stato della chiave del registro di sistema virtualizzato (override/merge).</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Impostare lo stato della cartella virtualizzata.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modificare i mapping di file system virtuali.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esaminare tutte le proprietà del file del sistema operativo associato per un pacchetto.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aggiungere altri servizi.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aggiungere altri file.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Raccogliere e configurare i descrittori di sicurezza associati.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applicare gli aggiornamenti della sicurezza o eseguire l'aggiornamento a una nuova versione.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Aggiungere un'applicazione aggiuntiva.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applicare gli aggiornamenti che richiedono l'apertura dell'applicazione.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Applicare gli aggiornamenti che richiedono il riavvio del computer.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Come modificare un'applicazione virtuale esistente](how-to-edit-an-existing-virtual-application.md)

[Come eseguire l'aggiornamento di un'applicazione virtuale esistente](how-to-upgrade-an-existing-virtual-application.md)

 

 





