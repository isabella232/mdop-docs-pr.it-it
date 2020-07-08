---
title: Pianificazione della distribuzione del client di MBAM 2.5
description: Pianificazione della distribuzione del client di MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825995"
---
# Pianificazione della distribuzione del client di MBAM 2.5


A seconda di quando si distribuisce il software client di amministrazione e monitoraggio di Microsoft BitLocker (MBAM), è possibile abilitare la crittografia unità BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito. Sia per MBAM stand-alone che per le topologie di integrazione di System Center Configuration Manager, è necessario configurare le impostazioni dei criteri di gruppo per MBAM.

Se si usa la topologia di MBAM autonoma, è consigliabile usare un sistema di distribuzione del software aziendale per distribuire il software client MBAM ai computer degli utenti finali.

Se si distribuisce MBAM con la topologia di integrazione di Configuration Manager, è possibile usare Gestione configurazione per distribuire il software del client MBAM ai computer degli utenti finali. In Configuration Manager, l'installazione di MBAM crea una raccolta di computer che MBAM può gestire. Questa raccolta include workstation e dispositivi che non dispongono di un TPM (Trusted Platform Module), ma che eseguono Windows 8, Windows 8,1 o Windows 10.

**Nota**  Windows to go non è supportato per l'installazione della topologia di integrazione di Configuration Manager quando si usa Configuration Manager 2007.

 

## Distribuzione del client MBAM per abilitare la crittografia unità BitLocker dopo la distribuzione del computer agli utenti finali


Dopo aver configurato Criteri di gruppo, è possibile usare un prodotto di sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager o Active Directory Domain Services (AD DS) per distribuire i file di Windows Installer dell'installazione del client MBAM in computer di destinazione. Per distribuire il client MBAM, è possibile usare i file di MbamClientSetup.exe o di MBAMClient.msi bit a 32 o 64, forniti con il software client MBAM.

**Nota**  A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM. È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto.

 

Quando si distribuisce il client MBAM dopo la distribuzione di computer ai computer client, agli utenti finali viene richiesto di crittografare il computer. Questa azione consente a MBAM di raccogliere i dati, che includono il PIN e la password (se necessario per i criteri) e quindi per iniziare il processo di crittografia.

**Nota**  In questo approccio gli utenti finali che hanno computer con un chip TPM viene richiesto di attivare e inizializzare il chip TPM se il chip non è stato attivato in precedenza.

 

## Uso del client MBAM per abilitare la crittografia unità BitLocker prima della distribuzione del computer per gli utenti finali


Nelle organizzazioni in cui i computer vengono ricevuti e configurati centralmente e in cui i computer hanno un chip TPM conforme, è possibile usare il client MBAM per gestire la crittografia unità BitLocker in ogni computer prima che vengano scritti i dati degli utenti. Il vantaggio di questo processo è che ogni computer è quindi conforme. Questo metodo non si basa sull'azione dell'utente finale perché l'amministratore ha già crittografato il computer. Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente finale.

Se l'organizzazione vuole usare il chip TPM per crittografare i computer, l'amministratore aggiunge la protezione TPM per crittografare il volume del sistema operativo del computer. Se l'organizzazione vuole usare il chip TPM e un dispositivo di protezione PIN, l'amministratore crittografa il volume del sistema operativo con la protezione TPM e quindi gli utenti finali selezionano un PIN quando accedono per la prima volta. Se l'organizzazione decide di usare solo la protezione PIN, l'amministratore non deve prima crittografare il volume. Quando gli utenti finali accedono, l'amministrazione e il monitoraggio di Microsoft BitLocker richiede loro di specificare un PIN oppure un PIN e una password da usare nei riavvii di un computer successivo.

**Nota**  L'opzione Protector TPM richiede all'amministratore di accettare il prompt del BIOS per attivare e inizializzare il TPM prima che il computer venga recapitato all'utente finale.

 

## Supporto di MBAM client per dischi rigidi crittografati


MBAM supporta BitLocker su dischi rigidi crittografati che soddisfano i requisiti per le specifiche TCG per gli standard Opal e IEEE 1667. Quando BitLocker è abilitato in questi dispositivi, genererà le chiavi ed eseguirà le funzioni di gestione nell'unità crittografata. Per altre informazioni, Vedi disco [rigido crittografato](https://technet.microsoft.com/library/hh831627.aspx) .


## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)

[Distribuzione del client di MBAM 2.5](deploying-the-mbam-25-client.md)

 

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




