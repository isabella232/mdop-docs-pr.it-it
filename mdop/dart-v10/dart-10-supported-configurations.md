---
title: Configurazioni supportate di DaRT 10
description: Configurazioni supportate di DaRT 10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804750"
---
# Configurazioni supportate di DaRT 10


Questo argomento specifica il software prerequisito e i requisiti di configurazione supportati necessari per installare ed eseguire Microsoft Diagnostics and Recovery Toolset (DaRT) 10 nell'ambiente. Sono specificati sia i requisiti del sistema operativo che i requisiti di sistema necessari per eseguire il dardo 10. Per informazioni sui prerequisiti che è necessario prendere in considerazione per creare l'immagine di ripristino delle freccette, vedere [pianificazione per creare l'immagine di ripristino di Dart 10](planning-to-create-the-dart-10-recovery-image.md).

Per le configurazioni supportate che si applicano alle versioni successive, vedere la documentazione relativa alla versione applicabile.

Puoi installare DaRT in uno dei due modi. È possibile installare tutte le funzionalità in un computer dell'amministratore IT, in cui verranno eseguite tutte le attività associate al dardo in esecuzione. In alternativa, è possibile installare, nel computer amministratore, solo la funzionalità DaRT che crea l'immagine di ripristino e quindi installare la funzionalità usata per eseguire il comando DaRT (ovvero il Visualizzatore di connessioni remote DaRT) in un computer dell'help desk.

## Software prerequisiti di DaRT 10


Verificare che siano soddisfatti i prerequisiti seguenti prima di installare dardo.

### Prerequisiti computer amministratore

La tabella seguente elenca i prerequisiti di installazione per il computer dell'amministratore durante l'installazione di DaRT 10 e tutti gli strumenti DaRT.

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
<td align="left"><p><strong>Windows Development Kit o Software Development Kit (facoltativo)</strong></p></td>
<td align="left"><p>Analizzatore crash richiede gli strumenti di debug di Windows 10 da Windows Driver Kit per analizzare i file di dump della memoria.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Immagine ISO di Windows 10 64 bit o 32 bit</strong></p></td>
<td align="left"><p>Dardo richiede l'ambiente Windows Recovery Environment (Windows RE) da Windows 10 Media. Scaricare la versione a 32 bit o a 64 bit di Windows 10, a seconda del tipo di immagine di recupero delle freccette che si vuole creare. Se si supportano entrambi i tipi di sistema nell'ambiente, scaricare entrambe le versioni di Windows 10.</p></td>
</tr>
</tbody>
</table>

 

### Prerequisiti del computer help desk

La tabella seguente elenca i prerequisiti di installazione per il computer dell'help desk quando si esegue il Visualizzatore di connessioni remote di DaRT 10.

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
<td align="left"><p><strong>Visualizzatore di connessioni remote di DaRT 10</strong></p></td>
<td align="left"><p>Deve essere installato in un sistema operativo Windows 10.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Strumenti di debug per Windows</strong></p></td>
<td align="left"><p>Obbligatorio solo se si sta installando lo strumento Analizzatore crash</p></td>
</tr>
</tbody>
</table>

 

### Prerequisiti per i computer degli utenti finali

Non esiste alcun software prerequisito che deve essere installato nei computer degli utenti finali, ad eccezione del sistema operativo Windows 10.

## <a href="" id="---------dart-10-operating-system-requirements"></a> Requisiti del sistema operativo DaRT 10


### Requisiti di sistema del computer amministratore

La tabella seguente elenca i sistemi operativi supportati per l'installazione del computer dell'amministratore di DaRT 10.

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
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> Requisiti di sistema del computer help desk DaRT

Se si consente a un help desk di risolvere in modo remoto i computer, è necessario che il Visualizzatore di connessione remota sia installato nel computer dell'help desk. È possibile installare facoltativamente lo strumento Analizzatore crash nel computer dell'help desk.

DaRT 10 consente a un lavoratore dell'help desk di connettersi a un computer con freccette 10 usando il Visualizzatore di connessione remota Dart 7,0, DaRT 8,0, DaRt 8,1 o il visore remoto di DaRT 10. Il dardo 7,0, il dardo 8,0 e il dardo 8,1, i visualizzatori di connessione remota richiedono rispettivamente i sistemi operativi Windows 7, Windows 8 o Windows 8,1, mentre il Visualizzatore di connessioni remote DaRT 10 richiede Windows 10. Il Visualizzatore di connessione remota DaRT 10 e tutti gli altri strumenti DaRT 10 possono essere installati solo in un computer con Windows 10.

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
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows10 (solo con il Visualizzatore di connessione remota 10,0)</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
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
<td align="left"><p>2 GB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>Standard, Enterprise, Data Center</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

DaRT offre anche i requisiti hardware minimi seguenti per il computer dell'utente finale:

Un'unità CD o DVD o una porta USB, necessaria solo se si distribuisce un dardo nell'organizzazione usando un CD, un DVD o un dispositivo USB.

Supporto del BIOS per avviare il computer da un CD o DVD, da un'unità flash USB o da una partizione remota o di ripristino.

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> Requisiti di sistema di computer per gli utenti finali DaRT 10

La finestra del set di strumenti di diagnostica e ripristino in DaRT 10 richiede che il computer dell'utente finale usi uno dei sistemi operativi seguenti insieme alla quantità specificata di memoria di sistema disponibile per DaRT:

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
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Tutte le edizioni</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bit</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Pianificazione della distribuzione di DaRT 10](planning-to-deploy-dart-10.md)

 

 





