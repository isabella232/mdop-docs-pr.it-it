---
title: Come caricare le applicazioni virtuali dall'area di notifica del desktop
description: Come caricare le applicazioni virtuali dall'area di notifica del desktop
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817216"
---
# Come caricare le applicazioni virtuali dall'area di notifica del desktop


Se si è un utente per dispositivi mobili, è consigliabile caricare completamente le applicazioni nella cache per usarle durante l'operazione disconnessa o la modalità offline. Per eseguire il flusso delle applicazioni dal server Application Virtualization (App-V) o dall'Application Virtualization (App-V) streaming server, è necessario essere connessi a un server per caricare le applicazioni. Se non si è connessi al server quando si tenta di caricare le applicazioni, il sistema genererà un messaggio di errore appropriato. È anche possibile eseguire il flusso di applicazioni nel client da un file o un disco.

Le applicazioni vengono caricate un'applicazione alla volta. La barra di stato Mostra il nome dell'applicazione, la percentuale di applicazione caricata e il numero di applicazioni già elaborate rispetto al numero totale delle applicazioni accodate. È possibile ignorare qualsiasi applicazione in corso prima che venga caricata 100%. È anche possibile ignorare il caricamento di tutte le applicazioni rimanenti.

**Nota**  Se il sistema rileva un errore durante il caricamento di un'applicazione, segnala l'errore. È necessario chiudere la finestra di dialogo di errore prima che venga caricata l'applicazione successiva.

 

**Per caricare tutte le applicazioni**

1.  Fare clic con il pulsante destro del mouse sull'icona Application Virtualization System nell'area di notifica.

2.  Selezionare **Carica applicazioni** dal menu a comparsa.

**Per ignorare le applicazioni**

1.  Fare clic sulla barra di stato per visualizzare la finestra di dialogo.

2.  Selezionare uno dei pulsanti seguenti per ottenere i risultati desiderati:

    1.  **Skip**-per ignorare l'applicazione attualmente caricata.

    2.  **Ignora tutto**: per ignorare tutte le applicazioni rimanenti.

    3.  **Continua**: per annullare la finestra di dialogo e continuare a caricare le applicazioni.

## Argomenti correlati


[Come usare l'area di notifica del desktop per Application Virtualization Client Management](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





