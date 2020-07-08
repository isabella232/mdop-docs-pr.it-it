---
title: Come abilitare la creazione di report nel client App-V 5.1 con PowerShell
description: Come abilitare la creazione di report nel client App-V 5.1 con PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805452"
---
# Come abilitare la creazione di report nel client App-V 5.1 con PowerShell


Usare la procedura seguente per configurare l'App V 5,1 per la creazione di report.

**Per configurare il computer in cui è in uso il client App-V 5,1 per la creazione di report**

1. Installare il client App-V 5,1. Per altre informazioni sull'installazione del client [, vedere come distribuire il client App-V](how-to-deploy-the-app-v-client-51gb18030.md).

2. Dopo aver installato il client App-V 5,1, usare la versione **set-AppvClientConfiguration** di PowerShell per configurare le impostazioni di configurazione della creazione di report appropriate:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Impostazione</th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>ReportingEnabled</p></td>
   <td align="left"><p>Consente al client di restituire informazioni a un server di report. Questa impostazione è necessaria per il client per raccogliere i dati dei report nel client.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingServerURL</p></td>
   <td align="left"><p>Specifica la posizione nel server di report in cui vengono salvate le informazioni sul client. Ad esempio, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Questo è il numero di porta assegnato durante la configurazione del server di Reporting</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Ora di inizio della segnalazione</p></td>
   <td align="left"><p>Questa operazione è impostata per pianificare il client per inviare automaticamente i dati al server. Questa impostazione indicherà l'ora in cui inizieranno a inviare i dati dei report. È nel formato 24 ore e prenderà un numero compreso tra 0-23.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingRandomDelay</p></td>
   <td align="left"><p>Specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report. Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra 0 e ReportingRandomDelay e attenderà la durata specificata prima di inviare i dati.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingInterval</p></td>
   <td align="left"><p>Specifica l'intervallo di tentativi che il client userà per rinviare i dati al server di report.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingDataCacheLimit</p></td>
   <td align="left"><p>Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report. Le dimensioni si applicano alla cache in memoria. Quando viene raggiunto il limite, il file di log verrà ribaltato.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingDataBlockSize</p></td>
   <td align="left"><p>Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report. Le dimensioni si applicano alla cache in memoria. Quando viene raggiunto il limite, il file di log verrà ribaltato.</p></td>
   </tr>
   </tbody>
   </table>



3. Dopo aver configurato le impostazioni appropriate, il computer che gestisce il client App-V 5,1 raccoglierà automaticamente i dati e invierà i dati al server di report.

   Gli amministratori possono inoltre restituire manualmente i dati in modo su richiesta usando il cmdlet di PowerShell **Send-AppvClientReport** .

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Amministrazione di App-V 5.1 con PowerShell](administering-app-v-51-by-using-powershell.md)









