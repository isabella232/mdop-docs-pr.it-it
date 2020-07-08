---
title: Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0
description: Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821216"
---
# Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0


Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è prima di tutto necessario determinare i criteri di gruppo che verranno usati nell'implementazione di MBAM. Per altre informazioni sui vari criteri disponibili, vedere [pianificazione per i requisiti dei criteri di gruppo di MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Dopo aver determinato i criteri da usare, è necessario usare il modello di criteri di gruppo MBAM 1,0 per creare e distribuire uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri di MBAM.

## Installare il modello MBAM 1,0 criteri di gruppo


Oltre a fornire funzionalità correlate al server di MBAM, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM. Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.

[Come installare il modello Criteri di gruppo di MBAM 1.0](how-to-install-the-mbam-10-group-policy-template.md)

## Distribuire le impostazioni dei criteri di gruppo di MBAM 1,0


Dopo aver creato i GPO necessari, è necessario distribuire le impostazioni dei criteri di gruppo di MBAM ai computer client dell'organizzazione.

[Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 1.0](how-to-edit-mbam-10-gpo-settings.md)

## Visualizzare il pannello di controllo di MBAM in Windows


Dato che MBAM offre un pannello di controllo di MBAM personalizzato che può sostituire il pannello di controllo predefinito di Windows BitLocker, puoi anche scegliere di nascondere il pannello di controllo predefinito di BitLocker dagli utenti finali usando criteri di gruppo.

[Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## Altre risorse per la distribuzione di oggetti Criteri di gruppo di MBAM 1,0


[Distribuzione di MBAM 1.0](deploying-mbam-10.md)

 

 





