---
title: Come aggiungere una versione del pacchetto
description: Come aggiungere una versione del pacchetto
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821405"
---
# Come aggiungere una versione del pacchetto


Quando si risequenzia un pacchetto in Application Virtualization Server Management Console, è possibile usare la procedura seguente per aggiungere la nuova versione ai server per lo streaming.

**Nota**  Quando si aggiorna un pacchetto con una nuova versione, è possibile abbandonare la versione esistente o eliminarla e lasciarla solo quella più recente. Potrebbe essere necessario abbandonare la versione precedente per la compatibilità con i documenti legacy o in modo da poter testare la nuova versione prima di renderla disponibile per tutti gli utenti.

 

**Per aggiungere una versione del pacchetto**

1.  Copiare il nuovo file SFT nella cartella contenuto del server applicazioni. Se la risequenziazione non è stata aggiunta alle modifiche apportate ai file OSD (Open Software Descriptor), Icon (ICO) o Sequencer Project (SPRJ), non è necessario copiarli. Puoi includere questi file se vuoi che tutti i file visualizzino la stessa data.

2.  Nel riquadro sinistro della console di gestione di Application Virtualization Server espandere il nodo **pacchetti** .

3.  Fare clic con il pulsante destro del mouse sul pacchetto che si vuole aggiornare e scegliere **Aggiungi versione**.

4.  Nella finestra di dialogo **Aggiungi versione pacchetto** cercare o digitare il nome del percorso per il nuovo file dell'applicazione nel campo **percorso completo per il file del pacchetto** . Questo deve essere un file SFT.

5.  Fai clic su **Avanti**.

6.  La finestra di dialogo **Riepilogo** Mostra il percorso del file e chiede di copiare il file se non è già stato fatto. Dopo aver verificato le informazioni, fare clic su **fine** .

    La nuova versione è ora completa e pronta per il flusso.

## Argomenti correlati


[Come eliminare un pacchetto](how-to-delete-a-packageserver.md)

[Come gestire i pacchetti in Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





