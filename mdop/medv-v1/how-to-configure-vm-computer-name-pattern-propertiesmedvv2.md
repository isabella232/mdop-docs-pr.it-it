---
title: Come configurare le proprietà dei modelli di nome dei computer VM
description: Come configurare le proprietà dei modelli di nome dei computer VM
author: dansimp
ms.assetid: ddf79ace-8cc3-4ee6-be5a-5940b4df5c36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa171712b6624b73fb5e0756aaf56277baa4c8cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827076"
---
# Come configurare le proprietà dei modelli di nome dei computer VM


È possibile assegnare un modello di nome computer della macchina virtuale sia per revertible che per le aree di lavoro MED-V permanenti.

-   Revertible-gli amministratori possono assegnare un nome univoco a ogni istanza di area di lavoro di Revertible MED-V per distinguere tra più computer usando la stessa area di lavoro MED-V.

-   Persistente: in un'area di lavoro MED-V persistente, gli amministratori possono impostare un computer per la ridenominazione durante uno script di configurazione.

## Come assegnare un modello di nome computer della macchina virtuale a un'area di lavoro di Revertible MED-V


**Per assegnare un modello di nome computer della macchina virtuale a un'area di lavoro di revertible MED-V**

1.  Fare clic sull'area di lavoro revertible MED-V per configurare.

2.  Nella sezione **configurazione di REVERTIBLE VM** selezionare la casella di controllo **Rinomina la VM in base al modello di nome computer** .

3.  Nella sezione **modello di nome computer VM** Immetti il modello da usare per la denominazione delle immagini della macchina virtuale, usando le opzioni seguenti:

    -   **Costante**: immettere testo gratuito che sarà costante in tutti i computer che usano l'area di lavoro MED-V.

    -   **Variabile**: immettere una variabile facendo clic su **Inserisci variabile**e quindi selezionare una delle opzioni seguenti.

        -   **Nome utente**

        -   **Nome dominio**

        -   **Nome dell'host**

        -   **Nome area di lavoro**

        -   **Nome macchina virtuale**

        La variabile selezionata sarà specifica del computer che usa l'area di lavoro MED-V. Ad esempio, se è selezionato il **nome di dominio** , il nome univoco per ogni computer includerà il nome di dominio del computer.

    -   **Caratteri casuali**: immettere "\ #" per ogni carattere casuale da includere nello schema. Ogni computer che usa l'area di lavoro MED-V avrà un suffisso della lunghezza specificata, che viene generata in modo casuale.

    **Nota**  
    Il nome del computer ha un limite di 15 caratteri. Se il modello supera il limite, verrà troncato.



4.  Nel menu **criteri** selezionare **commit**.

    **Nota**  
    Un modello di nome computer VM revertible può essere assegnato solo quando si **Rinomina la VM in base ai modelli di nome computer** (nella sezione **configurazione di revertible VM** ) è selezionata.



~~~
**Note**  
A unique computer name can be assigned only if it is configured prior to MED-V workspace setup. Changing the name will not affect MED-V workspaces that were already set up.
~~~



## Come assegnare un modello di nome computer della macchina virtuale a un'area di lavoro MED-V persistente


**Per assegnare un modello di nome computer macchina virtuale a un'area di lavoro MED-V persistente**

1.  Fare clic sull'area di lavoro MED-V persistente da configurare.

2.  Nella sezione **configurazione di VM persistente** fare clic su **Editor script**.

3.  Nella finestra di dialogo **azioni script** fare clic su **Aggiungi**e quindi nel sottomenu fare clic su **Rinomina computer**.

4.  Fare clic su **OK** per chiudere la finestra di dialogo **azioni script** .

5.  Nella sezione **modello di nome computer VM** della scheda **configurazione VM** immettere il modello da usare per rinominare il computer, usando quanto segue:

    -   **Costante**: immettere testo gratuito che verrà incluso nel nome del computer.

    -   **Variabile**: immettere una variabile facendo clic su **Inserisci variabile**e quindi selezionare una delle opzioni seguenti.

        -   **Nome utente**

        -   **Nome dominio**

        -   **Nome dell'host**

        -   **Nome area di lavoro**

        -   **Nome macchina virtuale**

        La variabile selezionata sarà specifica del computer che viene rinominato. Ad esempio, se è selezionato il **nome di dominio** , il nome del computer includerà il nome di dominio del computer.

    -   **Caratteri casuali**: immettere "\ #" per ogni carattere casuale da includere nello schema. Il computer avrà un suffisso della lunghezza specificata, che viene generata in modo casuale.

    **Nota**  
    Il nome del computer ha un limite di 15 caratteri. Se il modello supera il limite, verrà troncato.



6.  Nel menu **criteri** selezionare **commit**.

    **Nota**  
    Il computer viene rinominato solo se è impostato come azione nella finestra di dialogo **azioni script** . Per informazioni dettagliate, vedere [come configurare le azioni di script](how-to-set-up-script-actions.md).



## Argomenti correlati


[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Come configurare le azioni script](how-to-set-up-script-actions.md)

[Esempi di configurazioni della macchina virtuale](examples-of-virtual-machine-configurationsv2.md)









