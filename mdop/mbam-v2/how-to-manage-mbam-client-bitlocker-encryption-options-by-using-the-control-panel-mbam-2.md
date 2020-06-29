---
title: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
description: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825106"
---
# Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo


Un'applicazione per il pannello di controllo di amministrazione e monitoraggio di Microsoft BitLocker (MBAM), denominata opzioni di crittografia BitLocker, sarà disponibile in **sistema e sicurezza** quando viene installato il client di amministrazione e monitoraggio di Microsoft BitLocker. Questo pannello di controllo di MBAM personalizzato è un pannello di controllo aggiuntivo. Non sostituisce il pannello di controllo BitLocker predefinito di Windows. Il pannello di controllo di MBAM può essere usato per sbloccare le unità fisse e rimovibili crittografate e gestire anche il PIN o la password. Per altre informazioni su come abilitare il pannello di controllo di MBAM, vedere [come nascondere la crittografia BitLocker predefinita nel pannello di controllo di Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).

**Per usare il pannello di controllo del client MBAM**

1.  Per aprire le opzioni di crittografia BitLocker, fare clic sul pulsante **Start** e quindi selezionare **Pannello di controllo**. Quando si apre il **Pannello di controllo** , selezionare **sistema e sicurezza**.

2.  Fare doppio clic sulle **Opzioni di crittografia BitLocker** per aprire il pannello di controllo di mbam personalizzato. Verrà visualizzato un elenco di tutte le unità disco rigido del computer e il relativo stato di crittografia, oltre a un'opzione per gestire il PIN o le password.

    L'elenco delle unità disco rigido nel computer può essere usato per verificare lo stato di crittografia, sbloccare un'unità o richiedere un'esenzione per la protezione da BitLocker se sono stati distribuiti i criteri di esenzione per l'utente e il computer.

    Il pannello di controllo opzioni di crittografia BitLocker consente inoltre agli utenti non amministratori di gestire il PIN o le password. Selezionando **Gestisci pin**, viene chiesto agli utenti di immettere sia un PIN corrente che un nuovo PIN, oltre a confermare il nuovo PIN. Selezionando **Aggiorna pin** verrà reimpostato il pin su quello nuovo selezionato dagli utenti.

    Per gestire la password, selezionare **Sblocca unità** e immettere la password corrente. Non appena l'unità è sbloccata, selezionare **Reimposta password** per cambiare la password corrente.

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





