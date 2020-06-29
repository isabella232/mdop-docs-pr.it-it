---
title: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
description: Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino
author: dansimp
ms.assetid: 0d2192c1-4058-49fb-b0b6-baf4699ac7f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: bc5f295d35dff1e4fc2a84c47188be40153b85c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804701"
---
# Come distribuire l'immagine di ripristino di DaRT come parte di una partizione di ripristino


Dopo aver eseguito la creazione guidata immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10 e aver creato l'immagine di ripristino, è possibile estrarre il file Boot. wim dal file di immagine ISO e distribuirlo come partizione di ripristino in un'immagine di Windows 10. È consigliabile una partizione, perché i problemi di danneggiamento che impediscono l'avvio del sistema operativo Windows impediscono anche l'avvio dell'immagine di ripristino. Una partizione separata elimina inoltre la necessità di specificare due volte la chiave di ripristino di BitLocker. È consigliabile nascondere la partizione per evitare che gli utenti memorizzino i file.

**Per distribuire il dardo nella partizione di ripristino di un'immagine di Windows 10**

1.  Creare una partizione di destinazione nell'immagine di Windows 10 uguale o maggiore della dimensione del file di immagine ISO creato tramite la **creazione guidata immagine di ripristino di Dart 10**.

    La dimensione minima richiesta per una partizione DaRT è 500MB per adattare la funzionalità di connessione remota in DaRT.

2.  Estrarre il file Boot. wim dal file di immagine ISO DaRT.

    1.  Usando il metodo preferito della società, montare il file di immagine ISO creato nella pagina **Crea immagine di avvio** .

    2.  Aprire il file di immagine ISO e copiare il file Boot. wim dalla cartella \\sources nell'immagine montata in una posizione nel computer o in un'unità esterna.

        **Nota**  Se si è masterizzato un CD, un DVD o un USB dell'immagine di ripristino, è possibile aprire i file nel supporto rimovibile e copiare il file Boot. wim dalla cartella \\sources. Se si copia il file Boot. wim, non è necessario montare l'immagine.

         

3.  Usa il file Boot. wim per creare una partizione di ripristino avviabile usando il metodo standard della società per la creazione di un'immagine ripristino personalizzata di Windows.

    Per altre informazioni su come creare o personalizzare una partizione di ripristino, vedere [personalizzazione dell'esperienza Windows re](https://go.microsoft.com/fwlink/?LinkId=214222).

4.  Sostituisci la partizione di destinazione nell'immagine di Windows 10 con la partizione di ripristino.

    Per altre informazioni su come distribuire una soluzione di ripristino per reinstallare l'immagine Factory in caso di errore di sistema, vedere [distribuire un'immagine di ripristino del sistema](https://go.microsoft.com/fwlink/?LinkId=214221).

## Argomenti correlati


[Creazione dell'immagine di ripristino di DaRT 10](creating-the-dart-10-recovery-image.md)

[Distribuzione dell'immagine di ripristino di DaRT](deploying-the-dart-recovery-image-dart-10.md)

[Pianificazione di DaRT 10](planning-for-dart-10.md)

 

 





