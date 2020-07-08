---
title: Modifica della frequenza delle attività pianificate di UE-V 2. x
description: Modifica della frequenza delle attività pianificate di UE-V 2. x
author: dansimp
ms.assetid: ee486570-c6cf-4fd9-ba48-0059ba877c10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/29/2016
ms.openlocfilehash: 1c1e3c091431dc56068dcd1fe0e849b0df1f6aa0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824426"
---
# Modifica della frequenza delle attività pianificate di UE-V 2. x


Il programma di installazione dell'agente Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, AgentSetup.exe, crea le attività pianificate seguenti durante l'installazione dell'agente UE-V:

-   **Monitorare le impostazioni dell'applicazione**

-   **Applicazione controller di sincronizzazione**

-   **Sincronizzare le impostazioni alla disconnessione**

-   **Aggiornamento automatico del modello**

-   **Raccolta di dati analisi utilizzo software**

-   **Caricare i dati di analisi utilizzo software**

**Nota**  Ad eccezione della raccolta di dati di analisi utilizzo software, queste attività devono rimanere abilitate perché l'UE-V non può funzionare senza di essi.

 

Queste attività pianificate non possono essere configurate con gli strumenti UE-V. Gli amministratori che vogliono modificare l'attività pianificata per questi elementi possono creare uno script che usa le opzioni della riga di comando Schtasks.exe.

Per altre informazioni su Schtasks.exe, vedere [come usare schtasks, exe per pianificare le attività in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).

Per altre informazioni su

## Attività pianificate UE-V


Le attività pianificate seguenti sono incluse in UE-V 2 con i comandi di configurazione delle attività pianificate di esempio.

### Raccolta di dati analisi utilizzo software

Se al momento dell'installazione l'utente o l'amministratore sceglie di partecipare al programma Customer Experience Improvement Program (analisi utilizzo software), UE-V raccoglie i dati per migliorare il prodotto nelle versioni future. Questa attività pianificata viene eseguita solo all'accesso. L'attività di **dati Collect analisi utilizzo software** esegue la UevSqmSession.exe, che si trova nella directory di installazione dell'agente UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome attività</th>
<th align="left">Evento predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dati di \Microsoft\UE-V\Collect analisi utilizzo software</p></td>
<td align="left"><p>Accesso</p></td>
</tr>
</tbody>
</table>

 

### Monitorare le impostazioni dell'applicazione

L'attività **monitora le impostazioni dell'applicazione** viene usata per sincronizzare le impostazioni per le app di Windows. Viene eseguito all'accesso ma viene ritardato di 30 secondi per non influire negativamente sull'accesso. L'attività monitora lo stato dell'applicazione esegue il file UevAppMonitor.exe, che si trova nella directory di installazione dell'agente UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome attività</th>
<th align="left">Evento predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Stato applicazione \Microsoft\UE-V\Monitor</p></td>
<td align="left"><p>Accesso</p></td>
</tr>
</tbody>
</table>

 

### Applicazione controller di sincronizzazione

L'attività dell' **applicazione controller di sincronizzazione** viene usata per avviare il controller di sincronizzazione per sincronizzare le impostazioni dal computer alla posizione di archiviazione delle impostazioni. Per impostazione predefinita, l'attività viene eseguita ogni 30 minuti. In quel momento, le impostazioni locali vengono sincronizzate con il percorso di archiviazione delle impostazioni e le impostazioni aggiornate nella posizione di archiviazione delle impostazioni vengono sincronizzate con il computer. L'applicazione controller di sincronizzazione esegue la Microsoft.Uev.SyncController.exe, che si trova nella directory di installazione dell'agente UE-V.
**Nota:** Come per l'attività di **monitoraggio delle impostazioni dell'applicazione** , questa attività viene eseguita all'accesso, ma viene ritardata di 30 secondi per non influire negativamente sull'accesso.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome attività</th>
<th align="left">Evento predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Applicazione controller \Microsoft\UE-V\Sync</p></td>
<td align="left"><p>Accesso e ogni 30 minuti da allora in poi</p></td>
</tr>
</tbody>
</table>

 

Ad esempio, il comando seguente configura l'agente per la sincronizzazione delle impostazioni ogni 15 minuti anziché i 30 minuti predefiniti.

