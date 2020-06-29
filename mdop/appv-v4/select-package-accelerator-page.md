---
title: Pagina Seleziona Acceleratore pacchetto
description: Pagina Seleziona Acceleratore pacchetto
author: dansimp
ms.assetid: 865c2702-4dfd-41ae-8cfc-3514d5f41f76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5723f8244563539c27a3fa915c1a680905e61e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815595"
---
# Pagina Seleziona Acceleratore pacchetto


Usare la pagina **Seleziona accelerazione pacchetto** per selezionare l'Acceleratore pacchetto che verrà usato per creare il nuovo pacchetto di applicazione virtuale. È necessario copiare l'Acceleratore pacchetto in una cartella nel computer in cui è in uso l'App-V Sequencer. Per altre informazioni, vedere [informazioni sugli acceleratori di pacchetti App-v (app-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).

Eseguire solo gli acceleratori pacchetto dagli editori attendibili. Gli acceleratori di pacchetto includono in genere una firma digitale. Una firma digitale è un marchio di sicurezza elettronico che consente di indicare l'autore del software e se il pacchetto è stato manomesso dopo la firma originale della trasformazione. Se si usa una trasformazione che è stata firmata digitalmente da un autore e che il Publisher ne ha verificato l'identità con un'autorità di certificazione, è possibile avere la certezza che la trasformazione venga eseguita da tale editore specifico e non sia stato modificato.

L'App-V Sequencer informa se una delle condizioni seguenti è vera:

-   La trasformazione selezionata non è stata firmata digitalmente.

-   La trasformazione selezionata è firmata da un autore che non ne ha verificato l'identità con un'autorità di certificazione.

-   La trasformazione selezionata è stata modificata dopo che è stata firmata e rilasciata digitalmente.

Se uno di questi messaggi viene visualizzato quando si usa un Acceleratore pacchetto, visitare il sito Web dell'autore degli acceleratori del pacchetto per ottenere una versione con firma digitale della trasformazione.

Questa pagina contiene gli elementi seguenti:

<a href="" id="browse"></a>**Esplora**  
Fare clic su **Sfoglia** per specificare l'acceleratore di pacchetto che verrà usato per creare il pacchetto di applicazione virtuale. Salvare l'acceleratore del pacchetto specificato localmente nel computer in cui è in corso il sequencer.

## Argomenti correlati


[Procedura guidata di Sequencer - Acceleratore pacchetto (App-V 4.6 SP1)](sequencer-wizard---package-accelerator--appv-46-sp1-.md)

 

 





