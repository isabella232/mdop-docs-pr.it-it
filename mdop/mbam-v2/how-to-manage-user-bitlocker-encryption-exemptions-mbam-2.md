---
title: Come gestire le esenzioni della crittografia BitLocker dell'utente
description: Come gestire le esenzioni della crittografia BitLocker dell'utente
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825075"
---
# Come gestire le esenzioni della crittografia BitLocker dell'utente


Microsoft BitLocker Administration and Monitoring (MBAM) può essere usato per gestire la protezione di BitLocker esentando gli utenti se sono presenti utenti che non hanno bisogno o vogliono crittografare le unità.

Per esonerare gli utenti dalla protezione di BitLocker, un'organizzazione dovrà creare un'infrastruttura per supportare gli utenti esentati, ad esempio per consentire all'utente di usare un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica per richiedere un'esenzione. Inoltre, un utente esonerato dovrà essere aggiunto a un gruppo di sicurezza per un oggetto Criteri di gruppo creato in modo specifico per gli utenti esentati. Quando i membri di questo gruppo di sicurezza accedono a un computer, l'impostazione di criteri di gruppo dell'utente indica che l'utente è esonerato dalla protezione di BitLocker. L'impostazione di criteri di gruppo dell'utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.

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
<td align="left"><p>La protezione di BitLocker viene applicata al computer</p></td>
<td align="left"><p>La protezione BitLocker non viene applicata al computer</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Esenzione dall'utente</strong></p></td>
<td align="left"><p>La protezione BitLocker non viene applicata al computer</p></td>
<td align="left"><p>La protezione BitLocker non viene applicata al computer</p></td>
</tr>
</tbody>
</table>

 

**Per esonerare un utente dalla crittografia BitLocker**

1.  Creare un gruppo di sicurezza di ActiveDirectoryDomainServices che verrà usato per gestire le esenzioni dagli utenti dai requisiti di crittografia di BitLocker.

2.  Creare un'impostazione di un oggetto Criteri di gruppo usando il modello di criteri di gruppo amministrazione e monitoraggio di Microsoft BitLocker e associarlo al gruppo di Active Directory creato nel passaggio precedente. Le impostazioni dei criteri per gli utenti esenti possono essere trovate in **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP mbam (Gestione BitLocker)**.

3.  Dopo aver creato un gruppo di sicurezza per gli utenti esentati da BitLocker, aggiungere a questo gruppo i nomi degli utenti che chiedono un'esenzione. Quando gli utenti accedono a un computer controllato da BitLocker, il client MBAM verificherà l'impostazione dei criteri di esenzione dall'utente e sospenderà la protezione a seconda che l'utente faccia parte del gruppo di sicurezza dell'esenzione per BitLocker.

    **Importante**  Gli scenari di computer condivisi richiedono una particolare considerazione quando si usano le esenzioni dall'utente. Se un utente non esenta accede a un computer condiviso con un utente esentasse, il computer potrebbe essere crittografato.

     

**Per consentire agli utenti di richiedere un'esenzione dalla crittografia BitLocker**

1.  Se sono stati configurati criteri di esenzione dall'utente usando il modello di criteri di MBAM, un utente può richiedere un'esenzione dalla protezione di BitLocker tramite il client MBAM.

2.  Quando gli utenti accedono a un computer che deve essere crittografato, ricevono una notifica per cui il computer verrà crittografato. Possono selezionare **esenzione richiesta** e posticipare la crittografia selezionando **più avanti**oppure selezionare **inizia** per accettare la crittografia BitLocker.

    **Nota**  Selezionando **esenzione dalla richiesta** rinvia la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.

     

3.  Se gli utenti selezionano **esenzione dalla richiesta**, ricevono una notifica per comunicare loro di contattare il gruppo di amministrazione BitLocker dell'organizzazione. A seconda della configurazione dei criteri di esenzione per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:

    -   Numero di telefono

    -   URL della pagina Web

    -   Indirizzo di posta elettronica

    Dopo la ricezione della richiesta di esenzione, l'amministratore di MBAM può decidere se è appropriato aggiungere l'utente al gruppo Active Directory di esenzione da BitLocker.

    **Nota**  Quando un utente invia una richiesta di esenzione, l'agente MBAM segnala l'utente come "temporaneamente esonerato" e quindi attende un numero configurabile di giorni prima di verificare di nuovo la conformità del computer. Se l'amministratore di MBAM respinge la richiesta di esenzione, l'opzione per la richiesta di esenzione è disattivata, impedendo che l'utente possa richiedere di nuovo l'esenzione.

     

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





