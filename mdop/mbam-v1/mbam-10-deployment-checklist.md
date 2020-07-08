---
title: Elenco di controllo per la distribuzione di MBAM 1.0
description: Elenco di controllo per la distribuzione di MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804300"
---
# Elenco di controllo per la distribuzione di MBAM 1.0


Questo elenco di controllo è progettato per facilitare la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM).

**Nota**  
Questo elenco di controllo illustra la procedura consigliata e fornisce un elenco di elementi di alto livello da considerare quando si distribuiscono le caratteristiche di MBAM. È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo in base alle specifiche esigenze.



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
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)">Elenco di controllo per la pianificazione di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione delle funzionalità di MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configurazioni supportate di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Eseguire la configurazione di MBAM per distribuire le caratteristiche del server MBAM nell'ordine seguente:</p>
<ol>
<li><p>Database di ripristino e hardware</p></li>
<li><p>Database di stato conformità</p></li>
<li><p>Audit e report di conformità</p></li>
<li><p>Server di amministrazione e monitoraggio</p></li>
<li><p>Modello di criteri di gruppo di MBAM</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Tenere traccia dei nomi dei server in cui è installata ogni funzionalità. Si utilizzeranno queste informazioni durante il processo di installazione.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)">Distribuzione dell'infrastruttura server di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Aggiungere gruppi di sicurezza di servizi di dominio Active Directory creati durante la fase di pianificazione per i gruppi di amministratori locali appropriati di MBAM server nei server appropriati.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Pianificazione per i ruoli di amministratore di MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> come gestire i ruoli di amministratore di mbam</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Distribuire il software del client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Distribuzione del client MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Distribuzione di MBAM 1.0](deploying-mbam-10.md)









