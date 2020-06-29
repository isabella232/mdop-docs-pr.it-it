---
title: Come eliminare tutte le applicazioni virtuali usando la riga di comando
description: Come eliminare tutte le applicazioni virtuali usando la riga di comando
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817536"
---
# Come eliminare tutte le applicazioni virtuali usando la riga di comando


Per eliminare tutte le applicazioni virtuali da un computer specifico, è possibile usare la procedura seguente.

**Nota**  Quando tutte le applicazioni vengono eliminate da un pacchetto, il client di Application Virtualization (App-V) Elimina anche il pacchetto.

 

**Per eliminare tutte le applicazioni**

-   Eseguire il comando seguente per eliminare tutte le applicazioni per l'account utente in cui viene eseguito il comando. Se si esegue il comando con l'opzione/GLOBAL facoltativa, usando un account con diritti amministrativi, tutte le applicazioni vengono eliminate per tutti gli utenti.

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    **Nota**  Quando tutte le applicazioni vengono eliminate da un pacchetto, il client di Application Virtualization (App-V) Elimina anche il pacchetto.

     

## Argomenti correlati


[Come aggiungere un pacchetto con la riga di comando](how-to-add-a-package-by-using-the-command-line.md)

[Come rimuovere un pacchetto con la riga di comando](how-to-remove-a-package-by-using-the-command-line.md)

 

 





