---
title: Comprendere le opzioni di crittografia BitLocker e gli elementi di Crittografia unità BitLocker nel Pannello di controllo
description: Comprendere le opzioni di crittografia BitLocker e gli elementi di Crittografia unità BitLocker nel Pannello di controllo
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804479"
---
# Comprendere le opzioni di crittografia BitLocker e gli elementi di Crittografia unità BitLocker nel Pannello di controllo


Questo argomento descrive le **Opzioni di crittografia BitLocker** e gli elementi del pannello di controllo **crittografia unità BitLocker** e spiega quanto segue:

-   Come vengono creati questi elementi

-   Attività che consentono di eseguire

-   **Gestire BitLocker** menu di scelta rapida "fare clic con il pulsante destro del mouse", quando è visibile e nascosto e come impostarlo come visibile per impostazione predefinita

## Opzioni di crittografia BitLocker e elementi del pannello di controllo crittografia unità BitLocker


La tabella seguente elenca le attività che è possibile eseguire da ogni elemento del pannello di controllo e descrive il modo in cui vengono creati questi elementi.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Opzioni di crittografia BitLocker (MBAM)</th>
<th align="left">Crittografia unità BitLocker (Windows)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Attività che è possibile eseguire</p></td>
<td align="left"><ul>
<li><p>Cambiare il PIN o la password</p></li>
<li><p>Controllare lo stato di crittografia per un'unità</p></li>
<li><p>Aprire la console di gestione TPM</p></li>
<li><p>Attiva BitLocker</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Sospendere la protezione per un'unità</p></li>
<li><p>Eseguire il backup del tasto di ripristino</p></li>
<li><p>Cambiare il PIN</p></li>
<li><p>Disattivare BitLocker per un'unità</p></li>
<li><p>Attivare BitLocker per un'unità</p></li>
<li><p>Aprire la console di gestione TPM</p></li>
<li><p>Decrittografare un'unità (viene visualizzata solo se il client MBAM non è installato)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Come viene creata l'elemento del pannello di controllo</p></td>
<td align="left"><p>Creato nel pannello di controllo quando si installa il client MBAM. Questo elemento non può essere nascosto.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questo elemento viene visualizzato oltre a, ma non sostituisce, l'elemento del pannello di controllo crittografia unità BitLocker predefinito.</p>
</div>
<div>

</div></td>
<td align="left"><p>Viene visualizzato per impostazione predefinita nel pannello di controllo come parte del sistema operativo Windows, ma è possibile nasconderlo.</p>
<p>Per nasconderlo, vedere <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> nascondere l'elemento di crittografia unità BitLocker predefinito nel pannello di controllo </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a>Menu di scelta rapida "Gestisci BitLocker"


La tabella seguente descrive il modo in cui il menu di scelta rapida **Gestisci BitLocker** è diverso a seconda che il client mbam sia installato. Il termine "menu di scelta rapida" si riferisce alle opzioni visualizzate quando si fa clic con il pulsante destro del mouse su un'unità in Esplora risorse.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Quando viene installato MBAM client</th>
<th align="left">Quando MBAM client non è installato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Visibilità del menu di scelta rapida</p></td>
<td align="left"><p>L'opzione Gestisci BitLocker è nascosta.</p>
<p>Per rendere visibile l'opzione Gestisci BitLocker dal menu di scelta rapida, in cui viene visualizzata l'opzione per decrittografare un'unità, eliminare la chiave del registro di sistema seguente:</p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p>L'opzione Gestisci BitLocker viene visualizzata nel menu di scelta rapida.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cosa possono fare gli utenti</p></td>
<td align="left"><p>Con il collegamento nascosto, gli utenti possono aprire l'elemento del pannello di controllo crittografia unità BitLocker, ma l'opzione per decrittografare un'unità non è disponibile.</p></td>
<td align="left"><p>Con il collegamento visibile, selezionando l' <strong> opzione Gestisci BitLocker </strong> si apre l'elemento del pannello di controllo crittografia unità BitLocker, che Visualizza l'opzione per decrittografare un'unità.</p></td>
</tr>
</tbody>
</table>




## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 2.5](administering-mbam-25-features.md)



## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





