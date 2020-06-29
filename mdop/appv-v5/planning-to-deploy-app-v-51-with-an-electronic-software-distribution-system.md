---
title: Pianificazione della distribuzione di App-V 5.1 con un sistema di distribuzione elettronica del software
description: Pianificazione della distribuzione di App-V 5.1 con un sistema di distribuzione elettronica del software
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804948"
---
# Pianificazione della distribuzione di App-V 5.1 con un sistema di distribuzione elettronica del software


Se si usa un sistema di distribuzione del software elettronico per distribuire pacchetti App-V, vedere le considerazioni seguenti sulla pianificazione. Per informazioni sull'uso di System Center Configuration Manager per distribuire App-V, vedere [Introduzione alla gestione delle applicazioni in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).

Esaminare le opzioni di requisiti per il componente e l'architettura seguenti che si applicano quando si usa un ESD per distribuire pacchetti App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisito o opzione di distribuzione</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V Management Server, database di gestione e server di pubblicazione non sono obbligatori.</p></td>
<td align="left"><p>Queste funzioni vengono gestite dalla soluzione ESD implementata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Puoi distribuire l'App-V Reporting Server e il database di report affiancati all'ESD.</p></td>
<td align="left"><p>La distribuzione affiancata consente di raccogliere dati e generare report.</p>
<p>Se si Abilita il client App-V per inviare informazioni sul report e non si usa l'App-V Reporting Server, i dati dei report vengono archiviati nei file XML associati.</p></td>
</tr>
</tbody>
</table>

 






## Argomenti correlati


[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

 

 





