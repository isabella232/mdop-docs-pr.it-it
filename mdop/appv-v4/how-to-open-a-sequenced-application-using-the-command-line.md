---
title: Come aprire un'applicazione sequenziata usando la riga di comando
description: Come aprire un'applicazione sequenziata usando la riga di comando
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816916"
---
# Come aprire un'applicazione sequenziata usando la riga di comando


È possibile aprire pacchetti di applicazioni virtuali tramite la riga di comando. È necessario eseguire il prompt **cmd** come amministratore.

Usare la procedura seguente per aprire i pacchetti di applicazioni sequenziate tramite la riga di comando

**Per aprire un'applicazione sequenziata tramite la riga di comando**

1.  Per aprire il prompt dei comandi, fare clic sul pulsante **Start**e scegliere **Esegui**, digitare **cmd**e quindi fare clic su **OK**.

2.  Al prompt dei comandi digitare **cd\\** e specificare il percorso della directory in cui è installato Sequencer e quindi premere **INVIO.**

3.  Al prompt dei comandi digitare il comando seguente, sostituendo il testo in corsivo con i valori seguenti:

    SFTSequencer/OPEN:*"specifica il file con estensione SPRJ da aprire"*

    Premere **invio**.

4.  È anche possibile specificare i parametri facoltativi seguenti. Al prompt dei comandi digitare i comandi seguenti, sostituendo il testo in corsivo con i valori:

    /PACKAGENAME: "*specifica il nome del pacchetto"*

    /MSI-specifica la generazione di un programma di installazione di Microsoft Windows associato.

    /COMPRESS: specifica se il pacchetto verrà compresso. Per impostazione predefinita, i pacchetti non vengono compressi.

    Premere **invio**.

    **Nota**  Se il pacchetto di installazione o di Windows Installer ha un'interfaccia utente grafica, verrà visualizzato dopo aver specificato i parametri della riga di comando.

     

## Argomenti correlati


[Come gestire le applicazioni virtuali usando la riga di comando](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





