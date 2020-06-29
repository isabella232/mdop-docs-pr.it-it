---
title: Come modificare le proprietà del pacchetto
description: Come modificare le proprietà del pacchetto
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818045"
---
# Come modificare le proprietà del pacchetto


È possibile usare le procedure seguenti per modificare il nome di un pacchetto di virtualizzazione dell'applicazione e i commenti associati.

Se è la prima volta che il pacchetto è stato creato, è anche possibile modificare la dimensione del blocco dei parametri di sequenziazione, che determina la modalità di trasmissione di un pacchetto di applicazione sequenziata da un Application Virtualization Server a un client Desktop Application Virtualization.

**Nota**  Quando si seleziona una dimensione di blocco, prendere in considerazione le dimensioni del file SFT e la larghezza di banda della rete. Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda. I file con dimensioni di blocco più grandi potrebbero essere trasmessi più rapidamente, ma usano più larghezza di banda della rete. Grazie alla sperimentazione, è possibile individuare le dimensioni di blocco ottimali per le applicazioni di streaming della rete.

 

La restante parte delle proprietà del pacchetto nella scheda **Proprietà** viene generata automaticamente e non può essere modificata in questa scheda.

**Per modificare il nome o i commenti del pacchetto**

1.  Fare clic sulla scheda **Proprietà** .

2.  Nella casella di testo **nome pacchetto** immettere o modificare il singolo nome usato per il pacchetto, che può contenere più applicazioni.

3.  Nella casella di testo **Commenti** , facoltativamente, immettere o modificare i commenti. La procedura consigliata consigliata consiste nel creare informazioni dettagliate sul pacchetto e la sequenziazione.

4.  Scegliere **Salva**dal menu **file** .

**Per modificare le dimensioni del blocco**

1.  Fare clic sulla scheda **Proprietà** .

2.  Nell'elenco a discesa **dimensione blocco** selezionare **4 KB**, **16 kb**, **32 KB**o **64 KB**.

3.  Scegliere **Salva**dal menu **file** .

## Argomenti correlati


[Informazioni sulla scheda Proprietà](about-the-properties-tab.md)

[Console di Sequencer](sequencer-console.md)

 

 





