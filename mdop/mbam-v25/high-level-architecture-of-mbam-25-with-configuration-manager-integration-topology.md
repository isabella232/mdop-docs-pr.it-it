---
title: Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager
description: Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: 75af2e22981d76568916c36acadbbb25648b1f1d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825765"
---
# Architettura di alto livello di MBAM 2,5 con la topologia di integrazione di Configuration Manager

Questo argomento descrive l'architettura consigliata per la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia di integrazione di Configuration Manager. Questa topologia si integra con MBAM con System Center Configuration Manager. Per distribuire MBAM con la topologia autonoma, vedere [architettura di alto livello di MBAM 2,5 con topologia](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)autonoma.

Per un elenco delle versioni supportate del software menzionato in questo argomento, Vedi le [configurazioni supportate di MBAM 2,5](mbam-25-supported-configurations.md).

**Importante**  Windows to go non è supportato per l'installazione della topologia di integrazione di Configuration Manager quando si usa Configuration Manager 2007.

 

## Numero consigliato di server e numero di client supportati


Il numero consigliato di server e il numero di client supportati in un ambiente di produzione sono i seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architettura consigliata</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Numero di server e altri computer</p></td>
<td align="left"><p>Tre server</p>
<p>Una workstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Numero di computer client supportati</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Differenze tra l'integrazione di Configuration Manager e le topologie autonome


Le principali differenze tra le topologie sono:

-   Le funzionalità di conformità e creazione di report vengono rimosse da MBAM e si accede da Configuration Manager.

-   I report vengono visualizzati dalla console di gestione di Configuration Manager, ad eccezione del report di controllo del ripristino, che si continua a visualizzare dal sito Web di amministrazione e monitoraggio di MBAM.

## Consigliabile MBAM architettura di alto livello con la topologia di integrazione di Configuration Manager


Il diagramma e la tabella seguenti descrivono l'architettura di alto livello consigliata per MBAM con la topologia di integrazione di Configuration Manager. Le distribuzioni di MBAM multi-Forest richiedono un trust unidirezionale o bidirezionale. I trust unidirezionali richiedono che il dominio del server si fidi del dominio client.

![mbam2\-5](images/mbam2-5-cmserver.png)

### Server di database

#### Database di ripristino

Questa funzionalità è configurata in un computer con Windows Server e in un'istanza di SQL Server supportata.

Il **database di ripristino** archivia i dati di recupero raccolti dai computer client di mbam.

#### Database di controllo

Questa funzionalità è configurata in un computer con Windows Server e in un'istanza di SQL Server supportata.

Il **database di controllo** archivia i dati delle attività di controllo raccolti da computer client che hanno eseguito l'accesso ai dati di ripristino.

#### Rapporti

Questa funzionalità è configurata in un computer con Windows Server e in un'istanza di SQL Server supportata.

I **report** includono dati di controllo del ripristino per i computer client dell'organizzazione. È possibile visualizzare i report dalla console di Configuration Manager o direttamente da SQL Server Reporting Services.

### Server del sito primario di Configuration Manager

Funzionalità di integrazione di System Center Configuration Manager

-   Questa caratteristica è configurata nel server del sito primario di Configuration Manager, che è il server di livello superiore nell'infrastruttura di gestione configurazione.

-   Il **Server Configuration Manager** raccoglie le informazioni sull'inventario hardware dai computer client e viene usato per segnalare la conformità di BitLocker dei computer client.

-   Quando si esegue la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker per installare il software server, la raccolta di computer supportati MBAM, la previsione di configurazione e i report vengono configurati nel server del sito primario di Configuration Manager.

-   La **console di Configuration Manager** deve essere installata nello stesso computer in cui si installa il software del server mbam.

### Server di amministrazione e monitoraggio

#### Sito Web di amministrazione e monitoraggio

Questa caratteristica è configurata in un computer che gestisce Windows Server.

Il **sito Web di amministrazione e monitoraggio** viene usato per:

-   Aiutare gli utenti finali a recuperare l'accesso ai propri computer quando sono bloccati. (L'area del sito Web viene comunemente chiamata Help desk).

-   Visualizzare il report di controllo del ripristino, che mostra l'attività di ripristino per i computer client. Altri report vengono visualizzati dalla console di Configuration Manager.

#### Portale self-service

Questa caratteristica è configurata in un computer che gestisce Windows Server.

Il **portale self-service** è un sito Web che consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.

#### Monitoraggio dei servizi Web per questo sito Web

Questa funzionalità è installata in un computer che gestisce Windows Server.

I **servizi Web di monitoraggio** vengono usati dal client mbam e dai siti Web per comunicare con il database.

**Importante**<br>Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 dato che i siti Web di MBAM comunicano direttamente con il database di ripristino. 

 

### Workstation di gestione

#### Modelli di criteri di gruppo di MBAM

-   I **modelli dei criteri di gruppo di mbam** sono impostazioni di criteri di gruppo che definiscono le impostazioni di implementazione per mbam, che consentono di gestire la crittografia unità BitLocker.

