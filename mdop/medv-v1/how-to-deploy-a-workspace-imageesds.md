---
title: Come distribuire un'immagine dell'area di lavoro
description: Come distribuire un'immagine dell'area di lavoro
author: dansimp
ms.assetid: ccc8e89b-1625-4b58-837e-4c6d93d46070
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4cb16b0a4c278d135fdc9b737aa7a6e9b46115e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827005"
---
# Come distribuire un'immagine dell'area di lavoro


Quando si usa un sistema di distribuzione del software aziendale, è possibile distribuire una nuova immagine sui computer client in uno dei modi seguenti:

-   [Download Web](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pre-staging delle immagini](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Come distribuire un'immagine dell'area di lavoro tramite il Web


**Per distribuire un'immagine dell'area di lavoro tramite il Web**

1.  Caricare l'immagine MED-V nel server.

    Per informazioni sul caricamento dell'immagine, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).

2.  Usando il sistema di distribuzione del software aziendale, installare il pacchetto client. msi di MED-V nei computer degli utenti.

    Per informazioni sull'installazione del pacchetto client. msi di MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientesds.md).

    Il client MED-V viene installato e avviato per la prima volta. Durante l'avvio iniziale, il client Scarica l'immagine dall'indirizzo del server specificato nell'installazione del client.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Come distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini


**Per distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini**

1.  Creare una cartella di immagini pre-stage e spingere l'immagine nella cartella.

    Per informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).

2.  Usando il sistema di distribuzione del software aziendale, installare il pacchetto client. msi di MED-V nei computer degli utenti.

    Per informazioni sull'installazione del pacchetto client. msi di MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientesds.md).

    Il client MED-V viene installato e avviato per la prima volta. Durante l'avvio iniziale, il client recupera l'immagine dalla cartella pre-Stage specificata nell'installazione del client.

## Argomenti correlati


[Come configurare il server di distribuzione Web di immagini](how-to-configure-the-image-web-distribution-server.md)

 

 





