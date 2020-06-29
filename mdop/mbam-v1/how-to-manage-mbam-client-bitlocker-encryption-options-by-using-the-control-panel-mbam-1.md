---
title: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
description: Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804617"
---
# Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo


Un'applicazione per il pannello di controllo di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, denominata opzioni di crittografia BitLocker, sarà disponibile in **sistema e sicurezza** quando il client mbam è installato. Questo pannello di controllo di MBAM personalizzato sostituisce il pannello di controllo predefinito di Windows BitLocker. Il pannello di controllo di MBAM consente di sbloccare le unità crittografate (fisse e rimovibili) e consente anche di gestire il PIN o la password. Per altre informazioni su come abilitare il pannello di controllo di MBAM, vedere [come nascondere la crittografia BitLocker predefinita nel pannello di controllo di Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).

**Nota**  Per il client BitLocker, i file di registro dell'amministratore e dell'operativo si trovano nel Visualizzatore eventi, in **applicazione e servizi vengono registrati**  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.

 

**Per usare il pannello di controllo del client MBAM**

1.  Per aprire le opzioni di crittografia BitLocker, fare clic sul pulsante **Start**e quindi selezionare **Pannello di controllo**. Quando si apre il **Pannello di controllo** , selezionare **sistema e sicurezza**.

2.  Fare doppio clic sulle **Opzioni di crittografia BitLocker** per aprire il pannello di controllo di mbam personalizzato. Verrà visualizzato un elenco di tutte le unità disco rigido nel computer e il relativo stato di crittografia. Verrà visualizzata anche un'opzione per gestire il PIN o le password.

3.  Usare l'elenco di unità disco rigido nel computer per verificare lo stato di crittografia, sbloccare un'unità o richiedere un'esenzione per la protezione da BitLocker se sono stati distribuiti i criteri di esenzione dall'utente e dal computer.

4.  Gli utenti non amministratori possono usare il pannello di controllo opzioni di crittografia BitLocker per gestire i pin o le password. Un utente può selezionare **Gestisci pin** e quindi immettere sia un PIN corrente che un nuovo PIN. Gli utenti possono anche confermare il nuovo PIN. La funzione **Aggiorna pin** Reimposta il pin su quello nuovo selezionato dall'utente.

5.  Per gestire la password, selezionare **Sblocca unità** e immettere la password corrente. Non appena l'unità è sbloccata, selezionare **Reimposta password** per cambiare la password corrente.

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 1.0](administering-mbam-10-features.md)

 

 





