---
title: Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo
description: Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823096"
---
# Nascondere l'elemento di Crittografia unità BitLocker predefinito nel Pannello di controllo


Questo argomento descrive come nascondere la voce del pannello di controllo **crittografia unità BitLocker** , che viene visualizzata per impostazione predefinita nel pannello di controllo come parte del sistema operativo Windows.

**Nota**  Microsoft BitLocker Administration and Monitoring (MBAM) crea un'altra voce del pannello di controllo personalizzata, denominata **Opzioni di crittografia BitLocker**, che consente agli utenti finali di gestire il PIN e la password, attivare BitLocker per un'unità e verificare la crittografia.

 

Vedere informazioni sulle [Opzioni di crittografia BitLocker e sugli elementi di crittografia unità BitLocker nel pannello di controllo per la](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) lettura:

-   Differenze tra MBAM e gli elementi del pannello di controllo predefiniti

-   **Gestire** il menu di scelta rapida BitLocker visualizzato quando si fa clic con il pulsante destro del mouse su un'unità in Esplora risorse

**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** . In caso contrario, MBAM non funzionerà correttamente. Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di **crittografia unità BitLocker** .

 

**Per nascondere l'elemento di crittografia unità BitLocker predefinito nel pannello di controllo**

1.  Nella console di gestione di criteri di gruppo o in Gestione criteri di gruppo avanzati individuare il pannello **User configuration** di controllo dei &gt; **Policies** &gt; **modelli amministrativi** &gt; **Control Panel**di criteri di configurazione utente.

2.  Nel riquadro dei **Dettagli** fare doppio clic su **Nascondi elementi del pannello di controllo specificati**e quindi fare clic su **abilitato**.

3.  Fare clic su **Mostra**, su **Aggiungi**e quindi digitare **Microsoft. BitLockerDriveEncryption**.



## Argomenti correlati


[Comprendere le opzioni di crittografia BitLocker e gli elementi di Crittografia unità BitLocker nel Pannello di controllo](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[Distribuzione degli oggetti Criteri di gruppo di MBAM 2.5](deploying-mbam-25-group-policy-objects.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





