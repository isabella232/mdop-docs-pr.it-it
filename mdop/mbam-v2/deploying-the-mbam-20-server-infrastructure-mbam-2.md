---
title: Distribuzione dell'infrastruttura server di MBAM 2.0
description: Distribuzione dell'infrastruttura server di MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8aee322b9a1aacbf98ff8362e95e21c2dd3d289a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910801"
---
# <a name="deploying-the-mbam-20-server-infrastructure"></a>Distribuzione dell'infrastruttura server di MBAM 2.0


Le funzionalità di Microsoft BitLocker Administration and Monitoring (MBAM) Server per la topologia autonoma possono essere installate in configurazioni diverse in due o più server in un ambiente di produzione. La configurazione consigliata è due server per un ambiente di produzione, a seconda dei requisiti di scalabilità. Utilizzare un singolo server per un'installazione di MBAM solo in ambienti di test. Per ulteriori informazioni sulla pianificazione della distribuzione delle funzionalità del server MBAM, vedere [Planning for MBAM 2.0 Server Deployment.](planning-for-mbam-20-server-deployment-mbam-2.md)

Nel diagramma seguente viene illustrato un esempio di come configurare la distribuzione MBAM a due server consigliata. Questa configurazione supporta fino a 200.000 client MBAM in un ambiente di produzione. Le funzionalità e i database del server nell'immagine dell'architettura sono descritti nella sezione seguente e sono elencati nel computer o nel server in cui è consigliabile installarli.

![Topologia di distribuzione a due server mbam 2.](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>Amministrazione e Monitoring Server


Nel server sono installate le funzionalità seguenti:

-   **Amministrazione e Monitoring Server**. La funzionalità Amministrazione e Monitoring Server viene installata in un server Windows ed è costituita dal sito Web Help Desk e dai servizi Web di monitoraggio.

-   **Portale self-service**. Il Self-Service Portal è installato in un server Windows server. Il Self-Service Portal consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web, dove possono ottenere una chiave di ripristino per ripristinare un volume BitLocker bloccato.

## <a name="database-server"></a>Database Server


Nel server sono installate le funzionalità seguenti:

-   **Database di ripristino**. Il database di ripristino viene installato in un server Windows e in un'istanza supportata di Microsoft SQL Server. In questo database vengono archiviati i dati di ripristino raccolti dai computer client MBAM.

-   **Database di conformità e controllo**. Il database di conformità e controllo viene installato in un server Windows e in un'istanza supportata di SQL Server. Questo database archivia i dati di conformità per i computer client MBAM. Questi dati vengono utilizzati principalmente per i report SQL Server Reporting Services (SSRS).

-   **Report di conformità e di controllo**. I report di conformità e controllo vengono installati in un server Windows e in un'istanza supportata di SQL Server in cui è installata la funzionalità SQL Server Reporting Services (SSRS). Questi report forniscono report MBAM a cui è possibile accedere dal sito Web Help Desk o direttamente dal server SSRS.

## <a name="management-workstation"></a>Workstation di gestione


La funzionalità seguente viene installata nella workstation di gestione, che può essere un server Windows o un computer client.

-   **Modello di criteri**. Il modello di criteri è costituito da Criteri di gruppo che definiscono le impostazioni di implementazione mbam per la crittografia dell'unità BitLocker. È possibile installare il modello di criteri in qualsiasi server o workstation, ma in genere è installato in una workstation di gestione, che è un server o un computer client Windows supportati. La workstation non deve essere un computer dedicato.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> MBAM Client


Il client MBAM viene installato in un computer Windows e presenta le caratteristiche seguenti:

-   Usa Criteri di gruppo per applicare la crittografia dell'unità BitLocker dei computer client nell'organizzazione.

-   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

-   Raccoglie i dati di conformità per il computer e li passa al sistema di report.

## <a name="other-resources-for-deploying-mbam-20-server-features"></a>Altre risorse per la distribuzione delle funzionalità del server MBAM 2.0


[Distribuzione di MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





