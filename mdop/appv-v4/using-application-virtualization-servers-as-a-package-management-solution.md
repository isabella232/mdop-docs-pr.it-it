---
title: Uso di Application Virtualization Server come soluzione per la gestione dei pacchetti
description: Uso di Application Virtualization Server come soluzione per la gestione dei pacchetti
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815125"
---
# Uso di Application Virtualization Server come soluzione per la gestione dei pacchetti


Se non si dispone di un sistema ESD esistente per distribuire la soluzione di virtualizzazione dell'applicazione o non si vuole usarla, sarà necessario installare uno o più server di gestione della virtualizzazione delle applicazioni come nucleo dell'architettura di sistema. L'Application Virtualization Management Server richiede un computer server dedicato e necessita di un database di Microsoft SQL Server. Il database può essere nello stesso server oppure può essere configurato in un server di database aziendale accessibile per l'Application Virtualization Management Server tramite una connessione LAN ad alta velocità. Inoltre, è necessario installare Microsoft Application Virtualization Management Console, sia nell'Application Virtualization Management Server che in una workstation di gestione designata, e sarà necessario installare il servizio Web Microsoft Application Virtualization Management, che può essere installato anche nel server di gestione della virtualizzazione dell'applicazione o in un server IIS separato. L'Application Virtualization Management Console viene usato per la connessione al servizio Web Application Virtualization Management, che consente all'amministratore di sistema di interagire con l'Application Virtualization Management Server.

**Nota**  L'accesso alle applicazioni viene controllato tramite gruppi di sicurezza in servizi di dominio Active Directory, quindi sarà necessario pianificare un processo per configurare un gruppo di sicurezza per ogni applicazione virtualizzata e per la gestione degli utenti aggiunti a ogni gruppo. L'amministratore di Application Virtualization Management Server configura il server per l'uso di questi gruppi di Active Directory e il server controlla automaticamente l'accesso ai pacchetti in base all'appartenenza ai gruppi di Active Directory.

 

## In questa sezione


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[Panoramica dei componenti del sistema Application Virtualization](overview-of-the-application-virtualization-system-components.md)  
Elenca e descrive i componenti principali di Microsoft Application Virtualization Management System.

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
Viene fornita una breve panoramica del modo in cui vengono pubblicate le applicazioni virtuali in uno scenario di distribuzione basato su server Application Virtualization.

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
Descrive le opzioni disponibili per l'uso dei server di streaming Application Virtualization in combinazione con l'implementazione basata su Application Virtualization Management Server.

## Argomenti correlati


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Pianificazione della distribuzione del sistema Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 





