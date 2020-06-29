---
title: Informazioni sui report di MBAM in Configuration Manager
description: Informazioni sui report di MBAM in Configuration Manager
author: dansimp
ms.assetid: b2582190-c9de-4e64-bd5a-f31ac1916f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 995d628cafd03c8bdd209e467c9d22169b7e03c3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823825"
---
# Informazioni sui report di MBAM in Configuration Manager


Quando Microsoft BitLocker Administration and Monitoring (MBAM) viene installato con la topologia integrata di Configuration Manager, le caratteristiche di conformità e Reporting hardware vengono spostate nell'infrastruttura di Configuration Manager e fuori da MBAM. Quando si usa la topologia di Configuration Manager, è possibile eseguire report da Configuration Manager invece che da MBAM, ad eccezione del report di controllo di ripristino, a cui si continua ad accedere tramite il sito Web di amministrazione e monitoraggio.

I report per la topologia integrata di Configuration Manager mostrano la conformità di BitLocker per l'organizzazione e per i singoli computer e dispositivi gestiti da MBAM. I report offrono sia le informazioni tabulari che i grafici e consentono di filtrare i report per visualizzare i dati da prospettive diverse.

Le informazioni contenute in questo argomento descrivono i report di MBAM eseguiti da Configuration Manager. Per informazioni sui report di MBAM per la topologia autonoma, vedere Concetti relativi ai [report di mbam](understanding-mbam-reports-mbam-2.md).

## Accesso ai report in Configuration Manager


Per accedere alla funzionalità report in Configuration Manager, aprire la **console di Configuration Manager**. Per visualizzare l'elenco dei report disponibili:

-   In Configuration Manager 2007 espandere il nodo **Gestione computer** e quindi espandere il nodo **report** .

-   In SystemCenter2012 ConfigurationManager, nell'area di lavoro monitoraggio in **Panoramica**, espandere il nodo **report** e quindi fare clic su **report**.

### Dashboard di conformità di BitLocker Enterprise

Il dashboard conformità Enterprise di BitLocker offre i grafici seguenti, che mostrano lo stato di conformità di BitLocker nell'organizzazione:

-   Distribuzione dello stato di conformità

-   Distribuzione di errori non conformi

-   Distribuzione dello stato di conformità per tipo di unità

**Distribuzione dello stato di conformità**

Questo grafico a torta mostra lo stato di conformità del computer all'interno dell'organizzazione e Mostra la percentuale di computer, in confronto al numero totale di computer della raccolta selezionata, che hanno lo stato di conformità. Viene visualizzato anche il numero effettivo di computer con ogni stato. Il grafico a torta Mostra gli Stati di conformità seguenti:

-   Conformi

-   Non conforme

-   Esenzione dall'utente

-   Esenzione dall'utente temporaneo

-   Criteri non applicati

-   Unknown: i computer il cui stato è stato segnalato come errore o i dispositivi che fanno parte della raccolta, ma che non hanno mai segnalato lo stato di conformità, ad esempio se sono disconnessi dall'organizzazione

**Distribuzione di errori non conformi**

Questo grafico a torta mostra le categorie di computer dell'organizzazione che non sono conformi ai criteri di crittografia unità BitLocker e Mostra il numero di computer in ogni categoria. Ogni percentuale di categoria viene calcolata a partire dal numero totale di computer non conformi della raccolta.

-   Crittografia rimandata dall'utente

-   Non è possibile trovare TPM compatibile

-   Partizione di sistema non disponibile o abbastanza grande

-   Conflitto di criteri

-   Attesa del provisioning automatico del TPM

-   Si è verificato un errore sconosciuto

-   Nessuna informazione-computer che non hanno installato il client MBAM o che hanno installato il client MBAM, ma non attivato, ad esempio, il servizio non funziona

**Distribuzione dello stato di conformità per tipo di unità**

Questo grafico a barre Mostra lo stato di conformità corrente di BitLocker per tipo di unità. Lo stato è "conforme" e "non conforme". Le barre vengono visualizzate per le unità dati fisse e le unità del sistema operativo. I computer che non dispongono di un'unità dati fissa sono inclusi e visualizzano un valore solo nella barra dell'unità del sistema operativo. Il grafico non include gli utenti a cui è stata concessa un'esenzione dal criterio di crittografia unità BitLocker o dalla categoria "nessun criterio".

