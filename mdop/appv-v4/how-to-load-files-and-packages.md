---
title: Come caricare file e pacchetti
description: Come caricare file e pacchetti
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817236"
---
# Come caricare file e pacchetti


È possibile usare la procedura seguente per caricare file e pacchetti nei server di virtualizzazione delle applicazioni.

**Nota**  Durante il processo di installazione è stata specificata la posizione della directory \\Content nella pagina **percorso contenuto** . Questa directory deve essere creata e configurata come condivisione file standard prima di puntare alla relativa posizione.

 

**Per caricare file e pacchetti**

1.  Nel computer da cui si vuole eseguire il flusso delle applicazioni, passare al percorso specificato per la directory \\Content. Se necessario, creare la directory e configurarla come condivisione file standard.

2.  Trasferire i file SFT per le applicazioni e i pacchetti virtuali nella directory \\Content. Per organizzare i file SFT e per evitare confusione, inserire applicazioni e pacchetti in sottocartelle dedicate.

3.  Caricare le applicazioni e i pacchetti in base ai requisiti dello scenario e della configurazione, considerando le condizioni seguenti:

    -   Se le applicazioni e i pacchetti sono archiviati in un server di gestione di Application Virtualization (App-V), caricarli tramite la console di gestione. Per altre informazioni, Vedi [come caricare o scaricare un'applicazione](how-to-load-or-unload-an-application.md) o [come caricare applicazioni virtuali dall'area di notifica desktop](how-to-load-virtual-applications-from-the-desktop-notification-area.md).

    -   Se le applicazioni sono archiviate in un'app-V Streaming Server, in un server Web o in un computer configurato come file server, le applicazioni possono essere caricate automaticamente.

        **Nota**  App-V Streaming Server esegue automaticamente il polling della directory \\Content per le applicazioni e i pacchetti e inserisce queste informazioni in RAM per le richieste di applicazione del servizio.

        I client App-V devono essere configurati in modo appropriato per recuperare le applicazioni e i pacchetti da server Web e file server. Per altre informazioni, vedere [come configurare il client per il recupero del pacchetto dell'applicazione](how-to-configure-the-client-for-application-package-retrieval.md).

         

## Argomenti correlati


[Application Virtualization Server](application-virtualization-server.md)

 

 





