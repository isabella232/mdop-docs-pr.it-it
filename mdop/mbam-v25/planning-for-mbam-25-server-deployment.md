---
title: Pianificazione della distribuzione del server di MBAM 2.5
description: Pianificazione della distribuzione del server di MBAM 2.5
author: dansimp
ms.assetid: 88774c89-31c8-4eb8-a845-a00bbec8c870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2ecb510fab821118ce210577f9ffb83c39be050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826215"
---
# Pianificazione della distribuzione del server di MBAM 2.5


Questo argomento elenca le caratteristiche che vengono distribuite per le topologie di MBAM autonomo e di gestione configurazione ed elenca l'ordine in cui è necessario distribuirle. Esiste una configurazione consigliata per ogni topologia. Tuttavia, è possibile configurare i database e le funzionalità di MBAM server in diverse configurazioni e in più server, a seconda dei requisiti di scalabilità.

## Considerazioni importanti sulla pianificazione per entrambe le topologie


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Considerazioni</th>
<th align="left">Dettagli o finalità</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Prima di avviare la distribuzione, vedere la seguente procedura:</p>
<ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></li>
</ul></td>
<td align="left"><p>Ogni caratteristica MBAM ha prerequisiti specifici che devono essere soddisfatti prima di avviare l'installazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Le chiavi di ripristino di BitLocker in MBAM scadono dopo un uso singolo.</p></td>
<td align="left"><p>Un uso singolo indica che la chiave di ripristino è stata recuperata tramite il sito Web di amministrazione e monitoraggio (noto anche come Help desk), portale self-service o usando il <strong> cmdlet Get-MbamBitLockerRecoveryKey di </strong> Windows PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tenere traccia dei nomi dei computer in cui si configura ogni funzionalità. Userai queste informazioni durante il processo di configurazione.</p></td>
<td align="left"><p>Per questo scopo, è consigliabile usare l' <a href="mbam-25-deployment-checklist.md" data-raw-source="[MBAM 2.5 Deployment Checklist](mbam-25-deployment-checklist.md)"> elenco di controllo della distribuzione di MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare solo le impostazioni di criteri di gruppo nel nodo MDOP MBAM (BitLocker Management). Non modificare le impostazioni dei criteri di gruppo nel nodo crittografia unità BitLocker.</p></td>
<td align="left"><p>Se si modificano le impostazioni dei criteri di gruppo nel nodo crittografia unità BitLocker, MBAM non funzionerà.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="planning-for-mbam-server-deployment---stand-alone-topology"></a>Pianificazione per la distribuzione di MBAM server-topologia autonoma


Per la topologia autonoma è consigliabile usare una configurazione a due server per gli ambienti di produzione, anche se possono essere usate configurazioni da tre a quattro server.

L'infrastruttura server per la topologia autonoma di MBAM contiene le caratteristiche seguenti, che devono essere configurate nell'ordine indicato:

1.  Database (database di conformità e database di controllo e ripristino)

2.  Rapporti

3.  Applicazioni Web (e relativi servizi Web)

    -   Sito Web di amministrazione e monitoraggio

    -   Portale self-service

Per una descrizione di queste funzionalità, Vedi l' [architettura di alto livello di MBAM 2,5 con topologia autonoma](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

## <a href="" id="planning-for-mbam-server-deployment---configuration-manager-topology"></a>Pianificazione per la distribuzione di MBAM server-topologia di Configuration Manager


Per la topologia di integrazione di Configuration Manager, è consigliabile una configurazione a tre server per gli ambienti di produzione, anche se è possibile usare configurazioni di server aggiuntivi.

L'infrastruttura server per la topologia di MBAM Configuration Manager contiene le caratteristiche seguenti, che devono essere configurate o eseguite nell'ordine indicato:

1.  Database (database di conformità e database di controllo e ripristino)

2.  Rapporti

3.  Applicazioni Web (e relativi servizi Web)

    -   Sito Web di amministrazione e monitoraggio

    -   Portale self-service

4.  Integrazione di System Center Configuration Manager

Per una descrizione di queste funzionalità, Vedi l' [architettura di alto livello di MBAM 2,5 con la topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).



## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)

[Distribuzione dell'infrastruttura server di MBAM 2.5](deploying-the-mbam-25-server-infrastructure.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





