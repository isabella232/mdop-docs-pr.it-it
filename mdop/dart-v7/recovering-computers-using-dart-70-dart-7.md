---
title: Ripristino dei computer con DaRT 7.0
description: Ripristino dei computer con DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822766"
---
# Ripristino dei computer con DaRT 7.0


Esistono due metodi disponibili per recuperare i computer usando Microsoft Diagnostics and Recovery Toolset (DaRT) 7. È possibile eseguire l'immagine di ripristino DaRT7 localmente o usare la funzionalità di connessione remota disponibile in DaRT7 per recuperare un computer remoto. In questa sezione vengono descritti in modo più dettagliato entrambi i metodi.

## Recuperare i computer locali usando l'immagine di ripristino DaRT


Per recuperare un computer locale usando DaRT7, è necessario essere fisicamente presenti nel computer dell'utente finale che sta riscontrando problemi che richiedono dardo.

Sono disponibili diversi metodi tra cui scegliere per l'avvio in dardo, a seconda di come si distribuisce l'immagine di ripristino delle freccette.

-   Inserire un CD, un DVD o un'unità flash USB nel computer problema e usarlo per avviare il computer.

-   Avviare il dardo da una partizione di ripristino nel computer del problema.

-   Avviare il dardo da una partizione remota nella rete.

Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.

**Nota**  La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.

 

[Come ripristinare i computer locali usando l'immagine di ripristino di DaRT](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## Recuperare computer remoti usando l'immagine di ripristino DaRT


La funzionalità di connessione remota in DaRT consente a un amministratore IT di eseguire gli strumenti DaRT in remoto in un computer dell'utente finale. Dopo che alcune informazioni sono state fornite dall'utente finale (o da un helpdesk professionale che lavora nel computer dell'utente finale), l'amministratore IT o l'agente dell'helpdesk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.

**Importante**  I due computer che stabiliscono una connessione remota devono far parte della stessa rete.

 

La finestra del **set di strumenti di diagnostica e ripristino** include l'opzione per eseguire il comando Dart in un computer dell'utente finale da un computer amministratore. L'utente finale apre gli strumenti DaRT nel computer problema e avvia la sessione remota facendo clic su **connessione remota**.

La funzionalità di connessione remota nel computer dell'utente finale crea le informazioni di connessione seguenti: un numero di biglietto, una porta e un elenco di tutti gli indirizzi IP disponibili. Il numero di biglietto e la porta vengono generati in modo casuale.

L'amministratore IT o l'agente dell'helpdesk immette queste informazioni nel **Visualizzatore di connessione remota Dart** per stabilire la connessione ai Servizi terminal per il computer dell'utente finale. La connessione di Servizi terminal che viene stabilita consente a un amministratore IT di interagire in remoto con gli strumenti DaRT nel computer dell'utente finale. Il computer dell'utente finale elabora quindi le informazioni sulla connessione, condivide lo schermo e risponde alle istruzioni del computer dell'amministratore IT.

[Come ripristinare i computer remoti con l'immagine di ripristino di DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## Altre risorse per il recupero di computer con DaRT7


[Operazioni relative a DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





