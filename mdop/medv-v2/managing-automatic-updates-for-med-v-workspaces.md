---
title: Gestione degli aggiornamenti automatici per le aree di lavoro MED-V
description: Gestione degli aggiornamenti automatici per le aree di lavoro MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825295"
---
# Gestione degli aggiornamenti automatici per le aree di lavoro MED-V


L'area di lavoro MED-V è una macchina virtuale che contiene un sistema operativo distinto, il cui processo di aggiornamento automatico del software deve essere gestito proprio come i computer fisici dell'organizzazione. Poiché il sistema operativo guest non è sempre necessariamente in uso quando il sistema operativo ospitante è in funzione, è necessario assicurarsi che la macchina virtuale MED-V sia configurata in modo che gli aggiornamenti software possano essere applicati al sistema operativo guest in base alle esigenze. La soluzione Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 offre la funzionalità che consente di determinare il modo in cui vengono elaborati gli aggiornamenti software automatici in un'area di lavoro MED-V.

## Gestione dei criteri di riattivazione dell'area di lavoro MED-V


Il criterio di riattivazione dell'area di lavoro MED-V garantisce che la macchina virtuale MED-V sia resa disponibile per gli aggiornamenti per l'ora specificata nelle impostazioni di configurazione di MED-V. Questo vale per entrambi gli aggiornamenti pubblicati da Microsoft tramite Windows Update e gli aggiornamenti distribuiti e controllati da soluzioni non Microsoft, come le applicazioni antivirus.

**Importante**  I criteri di riattivazione dell'area di lavoro MED-V sono ottimizzati per l'infrastruttura Microsoft Update. Se si usa Microsoft System Center Configuration Manager per distribuire gli aggiornamenti non Microsoft, è consigliabile usare anche System Center Updates Publisher, che sfrutta la stessa infrastruttura di Microsoft Update e quindi beneficia dei criteri di riattivazione dell'area di lavoro MED-V. Per altre informazioni, vedere [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .

 

Quando è stato creato il pacchetto dell'area di lavoro MED-V, è stato configurato quando e come viene avviato, quando l'utente finale accede (**avvio veloce**) o quando l'utente finale apre per la prima volta un'applicazione pubblicata (**inizio normale**). Oppure imposta l'opzione per consentire all'utente finale di controllare questa impostazione.

In entrambi i casi, ogni volta che viene selezionata l'opzione **avvio veloce** , la macchina virtuale continua a essere eseguita purché l'host MED-V sia connesso come utente. In questa configurazione, poiché MED-V è attivo quando l'host è attivo, gli aggiornamenti automatici vengono applicati senza richiedere ulteriori elaborazioni da MED-V.

Tuttavia, per i casi in cui l' **avvio veloce** non viene specificato o la macchina virtuale viene sospesa o arrestata, Med-v garantisce attraverso i criteri di riattivazione dell'area di lavoro MED-v che il sistema operativo guest viene aggiornato regolarmente anche quando MED-V non viene usato regolarmente. MED-V esegue questa funzione regolarmente riattivando la macchina virtuale in base alle impostazioni di configurazione specificate. In questo modo i client di aggiornamento automatico della macchina virtuale verranno eseguiti in base alle loro configurazioni.Una volta trascorso il periodo di tempo definito dall'impostazione di configurazione di MED-V, MED-V restituirà la macchina virtuale allo stato precedente.

**Nota**  Se l'utente finale apre un'applicazione pubblicata durante il periodo di aggiornamento, gli aggiornamenti richiesti vengono applicati, ma MED-V non viene automaticamente ibernato o arrestato al termine del periodo di aggiornamento. Invece, MED-V continua a essere eseguito.

 

I criteri di riattivazione dell'area di lavoro MED-V includono tre componenti principali:

**Guest Update Manager**

Questo programma eseguibile autonomo che risiede nell'host MED-V è responsabile del risveglio della macchina virtuale in base a una pianificazione predefinita configurabile. Specificare le impostazioni di configurazione per indicare a che ora la macchina virtuale deve essere riattivata ogni giorno dall'Update Manager e per quanto tempo la macchina virtuale deve essere mantenuta (in minuti) per consentire l'applicazione degli aggiornamenti. Dopo che è stato raggiunto il numero di minuti specificati, la gestione aggiornamento Guest inserisce la macchina virtuale in ibernazione, preparata per l'uso successivo. Puoi programmare l'esecuzione di questo programma eseguibile tramite Windows Task Manager.

**Servizio di gestione riavvio Guest**

Questo servizio, che risiede nell'host MED-V, ha tre responsabilità principali. Insieme a Guest Update Manager, gestisce il riavvio della macchina virtuale all'accesso dell'utente, se necessario. Viene rilevato quando i riavvii della macchina virtuale sono necessari causati dagli aggiornamenti installati. E assicura che l'attività di gestione aggiornamento Guest sia sempre pianificata in base alla configurazione.

**Servizio di aggiornamento Guest**

Questo servizio Windows, che risiede nella macchina virtuale MED-V, è responsabile del monitoraggio quando gli aggiornamenti installati richiedono un riavvio. Dopo che il servizio viene a conoscenza della necessità di un riavvio, informa il servizio di gestione riavvio guest nell'host.

### Impostazioni di configurazione per i criteri di riattivazione dell'area di lavoro MED-V

Puoi controllare quando e per quanto tempo la macchina virtuale si risveglia per ricevere gli aggiornamenti automatici definendo i due valori di configurazione seguenti nel registro di sistema. Entrambi questi valori si trovano sotto la chiave HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.

**GuestUpdateTime** -configura l'ora e il minuto ogni giorno quando MED-V deve riattivare la macchina virtuale per l'aggiornamento, in base allo standard di 24 ore. Specificare l'ora nel formato HH: MM. Il valore predefinito è 00:00 (mezzanotte).

**GuestUpdateDuration** -configura il numero di minuti in cui MED-V deve conservare la macchina virtuale per l'aggiornamento, a partire dall'ora specificata nell'impostazione di configurazione di GuestUpdateTime. Il valore predefinito è 240 (4 ore). Impostando questo valore su zero (0) viene disabilitato il criterio di riattivazione dell'area di lavoro MED-V.

Per altre informazioni su come definire i valori di configurazione di MED-V, vedere [gestione delle impostazioni di configurazione dell'area di lavoro MED-v](managing-med-v-workspace-configuration-settings.md).

**Nota**  Una procedura consigliata per MED-V consiste nell'impostare l'intervallo di riattivazione in modo che corrisponda al momento in cui le macchine virtuali MED-V sono pianificate per l'aggiornamento periodico. Inoltre, ti consigliamo di configurare queste impostazioni per assomigliare al comportamento del computer host.

 

### Riavviare la notifica tramite il sistema ESD

Puoi configurare il sistema ESD per notificare a MED-V ogni volta che è necessario un riavvio per l'area di lavoro MED-V dopo l'applicazione degli aggiornamenti automatici. Quando si applicano aggiornamenti automatici tramite il sistema ESD che si sa che richiedono un riavvio, è necessario scrivere uno script per segnalare l'evento globale seguente nell'area di lavoro MED-V:

**Importante**  Per aprire l'evento è necessario modificare solo i diritti e quindi segnalarlo. Se non si apre con le autorizzazioni corrette, non funziona.

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

Quando segnali questo evento, MED-V la acquisisce e informa la macchina virtuale che è necessario riavviare il computer.

## Argomenti correlati


[Gestione degli aggiornamenti software per le aree di lavoro MED-V](managing-software-updates-for-med-v-workspaces.md)

 

 





