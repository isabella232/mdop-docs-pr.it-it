---
title: Come creare una diramazione di un pacchetto
description: Come creare una diramazione di un pacchetto
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818126"
---
# Come creare una diramazione di un pacchetto


Usare questa procedura per modificare un pacchetto di applicazione sequenziale esistente in modo da poterlo eseguire affiancato al pacchetto di applicazione sequenziata originale. Questo processo è denominato branching. Quando si dirama un pacchetto di applicazione virtuale, è possibile eseguire due versioni dello stesso pacchetto. Ad esempio, puoi applicare un Service Pack a un pacchetto esistente ed eseguirlo affiancato con il pacchetto di applicazione virtuale sequenziato originale.

Usare la procedura seguente per creare un branching di un pacchetto di applicazione virtuale sequenziato.

**Per creare una succursale di un pacchetto di applicazione virtuale sequenziato**

1.  Aprire il sequencer di Microsoft Application Virtualization (App-V). Per specificare la directory di destinazione che contiene il pacchetto (con estensione SPRJ) che si vuole diramare selezionare **file**, **aprire**.

2.  Passare alla directory che contiene l'applicazione sequenziata che si prevede di diramazione e fare clic su **Apri**.

3.  Per salvare una copia del pacchetto, in App-V Sequencer selezionare **file**, **Salva con nome**. Specifica un nuovo nome univoco e specifica una nuova directory radice del pacchetto univoco per la copia del pacchetto. Fare clic su **Save**.

    **Importante**  
    Devi specificare un nuovo nome di pacchetto o sovrascrivere la versione esistente del pacchetto.



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. Dopo aver salvato la nuova versione, è possibile applicare le modifiche necessarie alla configurazione e salvare i file ICO, OSD, SFT e SPRJ associati per correggere la posizione nel server Application Virtualization (App-V).

## Argomenti correlati


[Attività per Application Virtualization Sequencer](tasks-for-the-application-virtualization-sequencer.md)









