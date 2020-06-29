---
title: Metodi di sincronizzazione per UE-V 2.x
description: Metodi di sincronizzazione per UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823576"
---
# Metodi di sincronizzazione per UE-V 2.x


L'agente Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 consente di sincronizzare le impostazioni dell'applicazione e di Windows degli utenti con la posizione di archiviazione delle impostazioni. La configurazione del *metodo di sincronizzazione* definisce il modo in cui l'agente UE-V carica e Scarica tali impostazioni nella posizione di archiviazione delle impostazioni. UE-V 2. x introduce una nuova SyncMethod denominata *SyncProvider*. Per altre informazioni sugli eventi trigger che avviano la sincronizzazione delle impostazioni dell'applicazione e di Windows, vedere [sincronizzazione degli eventi trigger per UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).

## Configurazione di SyncMethod


Questa tabella illustra le modifiche apportate a SyncMethod da UE-V v 1.0 a v 2.0 a v 2.1, nonché le impostazioni per ogni configurazione:

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurazione di SyncMethod</strong></p></td>
<td align="left"><p><strong>V 1.0</strong></p></td>
<td align="left"><p><strong>V 2.0</strong></p></td>
<td align="left"><p><strong>V 2.1 e V 2.1 SP1</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncProvider</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>Default</p></td>
<td align="left"><p>Default</p></td>
<td align="left"><p>Le modifiche alle impostazioni per un'applicazione specifica o per le impostazioni desktop di Windows globali vengono salvate localmente in una cartella della cache. Queste modifiche vengono quindi sincronizzate con il percorso di archiviazione delle impostazioni quando si verifica un evento trigger di sincronizzazione. La modifica delle modifiche consente di salvare le modifiche locali nel percorso di archiviazione delle impostazioni.</p>
<p>Questa impostazione predefinita è lo standard Gold per i computer. Questa opzione consente di sincronizzare l'impostazione e il timeout dopo un breve ritardo per verificare che l'avvio dell'applicazione o del sistema operativo non venga ritardato per un lungo periodo di tempo.</p>
<p>Questa funzionalità è legata anche all'attività programmata: applicazione di controllo di sincronizzazione. L'amministratore controlla la frequenza dell'attività pianificata. Per impostazione predefinita, i computer sincronizzano le impostazioni ogni 30 minuti dopo l'accesso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OfflineFiles</p></td>
<td align="left"><p>Default</p></td>
<td align="left"><p>Deprecato</p></td>
<td align="left"><p>Deprecato</p></td>
<td align="left"><p>Si comporta come SyncProvider in V 2.0.</p>
<p>Se i file offline sono abilitati e la cartella viene bloccata, l'UE-V sbloccare questa cartella e la sincronizzazione direttamente con la directory centrale SMB.</p>
<p><strong>Nota: </strong> in V 1.0 se si vuole usare l'UE-v in modalità disconnessa corpnet (aka che viaggia con un portatile), la guida consiste nell'usare i file offline per verificare che le impostazioni siano in roaming.È stato ricevuto un sufficiente feedback dei clienti che l'attivazione di file offline è un blocco aziendale non banale. Quindi in UE-V 2 abbiamo creato un motore di sincronizzazione strettamente accoppiato per memorizzare nella cache i dati localmente e sincronizzare le impostazioni con il server centrale. Questa area di funzionalità non sostituisce i file offline o il reindirizzamento delle cartelle.</p>
<p>UE-V 2 non funziona bene con le cartelle offline in modo che le indicazioni non consentiranno di impostare il percorso di archiviazione delle impostazioni su una cartella offline o CSC bloccata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>External</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>Supportato</p></td>
<td align="left"><p>Nuovo in UE-V 2,1, questo metodo di configurazione specifica che se le impostazioni UE-V vengono scritte in una cartella locale nel computer utente, è possibile usare qualsiasi motore di sincronizzazione esterno, ad esempio OneDrive for business, cartelle di lavoro, SharePoint o Dropbox, per applicare queste impostazioni ai diversi computer a cui gli utenti accedono.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Questa impostazione di configurazione è progettata principalmente per l'infrastruttura VDI (Virtual Desktop Infrastructure) e per l'esperienza di applicazione in streaming. Questa impostazione deve essere usata nelle caselle di Windows Server usate in un Data Center, dove la connessione sarà sempre disponibile.</p>
<p>Tutte le modifiche apportate alle impostazioni vengono salvate direttamente nel server. Se la connessione di rete al percorso di archiviazione delle impostazioni non è disponibile, le modifiche apportate alle impostazioni vengono memorizzate nella cache del dispositivo e vengono sincronizzate la volta successiva che il provider di sincronizzazione viene eseguito. Se il percorso di archiviazione delle impostazioni non viene trovato e il profilo utente viene rimosso da un ambiente VDI in pool durante la disconnessione, le modifiche alle impostazioni andranno perse e l'utente dovrà riapplicare la modifica quando il computer potrà raggiungere di nuovo il percorso di archiviazione delle impostazioni.</p>
<p>Le app e il sistema operativo aspetteranno indefinitamente che la posizione sia presente. Ciò potrebbe causare il caricamento dell'app o il tempo di accesso del sistema operativo per aumentare in modo significativo se la posizione non viene trovata.</p></td>
</tr>
</tbody>
</table>

 

Puoi configurare il metodo di sincronizzazione in questi modi:

-   Quando si [distribuisce l'agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) tramite un parametro della riga di comando o in uno script batch

-   Impostazioni di [criteri di gruppo](https://technet.microsoft.com/library/dn458893.aspx)

-   Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) per UE-V

-   Dopo l'installazione dell'agente UE-V, usare [Windows PowerShell o Strumentazione gestione Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)






## Argomenti correlati


[Distribuire le funzionalità necessarie per UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[Distribuire le funzionalità necessarie per UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





