---
title: Visualizzazione dei report di MBAM 2.5 per la topologia di integrazione di Configuration Manager
description: Visualizzazione dei report di MBAM 2.5 per la topologia di integrazione di Configuration Manager
author: dansimp
ms.assetid: 60d11b2f-3a76-4023-8da4-f89e9f35b790
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3384fee62d302ac47775fe106265456ef119ab47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824045"
---
# Visualizzazione dei report di MBAM 2.5 per la topologia di integrazione di Configuration Manager


Questo argomento descrive i report disponibili quando si configura Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia di integrazione di Configuration Manager. I report mostrano la conformità di BitLocker per l'organizzazione e per i singoli computer e dispositivi gestiti da MBAM. I report contengono informazioni tabulari e grafici e contengono filtri che consentono di visualizzare i dati da prospettive diverse.

Nella topologia di integrazione di Configuration Manager è possibile visualizzare i report di Configuration Manager invece che dal sito Web di amministrazione e monitoraggio, ad eccezione del **report di controllo del ripristino**, che si continua a visualizzare dal sito Web di amministrazione e monitoraggio.

Per informazioni sui report MBAM per la topologia autonoma, vedere [visualizzazione di report di mbam 2,5 per la topologia](viewing-mbam-25-reports-for-the-stand-alone-topology.md)autonoma.

## Accesso ai report in Configuration Manager


Per accedere alla funzionalità report in Configuration Manager:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di Configuration Manager</th>
<th align="left">Come visualizzare i report</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ConfigurationManager di SystemCenter2012</p></td>
<td align="left"><ol>
<li><p>Nel riquadro sinistro selezionare l'area di <strong> </strong> lavoro monitoraggio.</p></li>
<li><p>Nell'albero, espandere <strong> Panoramica </strong> &gt; <strong> </strong> &gt; <strong> report </strong> &gt; <strong> mbam </strong> .</p></li>
<li><p>Selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro destro.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007</p></td>
<td align="left"><ol>
<li><p>Nel riquadro sinistro espandere <strong> Gestione computer </strong> &gt; <strong> Reporting </strong> &gt; <strong> Services </strong> &gt; <strong> &lt; report nome server &gt; </strong> &gt; <strong> cartella </strong> &gt; <strong> mbam </strong> .</p></li>
<li><p>Selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro destro.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## Descrizione dei report in Configuration Manager


Esistono alcune differenze minime nei report per la topologia di integrazione di Configuration Manager e per la topologia autonoma. Nelle sezioni seguenti vengono descritti i dati nei report di MBAM per la topologia di integrazione di Configuration Manager:

