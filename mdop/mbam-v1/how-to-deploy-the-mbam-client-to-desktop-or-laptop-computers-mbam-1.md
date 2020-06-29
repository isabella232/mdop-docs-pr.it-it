---
title: Come distribuire il client MBAM a computer desktop o portatili
description: Come distribuire il client MBAM a computer desktop o portatili
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825545"
---
# Come distribuire il client MBAM a computer desktop o portatili


Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client MBAM può essere integrato in un'organizzazione distribuendo il client tramite strumenti, ad esempio servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale, ad esempio MicrosoftSystemCenter2012 ConfigurationManager.

**Nota**  Per esaminare i requisiti di sistema client di MBAM, vedere [configurazioni supportate di mbam 1,0](mbam-10-supported-configurations.md).

 

**Per distribuire il client MBAM in computer desktop o portatili**

1.  Individuare i file di installazione del client MBAM forniti con il software MBAM.

2.  Distribuire il pacchetto di Windows Installer in computer di destinazione usando servizi di dominio Active Directory o uno strumento di distribuzione del software aziendale, ad esempio MicrosoftSystemCenter2012 ConfigurationManager.

    **Nota**  Non usare criteri di gruppo per distribuire il pacchetto di Windows Installer.

     

3.  Configurare le impostazioni di distribuzione o criteri di gruppo per eseguire il file di installazione del client MBAM. Dopo aver completato l'installazione, il client MBAM applica le impostazioni dei criteri di gruppo ricevute da un controller di dominio per avviare le funzioni di crittografia e gestione di BitLocker. Per altre informazioni sulle impostazioni dei criteri di gruppo di MBAM, vedere [pianificazione per i requisiti di criteri di gruppo di mbam 1,0](planning-for-mbam-10-group-policy-requirements.md).

    **Importante**  Il client MBAM non avvierà le azioni di crittografia BitLocker se è attiva una connessione di protocollo desktop remoto. Tutte le connessioni della console remota devono essere chiuse prima che venga avviata la crittografia BitLocker.

     

## Argomenti correlati


[Distribuzione del client MBAM 1.0](deploying-the-mbam-10-client.md)

 

 





