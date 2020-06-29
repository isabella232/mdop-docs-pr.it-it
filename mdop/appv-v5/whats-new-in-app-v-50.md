---
title: Novità in App-V 5.0
description: Novità in App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804815"
---
# Novità in App-V 5.0


Questa sezione è dedicata agli utenti che hanno già familiarità con App-V e vogliono sapere cosa è cambiato in App-V 5,0 se non si ha già familiarità con App-V, è consigliabile iniziare leggendo [la pianificazione per l'app-v 5,0](planning-for-app-v-50-rc.md).

## Modifiche della funzionalità standard


Le sezioni seguenti contengono informazioni sulle modifiche apportate alle funzionalità standard per l'App-V 5,0.

### Modifiche ai sistemi operativi supportati

Per altre informazioni, Vedi [configurazioni supportate in App-V 5,0](app-v-50-supported-configurations.md).

## Modifiche al sequencer


Le sezioni seguenti contengono informazioni sulle modifiche apportate all'App-V 5,0 sequencer.

### Modifica specifica del sequencer

La tabella seguente mostra le informazioni sulle modifiche apportate all'App-V 5,0 sequencer

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Funzionalità sequenziatore</th>
<th align="left">Funzionalità sequencer App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Riavviare l'elaborazione</p></td>
<td align="left"><p>Quando un'applicazione richiede un riavvio, è consigliabile consentire all'applicazione di riavviare il computer in cui è in uso il sequencer. Il computer in cui viene eseguito il sequencer verrà riavviato e il sequencer riprenderà in modalità di monitoraggio.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Specifica della directory dell'applicazione virtuale</p></td>
<td align="left"><p>La directory dell'applicazione virtuale è un parametro obbligatorio. Per ottenere risultati ottimali, deve corrispondere alla directory di installazione dell'applicazione Installer. Questo comporta una maggiore compatibilità delle prestazioni e delle applicazioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modifica di tasti di scelta rapida/accordi</p></td>
<td align="left"><p>La pagina collegamenti/FTA si trova nella <strong> </strong> pagina di modifica avanzata dopo il completamento della procedura guidata di sequenziazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scheda Cronologia modifiche</p></td>
<td align="left"><p>La scheda Cambia cronologia è stata rimossa per App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scheda OSD</p></td>
<td align="left"><p>La scheda OSD è stata rimossa per App-V 5,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scheda Servizi virtuali</p></td>
<td align="left"><p>La scheda servizi virtuali è stata rimossa per App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Scheda file/file system virtuale</p></td>
<td align="left"><p>Queste schede vengono combinate e consentono di modificare i file del pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scheda Distribuzione</p></td>
<td align="left"><p>Non sono più disponibili opzioni per configurare l'URL del server nei pacchetti. È necessario configurare ora l'uso della configurazione di distribuzione o del server di gestione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Strumento convertitore pacchetti</p></td>
<td align="left"><p>È ora possibile usare PowerShell per convertire i pacchetti creati in versioni precedenti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Componente aggiuntivo/middleware</p></td>
<td align="left"><p>È possibile espandere i pacchetti padre quando si esegue la sequenziazione di un componente aggiuntivo o di un'applicazione middleware. I pacchetti di componenti aggiuntivi e middleware devono essere connessi con i gruppi di connessione in App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Output file</p></td>
<td align="left"><p>I file seguenti vengono creati con App-V 5,0, Windows Installer (. msi),. AppV, configurazione della distribuzione, configurazione utente e Report.XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrittori di compressione/sicurezza/pacchetti MSI</p></td>
<td align="left"><p>La compressione e la creazione di un file di Windows Installer (con estensione msi) sono automatiche per tutti i pacchetti e non è più possibile ignorare i descrittori di sicurezza.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Strumenti/opzioni</p></td>
<td align="left"><p>La finestra di diagnostica è stata rimossa, oltre a diverse altre impostazioni.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unità di installazione</p></td>
<td align="left"><p>Un'unità di installazione non è più necessaria quando si installa un'applicazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Flusso di OOS</p></td>
<td align="left"><p>Se non viene eseguita l'ottimizzazione del flusso, i pacchetti vengono trasmessi in errore quando richiesto dai computer che eseguono il client App-V 5,0 finché non vengono avviati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>D: &lt; /p&gt;</td>
<td align="left"><p>App-V 5,0 usa il file system nativo e non richiede più un D:.</p></td>
</tr>
</tbody>
</table>

 

## Rilevamento degli errori di sequenziazione


Il sequencer App-V 5,0 può rilevare i problemi di sequenziazione comuni durante la sequenziazione. La pagina del **report di installazione** alla fine della sequenziazione guidata Visualizza i messaggi di diagnostica categorizzati in **errori**, **avvisi**e **informazioni** in base alla gravità del problema.

Per visualizzare informazioni più dettagliate su un evento, fare doppio clic sull'elemento che si vuole rivedere nel report. I problemi di sequenziazione e i suggerimenti su come risolvere i problemi vengono visualizzati. Le informazioni contenute nel report di preparazione del sistema e nel report di installazione vengono riepilogate al termine della creazione di un pacchetto. Nell'elenco seguente sono visualizzati i tipi di problemi disponibili nel report:

-   File esclusi.

-   Informazioni sui driver.

-   Differenze di sistema COM+.

-   Conflitti side-by-Side (SxS).

-   Estensioni della shell.

-   Informazioni sui servizi non supportati.

-   DCOM.

## Gruppi di connessioni


La funzionalità App-V in precedenza nota come **composizione della famiglia dinamica** viene ora definita **gruppi di connessioni** in App-v 5,0. Per altre informazioni sull'uso dei gruppi di connessioni, vedere [gestire i gruppi di connessioni](managing-connection-groups.md).

## Funzionalità di licenza e misurazione


La funzionalità applicazione e licenze è stata rimossa in App-V 5,0. Le posizioni effettive della licenza nell'ambiente dipendono dalla licenza specifica per il titolo del software e dai diritti di utilizzo concessi dalle condizioni di licenza associate.

## Cache di file e applicazioni


Non è disponibile una cache di file o applicazioni con App-V 5,0.






## Argomenti correlati


[Informazioni su App-V 5.0](about-app-v-50.md)

 

 





