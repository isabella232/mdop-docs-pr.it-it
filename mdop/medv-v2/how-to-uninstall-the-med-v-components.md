---
title: Come disinstallare i componenti MED-V
description: Come disinstallare i componenti MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804671"
---
# Come disinstallare i componenti MED-V


In alcuni casi potrebbe essere necessario disinstallare tutti o parte dei componenti di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 dall'organizzazione. Ad esempio, sono stati risolti tutti i problemi di compatibilità dei sistemi operativi delle applicazioni oppure si vuole distribuire un'area di lavoro MED-V diversa nell'organizzazione.

In genere è possibile configurare il sistema ESD (Electronic Software Distribution) per disinstallare i componenti MED-V usando un programma di installazione basato su Windows. In alternativa, è possibile disinstallare manualmente tutti i componenti MED-V.

**Importante**  Prima di poter disinstallare l'agente host MED-V, è necessario prima disinstallare qualsiasi area di lavoro MED-V installata.

 

Usare le procedure seguenti per disinstallare i componenti MED-V dall'organizzazione.

**Per disinstallare MED-V usando un sistema di distribuzione elettronica del software**

1.  Usa il sistema ESD per distribuire uno script che richiama il programma eseguibile uninstall.exe per ogni area di lavoro MED-V che vuoi disinstallare. Il file si trova in C:\\ProgramData\\Microsoft\\Medv\\Workspace. Puoi impostare un contrassegno per eseguire automaticamente il programma eseguibile di disinstallazione in modo che gli utenti finali non siano a conoscenza della disinstallazione.

2.  Creare un pacchetto per distribuire il file di installazione dell'agente host MED-V in ogni computer in cui è stata disinstallata un'area di lavoro MED-V. Configurare il pacchetto per eseguire la disinstallazione in modalità invisibile all'utente.

Il client ESD riconosce la disponibilità dei nuovi pacchetti e avvia la disinstallazione dei pacchetti per la definizione e i requisiti.

**Per disinstallare manualmente un'area di lavoro MED-V**

1.  Nel computer host fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **programmi e funzionalità**.

2.  Nella finestra **programmi e funzionalità** selezionare l'area di lavoro MED-V che si vuole rimuovere e quindi fare clic su **Disinstalla**. L'area di lavoro MED-V è denominata "area di lavoro MED-V- &lt; *area di lavoro \ _name* &gt; "). &lt;Verrà visualizzata la configurazione guidata Area di *lavoro \ _name* &gt; **Setup Wizard** .

3.  Nella **Configurazione guidata**fare clic su **Avanti**e quindi su **Rimuovi**.

4.  Se si preferisce, selezionare la casella di controllo per eliminare il disco VHD master e i dischi differenze creati da MED-V. Questa operazione non è necessaria, ma libera lo spazio su disco dopo la fine della disinstallazione.

5.  Fare clic su **Rimuovi**.

    **Nota**  Se MED-V è attualmente in uso, viene visualizzata una finestra di dialogo che chiede se si vuole arrestarla. Fare clic su **Sì** per continuare con la disinstallazione. Fare clic su **No** per annullare la disinstallazione.

     

In alternativa, è possibile rimuovere un'area di lavoro MED-V eseguendo il `uninstall.exe` file, in genere disponibile in C:\\ProgramData\\Microsoft\\Medv\\Workspace.

**Per disinstallare manualmente l'agente host MED-V**

1.  Nel computer host Windows 7 fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **programmi e funzionalità**.

2.  Nella finestra **programmi e funzionalità** selezionare **agente host MED-V**e quindi fare clic su **Disinstalla**.

    Windows Installer rimuove l'agente host MED-V.

    **Nota**  Se si prova a disinstallare l'agente host MED-V prima di disinstallare l'area di lavoro MED-V, viene visualizzata una finestra di dialogo che indica che è necessario prima disinstallare l'area di lavoro MED-V. Fai clic su **OK** per continuare.

     

**Per disinstallare manualmente il Packager area di lavoro MED-V**

1.  Nel computer host fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **programmi e funzionalità**.

2.  Nella finestra **programmi e funzionalità** selezionare **Packager area di lavoro MED-V**e quindi fare clic su **Disinstalla**.

    Windows Installer rimuove il Packager area di lavoro MED-V.

    **Nota**  Puoi disinstallare il Packager area di lavoro MED-V in qualsiasi momento senza influire sulle aree di lavoro MED-V distribuite.

     

## Argomenti correlati


[Distribuire i componenti MED-V](deploy-the-med-v-components.md)

 

 





