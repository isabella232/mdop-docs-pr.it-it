---
title: Come comprimere un'immagine MED-V
description: Come comprimere un'immagine MED-V
author: dansimp
ms.assetid: e1ce2307-0f1b-4bf8-b146-e4012dc138d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a330b8feca922239691bed083767c3acc57105d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824676"
---
# Come comprimere un'immagine MED-V


Un'immagine MED-V deve essere imballata prima che possa essere aggiunta a un pacchetto di distribuzione o caricata nel server.

**Per creare un'immagine di MED-V imballata**

1.  Fare clic sul pulsante Gestione **Immagini** .

2.  Nel modulo **Immagini** , nel riquadro **Immagini imballate locali** , fare clic su **nuovo**.

3.  Nella finestra di dialogo **creazione immagine imballata** selezionare l'immagine della macchina virtuale eseguendo una delle operazioni seguenti:

    -   Nel campo **file di immagine di base** Digitare il percorso completo della directory in cui si trova l'immagine PC virtuale Microsoft predisposta per MED-V.

    -   Fare clic su **Sfoglia** per passare alla directory in cui si trova l'immagine del PC virtuale Microsoft predisposta per MED-V.

4.  Specificare il nome della nuova immagine eseguendo una delle operazioni seguenti:

    -   Nel campo **nome immagine** Digitare il nome desiderato.

        **Nota**  
        I caratteri seguenti non possono essere inclusi nel nome dell'immagine: Space " &lt; &gt; | \\ / : \* ?



~~~
    A new packed image will be created.

-   From the drop-down list, select an existing name.

    A new version of the existing image will be created.
~~~

5. Fai clic su **OK**.

   Nel computer host viene creata una nuova immagine imballata di MED-V con le proprietà definite nella tabella seguente.

**Nota**  
Nelle immagini imballate **locali** e nelle **Immagini imballate nei** riquadri del server, la versione più recente di ogni immagine viene visualizzata come nodo padre. Fare clic sul nodo padre per visualizzare tutte le altre versioni esistenti dell'immagine.



**Proprietà delle immagini imballate locali**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome immagine</p></td>
<td align="left"><p>Nome dell'immagine imballata come è stato definito quando l'amministratore ha creato l'immagine.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versione</p></td>
<td align="left"><p>La versione dell'immagine visualizzata.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Tutte le versioni precedenti vengono mantenute, a meno che non vengano eliminate.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Dimensioni file (compressi)</p></td>
<td align="left"><p>Dimensione compressa fisica dell'immagine.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dimensioni immagine (non compresso)</p></td>
<td align="left"><p>Dimensioni non compresse fisiche dell'immagine.</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Come installare il client MED-V e MED-V Management Console](how-to-install-med-v-client-and-med-v-management-console.md)

[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'immagine Virtual PC per MED-V](creating-a-virtual-pc-image-for-med-v.md)









