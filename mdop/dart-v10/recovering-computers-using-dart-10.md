---
title: Ripristino dei computer con DaRT 10
description: Ripristino dei computer con DaRT 10
author: dansimp
ms.assetid: 2ad7fab0-c22d-4171-8b5a-b2b7d7c0ad2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2031d55427e24638e41dfc6ed7b0ef437922e9c4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822956"
---
# Ripristino dei computer con DaRT 10


Dopo aver distribuito l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10, puoi usare DaRT 10 per recuperare i computer. Le informazioni in questa sezione illustrano le attività di ripristino che è possibile eseguire.

Sono disponibili diversi metodi tra cui scegliere per l'avvio in dardo, a seconda di come si distribuisce l'immagine di ripristino delle freccette.

-   Inserire un CD, un DVD o un'unità flash USB nel computer problema e usarlo per avviare il computer.

-   Avviare il dardo da una partizione di ripristino nel computer del problema.

-   Avviare il dardo da una partizione remota nella rete.

Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di Dart 10](planning-how-to-save-and-deploy-the-dart-10-recovery-image.md).

Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.

**Nota**  La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.

 

## Recuperare un computer locale usando l'immagine di ripristino DaRT


Per recuperare un computer locale tramite dardo, è necessario essere fisicamente presenti nel computer dell'utente finale che sta riscontrando problemi che richiedono dardo.

[Come ripristinare i computer locali usando l'immagine di ripristino di DaRT](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md)

## Recuperare un computer remoto usando l'immagine di ripristino DaRT


La funzionalità di connessione remota in DaRT consente a un amministratore IT di eseguire gli strumenti DaRT in remoto in un computer dell'utente finale. Dopo che alcune informazioni sono state fornite dall'utente finale (o da un Help Desk Professional che lavora nel computer dell'utente finale), l'amministratore IT o il lavoratore dell'help desk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.

**Importante**  I due computer che stabiliscono una connessione remota devono far parte della stessa rete.

 

La finestra del **set di strumenti di diagnostica e ripristino** include l'opzione per eseguire il comando Dart in un computer dell'utente finale da un computer amministratore. L'utente finale apre gli strumenti DaRT nel computer problema e avvia la sessione remota facendo clic su **connessione remota**.

La funzionalità di connessione remota nel computer dell'utente finale crea le informazioni di connessione seguenti: un numero di biglietto, una porta e un elenco di tutti gli indirizzi IP disponibili. Il numero di biglietto e la porta vengono generati in modo casuale.

L'amministratore IT o il lavoratore dell'help desk immette queste informazioni nel **Visualizzatore di connessioni remote di Dart** per stabilire la connessione di Servizi terminal al computer dell'utente finale. La connessione di Servizi terminal che viene stabilita consente a un amministratore IT di interagire in remoto con gli strumenti DaRT nel computer dell'utente finale. Il computer dell'utente finale elabora quindi le informazioni sulla connessione, condivide lo schermo e risponde alle istruzioni del computer dell'amministratore IT.

[Come ripristinare i computer remoti con l'immagine di ripristino di DaRT](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md)

## Altre risorse per il recupero di computer con il dardo 10


[Operazioni relative a DaRT 10](operations-for-dart-10.md)

 

 





