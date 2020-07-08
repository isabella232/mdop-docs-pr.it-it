---
title: Informazioni sull'utilizzo della riga di comando di Sequencer
description: Informazioni sull'utilizzo della riga di comando di Sequencer
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819905"
---
# Informazioni sull'utilizzo della riga di comando di Sequencer


Puoi usare la riga di comando per creare pacchetti di applicazioni sequenziate. L'uso della riga di comando per creare applicazioni virtuali è utile negli scenari seguenti:

-   È necessario creare un numero elevato di pacchetti di applicazioni sequenziate.

-   È necessario creare un pacchetto di applicazione sequenziale su base periodica.

**Importante**  La sequenziazione al prompt dei comandi consente solo la sequenziazione predefinita. Se è necessario modificare i parametri di sequenziazione predefiniti, è necessario modificare manualmente un pacchetto di applicazione sequenziata o ripetere la sequenza dell'applicazione.

 

Tutte le modifiche successive apportate ai pacchetti di applicazioni sequenziate esistenti devono essere eseguite tramite la sequenziazione guidata.

## Prerequisiti


Per sequenziare un'applicazione usando il prompt dei comandi, è necessario che siano soddisfatte le condizioni seguenti:

-   L'applicazione che sta per essere sequenziata non deve richiedere modifiche o soluzioni alternative apportate all'esterno del pacchetto di installazione o di Windows Installer.

-   Prima della sequenziazione, è necessario preparare un elenco di file batch per la creazione dei pacchetti di applicazioni sequenziate.

-   Per altre informazioni sui parametri della riga di comando, vedere [parametri della riga](command-line-parameters.md)di comando.

-   Esaminare gli errori che potrebbero essere visualizzati quando si crea un pacchetto di applicazione sequenziata tramite la riga di comando. Per altre informazioni, vedere questi errori, vedere [errori della riga di comando](command-line-errors.md).

## Argomenti correlati


[Come gestire le applicazioni virtuali usando la riga di comando](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