-   [Dashboard di conformità di BitLocker Enterprise](#bkmk-dashboard)

-   [Dettagli di conformità di BitLocker Enterprise](#bkmk-compliancedetails)

-   [Riepilogo conformità di BitLocker Enterprise](#bkmk-compliancesummary)

-   [Report conformità computer BitLocker](#bkmk-compliancereport)

### <a href="" id="bkmk-dashboard"></a>Dashboard di conformità di BitLocker Enterprise

Il dashboard conformità Enterprise di BitLocker offre i grafici seguenti, che mostrano lo stato di conformità di BitLocker nell'organizzazione:

-   Distribuzione dello stato di conformità

-   Distribuzione di errori non conformi

-   Distribuzione dello stato di conformità per tipo di unità

**Distribuzione dello stato di conformità**

Questo grafico a torta mostra lo stato di conformità per i computer all'interno dell'organizzazione. Viene inoltre visualizzata la percentuale di computer, in confronto al numero totale di computer della raccolta selezionata, con lo stato di conformità. Viene visualizzato anche il numero effettivo di computer con ogni stato. Il grafico a torta Mostra gli Stati di conformità seguenti:

-   Conformi

-   Non conforme

-   Esenzione dall'utente

-   Esenzione dall'utente temporaneo

-   Criteri non applicati

-   Sconosciuto. Questo computer ha segnalato un errore di stato o fa parte della raccolta, ma non ha mai segnalato lo stato di conformità. Se il computer è disconnesso dall'organizzazione, potrebbe verificarsi la mancanza di uno stato di conformità.

**Distribuzione di errori non conformi**

Questo grafico a torta mostra le categorie di computer dell'organizzazione che non sono conformi ai criteri di crittografia unità BitLocker e Mostra il numero di computer in ogni categoria. Ogni percentuale di categoria viene calcolata a partire dal numero totale di computer non conformi della raccolta.

-   Crittografia rimandata dall'utente

-   Non è possibile trovare TPM compatibile

-   Partizione di sistema non disponibile o abbastanza grande

-   Conflitto di criteri

-   Attesa del provisioning automatico del TPM

-   Si è verificato un errore sconosciuto

-   Nessuna informazione. Questi computer non hanno installato il client MBAM, o hanno installato il client MBAM, ma non attivato (ad esempio, il servizio non funziona).

**Distribuzione dello stato di conformità per tipo di unità**

Questo grafico a barre Mostra lo stato di conformità corrente di BitLocker per tipo di unità. Gli Stati sono **conformi** e **non conformi**. Le barre vengono visualizzate per le unità dati fisse e le unità del sistema operativo. I computer che non dispongono di un'unità dati fissa sono inclusi e visualizzano un valore solo nella barra dell' **unità del sistema operativo** . Il grafico non include gli utenti a cui è stata concessa un'esenzione dal criterio di crittografia unità BitLocker o dalla categoria nessun criterio.

### <a href="" id="bkmk-compliancedetails"></a>Dettagli di conformità di BitLocker Enterprise

Questo report Mostra le informazioni sulla conformità complessiva di BitLocker nell'organizzazione per la raccolta di computer mirati per l'uso di BitLocker.

**Campi dettagli conformità Enterprise di BitLocker**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome colonna</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computer gestiti</p></td>
<td align="left"><p>Numero di computer gestiti da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conforme%</p></td>
<td align="left"><p>Percentuale di computer conformi nell'organizzazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Non conforme</p></td>
<td align="left"><p>Percentuale di computer non conformi nell'organizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Conformità sconosciuta</p></td>
<td align="left"><p>Percentuale di computer con uno stato di conformità non noto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Esenti</p></td>
<td align="left"><p>Percentuale di computer esenti dal requisito di crittografia di BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Non esenti</p></td>
<td align="left"><p>Percentuale di computer non esenti dal requisito di crittografia BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Percentuale di computer conformi nell'organizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Percentuale di computer non conformi nell'organizzazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformità sconosciuta</p></td>
<td align="left"><p>Percentuale di computer con uno stato di conformità non noto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esenti</p></td>
<td align="left"><p>Totale computer esenti dal requisito di crittografia BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non esenti</p></td>
<td align="left"><p>Totale computer non esenti dal requisito di crittografia di BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Stati dei dettagli di conformità Enterprise di BitLocker**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Stato conformità</th>
<th align="left">Esenzione</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Non esenti</p></td>
<td align="left"><p>Il computer non è conforme, in base ai criteri specificati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Non esenti</p></td>
<td align="left"><p>Il computer è conforme ai criteri specificati.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancesummary"></a>Riepilogo conformità di BitLocker Enterprise

Usare questo tipo di report per visualizzare informazioni sulla conformità complessiva di BitLocker nell'organizzazione e per mostrare la conformità per i singoli computer presenti nella raccolta di computer destinati all'uso di BitLocker.

**Campi di riepilogo conformità Enterprise di BitLocker**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome colonna</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Computer gestiti</p></td>
<td align="left"><p>Numero di computer gestiti da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conforme%</p></td>
<td align="left"><p>Percentuale di computer conformi nell'organizzazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Non conforme</p></td>
<td align="left"><p>Percentuale di computer non conformi nell'organizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Conformità sconosciuta</p></td>
<td align="left"><p>Percentuale di computer con uno stato di conformità non noto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Esenti</p></td>
<td align="left"><p>Percentuale di computer esenti dal requisito di crittografia di BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Non esenti</p></td>
<td align="left"><p>Percentuale di computer non esenti dal requisito di crittografia BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Percentuale di computer conformi nell'organizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Percentuale di computer non conformi nell'organizzazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformità sconosciuta</p></td>
<td align="left"><p>Percentuale di computer con uno stato di conformità non noto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esenti</p></td>
<td align="left"><p>Totale computer esenti dal requisito di crittografia BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non esenti</p></td>
<td align="left"><p>Totale computer non esenti dal requisito di crittografia di BitLocker.</p></td>
</tr>
</tbody>
</table>

 

**Dettagli del computer di riepilogo conformità di BitLocker Enterprise**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome colonna</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome computer</p></td>
<td align="left"><p>Nome computer DNS specificato dall'utente gestito da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome di dominio</p></td>
<td align="left"><p>Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Stato complessivo di conformità del computer gestito da MBAM. Gli stati validi sono conformi e conformi. Si noti che lo stato di conformità per unità (Vedi la tabella seguente) può indicare stati di conformità diversi. Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Stato che indica se l'utente è esonerato o non è esentato dai criteri di BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di dispositivi</p></td>
<td align="left"><p>Utente del dispositivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato relativi allo stato di conformità del computer in conformità con i criteri specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ultimo contatto</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. La frequenza dei contatti può essere configurata tramite le impostazioni dei criteri di gruppo.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-compliancereport"></a>Report conformità computer BitLocker

Usare questo tipo di report per raccogliere informazioni specifiche di un computer. Il report conformità computer BitLocker fornisce informazioni dettagliate sulla crittografia di ogni unità in un computer (sistema operativo e unità dati fisse). Fornisce anche un'indicazione dei criteri applicati a ogni tipo di unità nel computer. Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.

**Nota**  Lo stato di crittografia dei volumi di dati rimovibili non viene visualizzato nel report.

 

**Report conformità computer BitLocker: campi dettagli computer**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome colonna</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome computer</p></td>
<td align="left"><p>Nome computer DNS specificato dall'utente gestito da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome di dominio</p></td>
<td align="left"><p>Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di computer</p></td>
<td align="left"><p>Tipo di computer. I tipi validi non sono portatili e portatili.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operativo</p></td>
<td align="left"><p>Tipo di sistema operativo disponibile nel computer client di MBAM Managed.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformità complessiva</p></td>
<td align="left"><p>Stato complessivo di conformità del computer gestito da MBAM. Gli stati validi sono conformi e conformi. Si noti che lo stato di conformità per unità (Vedi la tabella seguente) può indicare stati di conformità diversi. Tuttavia, questo campo rappresenta lo stato di conformità in base ai criteri specificati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformità del sistema operativo</p></td>
<td align="left"><p>Stato di conformità del sistema operativo gestito da MBAM. Gli stati validi sono conformi e conformi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformità con l'unità dati fissa</p></td>
<td align="left"><p>Stato di conformità dell'unità dati fissa gestita da MBAM. Gli stati validi sono conformi e conformi.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Data ultimo aggiornamento</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. La frequenza dei contatti può essere configurata tramite le impostazioni dei criteri di gruppo.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Stato che indica se l'utente è esonerato o non è esentato dai criteri di BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utente esentato</p></td>
<td align="left"><p>Utente che è esonerato dai criteri di BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Data di esenzione</p></td>
<td align="left"><p>Data in cui è stata concessa l'esenzione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato relativi allo stato di conformità del computer in conformità con i criteri specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Intensità cifratura criteri</p></td>
<td align="left"><p>Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri MBAM, ad esempio 128 bit con diffusore.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Criteri: unità di sistema operativo</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per il sistema operativo e per il tipo di protezione appropriato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Criteri: unità dati fissa</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'unità dati fissa.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Produttore</p></td>
<td align="left"><p>Nome del produttore del computer come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modello</p></td>
<td align="left"><p>Nome del modello del produttore del computer come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di dispositivi</p></td>
<td align="left"><p>Utenti noti nel computer gestito da MBAM.</p></td>
</tr>
</tbody>
</table>

 

**Report conformità computer BitLocker: campi volume computer**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome colonna</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Lettera di unità</p></td>
<td align="left"><p>Lettera dell'unità del computer assegnata all'unità specifica dall'utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo di unità</p></td>
<td align="left"><p>Tipo di unità. I valori validi sono unità di sistema operativo e unità dati fissa. Si tratta di unità fisiche anziché di volumi logici.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Intensità cifratura</p></td>
<td align="left"><p>Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipi di protezione</p></td>
<td align="left"><p>Tipo di protezione selezionata tramite il criterio usato per crittografare un sistema operativo o un'unità dati fissa. I tipi di protezione validi per un sistema operativo sono TPM o TPM + PIN. Il tipo di protezione valido per un'unità dati fissa è una password.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato Protector</p></td>
<td align="left"><p>Indica che il computer gestito da MBAM ha abilitato il tipo di protezione specificato nel criterio. Gli stati validi sono attivato o disattivato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Stato di crittografia</p></td>
<td align="left"><p>Stato di crittografia dell'unità. Gli stati validi sono crittografati, non crittografati e crittografati.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





