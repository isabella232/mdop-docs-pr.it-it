---
title: Come creare e usare un modello di progetto
description: Come creare e usare un modello di progetto
author: dansimp
ms.assetid: e5ac1dc8-a88f-4b16-8e3c-df07ef5e4c3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de3471eca39d3804e8c5f070c5ec37560fae5dc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805584"
---
# Come creare e usare un modello di progetto


Puoi usare un modello di progetto App-V 5,1 per salvare le impostazioni comunemente applicate associate a un pacchetto di applicazione virtuale esistente. Queste impostazioni possono quindi essere applicate quando crei nuovi pacchetti di applicazioni virtuali nell'ambiente. L'uso di un modello di progetto consente di semplificare il processo di creazione di pacchetti di applicazioni virtuali.

**Nota**  
È possibile e spesso deve applicare un modello di progetto App-V 5,1 durante l'aggiornamento di un pacchetto. Se ad esempio è stata sequenziata un'applicazione con un elenco di esclusione personalizzato, è consigliabile creare e salvare un modello associato per l'uso successivo durante l'aggiornamento dell'applicazione sequenziata.



I modelli di progetto di App-V 5,1 si differenziano dagli acceleratori delle applicazioni App-V 5,1 perché gli acceleratori di applicazioni App-V 5,1 sono specifici dell'applicazione e i modelli di progetto di App-V 5,1 possono essere applicati a più applicazioni.

Usare le procedure seguenti per creare e applicare un nuovo modello.

**Per creare un modello di progetto**

1.  Per avviare l'App-V 5,1 sequencer, nel computer in cui è in corso il Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**Microsoft.

2.  **Nota**  
    Se il pacchetto di applicazione virtuale è attualmente aperto nella console sequencer di App-V 5,1, passare al passaggio 3 di questa procedura.



~~~
To open the existing virtual application package that contains the settings you want to save with the App-V 5.1 project template, click **File** / **Open**, and then click **Edit Package**. On the **Select Package** page, click **Browse** and locate the virtual application package that you want to open. Click **Edit**.
~~~

3. Nella console sequencer App-V 5,1 per salvare il file del modello, fare clic su **file**  /  **Salva come modello**. Dopo aver esaminato le impostazioni che verranno salvate con il nuovo modello, fare clic su **OK**. Specifica un nome che verrà associato al nuovo modello di progetto App-V 5,1. Fare clic su Salva.

   Il nuovo modello di progetto App-V 5,1 viene salvato nella directory specificata nel passaggio 3 di questa procedura.

**Per applicare un modello di progetto**

1.  **Importante**  
    La creazione di un pacchetto di applicazione virtuale con un modello di progetto in combinazione con un Acceleratore pacchetto non è supportata.



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. Per creare o aggiornare un nuovo pacchetto di applicazione virtuale usando un modello di progetto App-V 5,1, fare clic su **file**  /  **nuovo da modello**.

3. Per selezionare il modello di progetto che si vuole usare, passare alla directory in cui è stato salvato il modello di progetto, selezionare il modello di progetto e quindi fare clic su **Apri**.

   Creare il nuovo pacchetto di applicazione virtuale. Le impostazioni salvate con il modello specificato verranno applicate al nuovo pacchetto di applicazione virtuale che si sta creando.

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)









