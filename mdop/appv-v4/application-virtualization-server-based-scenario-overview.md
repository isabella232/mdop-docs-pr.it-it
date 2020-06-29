---
title: Panoramica di uno scenario basato su Application Virtualization Server
description: Panoramica di uno scenario basato su Application Virtualization Server
author: dansimp
ms.assetid: 2d91392b-5085-4a5d-94f2-15eed1ed2928
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b3ac3f10a5b7c7705e6d72c122d52be801a6d50
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822095"
---
# Panoramica di uno scenario basato su Application Virtualization Server


Se si prevede di usare uno scenario di distribuzione basato su server per l'ambiente di virtualizzazione delle applicazioni Microsoft, è importante comprendere le differenze tra *Application Virtualization Management Server* e *Application Virtualization Streaming Server*. In questo argomento vengono illustrate le differenze e vengono fornite anche informazioni sui metodi di recapito dei pacchetti, sui protocolli di trasmissione e sui componenti esterni che è necessario considerare mentre si procede alla distribuzione.

## Application Virtualization Management Server


L'Application Virtualization Management Server esegue sia la funzione Publishing che la funzione streaming. Il server pubblica le icone delle applicazioni, i collegamenti e le associazioni di tipi di file nei client App-V per gli utenti autorizzati. Quando vengono ricevute richieste utente per le applicazioni, il server trasmette i dati su richiesta agli utenti autorizzati usando i protocolli RTSP o RTSPs. Nella maggior parte delle configurazioni che usano questo server, uno o più server di gestione condividono un archivio dati comune per le informazioni di configurazione e pacchetto.

I server di gestione della virtualizzazione delle applicazioni usano i gruppi di Active Directory per gestire l'autorizzazione degli utenti. Oltre ai servizi di dominio Active Directory, questi server hanno installato SQL Server per la gestione del database e dell'archivio dati. Il server di gestione viene controllato tramite Application Virtualization Management Console, uno snap-in di Microsoft Management Console.

Dato che le applicazioni di flusso di Application Virtualization Management Server vengono trasmesse agli utenti finali su richiesta, questi server sono ideali per le configurazioni di sistema con LAN affidabili e a larghezza di banda elevata.

## Application Virtualization Streaming Server


Application Virtualization Streaming Server offre le stesse funzionalità di aggiornamento di flusso e pacchetto fornite dal server di gestione, ma senza i requisiti di Active Directory o SQL Server. Tuttavia, il server di flusso non dispone di un servizio di pubblicazione, né offre licenze o funzionalità di misurazione. Il servizio di pubblicazione di un server di gestione di App-V distinto viene usato in combinazione con App-V Streaming Server. App-V streaming server risponde alle esigenze delle aziende che vogliono usare la virtualizzazione delle applicazioni in più posizioni con le funzionalità di flusso della configurazione classica del server, ma potrebbero non avere l'infrastruttura per supportare i server di gestione di App-V in ogni posizione.

L'Application Virtualization Streaming Server può essere usato anche in ambienti con un sistema ESD (Electronic Software Distribution System) esistente. Si usa l'ESD per gestire le applicazioni di flusso. Diversamente dall'Application Virtualization Management Server, il server di streaming non usa SQL o una console di gestione. Questi server usano gli elenchi di controllo di accesso (ACL) per concedere l'autorizzazione dell'utente.

## Metodi di distribuzione del pacchetto


Se si prevede di usare un Application Virtualization Server come metodo di recapito della pubblicazione, è necessario determinare quale dei seguenti metodi di recapito del pacchetto si applica allo scenario:

-   *Recapito dinamico del pacchetto*

-   *Caricamento da un pacchetto di file*

### Recapito dinamico del pacchetto

Durante il recapito dinamico del pacchetto, il server (Application Virtualization Management Server, Application Virtualization Streaming Server o IIS Server) offre le applicazioni virtualizzate agli utenti finali tramite la distribuzione su richiesta. Il server recapita le applicazioni e i pacchetti virtualizzati a un computer client solo quando un utente tenta prima di avviare un'applicazione (su richiesta). Il server trasmette solo i blocchi necessari per avviare l'applicazione (blocco di funzionalità principale). Dopo che il blocco di funzionalità principale viene recapitato al client, l'applicazione viene eseguita; il client non riceve l'applicazione completa (distribuzione incrementale), a meno che il client non abbia bisogno di accedere a una parte dell'applicazione non inclusa nel blocco di funzionalità principale. In questo caso, il client esegue una richiesta fuori sequenza e il blocco di funzionalità secondario viene trasmesso al client. Il recapito dinamico del pacchetto consente l'avvio rapido dell'applicazione.

### Caricamento da un pacchetto di file

Per il caricamento da un pacchetto di file, il server recapita l'intero pacchetto di applicazioni virtualizzate a un computer client prima che l'utente avvii l'applicazione. In questo scenario, le applicazioni virtualizzate vengono recapitate come pacchetto completo, anziché tramite il metodo dinamico incrementale usato dal modello di recapito dinamico.

