---
title: Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli
description: Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli
author: dansimp
ms.assetid: e391fa91-3956-4150-9d43-900cfc88d543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 88c37a3723c31fb110e731084237a8d89350a4ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820775"
---
# Identificare le differenze tra oggetti Criteri di gruppo, versioni di oggetti Criteri di gruppo o modelli


Per analizzare le differenze tra gli oggetti Criteri di gruppo, i modelli o le diverse versioni di un GPO, è possibile generare report di differenze basati su HTML o su XML.

Per completare questa procedura è necessario un account utente con il ruolo di revisore, editor, approvatore o amministratore Gestione avanzata Criteri di gruppo (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

## Identificazione delle differenze tra GPO, versioni GPO o modelli


-   [Tra due GPO o modelli](#bkmk-two-gpos)

-   [Tra un GPO e un modello](#bkmk-gpo-and-template)

-   [Tra due versioni di un oggetto Criteri di stato](#bkmk-two-versions)

-   [Tra una versione di un GPO e un modello](#bkmk-gpo-version-and-template)

## <a href="" id="bkmk-two-gpos"></a>


**Per identificare le differenze tra due GPO o modelli**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).

3.  Selezionare i due GPO o i modelli.

4.  Fare clic con il pulsante destro del mouse su uno dei GPO o sui modelli, scegliere **differenze**e quindi fare clic su **report HTML** o **report XML** per visualizzare un report differenze che riepiloga le impostazioni dei GPO o modelli.

### <a href="" id="bkmk-gpo-and-template"></a>

**Per identificare le differenze tra un GPO e un modello**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).

3.  Fare clic con il pulsante destro del mouse sul GPO, scegliere **differenze**e quindi fare clic su **modello**.

4.  Selezionare il modello e il tipo di report e quindi fare clic su **OK** per visualizzare un report di differenza che riepiloga le impostazioni del GPO e del modello.

### <a href="" id="bkmk-two-versions"></a>

**Per identificare le differenze tra due versioni di un oggetto Criteri di tipo**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).

3.  Fare doppio clic sull'oggetto Criteri di confronto per visualizzarne la cronologia e quindi evidenziare le versioni da confrontare.

4.  Fare clic con il pulsante destro del mouse su una delle versioni, scegliere **differenze**e quindi fare clic su **report HTML** o **report XML** per visualizzare un report di differenza che riepiloga le impostazioni degli oggetti Criteri di stato.

### <a href="" id="bkmk-gpo-version-and-template"></a>

**Per identificare le differenze tra una versione di un GPO e un modello**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare GPO (o modelli, se si confrontano due modelli).

3.  Fare doppio clic sul GPO per visualizzarne la cronologia.

4.  Fare clic con il pulsante destro del mouse sulla versione degli oggetti Criteri di interesse, scegliere **differenze**e quindi fare clic su **modello**.

5.  Selezionare il modello e il tipo di report e quindi fare clic su **OK** per visualizzare un report di differenza che riepiloga le impostazioni della versione e del modello del GPO.

## Chiave per i report differenze


<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Simbolo</th>
<th align="left">Significato</th>
<th align="left">Colore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>L'elemento esiste con impostazioni identiche in entrambi i GPO</p></td>
<td align="left"><p>Varia in base al livello</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[#]</strong></p></td>
<td align="left"><p>L'elemento è presente in entrambi i GPO, ma con le impostazioni modificate</p></td>
<td align="left"><p>Blu</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>[-]</strong></p></td>
<td align="left"><p>L'elemento esiste solo nel primo GPO</p></td>
<td align="left"><p>Rosso</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>[+]</strong></p></td>
<td align="left"><p>L'elemento esiste solo nel secondo GPO</p></td>
<td align="left"><p>Verde</p></td>
</tr>
</tbody>
</table>

 

-   Per gli elementi con impostazioni modificate, le impostazioni modificate vengono identificate quando l'elemento viene espanso. Il valore dell'attributo in ogni oggetto Criteri di ricerca viene visualizzato nello stesso ordine in cui vengono visualizzati i GPO nel report.

-   Alcune modifiche alle impostazioni possono comportare la segnalazione di un elemento come due elementi diversi (uno presente solo nel primo GPO, uno presente solo nel secondo) anziché un elemento modificato.

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo). In particolare, è necessario disporre delle autorizzazioni per il **contenuto dell'elenco** e per le **impostazioni di lettura** per il GPO. Inoltre, per visualizzare l'elenco degli oggetti Criteri di ricerca, è necessario avere l'autorizzazione **contenuto elenco** per il dominio.

### Riferimenti aggiuntivi

-   [Attività del revisore](performing-reviewer-tasks-agpm30ops.md)

 

 





