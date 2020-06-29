---
title: Come creare un ambiente di test
description: Come creare un ambiente di test
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827286"
---
# Come creare un ambiente di test


Di seguito sono riportati alcuni passaggi e istruzioni utili per creare un ambiente di test che è possibile usare per testare il pacchetto dell'area di lavoro MED-V localmente prima di distribuirlo in tutta l'organizzazione. Questa sezione fornisce indicazioni su come creare un ambiente di test, manualmente o usando un sistema di distribuzione elettronica del software.

**Per creare un ambiente di test usando un ESD**

1.  Usa il metodo aziendale di distribuzione del software in tutta l'organizzazione per distribuire i componenti necessari seguenti in un computer di test. Installarle nell'ordine seguente:

    -   **Windows Virtual PC** -se non è già installato. Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

    -   **Aggiunte e aggiornamenti di Windows Virtual PC**, se non sono già installati. Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

    -   **File di installazione dell'agente host MED-v** : installa l'agente host (MED-v \ _HostAgent \ _setup file di installazione). Per altre informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).

    -   **Programma di installazione dell'area di lavoro MED-v, VHD e configurazione eseguibile** -creato nel **Packager area di lavoro MED-v**. Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).

        **Importante**  Il programma eseguibile e la configurazione del disco rigido virtuale devono essere nella stessa cartella di installazione dell'area di lavoro MED-V. Installare quindi il programma di installazione dell'area di lavoro MED-V eseguendo setup.exe.

         

2.  Dopo aver installato tutti i componenti nel computer di test, eseguire l'agente host MED-V per iniziare la configurazione per la prima volta.

    Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-V**.

    **Nota**  Se non è possibile eseguire fisicamente l'agente host MED-V nel computer di test, viene avviata automaticamente la prima volta che il computer viene riavviato.

     

La prima volta che viene avviata la configurazione e può richiedere dieci minuti o più per terminare.

Per informazioni su come testare le impostazioni di configurazione quando è in esecuzione la configurazione iniziale, vedere [come verificare le impostazioni di configurazione per la prima volta](how-to-verify-first-time-setup-settings.md).

**Per creare manualmente un ambiente di test**

1.  Installare l'agente host MED-V in un ambiente di test locale che include prerequisiti MED-V, ad esempio Windows Virtual PC con aggiunte e aggiornamenti. Per informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).

2.  Copiare i file dell'area di lavoro MED-V nell'ambiente di test. I file dell'area di lavoro MED-V si trovano nella cartella di destinazione specificata nel **Packager area di lavoro MED-v**.

    **Importante**  Il programma eseguibile e la configurazione del disco rigido virtuale devono trovarsi nella stessa cartella dell'ambiente di test di installazione dell'area di lavoro MED-V.

     

3.  Installare l'area di lavoro MED-V eseguendo setup.exe.

4.  Avviare la configurazione per la prima volta eseguendo l'agente host MED-V.

    Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-V**.

La prima volta che viene avviata la configurazione e può richiedere diversi minuti per il completamento, a seconda delle dimensioni del VHD specificato.

Ora si è pronti per testare le diverse impostazioni per la configurazione, la pubblicazione delle applicazioni e il reindirizzamento degli URL specificati per l'area di lavoro MED-V.

**Nota**  Per impostazione predefinita, MED-V esegue l'override dei criteri di blocco dello schermo nell'ospite. Tuttavia, questo non pone un problema di sicurezza perché il computer host rispetta ancora i criteri di blocco dello schermo.

 

## Argomenti correlati


[Come verificare le impostazioni della prima configurazione](how-to-verify-first-time-setup-settings.md)

[Come verificare la pubblicazione delle applicazioni](how-to-test-application-publishing.md)

[Come verificare il reindirizzamento URL](how-to-test-url-redirection.md)

 

 





