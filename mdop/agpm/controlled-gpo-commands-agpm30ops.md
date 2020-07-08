---
title: Comandi dell'oggetto Criteri di gruppo controllati
description: Comandi dell'oggetto Criteri di gruppo controllati
author: dansimp
ms.assetid: 82db4772-154a-4a8d-99cd-2c69e1738698
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8e537751107a2796727e5ed71511649b6bce953a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818876"
---
# Comandi dell'oggetto Criteri di gruppo controllati


Scheda **controllata** :

-   Consente di visualizzare un elenco degli oggetti Criteri di gruppo gestiti da Advanced Group Policy Management.

-   Fornisce un menu di scelta rapida con comandi per la gestione degli oggetti Criteri di ricerca e per la visualizzazione della cronologia e dei report per GPO.

-   Visualizza un elenco dei gruppi e degli utenti che hanno l'autorizzazione per accedere a un oggetto Criteri di gruppo selezionato.

Facendo clic con il pulsante destro del mouse sull'elenco **oggetti Criteri di gruppo** in questa scheda viene visualizzato un menu di scelta rapida, che include le opzioni seguenti.

## Controllo e cronologia


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
<td align="left"><p>Creare un nuovo GPO con controllo delle modifiche gestito tramite Advanced Group Policy Management e distribuirlo nell'ambiente di produzione. Se non si dispone dell'autorizzazione per creare un GPO, verrà richiesto di inviare una richiesta. (Questa opzione viene visualizzata se non è selezionato alcun GPO quando si fa clic con il pulsante destro del <strong> mouse Elenco oggetti Criteri di gruppo </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Cronologia</strong></p></td>
<td align="left"><p>Aprire una finestra che elenca tutte le versioni dell'oggetto Criteri di stato selezionato salvate nell'archivio. Nella cronologia è possibile ottenere un report delle impostazioni in un oggetto Criteri di confronto, confrontare due versioni di un oggetto Criteri di confronto, confrontare un oggetto Criteri di un modello o eseguire il rollback a una versione precedente di un oggetto Criteri di stato.</p></td>
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
<td align="left"><p>Genera un report basato su HTML o basato su XML che visualizza le impostazioni all'interno dell'oggetto Criteri di stato selezionato o Visualizza i collegamenti ai GPO selezionati dalle unità organizzative a partire dal momento in cui l'oggetto o i GPO sono stati controllati, importati o archiviati più di recente.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Differenze</strong></p></td>
<td align="left"><p>Genera un report basato su HTML o basato su XML per confrontare le impostazioni in due GPO selezionati o nell'oggetto Criteri di un modello selezionato.</p></td>
</tr>
</tbody>
</table>

 

## Modifica


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
<td align="left"><p><strong>Modifica</strong></p></td>
<td align="left"><p>Aprire la <strong> finestra Editor gestione criteri </strong> di gruppo per apportare modifiche al GPO selezionato.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Estrarre</strong></p></td>
<td align="left"><p>Ottenere una copia dell'oggetto Criteri di ricerca selezionato dall'archivio per la modifica offline e impedire che altri utenti la modifichino finché non viene eseguito il check-in nell'archivio. (L'estrazione può essere ignorata da un amministratore della gestione avanzata Criteri di amministrazione (controllo completo).)</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Archiviare</strong></p></td>
<td align="left"><p>Controllare la versione modificata dell'oggetto Criteri di ricerca selezionato nell'archivio, in modo che gli altri editor autorizzati possano apportare modifiche o un responsabile dell'approvazione può distribuirlo nell'ambiente di produzione.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Annulla estrazione</strong></p></td>
<td align="left"><p>Restituire un GPO Estratto all'archivio senza apportare alcuna modifica.</p></td>
</tr>
</tbody>
</table>

 

## Gestione delle versioni


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
<td align="left"><p><strong>Importare dalla produzione</strong></p></td>
<td align="left"><p>Per l'oggetto Criteri di stato selezionato, copiare la versione nell'ambiente di produzione nell'archivio.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Delete</strong></p></td>
<td align="left"><p>Spostare il GPO selezionato nel cestino e indicare se abbandonare la versione distribuita (se presente) in produzione o eliminarla, nonché la versione nell'archivio. Se non si dispone dell'autorizzazione per eliminare un GPO, verrà richiesto di inviare una richiesta.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Distribuisci</strong></p></td>
<td align="left"><p>Consente di trasferire l'oggetto Criteri di stato selezionato archiviato nell'archivio nell'ambiente di produzione. Questa azione la rende attiva in rete e sovrascrive la versione precedentemente attiva del GPO, se esiste. Se non si dispone dell'autorizzazione per la distribuzione di un GPO, verrà richiesto di inviare una richiesta.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Label</strong></p></td>
<td align="left"><p>Contrassegnare l'oggetto Criteri di ricerca selezionato con un'etichetta descrittiva, ad esempio &quot; Nota bene &quot; , e commentare per la conservazione dei record. Le etichette vengono visualizzate <strong> nella </strong> colonna stato e i commenti <strong> nella </strong> colonna commento della <strong> </strong> finestra cronologia, consentendo di identificare facilmente le versioni precedenti di un oggetto Criteri di controllo identificato con una particolare etichetta, in modo da poter eseguire il rollback in caso di problemi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>Modificare il nome del GPO selezionato. Se il GPO è già stato distribuito, il nome verrà aggiornato nell'ambiente di produzione quando l'oggetto Criteri di stato viene ridistribuito.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Salva come modello</strong></p></td>
<td align="left"><p>Creare un nuovo modello in base alle impostazioni del GPO selezionato.</p></td>
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
<td align="left"><p>Aggiornare la visualizzazione della console Gestione criteri di gruppo per incorporare le eventuali modifiche. Alcune modifiche non sono visibili finché non viene aggiornata la visualizzazione.</p></td>
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

-   [Attività del responsabile approvazione](performing-approver-tasks-agpm30ops.md)

-   [Attività del revisore](performing-reviewer-tasks-agpm30ops.md)

 

 





