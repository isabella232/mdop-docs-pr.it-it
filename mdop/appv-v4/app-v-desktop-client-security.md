---
title: Sicurezza di App-V Desktop Client
description: Sicurezza di App-V Desktop Client
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822316"
---
# Sicurezza di App-V Desktop Client


Il client Desktop App-V offre numerosi miglioramenti della sicurezza non disponibili nelle versioni precedenti del prodotto. Queste modifiche conferiscono livelli di sicurezza più alti per impostazione predefinita e tramite la configurazione delle impostazioni del client.

**Nota**  Quando si installa il client Desktop App-V in un computer, il software viene impostato automaticamente sulle impostazioni più sicure. Tuttavia, durante l'aggiornamento, le impostazioni precedenti del client persistono.

 

Per impostazione predefinita, il client Desktop App-V è configurato solo con le autorizzazioni necessarie per consentire a un utente non amministrativo di eseguire un'applicazione di aggiornamento e flusso di pubblicazione. I miglioramenti aggiuntivi per la sicurezza forniti nel client desktop di App-V includono i seguenti:

-   Per impostazione predefinita, un aggiornamento della cache OSD è consentito solo dal processo di aggiornamento della pubblicazione.

-   Il file di log ( `sftlog.txt` ) è accessibile solo dagli account con accesso amministrativo locale al client.

-   Il file di log ha ora una dimensione massima.

-   I file di log vengono gestiti tramite le impostazioni di archiviazione.

-   Ora viene eseguita la registrazione degli eventi di sistema.

## Autorizzazioni


Dopo aver installato il client desktop, è possibile configurare altre impostazioni di sicurezza tramite MMC o un singolo client usando il registro di sistema o il modello ADM fornito da Microsoft. Il client Desktop App-V dispone delle autorizzazioni che è possibile impostare per limitare l'accesso a tutte le funzionalità del client desktop da parte di utenti non amministrativi. Per un elenco completo delle autorizzazioni, vedere il file della Guida dell'App-V client o l'App-V Operations Guide.

**Importante**  Valutare attentamente le conseguenze della modifica dei diritti di accesso, in particolare nei sistemi condivisi da più utenti, ad esempio i server terminal.

 

**Nota**  Se gli utenti dell'ambiente hanno privilegi di amministratore locale per i propri computer, le autorizzazioni vengono ignorate.

 

### Modello ADM

Microsoft Application Virtualization (App-V) introduce un modello ADM che può essere usato per configurare le impostazioni client più comuni tramite criteri di gruppo. Questo modello consente agli amministratori di implementare e modificare molte delle impostazioni del client tramite un modello di amministrazione centralizzato. Alcune delle impostazioni disponibili nel modello ADM sono le impostazioni di sicurezza.

**Importante**  Quando si usa il modello ADM, tenere presente che le impostazioni sono le impostazioni delle preferenze dei criteri di gruppo e i criteri di gruppo non completamente gestiti.

 

Per una descrizione completa del modello ADM, delle impostazioni specifiche e delle indicazioni per la distribuzione corretta dei client nell'ambiente, vedere il white paper su App-V ADM [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .

## Rimozione delle associazioni di tipi di file OSD


Se l'organizzazione non richiede agli utenti di aprire applicazioni direttamente da un file OSD, è possibile migliorare la sicurezza rimuovendo le associazioni di tipi di file nel client. Rimuovere le `HKEY_CURRENT_USERS` chiavi per OSD e `Softgird.osd.file` usare l'editor del registro di sistema. Puoi inserire questo processo in uno script di accesso o in uno script di post-installazione per automatizzare le modifiche.

 

 





