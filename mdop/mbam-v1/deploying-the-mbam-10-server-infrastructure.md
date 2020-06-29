---
title: Distribuzione dell'infrastruttura server di MBAM 1.0
description: Distribuzione dell'infrastruttura server di MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825176"
---
# Distribuzione dell'infrastruttura server di MBAM 1.0


È possibile installare le caratteristiche del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker in diverse configurazioni usando uno-cinque server. In genere, è consigliabile usare una configurazione di tre-cinque server per gli ambienti di produzione, a seconda delle esigenze di scalabilità. Per altre informazioni sulla scalabilità delle prestazioni di MBAM e delle topologie di distribuzione consigliate, vedere la [scalabilità di mbam e la Guida di alta disponibilità di white paper](https://go.microsoft.com/fwlink/p/?LinkId=258314).

## Distribuire tutti i MBAM 1,0 su un singolo server


In questa configurazione tutte le funzionalità di MBAM sono installate in un singolo server. Questa topologia di distribuzione per MBAM Server Infrastructure supporta fino a 21.000 computer client MBAM.

**Importante**  Questa configurazione è supportata, ma è consigliabile solo per i test.

 

Le procedure descritte in questa sezione descrivono l'installazione completa delle funzionalità di MBAM in un singolo server.

[Come installare e configurare MBAM in un server singolo](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## Distribuire MBAM 1,0 nei server distribuiti


Le funzionalità di MBAM possono essere installate in diverse configurazioni, a seconda delle esigenze di scalabilità. Per altre informazioni su come pianificare la distribuzione delle funzionalità di MBAM server, vedere [pianificazione della distribuzione di mbam 1,0 Server](planning-for-mbam-10-server-deployment.md).

Le procedure descritte in questa sezione descrivono l'installazione completa delle funzionalità di MBAM nei server distribuiti.

### Configurazione con tre computer

Il diagramma seguente mostra la topologia di distribuzione di tre computer per MBAM. Questa topologia è consigliata per gli ambienti di produzione che supportano fino a 55.000 client MBAM.

![mbam tre topologia di distribuzione del computer](images/mbam-3-server.jpg)

In questa configurazione, le caratteristiche di MBAM sono installate nella configurazione seguente:

1.  Database di ripristino e hardware, database di conformità e controllo e report di conformità e controllo sono installati in un server.

2.  La funzionalità Amministrazione e monitoraggio Server è installata in un server.

3.  Il modello di criteri di gruppo di MBAM viene installato in un computer in grado di modificare gli oggetti Criteri di gruppo.

### Configurazione a quattro computer

Il diagramma seguente mostra la topologia di distribuzione di quattro computer per MBAM. Questa topologia è stata consigliata per gli ambienti di produzione che supportano fino a 110.000 client MBAM.

![mbam Four computer topologia di distribuzione.](images/mbam-4-computer.jpg)

In questa configurazione, le caratteristiche di MBAM sono installate nella configurazione seguente:

1.  Database di ripristino e hardware, database di conformità e controllo e report di conformità e controllo sono installati in un server.

2.  La funzionalità Amministrazione e monitoraggio Server è installata in un server configurato in un cluster di server NLB (Network Load Balancing).

3.  Il modello di criteri di gruppo di MBAM viene installato in un computer in grado di modificare gli oggetti Criteri di gruppo.

### Configurazione a cinque computer

Il diagramma seguente mostra la topologia di distribuzione di cinque computer per MBAM. Questa topologia è consigliata per gli ambienti di produzione che supportano fino a 135.000 client MBAM.

![la topologia di distribuzione del computer mbam Five.](images/mbam-5-computer.jpg)

In questa configurazione, le caratteristiche di MBAM sono installate nella configurazione seguente:

1.  Il database di ripristino e hardware viene installato in un server.

2.  Il database di conformità e controllo e i report di conformità e controllo sono installati in un server.

3.  La funzionalità Amministrazione e monitoraggio Server è installata in un server configurato in un cluster di server NLB (Network Load Balancing).

4.  Il modello di criteri di gruppo di MBAM viene installato in un computer in grado di modificare gli oggetti Criteri di gruppo.

[Come installare e configurare MBAM su server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[Come configurare Bilanciamento carico di rete per MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## Altre risorse per la distribuzione delle funzionalità di MBAM 1,0 Server


[Distribuzione di MBAM 1.0](deploying-mbam-10.md)

 

 