**Nota**  Per ogni metodo di recapito, il processo di recapito dell'applicazione virtuale iniziale e il processo di aggiornamento delle applicazioni virtuali sono gli stessi. il pacchetto di applicazione virtuale aggiornato sostituisce il pacchetto di applicazione originale.

 

Nella tabella seguente vengono confrontati i vantaggi e gli svantaggi di ogni metodo di recapito del pacchetto.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Vantaggi</th>
<th align="left">Svantaggi</th>
<th align="left">Commenti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Recapito dinamico del pacchetto</p></td>
<td align="left"><p>Le applicazioni vengono recapitate e aggiornate su richiesta.</p>
<p>Le applicazioni vengono recapitate e aggiornate in modo incrementale per ottimizzare il tempo di avvio.</p>
<p>Gli aggiornamenti vengono recapitati automaticamente al desktop client.</p></td>
<td align="left"><p>Maggiore ingombro nella topologia aziendale a causa dei requisiti del server.</p>
<p>Lo streaming delle applicazioni deve essere su una LAN; gli scenari di distribuzione su una rete WAN o che usano una connessione non affidabile o intermittente tra il server e il client potrebbero essere inutilizzabili.</p></td>
<td align="left"><p>Richiede un'infrastruttura di flusso.</p>
<p>Windows Installer usato per distribuire il software client Desktop Application Virtualization per i computer degli utenti finali.</p>
<p>Le grandi aziende dovrebbero usare i server di streaming Application Virtualization come punti di distribuzione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Caricamento da un pacchetto di file</p></td>
<td align="left"><p>Coerenti con le tipiche procedure di gestione aziendale.</p>
<p>Supporta lo scenario di configurazione autonomo.</p>
<p>Fornisce una soluzione a un problema di micro-filiale aziendale.</p></td>
<td align="left"><p>Il recapito e l'aggiornamento delle applicazioni non sono possibili su richiesta.</p>
<p>Il recapito e l'aggiornamento delle applicazioni non sono incrementali. aumenta il consumo di risorse rispetto al recapito dinamico.</p></td>
<td align="left"><p>L'organizzazione IT è spesso responsabile della gestione delle licenze dell'applicazione, dell'autorizzazione dell'utente e dell'autenticazione.</p></td>
</tr>
</tbody>
</table>

 

## Protocolli e componenti esterni correlati al server


La tabella seguente elenca i tipi di server che possono essere usati in uno scenario basato su Application Virtualization Server, insieme ai relativi protocolli di trasmissione e ai componenti esterni necessari per supportare la configurazione specifica del server. La tabella include anche il meccanismo di creazione di report e il meccanismo di aggiornamento attivo per ogni tipo di server. Poiché questi scenari usano tutti il server di gestione della virtualizzazione dell'applicazione, è possibile usare le funzionalità di creazione di report interne integrate nel sistema. Se si usa una Application Virtualization Management o un Application Virtualization Streaming Server per consegnare i pacchetti al client, i pacchetti sul server vengono aggiornati automaticamente quando un utente accede al client; Se si usano server IIS o un file per consegnare i pacchetti al client, i pacchetti nel client devono essere aggiornati manualmente.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di server</th>
<th align="left">Protocolli</th>
<th align="left">Componenti esterni necessari</th>
<th align="left">Creazione di rapporti</th>
<th align="left">Aggiornamento attivo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Application Virtualization Management Server</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPS</p></td>
<td align="left"><p>Quando si usa HTTPS, usare un server IIS per scaricare i file ICO e OSD e un firewall per proteggere il server dall'esposizione a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Application Virtualization Streaming Server</p></td>
<td align="left"><p>RTSP</p>
<p>RTSPS</p></td>
<td align="left"><p>Usare un meccanismo per sincronizzare il contenuto tra il server di gestione e il server di flusso. Quando si usa HTTPS, usare un server IIS per scaricare i file ICO e OSD e usare un firewall per proteggere il server dall'esposizione a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Supportato</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Server IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Usare un meccanismo per sincronizzare il contenuto tra il server di gestione e il server di flusso. Quando si usa HTTP o HTTPS, usare un server IIS per scaricare i file ICO e OSD e un firewall per proteggere il server dall'esposizione a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Non supportato</p></td>
</tr>
<tr class="even">
<td align="left"><p>File</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>È necessario un modo per sincronizzare il contenuto tra il server di gestione e il server di flusso. È necessario un computer client con funzionalità di condivisione file o flusso.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"><p>Non supportato</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Come configurare i server per la distribuzione basata su server](how-to-configure-servers-for-server-based-deployment.md)

[Come installare i server e i componenti del sistema](how-to-install-the-servers-and-system-components.md)

 

 





