---
title: Come disinstallare il client App-V
description: Come disinstallare il client App-V
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816525"
---
# Come disinstallare il client App-V


Usare la procedura seguente per disinstallare il client di virtualizzazione dell'applicazione dal computer.

**Per disinstallare il client Desktop Application Virtualization**

1.  Nel pannello di controllo fare doppio clic su **installazione** applicazioni o in Windows Vista, **programmi e funzionalità**e quindi fare doppio clic su **client desktop Microsoft Application Virtualization**.

2.  Nella finestra di dialogo visualizzata fare clic su **Sì** per continuare con il processo di disinstallazione.

    **Importante**  Il processo di disinstallazione non può essere annullato o interrotto.

     

3.  Quando viene visualizzato un messaggio che indica che l'applicazione vassoio di Microsoft Application Virtualization Client deve essere chiusa prima di continuare a essere visualizzata, fare clic con il pulsante destro del mouse sull'icona dell'App-V nell'area di notifica e scegliere **Exit** per chiudere l'applicazione. Quindi fare clic su **Riprova** per continuare con il processo di disinstallazione.

    **Importante**  Potrebbe essere visualizzato un messaggio che indica che sono in uso una o più applicazioni virtuali. Chiudere tutte le applicazioni aperte e salvare i dati prima di continuare. Quindi fare clic su **OK** per continuare con il processo di disinstallazione.

     

4.  Una barra di stato indica il tempo rimanente. Al termine di questo passaggio, è necessario riavviare il computer in modo che tutti i driver associati possano essere fermati per completare il processo di disinstallazione.

    **Nota**  Le chiavi del registro di sistema seguenti restano al termine del processo di disinstallazione:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "client" = DWORD: 00000000

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey

     

## Argomenti correlati


[Come installare il client usando la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md)

[Come installare manualmente Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md)

 

 





