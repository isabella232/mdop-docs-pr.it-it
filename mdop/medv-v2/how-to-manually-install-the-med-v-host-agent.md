---
title: Come installare manualmente l'agente host MED-V
description: Come installare manualmente l'agente host MED-V
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804570"
---
# Come installare manualmente l'agente host MED-V


Esistono due componenti distinti ma correlati alla soluzione Microsoft Enterprise Desktop Virtualization (MED-V) 2,0: l'agente host MED-V e l'agente guest. L'agente host risiede nel computer host (un computer dell'utente che sta usando Windows 7) e fornisce un canale per comunicare con il guest MED-V (la macchina virtuale MED-V in uso nel computer host). Offre anche alcune funzionalità correlate a MED-V, ad esempio la pubblicazione di applicazioni.

In genere, si distribuisce e si installa l'agente host MED-V usando il metodo preferito della società per il provisioning del software. Tuttavia, prima di distribuire MED-V nell'organizzazione, potrebbe essere preferibile installare l'agente host localmente per i test. Questa sezione fornisce istruzioni dettagliate per l'installazione manuale dell'agente host MED-V.

**Nota**  L'agente guest MED-V viene installato automaticamente durante la configurazione per la prima volta.

 

**Importante**  Chiudere Internet Explorer prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL. Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.

 

**Per installare l'agente host MED-V**

1.  Individuare i file di installazione di MED-V ricevuti come parte del download del software.

2.  Fare doppio clic sul file di installazione MED-V \ _HostAgent \ _Setup.

    Verrà visualizzata la **Configurazione guidata agente host di Microsoft Enterprise Desktop Virtualization (MED-V)** . Fai clic su **Next** per continuare.

3.  Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.

4.  Selezionare la cartella di destinazione per l'installazione dell'agente host MED-V. Fai clic su **Avanti**.

5.  Per avviare l'installazione dell'agente host, fare clic su **Installa**.

6.  Dopo aver completato l'installazione, fare clic su **fine** per chiudere la procedura guidata.

    Per verificare che l'installazione dell'agente host sia stata eseguita correttamente, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **agente host MED-V**.

**Nota**  Finché non viene installata un'area di lavoro MED-V, l'agente host MED-V può essere avviato ed eseguito, ma non offre alcuna funzionalità.

 

## Argomenti correlati


[Come distribuire i componenti MED-V con un sistema di distribuzione elettronica del software](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[Come installare Packager nell'area di lavoro MED-V](how-to-install-the-med-v-workspace-packager.md)

[Come disinstallare i componenti MED-V](how-to-uninstall-the-med-v-components.md)

 

 





