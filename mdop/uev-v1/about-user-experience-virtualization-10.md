---
title: Informazioni su User Experience Virtualization 1.0
description: Informazioni su User Experience Virtualization 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822715"
---
# Informazioni su User Experience Virtualization 1.0


Microsoft User Experience Virtualization (UE-V) monitora le modifiche apportate dagli utenti alle impostazioni delle applicazioni e alle impostazioni del sistema operativo Windows. Le impostazioni utente vengono acquisite e centralizzate in una posizione di archiviazione delle impostazioni. Queste impostazioni possono quindi essere applicate ai diversi computer a cui l'utente ha eseguito l'accesso, inclusi i computer desktop, i computer portatili e le sessioni VDI (Virtual Desktop Infrastructure).

User Experience Virtualization usa i modelli di posizione delle impostazioni per specificare quali applicazioni e impostazioni di Windows nei computer degli utenti vengono monitorate e centralizzate. Il modello di posizione delle impostazioni è un file XML che specifica quali posizioni di file e del registro di sistema sono associate a ogni applicazione o impostazione di sistemi operativi. Il modello non contiene valori per le impostazioni; contiene solo le posizioni delle impostazioni da monitorare.

Le impostazioni dell'applicazione e le impostazioni di Windows vengono monitorate da UE-V quando gli utenti stanno lavorando ai loro computer. I valori per le impostazioni dell'applicazione sono archiviati nel server di archiviazione delle impostazioni quando l'utente chiude l'applicazione. I valori per le impostazioni di Windows vengono archiviati quando l'utente si disconnette, quando il computer è bloccato o quando si disconnette in remoto da un computer.

Un amministratore può creare un modello di posizione delle impostazioni di UE-V per specificare quali impostazioni dell'applicazione aziendale andranno in roaming. UE-V include un set di modelli di posizione delle impostazioni per alcune applicazioni Microsoft e le impostazioni di Windows. Per un elenco delle applicazioni e delle impostazioni predefinite in UE-V, vedere [pianificazione delle applicazioni da sincronizzare con UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).

## Note sulla versione di UEV 1,0


Per altre informazioni e per le ultime notizie che non hanno reso disponibile la documentazione, vedere [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1,0](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).

## Argomenti correlati


[Attività iniziali di User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Microsoft User Experience Virtualization (UE-V) 1.0](index.md)

[Architettura di alto livello per UE-V 1.0](high-level-architecture-for-ue-v-10.md)

 

 





