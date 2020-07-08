---
title: Pianificazione della distribuzione del server di MBAM 1.0
description: Pianificazione della distribuzione del server di MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804221"
---
# Pianificazione della distribuzione del server di MBAM 1.0


L'infrastruttura del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione.

## Pianificazione della distribuzione di MBAM server


Le caratteristiche di MBAM seguenti rappresentano l'infrastruttura server per una distribuzione di MBAM server:

-   Database di ripristino e hardware

-   Database di conformità e controllo

-   Report di conformità e controllo

-   Server di amministrazione e monitoraggio

I database e le funzionalità di MBAM server possono essere installati in configurazioni diverse, a seconda delle esigenze di scalabilità. Tutte le funzionalità di MBAM server possono essere installate in un singolo server o distribuite in più server. In generale, ti consigliamo di usare una configurazione a tre server o a cinque server per gli ambienti di produzione, anche se possono essere usate anche configurazioni di due o quattro server, a seconda delle esigenze di calcolo.

**Nota**  Per altre informazioni sulla scalabilità delle prestazioni di MBAM e delle topologie di distribuzione consigliate, vedere la scalabilità di MBAM e l'elevata disponibilità della Guida white paper at <https://go.microsoft.com/fwlink/p/?LinkId=258314> .

 

Ogni funzionalità di MBAM contiene prerequisiti specifici. Per un elenco completo dei prerequisiti di funzionalità del server e i requisiti hardware e software, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md) e le [configurazioni supportate di MBAM 1,0](mbam-10-supported-configurations.md).

Oltre alle funzionalità di MBAM correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM. Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.

## Ordine di distribuzione delle funzionalità di MBAM server


Quando si distribuiscono le funzionalità di MBAM server, installare le funzionalità nell'ordine seguente:

1.  Database di ripristino e hardware

2.  Database di conformità e controllo

3.  Audit e report di conformità

4.  Server di amministrazione e monitoraggio

5.  Modello di criteri

**Nota**  Tenere traccia dei nomi dei computer in cui si installano le singole funzionalità. Si utilizzeranno queste informazioni durante il processo di installazione. Puoi stampare e usare un elenco di controllo della distribuzione per assisterti nel processo di installazione. Per altre informazioni sull'elenco di controllo della distribuzione di MBAM, vedere [elenco di controllo della distribuzione di mbam 1,0](mbam-10-deployment-checklist.md).

 

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 1.0](planning-to-deploy-mbam-10.md)

[Distribuzione dell'infrastruttura server di MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





