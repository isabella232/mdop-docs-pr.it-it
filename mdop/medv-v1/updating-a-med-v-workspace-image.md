---
title: Aggiornamento di un'immagine dell'area di lavoro MED-V
description: Aggiornamento di un'immagine dell'area di lavoro MED-V
author: dansimp
ms.assetid: 1b9c4a73-3487-43d2-98e3-43dbc79e10e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60a5d12622e0cb7012c6d0a22124d63c085f6d0a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825855"
---
# Aggiornamento di un'immagine dell'area di lavoro MED-V


Un'immagine può essere aggiornata in uno dei modi seguenti:

-   L'aggiornamento può essere inserito nel sistema operativo guest usando il sistema di distribuzione del software aziendale.

-   L'aggiornamento può essere caricato nel server di distribuzione Web Image e quindi scaricato dal client e applicato all'immagine MED-V.

-   L'immagine di base di MED-V può essere aggiornata e ridistribuita.

## <a href="" id="bkmk-howtoupdateamedvimageusinganesd"></a>Come aggiornare un'immagine MED-V usando un sistema di distribuzione del software aziendale


**Per aggiornare un'immagine MED-V usando un sistema di distribuzione del software aziendale**

-   Fare riferimento alla documentazione del sistema in uso.

## <a href="" id="bkmk-howtoupdateamedvimageusingwebdownload"></a>Come aggiornare un'immagine MED-V tramite il download Web


**Per aggiornare un'immagine MED-V tramite download Web**

1.  In gestione MED-V, nella scheda **macchina virtuale** verificare che le impostazioni seguenti vengano applicate ai criteri dell'area di lavoro MED-v associati all'immagine MED-v da aggiornare:

    -   La casella **di controllo Suggerisci aggiornamento quando è disponibile una nuova versione** è selezionata.

    -   Facoltativamente, i **client devono usare il trasferimento trim durante il download delle immagini per l'area di lavoro** selezionata.

    Per altre informazioni, vedere [come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md).

2.  Caricare l'aggiornamento delle immagini nel server di distribuzione di immagini Web.

    Tutti i client con immagini che devono essere aggiornati scaricano automaticamente l'aggiornamento e lo applicano all'immagine.

## <a href="" id="bkmk-howtoupdateamedvbaseimage"></a>Come aggiornare un'immagine di base di MED-V


**Per aggiornare un'immagine di base di MED-V**

1.  Aprire l'immagine esistente in Virtual PC2007.

2.  Apportare le modifiche necessarie all'immagine, aggiornando l'immagine, ad esempio l'installazione di un nuovo software.

3.  Chiudere Virtual PC2007.

4.  Testare l'immagine.

5.  Dopo aver testato l'immagine, imballarla nel repository locale usando lo stesso nome dell'immagine esistente.

    **Nota**  Se il nome dell'immagine è diverso rispetto alla versione esistente, verrà creata una nuova immagine invece di una nuova versione dell'immagine esistente.

     

6.  Caricare la nuova versione nel server, premerla nella cartella di pre-stage dell'immagine o distribuirla tramite un pacchetto di distribuzione.

## Argomenti correlati


[Creazione di un'immagine MED-V](creating-a-med-v-image.md)

[Come aggiornare un'immagine MED-V](how-to-update-a-med-v-image.md)

[Configurazione dei criteri dell'area di lavoro MED-V](configuring-med-v-workspace-policies.md)

[Come configurare il server di distribuzione Web di immagini](how-to-configure-the-image-web-distribution-server.md)

 

 





