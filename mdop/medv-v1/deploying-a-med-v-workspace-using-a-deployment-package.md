---
title: Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione
description: Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione
author: dansimp
ms.assetid: e07fa70a-1a9f-486f-9a86-b33593b234da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc16b32fd44e45606df5502fda2e580d404dbb19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823635"
---
# Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione


L'installazione del pacchetto di distribuzione offre un metodo per installare client MED-V insieme a tutti i prerequisiti necessari e alle impostazioni predefinite dall'amministratore.

Quando si usa un pacchetto di distribuzione, il pacchetto viene distribuito tramite una rete condivisa o un supporto rimovibile. L'immagine può essere inclusa nel pacchetto o può essere distribuita separatamente.

Prima di creare un pacchetto di distribuzione, verificare di aver creato un'immagine MED-V pronta per la distribuzione. Per altre informazioni sulla creazione di un'immagine MED-V, vedere [creazione di un'immagine MED-v](creating-a-med-v-image.md).

Dopo aver preparato l'immagine MED-V, prendere in considerazione il metodo migliore per distribuire l'immagine nell'ambiente. L'immagine può essere distribuita in uno dei modi seguenti:

-   Caricato sul Web e distribuito tramite download Web, facoltativamente usando la tecnologia di trasferimento trim.

-   Distribuiti usando la pre-staging delle immagini.

-   Incluso nel pacchetto di distribuzione e distribuito insieme a tutti gli altri componenti MED-V.

Se l'immagine verrà inclusa nel pacchetto, non saranno necessarie altre configurazioni per l'immagine. Se l'immagine non verrà inclusa nel pacchetto di distribuzione, eseguire una delle operazioni seguenti:

-   Se si sta distribuendo l'immagine tramite il Web, caricare l'immagine MED-V nel server di distribuzione Web Image. Per informazioni sulla configurazione di un server di distribuzione Web delle immagini, vedere [come configurare il server di distribuzione Web Image](how-to-configure-the-image-web-distribution-server.md). Per informazioni sul caricamento di un'immagine nel server, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).

-   Se si sta distribuendo l'immagine tramite pre-staging delle immagini, configurare la cartella pre-stage e premere l'immagine MED-V nella cartella. Per altre informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).

**Nota**  Se si usa la pre-staging delle immagini, è importante configurare la cartella di pre-stage dell'immagine prima di creare il pacchetto di distribuzione. Il percorso della cartella deve essere incluso nel pacchetto di distribuzione.

 

Infine, crea il pacchetto di distribuzione. Per altre informazioni sulla creazione di un pacchetto di distribuzione, vedere [come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md). Dopo aver completato il pacchetto, distribuirlo per la distribuzione.

Una volta distribuito il pacchetto di distribuzione, è possibile installare client MED-V e distribuire l'immagine. Per altre informazioni sull'installazione di client MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientdeployment-package.md). Per altre informazioni sulla distribuzione dell'immagine, vedere [come distribuire un'immagine dell'area di lavoro](how-to-deploy-a-workspace-imagedeployment-package.md).

 

 





