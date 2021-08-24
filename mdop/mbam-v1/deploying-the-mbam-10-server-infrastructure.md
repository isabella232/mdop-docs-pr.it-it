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
ms.openlocfilehash: 63099d425b51bfde52eac59771007b1c765acf05
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910421"
---
# <a name="deploying-the-mbam-10-server-infrastructure"></a>Distribuzione dell'infrastruttura server di MBAM 1.0


È possibile installare le funzionalità di Microsoft BitLocker Administration and Monitoring (MBAM) Server in configurazioni diverse utilizzando da uno a cinque server. In genere, è consigliabile utilizzare una configurazione da tre a cinque server per gli ambienti di produzione, a seconda delle esigenze di scalabilità. Per ulteriori informazioni sulla scalabilità delle prestazioni di MBAM e sulle topologie di distribuzione consigliate, vedere il [white paper MBAM Scalability and High-Availability Guide](https://go.microsoft.com/fwlink/p/?LinkId=258314).

## <a name="deploy-all-mbam-10-on-a-single-server"></a>Distribuire tutto MBAM 1.0 in un singolo server


In questa configurazione tutte le funzionalità di MBAM vengono installate in un singolo server. Questa topologia di distribuzione per l'infrastruttura del server MBAM supporterà fino a 21.000 computer client MBAM.

**Importante**  
Questa configurazione è supportata, ma è consigliabile solo per i test.

 

Le procedure descritte in questa sezione descrivono l'installazione completa delle funzionalità di MBAM in un singolo server.

[Come installare e configurare MBAM in un server singolo](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## <a name="deploy-mbam-10-on-distributed-servers"></a>Distribuire MBAM 1.0 nei server distribuiti


Le funzionalità mbam possono essere installate in configurazioni diverse, a seconda delle esigenze di scalabilità. Per ulteriori informazioni su come pianificare la distribuzione delle funzionalità del server MBAM, vedere [Planning for MBAM 1.0 Server Deployment.](planning-for-mbam-10-server-deployment.md)

Le procedure descritte in questa sezione descrivono l'installazione completa delle funzionalità di MBAM nei server distribuiti.

### <a name="three-computer-configuration"></a>Configurazione di tre computer

Nel diagramma seguente viene visualizzata la topologia di distribuzione con tre computer per MBAM. È consigliabile utilizzare questa topologia per ambienti di produzione che supportano fino a 55.000 client MBAM.

![Topologia di distribuzione di tre computer mbam.](images/mbam-3-server.jpg)

In questa configurazione, le funzionalità di MBAM vengono installate nella configurazione seguente:

1.  Il database di ripristino e hardware, il database di conformità e di controllo e i report di conformità e di controllo vengono installati in un server.

2.  La funzionalità Amministrazione e Monitoring Server è installata in un server.

3.  Il modello Criteri di gruppo MBAM è installato in un computer in grado di modificare oggetti Criteri di gruppo.

### <a name="four-computer-configuration"></a>Configurazione di quattro computer

Nel diagramma seguente viene visualizzata la topologia di distribuzione con quattro computer per MBAM. Questa topologia è consigliata per ambienti di produzione che supportano fino a 110.000 client MBAM.

![Topologia di distribuzione di quattro computer mbam.](images/mbam-4-computer.jpg)

In questa configurazione, le funzionalità di MBAM vengono installate nella configurazione seguente:

1.  Il database di ripristino e hardware, il database di conformità e di controllo e i report di conformità e di controllo vengono installati in un server.

2.  La funzionalità Amministrazione e Monitoring Server viene installata in un server configurato in un cluster di server di Bilanciamento carico di rete.

3.  Il modello Criteri di gruppo MBAM è installato in un computer in grado di modificare gli oggetti Criteri di gruppo.

### <a name="five-computer-configuration"></a>Configurazione a cinque computer

Nel diagramma seguente viene visualizzata la topologia di distribuzione con cinque computer per MBAM. È consigliabile utilizzare questa topologia per ambienti di produzione che supportano fino a 135.000 client MBAM.

![Topologia di distribuzione di cinque computer mbam.](images/mbam-5-computer.jpg)

In questa configurazione, le funzionalità di MBAM vengono installate nella configurazione seguente:

1.  Il database di ripristino e hardware è installato in un server.

2.  Il database di conformità e di controllo e i report di conformità e di controllo vengono installati in un server.

3.  La funzionalità Amministrazione e Monitoring Server viene installata in un server configurato in un cluster di server di Bilanciamento carico di rete.

4.  Il modello Criteri di gruppo MBAM viene installato in un computer in grado di modificare oggetti Criteri di gruppo.

[Come installare e configurare MBAM su server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[Come configurare Bilanciamento carico di rete per MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## <a name="other-resources-for-mbam-10-server-features-deployment"></a>Altre risorse per la distribuzione delle funzionalità del server MBAM 1.0


[Distribuzione di MBAM 1.0](deploying-mbam-10.md)

 

 





