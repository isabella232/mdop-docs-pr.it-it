---
title: Pagina delle opzioni avanzate per la sequenziazione della virtualizzazione delle applicazioni
description: Pagina delle opzioni avanzate per la sequenziazione della virtualizzazione delle applicazioni
author: dansimp
ms.assetid: 2c4c5d95-d55e-463d-a851-8486f6a724f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 716fa27852f1cadfebec31a267ce1b9b581b8ff7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819596"
---
# Pagina delle opzioni avanzate per la sequenziazione della virtualizzazione delle applicazioni


Usare la pagina **Opzioni avanzate** della procedura guidata di sequenziazione della Application Virtualization (App-V) per specificare le opzioni avanzate per l'installazione dell'applicazione. La pagina contiene gli elementi descritti nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Dimensione blocco</strong></p></td>
<td align="left"><p>Consente di specificare le dimensioni dei blocchi in cui verrà suddiviso il file SFT in caso di flusso in una rete. Tutti i blocchi equivalgono alle dimensioni specificate; l'ultimo blocco potrebbe tuttavia essere più piccolo di quello specificato. Selezionare uno dei valori seguenti:</p>
<ul>
<li><p><strong>4 KB</strong></p></li>
<li><p><strong>16 KB</strong></p></li>
<li><p><strong>32 KB</strong></p></li>
<li><p><strong>64 KB</strong></p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Quando si seleziona una dimensione di blocco, prendere in considerazione le dimensioni del file SFT e la larghezza di banda della rete. Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda. I file con dimensioni di blocco più grandi potrebbero essere trasmessi più rapidamente, ma usano più larghezza di banda della rete. Grazie alla sperimentazione, è possibile individuare le dimensioni di blocco ottimali per le applicazioni di streaming della rete.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Abilitare Microsoft Update durante il monitoraggio</strong></p></td>
<td align="left"><p>Consente l'installazione di Microsoft Updates durante la sequenziazione guidata&#39;la fase di monitoraggio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rebase dll</strong></p></td>
<td align="left"><p>Consente di rimappare le raccolte di collegamenti dinamici supportate in uno spazio contiguo della RAM, salvando la memoria e migliorando le prestazioni.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Back</strong></p></td>
<td align="left"><p>Accede alla procedura guidata di sequenziazione&#39;s pagina precedente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Next</strong></p></td>
<td align="left"><p>Accede alla procedura guidata di sequenziazione&#39;s pagina successiva.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Annulla</strong></p></td>
<td align="left"><p>Termina l'operazione della procedura guidata di sequenziazione.</p></td>
</tr>
</tbody>
</table>



\ [Valore token modello \]

Usare la pagina **Opzioni avanzate** della procedura guidata di sequenziazione App-V per specificare le opzioni avanzate per l'applicazione che si sta sequenziando. Questa pagina contiene gli elementi descritti nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Consentire l'esecuzione di Microsoft Update durante il monitoraggio</strong></p></td>
<td align="left"><p>Specifica se gli aggiornamenti software verranno applicati all'applicazione durante la fase di monitoraggio della sequenziazione dell'applicazione. Questa opzione è utile se è necessario aggiornare gli aggiornamenti per completare correttamente l'installazione dell'applicazione. Questa opzione non è selezionata per impostazione predefinita.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Rebase dll</strong></p></td>
<td align="left"><p>Consente di rimappare le raccolte di collegamenti dinamici supportate in uno spazio contiguo della RAM. La selezione di questa opzione consente di gestire la memoria e migliorare le prestazioni dell'applicazione. Questa opzione non è selezionata per impostazione predefinita.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Back</strong></p></td>
<td align="left"><p>Passa alla pagina precedente della procedura guidata.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Next</strong></p></td>
<td align="left"><p>Passa alla pagina successiva della procedura guidata.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Annulla</strong></p></td>
<td align="left"><p>Elimina le impostazioni e chiude la procedura guidata.</p></td>
</tr>
</tbody>
</table>



\ [Valore token modello \]

## Argomenti correlati


[Procedura di sequenziazione guidata](sequencing-wizard.md)









