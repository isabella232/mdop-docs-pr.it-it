---
title: Pianificazione della distribuzione del client di MBAM 1.0
description: Pianificazione della distribuzione del client di MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825876"
---
# Pianificazione della distribuzione del client di MBAM 1.0


A seconda di quando si distribuisce il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, è possibile abilitare la crittografia BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito. Per abilitare la crittografia BitLocker dopo che l'utente finale ha ricevuto il computer, configurare criteri di gruppo. Per abilitare la crittografia BitLocker prima che l'utente finale riceva il computer, distribuire il software del client MBAM usando un sistema di distribuzione del software aziendale.

Puoi usare uno o entrambi i metodi dell'organizzazione. Se si usano entrambi i metodi, è possibile migliorare la conformità, la creazione di report e il supporto per il recupero della chiave.

**Nota**  Per esaminare i requisiti di sistema client di MBAM, vedere [configurazioni supportate di mbam 1,0](mbam-10-supported-configurations.md).

 

## Distribuzione del client MBAM per abilitare la crittografia BitLocker dopo la distribuzione del computer agli utenti finali


Dopo aver configurato i criteri di gruppo, è possibile usare un prodotto di sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager 2012 o Active Directory Domain Services, per distribuire i file di installazione di Windows Installer di MBAM client nei computer di destinazione. I due file di installazione di Windows Installer di MBAM client sono MBAMClient-64bit.msi e MBAMClient-32bit.msi, forniti con il software MBAM. Per altre informazioni su come distribuire gli oggetti dei criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 1,0](deploying-mbam-10-group-policy-objects.md).

Quando si distribuisce il client MBAM, dopo aver distribuito i computer agli utenti finali, viene chiesto agli utenti finali di crittografare i propri computer. In questo modo MBAM raccoglie i dati, includendo il PIN e la password e quindi inizia il processo di crittografia.

**Nota**  In questo approccio agli utenti viene richiesto di attivare e inizializzare il chip Trusted Platform Module (TPM), se non è stato attivato in precedenza.

 

## Uso del client MBAM per abilitare la crittografia BitLocker prima della distribuzione del computer per gli utenti finali


Nelle organizzazioni in cui i computer vengono ricevuti e configurati in modo centralizzato, è possibile installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che vengano scritti i dati degli utenti. Il vantaggio di questo processo è che ogni computer sarà conforme alla crittografia BitLocker. Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer. Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.

Se l'organizzazione vuole usare (TPM) per crittografare i computer, l'amministratore deve crittografare il volume del sistema operativo del computer con TPM Protector. Se l'organizzazione vuole usare il chip TPM e una protezione PIN, l'amministratore deve crittografare il volume di sistema con la protezione TPM, quindi gli utenti selezionano un PIN la prima volta che accedono. Se l'organizzazione decide di usare solo la protezione PIN, l'amministratore non deve prima crittografare il volume. Quando gli utenti accedono ai propri computer, MBAM chiede di specificare un PIN o un PIN e una password che utilizzeranno quando riavviano il computer in un secondo momento.

**Nota**  L'opzione Protector TPM richiede all'amministratore di accettare il prompt del BIOS per attivare e inizializzare il TPM prima di consegnare il computer all'utente.

 

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 1.0](planning-to-deploy-mbam-10.md)

[Distribuzione del client MBAM 1.0](deploying-the-mbam-10-client.md)

 

 





