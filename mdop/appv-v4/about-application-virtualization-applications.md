---
title: Informazioni sulle applicazioni di Application Virtualization
description: Informazioni sulle applicazioni di Application Virtualization
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820086"
---
# Informazioni sulle applicazioni di Application Virtualization


Nella virtualizzazione delle applicazioni un' *applicazione* è un programma eseguibile, ad esempio Microsoft Visio, che viene trasmesso al client Desktop Application Virtualization o al client per Servizi Desktop remoto (in precedenza Servizi terminal) da un Application Virtualization Management Server. Prima di poter eseguire il flusso di un'applicazione a un client, l'applicazione deve essere preparata per il flusso tramite l'elaborazione con Application Virtualization Sequencer.

## Gestione delle applicazioni


È necessario aggiungere applicazioni al sistema prima di rendere le applicazioni disponibili per gli utenti. Il metodo più comune per l'aggiunta di applicazioni al sistema consiste nell'importarli. Per accedere a questa caratteristica, fare clic con il pulsante destro del mouse sul nodo **applicazioni** nella console di gestione di Application Virtualization Server e scegliere **Importa applicazioni**.

È possibile importare contemporaneamente più file OSD (Open Software Descriptor) oppure importare un file di progetto sequencer (SPRJ) che può contenere più file OSD. Questa funzionalità consente di configurare le applicazioni correlate in modo simile.

È anche possibile usare le caratteristiche seguenti per gestire le applicazioni:

-   **Gruppi**di applicazioni: consente di creare gruppi logici di applicazioni per la gestione semplificata. Quando si apportano modifiche a un gruppo (ad esempio le autorizzazioni di accesso), le modifiche vengono applicate a tutte le applicazioni del gruppo. Le applicazioni di un gruppo possono provenire da pacchetti diversi.

-   **Selezione multipla**: consente di selezionare più applicazioni contemporaneamente tenendo premuto il tasto CTRL quando si fa clic su un'applicazione per modificare le proprietà dell'applicazione. Tuttavia, se si vuole mantenere una relazione tra le applicazioni, è necessario creare un gruppo di applicazioni per contenere le applicazioni.

-   **Copia Cross System**: consente di copiare le applicazioni da un ambiente a un altro ambiente in cui è in esecuzione la stessa versione di App-V in un unico passaggio. Ad esempio, potresti avere un ambiente di test di accettazione degli utenti in cui devi inizialmente distribuire e configurare le applicazioni. Dopo aver terminato la fase di test, è consigliabile replicare lo stesso set di applicazioni (incluse le autorizzazioni) nell'ambiente di produzione.

## Argomenti correlati


[Informazioni sui pacchetti di Application Virtualization](about-application-virtualization-packages.md)

[Informazioni su Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[Come gestire i gruppi di applicazioni in Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[Come gestire le applicazioni in Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





