---
title: Come creare e testare un'immagine MED-V
description: Come creare e testare un'immagine MED-V
author: dansimp
ms.assetid: 40e4aba6-12cb-4794-967d-2c09dc20d808
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f7989871a695b09c987124ab02c0143082148f3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827045"
---
# Come creare e testare un'immagine MED-V


L'amministratore di MED-V crea un'immagine MED-V in modo che possa essere caricata, associata a un'area di lavoro MED-V e quindi distribuita al client sul Web, aggiunta a un pacchetto MED-V o scaricata nel client usando un sistema di terze parti. È consigliabile creare prima di tutto un'immagine di test e testarla nel client MED-V prima di distribuirla.

Quando si crea un'immagine MED-V, viene eseguito l'esecuzione delle fasi seguenti:

1.  **Immagine di test locale**: un'immagine di base che può essere testata localmente.

2.  **Immagine imballata locale**: dopo aver testato l'immagine, l'immagine viene imballata come esisteva prima del test. Nessuna modifica apportata durante il test è inclusa nell'immagine compressa.

3.  **Immagine imballata sul server**: l'immagine compressa viene caricata nel server.

## Come creare un'immagine di test MED-V


**Per creare una nuova immagine di test MED-V**

1.  Fare clic sul pulsante Gestione **Immagini** .

    Viene visualizzato il modulo **Immagini** .

    -   Il modulo **Immagini** è costituito dai riquadri seguenti:

        -   **Immagini di test locali**: immagini decomprimete locali.

        -   **Immagini imballate locali**: tutte le immagini imballate nel computer locale.

        -   **Immagini imballate sul server**: tutte le immagini imballate e caricate nel server.

    -   Nelle immagini imballate **locali** e nelle **Immagini imballate nei** riquadri del server, la versione più recente di ogni immagine viene visualizzata come nodo padre. Fare clic sul nodo padre per visualizzare tutte le altre versioni esistenti dell'immagine.

2.  Nel riquadro **Immagini di test locali** fare clic su **nuovo**.

3.  Nella finestra di dialogo **creazione immagine di test** selezionare l'immagine della macchina virtuale che si vuole configurare come immagine di test MED-V eseguendo una delle operazioni seguenti:

    -   Nel campo file di **immagine di base** Digitare il percorso completo della directory in cui si trova l'immagine PC virtuale Microsoft predisposta per MED-V.

    -   Fare clic su **Sfoglia** per passare alla directory in cui si trova l'immagine del PC virtuale Microsoft predisposta per MED-V.

4.  Nel campo **nome immagine** Digitare o selezionare il nome desiderato.

    **Nota**  I caratteri seguenti non possono essere inclusi nel nome dell'immagine: Space " &lt; &gt; | \\ / : \* ?

     

5.  Fai clic su **OK**.

    Nel computer host viene creata una nuova immagine di test MED-V con le proprietà definite nella tabella seguente.

    Per altre informazioni sulla configurazione dell'immagine dell'area di lavoro MED-V, vedere [configurazione dei criteri di area di lavoro MED-v](configuring-med-v-workspace-policies.md).

**Proprietà delle immagini di test locali**

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
<td align="left"><p>Nome dell'immagine di test come è stato definito quando l'amministratore ha creato l'immagine.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Percorso immagine</p></td>
<td align="left"><p>Percorso locale dell'immagine di test.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Creato</p></td>
<td align="left"><p>Data in cui è stata creata l'immagine di test.</p></td>
</tr>
</tbody>
</table>

 

## Come testare un'immagine MED-V dal client MED-V


Dopo aver creato un'immagine di test MED-V, usare la procedura seguente per testare localmente l'immagine.

**Per testare un'immagine MED-V**

1.  Fare clic sul pulsante Gestione **criteri** .

2.  Nel modulo **criteri** assegnare l'immagine di test med-v a un'area di lavoro MED-v eseguendo le operazioni seguenti:

    1.  Fare clic sulla scheda **macchina virtuale** .

    2.  Nel campo **immagine assegnata** selezionare l'immagine di test MED-V creata. Se l'immagine di test non è presente nell'elenco, fare clic su **Aggiorna**.

    3.  Sulla barra degli strumenti fare clic su **Salva modifiche**.

3.  Configurare le altre impostazioni dell'area di lavoro MED-V da testare. Per altre informazioni, vedere [configurazione dei criteri di area di lavoro MED-V](configuring-med-v-workspace-policies.md).

4.  Avviare client MED-V.

5.  Nella casella **conferma test di verifica in corso** fare clic su **Usa immagine di test**.

6.  Testare l'immagine di test dell'area di lavoro MED-V.

    Per informazioni su come avviare ed eseguire client MED-V, vedere [operazioni client Med-v](med-v-client-operations.md).

**Nota**  Durante il test di un'immagine, non aprire VPC e apportare modifiche all'immagine.

 

**Nota**  Quando si esegue il test di un'immagine, nessuna modifica viene salvata nell'immagine tra le sessioni. al contrario, vengono salvati in un file temporaneo separato. In questo modo, quando l'immagine viene imballata ed eseguita nell'ambiente di produzione, è l'immagine originale e pulita.

 

## Argomenti correlati


[Creazione di un'immagine Virtual PC per MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Configurazione dei criteri dell'area di lavoro MED-V](configuring-med-v-workspace-policies.md)

[Operazioni del client MED-V](med-v-client-operations.md)

 

 





