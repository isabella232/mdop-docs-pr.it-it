---
title: Architettura di alto livello per MBAM 1.0
description: Architettura di alto livello per MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d06c7bd801a9dd63916d310af75e88a307e7226a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910411"
---
# <a name="high-level-architecture-for-mbam-10"></a>Architettura di alto livello per MBAM 1.0


Microsoft BitLocker Administration and Monitoring (MBAM) è una soluzione di crittografia dei dati client/server che consente di semplificare il provisioning e la distribuzione di BitLocker, migliorare la conformità e la creazione di report di BitLocker e ridurre i costi di supporto. MBAM include le funzionalità descritte in questo argomento.

Inoltre, è disponibile un video che fornisce una panoramica dell'architettura MBAM e dell'installazione di MBAM. Per ulteriori informazioni, vedere [MbAM Deployment and Architecture Overview](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## <a name="architecture-overview"></a>Panoramica dell'architettura


Nel diagramma seguente viene visualizzata l'architettura MBAM. La topologia di distribuzione MBAM a server singolo viene illustrata per introdurre le funzionalità di MBAM. Tuttavia, questa topologia di distribuzione di MBAM è consigliata solo per gli ambienti lab.

**Nota**  
Per una distribuzione di produzione è consigliata almeno una topologia di distribuzione MBAM con tre computer. Per ulteriori informazioni sulle topologie di distribuzione mbam, vedere [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).

 

![Topologia di distribuzione a server singolo mbam.](images/mbam-1-server.jpg)

1.  **Amministrazione e Monitoring Server**. MbAM Administration and Monitoring Server viene installato in un server Windows e ospita il sito Web Amministrazione e gestione MBAM e i servizi Web di monitoraggio. Il sito Web Amministrazione e gestione MBAM viene utilizzato per determinare lo stato di conformità aziendale, controllare l'attività, gestire le funzionalità hardware e accedere ai dati di ripristino, ad esempio le chiavi di ripristino di BitLocker. Administration e Monitoring Server si connettono ai database e ai servizi seguenti:

    -   Ripristino e database hardware. Il database di ripristino e hardware viene installato in un server Windows e supportato SQL Server'istanza. In questo database vengono archiviati i dati di ripristino e le informazioni hardware raccolti dai computer client MBAM.

    -   Database di conformità e controllo. Il database di conformità e controllo viene installato in un server Windows e supportato SQL Server istanza. Questo database archivia i dati di conformità per i computer client MBAM. Questi dati vengono utilizzati principalmente per i report ospitati da SQL Server Reporting Services (SSRS).

    -   Report di conformità e di controllo. I report di conformità e di controllo vengono installati in un server Windows e sono supportati SQL Server'istanza in cui è installata la funzionalità SSRS. Questi report forniscono i report di amministrazione e monitoraggio di Microsoft BitLocker. È possibile accedere a questi report dal sito Web Di amministrazione e gestione di MBAM o direttamente dal server SSRS.

2.  **MbAM Client**. Microsoft BitLocker Administration and Monitoring Client esegue le attività seguenti:

    -   Usa Criteri di gruppo per applicare la crittografia BitLocker dei computer client nell'organizzazione.

    -   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

    -   Raccoglie informazioni di ripristino e informazioni hardware sui computer client.

    -   Raccoglie i dati di conformità per il computer e li passa al sistema di report.

3.  **Modello di criteri**. Il modello Criteri di gruppo MBAM viene installato in un server Windows o un computer client basato su Windows. Questo modello viene usato per specificare le impostazioni di implementazione MBAM per la crittografia dell'unità BitLocker.

## <a name="related-topics"></a>Argomenti correlati


[Attività iniziali di MBAM 1.0](getting-started-with-mbam-10.md)

 

 





