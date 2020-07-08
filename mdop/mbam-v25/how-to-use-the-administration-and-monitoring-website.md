---
title: Come usare il sito Web di gestione e monitoraggio
description: Come usare il sito Web di gestione e monitoraggio
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804683"
---
# Come usare il sito Web di gestione e monitoraggio


Il sito Web di amministrazione e monitoraggio, noto anche come Help desk, è un'interfaccia amministrativa per la crittografia unità BitLocker. Usare il sito Web per esaminare i report, recuperare le unità degli utenti finali e gestire le TPMs degli utenti finali, come descritto nelle sezioni seguenti.

**Nota**  Se si usa MBAM nella topologia autonoma, è possibile visualizzare tutti i report dal sito Web amministrazione e monitoraggio. Se si usa la topologia di integrazione di Configuration Manager, è possibile visualizzare tutti i report di Configuration Manager, ad eccezione del report di controllo del ripristino, che si continua a visualizzare dal sito Web di amministrazione e monitoraggio. Per altre informazioni sui report, vedere [monitoraggio e segnalazione della conformità di BitLocker con MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).

 

## Ruoli obbligatori per l'uso del sito Web amministrazione e monitoraggio


Per accedere a specifiche aree del sito Web di amministrazione e monitoraggio, è necessario avere uno dei ruoli seguenti, ovvero i gruppi creati in Active Directory. Puoi usare qualsiasi nome per questi gruppi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Account</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM Advanced helpdesk utenti</p></td>
<td align="left"><p>Consente di accedere a tutte le aree del sito Web di amministrazione e monitoraggio. Gli utenti che hanno questo ruolo immettono solo la chiave di ripristino e non il nome utente e il dominio dell'utente finale quando aiutano gli utenti finali a recuperare le proprie unità. Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti di mbam Advanced helpdesk eseguono l'override delle autorizzazioni di gruppo utenti di MBAM helpdesk.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di MBAM helpdesk</p></td>
<td align="left"><p>Consente di accedere alle aree Gestisci TPM e ripristino unità del sito Web di amministrazione e monitoraggio. Gli utenti che hanno questo ruolo devono compilare tutti i campi, incluso il dominio dell'utente finale e il nome dell'account, quando usano un'area qualsiasi.</p>
<p>Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti di mbam Advanced helpdesk eseguono l'override delle autorizzazioni di gruppo utenti di MBAM helpdesk.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di report MBAM</p></td>
<td align="left"><p>Consente di accedere ai report nell' <strong> area report </strong> del sito Web amministrazione e monitoraggio.</p></td>
</tr>
</tbody>
</table>

 

## Attività che è possibile eseguire nel sito Web di amministrazione e monitoraggio


La tabella seguente riepiloga le attività che è possibile eseguire nel sito Web di amministrazione e monitoraggio e fornisce collegamenti ad altre informazioni su ogni attività.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Area del sito Web in cui si accede all'attività</th>
<th align="left">Descrizione</th>
<th align="left">Per altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Visualizzare i report</p></td>
<td align="left"><p>Rapporti</p></td>
<td align="left"><p>Consente di eseguire report per monitorare l'utilizzo, la conformità e l'attività di ripristino della chiave di BitLocker. I report includono dati relativi alla conformità aziendale, ai singoli computer e alle persone che hanno richiesto le chiavi di ripristino o il pacchetto OwnerAuth TPM per un computer specifico.</p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)">Visualizzazione dei report di MBAM 2.5 per la topologia autonoma</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Determinare lo stato di crittografia di BitLocker per i computer persi o rubati</p></td>
<td align="left"><p>Rapporti</p></td>
<td align="left"><p>Determinare se un volume è stato crittografato se il computer viene perso o rubato.</p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)">Come determinare lo stato della crittografia BitLocker nei computer smarriti</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recuperare le unità perse</p></td>
<td align="left"><p>Ripristino unità</p></td>
<td align="left"><p>Recuperare le unità che sono:</p>
<ul>
<li><p>In modalità di ripristino</p></li>
<li><p>Sono stati spostati</p></li>
<li><p>Sono danneggiati</p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)">Come recuperare un'unità in modalità di ripristino</a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)">Come recuperare un'unità spostata</a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)">Come recuperare un'unità danneggiata</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Reimpostare un blocco TPM</p></td>
<td align="left"><p>Gestisci TPM</p></td>
<td align="left"><p>Consente di accedere ai dati del TPM raccolti dal client MBAM. In un blocco TPM usare il sito Web amministrazione e monitoraggio per recuperare il file di password necessario per sbloccare il TPM.</p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)">Come ripristinare un blocco del TPM</a></p></td>
</tr>
</tbody>
</table>

 


## Argomenti correlati


[Gestione di BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





