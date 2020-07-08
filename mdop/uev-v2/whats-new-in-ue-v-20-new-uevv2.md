---
title: Novità in UE-V 2.0
description: Novità in UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824965"
---
# Novità in UE-V 2.0


Microsoft User Experience Virtualization (UE-V) 2,0 offre queste nuove caratteristiche e funzionalità rispetto a UE-V 1,0. Le [Note sulla versione di Microsoft User Experience Virtualization (UE-v) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) contengono ulteriori informazioni sulla versione UE-v 2,0.

## La cache lato client (CSC) non è più necessaria


Questa versione di UE-V introduce il **provider di sincronizzazione**, che sostituisce il requisito della funzionalità file offline di Windows per supportare una cache lato client di impostazioni.

Mentre UE-V consente di sincronizzare le impostazioni solo quando un'applicazione è stata aperta, chiusa o quando Windows è stato bloccato o sbloccato oppure all'accesso o alla disconnessione, anche il provider di sincronizzazione...

-   Sincronizza l'applicazione locale e le impostazioni di Windows fuori banda usando "**eventi trigger**"

-   Usa un' **attività pianificata** per sincronizzare il pacchetto di archiviazione delle impostazioni in qualsiasi intervallo scelto per i requisiti aziendali (ogni 30 minuti per impostazione predefinita)

Alcune condizioni garantiscono una sincronizzazione più frequente.

-   Le impostazioni vengono sincronizzate quando l'utente fa clic sul pulsante **Sincronizza ora** nell'applicazione nuovo centro impostazioni società.

-   Il provider di sincronizzazione può anche iniziare per una singola applicazione senza attendere l'attività di sincronizzazione pianificata. Ad esempio, quando un'applicazione viene chiusa, le modifiche apportate alle impostazioni vengono scritte nella cache locale e il processo del provider di sincronizzazione viene eseguito in modo asincrono per trasferire le nuove impostazioni nella posizione di archiviazione delle impostazioni.

## Sincronizzazione delle app di Windows


Lo sviluppatore di un'app di Windows può definire le impostazioni, se presenti, da sincronizzare e queste impostazioni ora possono essere acquisite e sincronizzate con UE-V.

Per impostazione predefinita, UE-V sincronizza le impostazioni di molte delle app di Windows incluse in Windows 8 e Windows 8,1. Puoi modificare l'elenco delle app sincronizzate con Windows PowerShell, Strumentazione gestione Windows (WMI) o criteri di gruppo.

**Nota**  UE-V non sincronizza le impostazioni delle app di Windows se gli utenti del dominio collegano le credenziali di accesso al proprio account Microsoft. Questo collegamento sincronizza le impostazioni con Microsoft OneDrive in modo che UE-V Sincronizza solo le applicazioni desktop.

 

## Collegamento a un account Microsoft


La sincronizzazione delle impostazioni tramite OneDrive è una novità di Windows 8 quando è stato effettuato l'accesso con un account Microsoft o se si collega l'account Microsoft al proprio account di dominio. Se un utente di dominio USA UE-V e ha eseguito l'accesso a un account Microsoft, allora...

-   UE-V Sincronizza solo le impostazioni per le applicazioni desktop

-   L'account Microsoft gestisce le impostazioni delle app di Windows e le impostazioni desktop di Windows

## Centro impostazioni società


Puoi offrire agli utenti un certo controllo sulle impostazioni sincronizzate tramite un'applicazione in UE-V 2 denominata centro impostazioni società. Il centro impostazioni società viene installato insieme all'agente UE-V e gli utenti possono accedervi dal pannello di controllo, dal menu **Start** o dalla schermata **Start** e dall'icona dell'area di notifica UE-v.

Il centro impostazioni società Visualizza le impostazioni sincronizzate e consente agli utenti di visualizzare lo stato di sincronizzazione di UE-V. Se si consente loro, gli utenti possono usare il centro impostazioni società per selezionare le impostazioni da sincronizzare. Possono anche fare clic sul pulsante **Sincronizza ora** per sincronizzare tutte le impostazioni immediatamente.






## Argomenti correlati


[Introduzione a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparare una distribuzione UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





