---
title: Elenco di controllo pre-installazione di App-V
description: Elenco di controllo pre-installazione di App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819786"
---
# Elenco di controllo pre-installazione di App-V


L'elenco di controllo seguente ha lo scopo di specificare un alto livello di elementi da tenere in considerazione e illustrare i passaggi da eseguire prima di installare i server di Microsoft Application Virtualization (App-V).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Riferimento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Verificare che l'ambiente di elaborazione soddisfi le configurazioni supportate necessarie per App-V.</p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)">Requisiti per la distribuzione di Application Virtualization</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare i gruppi e gli account di Active Directory necessari.</p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)">Configurazione dei gruppi di prerequisiti in Active Directory per App-V</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare le impostazioni di Internet Information Services (IIS) nel server in cui è in uso IIS.</p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)">Come configurare Windows Server 2008 per i server di gestione di App-V</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare il server che utilizza IIS per essere considerato attendibile per la delega.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa operazione è necessaria solo se si sta installando App-V Management Server utilizzando un'architettura di sistema distribuita, ovvero se si installa App-V Management Console, il servizio Web di gestione e il database in computer diversi.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)">Come configurare il server in modo che sia attendibile per la delega</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare Microsoft SQL Server 2008.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)">Installare SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Elenchi di controllo per la distribuzione e l'aggiornamento di Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

[Elenco di controllo installazione di App-V](app-v-installation-checklist.md)









