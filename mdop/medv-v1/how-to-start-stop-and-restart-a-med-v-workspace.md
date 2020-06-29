---
title: Come avviare, arrestare e riavviare un'area di lavoro MED-V
description: Come avviare, arrestare e riavviare un'area di lavoro MED-V
author: dansimp
ms.assetid: 54ce139c-8f32-499e-944b-72f123ebfd2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2739ace085a4d57d333daf7872e01a7712a7fbd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825725"
---
# Come avviare, arrestare e riavviare un'area di lavoro MED-V


**Per avviare un'area di lavoro MED-V**

1.  Nell'area di notifica fare clic con il pulsante destro del mouse sull'icona MED-V.

2.  Nel sottomenu fare clic su **Avvia area di lavoro**.

    -   Se nel computer sono in uso più aree di lavoro MED-V, viene visualizzata la finestra di **selezione dell'area di lavoro** .

        1.  Selezionare un'area di lavoro MED-V.

        2.  Selezionare la casella di controllo **Avvia l'area di lavoro selezionata senza chiedermi** di ignorare questa finestra al successivo avvio del client e per aprire automaticamente l'area di lavoro MED-V selezionata.

        3.  Fai clic su **OK**.

    Verrà visualizzata la finestra di **autenticazione avvia area di lavoro** .

    -   Se nel computer sono presenti diverse aree di lavoro MED-V e si è scelto di usare un'area di lavoro MED-V specificata, viene visualizzata la finestra visualizzata nella figura seguente.

        ![](images/medv-logon.gif)

    -   Se nel computer è presente una sola area di lavoro MED-V, l'opzione "Start last used Workspace" non è disponibile.

3.  Digitare le credenziali utente del dominio.

    **Nota**  La prima volta che viene avviata un'area di lavoro MED-V, il nome utente deve avere il formato seguente: &lt; Domain Name &gt; \\ &lt; User Name &gt; .

     

4.  Selezionare **Salva la password** per salvare la password tra le sessioni.

    **Nota**  Per abilitare la caratteristica Salva password, l'attributo EnableSavePassword deve essere impostato su true nel file ClientSettings.xml. Il file si trova nella cartella *Servers\\Configuration Server\\*

     

5.  Deselezionare la casella di controllo **Avvia ultima area di lavoro usata** per scegliere un'area di lavoro MED-V diversa.

6.  Fai clic su **OK**.

    Diverse schermate di stato vengono visualizzate a seconda della configurazione dell'area di lavoro MED-V.

    Viene visualizzata la schermata **Avvia area di lavoro** .

**Per riavviare un'area di lavoro MED-V**

1.  Quando il client è in funzione, nell'area di notifica fare clic con il pulsante destro del mouse sull'icona MED-V.

2.  Nel sottomenu fare clic su **Riavvia area di lavoro**.

    L'area di lavoro MED-V viene riavviata.

    -   In un'area di lavoro MED-V persistente, la macchina virtuale viene arrestata e quindi riavviata.

    -   In un'area di lavoro di revertible MED-V la macchina virtuale non viene effettivamente chiusa; Restituisce invece lo stato originale.

**Per arrestare un'area di lavoro MED-V**

1.  Nell'area di notifica fare clic con il pulsante destro del mouse sull'icona MED-V.

2.  Nel sottomenu fare clic su **Interrompi area di lavoro**.

    L'area di lavoro MED-V viene interrotta.

## Argomenti correlati


[Come avviare e chiudere il client MED-V](how-to-start-and-exit-the-med-v-client.md)

 

 





