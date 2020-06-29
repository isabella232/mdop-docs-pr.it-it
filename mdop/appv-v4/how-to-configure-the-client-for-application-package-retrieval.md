---
title: Come configurare il client per il recupero del pacchetto dell'applicazione
description: Come configurare il client per il recupero del pacchetto dell'applicazione
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817826"
---
# Come configurare il client per il recupero del pacchetto dell'applicazione


Quando il client è configurato con un server di gestione di Application Virtualization (App-V) come server di pubblicazione, per impostazione predefinita durante il successivo ciclo di aggiornamento della pubblicazione, il client recupera dal server i file OSD (Open Software Descriptor) e del manifesto del pacchetto per ogni pacchetto che l'utente è autorizzato a usare. Il client usa le informazioni di origine del pacchetto definite in questi file per determinare dove trovare il contenuto del pacchetto, le icone e le associazioni di tipi di file.

Se si vuole che il client ottenga il contenuto del pacchetto (file SFT) da un'app locale-V Streaming Server o da un'altra origine alternativa, ad esempio un server Web o un file server, invece che da App-V Management Server, è possibile configurare il valore della chiave del registro di sistema ApplicationSourceRoot nel computer in modo che punti alla condivisione di contenuto locale nell'altro server. Il file OSD definisce ancora il percorso di origine originale per il contenuto del pacchetto. Tuttavia, il client usa il valore dell'impostazione ApplicationSourceRoot al posto del server e la condivisione specificata nel percorso di contenuto nel file OSD. Questo reindirizza il client per recuperare il contenuto dall'altro server.

È anche possibile configurare i valori della chiave del registro di sistema OSDSourceRoot e IconSourceRoot se si vuole eseguire l'override di tali impostazioni nel file manifesto del pacchetto o nei percorsi inviati da un server di pubblicazione. OSDSourceRoot specifica una posizione di origine per il recupero dei file OSD per un pacchetto di applicazione durante la pubblicazione. IconSourceRoot specifica una posizione di origine per il recupero di icone per un pacchetto di applicazione durante la pubblicazione.

**Nota**  
-   Le impostazioni IconSourceRoot e OSDSourceRoot eseguono l'override dei valori nel file manifesto del pacchetto, quindi se tenti di distribuire un pacchetto usando il metodo di file con estensione msi di Windows Installer, eseguirà anche l'override dei valori del file manifesto del pacchetto contenuto all'interno del file MSI.

-   Durante le operazioni di pubblicazione e di flusso HTTP (S), i client App-V 4,5 SP1 usano le impostazioni del server proxy configurate in Internet Explorer nel computer dell'utente.



**Per configurare il valore della chiave del registro di sistema ApplicationSourceRoot**

-   Configurare ApplicationSourceRoot nel valore della chiave del registro di sistema seguente con un percorso UNC o un URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot

    Il formato corretto per il percorso UNC (Universal Naming Convention) è **\\\\computername\\sharefolder\\\ [Folder \] \ [\ \ \]**, dove **cartella** è facoltativa. **Nomecomputer** può essere un nome di dominio completo (FQDN) o un indirizzo IP e **cartellacondivisione** può essere una lettera di unità. Viene sostituita solo la parte **\\\\computername\\sharedfolder** o lettera dell'unità del percorso OSD.

    Il formato corretto per il percorso URL è **Protocol://nomeserver: \ [Port \] \ [/path\] \ [/\]**, dove **porta** e **percorso** sono facoltativi. Se la **porta** non è specificata, viene usata la porta predefinita per il protocollo. Viene sostituita solo la parte **protocollo://Server: Port** dell'URL OSD.

    **Importante**  
    Le variabili di ambiente non sono supportate nella definizione ApplicationSourceRoot.



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**Per configurare il valore OSDSourceRoot**

-   Configurare OSDSourceRoot nel valore della chiave del registro di sistema seguente con un percorso UNC o un URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot

    I formati accettabili per OSDSourceRoot includono percorsi UNC e URL, come nell'esempio seguente:

    **\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o ** &lt; unità &gt; : \\foldername**

    **http://computername/productivity/** o**https://computername/productivity/**

**Per configurare il valore IconSourceRoot**

-   Configurare IconSourceRoot nel valore della chiave del registro di sistema seguente con un percorso UNC o un URL:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot

    I formati accettabili per IconSourceRoot includono percorsi UNC e URL, come nell'esempio seguente:

    **\\\\computername\\sharefolder\\resource** o **\\\\computername\\content** o ** &lt; unità &gt; : \\foldername**

    **http://computername/productivity/** o**https://computername/productivity/**

## Argomenti correlati


[Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









