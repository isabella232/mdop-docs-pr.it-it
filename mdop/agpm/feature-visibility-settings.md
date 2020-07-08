---
title: Impostazioni di visibilità delle funzionalità
description: Impostazioni di visibilità delle funzionalità
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820806"
---
# Impostazioni di visibilità delle funzionalità


Le impostazioni del modello amministrativo per gestione avanzata Criteri di gruppo consentono di configurare centralmente la visibilità del nodo di **controllo delle modifiche** e della scheda **cronologia** per gli amministratori dei criteri di gruppo a cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.

Le impostazioni seguenti sono disponibili in utenti Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console \ \ Restricted/consentiti degli snap-in Snap-ins\\Extension nell' **Editor oggetti Criteri di gruppo** durante la modifica di un oggetto Criteri di gruppo in console Gestione criteri di raggruppamento. Se il percorso non è visibile, fare clic con il pulsante destro del mouse su **modelli amministrativi**e quindi aggiungere il modello Advanced Group Policy Management. admx o Advanced Group Policy Management.

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
<td align="left"><p><strong>Controllo delle modifiche per Advanced Group Policy</strong></p></td>
<td align="left"><p>Se abilitato o non configurato, il <strong> nodo cambia controllo </strong> è visibile in GPMC.</p>
<p>Se disabilitato, il <strong> nodo cambia controllo </strong> non è visibile in GPMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estensione del collegamento Advanced Group Policy</strong></p></td>
<td align="left"><p>Se abilitata o non configurata, <strong> </strong> nella GPMC per ogni GPO collegato viene visualizzata una scheda cronologia.</p>
<p>Se disabilitata, <strong> la </strong> scheda cronologia non è visibile per i GPO collegati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Estensione GPO in Advanced Group Policy</strong></p></td>
<td align="left"><p>Se abilitata o non configurata, <strong> </strong> nella GPMC per ogni GPO viene visualizzata una scheda cronologia.</p>
<p>Se disabilitata, <strong> la </strong> scheda cronologia non è visibile per gli oggetti Criteri di ricerca.</p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

-   [Impostazioni del modello amministrativo](administrative-template-settings.md)

 

 





