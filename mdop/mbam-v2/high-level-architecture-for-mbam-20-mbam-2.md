---
title: Architettura di alto livello per MBAM 2.0
description: Architettura di alto livello per MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f19480b5797362e6e4119fff9a14afd9d5a74d98
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910501"
---
# <a name="high-level-architecture-for-mbam-20"></a>Architettura di alto livello per MBAM 2.0


Microsoft BitLocker Administration and Monitoring (MBAM) è una soluzione client/server che consente di semplificare il provisioning e la distribuzione di BitLocker, migliorare la conformità e la creazione di report su BitLocker e ridurre i costi di supporto. Microsoft BitLocker Administration and Monitoring include le funzionalità descritte in questo argomento.

Microsoft BitLocker Administration and Monitoring può essere distribuito nella topologia autonoma o in una topologia integrata con Microsoft System Center Configuration Manager 2007 o Microsoft System Center 2012 Configuration Manager. In questo argomento viene descritta l'architettura per la topologia autonoma. Per informazioni sulla distribuzione nella topologia integrata di Configuration Manager, vedere [Using MBAM with Configuration Manager](using-mbam-with-configuration-manager.md).

Nel diagramma seguente viene illustrata l'architettura consigliata di MBAM per un ambiente di produzione, costituita da due server e una workstation di gestione. Questa architettura supporta fino a 200.000 client MBAM. Le funzionalità e i database del server nell'immagine dell'architettura sono descritti nella sezione seguente e sono elencati nel computer o nel server in cui è consigliabile installarli.

**Nota**  
Un'architettura a server singolo deve essere utilizzata solo negli ambienti di test.

 

![Topologia di distribuzione a due server mbam 2.](images/mbam2-3-servers.gif)

## <a name="administration-and-monitoring-server"></a>Amministrazione e Monitoring Server


Nel server sono installate le funzionalità seguenti:

-   **Amministrazione e Monitoring Server**. La funzionalità Amministrazione e Monitoring Server è installata in un server Windows ed è costituita dal sito Web Amministrazione e monitoraggio, che include i report e il portale help desk e i servizi Web di monitoraggio.

-   **Portale self-service**. Il Self-Service Portal è installato in un server Windows server. Il Self-Service Portal consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web, dove possono ottenere una chiave di ripristino per ripristinare un volume BitLocker bloccato.

## <a name="database-server"></a>Database Server


Nel server sono installate le funzionalità seguenti:

-   **Database di ripristino**. Il database di ripristino viene installato in un server Windows e in un'istanza supportata di Microsoft SQL Server. In questo database vengono archiviati i dati di ripristino raccolti dai computer client MBAM.

-   **Database di conformità e controllo**. Il database di conformità e controllo viene installato in un server Windows e in un'istanza supportata di SQL Server. Questo database archivia i dati di conformità per i computer client MBAM. Questi dati vengono utilizzati principalmente per i report SQL Server Reporting Services (SSRS).

-   **Report di conformità e di controllo**. I report di conformità e controllo vengono installati in un server Windows e in un'istanza supportata di SQL Server in cui è installata la funzionalità SQL Server Reporting Services (SSRS). Questi report forniscono report MBAM a cui è possibile accedere dal sito Web amministrazione e monitoraggio o direttamente dal server SSRS.

## <a name="management-workstation"></a>Workstation di gestione


La funzionalità seguente viene installata nella workstation di gestione, che può essere un server Windows o un computer client.

-   **Modello di criteri**. Il modello di criteri è costituito dalle impostazioni di Criteri di gruppo che definiscono le impostazioni di implementazione mbam per la crittografia dell'unità BitLocker. È possibile installare il modello di criteri in qualsiasi server o workstation, ma in genere viene installato in una workstation di gestione, che è un server Windows o un computer client. La workstation non deve essere un computer dedicato.

## <a name="mbam-client"></a><a href="" id="---------mbam-client"></a> MBAM Client


Il client MBAM viene installato in un computer Windows e presenta le caratteristiche seguenti:

-   Usa Criteri di gruppo per applicare la crittografia dell'unità BitLocker dei computer client nell'organizzazione.

-   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

-   Raccoglie i dati di conformità per il computer e li passa al sistema di report.

## <a name="related-topics"></a>Argomenti correlati


[Attività iniziali di MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





