---
title: Installazione di applicazioni in un'immagine di Windows Virtual PC
description: Installazione di applicazioni in un'immagine di Windows Virtual PC
author: dansimp
ms.assetid: 32651eff-e3c6-4ef4-947d-2beddc695eac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bf73fec0b33b37c2553dfe6f923917aa926b8e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826835"
---
# Installazione di applicazioni in un'immagine di Windows Virtual PC


Dopo aver creato un'immagine di Windows Virtual PC per l'uso con Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, è possibile installare altri componenti utili quando si esegue MED-V, ad esempio un sistema ESD (Electronic Software Distribution) e un software antivirus.

La sezione seguente contiene informazioni utili per installare il software nell'immagine MED-V.

**Attenzione**  Per semplificare la gestione dell'area di lavoro MED-V dopo la distribuzione, è consigliabile limitare il numero di componenti da installare nell'immagine MED-V per i componenti necessari o utili quando si usa MED-V. Ad esempio, anche se non è necessario eseguire MED-V, è possibile installare un sistema ESD da usare in seguito per l'installazione di applicazioni in un'area di lavoro MED-V e un software antivirus per la sicurezza sull'immagine.

 

**Installazione del software in un'immagine MED-V**

1.  Se non è attualmente in uso, aprire la macchina virtuale MED-V.

    1.  Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC** e quindi fare clic su **Virtual PC Windows**.

    2.  Fare doppio clic sulla macchina virtuale MED-V.

2.  Nel sistema operativo della macchina virtuale individuare i file di installazione per il software che si vuole installare.

3.  Seguire le istruzioni di installazione fornite dal fornitore del software.

    **Nota**  Dopo aver completato l'installazione, potrebbe essere necessario chiudere e quindi riavviare la macchina virtuale.

     

Ripetere questi passaggi per qualsiasi software o applicazione che si vuole installare nell'immagine MED-V. È consigliabile limitare il numero di applicazioni preinstallate nell'immagine. Il processo consigliato per l'installazione di applicazioni e altri software nell'immagine consiste nel preinstallare ora un sistema ESD e usarlo in seguito per distribuire il software all'immagine. In alternativa, puoi anche usare criteri di gruppo o App-V per aggiungere o rimuovere applicazioni in un'area di lavoro MED-V. Per altre informazioni, vedere [gestione delle applicazioni distribuite nelle aree di lavoro MED-V](managing-applications-deployed-to-med-v-workspaces.md).

Per altre informazioni su come installare il software in un'immagine virtuale, vedere gli articoli seguenti:

-   [Pubblicare e usare le applicazioni virtuali](https://go.microsoft.com/fwlink/?LinkId=195926) ( https://go.microsoft.com/fwlink/?LinkId=195926) .

-   [Guida di Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Dopo aver installato tutto il software desiderato nell'immagine MED-V, l'immagine è pronta per essere inclusa nel pacchetto.

## Argomenti correlati


[Configurazione di un'immagine di Windows Virtual PC per MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Creare un'immagine MED-V](prepare-a-med-v-image.md)

 

 