``` syntax
Schtasks /change /tn “Microsoft\UE-V\Sync Controller Application” /ri 15
```

### Sincronizzare le impostazioni alla disconnessione

L'attività **Sincronizza impostazioni a disconnessione** viene usata per avviare un'applicazione all'accesso che controlla la sincronizzazione delle applicazioni alla disconnessione per l'UE-V. L'attività Sincronizza impostazioni a disconnessione esegue il file Microsoft.Uev.SyncController.exe, che si trova nella directory di installazione dell'agente UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome attività</th>
<th align="left">Evento predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Impostazioni di \Microsoft\UE-V\Synchronize alla disconnessione</p></td>
<td align="left"><p>Accesso</p></td>
</tr>
</tbody>
</table>

 

### Aggiornamento automatico del modello

L'attività di **aggiornamento automatico del modello** controlla il catalogo di modelli di impostazioni per nuovi, aggiornati o rimossi. Questa attività viene eseguita solo se il SettingsTemplateCatalog è configurato. L'attività di **aggiornamento automatico del modello** esegue il file ApplySettingsCatalog.exe, che si trova nella directory di installazione dell'agente UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome attività</th>
<th align="left">Evento predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aggiornamento automatico di \Microsoft\UE-V\Template</p></td>
<td align="left"><p>Avvio del sistema e a 3:30 AM ogni giorno, in un momento casuale in una finestra di 1 ora</p></td>
</tr>
</tbody>
</table>

 

**Esempio:** Con il comando seguente viene configurato l'agente UE-V per controllare l'archivio di catalogo dei modelli di impostazioni ogni ora.

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

### Caricare i dati di analisi utilizzo software

L'attività di **dati upload analisi utilizzo software** viene eseguita durante l'installazione se l'utente o l'amministratore ha scelto di partecipare al programma Customer Experience Improvement Program (analisi utilizzo software). Questa attività carica i dati nei server analisi utilizzo software in cui vengono usati i dati per migliorare il prodotto per le versioni future di UE-V. Questa attività pianificata viene eseguita all'accesso e ogni 4 ore dopo. L'attività di **dati upload analisi utilizzo software** esegue il file UevSqmUploader.exe, che si trova nella directory di installazione dell'agente UE-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome attività</th>
<th align="left">Evento predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dati di \Microsoft\UE-V\Upload analisi utilizzo software</p></td>
<td align="left"><p>All'accesso e ogni 4 ore</p></td>
</tr>
</tbody>
</table>

 

## Dettagli delle attività pianificate UE-V 2


Il grafico seguente fornisce informazioni aggiuntive sulle attività pianificate per la versione UE-V 2:

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
<td align="left"><p><strong>Nome attività </strong> (nome file)</p></td>
<td align="left"><p><strong>Frequenza predefinita</strong></p></td>
<td align="left"><p><strong>Interruttore di alimentazione</strong></p></td>
<td align="left"><p><strong>Solo inattività</strong></p></td>
<td align="left"><p><strong>Connessione di rete</strong></p></td>
<td align="left"><p><strong>Descrizione</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Monitorare le impostazioni dell'applicazione </strong> (UevAppMonitor.exe)</p></td>
<td align="left"><p>Avvia 30 secondi dopo l'accesso e continua fino alla disconnessione.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Sincronizza le impostazioni per le app di Windows (AppX).</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Applicazione controller di sincronizzazione </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>All'accesso e ogni 30 minuti da allora in poi.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Solo se la rete è connessa</p></td>
<td align="left"><p>Avvia il controller di sincronizzazione che sincronizza le impostazioni locali con il percorso di archiviazione delle impostazioni.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Sincronizzare le impostazioni alla disconnessione </strong> (Microsoft.Uev.SyncController.exe)</p></td>
<td align="left"><p>Viene eseguito all'accesso e quindi attende la disconnessione per la sincronizzazione delle impostazioni.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Avviare un'applicazione all'accesso che controlla la sincronizzazione delle applicazioni a fine sessione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Aggiornamento automatico del modello </strong> (ApplySettingsCatalog.exe)</p></td>
<td align="left"><p>Viene eseguito all'accesso iniziale e alle 3:30 ogni giorno da allora in poi.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Controlla il catalogo del modello di impostazioni per i modelli nuovi, aggiornati o rimossi. Questa attività viene eseguita solo se è configurato SettingsTemplateCatalog.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Raccogliere dati di analisi utilizzo software </strong> (UevSqmSession.exe)</p></td>
<td align="left"><p>Al servizio avvia accesso</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>Se l'utente o l'amministratore opta per il programma Analisi utilizzo software (Customer Experience Improvement Program), questa attività raccoglie i dati che consentono di migliorare le versioni future di UE-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Caricare i dati di analisi utilizzo software </strong> (UevSqmUploader.exe)</p></td>
<td align="left"><p>Viene eseguito all'accesso e alle 4:00 ogni giorno da allora in poi.</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Solo se la rete è connessa</p></td>
<td align="left"><p>Se l'utente o l'amministratore opta per il programma Analisi utilizzo software (Customer Experience Improvement Program), questa attività carica i dati nei server di analisi utilizzo software.</p></td>
</tr>
</tbody>
</table>

 

