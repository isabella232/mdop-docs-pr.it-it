---
title: Modifica della frequenza delle attività pianificate di UE-V
description: Modifica della frequenza delle attività pianificate di UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822686"
---
# Modifica della frequenza delle attività pianificate di UE-V


Il programma di installazione dell'agente Microsoft User Experience Virtualization (UE-V), AgentSetup.exe, crea due attività pianificate durante l'installazione di agente UE-V. Le due attività sono l'attività di **aggiornamento automatico del modello** e l'impostazione dell'attività di **stato della posizione di archiviazione** . Queste attività pianificate non possono essere configurate con gli strumenti UE-V. Gli amministratori che desiderano modificare l'attività pianificata per questi elementi possono creare uno script che usa le opzioni della riga di comando Schtasks.exe.

Per altre informazioni su Schtasks.exe, vedere [come usare schtasks, exe per pianificare le attività in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

## Aggiornamento automatico del modello


L'attività di **aggiornamento automatico del modello** controlla il catalogo di modelli di impostazioni per nuovi, aggiornati o rimossi. Questa attività viene eseguita solo se il SettingsTemplateCatalog è configurato. L'attività di **aggiornamento automatico del modello** esegue il file ApplySettingsCatalog.exe, che si trova nella directory di installazione dell'agente UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome attività</th>
<th align="left">Trigger predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aggiornamento automatico di \Microsoft\UE-V\Template</p></td>
<td align="left"><p>3:30 AM ogni giorno</p></td>
</tr>
</tbody>
</table>

 

**Esempio:** Il comando seguente consente di configurare l'agente per controllare l'archivio di catalogo dei modelli di impostazioni ogni ora.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## Stato della posizione di archiviazione delle impostazioni


L'attività per l' **impostazione dello stato della posizione di archiviazione** esegue le operazioni seguenti:

1.  Verifica che le cartelle UE-V siano ancora bloccate o registrate con la caratteristica file offline.

2.  Verifica se la posizione di archiviazione delle impostazioni è offline o online.

3.  Impone una sincronizzazione nell'intervallo specificato anziché l'intervallo predefinito per i file offline.

4.  Sincronizza tutti i pacchetti di impostazioni configurati per essere precaricati.

5.  Verifica se il percorso della directory Home di Active Directory è cambiato.

6.  Scrive la configurazione dello spazio di archiviazione delle impostazioni corrente nella posizione seguente

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Nome attività</th>
    <th align="left">Trigger predefinito</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Stato della posizione di archiviazione di \Microsoft\UE-V\Settings</p></td>
    <td align="left"><p>All'accesso di qualsiasi utente, dopo l'attivazione, ripetere ogni 30 minuti a tempo indeterminato.</p></td>
    </tr>
    </tbody>
    </table>

     

**Esempio:** Il comando seguente configura l'agente per eseguire l'azione sopra ogni ora.

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## Argomenti correlati


[Amministrazione di UE-V 1.0](administering-ue-v-10.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

 

 





