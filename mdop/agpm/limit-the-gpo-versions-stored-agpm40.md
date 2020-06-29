---
title: Limitare le versioni degli oggetti Criteri di gruppo archiviate
description: Limitare le versioni degli oggetti Criteri di gruppo archiviate
author: dansimp
ms.assetid: d802c7b6-f303-4b23-aefd-f19f1300b0ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: df6f6df2e2b1bae2cd972b67b76c27905622a723
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820616"
---
# Limitare le versioni degli oggetti Criteri di gruppo archiviate


Per impostazione predefinita, tutte le versioni di ogni oggetto Criteri di gruppo (GPO) controllato vengono mantenute nell'archivio nel server Advanced Group Policy Management. Tuttavia, puoi limitare il numero di versioni conservate per ogni GPO ed eliminare le versioni meno recenti quando tale limite viene superato. Quando vengono eliminate le versioni di GPO, un record della versione rimane nella cronologia dell'oggetto Criteri di controllo, ma la versione del GPO viene eliminata dall'archivio.

Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per limitare il numero di versioni degli oggetti Criteri di archiviazione archiviate**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nel riquadro dei dettagli fare clic sulla scheda **server Advanced Group Policy Management** .

3.  Selezionare la casella di controllo **Elimina versioni precedenti di ogni oggetto Criteri** di ricerca e digitare il numero massimo di versioni di GPO da archiviare per ogni oggetto Criteri di ricerca, senza includere la versione corrente. Per mantenere solo la versione corrente, immettere 0. Il valore massimo non deve essere maggiore di 999.

    **Importante**  Solo le versioni di GPO visualizzate nella scheda **versioni univoche** del conteggio della finestra **cronologia** verso il limite.

     

4.  Fare clic sul pulsante **applica** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura. In particolare, devi avere il **contenuto dell'elenco** e modificare le autorizzazioni di **Opzioni** per il dominio.

-   È possibile impedire l'eliminazione di una versione di un GPO contrassegnata nella cronologia come non idonea per l'eliminazione. A questo scopo, fai clic con il pulsante destro del mouse sulla versione nella cronologia del GPO e fai clic su non **eliminare**.

### Riferimenti aggiuntivi

-   [Gestione dell'archivio](managing-the-archive-agpm40.md)

 

 





