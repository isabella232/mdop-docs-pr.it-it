---
title: Amministrazione delle funzionalità di MBAM 1.0
description: Amministrazione delle funzionalità di MBAM 1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821225"
---
# Amministrazione delle funzionalità di MBAM 1.0


Dopo aver completato tutte le necessarie pianificazione e distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurare e usare MBAM per gestire la crittografia BitLocker aziendale. Le informazioni in questa sezione illustrano le attività quotidiane di post-installazione di MBAM.

## Gestire i ruoli di amministratore di MBAM


Dopo aver completato la configurazione di MBAM per tutte le funzionalità del server, agli utenti amministrativi deve essere concesso l'accesso a queste funzionalità del server. Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di MBAM server devono essere assegnati a gruppi di sicurezza di Active Directory e quindi tali gruppi devono essere aggiunti al gruppo locale amministrativo di MBAM appropriato.

[Come gestire i ruoli di amministrazione di MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md)

## Gestire la compatibilità hardware


La funzionalità di compatibilità hardware di MBAM può essere utile per verificare che solo l'hardware del computer specificato come supporto di BitLocker venga crittografato. Quando questa funzionalità è attivata, bit \ _admmontla Crittografa solo i computer contrassegnati come compatibili.

**Importante**  Quando questa caratteristica è disattivata, verranno crittografati tutti i computer in cui viene distribuito il criterio MBAM.

 

MBAM può raccogliere informazioni sia sulla creazione che sul modello di computer client se si distribuisce il criterio di gruppo "Consenti compatibilità hardware". Se si configura questo criterio, l'agente di MBAM riporta il computer e le informazioni sul modello al server MBAM quando il client MBAM viene distribuito in un computer client.

[Come gestire la compatibilità hardware](how-to-manage-hardware-compatibility-mbam-1.md)

[Come gestire le esenzioni della crittografia BitLocker dell'utente](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## Gestire le esenzioni crittografiche di BitLocker


MBAM può concedere due forme di esenzione dalla crittografia BitLocker: esenzione dal computer e esenzione dall'utente. L'esenzione dal computer viene in genere usata quando una società dispone di computer che non devono essere crittografati, ad esempio i computer usati in sviluppo o test o i computer meno recenti che non supportano BitLocker. In alcuni casi, la legge locale può anche richiedere che determinati computer non siano crittografati. Si può anche scegliere di esonerare gli utenti che non hanno bisogno o vogliono che le unità vengano crittografate.

[Come gestire le esenzioni della crittografia BitLocker del computer](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## Gestire le opzioni di crittografia di BitLocker client di MBAM tramite il pannello di controllo


Se abilitata tramite un oggetto Criteri di gruppo, un pannello di controllo di MBAM personalizzato denominato opzioni di crittografia BitLocker sarà disponibile in **sistema e sicurezza**. Questo pannello di controllo personalizzato sostituisce il pannello di controllo BitLocker predefinito di Windows. Il pannello di controllo di MBAM consente di sbloccare le unità crittografate (fisse e rimovibili) e consente anche di gestire il PIN o la password.

[Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## Altre risorse per l'amministrazione delle funzionalità di MBAM


[Operazioni relative a MBAM 1.0](operations-for-mbam-10.md)

 

 





