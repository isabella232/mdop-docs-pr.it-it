---
title: Come configurare le impostazioni Web per un'area di lavoro MED-V
description: Come configurare le impostazioni Web per un'area di lavoro MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827066"
---
# Come configurare le impostazioni Web per un'area di lavoro MED-V


I siti Web che possono essere visualizzati solo nelle versioni precedenti di Internet Explorer e che non sono presenti nel sistema operativo host possono essere visualizzati in versioni precedenti di Internet Explorer all'interno dell'area di lavoro MED-V. L'utente non deve aprire un browser nell'area di lavoro MED-V per visualizzare i siti Web specificati. L'utente può aprire un browser nell'host e reindirizzarlo automaticamente all'area di lavoro MED-V e viceversa.

Le procedure seguenti descrivono come è possibile impostare un elenco di regole di esplorazione Web per un'area di lavoro MED-V. Tutti i siti inclusi nelle regole possono essere visualizzati nell'area di lavoro MED-V o nell'host, come definito dall'amministratore. Tutti i siti non definiti nelle regole vengono visualizzati dall'ambiente in cui sono stati richiesti. Tuttavia, è possibile configurarli anche come gruppo, per essere visualizzati nell'area di lavoro MED-V o nell'host.

**Nota**  
Le impostazioni Web vengono applicate solo a Internet Explorer e a nessun altro browser.



Tutte le impostazioni Web sono configurate nel modulo **criteri** , nella scheda **Web** .

## Come configurare le impostazioni Web per l'area di lavoro MED-V


**Per configurare le impostazioni Web per l'area di lavoro MED-V**

1.  Fare clic sull'area di lavoro MED-V da configurare.

2.  Selezionare la casella di controllo **Sfoglia l'elenco degli URL definiti nella tabella seguente** per reindirizzare l'utente a un browser all'interno dell'area di lavoro o dell'host MED-V, quando l'utente accede a un URL conforme alle regole Web specificate.

3.  Fare clic su una delle opzioni seguenti:

    -   **Nell'area di lavoro**: reindirizza a un browser nell'area di lavoro MED-V.

    -   **Nell'host**: reindirizza a un browser nell'host.

4.  Selezionare la casella di controllo **Sfoglia tutti gli altri URL** per reindirizzare tutti gli URL esclusi dalle regole Web all'area di lavoro host o MED-V.

5.  Fare clic su una delle opzioni seguenti:

    -   **Nell'area di lavoro**: reindirizza tutti gli altri URL in un browser nell'area di lavoro MED-V.

    -   **Nell'host**: reindirizza tutti gli altri URL in un browser nell'host.

6.  Nel menu **criteri** selezionare **commit**.

## Come aggiungere una regola Web


**Per aggiungere una regola Web**

1.  Selezionare la casella di controllo **Sfoglia l'elenco degli URL definiti nella tabella seguente** per abilitare le regole di esplorazione Web.

2.  Fai clic su **Aggiungi**.

    Viene aggiunta una nuova regola Web.

3.  Configurare le proprietà della regola Web come descritto nella tabella seguente.

4.  Nel menu **criteri** selezionare **commit**.

**Proprietà Web dell'area di lavoro MED-V**

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
<td align="left"><p>Tipo</p></td>
<td align="left"><ul>
<li><p><strong>Suffisso </strong> di dominio: consente di accedere a qualsiasi indirizzo host che termina con il suffisso specificato nella <strong> </strong> proprietà Value e viene impostato in base all'opzione impostata nell' <strong> esplorazione Web </strong> .</p></li>
<li><p><strong>Prefisso IP </strong> : consente di accedere a qualsiasi indirizzo IP completo o parziale nell'intervallo del prefisso specificato nella <strong> proprietà Value </strong> e viene impostato in base all'opzione impostata nell' <strong> esplorazione Web </strong> .</p></li>
<li><p><strong>Tutti gli indirizzi locali </strong> : accedere a tutti gli indirizzi senza &#39;. &#39; e viene impostato in base all'opzione impostata in <strong> Web browsing </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Value</p></td>
<td align="left"><ul>
<li><p>Se <strong> il suffisso </strong> di dominio è selezionato nella <strong> </strong> proprietà Type, immettere un suffisso di dominio.</p>
<div class="alert">
<strong>Nota</strong><br/><ul>
<li><p>Non immettere &quot; * &quot; prima del suffisso.</p></li>
<li><p>I suffissi di dominio supportano anche gli alias.</p></li>
</ul>
</div>
<div>

</div></li>
<li><p>Se l'opzione prefisso IP è selezionata <strong> nella </strong> Proprietà tipo, immettere un indirizzo IP completo o parziale.</p></li>
</ul></td>
</tr>
</tbody>
</table>



## Come eliminare una regola Web


**Per eliminare una regola Web**

1.  Nel riquadro **Web** selezionare la regola Web da eliminare.

2.  Fare clic su **Rimuovi**.

    La regola Web viene eliminata.

## Argomenti correlati


[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