-   Prima di eseguire MBAM, è necessario scaricare i modelli di criteri di gruppo da [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation che esegue un sistema operativo Windows Server o Windows supportato.

    **NOTA**<br>La workstation non deve essere un computer dedicato.

     

### Client MBAM e computer client di Configuration Manager

#### Software client MBAM

Il **client mbam**:

-   USA gli oggetti Criteri di gruppo per applicare la crittografia unità BitLocker nei computer client dell'organizzazione.

-   Raccoglie la chiave di ripristino di BitLocker per tre tipi di unità dati: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

-   Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.

#### Client di Gestione configurazione

Il **client Configuration Manager** consente a Gestione configurazione di raccogliere i dati di compatibilità hardware relativi ai computer client e di segnalare le informazioni sulla conformità.

 

## Differenze nella distribuzione di MBAM per le versioni supportate di Configuration Manager


Quando si distribuisce MBAM con la topologia di integrazione di Configuration Manager, è possibile installare MBAM in un server del sito principale. Tuttavia, l'installazione di MBAM funziona in modo diverso per System Center2012 Configuration Manager e Configuration Manager2007.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di Configuration Manager</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>System Center2012 R2 Configuration Manager</p>
<p>Gestione configurazione di sistema Center2012</p></td>
<td align="left"><p>Se si installa MBAM in un server del sito principale o in un server di amministrazione centrale, MBAM esegue tutte le operazioni di installazione nel server del sito.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurazione Manager2007 R2</p>
<p>Configurazione Manager2007</p></td>
<td align="left"><p>Se si installa MBAM in un server del sito principale che fa parte di una gerarchia di gestione configurazione più grande con un server padre del sito centrale, MBAM identifica il server padre del sito centrale ed esegue tutte le azioni di installazione nel server padre. L'installazione include il controllo dei prerequisiti e l'installazione di oggetti e report di Configuration Manager.</p>
<p>Ad esempio, se si installa MBAM in un server del sito principale che è un elemento figlio di un server padre del sito centrale, MBAM installa tutti gli oggetti e i report di Configuration Manager nel server padre. Se si installa MBAM nel server padre, MBAM esegue tutte le operazioni di installazione in tale server padre.</p></td>
</tr>
</tbody>
</table>

 

## Funzionamento di MBAM con Configuration Manager


L'integrazione di MBAM con Configuration Manager si basa su un pacchetto di configurazione che installa gli elementi descritti nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elementi installati in Configuration Manager</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dati di configurazione</p></td>
<td align="left"><p>I dati di configurazione installano una previsione di configurazione, denominata "protezione BitLocker", che contiene due elementi di configurazione:</p>
<ul>
<li><p>Protezione unità sistema operativo BitLocker</p></li>
<li><p>Protezione delle unità dati fisse di BitLocker</p></li>
</ul>
<p>La linea di base della configurazione viene distribuita nella raccolta di computer supportati MBAM, che viene creata anche quando MBAM è installato.</p>
<p>I due elementi di configurazione costituiscono la base per valutare lo stato di conformità dei computer client. Queste informazioni vengono acquisite, archiviate e valutate in Gestione configurazione.</p>
<p>Gli elementi di configurazione si basano sui requisiti di conformità per le unità del sistema operativo e le unità dati fisse. I dettagli necessari per i computer distribuiti vengono raccolti in modo da poter valutare la conformità per tali tipi di unità.</p>
<p>Per impostazione predefinita, la linea di base della configurazione valuta lo stato di conformità every12 ore e invia i dati di conformità a Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Raccolta di computer supportati MBAM</p></td>
<td align="left"><p>MBAM crea una raccolta che si chiama MBAM computer supportati. La linea di base della configurazione è destinata ai computer client inclusi in questa raccolta.</p>
<p>Si tratta di una raccolta dinamica. Per impostazione predefinita, esegue every12 ore e valuta l'appartenenza, in base a tre criteri:</p>
<ul>
<li><p>Il computer è una versione supportata del sistema operativo Windows.</p></li>
<li><p>Il computer è un computer fisico. Le macchine virtuali non sono supportate.</p></li>
<li><p>Il computer ha un modulo TPM (Trusted Platform Module) disponibile. Per Windows7 è necessaria una versione compatibile del TPM 1.2 o versione successiva. Windows10, Windows 8.1, Windows8 e Windows to go non richiedono un TPM.</p></li>
</ul>
<p>La raccolta viene valutata in tutti i computer e viene creato un sottoinsieme di computer compatibili, che fornisce la base per la valutazione della conformità e la creazione di report per l'integrazione con MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rapporti</p></td>
<td align="left"><p>Quando si configura MBAM con la topologia di integrazione di Configuration Manager, è possibile visualizzare tutti i report di Configuration Manager, eccetto il report di controllo di ripristino, il secondo dei quali si continua a visualizzare nel sito Web di amministrazione e monitoraggio di MBAM. I report disponibili in Gestione configurazione sono i seguenti:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Rapporto</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dashboard di conformità di BitLocker Enterprise</p></td>
<td align="left"><p>Assegna agli amministratori IT tre visualizzazioni delle informazioni in un singolo report: distribuzione dello stato di conformità, distribuzione degli errori non conforme e distribuzione dello stato di conformità per tipo di unità. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli di conformità di BitLocker Enterprise</p></td>
<td align="left"><p>Consente agli amministratori IT di visualizzare informazioni sullo stato di conformità della crittografia BitLocker dell'organizzazione e include lo stato di conformità per ogni computer. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformità al computer BitLocker</p></td>
<td align="left"><p>Consente agli amministratori IT di visualizzare un singolo computer e determinare il motivo per cui è stato segnalato con uno stato conforme o non conforme. Il report visualizza anche lo stato di crittografia delle unità del sistema operativo e delle unità dati fisse.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Riepilogo conformità di BitLocker Enterprise</p></td>
<td align="left"><p>Consente agli amministratori IT di visualizzare lo stato della conformità ai criteri di MBAM nell'organizzazione. Lo stato di ogni computer viene valutato e il report Mostra un riepilogo della conformità di tutti i computer dell'organizzazione rispetto al criterio. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## Argomenti correlati


[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

[Architettura di alto livello di MBAM 2.5 con topologia autonoma](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Funzionalità illustrate di una distribuzione di MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




