---
title: Riferimento della riga di comando dell'installazione client
description: Riferimento della riga di comando dell'installazione client
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826726"
---
# Riferimento della riga di comando dell'installazione client


**Per installare MED-V dalla riga di comando**

1.  Dalla riga di comando eseguire il pacchetto MED-V. msi seguito da uno dei parametri facoltativi descritti nella tabella seguente.

2.  Il pacchetto MED-V. msi si chiama *MED-V\_x.msi*, dove *x* corrisponde al numero di versione.

    Ad esempio, *MED-V\_1.0.65.msi*.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Valore</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/quiet</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Installazione invisibile all'utente</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;percorso completo di/log per il file di log&gt;</p></td>
<td align="left"><p>Percorso completo del file di log.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>Percorso completo della directory di installazione.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>VMSFOLDER</p></td>
<td align="left"><p>Percorso completo della cartella della macchina virtuale.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALL_ADMIN_TOOLS</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Impostazione predefinita: <strong> 0</strong></p></td>
<td align="left"><p>Installa gli strumenti di amministrazione di MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>START_AUTOMATICALLY</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Impostazione predefinita: <strong> 0</strong></p></td>
<td align="left"><p>Avvia automaticamente il client MED-V ogni volta che l'utente accede a Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_ADDRESS</p></td>
<td align="left"><p>nome host o IP</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER_PORT</p></td>
<td align="left"><p>porta</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_SSL</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>per <strong> https </strong> o <strong> http</strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>START_MEDV</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Impostazione predefinita: <strong> 1</strong></p></td>
<td align="left"><p>Avvia MED-V al completamento dell'installazione di MED-V.</p>
<div class="alert">
<strong>Nota</strong><br/><p>È consigliabile impostare START_MEDV = 0 nel caso in cui MED-V sia installato dal sistema.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DESKTOP_SHORTCUT</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Impostazione predefinita: <strong> 1</strong></p></td>
<td align="left"><p>Crea un collegamento sul desktop, che avvia il client MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MINIMAL_RAM_REQUIRED</p></td>
<td align="left"><p>RAM in MB</p></td>
<td align="left"><p>Durante l'installazione di MED-V, controlla se il computer ha la quantità minima di RAM specificata. In caso contrario, l'installazione viene interrotta.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SKIP_OS_CHECK</p></td>
<td align="left"><p><strong>1,0</strong></p></td>
<td align="left"><p>Omette la convalida del sistema operativo.</p></td>
</tr>
</tbody>
</table>











