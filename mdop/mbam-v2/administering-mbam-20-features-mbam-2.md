---
title: Amministrazione delle funzionalità di MBAM 2.0
description: Amministrazione delle funzionalità di MBAM 2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823506"
---
# Amministrazione delle funzionalità di MBAM 2.0


Dopo aver completato tutte le pianificazioni necessarie e aver poi distribuito Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurarlo e usarlo per gestire la crittografia BitLocker nell'organizzazione le informazioni in questa sezione descrivono le attività di amministrazione e monitoraggio di Microsoft BitLocker per la gestione quotidiana delle funzionalità.

## Gestire i ruoli di amministratore di MBAM


Dopo aver completato la configurazione di MBAM per tutte le funzionalità del server, agli utenti amministrativi deve essere concesso l'accesso. Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di MBAM server devono essere assegnati ai gruppi di sicurezza di Active Directory Domain Services e quindi tali gruppi devono essere aggiunti al gruppo locale amministrativo di MBAM appropriato.

[Come gestire i ruoli di amministrazione di MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md)

## Gestire le esenzioni crittografiche di BitLocker


MBAM consente di concedere esenzioni di crittografia a utenti specifici che non hanno bisogno o vogliono crittografare le unità. L'esenzione dal computer viene in genere usata quando una società dispone di computer che non devono essere crittografati, ad esempio i computer usati in sviluppo o test o i computer meno recenti che non supportano BitLocker. In alcuni casi, la legge locale può anche richiedere che determinati computer non siano crittografati.

[Come gestire le esenzioni della crittografia BitLocker dell'utente](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## Gestire le opzioni di crittografia di BitLocker client di MBAM tramite il pannello di controllo


MBAM fornisce un pannello di controllo personalizzato, denominato opzioni di crittografia BitLocker, che verrà visualizzato in **sistema e sicurezza**. Il pannello di controllo di MBAM può essere usato per sbloccare le unità fisse e rimovibili crittografate e gestire anche il PIN o la password.

**Nota**  Questo pannello di controllo personalizzato non sostituisce il pannello di controllo BitLocker predefinito di Windows.

 

[Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## Altre risorse per l'amministrazione delle funzionalità di MBAM


[Operazioni relative a MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





