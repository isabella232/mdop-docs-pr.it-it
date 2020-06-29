---
title: Pianificazione della distribuzione del server di MBAM 2.0
description: Pianificazione della distribuzione del server di MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804359"
---
# Pianificazione della distribuzione del server di MBAM 2.0


L'infrastruttura del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione. Se si sta installando l'amministrazione e il monitoraggio di Microsoft BitLocker con la topologia di Configuration Manager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

**Nota**  Le installazioni di amministrazione e monitoraggio di Microsoft BitLocker in un singolo server sono consigliate solo per gli ambienti di test.

 

## Pianificazione della distribuzione di MBAM server


L'infrastruttura per una distribuzione di MBAM Server include le caratteristiche seguenti:

-   Database di ripristino

-   Database di conformità e controllo

-   Report di conformità e controllo

-   Portale self-service

-   Server di amministrazione e monitoraggio

-   Modello di criteri di gruppo di MBAM

I database e le funzionalità di MBAM server possono essere installati in configurazioni diverse, a seconda dei requisiti di scalabilità. Tutte le funzionalità di MBAM server possono essere installate in un singolo server o distribuite in più server. È consigliabile usare una configurazione a due server per gli ambienti di produzione, anche se possono essere usate anche configurazioni da due a quattro server, a seconda dei requisiti di calcolo.

Ogni funzionalità di MBAM contiene prerequisiti specifici. Per un elenco completo dei prerequisiti di funzionalità del server e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md) e le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).

Oltre alle funzionalità di MBAM correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM. Il modello contiene le impostazioni degli oggetti Criteri di gruppo (GPO) che vengono configurate per gestire la crittografia unità BitLocker nell'organizzazione. Questo modello può essere installato in qualsiasi computer che può eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.

Man mano che pianifichi la distribuzione di MBAM server, tieni presente che le chiavi di ripristino di BitLocker in MBAM sono destinate solo all'uso singolo, dopodiché scadono i tasti di ripristino. Affinché le chiavi scadano dopo l'uso, devono essere recuperate tramite il portale help desk o il portale self-service.

## Ordine di distribuzione delle funzionalità di MBAM server


Per distribuire le caratteristiche di MBAM in più server, è necessario installare le funzionalità nell'ordine seguente:

1.  Database di ripristino

2.  Database di conformità e controllo

3.  Audit e report di conformità

4.  Portale self-service

5.  Server di amministrazione e monitoraggio

6.  Modello di criteri di gruppo di MBAM

**Nota**  Tenere traccia dei nomi dei computer in cui si installano le singole funzionalità. È necessario usare queste informazioni durante il processo di installazione. È possibile stampare e usare un elenco di controllo della distribuzione per facilitare questo sforzo. Per altre informazioni sull'elenco di controllo della distribuzione di MBAM, vedere [elenco di controllo della distribuzione di mbam 2,0](mbam-20-deployment-checklist-mbam-2.md).

 

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Distribuzione dell'infrastruttura server di MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





