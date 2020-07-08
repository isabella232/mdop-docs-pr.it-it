---
title: Informazioni sulla scheda Distribuzione
description: Informazioni sulla scheda Distribuzione
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819965"
---
# Informazioni sulla scheda Distribuzione


Usare la scheda **distribuzione** nella console Application Virtualization Sequencer per modificare le informazioni relative a un'applicazione che si sta per eseguire la sequenza. Questa scheda contiene gli elementi seguenti.

## URL del server


Usare i controlli **URL del server** per specificare le impostazioni di configurazione del server delle applicazioni virtuali.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Controllo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Protocollo</strong></p></td>
<td align="left"><p>Consente di selezionare il protocollo che eseguirà il flusso del pacchetto dell'applicazione sequenziata da un server delle applicazioni virtuali a un client Desktop Application Virtualization. Sono disponibili i protocolli seguenti:</p>
<ul>
<li><p><strong>RTSP </strong> : l'impostazione predefinita specifica che il protocollo di flusso in tempo reale controlla lo scambio di applicazioni abilitate per la virtualizzazione.</p></li>
<li><p><strong>RTSPs </strong> : specifica che il protocollo di streaming in tempo reale con Transport Layer Security controlla lo scambio di un pacchetto di applicazione sequenziata.</p></li>
<li><p><strong>File </strong> : specifica che l'applicazione sequenziata verrà trasmessa da una condivisione file.</p></li>
<li><p><strong>HTTPS </strong> : specifica che il protocollo Secure Hypertext Transport controlla lo scambio di un pacchetto.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Hostname</strong></p></td>
<td align="left"><p>Consente di selezionare il server delle applicazioni virtuali o il bilanciamento del carico davanti a un gruppo di server delle applicazioni virtuali che eseguiranno il flusso del pacchetto software in un client Desktop Application Virtualization. È necessario completare questo elemento per creare un pacchetto di applicazione sequenziata, ma è possibile passare dalla variabile di ambiente% SFT_SOFTGRIDSERVER% predefinita al nome host o all'indirizzo IP effettivo di un server delle applicazioni virtuali.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se si sceglie di non specificare un nome host o un indirizzo IP statico, in ogni client Desktop Application Virtualization è necessario configurare una variabile di ambiente denominata SFT_SOFTGRIDSERVER. Il relativo valore deve essere il nome host o l'indirizzo IP del server delle applicazioni virtuali o di un bilanciamento del carico che è il client&#39;origine dell'applicazione. Devi impostare questa variabile di ambiente come variabile di sistema anziché come variabile utente. Qualsiasi sessione client Desktop Application Virtualization che viene eseguita nel computer durante l'assegnazione di questa variabile deve essere chiusa e quindi aperta in modo che la sessione ripresa venga a conoscenza della nuova origine dell'applicazione.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Port</strong></p></td>
<td align="left"><p>Consente di specificare la porta in cui il server delle applicazioni virtuali o il bilanciamento del carico ascolteranno un client Desktop Application Virtualization&#39;richiesta di s per il pacchetto. Queste informazioni sono necessarie per creare un pacchetto, ma è possibile modificarlo. La porta predefinita è 554.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Percorso</strong></p></td>
<td align="left"><p>Consente di specificare il percorso relativo nel server delle applicazioni virtuali in cui è archiviato il pacchetto software e da cui verrà trasmesso. Queste informazioni sono necessarie per creare un pacchetto se il file SFT verrà archiviato in una sottodirectory di contenuto; in caso contrario, queste informazioni non sono necessarie.</p></td>
</tr>
</tbody>
</table>



## Sistemi operativi


USA i controlli **sistemi operativi** per specificare i requisiti del sistema operativo dell'applicazione. Se un client Desktop Application Virtualization non supporta alcuno dei sistemi operativi selezionati, l'applicazione non si avvia.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Controlli</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Sistemi operativi disponibili</strong></p></td>
<td align="left"><p>Visualizza un elenco di sistemi operativi in grado di supportare le applicazioni nel pacchetto.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Sistemi operativi selezionati</strong></p></td>
<td align="left"><p>Visualizza un elenco di sistemi operativi selezionati che supportano le applicazioni nel pacchetto.</p></td>
</tr>
</tbody>
</table>



## Opzioni di output


USA i controlli delle **Opzioni di output** per specificare le opzioni di output per l'applicazione da installare.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Controllo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Algoritmo di compressione</strong></p></td>
<td align="left"><p>Consente di selezionare il metodo per comprimere il file SFT per lo streaming in una rete. Selezionare uno dei metodi di compressione seguenti:</p>
<ul>
<li><p><strong>Compresso </strong> : specifica che il file SFT deve essere compresso nel <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> </a> formato zlib.</p></li>
<li><p><strong>Non compresso </strong> : l'impostazione predefinita; specifica che il file SFT non deve essere compresso.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Applicare i descrittori di sicurezza</strong></p></td>
<td align="left"><p>Selezionare questa opzione per applicare i descrittori di sicurezza delle applicazioni nel pacchetto dopo la distribuzione nel client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Generare il pacchetto di Microsoft Windows Installer (MSI)</strong></p></td>
<td align="left"><p>Selezionare per installare o distribuire un pacchetto di applicazione sequenziata con Windows Installer. Se sono state apportate modifiche con il sequencer, le modifiche non verranno incluse nel file di Windows Installer. Il file di Windows Installer verrà sempre creato usando il file SFT salvato nel disco rigido.</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Come modificare le proprietà di distribuzione](how-to-change-deployment-properties.md)

[Console di Sequencer](sequencer-console.md)









