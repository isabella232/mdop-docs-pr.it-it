---
title: Comandi del modello
description: Comandi del modello
author: dansimp
ms.assetid: 2ec11b3f-0c5c-4788-97bd-bd4bf64ba51a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7de90780caa1eb938f78597a760723f89e2e55ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820185"
---
# Comandi del modello


Scheda **modelli** :

-   Visualizza un elenco di modelli disponibili che è possibile usare per creare nuovi oggetti Criteri di gruppo.

-   Fornisce un menu di scelta rapida con i comandi per la creazione di un GPO basato su un modello selezionato, sulla gestione dei modelli e sulla visualizzazione dei report per i modelli.

-   Visualizza un elenco dei gruppi e degli utenti che hanno l'autorizzazione per accedere a un modello selezionato.

Poiché un modello non può essere modificato, i modelli non hanno cronologia. Tuttavia, come per qualsiasi versione di GPO, le impostazioni di un modello possono essere visualizzate con un report di impostazioni o in confronto a un altro oggetto Criteri di tipo con un report differenze.

**Nota**  Un modello è una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO modificabili.

 

Facendo clic con il pulsante destro del mouse sull'elenco **oggetti Criteri di gruppo** in questa scheda viene visualizzato un menu di scelta rapida, che include le opzioni seguenti.

## Controllo


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Effetto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nuovo oggetto Criteri di controllo controllato</strong></p></td>
<td align="left"><p>Creare un nuovo GPO basato sul modello selezionato. È disponibile l'opzione per distribuire il nuovo GPO nell'ambiente di produzione. Se non si dispone dell'autorizzazione per creare un GPO, verrà richiesto di inviare una richiesta. (Questa opzione viene visualizzata se non è selezionato alcun GPO quando si fa clic con il pulsante destro del <strong> mouse Elenco oggetti Criteri di gruppo </strong> .</p></td>
</tr>
</tbody>
</table>

 

## Rapporti


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Effetto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Impostazioni</strong></p></td>
<td align="left"><p>Genera un report basato su HTML o basato su XML che visualizza le impostazioni nell'oggetto Criteri di stato selezionato.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Differenze</strong></p></td>
<td align="left"><p>Genera un report basato su HTML o basato su XML per confrontare le impostazioni in due modelli di GPO selezionati.</p></td>
</tr>
</tbody>
</table>

 

## Gestione dei modelli


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Effetto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Imposta come predefinito</strong></p></td>
<td align="left"><p>Imposta il modello selezionato come predefinito da usare automaticamente durante la creazione di un nuovo oggetto Criteri di gruppo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Delete</strong></p></td>
<td align="left"><p>Spostare il modello selezionato nel <strong> Cestino </strong> . Se non si dispone dell'autorizzazione per eliminare un GPO, verrà richiesto di inviare una richiesta.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>Modificare il nome del modello selezionato.</p></td>
</tr>
</tbody>
</table>

 

## Vari


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Effetto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Aggiorna</strong></p></td>
<td align="left"><p>Aggiornare la visualizzazione della console di gestione di criteri di gruppo per incorporare le eventuali modifiche. Alcune modifiche non sono visibili finché non viene aggiornata la visualizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Help</strong></p></td>
<td align="left"><p>Visualizzare la guida per Advanced Group Policy Management.</p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

-   [Scheda Contenuto](contents-tab-agpm30ops.md)

-   [Attività dell'editor](performing-editor-tasks-agpm30ops.md)

-   [Attività del revisore](performing-reviewer-tasks-agpm30ops.md)

 

 





