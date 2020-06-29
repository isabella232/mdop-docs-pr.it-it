---
title: Come aggiungere un pacchetto con la riga di comando
description: Come aggiungere un pacchetto con la riga di comando
author: dansimp
ms.assetid: e75af49e-811a-407a-a7f0-6de8562b9188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ab418017a075300f308d4ef4c6eceb4f623a05c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821406"
---
# Come aggiungere un pacchetto con la riga di comando


Le procedure seguenti elencano i passaggi necessari per aggiungere un pacchetto di applicazione virtuale al client Application Virtualization (App-V) in un computer specifico.

**Per aggiungere un pacchetto di applicazione virtuale per un utente specifico**

-   Eseguire il comando seguente sotto l'account utente della persona che deve ottenere il pacchetto. Il comando aggiunge e pubblica il pacchetto per l'utente.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

**Per aggiungere un pacchetto di applicazione virtuale per tutti gli utenti**

-   Eseguire il comando seguente in un account con diritti di amministratore. Il pacchetto viene aggiunto e pubblicato per tutti gli utenti nel computer.

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

**Per aggiungere un pacchetto usando un sistema di distribuzione elettronica del software**

1.  Se si usa un sistema di distribuzione del software elettronico che esegue i comandi sotto l'account di **sistema** del computer, il pacchetto viene pubblicato solo per l'account, a meno che non si usi l'opzione/Global. Eseguire il comando seguente per aggiungere e pubblicare il pacchetto per tutti gli utenti nel computer:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path> /GLOBAL`

2.  

    Se si vuole aggiungere il pacchetto solo per utenti specifici, eseguire il comando **Aggiungi pacchetto** e quindi pubblicare esplicitamente il pacchetto per ogni utente eseguendo il comando **pubblica pacchetto** seguente sotto l'account utente di ogni persona:

    `SFTMIME ADD PACKAGE:”name” /MANIFEST <manifest-path>`

    `SFTMIME PUBLISH PACKAGE:”name” /MANIFEST <manifest-path>`

    La pubblicazione del pacchetto senza il parametro globale concede all'utente l'accesso alle applicazioni nel pacchetto e pubblica i tipi di file e i tasti di scelta rapida elencati nel manifesto nel profilo dell'utente. Le autorizzazioni necessarie sono "Manage tipo di file Associations" (**ManageTypes**) e "Publish Shortcuts" (**PublishShortcut**).

## Argomenti correlati


[Come eliminare tutte le applicazioni virtuali usando la riga di comando](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

[Come rimuovere un pacchetto con la riga di comando](how-to-remove-a-package-by-using-the-command-line.md)

 

 





