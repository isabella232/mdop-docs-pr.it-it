---
title: Applicazione di hotfix su MBAM 2.5 SP1
description: Applicazione di hotfix su MBAM 2.5 SP1
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824186"
---
# Applicazione di hotfix su MBAM 2.5 SP1
Questo argomento descrive il processo per l'applicazione degli hotfix per Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1

### Prima di iniziare, scaricare l'hotfix più recente di Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1
[Pacchetto di ottimizzazione desktop](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> Per altre informazioni sulle versioni di hotfix, vedere il [grafico mbam Version](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).

#### Procedura per aggiornare il server MBAM per l'ambiente attuale MBAM 
1. Rimuovere la caratteristica del server MBAM (eseguire questa operazione aprendo lo strumento di configurazione del server MBAM, quindi selezionando Rimuovi funzionalità).
2. Rimuovere MDOP MBAM dal pannello di controllo | Programmi e funzionalità.
3. Installare i componenti del server di MBAM 2,5 SP1 RTM.
4. Installare l'ultimo aggiornamento cumulativo di MBAM 2,5 SP1.
5. Configurare le caratteristiche di MBAM con MBAM Server Configurator.

#### Procedura per installare il nuovo hotfix per il server MBAM 2,5 SP1
Fare riferimento al documento per l'installazione di un [nuovo server](deploying-the-mbam-25-server-infrastructure.md).
