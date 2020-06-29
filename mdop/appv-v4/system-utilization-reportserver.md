---
title: Report sull'uso del sistema
description: Report sull'uso del sistema
author: dansimp
ms.assetid: 4d490d15-2d1f-4f2c-99bb-0685447c0672
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe7ff547d969c63ace234104c3e6b7146da2c113
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815255"
---
# Report sull'uso del sistema


Usare il report utilizzo sistema per rappresentare il grafico dell'utilizzo totale del sistema giornaliero. Puoi usare questo report per determinare il carico nel sistema di virtualizzazione dell'applicazione.

Questo report rileva l'utilizzo nel tempo durante il periodo di riferimento per il server specificato o per il gruppo di server.

Il report utilizzo sistema rappresenta anche il seguente utilizzo del sistema:

-   Utilizzo per giorno della settimana

-   Utilizzo per ora del giorno

Il report utilizzo sistema include anche un riepilogo dell'utilizzo totale del sistema per gli utenti specifici e per i conteggi totali delle sessioni.

Quando si crea un report, è necessario specificare i parametri usati per raccogliere i dati quando il report viene eseguito.

I report non vengono eseguiti automaticamente; è necessario eseguirli in modo esplicito per generare i dati di output. Il periodo di tempo necessario per l'esecuzione del report è determinato dalla quantità di dati raccolti nell'archivio dati.

Dopo l'esecuzione di un report e l'output visualizzato nella console di gestione di Application Virtualization Server, è possibile esportare il report nei formati seguenti:

-   Adobe Acrobat (PDF)

-   Microsoft Office Excel

**Nota**  Il nome dell'App-V Server segnalato dai client deve far parte del gruppo predefinito del server in modo che il report di utilizzo del sistema visualizzi i dati. Se ad esempio si usano più server con un bilanciamento del carico di rete (NLB), è necessario aggiungere il nome del cluster NLB al gruppo di server predefinito.

 

## Argomenti correlati


[Come creare un report](how-to-create-a-reportserver.md)

[Come eliminare un report](how-to-delete-a-reportserver.md)

[Come esportare un report](how-to-export-a-reportserver.md)

[Come stampare un report](how-to-print-a-reportserver.md)

[Come eseguire un report](how-to-run-a-reportserver.md)

 

 





