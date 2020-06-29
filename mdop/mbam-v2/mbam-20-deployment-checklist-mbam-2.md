---
title: Elenco di controllo per la distribuzione di MBAM 2.0
description: Elenco di controllo per la distribuzione di MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826436"
---
# Elenco di controllo per la distribuzione di MBAM 2.0


Questo elenco di controllo può essere usato per facilitare la distribuzione di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker con una topologia autonoma.

**Nota**  
Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da tenere in considerazione durante la distribuzione delle funzionalità di amministrazione e monitoraggio di Microsoft BitLocker. È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Attività</th>
<th align="left">Riferimenti</th>
<th align="left">Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Completare la fase di pianificazione per preparare l'ambiente di calcolo per la distribuzione di MBAM.</p></td>
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)">Elenco di controllo per la pianificazione di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione delle funzionalità di MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configurazioni supportate di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Eseguire la configurazione di MBAM per distribuire le caratteristiche del server MBAM nell'ordine seguente:</p>
<ol>
<li><p>Database di ripristino</p></li>
<li><p>Database di conformità e controllo</p></li>
<li><p>Audit e report di conformità</p></li>
<li><p>Server self-service</p></li>
<li><p>Server di amministrazione e monitoraggio</p></li>
<li><p>Modello di criteri di gruppo di MBAM</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Tenere traccia dei nomi dei server in cui è installata ogni funzionalità. Queste informazioni verranno usate durante il processo di installazione.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)">Distribuzione dell'infrastruttura server di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Aggiungere gruppi di sicurezza di servizi di dominio Active Directory creati durante la fase di pianificazione per i gruppi di amministratori locali appropriati di MBAM server nei server appropriati.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Pianificazione per i ruoli di amministratore di MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> come gestire i ruoli di amministratore di mbam</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Distribuire il software del client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Distribuzione del client MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Distribuzione di MBAM 2.0](deploying-mbam-20-mbam-2.md)









