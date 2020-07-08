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
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824756"
---
# Distribuzione dell'infrastruttura server di MBAM 2.0


Le funzionalità del server di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker per la topologia autonoma possono essere installate in configurazioni diverse in due o più server in un ambiente di produzione. La configurazione consigliata è due server per un ambiente di produzione, a seconda dei requisiti di scalabilità. Usare un singolo server per un'installazione di MBAM solo in ambienti di test. Per altre informazioni sulla pianificazione della distribuzione delle funzionalità di MBAM server, vedere [pianificazione della distribuzione di mbam 2,0 Server](planning-for-mbam-20-server-deployment-mbam-2.md).

Il diagramma seguente mostra un esempio di come è possibile configurare la distribuzione di MBAM a due server consigliata. Questa configurazione supporta fino a 200.000 client MBAM in un ambiente di produzione. Le caratteristiche e i database del server nell'immagine dell'architettura sono descritti nella sezione seguente e sono elencati sotto il computer o il server in cui è consigliabile installarli.

![MBAM 2 2-topologia di distribuzione server](images/mbam2-3-servers.gif)

## Server di amministrazione e monitoraggio


In questo server sono installate le caratteristiche seguenti:

-   **Server di amministrazione e monitoraggio**. La funzionalità Amministrazione e monitoraggio Server è installata in un server Windows ed è costituita dal sito Web dell'help desk e dai servizi Web di monitoraggio.

-   **Portale self-service**. Il portale self-service è installato in un server Windows. Il portale self-service consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web, in cui possono ottenere una chiave di ripristino per recuperare un volume di BitLocker bloccato.

## Server di database


In questo server sono installate le caratteristiche seguenti:

-   **Database di ripristino**. Il database di ripristino viene installato in un server Windows e un'istanza supportata di Microsoft SQLServer. Questo database archivia i dati di recupero raccolti dai computer client di MBAM.

-   **Database di conformità e controllo**. Il database di conformità e controllo viene installato in un server Windows e un'istanza supportata di SQLServer. Questo database archivia i dati di conformità per i computer client MBAM. Questi dati vengono usati principalmente per i report ospitati da SQL Server Reporting Services (SSRS).

-   **Report di conformità e controllo**. I report di conformità e controllo vengono installati in un server Windows e un'istanza supportata di SQLServer con la funzionalità SQL Server Reporting Services (SSRS) installata. Questi report includono i report di MBAM a cui è possibile accedere dal sito Web dell'help desk o direttamente dal server SSRS.

## Workstation di gestione


La caratteristica seguente è installata nella workstation di gestione, che può essere un computer Windows Server o client.

-   **Modello di criteri**. Il modello di criteri è costituito da criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per crittografia unità BitLocker. È possibile installare il modello di criteri in qualsiasi server o workstation, ma in genere viene installato in una workstation di gestione, che è un computer Windows Server o client supportato. La workstation non deve essere un computer dedicato.

## <a href="" id="---------mbam-client"></a> Client MBAM


Il client MBAM viene installato in un computer Windows e presenta le caratteristiche seguenti:

-   Usa criteri di gruppo per applicare la crittografia unità BitLocker dei computer client nell'organizzazione.

-   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità USB (removibile Data).

-   Raccoglie i dati di conformità per il computer e passa i dati al sistema di creazione di report.

## Altre risorse per la distribuzione delle funzionalità di MBAM 2,0 Server


[Distribuzione di MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





