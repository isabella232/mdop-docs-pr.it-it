---
title: Impostazioni di registrazione e traccia
description: Impostazioni di registrazione e traccia
author: dansimp
ms.assetid: 858b6fbf-65b4-42fa-95a9-69b04e5734d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 078bda16b5fcf968d45e0c4890487471105e8c44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820595"
---
# Impostazioni di registrazione e traccia


Le impostazioni del modello amministrativo per la gestione avanzata dei criteri di gruppo consentono di configurare in modo centralizzato le opzioni di registrazione e traccia per i server e i client di Advanced Group Policy in cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.

L'impostazione seguente è disponibile in computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM durante la modifica di un oggetto Criteri di gruppo.

**Percorsi dei file di traccia**:

-   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Impostazione</th>
<th align="left">Effetto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Advanced Group Policy Management: configurare la registrazione</strong></p></td>
<td align="left"><p>Questa impostazione consente di attivare e configurare la registrazione per Advanced Group Policy Management. Questa impostazione interessa sia i componenti client che quelli del server di Advanced Group Policy Management.</p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

-   [Cartella dei modelli amministrativi](administrative-templates-folder-agpm30ops.md)

 

 





