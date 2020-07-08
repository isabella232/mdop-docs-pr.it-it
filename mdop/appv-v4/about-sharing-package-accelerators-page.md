---
title: Pagina Informazioni sulla condivisione degli Acceleratori pacchetto
description: Pagina Informazioni sulla condivisione degli Acceleratori pacchetto
author: dansimp
ms.assetid: 9630cde0-e2c3-476f-8fa1-58b3c9f7d3f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 34fe55d910a7532f011b239ff5b8162aa9240f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819995"
---
# Pagina Informazioni sulla condivisione degli Acceleratori pacchetto


Le informazioni seguenti forniscono informazioni sulle procedure consigliate per condividere gli acceleratori di pacchetto. Se si prevede di condividere i file degli acceleratori di pacchetto, le informazioni come i nomi di computer, le informazioni sugli account utente e le informazioni sulle applicazioni incluse nelle trasformazioni potrebbero essere incluse nel file degli acceleratori di pacchetto. È consigliabile esaminare le impostazioni o i file di configurazione associati al pacchetto di applicazione virtuale per assicurarsi che le applicazioni non contengano informazioni personali. Questa pagina contiene gli elementi seguenti.

-   **Username**. Quando si accede al computer che utilizza Microsoft App-V Sequencer, è necessario usare un account utente generico, ad esempio l'account di **amministratore** predefinito. Non usare un account basato su un nome utente esistente.

-   **Nome computer**. Specificare un nome generale non Identificativo del computer che usa il sequencer.

-   **URL del server**. Nella scheda **distribuzione** della console App-V Sequencer usare le impostazioni predefinite per le informazioni di configurazione dell'URL del server.

-   **Applicazioni**. Se non si vuole condividere l'elenco delle applicazioni installate nel computer che esegue il sequencer quando è stato creato l'acceleratore del pacchetto, è necessario eliminare il file **appv\_manifest.xml** . Questo file si trova nella directory radice del pacchetto del pacchetto di applicazione virtuale.

## Argomenti correlati


[Procedura guidata Crea Acceleratore pacchetto (AppV 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

[Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md)

 

 





