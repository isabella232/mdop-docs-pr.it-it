---
title: Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale
description: Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale
author: dansimp
ms.assetid: 881d573f-2f18-4c5f-838e-2f5320179f94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6f398c56b7c631145388541b71229d69c16bf6f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822786"
---
# Come eseguire Analizzatore di arresti anomali in modalità autonoma in un computer diverso quello dell'utente finale


Se non è possibile accedere agli strumenti di debug Microsoft per Windows o ai file di simboli nel computer dell'utente finale, è possibile copiare il file di dump dal computer del problema e analizzarlo in un computer in cui è installata la versione autonoma di Crash Analyzer, ad esempio un computer dell'amministratore dell'helpdesk.

**Per eseguire l'analizzatore crash in modalità autonoma**

1.  In un computer in cui è installato DaRT7, fare clic su **Avvia**  /  **tutti i programmi**  /  **Microsoft DaRT 7**.

2.  Specificare le informazioni necessarie per le operazioni seguenti:

    -   Strumenti di debug Microsoft per Windows

    -   File di simboli

        Per altre informazioni sui file di simboli, vedere [come verificare che l'analizzatore crash possa accedere ai file di simboli](how-to-ensure-that-crash-analyzer-can-access-symbol-files-dart-7.md).

    -   Un file di dump di arresto anomalo

        **Nota**  Usare lo strumento di ricerca in DaRT7 per individuare il file di dump dell'arresto anomalo copiato.

         

3.  L' **analizzatore crash** analizza il file di dump di arresto anomalo e segnala una causa probabile dell'arresto anomalo. È possibile visualizzare altre informazioni sull'arresto anomalo, ad esempio il messaggio di arresto anomalo specifico e la descrizione, i driver caricati al momento dell'arresto anomalo e l'output completo dell'analisi.

4.  Decidere su una strategia appropriata per risolvere il problema. Questo potrebbe richiedere la disabilitazione o l'aggiornamento del driver di dispositivo che ha causato l'arresto anomalo usando il nodo **Servizi e driver** dello strumento **Gestione computer** in DART.

## Argomenti correlati


[Diagnosi degli errori di sistema con Analizzatore di arresti anomali](diagnosing-system-failures-with-crash-analyzer--dart-7.md)

 

 





