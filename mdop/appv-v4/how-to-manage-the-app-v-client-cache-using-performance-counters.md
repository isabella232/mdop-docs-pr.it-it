---
title: Come gestire la cache del client App-V con i contatori delle prestazioni
description: Come gestire la cache del client App-V con i contatori delle prestazioni
author: dansimp
ms.assetid: 49d6c3f2-68b8-4c69-befa-7598a8737d05
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 396cceaf9a3bde661200be2771a85596a512732f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817135"
---
# Come gestire la cache del client App-V con i contatori delle prestazioni


È possibile usare la procedura seguente per determinare la quantità di spazio disponibile nella cache client Application Virtualization (App-V) usando Performance Monitor per visualizzare le informazioni graficamente. Queste informazioni vengono acquisite nel computer client da un contatore delle prestazioni denominato "App Virt client cache", che include i seguenti contatori: "dimensione cache (MB)," "cache spazio disponibile (MB)," e "% spazio libero".

**Per determinare l'utilizzo dello spazio della cache client**

1.  Aprire un prompt dei comandi come amministratore oppure fare clic su **Start**, **esegui**, digitare **perfmon.exe**e quindi fare clic su **OK**.

2.  A seconda del sistema operativo Windows in uso, fare clic sullo strumento Monitoraggio prestazioni o monitor di sistema dopo l'apertura della finestra di MMC.

3.  Per aggiungere contatori, fare clic con il pulsante destro del mouse sull'area del grafico e scegliere **Aggiungi contatori**.

4.  Fare clic sul menu a discesa per visualizzare l'elenco dei contatori disponibili, scorrere fino a individuare l' **App Virt client cache**e quindi aggiungere i tre contatori.

    **Importante**  I contatori delle prestazioni di App-V vengono implementati in una DLL a 32 bit, quindi per vederli è necessario usare il comando seguente per avviare la versione a 32 bit di performance monitor: **MMC/32 perfmon. msc**. Questo comando deve essere eseguito direttamente nel computer monitorato e non può essere usato per monitorare un computer remoto che esegue un sistema operativo a 64 bit.

     

## Argomenti correlati


[Come gestire le applicazioni virtuali usando la riga di comando](how-to-manage-virtual-applications-by-using-the-command-line.md)

 

 





