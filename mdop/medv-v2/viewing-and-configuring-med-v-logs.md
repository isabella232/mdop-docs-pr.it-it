---
title: Visualizzazione e configurazione dei log MED-V
description: Visualizzazione e configurazione dei log MED-V
author: dansimp
ms.assetid: a15537ce-981d-4f55-9c3c-e7fbf94b8fe5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7984cec072827136db9ea52a535c0ea44c6bc2c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823726"
---
# Visualizzazione e configurazione dei log MED-V


Durante la risoluzione dei problemi di MED-V, potrebbe essere utile o necessario accedere ai registri eventi di MED-V. È possibile aprire il Visualizzatore eventi per il computer host e la macchina virtuale guest tramite il Toolkit di amministrazione MED-V. È anche possibile usare il Toolkit di amministrazione MED-V per impostare il livello di registrazione in cui i registri eventi MED-V segnalano gli eventi MED-V.

Per informazioni su come aprire il Toolkit di amministrazione MED-V, vedere [risoluzione dei problemi relativi a Med-v tramite Administration Toolkit](troubleshooting-med-v-by-using-the-administration-toolkit.md).

## Visualizzazione dei registri eventi di MED-V


Nella finestra **Toolkit di amministrazione MED-V** fare clic su **eventi host** per aprire il Visualizzatore eventi per il computer host. In alternativa, fare clic su **eventi Guest** per aprire il Visualizzatore eventi per la macchina virtuale guest.

Il Visualizzatore eventi viene aperto e Visualizza i registri eventi corrispondenti che è possibile usare per risolvere i problemi che possono verificarsi durante la distribuzione o la gestione di MED-V. Per impostazione predefinita, vengono visualizzati solo gli errori e gli avvisi. Per altre informazioni su specifici ID evento e messaggi, vedere [messaggi del log eventi di MED-V](med-v-event-log-messages.md).

**Nota**  Gli utenti finali possono salvare solo i file del log eventi nel Guest se hanno autorizzazioni amministrative.

 

### Per aprire manualmente il Visualizzatore eventi nel computer host

1.  Fare clic sul pulsante **Start**, scegliere **Pannello di controllo**e quindi fare clic su **strumenti di amministrazione**.

2.  Fare doppio clic su **Visualizzatore eventi**e quindi su **registri applicazioni e servizi**.

3.  Fare doppio clic su **MEDV**.

## Configurazione dei log eventi di MED-V


Puoi specificare il livello di registrazione eventi MED-V selezionando il pulsante di opzione corrispondente nel Toolkit di amministrazione di MED-V. È possibile decidere se la registrazione degli eventi include solo errori, errori e avvisi o errori, avvisi e messaggi informativi. Il livello di registrazione degli eventi specificato è impostato sia per il computer host che per la macchina virtuale guest.

Puoi anche specificare il livello di registrazione degli eventi modificando il valore del registro di sistema EventLogLevel. Per altre informazioni, vedere [gestione delle impostazioni di configurazione dell'area di lavoro MED-V](managing-med-v-workspace-configuration-settings.md).

**Nota**  Il livello specificato nella finestra **Toolkit di amministrazione di Med-v** si applica alla registrazione eventi futura di Med-v. Se si imposta il livello per acquisire tutti gli errori, gli avvisi e i messaggi informativi, i log eventi si riempiono più rapidamente e gli eventi meno recenti vengono rimossi.

 

## Argomenti correlati


[Riavvio e ripristino di un'area di lavoro MED-V](restarting-and-resetting-a-med-v-workspace.md)

[Visualizzazione delle configurazioni dell'area di lavoro MED-V](viewing-med-v-workspace-configurations.md)

 

 





