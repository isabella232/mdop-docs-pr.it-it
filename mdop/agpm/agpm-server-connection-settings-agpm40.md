---
title: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
description: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: cc67f122-6309-4820-92c2-f6a27d897123
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55bd5c04f573a421674068bea6fc9c6adcd29a12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804522"
---
# Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo


È possibile usare le impostazioni dei modelli amministrativi per la gestione avanzata dei criteri di gruppo per configurare centralmente le connessioni del server Advanced Group Policy Management per gli amministratori dei criteri di gruppo a cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.

Le impostazioni seguenti sono disponibili in utenti Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM durante la modifica di un oggetto Criteri di gruppo.

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
<td align="left"><p><strong>Advanced Group Policy Management: specificare il server Advanced Group Policy Management (tutti i domini)</strong></p></td>
<td align="left"><p>Questa impostazione dei criteri consente di specificare un server Advanced Group Policy Management per tutti i domini. Viene usato solo dai client Advanced Group Policy Management e limita gli amministratori dei criteri di gruppo a connettersi a un altro archivio. Puoi eseguire l'override di questo valore predefinito per singoli domini usando <strong> Advanced Group Policy Management: specificare l'impostazione dei server Advanced Group Policy </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Advanced Group Policy Management: specificare server Advanced Group Policy</strong></p></td>
<td align="left"><p>Questa impostazione dei criteri consente di specificare i server Advanced Group Policy Management per singoli domini. Viene usato solo dai client Advanced Group Policy Management e limita gli amministratori dei criteri di gruppo a connettersi a un altro archivio per il dominio specificato. Per specificare un server Advanced Group Policy Management predefinito, usare <strong> Advanced Group Policy Management: specificare l'impostazione predefinita del server Advanced Group Policy Management (tutti i domini) </strong> e usare questa impostazione per ignorare il valore predefinito in base al dominio.</p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

-   [Cartella dei modelli amministrativi](administrative-templates-folder-agpm40.md)

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks-agpm40.md)

 

 





