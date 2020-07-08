---
title: Come gestire le esenzioni della crittografia BitLocker dell'utente
description: Come gestire le esenzioni della crittografia BitLocker dell'utente
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804623"
---
# Come gestire le esenzioni della crittografia BitLocker dell'utente


Microsoft BitLocker Administration and Monitoring (MBAM) può essere usato per gestire la protezione di BitLocker esentando gli utenti che non hanno bisogno o vogliono crittografare le unità.

Per esonerare gli utenti dalla protezione di BitLocker, un'organizzazione deve prima di tutto creare un'infrastruttura per supportare tali esenzioni. L'infrastruttura di supporto può includere un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica per richiedere l'esenzione. Inoltre, tutti gli utenti esenti dovranno essere aggiunti a un gruppo di sicurezza per i criteri di gruppo creati in modo specifico per gli utenti esentati. Quando i membri di questo gruppo di sicurezza accedono a un computer, i criteri di gruppo degli utenti indicano che l'utente è esonerato dalla protezione da BitLocker. Il criterio utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.

**Nota**  Se il computer è già protetto da BitLocker, il criterio di esenzione dall'utente non ha alcun effetto.

 

Nella tabella seguente viene illustrato il modo in cui viene applicata la protezione BitLocker in base al modo in cui vengono impostate le esenzioni.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Stato utente</th>
<th align="left">Computer non esonerato</th>
<th align="left">Computer esenti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>L'utente non è esonerato</strong></p></td>
<td align="left"><p>La protezione di BitLocker viene applicata nel computer.</p></td>
<td align="left"><p>La protezione di BitLocker non viene applicata nel computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Esenzione dall'utente</strong></p></td>
<td align="left"><p>La protezione di BitLocker non viene applicata nel computer.</p></td>
<td align="left"><p>La protezione di BitLocker non viene applicata nel computer.</p></td>
</tr>
</tbody>
</table>

 

**Per esonerare un utente dalla crittografia BitLocker**

1.  Creare un gruppo di sicurezza di ActiveDirectoryDomainServices che verrà usato per gestire le esenzioni dagli utenti dalla crittografia BitLocker.

2.  Creare un'impostazione di un oggetto Criteri di gruppo usando il modello di criteri di gruppo di MBAM. Associa l'oggetto Criteri di gruppo al gruppo di Active Directory creato nel passaggio precedente. Per altre informazioni sulle impostazioni dei criteri necessarie per consentire agli utenti di richiedere l'esenzione dalla crittografia BitLocker, vedere la sezione configurare i criteri di esenzione dall'utente nella [pianificazione per i requisiti di criteri di gruppo di MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).

3.  Dopo aver creato un gruppo di sicurezza per gli utenti esentati da BitLocker, aggiungere al gruppo i nomi degli utenti che chiedono l'esenzione. Quando un utente accede a un computer controllato da BitLocker, il client MBAM verificherà l'impostazione di criteri di esenzione dall'utente e sospenderà la protezione a seconda che l'utente faccia parte del gruppo di sicurezza per l'esenzione da BitLocker.

    **Nota**  Gli scenari di computer condivisi richiedono una particolare considerazione per quanto riguarda l'esenzione dall'utente. Se un utente non esenta accede a un computer condiviso con un utente esentasse, il computer potrebbe essere crittografato.

     

**Per consentire agli utenti di richiedere l'esenzione dalla crittografia BitLocker**

1.  Dopo aver configurato i criteri di esenzione dall'utente usingwith il modello di MBAM Policy, un utente può richiedere l'esenzione dalla protezione di BitLocker tramite il client MBAM.

2.  Quando un utente accede a un computer contrassegnato come **compatibile** nell'elenco di compatibilità hardware di mbam, il sistema presenta all'utente una notifica che il computer verrà crittografato. L'utente può selezionare **esenzione dalla richiesta** e rinviare la crittografia selezionando **più avanti**oppure selezionare **inizia** per accettare la crittografia BitLocker.

    **Nota**  Selezionando **esenzione dalla richiesta** verrà rinviata la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.

     

3.  Quando un utente seleziona la **richiesta di esenzione**, l'utente riceve una notifica per contattare il gruppo di amministrazione BitLocker dell'organizzazione. A seconda della configurazione dei criteri di esenzione per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:

    -   Numero di telefono

    -   URL della pagina Web

    -   Indirizzo di posta elettronica

    Dopo l'invio della richiesta, l'amministratore di MBAM può decidere se è appropriato aggiungere l'utente al gruppo Active Directory di esenzione da BitLocker.

    **Nota**  Quando il limite di tempo di posticipazione dei criteri di esenzione dall'utente è scaduto, gli utenti non vedranno l'opzione per richiedere l'esenzione ai criteri di crittografia. A questo punto, gli utenti devono contattare direttamente l'amministratore di MBAM per ricevere l'esenzione dalla protezione di BitLocker.

     

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 1.0](administering-mbam-10-features.md)

 

 





