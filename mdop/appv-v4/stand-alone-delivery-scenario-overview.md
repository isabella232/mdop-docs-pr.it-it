---
title: Panoramica dello scenario di recapito autonomo
description: Panoramica dello scenario di recapito autonomo
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815306"
---
# Panoramica dello scenario di recapito autonomo


Lo scenario di recapito autonomo è una soluzione ideale per la virtualizzazione dell'applicazione per ambienti in cui una connettività a larghezza di banda ridotta o nessuna connettività limita la capacità del client Desktop Application Virtualization di eseguire lo streaming delle applicazioni da server centralizzati. In questi ambienti gli utenti lavorano spesso in remoto e i proprietari di dispositivi installano le applicazioni usando i file di Windows Installer.

Puoi usare Application Virtualization Sequencer per creare applicazioni sequenziate che includono file di Windows Installer. Questi pacchetti includono le applicazioni virtualizzate, le informazioni sulla pubblicazione e le routine di installazione necessarie per l'installazione dei pacchetti nei sistemi client. Il programma di installazione aggiunge il pacchetto dell'applicazione virtuale al client desktop Microsoft Application Virtualization. Le informazioni sulla pubblicazione sono configurate per caricare le applicazioni da una posizione locale invece che tramite una WAN. Gli utenti possono connettersi temporaneamente a una rete per recuperare i file di Windows Installer o eseguirli da un DVD.

Lo scenario di recapito autonomo offre agli utenti i vantaggi seguenti:

-   Operazione di distribuzione semplice.

-   La rete e i server non sono necessari in fase di esecuzione.

-   Applicazioni pre-memorizzate nella cache e disponibili per tutti gli utenti.

Lo scenario di recapito autonomo presenta le limitazioni seguenti:

-   Il reporting automatizzato incorporato non è disponibile. i report devono essere generati con strumenti per la creazione di report esterni.

-   Le applicazioni devono essere recapitate manualmente al client, ad esempio i file di Windows Installer originali.

## Argomenti correlati


[Come installare manualmente Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md)

 

 





