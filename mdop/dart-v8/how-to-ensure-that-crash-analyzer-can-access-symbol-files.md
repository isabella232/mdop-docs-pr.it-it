---
title: Come verificare che Analizzatore di arresti anomali possa accedere ai file di simboli
description: Come verificare che Analizzatore di arresti anomali possa accedere ai file di simboli
author: dansimp
ms.assetid: 99839013-1cd8-44d1-8484-0e15261c5a4b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 944198b95528a548acbe1229f9f3aad4c224af29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821226"
---
# Come verificare che Analizzatore di arresti anomali possa accedere ai file di simboli


In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'applicazione. Quando si effettua il debug di un'applicazione che ha smesso di rispondere, è necessario avere accesso alle informazioni sui simboli.

I file di simboli vengono scaricati automaticamente quando si esegue **analizzatore crash**. Se il computer non dispone di una connessione Internet o se la rete richiede che il computer acceda a un server proxy HTTP, non è possibile scaricare i file di simboli.

**Per assicurarsi che l'analizzatore crash possa accedere ai file di simboli**

1.  **Copiare il file di dump in un altro computer.** Se non è possibile scaricare i simboli a causa della mancanza di una connessione Internet, copiare il file di dump della memoria in un computer in cui è presente una connessione Internet ed eseguire l' **analizzatore della procedura guidata** autonomo nel computer in uso.

2.  **Accedere ai file di simboli da un altro computer.** Se non è possibile scaricare i simboli a causa della mancanza di una connessione Internet, è possibile scaricarli da un computer in cui è presente una connessione Internet e quindi copiarli nel computer in cui non è disponibile una connessione Internet oppure è possibile eseguire il mapping di un'unità di rete a una posizione in cui i simboli sono disponibili nella rete locale. Se si esegue l' **analizzatore crash** in un ambiente di ripristino di Windows (WindowsRE), è possibile includere i file di simboli nell'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.

3.  **Accedere ai file di simboli tramite un server proxy HTTP.** Se non è possibile scaricare i simboli perché è necessario accedere a un server proxy HTTP, eseguire la procedura seguente per accedere a un server proxy HTTP. In DaRT 8,0, la **procedura guidata Analizzatore crash** ha un'impostazione disponibile nella pagina **specifica posizione file di simboli** , contrassegnata con il **server proxy etichetta (facoltativo, usando il formato "Server: porta")**. Puoi usare questa casella di testo per specificare un server proxy. Immettere l'indirizzo proxy nel formato ** &lt; hostname &gt; : &lt; Port &gt; **, in cui il &lt; nome **host** &gt; è un DNS o un indirizzo IP e la &lt; **porta** &gt; è un numero di porta TCP, in genere 80. Esistono due modalità in cui è possibile eseguire l' **analizzatore crash** . Di seguito viene illustrato il modo in cui si usa l'impostazione proxy in ognuna di queste modalità:

    -   **Modalità online:** In questa modalità, se il campo del server proxy viene lasciato vuoto, la procedura guidata usa le impostazioni proxy da Opzioni Internet nel pannello di controllo. Se si immette un indirizzo proxy nella casella di testo fornita, verrà usato questo indirizzo, che sostituirà l'impostazione nelle opzioni Internet.

    -   Ambiente di ripristino di Windows (WindowsRE): quando si esegue **analizzatore crash** dalla finestra del **set di strumenti di diagnostica e ripristino** , non esiste alcun indirizzo proxy predefinito. Se il computer è connesso direttamente a Internet, non è necessario un indirizzo proxy. Di conseguenza, è possibile omettere questo campo nell'impostazione della procedura guidata. Se il computer non è connesso direttamente a Internet e si trova in un ambiente di rete con un server proxy, è necessario impostare il campo proxy nella procedura guidata per accedere all'archivio simboli. L'indirizzo proxy può essere ottenuto dall'amministratore di rete. L'impostazione del server proxy è importante solo quando l'archivio simboli pubblico è connesso a Internet. Se i simboli sono già presenti nell'immagine di ripristino delle freccette o se sono disponibili localmente, l'impostazione del server proxy non è obbligatoria.

## Argomenti correlati


[Diagnosi degli errori di sistema con Analizzatore di arresti anomali](diagnosing-system-failures-with-crash-analyzer--dart-8.md)

[Operazioni relative a DaRT 8.0](operations-for-dart-80-dart-8.md)

 

 





