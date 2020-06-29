---
title: Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)
description: Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817486"
---
# Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)


Puoi sequenziare tre tipi di applicazioni di base usando Microsoft Application Virtualization (App-V) Sequencer.

## Per determinare il tipo di applicazione da sequenziare


Usare la tabella seguente per determinare il tipo di applicazione che deve essere sequenziato e per ottenere altre informazioni su come sequenziare l'applicazione.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di applicazione</th>
<th align="left">Descrizione</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Standard</p></td>
<td align="left"><p>Selezionare questa opzione per creare un pacchetto che contiene un'applicazione o una famiglia di applicazioni. È necessario selezionare questa opzione per la maggior parte delle applicazioni che si prevede di sequenziare.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)">Come sequenziare una nuova applicazione standard (App-V 4.6 SP1)</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Componente aggiuntivo o plug-in</p></td>
<td align="left"><p>Selezionare questa opzione per creare un pacchetto che estende la funzionalità di un'applicazione standard, ad esempio un plug-in per Microsoft Excel. È inoltre possibile usare i plug-in per le applicazioni installate nativamente o un altro pacchetto collegato tramite la composizione Dynamic Suite. Per altre informazioni sulla composizione della famiglia di prodotti dinamici, Vedi <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> come usare la composizione della famiglia dinamica </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)">Come sequenziare un nuovo componente aggiuntivo o applicazione plug-in (App-V 4.6 SP1)</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Middleware</p></td>
<td align="left"><p>Selezionare questa opzione per creare un pacchetto richiesto da un'applicazione standard, ad esempio Microsoft .NET Framework. I pacchetti middleware vengono usati per il collegamento ad altri pacchetti tramite la composizione di suite dinamiche. Per altre informazioni sulla composizione della famiglia di prodotti dinamici, Vedi <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> come usare la composizione della famiglia dinamica </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)">Come sequenziare una nuova applicazione middleware (App-V 4.6 SP1)</a></p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Attività per Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





