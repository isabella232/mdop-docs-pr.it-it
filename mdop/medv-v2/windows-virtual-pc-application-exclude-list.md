---
title: Elenco esclusioni dell'applicazione Windows Virtual PC
description: Elenco esclusioni dell'applicazione Windows Virtual PC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823695"
---
# Elenco esclusioni dell'applicazione Windows Virtual PC


In alcuni casi potrebbe non essere necessario che le applicazioni installate nell'area di lavoro MED-V vengano pubblicate nel menu **Start** del computer host. È possibile annullare la pubblicazione di queste applicazioni seguendo le istruzioni [su come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md). Tuttavia, se il programma viene aggiornato automaticamente, potrebbe anche essere ripubblicato automaticamente. In questo modo è necessario annullare la pubblicazione dell'applicazione.

Windows Virtual PC include una caratteristica nota come "elenco di esclusione" che consente di specificare alcune applicazioni installate che non si desidera pubblicare nel menu **Start** dell'host. L'"elenco esclusioni" si trova nel registro di sistema guest nella chiave HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList ed elenca le applicazioni non pubblicate nel menu **Start** dell'host. Si può pensare all'"elenco Escludi", come se si depubblicano definitivamente le applicazioni specificate, perché gli aggiornamenti automatici delle applicazioni elencate non possono essere ripubblicati automaticamente.

## Gestione delle applicazioni tramite l'elenco Escludi in Windows Virtual PC


****

1.  Aprire l'area di lavoro MED-V a schermo intero.

    Per informazioni sull'apertura dell'area di lavoro MED-V in modalità schermo intero tramite il Toolkit di amministrazione MED-V, vedere [visualizzazione delle configurazioni dell'area di lavoro MED-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen). In alternativa, è possibile aprirlo manualmente a schermo intero facendo clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**, **Windows Virtual PC**e quindi fare doppio clic sull'area di lavoro MED-V.

2.  Nell'area di lavoro MED-V Windows Virtual PC aprire l'editor del registro di sistema.

    Fare clic sul pulsante **Start**, scegliere **Esegui**e quindi digitare regedit. Quindi fare clic su **OK**.

3.  Nell'editor del registro di sistema individuare la chiave del registro di sistema HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.

4.  Creare un nuovo valore del registro di sistema per l'applicazione installata che non si vuole pubblicare nel menu **Start** del computer host. Se ad esempio si vuole annullare la pubblicazione del programma pubblicato automaticamente in Microsoft Silverlight, eseguire le operazioni seguenti:

    1.  Con la chiave del registro di sistema VPCVAppExcludeList evidenziata, fare clic su **modifica**, su **nuovo**e quindi su **valore stringa**.

    2.  Immettere il nome del nuovo valore del registro di sistema. Ad esempio, per Microsoft Silverlight, è possibile immettere sllauncher.exe.

    3.  Fare doppio clic sul nuovo valore del registro di sistema e immettere i dati del valore.

        I dati del valore sono il percorso completo del comando che si vuole annullare la pubblicazione. Per trovare il percorso completo, fare clic con il pulsante destro del mouse sul collegamento nel menu **Start** per l'applicazione che non si vuole pubblicare e quindi scegliere **Proprietà**. Il percorso completo è elencato nella scheda **collegamento** in **destinazione**.

        Ad esempio, per il programma Microsoft Silverlight, il percorso completo potrebbe essere "C:\\Programmi \\Programmi\\microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe."

        **Importante**  Se applicabile, rimuovere le virgolette dal percorso completo quando viene immesso nel campo dati valore.

         

5.  Chiudere l'editor del registro di sistema e riavviare la macchina virtuale dell'area di lavoro MED-V.

    L'applicazione è ancora installata nell'area di lavoro MED-V, ma ora è stata rimossa dal menu **Start** del computer host.

È anche possibile ripubblicare un'applicazione esclusa nel menu **Start** dell'host eliminando il valore corrispondente dalla chiave VPCVAppExcludeList. Ad esempio, per ripubblicare Microsoft Silverlight, fare clic con il pulsante destro del mouse sul valore del registro di sistema sllauncher.exe e scegliere **Elimina**.

## Argomenti correlati


[Documentazione tecnica su MED-V](technical-reference-for-med-v.md)

[Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





