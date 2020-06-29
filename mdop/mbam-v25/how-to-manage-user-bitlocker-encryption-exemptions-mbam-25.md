---
title: Come gestire le esenzioni della crittografia BitLocker dell'utente
description: Come gestire le esenzioni della crittografia BitLocker dell'utente
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826795"
---
# Come gestire le esenzioni della crittografia BitLocker dell'utente


Microsoft BitLocker Administration and Monitoring (MBAM) consente di esonerare gli utenti dai requisiti di crittografia unità BitLocker.

Per esonerare gli utenti dalla protezione di BitLocker, è necessario:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Creare un'infrastruttura per supportare gli utenti esentati.</p></td>
<td align="left"><p>Gli esempi di questa infrastruttura includono fornire agli utenti un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica che possono usare per richiedere un'esenzione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aggiungere l'utente esentato a un gruppo di sicurezza per un oggetto Criteri di gruppo configurato in modo specifico per gli utenti esentati.</p></td>
<td align="left"><p>Quando i membri di questo gruppo di sicurezza si iscrivono a un computer, l'impostazione di criteri di gruppo dell'utente esonera l'utente dalla protezione BitLocker. L'impostazione di criteri di gruppo dell'utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.</p>
<div class="alert">
<strong>Nota</strong><br/><p>MBAM non emana i criteri di crittografia se il computer è già protetto da BitLocker e l'utente è esonerato. Tuttavia, se un altro utente che non è esonerato dai criteri di crittografia accede al computer, verrà applicata la crittografia.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



I passaggi seguenti descrivono ciò che accade quando gli utenti finali richiedono un'esenzione dal processo di esenzione dalla crittografia unità BitLocker tramite il client MBAM o attraverso qualsiasi processo usato dall'organizzazione. È necessario configurare le impostazioni dei criteri di gruppo di MBAM per consentire agli utenti finali di richiedere un'esenzione dalla crittografia unità BitLocker.

1.  Quando gli utenti finali accedono a un computer che deve essere crittografato, ricevono una notifica per cui il computer verrà crittografato. Possono selezionare l' **esenzione dalla richiesta** e posticipare la crittografia selezionando **rinvia**oppure selezionare **Avvia crittografia** per accettare la crittografia BitLocker.

    **Nota**  
    Selezionando **esenzione dalla richiesta** rinvia la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.



2.  Se gli utenti finali selezionano **esenzione dalla richiesta**, ricevono una notifica che informa loro di contattare il gruppo di amministrazione BitLocker dell'organizzazione. A seconda della configurazione dei **criteri di esenzione** per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:

    -   Numero di telefono

    -   URL della pagina Web

    -   Indirizzo di posta elettronica

3.  Dopo aver ricevuto la richiesta di esenzione, l'amministratore di MBAM decide se aggiungere l'utente al gruppo servizi di dominio Active Directory (AD DS) di esenzione per BitLocker.

4.  Dopo che un utente finale invia una richiesta di esenzione, il client MBAM segnala l'utente come "temporaneamente esenti". Il client attende quindi un numero specificato di giorni, che gli amministratori IT configurano, prima di verificare di nuovo la conformità del computer. Se l'amministratore di MBAM respinge la richiesta di esenzione, l'opzione per la richiesta di esenzione è disattivata, che impedisce che l'utente richieda l'esenzione.

Microsoft BitLocker Administration and Monitoring (MBAM) consente di esonerare gli utenti dai requisiti di crittografia unità BitLocker.

Per esonerare gli utenti dalla protezione di BitLocker, è necessario:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Creare un'infrastruttura per supportare gli utenti esentati.</p></td>
<td align="left"><p>Gli esempi di questa infrastruttura includono fornire agli utenti un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica che possono usare per richiedere un'esenzione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aggiungere l'utente esentato a un gruppo di sicurezza per un oggetto Criteri di gruppo configurato in modo specifico per gli utenti esentati.</p></td>
<td align="left"><p>Quando i membri di questo gruppo di sicurezza si iscrivono a un computer, l'impostazione di criteri di gruppo dell'utente esonera l'utente dalla protezione BitLocker. L'impostazione di criteri di gruppo dell'utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se il computer è già protetto da BitLocker, il criterio di esenzione dall'utente non ha alcun effetto. Inoltre, se un altro utente accede a un computer che non è esentato dai criteri di crittografia, verrà applicata la crittografia.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



I passaggi seguenti descrivono ciò che accade quando gli utenti finali richiedono un'esenzione dal processo di esenzione dalla crittografia unità BitLocker tramite il client MBAM o attraverso qualsiasi processo usato dall'organizzazione. È necessario configurare le impostazioni dei criteri di gruppo di MBAM per consentire agli utenti finali di richiedere un'esenzione dalla crittografia unità BitLocker.

1.  Quando gli utenti finali accedono a un computer che deve essere crittografato, ricevono una notifica per cui il computer verrà crittografato. Possono selezionare l' **esenzione dalla richiesta** e posticipare la crittografia selezionando **rinvia**oppure selezionare **Avvia crittografia** per accettare la crittografia BitLocker.

    **Nota**  
    Selezionando **esenzione dalla richiesta** rinvia la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.



2.  Se gli utenti finali selezionano **esenzione dalla richiesta**, ricevono una notifica che informa loro di contattare il gruppo di amministrazione BitLocker dell'organizzazione. A seconda della configurazione dei **criteri di esenzione** per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:

    -   Numero di telefono

    -   URL della pagina Web

    -   Indirizzo di posta elettronica

3.  Dopo aver ricevuto la richiesta di esenzione, l'amministratore di MBAM decide se aggiungere l'utente al gruppo servizi di dominio Active Directory (AD DS) di esenzione per BitLocker.

4.  Dopo che un utente finale invia una richiesta di esenzione, il client MBAM segnala l'utente come "temporaneamente esenti". Il client attende quindi un numero specificato di giorni, che gli amministratori IT configurano, prima di verificare di nuovo la conformità del computer. Se l'amministratore di MBAM respinge la richiesta di esenzione, l'opzione per la richiesta di esenzione è disattivata, che impedisce che l'utente richieda l'esenzione.

**Per esonerare un utente dalla crittografia unità BitLocker**

1.  Creare un gruppo di sicurezza di servizi di dominio Active Directory che verrà usato per gestire le esenzioni dagli utenti dai requisiti di crittografia BitLocker.

2.  Creare un oggetto Criteri di gruppo usando i modelli di criteri di gruppo per l'amministrazione e il monitoraggio di Microsoft BitLocker.

3.  Associa l'oggetto Criteri di gruppo al gruppo di servizi di dominio Active Directory creato nel passaggio precedente. Le impostazioni dei criteri per gli utenti esenti si trovano in: **UserConfiguration** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management)**.

4.  Per il gruppo di sicurezza creato per gli utenti esentati da BitLocker, aggiungere i nomi degli utenti che chiedono un'esenzione.

    Quando un utente accede a un computer controllato da BitLocker, il client MBAM controlla l'impostazione dei criteri di esenzione dall'utente. Se il computer è già crittografato, la protezione di BitLocker non viene sospesa. Se il computer non è crittografato, MBAM non chiede all'utente di crittografarlo.

    **Importante**  
    Gli scenari di computer condivisi richiedono una particolare considerazione quando si usano le esenzioni degli utenti di BitLocker. Se un utente non esonerato accede a un computer condiviso con un utente esenta, il computer potrebbe essere crittografato.




## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 2.5](administering-mbam-25-features.md)

[Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)




## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




