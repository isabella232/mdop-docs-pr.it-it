---
title: Configurazioni supportate di DaRT 8.0
description: Configurazioni supportate di DaRT 8.0
author: dansimp
ms.assetid: 95d68e5c-d202-4f4a-adef-d2098328172e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02c891555992652bf2a9b2b674ab8377536ef9d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823926"
---
# Configurazioni supportate di DaRT 8.0


Questo argomento specifica il software prerequisito e i requisiti di configurazione supportati necessari per installare ed eseguire Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 nell'ambiente. Vengono specificati sia i requisiti del sistema operativo che i requisiti di sistema necessari per eseguire il comando DaRT 8,0. Per informazioni sui prerequisiti che è necessario prendere in considerazione per creare l'immagine di ripristino delle freccette, vedere [pianificazione per creare l'immagine di ripristino di dart 8,0](planning-to-create-the-dart-80-recovery-image-dart-8.md).

Per le configurazioni supportate che si applicano alle versioni successive, vedere la documentazione relativa alla versione applicabile.

Puoi installare DaRT in uno dei due modi. È possibile installare tutte le funzionalità in un computer dell'amministratore IT, in cui verranno eseguite tutte le attività associate al dardo in esecuzione. In alternativa, è possibile installare, nel computer amministratore, solo la funzionalità DaRT che crea l'immagine di ripristino e quindi installare la funzionalità usata per eseguire il comando DaRT (ovvero il Visualizzatore di connessioni remote DaRT) in un computer dell'help desk.

## <a href="" id="---------dart-8-0-prerequisite-software"></a> Software prerequisiti di DaRT 8,0


Verificare che siano soddisfatti i prerequisiti seguenti prima di installare dardo.

### Prerequisiti computer amministratore

La tabella seguente elenca i prerequisiti di installazione per il computer dell'amministratore durante l'installazione di DaRT 8,0 e di tutti gli strumenti DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Windows Assessment and Development Kit (ADK)</strong></p></td>
<td align="left"><p>Obbligatorio per la creazione guidata immagine di ripristino di DaRT. Contiene gli strumenti di distribuzione, che vengono usati per personalizzare, distribuire e servire immagini di Windows e contiene l'ambiente di preinstallazione di Windows (Windows PE). ADK non è obbligatorio se si sta installando solo il Visualizzatore di connessioni remote e/o l'analizzatore di crash.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>.NET Framework 4,5</strong></p></td>
<td align="left"><p>Richiesto dalla creazione guidata immagine di ripristino di DaRT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows Development Kit o Software Development Kit (facoltativo)</strong></p></td>
<td align="left"><p>Analizzatore crash richiede gli strumenti di debug di Windows 8 da Windows Driver Kit per analizzare i file di dump della memoria.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Immagine ISO di Windows 8 64 bit</strong></p></td>
<td align="left"><p>Dardo richiede l'ambiente Windows Recovery Environment (Windows RE) da Windows 8 Media. Scaricare la versione a 32 bit o a 64 bit di Windows 8, a seconda del tipo di immagine di recupero DaRT che si vuole creare. Se si supportano entrambi i tipi di sistema nell'ambiente, scaricare entrambe le versioni di Windows 8.</p></td>
</tr>
</tbody>
</table>

 

### Prerequisiti del computer help desk

La tabella seguente elenca i prerequisiti di installazione per il computer dell'help desk quando si esegue il Visualizzatore di connessioni remote di DaRT 8,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Visualizzatore connessione remota di DaRT 8,0</strong></p></td>
<td align="left"><p>Deve essere installato in un sistema operativo Windows 8.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>NET Framework 4,5</strong></p></td>
<td align="left"><p>Richiesto dalla creazione guidata immagine di ripristino di freccette</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Strumenti di debug per Windows</strong></p></td>
<td align="left"><p>Obbligatorio solo se si sta installando lo strumento Analizzatore crash</p></td>
</tr>
</tbody>
</table>

 

### Prerequisiti per i computer degli utenti finali

Non esiste alcun software prerequisito che deve essere installato nei computer degli utenti finali, ad eccezione del sistema operativo Windows 8.

## <a href="" id="---------dart-operating-system-requirements"></a> Requisiti del sistema operativo DaRT


### Requisiti di sistema del computer amministratore

La tabella seguente elenca i sistemi operativi supportati per l'installazione del computer dell'amministratore DaRT.

**Nota**  Assicurarsi di allocare spazio sufficiente per gli eventuali strumenti aggiuntivi che si desidera installare nel computer dell'amministratore.

 

**Nota**  Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack immediatamente precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
<th align="left">Requisiti del sistema operativo</th>
<th align="left">Requisito RAM per l'uso di freccette</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise, Data Center</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>512 MB</p></td>
<td align="left"><p>1.0 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> Requisiti di sistema del computer help desk DaRT

Se si consente a un help desk di risolvere in modo remoto i computer, è necessario che il Visualizzatore di connessione remota sia installato nel computer dell'help desk. È possibile installare facoltativamente lo strumento Analizzatore crash nel computer dell'help desk.

DaRT 8,0 consente a un lavoratore dell'help desk di connettersi a un computer DaRT 8,0 usando il Visualizzatore di connessione remota Dart 7,0 o DaRT 8,0. Il Visualizzatore di connessioni remote di DaRT 7,0 richiede un sistema operativo Windows 7, mentre il Visualizzatore di connessione remota DaRT 8,0 richiede Windows 8. Il Visualizzatore di connessione remota DaRT 8,0 e tutti gli altri strumenti DaRT 8,0 possono essere installati solo in un computer che utilizza Windows 8.

La tabella seguente elenca i sistemi operativi supportati per l'installazione del computer help desk DaRT.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
<th align="left">Requisiti del sistema operativo</th>
<th align="left">Requisiti di RAM per l'uso di freccette</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8 (solo con il Visualizzatore di connessione remota 8,0)</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 (solo con il Visualizzatore di connessione remota 7,0)</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bit o 32 bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>N/D</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise, Data Center</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>51</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

DaRT offre anche i requisiti hardware minimi seguenti per il computer dell'utente finale:

Un'unità CD o DVD o una porta USB, necessaria solo se si distribuisce un dardo nell'organizzazione usando un CD, un DVD o un dispositivo USB.

Supporto del BIOS per avviare il computer da un CD o DVD, da un'unità flash USB o da una partizione remota o di ripristino.

### <a href="" id="-------------dart-end-user-computer-system-requirements"></a> Requisiti di sistema di computer per gli utenti finali di DaRT

La finestra del set di strumenti di diagnostica e ripristino in DaRT richiede che il computer dell'utente finale usi uno dei sistemi operativi seguenti insieme alla quantità specificata di memoria di sistema disponibile per DaRT:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edizione</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
<th align="left">Requisiti del sistema operativo</th>
<th align="left">Requisiti di RAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard, Enterprise, Data Center</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>512 MB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Pianificazione della distribuzione di DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