**Legenda**

-   **Power Toggle** : l'utilità di pianificazione ottimizza il consumo di energia quando non viene collegata all'alimentazione CA. Se il computer passa all'alimentazione a batteria, l'attività potrebbe arrestarsi.

-   **Solo inattivo** : l'attività smetterà di funzionare se il computer cessa di essere inattivo. Per impostazione predefinita, l'attività non viene riavviata quando il computer è di nuovo inattivo. L'attività verrà invece riavviata nel trigger di attività successiva.

-   **Connessione di rete** : le attività contrassegnate come "Sì" vengono eseguite solo se il computer dispone di una connessione di rete disponibile. Le attività contrassegnate come "N/d" vengono eseguite indipendentemente dalla connettività di rete.

### Come gestire le attività pianificate

Per trovare le attività pianificate, eseguire le operazioni seguenti:

1.  Aprire "Pianifica attività" nel computer dell'utente.

2.  Passare a: utilità di pianificazione- &gt; raccolta utilità di pianificazione- &gt; Microsoft- &gt; UE-V

3.  Selezionare l'attività programmata che si vuole gestire e configurare nel riquadro dei dettagli.

### Altre informazioni

Le informazioni aggiuntive seguenti si applicano alle attività pianificate di UE-V:

-   i programmi di sequenza delle attività si trovano nella cartella di installazione dell'agente UE-V, `%programFiles%\Microsoft User Experience Virtualization\Agent\[architecture]\` per impostazione predefinita.

-   L'attività programmata del controller di sincronizzazione è il componente cruciale quando l'opzione UE-V SyncMethod è impostata su "SyncProvider" (configurazione predefinita di UE-V 2). Questa attività pianificata mantiene la sincronizzazione di SettingsSToragePath con le versioni localmente memorizzate nella cache dei file del pacchetto di impostazioni. Se gli utenti si lamentano che le impostazioni non vengono sincronizzate abbastanza spesso, è possibile ridurre l'impostazione di un'attività pianificata su un minimo di 1 minuto.Se necessario, è anche possibile aumentare i 30 minuti predefiniti per un importo superiore. Se gli utenti si lamentano che le impostazioni non vengono sincronizzate abbastanza velocemente per l'accesso, è possibile rimuovere l'impostazione di ritardo per l'attività pianificata. (È possibile trovare l'impostazione ritardo nella finestra di dialogo **Modifica trigger** )

-   Non è necessario disabilitare l'attività programmata di aggiornamento automatico del modello se si usa un altro metodo per sincronizzare i modelli dei client (ad esempio criteri di gruppo o previsioni di gestione configurazione). Se si esce dal valore della proprietà SettingsTemplateCatalog, viene impedito a UE-V di controllare il catalogo delle impostazioni per i modelli personalizzati. Questa attività pianificata viene eseguita ApplySettingsCatalog.exe e verrà essenzialmente restituita immediatamente.

-   L'attività programmata per le impostazioni dell'applicazione di monitoraggio aggiornerà le impostazioni di app di Windows (AppX) in tempo reale, in base ai trigger di impostazione di programmi app di Windows incorporati in ogni app.






## Argomenti correlati


[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#deploycatalogue)

 

 





