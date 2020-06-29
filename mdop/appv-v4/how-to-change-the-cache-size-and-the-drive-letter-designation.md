---
title: Come modificare le dimensioni della cache e definire la lettera di unità
description: Come modificare le dimensioni della cache e definire la lettera di unità
author: dansimp
ms.assetid: e7d7b635-079e-41aa-a5e6-655f33b4e317
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf972f114845064ecf3027cf52d1a038dc6a5118
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818036"
---
# Come modificare le dimensioni della cache e definire la lettera di unità


È possibile modificare le dimensioni della cache e la designazione delle lettere di unità direttamente dal nodo **Application Virtualization** nella console di gestione client Application Virtualization.

**Nota**  
Dopo aver impostato la dimensione della cache, non può essere ridotta.



**Per modificare le dimensioni della cache**

1.  Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.

2.  Selezionare la scheda **file System** nella finestra di dialogo **Proprietà** . Nella sezione **impostazioni di configurazione della cache client** fare clic su uno dei pulsanti di opzione seguenti per scegliere come gestire lo spazio della cache:

    **Importante**  
    Se si seleziona l'impostazione **USA soglia spazio libero su disco** , il valore immesso imposterà le dimensioni della cache sulla dimensione totale del disco meno il numero di soglia dello spazio libero su disco immesso. Se si vuole quindi ripristinare l'uso dell'impostazione **Usa la dimensione massima della cache** , è necessario specificare un numero più grande rispetto alle dimensioni della cache esistenti. In caso contrario, verrà visualizzato l'errore "la nuova dimensione deve essere superiore alla dimensione della cache esistente".



~~~
-   **Use maximum cache size**

    Enter a numeric value from 100 to 1,048,576 (1 TB) in the **Maximum size (MB)** field to specify the maximum size of the cache. The value shown in **Reserved Cache Size** indicates the amount of cache in use.

-   **Use free disk space threshold**

    Enter a numeric value to specify the amount of free disk space, in MB, that the cache must leave available on the disk. This allows the cache to grow until the amount of free disk space reaches this limit. The value shown in **Free disk space remaining** indicates how much disk space is unused.
~~~

3. Fare clic su **OK** o su **applica** per modificare l'impostazione.

**Per modificare la denominazione della lettera dell'unità**

1.  Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.

2.  Nella scheda **file System** nella finestra di dialogo **Proprietà** , nel campo **unità da usare** , selezionare la lettera di unità desiderata nell'elenco a discesa delle lettere di unità disponibili. Questa impostazione diventa effettiva quando il computer viene riavviato.

3.  Fare clic su **OK** o su **applica** per modificare l'impostazione.

## Argomenti correlati


[Come configurare il client in Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)









