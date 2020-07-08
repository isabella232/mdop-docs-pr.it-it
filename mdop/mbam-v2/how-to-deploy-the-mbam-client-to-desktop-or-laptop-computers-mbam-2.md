---
title: Come distribuire il client MBAM a computer desktop o portatili
description: Come distribuire il client MBAM a computer desktop o portatili
author: dansimp
ms.assetid: 56744922-bfdd-48f6-ae01-645ff53b64a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49340ae970dafc9d263f5564e7981a402da40f19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804654"
---
# Come distribuire il client MBAM a computer desktop o portatili


Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione elettronica del software, ad esempio servizi di dominio Active Directory o MicrosoftSystemCenterConfigurationManager.

**Nota**  Per esaminare i requisiti di sistema per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).

 

**Per distribuire il client MBAM in computer desktop o portatili**

1.  Individuare i file di installazione del client MBAM forniti con il software MBAM.

2.  Usare servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale, come MicrosoftSystemCenterConfigurationManager, per distribuire il pacchetto di Windows Installer in computer di destinazione.

3.  Configurare le impostazioni di distribuzione o criteri di gruppo per eseguire il file di installazione del client MBAM. Dopo aver completato l'installazione, il client MBAM applica le impostazioni dei criteri di gruppo ricevute da un controller di dominio per avviare le funzioni di crittografia e gestione di BitLocker. Per altre informazioni sulle impostazioni dei criteri di gruppo di MBAM, vedere [pianificazione per i requisiti di criteri di gruppo di mbam 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md).

    **Importante**  Il client MBAM non avvierà le azioni di crittografia BitLocker se è attiva una connessione di protocollo desktop remoto. Tutte le connessioni della console remota devono essere chiuse prima che venga avviata la crittografia BitLocker.

     

## Argomenti correlati


[Distribuzione del client MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)

 

 





