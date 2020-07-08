---
title: Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7
description: Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827285"
---
# Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7


Puoi installare tutti i componenti MED-V in un'immagine di Windows 7 distribuita in tutta l'organizzazione come per qualsiasi nuova installazione di Windows 7. L'utente finale termina quindi l'installazione dell'area di lavoro MED-V facendo clic su un collegamento al menu **Start** configurato per avviare MED-v. La prima volta che viene avviata la configurazione e l'utente finale segue le istruzioni per completare la configurazione.

La sezione seguente contiene informazioni e istruzioni utili per distribuire l'area di lavoro MED-V in tutta l'organizzazione usando un'immagine di Windows 7.

**Per distribuire un'area di lavoro MED-V in un'immagine di Windows 7**

1.  Creare un'immagine standard di Windows 7. Per altre informazioni, vedere [creazione di un'immagine standard di Windows 7: Guida dettagliata](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .

2.  Nell'immagine di Windows 7 installare Windows Virtual PC e gli aggiornamenti di Windows Virtual PC. Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

3.  Installare l'agente host MED-V usando il file di installazione MED-V \ _HostAgent \ _Setup. Per altre informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).

    **Avviso**  Internet Explorer deve essere chiuso prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL. Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.

     

4.  Copiare i file del pacchetto dell'area di lavoro MED-V nell'immagine di Windows 7. I file del pacchetto area di lavoro MED-V sono il programma di installazione dell'area di lavoro MED-V, il file con estensione MEDV e il file setup.exe creato tramite **Packager area di lavoro MED-v**.

    **Importante**  Il file con estensione MEDV e setup.exe deve trovarsi nella stessa cartella del programma di installazione dell'area di lavoro MED-V. Installare quindi l'area di lavoro MED-V eseguendo setup.exe.

     

5.  Configurare un collegamento nel menu **Start** per aprire l'installazione del pacchetto area di lavoro MED-V.

    Creare un collegamento al menu **Start** al file setup.exe che consente all'utente finale di avviare un'installazione di MED-V come richiesto.

6.  Usando il processo di distribuzione delle immagini standard della società, distribuire l'immagine di Windows 7 ai computer dell'organizzazione che richiedono MED-V.

Quando l'utente finale deve accedere a un'applicazione pubblicata nell'area di lavoro MED-V, può fare clic sul collegamento al menu **Start** per installare l'area di lavoro MED-v. In questo modo viene avviata automaticamente la prima configurazione e viene completata la configurazione di MED-V. Dopo aver completato la configurazione per la prima volta, l'utente finale può accedere alle applicazioni MED-V nel menu **Start** .

## Argomenti correlati


[Panoramica della distribuzione di MED-V 2.0](med-v-20-deployment-overview.md)

[Come distribuire un'area di lavoro MED-V con un sistema di distribuzione elettronica del software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





