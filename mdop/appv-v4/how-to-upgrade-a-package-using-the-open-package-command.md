---
title: Come aggiornare un pacchetto usando il comando Apri pacchetto
description: Come aggiornare un pacchetto usando il comando Apri pacchetto
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816516"
---
# Come aggiornare un pacchetto usando il comando Apri pacchetto


Usare il comando Apri pacchetto per aggiornare o applicare un aggiornamento a un pacchetto di applicazione sequenziale. Quando si aggiorna un pacchetto di applicazione virtuale esistente tramite la riga di comando, la versione originale del file SFT viene eliminata. È consigliabile eseguire il backup del file SFT associato prima di aggiornare il pacchetto tramite la riga di comando.

**Per aggiornare un pacchetto tramite il comando Apri pacchetto**

1.  Per aprire il pacchetto che verrà aggiornato, nella console di Application Virtualization (App-V) selezionare **file**, **aprire il pacchetto per l'aggiornamento**. Nella finestra di dialogo **Apri** selezionare il pacchetto che verrà aggiornato.

2.  Per avviare la **sequenziazione** guidata, selezionare **strumenti**, **sequenziazione guidata**. Completare la procedura guidata applicando le modifiche alla configurazione, per salvare la nuova applicazione sequenziata, selezionare **file**, **Salva**.

3.  Per aggiungere il numero di versione al nome del pacchetto, nella console sequencer selezionare **strumenti**, **Opzioni**. Selezionare **Accoda versione pacchetto a nomefile**. Fai clic su **OK**.

    **Importante**  L'aggiornamento del nome file con la versione del pacchetto è essenziale per completare correttamente l'aggiornamento.

     

## Argomenti correlati


[Come gestire le applicazioni virtuali usando la riga di comando](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





