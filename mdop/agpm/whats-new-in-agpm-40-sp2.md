---
title: Novità di Gestione avanzata Criteri di gruppo 4.0 SP2
description: Novità di Gestione avanzata Criteri di gruppo 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818146"
---
# Novità di Gestione avanzata Criteri di gruppo 4.0 SP2


Questo contenuto descrive i miglioramenti e le configurazioni supportate per il servizio Pack2 (Advanced Group Policy Management) 4.0 (SP2). Se c'è una differenza tra questo contenuto e altre documentazioni di Advanced Group Policy Management, considera questo contenuto autorevole e presupponga che sostituisca l'altra documentazione.

## <a href="" id="what-s-new"></a>Novità


Advanced Group Policy Management 4.0 SP2 supporta le caratteristiche e le funzionalità seguenti.

### Supporto per Windows 8.1 e Windows Server2012 R2

Advanced Group Policy Management 4.0 SP2 aggiunge il supporto per i sistemi operativi Windows 8.1 e Windows Server2012 R2.

### Estensioni lato client nuove e modificate

Le estensioni lato client di criteri di gruppo sono state aggiunte o modificate per Advanced Group Policy Management per supportare le nuove impostazioni dei criteri in Windows 8.1. Queste impostazioni dei criteri consentono agli amministratori dei criteri di gruppo di gestire e tenere traccia delle impostazioni dei criteri specifiche di Windows 8.1 che cambiano tra due oggetti Criteri di gruppo o i modelli. Per visualizzare le estensioni lato client, usare i report impostazioni e differenze disponibili nel client Advanced Group Policy Management.

Le nuove estensioni lato client di criteri di gruppo modificate sono:

-   **Specificare le impostazioni delle cartelle di lavoro**. Se si abilita questa impostazione, gli amministratori IT possono configurare le cartelle di lavoro per la creazione automatica. La caratteristica cartelle di lavoro consente agli utenti finali di sincronizzare i file dai loro dispositivi desktop Windows con altri dispositivi. Usa questa impostazione per creare la relazione di sincronizzazione nei dispositivi di un utente finale e per configurare come identificare il file server in cui sono archiviate le cartelle di lavoro dell'utente. Se si seleziona la casella di controllo **sincronizzazione automatica provisioning** , la relazione di sincronizzazione verrà creata senza l'input dell'utente e i dati inizieranno automaticamente la sincronizzazione con il dispositivo dell'utente. Se non si seleziona la casella di controllo **sincronizzazione automatica provisioning** , gli utenti devono fornire l'input per avviare la sincronizzazione.

-   **Forzare la configurazione automatica per tutti gli utenti**. Se si abilita questa impostazione, gli amministratori IT possono determinare se creare automaticamente la partnership delle cartelle di lavoro nei dispositivi dell'utente finale senza input dagli utenti finali. Se si abilita questa impostazione, la sincronizzazione verrà configurata in base alla configurazione dell'impostazione specifica dei criteri **delle impostazioni delle cartelle di lavoro** . Se si imposta l'impostazione **Imponi configurazione automatica per tutti gli utenti** su **disabilitata** o **non configurata**, la partnership delle cartelle di lavoro verrà configurata in base a come si imposta l'opzione di **provisioning automatico** nell'impostazione specifica dei criteri **delle cartelle di lavoro** .

