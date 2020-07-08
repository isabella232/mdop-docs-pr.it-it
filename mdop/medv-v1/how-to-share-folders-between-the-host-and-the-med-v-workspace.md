---
title: Come condividere le cartelle tra l'host e l'area di lavoro MED-V
description: Come condividere le cartelle tra l'host e l'area di lavoro MED-V
author: dansimp
ms.assetid: 3cb295f2-c07e-4ee6-aa3c-ce4c8c45c191
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 87f315c9894cd38834413d2549e652a36c5cc16d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825755"
---
# Come condividere le cartelle tra l'host e l'area di lavoro MED-V


È possibile condividere cartelle tra l'host e l'area di lavoro MED-V. Le cartelle condivise possono essere archiviate in questa procedura:

-   Un computer esterno della rete

-   Il computer host

Le procedure seguenti illustrano come condividere cartelle tra l'host e l'area di lavoro MED-V.

**Per condividere le cartelle presenti nella rete**

1.  Configurare MED-V in modalità desktop completo.

2.  In gestione MED-V, nella scheda rete, fare clic su **Usa indirizzo IP diverso da host (Bridge)**.

3.  Eseguire le operazioni seguenti nel computer host:

    1.  Nel pannello di controllo fare clic su **Visualizza stato e attività della rete**e impostare **individuazione rete** **su**attivato.

    2.  Nel menu Start fare clic con il pulsante destro del mouse su **computer**e scegliere **Mappa unità di rete**.

    3.  Nella finestra di dialogo **Map Drive di rete** selezionare un'unità nel campo **unità** .

        **Nota**  Assicurarsi che la stessa lettera di unità non sia in uso in entrambi i computer.

         

    4.  Fai clic su **Browse**.

    5.  Nella finestra di dialogo **Sfoglia per la cartella** individuare l'unità condivisa e fare clic su **OK**.

    6.  Fai clic su **Fine**.

4.  Ripetere il passaggio 3 nell'area di lavoro MED-V. Posizionare il puntatore sulla stessa unità del computer host.

**Per condividere le cartelle presenti nell'host**

1.  Configurare la cartella da condividere con le autorizzazioni appropriate.

2.  Nell'area di lavoro MED-V passare a **risorse di rete** e individuare la cartella condivisa.

3.  Nell'area di lavoro MED-V individuare la cartella condivisa.

**Nota**  Assicurarsi che i computer dell'area di lavoro host e MED-V si trovino nello stesso dominio o in un gruppo.

 

 

 





