---
title: Come configurare il server di distribuzione Web di immagini
description: Come configurare il server di distribuzione Web di immagini
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825156"
---
# Come configurare il server di distribuzione Web di immagini


Un repository di immagini è un server facoltativo usato per la distribuzione delle immagini (dove gli amministratori caricano le nuove immagini e i computer client controllano il server ogni 15 minuti e ne aggiornano l'immagine se ne è disponibile uno nuovo).

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


Un server di distribuzione delle immagini richiede le operazioni seguenti:

-   Internet Information Services (IIS): per informazioni, vedere [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).

    Durante l'aggiunta di servizi ruolo durante l'installazione di IIS, selezionare i metodi di autenticazione supportati seguenti:

    -   **Autenticazione di base**

    -   **Autenticazione di Windows**

    -   **Autenticazione del mapping dei certificati client**

    Per la configurazione di IIS, includere i seguenti elementi:

    -   Aggiungere una directory virtuale con l'alias denominato **MEDVImages**. Il percorso fisico deve puntare alla posizione delle immagini.

    -   Abilitare BITS.

    -   Aggiungere i tipi MIME seguenti:

        -   **. CKM (applicazione/ottetto-Stream)**

        -   **. index (applicazione/ottetto-Stream**)

    -   Nel sito MED-V aggiungere le autorizzazioni di lettura per **tutti gli utenti**.

    -   Riavviare IIS.

-   Estensioni del server BITS per IIS: per informazioni, vedere [installare le estensioni del server BITS](https://go.microsoft.com/fwlink/?LinkId=142996).

## Argomenti correlati


[Configurazioni supportate](supported-configurationsmedv-orientation.md)

[Progettare i repository delle immagini MED-V](design-the-med-v-image-repositories.md)

 

 





