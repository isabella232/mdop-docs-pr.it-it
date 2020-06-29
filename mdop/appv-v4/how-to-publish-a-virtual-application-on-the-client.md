---
title: Come pubblicare un'applicazione virtuale nel client
description: Come pubblicare un'applicazione virtuale nel client
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816875"
---
# Come pubblicare un'applicazione virtuale nel client


Quando si distribuisce la virtualizzazione delle applicazioni usando un sistema di distribuzione elettronica del software, è possibile usare una delle procedure seguenti per pubblicare un pacchetto di applicazione per gli utenti.

**Per pubblicare un pacchetto usando un file autonomo di Windows Installer**

1.  Il client deve essere installato con il parametro *RequireAuthorizationIfCached* impostato su 0 (zero). Per altre informazioni sull'impostazione di questo parametro, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md)

2.  Copiare il file di Windows Installer e il file SFT nella stessa cartella nel computer di destinazione.

3.  Eseguire il comando seguente nel computer:

    `Msiexec.exe /I "packagename.msi" /q`

**Per pubblicare un pacchetto con Windows Installer e il manifesto del pacchetto**

1.  Copiare il file di Windows Installer nel computer di destinazione e il file SFT nella condivisione contenuto nel server di streaming.

2.  Eseguire il comando seguente nel computer di ogni utente:

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    **Importante**  Per OVERRIDEURL tutti i caratteri della barra rovesciata devono essere sfuggiti usando una barra rovesciata precedente o il percorso di OVERRIDEURL non verrà analizzato correttamente. Inoltre, le proprietà e i valori devono essere immessi in maiuscolo, ad eccezione del caso in cui il valore è un percorso di un file.

     

**Per pubblicare un pacchetto con SFTMIME**

-   Per un esempio di come pubblicare un'applicazione per tutti gli utenti in un computer, eseguire il comando seguente nel computer dell'utente:

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    Per altre informazioni su questi e altri comandi di SFTMIME, Vedi [riferimento al comando SFTMIME](sftmime--command-reference.md).

## Argomenti correlati


[Determinare il metodo di pubblicazione](determine-your-publishing-method.md)

[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

[Scenario di recapito autonomo per i Application Virtualization Client](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





