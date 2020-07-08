---
title: Pianificazione della distribuzione del client di MBAM 2.0
description: Pianificazione della distribuzione del client di MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804365"
---
# Pianificazione della distribuzione del client di MBAM 2.0


A seconda di quando si distribuisce il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, è possibile abilitare la crittografia unità BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito. Sia per il MBAM autonomo che per le topologie di Configuration Manager, è necessario configurare le impostazioni dei criteri di gruppo per MBAM.

Se si usa la topologia autonoma di MBAM, è consigliabile usare un sistema di distribuzione del software aziendale per distribuire il software client MBAM ai computer degli utenti finali.

Se si distribuisce MBAM con la topologia di Configuration Manager, è possibile usare Configuration Manager per distribuire il software client MBAM ai computer degli utenti finali. In Configuration Manager, l'installazione di MBAM crea una raccolta di computer che MBAM può gestire. Questa raccolta include workstation e dispositivi che non dispongono di un TPM (Trusted Platform Module), ma che eseguono Windows 8.

**Nota**  Windows to go non è supportato per le installazioni di gestione configurazione integrata di MBAM se si usa Configuration Manager 2007.

 

## Distribuzione del client MBAM per abilitare la crittografia BitLocker dopo la distribuzione del computer agli utenti finali


Dopo aver configurato Criteri di gruppo, è possibile usare un prodotto di sistema di distribuzione del software aziendale, ad esempio Microsoft System Center Configuration Manager o Active Directory Domain Services (AD DS) per distribuire i file di Windows Installer dell'installazione del client MBAM in computer di destinazione. Per distribuire il client MBAM, è possibile usare i file di MbamClientSetup.exe o di MBAMClient.msi bit a 32 o 64, forniti con il software MBAM.

Quando si distribuisce il client MBAM dopo la distribuzione di computer ai computer client, agli utenti finali viene richiesto di crittografare il computer. Questo consente a MBAM di raccogliere i dati, che includono il PIN e la password e quindi di iniziare il processo di crittografia.

**Nota**  In questo approccio gli utenti che dispongono di computer con un chip TPM viene richiesto di attivare e inizializzare il chip TPM se il chip non è stato attivato in precedenza.

 

## Uso del client MBAM per abilitare la crittografia BitLocker prima della distribuzione del computer per gli utenti finali


Nelle organizzazioni in cui i computer vengono ricevuti e configurati centralmente e in cui i computer hanno un chip TPM conforme, è possibile installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che vengano scritti i dati degli utenti. Il vantaggio di questo processo consiste nel fare in modo che tutti i computer siano conformi alla crittografia BitLocker. Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer. Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.

Se l'organizzazione vuole usare il chip TPM per crittografare i computer, l'amministratore aggiunge la protezione TPM per crittografare il volume del sistema operativo del computer. Se l'organizzazione vuole usare il chip TPM e una protezione PIN, l'amministratore crittografa il volume del sistema operativo con la protezione TPM e quindi gli utenti selezionano un PIN durante l'accesso per la prima volta. Se l'organizzazione decide di usare solo la protezione PIN, l'amministratore non deve prima crittografare il volume. Quando gli utenti accedono all'accesso, l'amministrazione e il monitoraggio di Microsoft BitLocker richiedono loro di specificare un PIN oppure un PIN e una password da usare nei riavvii di un computer successivo.

**Nota**  L'opzione Protector TPM richiede all'amministratore di accettare il prompt del BIOS per attivare e inizializzare il TPM prima che il computer venga recapitato all'utente.

 

## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Distribuzione del client MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)

 

 





