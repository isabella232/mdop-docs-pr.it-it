---
title: Distribuzione del client di MBAM 2.5
description: Distribuzione del client di MBAM 2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826276"
---
# Distribuzione del client di MBAM 2.5


Il software client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione elettronica del software, ad esempio servizi di dominio Active Directory, oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.

A seconda di quando si distribuisce il software client di amministrazione e monitoraggio di Microsoft BitLocker, è possibile abilitare la crittografia unità BitLocker in un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito configurando criteri di gruppo e distribuendo il software del client MBAM usando un sistema di distribuzione del software aziendale.

## Distribuire il client MBAM in computer desktop o portatili


Dopo aver configurato le impostazioni dei criteri di gruppo, è possibile usare un prodotto del sistema di distribuzione del software aziendale, ad esempio MicrosoftSystemCenter2012 ConfigurationManager o Active Directory Domain Services per distribuire i file di installazione di Windows Installer di MBAM client in computer di destinazione. È possibile usare i file di MbamClientSetup.exe a 32 bit o 64 bit o i file di MBAMClient.msi a 32 bit o 64 bit, forniti con il software client MBAM. Per altre informazioni sulla distribuzione delle impostazioni dei criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 2,5](deploying-mbam-25-group-policy-objects.md).

**Nota**  A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM. È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto.

 

[Come distribuire il client MBAM a computer desktop o portatili](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## Distribuire il client MBAM come parte di una distribuzione di Windows


Nelle organizzazioni in cui i computer vengono ricevuti e configurati in modo centralizzato, è possibile installare il client MBAM per gestire la crittografia unità BitLocker in ogni computer prima che vengano scritti i dati degli utenti. Il vantaggio di questo processo è che tutti i computer sono conformi alla crittografia unità BitLocker. Questo metodo non si basa sull'azione dell'utente perché l'amministratore ha già crittografato il computer. Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente. Se le impostazioni dei criteri di gruppo sono state configurate per richiedere un PIN, viene chiesto agli utenti di impostare un PIN dopo la ricezione del criterio.

[Come abilitare BitLocker usando MBAM come parte di una distribuzione di Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## Come distribuire il client MBAM usando una riga di comando


Questa sezione spiega come installare il client MBAM usando una riga di comando.

[Come distribuire il client di MBAM usando una riga di comando](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## Altre risorse per la distribuzione del client MBAM


[Distribuzione di MBAM 2.5](deploying-mbam-25.md)



## Argomenti correlati


[Distribuzione di MBAM 2.5](deploying-mbam-25.md)

[Pianificazione di MBAM 2.5](planning-for-mbam-25.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





