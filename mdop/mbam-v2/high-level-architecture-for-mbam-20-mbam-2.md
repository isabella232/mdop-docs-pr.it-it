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
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824705"
---
# Architettura di alto livello per MBAM 2.0


Microsoft BitLocker Administration and Monitoring (MBAM) è una soluzione client/server che consente di semplificare il provisioning e la distribuzione di BitLocker, migliorare la conformità e la creazione di report su BitLocker e ridurre i costi di supporto. L'amministrazione e il monitoraggio di Microsoft BitLocker includono le caratteristiche descritte in questo argomento.

L'amministrazione e il monitoraggio di Microsoft BitLocker possono essere distribuiti nella topologia autonoma o in una topologia integrata con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager. Questo argomento descrive l'architettura per la topologia autonoma. Per informazioni sulla distribuzione nella topologia di Configuration Manager integrata, vedere [uso di mbam con Configuration Manager](using-mbam-with-configuration-manager.md).

Il diagramma seguente mostra l'architettura di MBAM recommended per un ambiente di produzione, costituito da due server e una workstation di gestione. Questa architettura supporta fino a 200.000 client MBAM. Le caratteristiche e i database del server nell'immagine dell'architettura sono descritti nella sezione seguente e sono elencati sotto il computer o il server in cui è consigliabile installarli.

**Nota**  Un'architettura a server singolo deve essere usata solo in ambienti di test.

 

![MBAM 2 2-topologia di distribuzione server](images/mbam2-3-servers.gif)

## Server di amministrazione e monitoraggio


In questo server sono installate le caratteristiche seguenti:

-   **Server di amministrazione e monitoraggio**. La funzionalità Amministrazione e monitoraggio Server è installata in un server Windows ed è costituita dal sito Web di amministrazione e monitoraggio, che include i report e il portale help desk e i servizi Web di monitoraggio.

-   **Portale self-service**. Il portale self-service è installato in un server Windows. Il portale self-service consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web, in cui possono ottenere una chiave di ripristino per recuperare un volume di BitLocker bloccato.

## Server di database


In questo server sono installate le caratteristiche seguenti:

-   **Database di ripristino**. Il database di ripristino viene installato in un server Windows e un'istanza supportata di Microsoft SQLServer. Questo database archivia i dati di recupero raccolti dai computer client di MBAM.

-   **Database di conformità e controllo**. Il database di conformità e controllo viene installato in un server Windows e un'istanza supportata di SQLServer. Questo database archivia i dati di conformità per i computer client MBAM. Questi dati vengono usati principalmente per i report ospitati da SQL Server Reporting Services (SSRS).

-   **Report di conformità e controllo**. I report di conformità e controllo vengono installati in un server Windows e un'istanza supportata di SQLServer con la funzionalità SQL Server Reporting Services (SSRS) installata. Questi report includono i report di MBAM a cui è possibile accedere dal sito Web di amministrazione e monitoraggio o direttamente dal server SSRS.

## Workstation di gestione


La caratteristica seguente è installata nella workstation di gestione, che può essere un computer Windows Server o client.

-   **Modello di criteri**. Il modello di criteri è costituito da impostazioni di criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per crittografia unità BitLocker. È possibile installare il modello di criteri in qualsiasi server o workstation, ma in genere viene installato in una workstation di gestione, che è un computer Windows Server o client supportato. La workstation non deve essere un computer dedicato.

## <a href="" id="---------mbam-client"></a> Client MBAM


Il client MBAM viene installato in un computer Windows e presenta le caratteristiche seguenti:

-   Usa criteri di gruppo per applicare la crittografia unità BitLocker dei computer client nell'organizzazione.

-   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità USB (removibile Data).

-   Raccoglie i dati di conformità per il computer e passa i dati al sistema di creazione di report.

## Argomenti correlati


[Attività iniziali di MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





