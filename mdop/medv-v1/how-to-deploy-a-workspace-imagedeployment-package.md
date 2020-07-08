---
title: Come distribuire un'immagine dell'area di lavoro
description: Come distribuire un'immagine dell'area di lavoro
author: dansimp
ms.assetid: b2c77e0d-101d-4956-a27c-8beb0e4f262e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d691514691286c92bd62d6fda6666345e17eb9f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827015"
---
# Come distribuire un'immagine dell'area di lavoro


Quando si usa un pacchetto di distribuzione, è possibile distribuire una nuova immagine sui computer client in uno dei modi seguenti:

-   [Download Web](#bkmk-howtodeployaworkspaceimageviatheweb)

-   [Pre-staging delle immagini](#bkmk-howtodeployaworkspaceimageusingimageprestaging)

-   [Distribuzione dell'immagine all'interno del pacchetto di distribuzione](#bkmk-howtodeployaworkspaceimageusingadeploymentapackage)

## <a href="" id="bkmk-howtodeployaworkspaceimageviatheweb"></a>Come distribuire un'immagine dell'area di lavoro tramite il Web


**Per distribuire un'immagine dell'area di lavoro tramite il Web**

1.  Caricare l'immagine MED-V nel server.

    Per informazioni sul caricamento dell'immagine, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).

2.  Creare un pacchetto di distribuzione e includere il percorso del server nella posizione dell'immagine.

    Per informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md).

3.  Distribuire il pacchetto agli utenti finali.

    Per informazioni sulla distribuzione del pacchetto, vedere [come installare client MED-V](how-to-install-med-v-clientdeployment-package.md).

    Il client MED-V viene installato e avviato per la prima volta. Durante l'avvio iniziale, il client Scarica l'immagine dall'indirizzo del server specificato nell'installazione del client.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingimageprestaging"></a>Come distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini


**Per distribuire un'immagine dell'area di lavoro usando la pre-staging delle immagini**

1.  Creare una cartella di immagini pre-stage e spingere l'immagine nella cartella.

    Per informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).

2.  Creare un pacchetto di distribuzione e includere il percorso della cartella di pre-stage dell'immagine.

    Per informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md).

3.  Distribuire il pacchetto agli utenti finali.

    Per informazioni sulla distribuzione del pacchetto, vedere [come installare client MED-V](how-to-install-med-v-clientdeployment-package.md).

    Il client MED-V viene installato e avviato per la prima volta. Durante l'avvio iniziale, il client recupera l'immagine dalla cartella pre-Stage specificata nell'installazione del client.

## <a href="" id="bkmk-howtodeployaworkspaceimageusingadeploymentapackage"></a>Come distribuire un'immagine dell'area di lavoro usando un pacchetto di distribuzione


**Per distribuire un'immagine dell'area di lavoro usando un pacchetto di distribuzione**

1.  Creare un pacchetto di distribuzione e includere l'immagine nel pacchetto.

    Per informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md).

2.  Distribuire il pacchetto agli utenti finali.

    Per informazioni sulla distribuzione del pacchetto, vedere [come installare client MED-V](how-to-install-med-v-clientdeployment-package.md).

    L'immagine viene importata nell'host come parte dell'installazione del pacchetto.

## Argomenti correlati


[Come configurare il server di distribuzione Web di immagini](how-to-configure-the-image-web-distribution-server.md)

[Come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md)

 

 





