---
title: Come installare Sequencer
description: Come installare Sequencer
author: dansimp
ms.assetid: 5e8f1696-9bc0-4f44-8cb7-b809b2daae10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b72330718a14cb8ffb0e582c946ff1e70539036c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805373"
---
# Come installare Sequencer


Usare la procedura seguente per installare il sequencer di Microsoft Application Virtualization (App-V) 5,1. Il computer in cui viene eseguito il sequencer non deve eseguire alcuna versione del client App-V 5,1.

L'aggiornamento di un'installazione precedente di App-V Sequencer non è supportato.

**Importante**  Per un elenco completo dei requisiti del sequencer, Vedi le sezioni sequencer dei [prerequisiti App-v 5,1](app-v-51-prerequisites.md) e delle [configurazioni supportate in app-v 5,1](app-v-51-supported-configurations.md).

 

È anche possibile usare la riga di comando per installare l'App-V 5,1 Sequencer. Nell'elenco seguente vengono visualizzate informazioni sulle opzioni per l'installazione del sequencer tramite la riga di comando e **appv\_sequencer\_setup.exe**:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/INSTALLDIR</p></td>
<td align="left"><p>Specifica la directory di installazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CEIPOPTIN</p></td>
<td align="left"><p>Consente la partecipazione al programma Microsoft Customer Experience Improvement.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Log</p></td>
<td align="left"><p>Specifica dove verrà salvato il log di installazione, la posizione predefinita è <strong> % temp% </strong> . Ad esempio, <strong> C:\ </strong>Log log. log.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/nocancel/q</p></td>
<td align="left"><p>Specifica un'installazione silenziosa o silenziosa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Uninstall</p></td>
<td align="left"><p>Specifica la rimozione del sequencer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ACCEPTEULA</p></td>
<td align="left"><p>Accetta il contratto di licenza. Questa operazione è necessaria per un'installazione automatica. Esempio di utilizzo: <strong> /AcceptEula </strong> o <strong> /ACCEPTEULA = 1 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAYOUT</p></td>
<td align="left"><p>Specifica l'azione di layout associata. Estrae anche Windows Installer (. msi) e i file di script in una cartella senza installare App-V 5,1. Nessun valore previsto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LAYOUTDIR</p></td>
<td align="left"><p>Specifica la directory del layout. Richiede un valore stringa. Esempio di utilizzo: <strong> /LAYOUTDIR = "client di virtualizzazione C:\Application" </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/? O/h o/Help</p></td>
<td align="left"><p>Visualizza la Guida associata.</p></td>
</tr>
</tbody>
</table>

 

**Per installare l'App-V 5,1 sequencer**

1.  Copiare i file di installazione del sequencer App-V 5,1 nel computer in cui verrà installato. Fare doppio clic **appv\_sequencer\_setup.exe** e quindi fare clic su **Installa**.

2.  Nella pagina **condizioni di licenza software** è necessario rivedere le condizioni di licenza. Per accettare le condizioni di licenza selezionare **Accetto le condizioni di licenza.** Fai clic su **Avanti**.

3.  In **usare Microsoft Update per semplificare la protezione e la pagina aggiornata del computer** per consentire agli aggiornamenti Microsoft selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).** Per disabilitare l'applicazione degli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**. Fai clic su **Avanti**.

4.  Nella pagina del **programma Analisi utilizzo** software per partecipare al programma selezionare **partecipa al programma Analisi utilizzo**software. Ciò consentirà di raccogliere informazioni su come si usa l'App-V 5,1. Se non si vuole partecipare al programma, selezionare non si **vuole partecipare al programma in questo momento**. Fai clic su **Installa**.

5.  Per aprire il sequencer, fare clic su **Start** e quindi su **Microsoft Application Virtualization Sequencer**.

**Per risolvere i problemi relativi all'installazione di sequencer App-V 5,1**

-   Per altre informazioni sull'installazione di Sequencer, è possibile visualizzare il log degli errori nella cartella **% Temp%** . Per rivedere i file di log, fare clic sul pulsante **Start**, digitare **% Temp%** e quindi cercare il **log di appv\_**.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

 

 





