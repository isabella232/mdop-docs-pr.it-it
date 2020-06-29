---
title: Preparazione dell'ambiente per UE-V
description: Preparazione dell'ambiente per UE-V
author: dansimp
ms.assetid: c93d3b33-e032-451a-9e1b-8534e1625396
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8f806f3c326bad5204a7f1ee69e11b61177e3cce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824646"
---
# Preparazione dell'ambiente per UE-V


Microsoft User Experience Virtualization (UE-V) sposta in roaming le impostazioni tra i computer per l'uso di una posizione di archiviazione delle impostazioni. La posizione di archiviazione delle impostazioni è una condivisione file e deve essere configurata durante la distribuzione dell'agente UE-V. Deve essere definita come posizione di archiviazione delle impostazioni o come directory Home di Active Directory. Inoltre, l'amministratore deve configurare un server temporale per supportare la sincronizzazione coerente. Per preparare l'ambiente per la versione UE-V, tenere presente quanto segue:

-   [Archiviazione delle impostazioni di UE-V](#bkmk-uevsettingsstorage):

    -   [Definizione di una posizione di archiviazione delle impostazioni](#bkmk-definingsettingsstoragelocation)

    -   [Uso della directory Home di Active Directory con UE-V](#bkmk-usingactivedirectoryhomedirectory)

-   [Sincronizzare gli orologi del computer per la sincronizzazione delle impostazioni UE-V](#bkmk-synchronizecomputerclocks)

-   [Pianificazione delle prestazioni e della capacità](#bkmk-performancecapacityplanning)

Per altre informazioni sui requisiti del sistema operativo e del computer, vedere [configurazioni supportate per la versione UE-V 1,0](supported-configurations-for-ue-v-10.md).

## <a href="" id="bkmk-uevsettingsstorage"></a>Archiviazione delle impostazioni di UE-V


Puoi definire l'archiviazione delle impostazioni di virtualizzazione dell'esperienza utente in una delle due configurazioni seguenti: posizione di archiviazione delle impostazioni o directory Home di Active Directory.

### <a href="" id="bkmk-definingsettingsstoragelocation"></a>Definire una posizione di archiviazione delle impostazioni

La posizione di archiviazione delle impostazioni di UE-V è una condivisione di rete standard accessibile dagli utenti di UE-V. Prima di definire la posizione di archiviazione delle impostazioni, è necessario creare una directory radice. Gli utenti che archivieranno le impostazioni nella condivisione devono avere le autorizzazioni di lettura/scrittura per la posizione di archiviazione. L'agente UE-V creerà cartelle specifiche dell'utente nella directory radice. La posizione di archiviazione delle impostazioni viene definita impostando l'opzione di configurazione **SettingsStoragePath** . Questa opzione può essere configurata nei modi seguenti:

-   Durante l'installazione dell'agente UE-V tramite un parametro della riga di comando o in uno script batch.

-   Uso dei criteri di gruppo.

-   Dopo l'installazione, usare PowerShell o WMI.

Il percorso deve trovarsi in un percorso UNC (Universal Naming Convention) del server e condividere. Ad esempio, **\\\\server\\settingsshare\\**. Questa opzione di configurazione supporta l'uso di variabili per abilitare scenari di roaming specifici.

È possibile usare la `%username%` variabile con il percorso UNC del server e condividere. In questo modo verranno fornite le stesse impostazioni in tutti i computer o le sessioni in cui un utente accede. Consideriamo questa configurazione per gli scenari seguenti:

1.  Gli utenti dell'organizzazione hanno più computer fisici configurati in modo simile e le impostazioni di ogni utente devono essere uguali in tutti i computer.

2.  Gli utenti dell'organizzazione usano pool VDI (Virtual Desktop Infrastructure) in cui le impostazioni devono essere mantenute nelle sessioni VDI di ogni utente.

3.  Gli utenti dell'organizzazione hanno un solo computer fisico e usano inoltre un sistema VDI. L'esperienza delle impostazioni di ogni utente dovrebbe essere la stessa se si usa il computer fisico o la sessione VDI.

4.  Più computer aziendali vengono usati da più utenti. L'esperienza delle impostazioni di ogni utente deve essere uguale in tutti i computer.

Puoi usare le variabili **%username%\\%ComputerName%** con il percorso UNC del server e Condividi. Ciò consentirà di mantenere l'esperienza delle impostazioni per ogni computer. Consideriamo questa configurazione per gli scenari seguenti:

1.  Gli utenti dell'organizzazione hanno più computer fisici e si vuole mantenere l'esperienza delle impostazioni per ogni computer.

2.  I computer aziendali vengono usati da più utenti. L'esperienza delle impostazioni deve essere mantenuta per ogni computer in cui l'utente esegue l'accesso.

L'agente UE-V crea dinamicamente il percorso di archiviazione delle impostazioni specifico dell'utente in base a un'impostazione di configurazione di UE-V `SettingsStoragePath` e alle variabili definite.

L'agente UE-V crea in modo dinamico una cartella di sistema nascosta denominata `SettingsPackages` all'interno di ogni posizione di archiviazione specifica dell'utente. L'agente UE-V legge e scrive le impostazioni in questa posizione, come definito dai modelli di posizione delle impostazioni UE-V registrati.

Se il percorso di archiviazione delle impostazioni è lo stesso per un set di computer gestiti di un utente, le impostazioni UE-V applicabili sono determinate dalla regola "ultima scrittura WINS". L'agente che viene eseguito in un computer legge e scrive nella posizione delle impostazioni in modo indipendente dagli agenti eseguiti in altri computer. Le ultime impostazioni e i valori scritti sono le impostazioni applicate quando l'agente successivo legge il percorso di archiviazione delle impostazioni. Per altre informazioni, vedere [distribuzione della posizione di archiviazione delle impostazioni per la versione UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md).

### <a href="" id="bkmk-usingactivedirectoryhomedirectory"></a>Usare Active Directory Home directory con UE-V

Se non è configurata la posizione di archiviazione delle impostazioni per UE-V quando l'agente viene distribuito, viene usata la directory Home Active Directory (AD) dell'utente per archiviare i pacchetti della posizione delle impostazioni. L'agente UE-V crea dinamicamente la cartella di archiviazione delle impostazioni sotto la radice della directory Home di ogni utente. L'agente usa solo la home directory di Active Directory se una posizione di archiviazione delle impostazioni (SettingsStoragePath) non è altrimenti definita.

## <a href="" id="bkmk-synchronizecomputerclocks"></a>Sincronizzare gli orologi del computer per la sincronizzazione delle impostazioni UE-V


I computer che eseguono l'agente UE-V per sincronizzare le impostazioni devono usare un server temporale. I timestamp vengono usati per determinare se le impostazioni devono essere sincronizzate dalla posizione di archiviazione delle impostazioni. Se l'orologio del computer non è accurato, le impostazioni precedenti possono sovrascrivere le impostazioni più recenti o le nuove impostazioni potrebbero non essere salvate nella posizione di archiviazione delle impostazioni. L'uso di un server temporale consente a UE-V di gestire un'esperienza di impostazioni coerenti.

## <a href="" id="bkmk-performancecapacityplanning"></a>Pianificazione delle prestazioni e della capacità


I requisiti di capacità per UE-V possono essere determinati dall'uso della capacità disco standard e del monitoraggio dell'integrità della rete. UE-V usa una condivisione SMB (Server Message Block) per l'archiviazione dei pacchetti di impostazioni. La dimensione dei pacchetti di impostazioni varia in base alle informazioni sulle impostazioni per un'applicazione specifica. Mentre la maggior parte dei pacchetti di impostazioni è di piccole dimensioni, la sincronizzazione di file potenzialmente di grandi dimensioni, ad esempio immagini desktop, può causare scarse prestazioni, in particolare sulle reti più lente. Per ridurre al minimo i problemi relativi alla latenza della rete, è consigliabile creare posizioni di archiviazione delle impostazioni nelle stesse reti locali in cui risiedono i computer degli utenti.

Per impostazione predefinita, la sincronizzazione UE-V verrà disattivata dopo 2 secondi se la rete è lenta o il pacchetto di impostazioni è di grandi dimensioni. È possibile configurare il timeout con criteri di gruppo. Per altre informazioni su come impostare il timeout, vedere [configurazione di UE-V con gli oggetti Criteri di gruppo](configuring-ue-v-with-group-policy-objects.md).

## Argomenti correlati


[Microsoft User Experience Virtualization (UE-V) 1.0](index.md)

[Pianificazione di UE-V 1.0](planning-for-ue-v-10.md)

[Configurazioni supportate per UE-V 1.0](supported-configurations-for-ue-v-10.md)

 

 





