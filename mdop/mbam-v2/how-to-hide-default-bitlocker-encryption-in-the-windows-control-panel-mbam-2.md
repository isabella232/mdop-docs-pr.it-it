---
title: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
description: Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824085"
---
# Come nascondere la crittografia BitLocker predefinita nel Pannello di controllo di Windows


Microsoft BitLocker Administration and Monitoring (MBAM) offre un pannello di controllo personalizzato per l'amministrazione di Microsoft BitLocker e il monitoraggio dei computer client, denominati opzioni di crittografia BitLocker. Questo pannello di controllo personalizzato può sostituire il pannello di controllo BitLocker predefinito di Windows, denominato crittografia unità BitLocker. Il pannello di controllo personalizzato, che si trova nel pannello di controllo in sistema e sicurezza, consente agli utenti di gestire il PIN e le password e di sbloccare le unità e nasconde l'interfaccia che consente agli amministratori di decrittografare un'unità o di sospendere o riprendere la crittografia unità BitLocker.

**Per nascondere la crittografia predefinita unità BitLocker nel pannello di controllo di Windows**

1.  Nella console Gestione criteri di gruppo (GPMC), in Advanced Group Policy Management o nell'Editor criteri di gruppo locali nel computer criteri di gruppo di BitLocker, passare alla **Configurazione utente**.

2.  Fare quindi clic su **criteri**, selezionare **modelli amministrativi**e quindi fare clic su **Pannello di controllo**.

3.  Fare doppio clic su **Nascondi elementi del pannello di controllo specificati** nel riquadro dei **Dettagli** e quindi selezionare **abilitato**.

4.  Fare clic su **Mostra**, su **Aggiungi**e quindi digitare **Microsoft. BitLockerDriveEncryption**. Questo criterio nasconde lo strumento di Gestione BitLocker predefinito di Windows dal pannello di controllo di Windows e, nel pannello di controllo, consente all'utente di aprire lo strumento per le opzioni di crittografia di BitLocker aggiornato di MBAM in sistema e sicurezza.

## Argomenti correlati


[Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





