---
title: Novità in UE-V 2.1 SP1
description: Novità in UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827426"
---
# Novità in UE-V 2.1 SP1


Esperienza utente virtualizzazione 2,1 SP1 offre queste nuove funzionalità e funzionalità rispetto a UE-V 2,1. Le [Note sulla versione di Microsoft User Experience Virtualization (UE-v) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) contengono ulteriori informazioni sulla versione UE-v 2,1 SP1.

## Supporto per Windows 10


UE-V 2,1 SP1 aggiunge il supporto per Windows 10, oltre allo stesso software supportato nelle versioni precedenti di UE-V.

### Compatibilità con Microsoft Azure

Windows 10 consente agli utenti aziendali di sincronizzare le impostazioni delle app di Windows e le impostazioni del sistema operativo Windows in Azure anziché in OneDrive. Puoi usare la funzionalità di sincronizzazione di Windows 10 Enterprise insieme a UE-V solo per i computer locali uniti al dominio. Per consentire la coesistenza tra Windows 10 e UE-V, è necessario disabilitare i modelli UE-V seguenti usando PowerShell per ogni client o criteri di gruppo.

In criteri di gruppo, in Microsoft User Experience Virtualization node, configurare queste impostazioni dei criteri:

-   Abilitare "non sincronizzare le app di Windows"

-   Disabilitare "Sincronizza impostazioni di Windows"

### Comportamento della sincronizzazione delle impostazioni modificato per il supporto di Windows 10

UE-V 2,1 SP1 si aggira sulle impostazioni della barra delle applicazioni tra i dispositivi Windows 10. Tuttavia, UE-V non sincronizza le impostazioni della barra delle applicazioni tra dispositivi e dispositivi Windows 10 in cui sono in uso sistemi operativi precedenti.

Inoltre, UE-V 2,1 SP1 non sincronizza le impostazioni tra la calcolatrice Microsoft in Windows 10 e la calcolatrice Microsoft nei sistemi operativi precedenti.

## Supporto aggiunto per le stampanti di rete mobili


UE-V 2,1 SP1 consente alle stampanti di rete di spostarsi tra i dispositivi in modo che l'utente abbia accesso alle stampanti di rete quando si è connessi a qualsiasi dispositivo della rete. Questo include il roaming della stampante impostata come predefinita.

La stampante in roaming in UE-V richiede uno di questi scenari:

-   Il server di stampa può scaricare il driver necessario quando si sposta in roaming su un nuovo dispositivo.

-   Il driver per la stampante di rete mobile è preinstallato in qualsiasi dispositivo che deve accedere alla stampante di rete.

-   Il driver della stampante può essere ottenuto da Windows Update.

**Nota**  La funzionalità di roaming della stampante UE-V **non** esegue la roaming delle impostazioni o delle preferenze della stampante, ad esempio la stampa fronte-retro.

 

## Modello di posizione delle impostazioni di Office 2013


UE-V 2,1 e 2,1 SP1 includono il modello di posizione delle impostazioni di Microsoft Office 2013 con il supporto per la firma di Outlook migliorato. È stata aggiunta la sincronizzazione delle impostazioni predefinite della firma per i messaggi di posta elettronica nuovi, di risposta e inoltrati. I clienti non devono più scegliere le impostazioni predefinite della firma.

**Nota**  È necessario creare un profilo di Outlook per qualsiasi dispositivo in cui un utente vuole sincronizzare la firma di Outlook. Se il profilo non è già stato creato, l'utente può crearne uno e quindi riavviare Outlook in tale dispositivo per abilitare la sincronizzazione della firma.

 

In precedenza la versione UE-V includeva i modelli di posizione delle impostazioni di Microsoft Office 2010 distribuiti automaticamente e registrati con l'agente UE-V. UE-V 2,1 funziona con Office 365 per determinare se le impostazioni di Office 2013 sono in roaming da Office 365. Se le impostazioni sono in roaming con Office 365, non vengono spostate in roaming da UE-V. [Panoramica delle impostazioni utente e roaming per Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) offre ulteriori informazioni.

Per abilitare la sincronizzazione delle impostazioni tramite UE-V 2,1, eseguire una delle operazioni seguenti:

-   Usare criteri di gruppo per disabilitare la sincronizzazione di Office 365

-   Non abilitare l'esperienza di sincronizzazione di Office 365 durante l'installazione di Office 2013

UE-V 2,1 include i [modelli di office 2013 e office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Questa versione rimuove i modelli di Office 2007. Gli utenti possono ancora usare i modelli di Office 2007 da UE-V 2,0 o versioni precedenti e possono ancora ottenere i modelli dalla raccolta modelli di UE-V che si trova [qui](https://go.microsoft.com/fwlink/p/?LinkID=246589).






## Argomenti correlati


[Introduzione a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparare una distribuzione UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





