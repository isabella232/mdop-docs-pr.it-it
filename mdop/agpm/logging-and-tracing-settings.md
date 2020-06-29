---
title: Impostazioni di registrazione e traccia
description: Impostazioni di registrazione e traccia
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820586"
---
# Impostazioni di registrazione e traccia


Le impostazioni del modello amministrativo per la gestione avanzata dei criteri di gruppo consentono di configurare in modo centralizzato le opzioni di registrazione e traccia per i server e i client di Advanced Group Policy in cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.

L'impostazione seguente è disponibile in computer Configuration\\Administrative Templates\\Windows Components\\AGPM nell' **Editor oggetti Criteri di gruppo** per la modifica di un oggetto Criteri di gruppo in console Gestione criteri di Group (GPMC). Se il percorso non è visibile, fare clic con il pulsante destro del mouse su **modelli amministrativi**e quindi aggiungere il modello Advanced Group Policy Management. admx o Advanced Group Policy Management.

**Percorsi dei file di traccia**:

-   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

-   Server:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log

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
<td align="left"><p><strong>Registrazione Advanced Group Policy</strong></p></td>
<td align="left"><p>Se abilitata, questa impostazione Configura se la traccia è attivata e il livello di dettaglio. Questa impostazione interessa sia i componenti client che quelli del server di Advanced Group Policy Management.</p>
<p>Se disabilitata o non configurata, questa impostazione non ha alcun effetto.</p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

-   [Impostazioni del modello amministrativo](administrative-template-settings.md)

 

 





