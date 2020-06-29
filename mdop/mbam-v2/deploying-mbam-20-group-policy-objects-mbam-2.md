---
title: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0
description: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823495"
---
# Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0


Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è necessario prima di tutto determinare i criteri di gruppo che verranno usati nell'implementazione dell'amministrazione e del monitoraggio di Microsoft BitLocker. Per altre informazioni sui diversi criteri disponibili, vedere [pianificazione dei requisiti di criteri di gruppo per MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) . Dopo aver determinato i criteri da usare, è necessario creare e distribuire uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri per MBAM tramite il modello di criteri di gruppo di MBAM 2,0.

## Installare il modello MBAM 2,0 criteri di gruppo


Oltre alle funzionalità di amministrazione e monitoraggio di Microsoft BitLocker correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM. Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.

[Come installare il modello Criteri di gruppo di MBAM 2.0](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## Distribuire le impostazioni dei criteri di gruppo di MBAM 2,0


Dopo aver creato i GPO necessari, è necessario distribuire le impostazioni dei criteri di gruppo di MBAM ai computer client dell'organizzazione.

[Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## Visualizzare il pannello di controllo di MBAM in Windows


Dato che MBAM offre un pannello di controllo di MBAM personalizzato che può sostituire il pannello di controllo predefinito di Windows BitLocker, puoi anche scegliere di nascondere il pannello di controllo predefinito di BitLocker dagli utenti finali usando criteri di gruppo.

[Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## Altre risorse per la distribuzione di oggetti Criteri di gruppo di MBAM 2,0


[Distribuzione di MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





