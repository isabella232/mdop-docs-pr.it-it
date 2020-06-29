---
title: Prerequisiti per i client di MBAM 2.5
description: Prerequisiti per i client di MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826966"
---
# Prerequisiti per i client di MBAM 2.5


Prima di installare il software del client MBAM nei computer degli utenti finali, verificare che l'ambiente e i computer client soddisfino i prerequisiti seguenti.

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
<td align="left"><p>Il dominio aziendale deve contenere almeno un controller di dominio di Windows Server 2008 (o versioni successive).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Il computer client deve essere connesso alla rete Intranet aziendale.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Solo per i computer client Windows 7: ogni client deve avere funzionalità TPM (Trusted Platform Module) (TPM 1,2 o successiva).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Solo per i computer client Windows 8,1, Windows 10 RTM o Windows 10 versione 1511: se si vuole che MBAM sia in grado di archiviare e gestire le chiavi di ripristino del TPM, il provisioning automatico TPM deve essere disattivato e MBAM deve essere impostato come proprietario del TPM prima di distribuire MBAM.</p>
<p>In MBAM 2,5 SP1 solo non è più necessario disattivare il provisioning automatico del TPM, ma è necessario assicurarsi che gli oggetti Criteri di gruppo TPM siano impostati su Active Directory con il TPM non OwnerAuth.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)">Considerazioni sulla sicurezza per MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM.</p>
<p>In MBAM 2,5 SP1 è necessario attivare il provisioning automatico.</p>
</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> </a> Per ulteriori informazioni, vedere password del proprietario del TPM.
</p></td>
</tr>
<tr class="even">
<td align="left"><p>Il chip TPM deve essere attivato nel BIOS e può essere ripristinato dal sistema operativo.</p></td>
<td align="left"><p>Per altre informazioni, vedere la documentazione del BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Il disco rigido del computer deve avere almeno due partizioni e deve essere formattato con il file system NTFS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Il disco rigido del computer deve avere un BIOS compatibile con TPM e che supporta i dispositivi USB durante l'avvio del computer.</p></td>
<td align="left"><div class="alert">
<strong>Nota</strong><br/><p>Verificare che la tastiera, il video o il mouse siano direttamente connessi e non gestiti tramite una tastiera, un video o un interruttore del mouse (KVM). Uno switch KVM può interferire con la capacità del computer di rilevare la presenza fisica dell'hardware.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Se si usa un proxy, deve essere visibile nel contesto di sistema. MBAM viene eseguito nel contesto di sistema, non nel contesto dell'utente.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**Importante**  
Se BitLocker è stato usato senza MBAM, MBAM può essere installato e utilizzare le informazioni esistenti sul TPM.




## Argomenti correlati


[Configurazioni supportate di MBAM 2.5](mbam-25-supported-configurations.md)

[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






