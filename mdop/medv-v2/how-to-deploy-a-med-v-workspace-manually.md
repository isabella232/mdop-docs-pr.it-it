---
title: Come distribuire manualmente un'area di lavoro MED-V
description: Come distribuire manualmente un'area di lavoro MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827276"
---
# Come distribuire manualmente un'area di lavoro MED-V


In alcuni casi potrebbe essere necessario distribuire manualmente l'area di lavoro MED-V, ad esempio se la società non usa un sistema di distribuzione del software elettronico per distribuire le applicazioni.

Questa sezione fornisce istruzioni su come distribuire manualmente un'area di lavoro MED-V.

**Per distribuire manualmente un'area di lavoro MED-V**

1.  Copiare tutte le applicazioni prerequisite e i file del pacchetto dell'area di lavoro MED-V in un'unità condivisa o in un DVD. Di seguito è riportato un elenco delle applicazioni e dei file necessari.

    -   **PC virtuale Windows**. Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

    -   **Aggiunte e aggiornamenti di Windows Virtual PC**. Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

    -   **File di installazione dell'agente host MED-v** : installa l'agente host (MED-v \ _HostAgent \ _setup file di installazione).

        **Warning**  
        Chiudere Internet Explorer prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL. Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. Installare gli elementi seguenti nell'ordine indicato. L'utente finale può eseguire questa attività manualmente oppure creare uno script per installare gli elementi seguenti:

   -   Windows Virtual PC e le aggiunte e gli aggiornamenti di Windows Virtual PC. È necessario riavviare il computer.

   -   Agente host MED-V.

       **Nota**  
       Se è in corso, Internet Explorer deve essere riavviato prima che l'installazione dell'agente host MED-V possa terminare.



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. Completare la configurazione per la prima volta.

   Dopo l'installazione dell'area di lavoro MED-V, è possibile avviare MED-V. Verrà avviata l'agente host MED-V. A questo punto è possibile avviare MED-V oppure avviare l'agente host MED-V in un secondo momento per completare la configurazione per la prima volta.

   Per avviare l'agente host MED-V, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-v**.

## Argomenti correlati


[Come distribuire un'area di lavoro MED-V con un sistema di distribuzione elettronica del software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[Distribuzione del pacchetto nell'area di lavoro MED-V](deploying-the-med-v-workspace-package.md)









