---
title: Come consentire solo agli amministratori l'abilitazione dei gruppi di connessione
description: Come consentire solo agli amministratori l'abilitazione dei gruppi di connessione
author: dansimp
ms.assetid: 42ca3157-5d85-467b-a148-09404f8f737a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 083d6386f02996d35255f90958705798f2cd5fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805739"
---
# Come consentire solo agli amministratori l'abilitazione dei gruppi di connessione


Puoi configurare il client App-V in modo che solo gli amministratori (non gli utenti finali) possano abilitare o disabilitare i gruppi di connessioni. Nelle versioni precedenti di App-V non è stato possibile impedire agli utenti finali di eseguire queste attività.

**Nota** 
 **Questa funzionalità è supportata a partire da App-V 5,0 SP3.**

 

Usa uno dei metodi seguenti per consentire solo agli amministratori di abilitare o disabilitare i gruppi di connessioni.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Passaggi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazione di Criteri di gruppo</p></td>
<td align="left"><p>Abilitare l'impostazione di criteri di gruppo "Richiedi pubblica come amministratore", disponibile nel nodo oggetto Criteri di gruppo seguente:</p>
<p><strong>Criteri di configurazione del computer &gt; &gt; modelli amministrativi &gt; &gt; App-V &gt; Publishing</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlet di PowerShell</p></td>
<td align="left"><p>Eseguire il <strong> cmdlet Set-AppvClientConfiguration </strong> con il <strong> parametro – RequirePublishAsAdmin </strong> .</p>
<p>Valori dei parametri:</p>
<ul>
<li><p>0-falso</p></li>
<li><p>1-vero</p></li>
</ul>
<p><strong>Esempio: </strong> : set-AppvClientConfiguration-RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

**Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Gestione dei gruppi di connessione](managing-connection-groups51.md)

 

 





