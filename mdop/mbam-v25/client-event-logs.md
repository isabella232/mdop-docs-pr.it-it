---
title: Registri eventi del client
description: Registri eventi del client
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824195"
---
# Registri eventi del client

I log eventi del client MBAM si trovano nel Visualizzatore eventi-log delle applicazioni e dei servizi-Microsoft-Windows-MBAM-Operational Path.
La tabella seguente contiene gli ID evento che possono verificarsi nel client MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID evento</th>
<th align="left">Canale</th>
<th align="left">Simbolo dell'evento</th>
<th align="left">Messaggio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>VolumeEnactmentSuccessful</p></td>
<td align="left"><p>I criteri di MBAM sono stati applicati correttamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>2</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>VolumeEnactmentFailed</p></td>
<td align="left"><p>Si è verificato un errore durante l'applicazione di criteri MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>TransferStatusDataSuccessful</p></td>
<td align="left"><p>I dati di stato della crittografia sono stati inviati correttamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TransferStatusDataFailed</p></td>
<td align="left"><p>Si è verificato un errore durante l'invio di dati sullo stato di crittografia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>8</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>SystemVolumeNotFound</p></td>
<td align="left"><p>Il volume di sistema non è presente. SystemVolume è necessario per crittografare l'unità del sistema operativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>9</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMNotFound</p></td>
<td align="left"><p>L'hardware TPM manca. TPM è necessario per crittografare l'unità del sistema operativo con qualsiasi protezione TPM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>10</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWExempted</p></td>
<td align="left"><p>Il computer è esentato dalla crittografia. Stato hardware della macchina: esentato</p></td>
</tr>
<tr class="even">
<td align="left"><p>11</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>MachineHWUnknown</p></td>
<td align="left"><p>Il computer è esentato dalla crittografia. Stato hardware della macchina: sconosciuto</p></td>
</tr>
<tr class="odd">
<td align="left"><p>12</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>HWCheckFailed</p></td>
<td align="left"><p>Controllo esenzione hardware non riuscito.</p></td>
</tr>
<tr class="even">
<td align="left"><p>13</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsExempted</p></td>
<td align="left"><p>L'utente è esonerato dalla crittografia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>14</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserIsWaiting</p></td>
<td align="left"><p>L'utente ha richiesto un'esenzione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>15</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserExemptionCheckFailed</p></td>
<td align="left"><p>Controllo di esenzione dall'utente non riuscito.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>16</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>UserPostponed</p></td>
<td align="left"><p>L'utente ha rinviato il processo di crittografia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>17</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TPMInitializationFailed</p></td>
<td align="left"><p>L'inizializzazione del TPM non è riuscita. L'utente ha rifiutato le modifiche del BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>18</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>CoreServiceDown</p></td>
<td align="left"><p>Non è possibile connettersi al servizio di ripristino e hardware di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>19</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>CoreServiceUp</p></td>
<td align="left"><p>Connesso correttamente al servizio di ripristino e hardware di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>20</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>PolicyMismatch</p></td>
<td align="left"><p>I criteri di MBAM sono in conflitto o corrotti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>21</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingOSVolumePolicies</p></td>
<td align="left"><p>Rilevato conflitto tra i criteri di crittografia del volume OS. Controlla i criteri di BitLocker e MBAM relativi alle protezioni unità OS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>22</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>ConflictingFDDVolumePolicies</p></td>
<td align="left"><p>Rilevato conflitto di criteri di crittografia del volume delle unità dati fisse. Controlla i criteri di BitLocker e MBAM relativi alle protezioni unità FDD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>27</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>EncryptionFailedNoDra</p></td>
<td align="left"><p>Si è verificato un errore durante la crittografia. Una protezione DRA (Data Recovery Agent) è necessaria in modalità FIPS per i computer pre-Windows 8,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>28</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>TpmOwnerAuthEscrowed</p></td>
<td align="left"><p>Il TPM OwnerAuth è stato escrowed.</p></td>
</tr>
<tr class="even">
<td align="left"><p>29</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>RecoveryKeyEscrowed</p></td>
<td align="left"><p>La chiave di ripristino di BitLocker per il volume è stata escrowed.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>30</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>RecoveryKeyReset</p></td>
<td align="left"><p>La chiave di ripristino di BitLocker per il volume è stata aggiornata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>31</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>EnforcePolicyDateSet</p></td>
<td align="left"><p>La data di applicazione dei criteri, <em> &lt; data &gt; </em> , è stata impostata per il volume</p></td>
</tr>
<tr class="odd">
<td align="left"><p>32</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>EnforcePolicyDateCleared</p></td>
<td align="left"><p>La data di applicazione dei criteri, <em> &lt; data &gt; </em> , è stata deselezionata per il volume.</p></td>
</tr>
<tr class="even">
<td align="left"><p>33</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>TpmLockOutResetSucceeded</p></td>
<td align="left"><p>Reimpostare correttamente il blocco TPM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>34</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmLockOutResetFailed</p></td>
<td align="left"><p>Non è possibile reimpostare il blocco TPM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalSucceeded</p></td>
<td align="left"><p>È stato recuperato correttamente TPM OwnerAuth da MBAM Services.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>36</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalFailed</p></td>
<td align="left"><p>Impossibile recuperare il TPM OwnerAuth da servizi MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>37</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>WmiProviderDllSearchPathUpdateFailed</p></td>
<td align="left"><p>Non è possibile aggiornare il percorso di ricerca della DLL per il provider WMI.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>38</p></td>
<td align="left"><p>Admin</p></td>
<td align="left"><p>TimedOutWaitingForWmiProvider</p></td>
<td align="left"><p>Interruzione dell'agente-timeout in attesa per l'istanza del provider WMI MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>39</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>RemovableDriveMounted</p></td>
<td align="left"><p>È stato montato un drive rimovibile.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>40</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>RemovableDriveDismounted</p></td>
<td align="left"><p>L'unità rimovibile è stata smontata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>41</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>FailedToEnactEndpointUnreachable</p></td>
<td align="left"><p>L'errore di connettersi al servizio di ripristino e hardware di MBAM ha impedito che i criteri di MBAM venissero applicati correttamente al volume.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>42</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>FailedToEnactLockedVolume</p></td>
<td align="left"><p>Lo stato del volume bloccato ha impedito che i criteri di MBAM venissero applicati correttamente al volume.</p></td>
</tr>
<tr class="even">
<td align="left"><p>43</p></td>
<td align="left"><p>Operativo</p></td>
<td align="left"><p>TransferStatusDataFailedEndpointUnreachable</p></td>
<td align="left"><p>L'omissione di connettersi al servizio di stato e conformità di MBAM ha impedito il trasferimento dei dati di stato della crittografia.</p></td>
</tr>
</tbody>
</table>

 


## Argomenti correlati
[Documentazione tecnica per MBAM 2.5](technical-reference-for-mbam-25.md)

[Registri eventi del server](server-event-logs.md)

 


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





