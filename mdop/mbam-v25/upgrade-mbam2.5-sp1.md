---
title: Aggiornamento da MBAM 2,5 a MBAM 2,5 SP1 Service Update Release
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804474"
---
# Aggiornamento da MBAM 2,5 a MBAM 2,5 SP1 aggiornamento della versione di manutenzione

Questo articolo fornisce istruzioni dettagliate per aggiornare Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 per MBAM 2,5 Service Pack 1 (SP1) insieme a [Microsoft Desktop Optimization Pack (MDOP) maggio 2019 manutenzione aggiornamento](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) in una configurazione autonoma.

In questa guida useremo una configurazione a due server. Un server sarà un server di database che sta usando Microsoft SQL Server 2016. Questo server ospiterà i database e i report di MBAM. L'altro server sarà un server Web di Windows Server 2012 R2. Questo server ospiterà "amministrazione e monitoraggio" e "portale self-service".

## Preparare l'aggiornamento MBAM 2,5 SP1

### Conoscere i server MBAM nell'ambiente

1. Motore di database di SQL Server: server che ospita i database di MBAM.
2. SQL Server Reporting Services: server che ospita i report di MBAM.
3. Server Web di Internet Information Services (IIS): server che ospita le applicazioni Web MBAM e i servizi MBAM.
4. Opzionale Server del sito principale di Microsoft System Center Configuration Manager: l'applicazione di configurazione MBAM viene eseguita su questo server per integrare i report di MBAM con Configuration Manager. Questi report vengono quindi Uniti con i report di gestione configurazione esistenti nell'istanza di SQL Server Reporting Services (SSRS) di Configuration Manager.

### Identificare gli account del servizio, i gruppi, il nome del server e l'URL report

1. Identificare l'account del servizio di pool di applicazioni MBAM usato dai server Web IIS per leggere e scrivere dati nei database di MBAM.
2. Identificare i gruppi usati durante la configurazione delle caratteristiche Web di MBAM e l'URL del servizio Web report.
3. Identificare il nome e il nome dell'istanza di SQL Server. Guarda questo video per saperne di più.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. Identificare l'account di SQL Server Reporting Services usato per leggere i dati di conformità dal database di conformità e controllo. Guarda questo video per saperne di più.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## Aggiornare l'infrastruttura MBAM all'ultima versione disponibile

L'installazione o l'aggiornamento di MBAM Server Infrastructure viene sempre eseguito nell'ordine seguente:

- Motore di database di SQL Server: database
- SQL Server Reporting Services: report
- Server Web: applicazioni Web
- Server SCCM: report integrati di SCCM se applicabile
- Client: agente MBAM o aggiornamento client
- Modelli di criteri di gruppo: aggiornare i criteri di gruppo esistenti con i nuovi modelli e abilitare le nuove impostazioni per i criteri di gruppo di MBAM esistenti

> [!NOTE]
> È consigliabile creare un backup completo dei database MBAM prima di eseguire gli aggiornamenti.

### Aggiornare il MBAM SQL Server

Guardare questo video per informazioni su come eseguire l'aggiornamento di MBAM SQL Server:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### Aggiornare il server Web di MBAM

Guardare questo video per informazioni su come aggiornare il server Web di MBAM:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## Altre informazioni

Per altre informazioni sui problemi noti di MBAM 2,5 SP1, vedere [Note sulla versione per mbam 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).
