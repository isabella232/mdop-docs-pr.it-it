---
title: Pianificazione per la creazione dell'immagine di ripristino di DaRT 10
description: Pianificazione per la creazione dell'immagine di ripristino di DaRT 10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822976"
---
# Pianificazione per la creazione dell'immagine di ripristino di DaRT 10


Usare le informazioni in questa sezione quando si prevede di creare l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10.

## Pianificazione della creazione dell'immagine di ripristino di DaRT 10


Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine. Per prendere la decisione, considera che gli utenti finali possono avere accesso a questi strumenti. Se i tecnici del supporto accettano il supporto di immagini di ripristino per consentire ai computer degli utenti di diagnosticare i problemi, è consigliabile installare tutti gli strumenti nell'immagine di ripristino. Se si prevede di diagnosticare i computer degli utenti finali in remoto, è consigliabile disabilitare alcuni degli strumenti, ad esempio la cancellazione del disco e l'editor del registro di sistema, e quindi abilitare altri strumenti, inclusa la connessione remota.

Quando si crea l'immagine di ripristino delle freccette, si specifica anche se si desidera includere altri driver o file. Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.

Per altre informazioni sugli strumenti DaRT, Vedi [Panoramica degli strumenti in DART 10](overview-of-the-tools-in-dart-10.md). Per altre informazioni su come semplificare la creazione di un'immagine di ripristino sicura, vedere [considerazioni sulla sicurezza per Dart 10](security-considerations-for-dart-10.md).

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
<td align="left"><p>File di origine di Windows 10</p></td>
<td align="left"><p>Necessario per creare l'immagine di ripristino delle freccette. Fornisci il percorso di un DVD di Windows 10 o di file di origine Windows 10.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Strumenti di debug di Windows per la tua piattaforma</p></td>
<td align="left"><p>Obbligatorio quando si esegue l' <strong> analizzatore crash </strong> per determinare la causa di un errore del computer. Ti consigliamo di specificare il percorso degli strumenti di debug di Windows al momento della creazione dell'immagine di ripristino DaRT. Puoi scaricare gli strumenti di debug di Windows qui: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> scaricare e installare gli strumenti di debug per Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Facoltativo: file di simboli Windows da usare con <strong> Crash Analyzer</strong></p></td>
<td align="left"><p>In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'applicazione. È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se ha smesso di funzionare. Per altre informazioni, vedere <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnostica degli errori di sistema con Crash Analyzer </a> .</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati

[Pianificazione della distribuzione di DaRT 10](planning-to-deploy-dart-10.md)

 

 




