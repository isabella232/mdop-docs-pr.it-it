---
title: Configurazione dei gruppi di prerequisiti in Active Directory per App-V
description: Configurazione dei gruppi di prerequisiti in Active Directory per App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821865"
---
# Configurazione dei gruppi di prerequisiti in Active Directory per App-V


Prima di installare il server di gestione di Microsoft Application Virtualization (App-V), è necessario creare gli oggetti seguenti in Active Directory. App-V usa i gruppi di Active Directory per controllare l'accesso alle applicazioni e alle funzioni amministrative. Si utilizzeranno questi gruppi durante il processo di installazione del server e quando si pubblicano le applicazioni.

## Configurazione dei gruppi prerequisiti in Active Directory per la virtualizzazione delle applicazioni


Questa tabella elenca i gruppi di Active Directory necessari per l'installazione di App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Oggetto</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Unità organizzativa (OU)</p></td>
<td align="left"><p>Creare un'unità organizzativa in Active Directory per i gruppi specifici necessari per App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gruppo amministrativo App-V</p></td>
<td align="left"><p>Durante l'installazione di App-V Management Server devi selezionare un gruppo di Active Directory da usare come gruppo amministratori di App-V per controllare l'accesso amministrativo alla console di gestione. Creare un gruppo di sicurezza per gli amministratori di App-V e aggiungere a questo gruppo ogni utente che deve usare la console di gestione. Non è possibile creare questo gruppo direttamente dal programma di installazione di App-V Management Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gruppo utenti App-V</p></td>
<td align="left"><p>App-V richiede che ogni account utente che accede alle funzioni App-V sia membro di un criterio di provider associato a un singolo gruppo per l'accesso alla piattaforma generale. Usare un gruppo esistente; ad esempio, gli utenti di dominio, se tutti gli utenti devono avere accesso a App-V o creare un nuovo gruppo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gruppi di applicazioni</p></td>
<td align="left"><p>App-V associa il diritto di usare una singola applicazione con un gruppo di Active Directory. Crea un gruppo di Active Directory per ogni applicazione e assegna gli utenti a questi gruppi in base alle esigenze per controllare l'accesso degli utenti alle applicazioni.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Requisiti per la distribuzione di Application Virtualization](application-virtualization-deployment-requirements.md)

[Come configurare Windows Server 2008 per i server di gestione di App-V](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





