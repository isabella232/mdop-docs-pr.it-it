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
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825236"
---
# Architettura di alto livello per MBAM 1.0


Microsoft BitLocker Administration and Monitoring (MBAM) è una soluzione per la crittografia dei dati client/server che consente di semplificare il provisioning e la distribuzione di BitLocker, migliorare la conformità e la creazione di report di BitLocker e ridurre i costi di supporto. MBAM include le caratteristiche descritte in questo argomento.

Inoltre, c'è un video che fornisce una panoramica dell'architettura MBAM e la configurazione di MBAM. Per altre informazioni, Vedi [Panoramica della distribuzione e dell'architettura di mbam](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## Panoramica dell'architettura


Il diagramma seguente mostra l'architettura MBAM. La topologia di distribuzione di MBAM a server singolo viene visualizzata per introdurre le caratteristiche di MBAM. Tuttavia, questa topologia di distribuzione di MBAM è consigliata solo per gli ambienti Lab.

**Nota**  È consigliabile almeno una topologia di distribuzione di MBAM con tre computer per una distribuzione di produzione. Per altre informazioni sulle topologie di distribuzione di MBAM, vedere [distribuzione dell'infrastruttura del server mbam 1,0](deploying-the-mbam-10-server-infrastructure.md).

 

![una topologia di distribuzione di mbam Single Server](images/mbam-1-server.jpg)

1.  **Server di amministrazione e monitoraggio**. Il server di amministrazione e monitoraggio di MBAM è installato in un server Windows e ospita il sito Web di amministrazione e gestione di MBAM e i servizi Web di monitoraggio. Il sito Web amministrazione e gestione di MBAM viene usato per determinare lo stato di conformità dell'organizzazione, per controllare le attività, per gestire le funzionalità hardware e per accedere ai dati di ripristino, ad esempio le chiavi di ripristino di BitLocker. Il server di amministrazione e monitoraggio si connette ai database e ai servizi seguenti:

    -   Database di ripristino e hardware. Il database di ripristino e hardware viene installato in un server basato su Windows e supporta l'istanza SQLServer. Questo database archivia i dati di ripristino e le informazioni hardware raccolte dai computer client di MBAM.

    -   Database di conformità e controllo. Il database di conformità e controllo viene installato in un server Windows e nell'istanza di SQLServer supportata. Questo database archivia i dati di conformità per i computer client MBAM. Questi dati vengono usati principalmente per i report ospitati da SQL Server Reporting Services (SSRS).

    -   Report di conformità e controllo. I report di conformità e controllo sono installati in un server basato su Windows e sono supportate istanze di SQLServer in cui è installata la funzionalità SSRS. Questi report includono i report di amministrazione e monitoraggio di Microsoft BitLocker. Questi report sono accessibili dal sito Web di amministrazione e gestione di MBAM o direttamente dal server SSRS.

2.  **Client mbam**. Il client di amministrazione e monitoraggio di Microsoft BitLocker esegue le attività seguenti:

    -   Usa criteri di gruppo per applicare la crittografia BitLocker dei computer client nell'organizzazione.

    -   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità USB (removibile Data).

    -   Raccoglie informazioni di ripristino e informazioni hardware sui computer client.

    -   Raccoglie i dati di conformità per il computer e passa i dati al sistema di creazione di report.

3.  **Modello di criteri**. Il modello di criteri di gruppo di MBAM viene installato in un server Windows o un computer client supportato. Questo modello viene usato per specificare le impostazioni di implementazione di MBAM per la crittografia unità BitLocker.

## Argomenti correlati


[Attività iniziali di MBAM 1.0](getting-started-with-mbam-10.md)

 

 





