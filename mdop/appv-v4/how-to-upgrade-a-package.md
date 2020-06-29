---
title: Come eseguire l'aggiornamento di un pacchetto
description: Come eseguire l'aggiornamento di un pacchetto
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816505"
---
# Come eseguire l'aggiornamento di un pacchetto


Il processo di aggiornamento automatico è uguale a quello per l'aggiunta di una versione del pacchetto nella console di gestione di Application Virtualization Server. Viene eseguito un aggiornamento automatico quando si risequenzia l'applicazione in un pacchetto esistente. È quindi possibile aggiungere la nuova versione ai server per lo streaming.

Quando si aggiorna un pacchetto con una nuova versione, è possibile abbandonare la versione esistente o eliminarla e lasciarla solo quella più recente. Potrebbe essere necessario abbandonare la versione precedente per la compatibilità con i documenti legacy o in modo da poter testare la nuova versione prima di renderla disponibile per tutti gli utenti.

**Per aggiornare automaticamente un pacchetto**

1.  Copiare il nuovo file SFT nella cartella contenuto del server Application Virtualization.

    **Nota**  Se la risequenziazione non aggiunge caratteristiche che hanno modificato i file OSD (Open Software Descriptor), Icon (ICO) o Sequencer Project (SPRJ), non è necessario copiarli. Puoi includere questi file se vuoi che tutti questi file visualizzino la stessa data.

     

2.  Nel riquadro sinistro della console di gestione di Application Virtualization Server espandere **pacchetti**.

3.  Fare clic con il pulsante destro del mouse sul pacchetto che si vuole aggiornare e scegliere **Aggiungi versione**.

4.  Nella finestra di dialogo **Aggiungi versione pacchetto** cercare o digitare il nome del percorso completo per la nuova versione dell'applicazione nel **percorso completo per il campo file** . Questo deve essere un file SFT.

5.  Fai clic su **Avanti**.

6.  La finestra di dialogo **Riepilogo** Mostra il percorso del file e chiede di copiare il file se non è già stato fatto. Dopo aver verificato le informazioni, fare clic su **fine** .

    La nuova versione è ora completa e pronta per il flusso.

## Argomenti correlati


[Come gestire i pacchetti in Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





