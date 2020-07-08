---
title: Esempi di configurazioni della macchina virtuale
description: Esempi di configurazioni della macchina virtuale
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824586"
---
# Esempi di configurazioni della macchina virtuale


Di seguito sono riportati alcuni esempi di configurazioni tipiche della macchina virtuale: una in un'area di lavoro MED-V persistente e una in un'area di lavoro di revertible MED-V.

**Nota**  Questi esempi non sono progettati per l'uso in tutti gli ambienti. Regolare la configurazione in base all'ambiente.

 

**Per configurare una configurazione tipica di un dominio in un'area di lavoro MED-V persistente**

1.  Configurare Sysprep nell'immagine di base per creare un SID univoco. Per altre informazioni, vedere [creazione di un'immagine Virtual PC per MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).

2.  Nella scheda **configurazione VM** selezionare la casella di controllo **Esegui configurazione VM** .

3.  Nella sezione **modello di nome computer VM** configura il modello per il nome dell'immagine computer. Per altre informazioni, vedere [come configurare le proprietà del modello di nome computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

4.  Fare clic su **editor di script**, quindi nella finestra di dialogo Editor di **script della configurazione VM** configurare le azioni seguenti:

    1.  **Rinominare il computer**

    2.  **Riavviare Windows**

    3.  **Verificare la connettività**

    4.  **Join Domain**

    5.  **Disabilitare l'accesso automatico**

    Per altre informazioni, vedere [come configurare le azioni di script](how-to-set-up-script-actions.md).

5.  Nel menu **criteri** fare clic su **commit**.

**Per configurare una configurazione tipica in un'area di lavoro di revertible**

1.  Nella scheda **configurazione VM** selezionare la casella di controllo **Rinomina la VM in base al modello di nome computer** .

2.  Nella sezione **modello di nome computer VM** configura il modello per il nome dell'immagine computer. Per altre informazioni, vedere [come configurare le proprietà del modello di nome computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

3.  Nel menu **criteri** fare clic su **commit**.

## Argomenti correlati


[Come configurare la macchina virtuale per un'area di lavoro MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Come configurare le proprietà dei modelli di nome dei computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[Come configurare le azioni script](how-to-set-up-script-actions.md)

 

 





