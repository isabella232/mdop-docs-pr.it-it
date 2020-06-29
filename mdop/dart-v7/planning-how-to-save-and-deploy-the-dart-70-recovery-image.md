---
title: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0
description: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822796"
---
# Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0


Usare le informazioni in questa sezione quando si prevede di salvare e distribuire l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 7.

## Pianificare come salvare e distribuire l'immagine di ripristino delle freccette


Puoi salvare e distribuire l'immagine di ripristino delle freccette usando i metodi seguenti. Quando si determina il metodo che si vuole usare, valutare i vantaggi e gli svantaggi di ognuno di essi. Considera inoltre come vuoi usare il dardo nell'azienda.

**Nota**  Potresti voler usare più di un metodo nell'organizzazione. Ad esempio, è possibile avviare il dardo da una partizione remota per la maggior parte delle situazioni e avere un'unità flash USB disponibile nel caso in cui il computer dell'utente finale non possa connettersi alla rete.

 

La tabella seguente mostra alcuni vantaggi e svantaggi di ogni metodo per l'uso di DaRT nell'organizzazione.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo per l'avvio in dardo</th>
<th align="left">Vantaggi</th>
<th align="left">Svantaggi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Da CD o DVD</p></td>
<td align="left"><p>Supporta scenari in cui il record di avvio Master (MBR) è danneggiato e non è possibile accedere al disco rigido. Supporta anche i casi in cui non è disponibile una connessione di rete.</p>
<p>Questo è il più noto agli utenti di versioni precedenti di DaRT e un CD o DVD può essere masterizzato direttamente dalla <strong> procedura guidata immagine di ripristino di Dart </strong> .</p></td>
<td align="left"><p>Richiede che qualcuno con accesso al CD o al DVD sia fisicamente al computer dell'utente finale per l'avvio in DaRT.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Da un'unità flash USB</p></td>
<td align="left"><p>Offre gli stessi vantaggi dell'avvio da un CD o DVD e fornisce anche il supporto per i computer che non dispongono di unità CD o DVD.</p></td>
<td align="left"><p>È necessario formattare l'unità flash USB prima di poterla usare per l'avvio in DaRT. Richiede inoltre che qualcuno con accesso all'unità flash USB sia fisicamente al computer dell'utente finale per l'avvio in DaRT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Da una partizione remota (rete)</p></td>
<td align="left"><p>Consente di avviare il dardo senza bisogno di un CD, un DVD o un'unità flash USB. Consente inoltre di aggiornare facilmente le freccette perché è disponibile un solo percorso di file.</p></td>
<td align="left"><p>Non funziona se il computer dell'utente finale non è connesso alla rete.</p>
<p>Ampiamente disponibile per gli utenti finali e potrebbe richiedere ulteriori considerazioni sulla sicurezza quando si crea l'immagine di ripristino.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Da una partizione di ripristino</p></td>
<td align="left"><p>Consente di avviare il dardo senza bisogno di un CD, un DVD o un'unità flash USB che include istanze in cui non è disponibile una connettività di rete.</p>
<p>Può inoltre essere implementato e gestito come parte del processo di immagine Windows standard usando strumenti di distribuzione automatici, ad esempio Microsoft endpoint Configuration Manager.</p></td>
<td align="left"><p>Quando si aggiorna il dardo, è necessario aggiornare tutti i computer dell'organizzazione anziché una sola partizione (in rete) o un dispositivo (CD, DVD o memoria flash USB).</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Pianificazione della distribuzione di DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





