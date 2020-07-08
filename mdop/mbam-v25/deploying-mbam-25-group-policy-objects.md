---
title: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5
description: Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824386"
---
# Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5


Per distribuire MBAM, è necessario impostare le impostazioni dei criteri di gruppo che definiscono le impostazioni di implementazione di MBAM per la crittografia unità BitLocker. Per completare questa attività, è necessario copiare i modelli di criteri di gruppo di MBAM in un server o una workstation in grado di eseguire la console Gestione criteri di gruppo o gestione avanzata Criteri di gruppo e quindi modificare le impostazioni.

**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** oppure mbam non funzionerà correttamente. Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di **crittografia unità BitLocker** .

 

## Copia dei modelli dei Criteri di gruppo di MBAM 2.5


Prima di installare il client MBAM, devi copiare oggetti Criteri di gruppo specifici per MBAM nella workstation di gestione. Questi GPO definiscono le impostazioni di implementazione di MBAM per la crittografia unità BitLocker. È possibile copiare i modelli di criteri di gruppo in qualsiasi server o workstation supportato da un computer Windows Server o client e che sia in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.

[Copia dei modelli dei Criteri di gruppo di MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

## Modifica delle impostazioni GPO di MBAM 2,0


Dopo aver creato i GPO necessari, è necessario distribuire le impostazioni dei criteri di gruppo di MBAM ai computer client dell'organizzazione. Per visualizzare e creare oggetti Criteri di gruppo, è necessario che sia installata la console di gestione dei criteri di raggruppamento o Advanced Group Policy Management.

[Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5](editing-the-mbam-25-group-policy-settings.md)

## Visualizzare o nascondere il pannello di controllo di MBAM nel pannello di controllo di Windows


Dato che MBAM offre un pannello di controllo di MBAM personalizzato che può sostituire il pannello di controllo predefinito di Windows BitLocker, puoi anche scegliere di mostrare o nascondere il pannello di controllo predefinito di BitLocker dagli utenti finali usando le impostazioni dei criteri di gruppo.

[Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## Altre risorse per la distribuzione di oggetti Criteri di gruppo di MBAM 2,0


[Distribuzione di MBAM 2.5](deploying-mbam-25.md)

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





