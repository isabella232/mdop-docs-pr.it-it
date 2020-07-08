---
title: Novità in App-V 5.0 SP1
description: Novità in App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804810"
---
# Novità in App-V 5.0 SP1


Questa sezione è dedicata agli utenti che hanno già familiarità con App-V e vogliono sapere cosa è cambiato in App-V 5,0 SP1. Se non si ha familiarità con l'App-V, è consigliabile iniziare leggendo [la pianificazione per l'app-v 5,0](planning-for-app-v-50-rc.md).

## Modifiche della funzionalità standard


Le sezioni seguenti contengono informazioni sulle modifiche apportate alle funzionalità standard per l'App-V 5,0 SP1.

### Modifiche alle lingue supportate

Per altre informazioni, vedere [informazioni su App-V 5,0 SP1](about-app-v-50-sp1.md).

L'elenco seguente contiene altre informazioni sui nuovi Language Pack:

-   I Language Pack di App-V 5.0 SP1 vengono raggruppati nel programma di installazione di **appv\_xxx\_setup.exe** per tutti i componenti di App-v 5,0.

-   Quando si esegue il programma di installazione, verrà installato automaticamente il Language Pack più appropriato in base alle impostazioni locali del sistema operativo associato in esecuzione nel computer di destinazione.

-   Se sono necessari altri Language Pack, è necessario estrarre questi Language Pack dal programma di installazione eseguendo il comando seguente: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` . Dopo l'esecuzione, il contenuto del programma di installazione viene estratto nella posizione specificata.

-   È necessario installare il Language Pack desiderato applicando il file di installazione di Windows del Language Pack appropriato. Ad esempio, **appv\_hib\_LP\_jmmb\_x86.msi** o **appv\_hib\_LP\_jmmb\_x64.msi**, in cui **Hib** si riferisce al componente e **jmmb** fa riferimento alle impostazioni locali.

## Supporto avanzato per Microsoft Office2010


**Microsoft Office 2010, kit di sequenziazione per Application Virtualization 5,0** , consente agli utenti un'esperienza coerente con una versione virtualizzata di Microsoft office2010. Il **Kit di sequenziazione di Microsoft office 2010 per Application Virtualization 5,0** viene usato in combinazione con **Microsoft Office 2010 Deployment Kit per App-V** e offre anche il servizio di gestione delle licenze Microsoft Office2010 richiesto.






## Argomenti correlati


[Informazioni su App-V 5.0](about-app-v-50.md)

 

 





