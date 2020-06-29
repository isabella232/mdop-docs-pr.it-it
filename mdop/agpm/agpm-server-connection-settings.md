---
title: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
description: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804665"
---
# Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo


È possibile usare le impostazioni dei modelli amministrativi per la gestione avanzata dei criteri di gruppo per configurare centralmente le connessioni del server Advanced Group Policy Management per gli amministratori dei criteri di gruppo a cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.

Le impostazioni seguenti sono disponibili in utenti Configuration\\Administrative Templates\\Windows Components\\AGPM durante la modifica di un oggetto Criteri di gruppo. Se il percorso non è visibile, fare clic con il pulsante destro del mouse su **modelli amministrativi**e quindi aggiungere il modello Advanced Group Policy Management. admx o Advanced Group Policy Management.

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
<td align="left"><p><strong>Server Advanced Group Policy Management (tutti i domini)</strong></p></td>
<td align="left"><p>Se abilitata, questa impostazione Configura centralmente una connessione al server Advanced Group Policy per l'uso da parte di tutti i domini e Disabilita le impostazioni nella <strong> scheda Server Advanced Group Policy Management </strong> per gli amministratori dei criteri di gruppo. Per più server Advanced Group Policy Management, configurare questa impostazione con un server predefinito e quindi configurare l' <strong> impostazione del server Advanced Group Policy Management </strong> nel modello amministrativo per eseguire l'override di questo server per altri domini.</p>
<p>Se disabilitata o non configurata, ogni amministratore dei criteri di gruppo deve selezionare il server Advanced Group Policy Management da visualizzare per ogni dominio nella <strong> scheda Server Advanced Group Policy Management </strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Server Advanced Group Policy Management</strong></p></td>
<td align="left"><p>Se abilitata, questa impostazione Configura centralmente più server di Advanced Group Policy Management specifici del dominio, eseguendo l'override del <strong> server Advanced Group Policy Management (tutti i domini) </strong> nel modello amministrativo. Se l'ambiente richiede solo un singolo server Advanced Group Policy Management, usare solo l' <strong> impostazione server Advanced Group Policy Management (tutti i domini) </strong> nel modello amministrativo.</p>
<p>Se disabilitata o non configurata, l' <strong> impostazione del server Advanced Group Policy Management (tutti i domini) </strong> nel modello amministrativo configura la connessione al server Advanced Group Policy Management.</p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

-   [Impostazioni del modello amministrativo](administrative-template-settings.md)

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks.md)

 

 