Per altre informazioni sulla funzionalità delle cartelle di lavoro, vedere [Panoramica delle cartelle di lavoro](https://go.microsoft.com/fwlink/?LinkId=330444).

### Feedback dei clienti e aggiornamento cumulativo

Advanced Group Policy Management 4.0 SP2 include un rollup di hotfix per risolvere i problemi riscontrati dopo la versione del servizio Advanced Group Policy Management 4.0 Service Pack1 (SP1). Advanced Group Policy Management 4.0 SP2 contiene le correzioni più recenti e include Microsoft Advanced Group Policy Manager 4.0 SP1 Hotfix1. Per altre informazioni, vedere l'articolo [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)della Knowledge base.

### Nuove estensioni dei criteri di gruppo nei report impostazioni e differenze

Le nuove estensioni di criteri di gruppo sono state aggiunte ai report impostazioni e differenze.

### Modifiche e supporto del programma di installazione

Le modifiche e il supporto per il programma di installazione di Advanced Group Policy Management 4.0 SP2 sono:

-   Se si installa Advanced Group Policy Management 4.0 SP2 nel sistema operativo Windows 8 o Windows Server 2012 o nei sistemi operativi successivi, il programma di installazione della Advanced Group Policy Manager verifica che sia installato il software necessario richiesto, ovvero la console Gestione criteri di gruppo e Microsoft .NET Framework 3.5. Se il software prerequisito non è installato, l'installazione di Advanced Group Policy Management 4.0 SP2 è bloccata.

-   Quando si installa il server Advanced Group Policy Management, l'attivazione di WCF, l'attivazione non HTTP e il servizio Attivazione processo Windows vengono abilitati automaticamente.

-   Nel sistema operativo client WindowsVista e nei sistemi operativi successivi scaricare la versione appropriata degli strumenti di amministrazione del sistema remoto per il sistema operativo prima di installare Advanced Group Policy Management 4.0 SP2.

-   Advanced Group Policy Management 4.0 SP2 supporta la compatibilità con le versioni precedenti dei sistemi operativi supportati.

### Possibilità di eseguire l'aggiornamento a Advanced Group Policy Management 4.0 SP2 senza immettere nuovamente i parametri di configurazione

È possibile eseguire l'aggiornamento del client Advanced Group Policy Management o del server Advanced Group Policy Management a Advanced Group Policy Management 4.0 SP2 senza che venga chiesto di immettere nuovamente i parametri di configurazione, detti Smart Upgrade, solo da Advanced Group Policy Management 4.0, come illustrato nella tabella seguente. Se si esegue l'aggiornamento a Advanced Group Policy Management 4.0 SP2 da altre versioni di Advanced Group Policy Management, come illustrato nella tabella, è necessario usare l'aggiornamento classico, che richiede di immettere nuovamente i parametri di configurazione. Poiché ogni versione di Advanced Group Policy Management è associata a un particolare sistema operativo, vedere [scelta della versione di Advanced Group Policy per l'installazione](https://go.microsoft.com/fwlink/?LinkId=254350) e verificare che il sistema operativo venga aggiornato in modo appropriato prima di aggiornare Advanced Group Policy Management.

**Aggiornamenti supportati di Advanced Group Policy Management SP2 4,0**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versione Advanced Group Policy Management da cui è possibile eseguire l'aggiornamento</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento classico</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
<td align="left"><p>L'installazione è bloccata</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,0 SP1</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Non applicabile</p></td>
<td align="left"><p>Aggiornamento intelligente</p></td>
</tr>
</tbody>
</table>

 

## Configurazioni supportate


Advanced Group Policy Management 4.0 SP2 supporta le configurazioni della tabella seguente. Anche se Advanced Group Policy Management supporta configurazioni miste, ti consigliamo vivamente di eseguire il client Advanced Group Policy Management e il server Advanced Group Policy Management nella stessa linea di sistema operativo, ad esempio Windows 8.1 con Windows Server2012 R2, Windows 8 con Windows Server 2012 e così via.

**Sistemi operativi e impostazioni dei criteri supportati da Advanced Group Policy Management 4.0 SP2**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configurazioni supportate per il server Advanced Group Policy Management</strong></th>
<th align="left"><strong>Configurazioni supportate per il client Advanced Group Policy Management</strong></th>
<th align="left"><strong>Supporto per Advanced Group Policy</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012, Windows 8.1 o Windows 8</p></td>
<td align="left"><p>Windows Server 2012 o Windows 8</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi preferenza esistenti solo in Windows 8.1 o Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o WindowsVista con Service Pack 1 (SP1)</p></td>
<td align="left"><p>Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</p></td>
<td align="left"><p>Non supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## Prerequisiti per l'installazione di Advanced Group Policy Management 4.0 SP2


La tabella seguente descrive il comportamento dei programmi di installazione del client e del server di Advanced Group Policy Management 4.0 SP2 in Windows 8.1 quando mancano gli strumenti di amministrazione del server remoto .NET Framework 3.5 o GPMC.

**Client Advanced Group Policy**

**Server Advanced Group Policy Management**

**Sistema operativo**

**.NET Framework**

**Strumenti di amministrazione remota del server**

**.NET Framework**

**Strumenti di amministrazione remota del server**

**Windows 8.1**

Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.

Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.

Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.

Se la console GPMC non è abilitata o installata, il programma di installazione blocca le installazioni.

**Windows Server2012 R2**

Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.

Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.

Se .NET Framework 3.5 non è abilitato o non è installato, il programma di installazione blocca le installazioni.

Se GPMC non è abilitato, il programma di installazione lo Abilita durante l'installazione.

 

## Come ottenere le tecnologie MDOP


Advanced Group Policy Management 4,0 SP2 fa parte di Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Argomenti correlati


[Gestione avanzata Criteri di gruppo](index.md)

[Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP2](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[Scelta della versione di Gestione avanzata Criteri di gruppo da installare](choosing-which-version-of-agpm-to-install.md)

 

 





