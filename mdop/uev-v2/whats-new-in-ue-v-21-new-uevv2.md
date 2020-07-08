---
title: Novità in UE-V 2.1
description: Novità in UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826265"
---
# Novità in UE-V 2.1


User Experience Virtualization 2,1 offre queste nuove funzionalità e funzionalità rispetto a UE-V 2,0. Le [Note sulla versione di Microsoft User Experience Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) contengono ulteriori informazioni sulla versione UE-v 2,1.

## Modello di posizione delle impostazioni di Office 2013


UE-V 2,1 include il modello di posizione delle impostazioni di Microsoft Office 2013 con il supporto per la firma di Outlook migliorato. In UE-V 2,1 i dati della firma vengono sincronizzati tra i dispositivi utente. È stata aggiunta la sincronizzazione delle impostazioni predefinite della firma per i messaggi di posta elettronica nuovi, di risposta e inoltrati. I clienti non devono più scegliere le impostazioni predefinite della firma.

**Nota**  È necessario creare un profilo di Outlook per qualsiasi dispositivo in cui un utente vuole sincronizzare la firma di Outlook. Se il profilo non è già stato creato, l'utente può crearne uno e quindi riavviare Outlook in tale dispositivo per abilitare la sincronizzazione della firma.

 

In precedenza la versione UE-V includeva i modelli di posizione delle impostazioni di Microsoft Office 2010 distribuiti automaticamente e registrati con l'agente UE-V. UE-V 2,1 funziona con Office 365 per determinare se le impostazioni di Office 2013 sono in roaming da Office 365. Se le impostazioni sono in roaming con Office 365, non vengono spostate in roaming da UE-V. [Panoramica delle impostazioni utente e roaming per Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) offre ulteriori informazioni.

Per abilitare la sincronizzazione delle impostazioni tramite UE-V 2,1, eseguire una delle operazioni seguenti:

-   Usare criteri di gruppo per disabilitare la sincronizzazione di Office 365

-   Non abilitare l'esperienza di sincronizzazione di Office 365 durante l'installazione di Office 2013

UE-V 2,1 include i [modelli di office 2013 e office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Questa versione rimuove i modelli di Office 2007. Gli utenti possono ancora usare i modelli di Office 2007 da UE-V 2,0 o versioni precedenti e possono ancora ottenere i modelli dalla raccolta modelli di UE-V che si trova [qui](https://go.microsoft.com/fwlink/p/?LinkID=246589).

## Correzione per gli utenti dello spazio dei nomi Distributed file System


In UE-V è stato migliorato il supporto dello spazio dei nomi Distributed file System (DFSN) aggiungendo una configurazione UE-V denominata SyncProviderPingEnabled. La disattivazione di questa configurazione tramite PowerShell o WMI consente agli utenti di disabilitare il ping di UE-V. Il ping di UE-V causa un errore quando si usano i server di DFSN perché questi server non rispondono ai ping. La mancata risposta impedisce la sincronizzazione delle impostazioni di UE-V. La disabilitazione del ping UE-V consente la sincronizzazione di UE-V in modo che funzioni normalmente.

Per disabilitare il ping di UE-V, usare questo cmdlet di PowerShell:

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## Sincronizzazione per le credenziali


UE-V 2,1 offre ai clienti la possibilità di sincronizzare credenziali e certificati archiviati in Gestione credenziali di Windows. Questo componente è disabilitato per impostazione predefinita. L'attivazione di questo componente consente agli utenti di conservare le credenziali di dominio e i certificati in sincronia. Gli utenti possono eseguire l'accesso una sola volta su un dispositivo e queste credenziali verranno spostate per l'utente in tutti i dispositivi abilitati per l'UE-V. [Gestisci le credenziali con UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) offre ulteriori informazioni.

**Nota**  In Windows 8 e versioni successive, gestione credenziali contiene le credenziali Web. Queste credenziali non vengono sincronizzate tra i dispositivi degli utenti.

 

## Sincronizzazione dell'account UE-V e Microsoft


UE-V rileva se "impostazioni di sincronizzazione con OneDrive", nota anche come sincronizzazione dell'account Microsoft, è attivata. Se l'account Microsoft non è configurato per la sincronizzazione delle impostazioni, UE-V sincronizza le app di Windows, i pacchetti AppX e le impostazioni desktop di Windows tra i dispositivi. Ciò consente agli utenti di accedere alle app dello Store, alla musica, alle immagini e ad altre applicazioni Microsoft per l'account, senza eseguire la sincronizzazione all'esterno del firewall aziendale. UE-V controlla se i criteri di gruppo interrompono la sincronizzazione delle impostazioni con OneDrive o se l'utente disabilita la **sincronizzazione delle impostazioni di questo computer** nei controlli utente.

## Supporto per il SyncMethod External


Una nuova [configurazione di SyncMethod](https://technet.microsoft.com/library/dn554321.aspx) denominata **External** specifica che se le impostazioni di UE-V vengono scritte in una cartella locale nel computer utente, è possibile usare qualsiasi motore di sincronizzazione esterno, ad esempio OneDrive for business, cartelle di lavoro, SharePoint o Dropbox, per applicare queste impostazioni ai diversi computer a cui gli utenti accedono.

## Supporto avanzato per la modalità VDI


UE-V 2,1 include il [supporto per le sessioni VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) condivise tra gli utenti finali. Come amministratore, puoi registrare e configurare uno speciale modello VDI, garantendo che UE-V mantenga intatte tutte le sue funzionalità per le sessioni VDI non persistenti.

**Nota**  Se non si Abilita la modalità VDI per le sessioni VDI non persistenti, alcune caratteristiche non funzionano, ad esempio backup/ripristino e LKG.

 

## Backup e ripristino amministrativi


Puoi ripristinare altre impostazioni quando un utente adotta un nuovo dispositivo inserendo un modello di posizione di impostazioni nel profilo di **backup** o **roaming (impostazione predefinita)** usando il cmdlet Set-UevTemplateProfile di PowerShell. In questo modo, le impostazioni del computer vengono sincronizzate con il nuovo computer, oltre alle impostazioni utente. I modelli assegnati al profilo di backup vengono backup per il dispositivo e configurati in base al dispositivo. [Gestire il backup e il ripristino amministrativi in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) offre ulteriori informazioni.

## Sincronizzazione per altre impostazioni di Windows


UE-V Sincronizza ora la personalizzazione della tastiera virtuale, il dizionario ortografico e consente l'attivazione dell'app per le app recenti e le impostazioni del bordo dello schermo per la sincronizzazione tra dispositivi Windows 8 e Windows 8,1.






## Argomenti correlati


[Introduzione a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparare una distribuzione UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





