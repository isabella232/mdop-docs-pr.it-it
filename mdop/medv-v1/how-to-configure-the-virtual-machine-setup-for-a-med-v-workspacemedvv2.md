---
title: Come configurare la macchina virtuale per un'area di lavoro MED-V
description: Come configurare la macchina virtuale per un'area di lavoro MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827075"
---
# Come configurare la macchina virtuale per un'area di lavoro MED-V


Tutte le impostazioni di configurazione della macchina virtuale sono configurate nel modulo **criteri** , nella scheda **configurazione VM** .

## Come configurare la configurazione della macchina virtuale per un'area di lavoro MED-V persistente


**Per configurare la configurazione della macchina virtuale per un'area di lavoro MED-V persistente**

1.  Fare clic su un'area di lavoro MED-V persistente da configurare.

2.  Nella sezione **configurazione di VM persistente** configurare le proprietà come descritto nella tabella seguente.

    **Nota**  
    Le proprietà di configurazione di VM persistenti sono abilitate solo per un'area di lavoro MED-V persistente.



3.  Nel menu **criteri** selezionare **commit**.

**Proprietà di configurazione della VM persistente**

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
<td align="left"><p>Eseguire l'installazione di VM</p></td>
<td align="left"><p>Selezionare questa casella di controllo per eseguire uno script di configurazione la prima volta che viene eseguita l'area di lavoro MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Editor script</p></td>
<td align="left"><p>Fare clic per configurare lo script di configurazione. Per altre informazioni, vedere <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> come configurare le azioni di script </a> .</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questo pulsante è abilitato solo quando <strong> è selezionata l'opzione Esegui script di configurazione VM </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Messaggio visualizzato durante l'esecuzione dello script</p></td>
<td align="left"><p>Messaggio da visualizzare durante l'esecuzione dello script. Se lasciato vuoto, viene visualizzato il messaggio predefinito.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questo campo è abilitato solo quando <strong> è selezionata l'opzione Esegui script di configurazione VM </strong> .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Come configurare la configurazione della macchina virtuale per un'area di lavoro di Revertible MED-V


**Per configurare la configurazione della macchina virtuale per un'area di lavoro di revertible MED-V**

1.  Fare clic su un'area di lavoro di revertible MED-V da configurare.

2.  Nella sezione **configurazione di REVERTIBLE VM** configurare le proprietà come descritto nella tabella seguente.

    **Nota**  
    Le proprietà di configurazione di revertible VM sono abilitate solo per un'area di lavoro di revertible MED-V.



3.  Nel menu **criteri** selezionare **commit**.

**Proprietà di configurazione di Revertible VM**

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
<td align="left"><p>Rinominare la VM in base al modello di nome computer</p></td>
<td align="left"><p>Selezionare questa casella di controllo per assegnare un nome univoco a ogni computer che usa l'area di lavoro MED-V in modo da poter distinguere tra più computer usando la stessa area di lavoro MED-V.</p>
<p>Per altre informazioni sulla configurazione dei nomi delle immagini del computer, vedere <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> come configurare le proprietà del modello di nome computer VM </a> .</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Esempi di configurazioni della macchina virtuale](examples-of-virtual-machine-configurationsv2.md)









