---
title: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
description: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824506"
---
# Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows


Microsoft BitLocker Administration and Monitoring (MBAM) offre un pannello di controllo personalizzato per i computer client di MBAM denominato opzioni di crittografia BitLocker. Questo pannello di controllo personalizzato può sostituire il pannello di controllo BitLocker predefinito di Windows denominato crittografia unità BitLocker. Il pannello di controllo opzioni di crittografia BitLocker, che si trova in sistema e sicurezza nel pannello di controllo di Windows, consente agli utenti di gestire il PIN e le password, sbloccare le unità e nascondere l'interfaccia che consente agli amministratori di decrittografare un'unità o di sospendere o riprendere la crittografia di BitLocker.

**Per nascondere la crittografia BitLocker predefinita nel pannello di controllo di Windows**

1.  Passare alla **Configurazione utente** usando la console Gestione criteri di gruppo, la gestione avanzata Criteri di gruppo o l'Editor criteri di gruppo locali nel computer criteri di gruppo di BitLocker.

2.  Fare clic su **criteri**, selezionare **modelli amministrativi**e quindi fare clic su **Pannello di controllo**.

3.  Nel riquadro dei **Dettagli** fare doppio clic su **Nascondi elementi del pannello di controllo specificati**e quindi selezionare **abilitato**.

4.  Fare clic su **Mostra**, **su Aggiungi...** e quindi digitare Microsoft. BitLockerDriveEncryption. Questo criterio nasconde lo strumento di Gestione BitLocker predefinito di Windows dal pannello di controllo di Windows e consente all'utente di aprire lo strumento per la crittografia di BitLocker aggiornato MBAM dal pannello di controllo di Windows.

## Argomenti correlati


[Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0](deploying-mbam-10-group-policy-objects.md)

 

 





