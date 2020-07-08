---
title: Determinare il metodo di pubblicazione
description: Determinare il metodo di pubblicazione
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821676"
---
# Determinare il metodo di pubblicazione


Dopo aver sequenziato un'applicazione usando l'Application Virtualization Sequencer, è necessario *pubblicare* l'applicazione per gli utenti. La pubblicazione dell'applicazione consiste nell'offrire le icone, le informazioni sulla definizione dei pacchetti e la posizione dell'origine contenuto in ogni computer in cui è stato installato il client di virtualizzazione dell'applicazione. La tabella seguente descrive i metodi di pubblicazione supportati quando si distribuisce la virtualizzazione delle applicazioni tramite un sistema ESD (Electronic Software Distribution).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Vantaggi</th>
<th align="left">Svantaggi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Genera un file di Windows Installer durante la sequenziazione, come soluzione autonoma.</p></td>
<td align="left"><ul>
<li><p>Molto semplice da usare.</p></li>
<li><p>Pacchetto caricato nella cache localmente in ogni computer.</p></li>
<li><p>Icone visualizzate per l'utente.</p></li>
<li><p>Simile alla distribuzione tradizionale del software.</p></li>
<li><p>Non è necessario per i server di streaming.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Nessuna flessibilità nella posizione del contenuto del pacchetto nei computer, stessa posizione in tutti i computer.</p></li>
<li><p>Per rimuovere le applicazioni, è necessario usare solo Aggiungi/Rimuovi programmi o msiexec.</p></li>
<li><p>Rimozione e sostituzione con la nuova versione necessaria per l'aggiornamento dei pacchetti.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Genera un file di Windows Installer durante la sequenziazione, usato con le proprietà della riga di comando modalità, carica e OVERRIDEURL e il manifesto del pacchetto.</p></td>
<td align="left"><ul>
<li><p>Semplice da usare, ma con maggiore flessibilità.</p></li>
<li><p>Icone visualizzate per l'utente.</p></li>
<li><p>Il file SFT che contiene le applicazioni può essere posizionato in una posizione di origine di flusso, con i client configurati per l'uso di tale posizione.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Flessibilità limitata: solo la posizione del contenuto del pacchetto può essere controllata in fase di esecuzione.</p></li>
<li><p>Per rimuovere l'applicazione, è necessario usare solo Aggiungi/Rimuovi programmi o msiexec.</p></li>
<li><p>Rimozione e sostituzione con la nuova versione necessaria per l'aggiornamento dei pacchetti, a meno che non si usi streaming server.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Eseguire i comandi di SFTMIME.</p></td>
<td align="left"><ul>
<li><p>Flessibilità completa: controllo completo di tutte le funzioni di gestione dei pacchetti.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>I comandi devono essere scritti per l'uso con il sistema ESD.</p></li>
<li><p>I comandi devono essere eseguiti in ogni computer in sequenza corretta.</p></li>
<li><p>Informazioni dettagliate sul linguaggio dei comandi e su una pianificazione accurata.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Per altre informazioni sull'uso di questi metodi di pubblicazione, vedere [come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md).

## Argomenti correlati


[Determinare il metodo di streaming](determine-your-streaming-method.md)

[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Panoramica di uno scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario-overview.md)

[Come pubblicare un'applicazione virtuale nel client](how-to-publish-a-virtual-application-on-the-client.md)

[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