### Report dettagli conformità di BitLocker Enterprise

Questo report Mostra le informazioni sulla conformità complessiva di BitLocker nell'organizzazione per la raccolta di computer mirati per l'uso di BitLocker.

**Campi rapporto Dettagli conformità Enterprise di BitLocker**

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
<td align="left"><p>Percentuale di computer il cui stato di conformità non è noto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Esenti</p></td>
<td align="left"><p>Percentuale di computer esenti dal requisito di crittografia di BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Non esenti</p></td>
<td align="left"><p>Percentuale di computer esenti dal requisito di crittografia di BitLocker.</p></td>
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
<td align="left"><p>Percentuale di computer il cui stato di conformità non è noto.</p></td>
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

 

**Report dettagli conformità di BitLocker Enterprise-stati di conformità**

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

 

### Report di riepilogo conformità Enterprise di BitLocker

Usare questo tipo di report per visualizzare informazioni sulla conformità complessiva di BitLocker nell'organizzazione e per mostrare la conformità per i singoli computer presenti nella raccolta di computer destinati all'uso di BitLocker.

**Campi rapporto di riepilogo conformità Enterprise di BitLocker**

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
<td align="left"><p>Percentuale di computer il cui stato di conformità non è noto.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Esenti</p></td>
<td align="left"><p>Percentuale di computer esenti dal requisito di crittografia di BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>% Non esenti</p></td>
<td align="left"><p>Percentuale di computer esenti dal requisito di crittografia di BitLocker.</p></td>
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
<td align="left"><p>Percentuale di computer il cui stato di conformità non è noto.</p></td>
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

 

**Report di riepilogo conformità aziendale di BitLocker-dettagli computer**

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
<td align="left"><p>Stato complessivo di conformità del computer gestito da MBAM. Gli stati validi sono conformi e conformi. Si noti che lo stato di conformità per unità (Vedi tabella seguente) può indicare stati di conformità diversi. Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Stato che indica se l'utente è esonerato o non esonerato dai criteri di BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di dispositivi</p></td>
<td align="left"><p>Utente del dispositivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato dello stato di conformità del computer in base ai criteri specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ultimo contatto</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. La frequenza di contatto è configurabile (Vedi impostazioni dei criteri di MBAM).</p></td>
</tr>
</tbody>
</table>

 

### Report conformità computer BitLocker

Usare questo tipo di report per raccogliere informazioni specifiche di un computer. Il report conformità computer fornisce informazioni dettagliate sulla crittografia per ogni unità (sistema operativo e unità dati fisse) in un computer e anche un'indicazione dei criteri applicati a ogni tipo di unità nel computer. Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.

**Nota**  Lo stato di crittografia dei volumi di dati rimovibili non viene visualizzato nel report.

 

**Report conformità computer BitLocker-campi dettagli computer**

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
<td align="left"><p>Stato complessivo di conformità del computer gestito da MBAM. Gli stati validi sono conformi e conformi. Si noti che lo stato di conformità per unità (Vedi tabella seguente) può indicare stati di conformità diversi. Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</p></td>
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
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. La frequenza di contatto è configurabile (Vedi impostazioni dei criteri di MBAM).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Stato che indica se l'utente è esonerato o non esonerato dai criteri di BitLocker.</p></td>
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
<td align="left"><p>Messaggi di errore e di stato dello stato di conformità del computer in base ai criteri specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Intensità cifratura criteri</p></td>
<td align="left"><p>Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM. (ad esempio, 128 bit con il diffusore).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Criteri: unità di sistema operativo</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'O/S e il tipo di protezione appropriato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Criteri: unità dati fissa</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'unità fissa.</p></td>
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

 

**Report conformità computer BitLocker-campi volume computer**

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
<td align="left"><p>Tipo di protezione selezionata tramite criteri usati per crittografare un sistema operativo o un volume fisso. I tipi di protezione validi in un sistema operativo sono TPM o TPM + PIN e per un volume di dati fisso si intende la password.</p></td>
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


[Uso di MBAM con Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





