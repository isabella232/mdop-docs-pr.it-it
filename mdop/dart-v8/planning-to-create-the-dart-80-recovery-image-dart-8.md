---
title: Pianificazione per la creazione dell'immagine di ripristino di DaRT 8.0
description: Pianificazione per la creazione dell'immagine di ripristino di DaRT 8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824806"
---
# Pianificazione per la creazione dell'immagine di ripristino di DaRT 8.0


Usare le informazioni in questa sezione quando si prevede di creare l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.

## Pianificazione della creazione dell'immagine di ripristino di DaRT 8,0


Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine. Per prendere la decisione, considera che gli utenti finali possono avere accesso a questi strumenti. Se i tecnici del supporto accettano il supporto di immagini di ripristino per consentire ai computer degli utenti di diagnosticare i problemi, è consigliabile installare tutti gli strumenti nell'immagine di ripristino. Se si prevede di diagnosticare i computer degli utenti finali in remoto, è consigliabile disabilitare alcuni degli strumenti, ad esempio la cancellazione del disco e l'editor del registro di sistema, e quindi abilitare altri strumenti, inclusa la connessione remota.

Quando si crea l'immagine di ripristino delle freccette, si specifica anche se si desidera includere altri driver o file. Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.

Per altre informazioni sugli strumenti DaRT, Vedi [Panoramica degli strumenti di dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md). Per altre informazioni su come semplificare la creazione di un'immagine di ripristino sicura, vedere [considerazioni sulla sicurezza per DaRT 8,0](security-considerations-for-dart-80--dart-8.md).

## Prerequisiti per l'immagine di ripristino


Gli elementi seguenti sono obbligatori o consigliati per creare l'immagine di ripristino DaRT:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Prerequisiti</strong></p></td>
<td align="left"><p><strong>Dettagli</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>File di origine di Windows 8</p></td>
<td align="left"><p>Necessario per creare l'immagine di ripristino delle freccette. Fornisci il percorso di un DVD di Windows 8 o di file di origine di Windows 8.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Strumenti di debug di Windows per la tua piattaforma</p></td>
<td align="left"><p>Obbligatorio quando si esegue l' <strong> analizzatore crash </strong> per determinare la causa di un errore del computer. Ti consigliamo di specificare il percorso degli strumenti di debug di Windows al momento della creazione dell'immagine di ripristino DaRT. Puoi scaricare gli strumenti di debug di Windows qui: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> scaricare e installare gli strumenti di debug per Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Facoltativo: <strong> </strong> definizioni Defender</p></td>
<td align="left"><p>Le definizioni più recenti per <strong> Defender </strong> sono necessarie quando si esegue <strong> Defender </strong> . Anche se è possibile scaricare le definizioni durante l'esecuzione di <strong> Defender </strong> , è consigliabile scaricare le definizioni più recenti al momento della creazione dell'immagine di ripristino delle freccette in modo da poter eseguire lo strumento con le definizioni più recenti anche se il computer problema non ha connettività di rete.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Facoltativo: file di simboli Windows da usare con <strong> Crash Analyzer</strong></p></td>
<td align="left"><p>In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'applicazione. È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se ha smesso di funzionare. Per altre informazioni, vedere <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> diagnostica degli errori di sistema con Crash Analyzer </a> .</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Pianificazione della distribuzione di DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





