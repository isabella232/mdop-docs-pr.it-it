---
title: Come distribuire i database App-V con script SQL
description: Come distribuire i database App-V con script SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805482"
---
# Come distribuire i database App-V con script SQL


Seguire le istruzioni seguenti per usare gli script SQL, invece di Windows Installer, per:

-   Installare i database di App-V 5,0

-   Aggiornare i database di 5,0 a una versione successiva

**Come installare i database di App-V usando gli script SQL**

1. Prima di installare gli script di database, rivedere e conservare una copia delle condizioni di licenza di App-V. Eseguendo gli script del database si accettano le condizioni di licenza. Se non è possibile accettarli, non usare questo software.

2. Copiare il **appv\_server\_setup.exe** dal supporto per la versione di App-V in un percorso temporaneo.

3. Da un prompt dei comandi eseguire **appv\_server\_setup.exe** e specificare una posizione temporanea per l'estrazione degli script di database.

   Esempio: appv\_server\_setup.exe/layout c:\\ &lt; percorso temporaneo&gt;

4. Passare al percorso temporaneo creato, aprire la cartella **DatabaseScripts** estratta e rivedere il file Readme.txt appropriato per le istruzioni:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Database</th>
   <th align="left">Posizione del file Readme.txt da usare</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Database di gestione</p></td>
   <td align="left"><p>Sottocartella ManagementDatabase</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Se si esegue l'aggiornamento o l'installazione del database di gestione di App-V 5,0 SP3, vedere <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> script SQL per installare o aggiornare il database del server di gestione di App-v 5,0 SP3 Fail </a> .</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Database di report</p></td>
   <td align="left"><p>Sottocartella ReportingDatabase</p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Distribuzione del server App-V 5.0](deploying-the-app-v-50-server.md)

[Come distribuire il server App-V 5.0](how-to-deploy-the-app-v-50-server-50sp3.md)









