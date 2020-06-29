---
title: Come applicare le impostazioni di rete a un'area di lavoro MED-V
description: Come applicare le impostazioni di rete a un'area di lavoro MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826516"
---
# Come applicare le impostazioni di rete a un'area di lavoro MED-V


Gli amministratori possono definire le impostazioni di rete per ogni area di lavoro MED-V.

Tutte le impostazioni di rete sono configurate nel modulo **criteri** , nella scheda **rete** .

**Per applicare le impostazioni di rete a un'area di lavoro MED-V**

1.  Fare clic sull'area di lavoro MED-V per configurare.

2.  Nel riquadro **rete** configurare le impostazioni come descritto nella tabella seguente.

3.  Nel menu **criteri** selezionare **commit**.

**Proprietà di rete dell'area di lavoro MED-V**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Proprietà TCP/IP</p></td>
<td align="left"><ul>
<li><p><strong>Usa l'indirizzo IP dell'host (NAT) </strong> : l'area di lavoro utilizzerà NAT per condividere l'IP dell'host per il traffico in uscita.</p></li>
<li><p><strong>Usare un indirizzo IP diverso da host (Bridge) </strong> : l'area di lavoro MED-V avrà un proprio indirizzo di rete, in genere ottenuto tramite DHCP.</p></li>
</ul>
<p>Selezionare la <strong> casella di controllo associa più adattatori all'area </strong> di lavoro quando nel computer host sono presenti più adapter. È consigliabile usare questa configurazione quando l'host si sposta tra reti diverse usando diversi adapter.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Server DNS</p></td>
<td align="left"><ul>
<li><p><strong>Non modificare </strong> : le impostazioni DNS impostate nella macchina virtuale dell'area di lavoro MED-V non verranno modificate.</p></li>
<li><p><strong>Usare l'indirizzo DNS dell'host </strong> : le impostazioni DNS dell'area di lavoro MED-V verranno sincronizzate in modo che corrispondano alle impostazioni dell'host. La sincronizzazione DNS è dinamica. Viene sincronizzata periodicamente con l'host in modo che, se è stata modificata nell'host, cambierà in modo dinamico nell'area di lavoro MED-V.</p></li>
<li><p><strong>Usare indirizzi DNS specifici </strong> : l'area di lavoro MED-V utilizzerà un DNS specifico, come specificato.</p>
<p>Nei <strong> campi primari </strong> e <strong> secondari </strong> immettere gli indirizzi DNS primari e secondari.</p>
<p>Selezionare la <strong> casella di controllo Accoda indirizzi DNS dell'host </strong> per aggiungere l'host agli indirizzi DNS configurati.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Assegnare suffissi DNS</p></td>
<td align="left"><ul>
<li><p><strong>Assegnare i suffissi seguenti </strong> : selezionare questa casella di controllo per assegnare specifici suffissi DNS; nella casella Immettere un suffisso o più suffissi separati da virgole.</p></li>
<li><p><strong>Accoda suffissi host </strong> : selezionare questa casella di controllo per accodare i suffissi dell'host all'indirizzo DNS.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

 

 





