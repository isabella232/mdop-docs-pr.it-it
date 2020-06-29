---
title: Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale
description: Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale
author: dansimp
ms.assetid: 867faed6-74ce-4573-84be-8bf26e66c08c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb9ebbc0fb605f84c5a8e67fc77fd9be51b29ff4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823626"
---
# Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale


Il client MED-V può essere distribuito usando un sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager.

**Nota**  Se MED-V viene installato con Microsoft System Center Configuration Manager, quando si crea un pacchetto per MED-V, impostare la modalità di esecuzione su diritti amministrativi.

 

Prima di distribuire MED-V usando un sistema di distribuzione del software aziendale, verificare di aver creato un'immagine MED-V pronta per la distribuzione. Per altre informazioni sulla creazione di un'immagine MED-V, vedere [creazione di un'immagine MED-v](creating-a-med-v-image.md).

Dopo aver preparato l'immagine MED-V, prendere in considerazione il metodo migliore per distribuire l'immagine nell'ambiente. L'immagine può essere distribuita in uno dei modi seguenti:

-   Caricato sul Web e distribuito tramite download Web, utilizzando facoltativamente la tecnologia di trasferimento trim.

-   Distribuiti usando la pre-staging delle immagini.

## Distribuzione dell'immagine tramite il Web


Se si distribuisce l'immagine tramite il Web, caricare l'immagine MED-V in un server di distribuzione Web delle immagini. Per informazioni sulla configurazione di un server di distribuzione Web delle immagini, vedere [come configurare il server di distribuzione Web Image](how-to-configure-the-image-web-distribution-server.md). Per informazioni sul caricamento di un'immagine nel server, vedere [come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md).

## Distribuzione dell'immagine tramite pre-staging


Se si sta distribuendo l'immagine tramite pre-staging delle immagini, configurare la cartella pre-stage e premere l'immagine MED-V nella cartella. Per altre informazioni sulla configurazione della pre-staging delle immagini, vedere [come configurare la pre-staging delle immagini](how-to-configure-image-pre-staging.md).

**Nota**  Se si usa la pre-staging delle immagini, è importante configurare la cartella di pre-stage dell'immagine prima di spingere il pacchetto client. msi. Il percorso della cartella deve essere incluso nel pacchetto client. msi.

 

Infine, premi il pacchetto client. MSI usando il centro di distribuzione del software aziendale. È quindi possibile installare MED-V e distribuire l'immagine. Per altre informazioni sull'installazione di client MED-V, vedere [come installare client Med-v](how-to-install-med-v-clientesds.md). Per altre informazioni sulla distribuzione dell'immagine, vedere [come distribuire un'immagine dell'area di lavoro](how-to-deploy-a-workspace-imageesds.md).

 

 





