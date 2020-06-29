---
title: Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization
description: Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization
author: dansimp
ms.assetid: f3d79284-3f82-4ca3-b741-1a80b61490da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 01b85d73ed0a6a8bf723be381e947fbbc003bf6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815766"
---
# Pubblicazione delle applicazioni virtuali con server di gestione di Application Virtualization


In una distribuzione basata su un Application Virtualization Server, i pacchetti di applicazioni virtuali che sono stati sequenziati, testati e trovati distribuibili vengono copiati nella principale condivisione di contenuto per essere usati dall'Application Virtualization Management Server. Dopo aver importato i pacchetti nell'Application Virtualization Management Server, questi possono essere pubblicati agli utenti finali.

**Nota**  La condivisione di contenuto deve trovarsi nell'archivio disco allegato del server. L'uso di un dispositivo di archiviazione di rete, ad esempio una SAN o una condivisione DFS, deve essere considerato attentamente a causa dell'impatto della rete.

 

Le applicazioni vengono provisionate in gruppi di Active Directory. In genere, l'amministratore di Application Virtualization creerà gruppi di Active Directory per ogni applicazione virtuale da pubblicare e quindi aggiungerà gli utenti appropriati a tali gruppi. Quando gli utenti accedono alle proprie workstation, l'Application Virtualization Client, per impostazione predefinita, esegue un aggiornamento della pubblicazione usando le credenziali dell'utente connesso. L'utente può quindi avviare le applicazioni ovunque si trovino i tasti di scelta rapida. L'amministratore di Application Virtualization determina la posizione e il numero di tasti di scelta rapida presenti nel sistema client durante la sequenziazione dell'applicazione.

**Nota**  Un *aggiornamento della pubblicazione* è una chiamata al server di virtualizzazione dell'applicazione definita nel client di virtualizzazione dell'applicazione per determinare quali tasti di scelta rapida dell'applicazione virtuale vengono inviati al client per l'uso da parte dell'utente finale.

 

## Argomenti correlati


[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md)

[Panoramica dei componenti del sistema Application Virtualization](overview-of-the-application-virtualization-system-components.md)

[Pianificazione della soluzione di streaming in un'implementazione basata su Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)

 

 





