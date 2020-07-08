---
title: Informazioni sui report autonomi di MBAM 2.5
description: Informazioni sui report autonomi di MBAM 2.5
author: dansimp
ms.assetid: 78b5aaf4-8257-4722-8eb9-e0de48db6a11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45e84c7c3b2bcb1602890c7c5a09592324da691e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804480"
---
# Informazioni sui report autonomi di MBAM 2.5


In questo argomento vengono descritti i report disponibili quando si esegue Microsoft BitLocker Administration and Monitoring (MBAM) nella topologia autonoma.

**Nota**  
Se si esegue MBAM con la topologia di integrazione di Configuration Manager, è possibile generare report da Configuration Manager invece che da MBAM. Per altre informazioni su questi report, vedere [visualizzazione di report di MBAM 2,5 per la topologia di integrazione di Configuration Manager](viewing-mbam-25-reports-for-the-configuration-manager-integration-topology.md) .



## Informazioni sui report della topologia autonoma di MBAM


MBAM offre tre tipi di report che è possibile usare per monitorare l'organizzazione per la conformità a BitLocker:

-   [Report conformità aziendale](#bkmk-enterprisecompliance)

-   [Report conformità computer](#bkmk-compliance)

-   [Report di controllo del ripristino](#bkmk-recovery)

Per accedere ai report di MBAM quando si esegue MBAM nella topologia autonoma, aprire un Web browser e quindi aprire il sito Web di amministrazione e monitoraggio. Selezionare **report** nella barra dei menu a sinistra. Nella barra dei menu superiore selezionare il tipo di report che si desidera generare. Per altre informazioni sulla generazione di questi report, vedere generazione di report autonomi di [MBAM 2,5](generating-mbam-25-stand-alone-reports.md).

### <a href="" id="bkmk-enterprisecompliance"></a>Report conformità aziendale

Usare questo tipo di report per raccogliere informazioni sulla conformità complessiva di BitLocker nell'organizzazione. È possibile usare i filtri per limitare i risultati della ricerca per ottenere maggiori informazioni sullo stato di conformità e sullo stato di errore dei computer dell'organizzazione.

**Panoramica sulla conformità aziendale**

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
<td align="left"><p>% Esenti</p></td>
<td align="left"><p>Percentuale di computer esenti dal requisito di crittografia di BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>% Non esenti</p></td>
<td align="left"><p>Percentuale di computer non esenti dal requisito di crittografia BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Percentuale di computer conformi nell'organizzazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Percentuale di computer non conformi nell'organizzazione.</p></td>
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



**Dettagli del computer conformità aziendale**

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
<td align="left"><p>Nome DNS specificato dall'utente gestito da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome di dominio</p></td>
<td align="left"><p>Nome di dominio completo in cui risiede il computer client e gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Stato di conformità per il computer, in base ai criteri specificati per il computer. Gli Stati non sono conformi e conforme. Per altre informazioni su come interpretare gli Stati di conformità, vedere la tabella degli Stati di conformità dell'organizzazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Stato che indica se il computer è esentato dai criteri di BitLocker.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato relativi allo stato di conformità del computer in base ai criteri specificati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ultimo contatto</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. La frequenza dei contatti è configurabile. Per altre informazioni, Vedi le impostazioni dei criteri di gruppo di MBAM.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-compliance"></a>Report conformità computer

Usare questo tipo di report per raccogliere informazioni specifiche per un computer o un utente.

Per visualizzare questo report, fare clic sul nome del computer nel report conformità aziendale oppure digitare il nome del computer nel report conformità computer. Questo report Mostra informazioni dettagliate sulla crittografia di ogni unità (sistema operativo e unità dati fisse) in un computer. Indica anche il criterio applicato a ogni tipo di unità nel computer. Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.

**Nota**  
Lo stato di crittografia dei volumi di dati rimovibili non viene visualizzato nel report.



**Campi rapporto conformità computer**

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
<td align="left"><p>Nome di dominio completo in cui risiede il computer client e gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di computer</p></td>
<td align="left"><p>Tipo di computer. I tipi validi non sono portatili e portatili.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operativo</p></td>
<td align="left"><p>Tipo di sistema operativo trovato nel computer client gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Stato di conformità generale del computer gestito da MBAM. Gli stati validi sono conformi e conformi.</p>
<p>Si noti che lo stato di conformità per unità (vedere la tabella seguente) può indicare stati di conformità diversi. Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Intensità cifratura criteri</p></td>
<td align="left"><p>Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM (ad esempio, 128 bit con diffusore).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unità del sistema operativo dei criteri</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per il sistema operativo e Mostra il tipo di protezione appropriato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Criteri-unità dati fissata</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'unità dati fissa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unità dati rimovibili dei criteri</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'unità rimovibile.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di dispositivi</p></td>
<td align="left"><p>Utenti noti nel computer gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Stato che indica se il computer è esentato dai criteri di BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Produttore</p></td>
<td align="left"><p>Nome del produttore del computer, come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modello</p></td>
<td align="left"><p>Nome del modello del produttore del computer, come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato relativi allo stato di conformità del computer, in conformità con i criteri specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ultimo contatto</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. La frequenza dei contatti è configurabile. Per altre informazioni, Vedi le impostazioni dei criteri di gruppo di MBAM.</p></td>
</tr>
</tbody>
</table>



**Campi unità report conformità computer**

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
<td align="left"><p>Tipo di protezione</p></td>
<td align="left"><p>Tipo di protezione selezionata tramite l'impostazione di criteri di gruppo utilizzata per crittografare un sistema operativo o un volume di dati fisso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato Protector</p></td>
<td align="left"><p>Indica che il computer gestito da MBAM ha abilitato il tipo di protezione specificato nel criterio. Gli stati validi sono attivato o disattivato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Stato di crittografia</p></td>
<td align="left"><p>Stato di crittografia dell'unità. Gli stati validi sono crittografati, non crittografati e crittografati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Stato che indica se l'unità è conforme ai criteri. Gli Stati non sono conformi e conforme.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato dello stato di conformità del computer, in base ai criteri specificati.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-recovery"></a>Report di controllo del ripristino

Usare questo tipo di report per controllare gli utenti che hanno richiesto l'accesso alle chiavi di ripristino di BitLocker. Il report offre diversi filtri in base ai criteri di filtro desiderati. È possibile filtrare in base a un tipo specifico di utente (un utente dell'help desk o un utente finale), se la richiesta non è riuscita o ha avuto esito positivo, il tipo specifico di chiave richiesta e un intervallo di date durante il quale si è verificato il recupero.

**Campi rapporto di controllo ripristino**

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
<td align="left"><p>Richiedere data e ora</p></td>
<td align="left"><p>Data e ora in cui una richiesta di recupero tasti è stata effettuata da un utente finale o da un utente dell'help desk.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Origine della richiesta di controllo</p></td>
<td align="left"><p>Il sito da cui è stata avviata la richiesta. Questa voce avrà uno dei due valori seguenti: <strong> portale self-service </strong> o <strong> helpdesk </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato della richiesta</p></td>
<td align="left"><p>Stato della richiesta. Gli stati validi hanno esito positivo (la chiave è stata recuperata) o non è riuscito (la chiave non è stata recuperata).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utente helpdesk</p></td>
<td align="left"><p>Utente dell'help desk che ha avviato la richiesta di recupero tasti.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se un utente di helpdesk avanzato ripristina la chiave senza specificare l'utente finale, il <strong> campo utente finale </strong> sarà vuoto. Un utente di helpdesk standard deve specificare l'utente finale e l'utente verrà visualizzato in questo campo.</p>
<p>Un recupero tramite il portale self-service elenca l'utente finale richiedente sia in questo campo che nel <strong> campo utente finale </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Utente finale</p></td>
<td align="left"><p>Utente finale che ha avviato la richiesta di recupero tasti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Computer</p></td>
<td align="left"><p>Nome computer del computer recuperato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di chiave</p></td>
<td align="left"><p>Tipo di chiave richiesto dall'utente dell'help desk o dall'utente finale. I tre tipi di chiavi che MBAM raccoglie sono:</p>
<ul>
<li><p>Password chiave di ripristino (usata per recuperare un computer in modalità di ripristino)</p></li>
<li><p>ID chiave di ripristino (usato per recuperare un computer in modalità di ripristino per conto di un altro utente)</p></li>
<li><p>Hash della password TPM (usato per recuperare un computer con un TPM bloccato)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione motivo</p></td>
<td align="left"><p>Motivo per cui il tipo di chiave specificato è stato richiesto dall'utente dell'help desk o dall'utente finale. I motivi sono specificati nelle funzionalità di recupero unità e Gestisci TPM del sito Web amministrazione e monitoraggio. Le voci valide sono testo immesso dall'utente o uno dei codici motivo seguenti:</p>
<ul>
<li><p>Modifica dell'ordine di avvio del sistema operativo</p></li>
<li><p>BIOS modificato</p></li>
<li><p>File di sistema operativo modificati</p></li>
<li><p>Tasto di avvio perduto</p></li>
<li><p>PIN perduto</p></li>
<li><p>Ripristino TPM</p></li>
<li><p>Passphrase smarrita</p></li>
<li><p>Smartcard persa</p></li>
<li><p>Reimposta blocco PIN</p></li>
<li><p>Attivare il TPM</p></li>
<li><p>Disattivare TPM</p></li>
<li><p>Modificare la password del TPM</p></li>
<li><p>Cancellare TPM</p></li>
</ul></td>
</tr>
</tbody>
</table>



**Nota**  
I risultati del report possono essere salvati in un file facendo clic sul pulsante **Esporta** nella barra dei menu **report** .




## Argomenti correlati


[Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Generazione di report autonomi di MBAM 2.5](generating-mbam-25-stand-alone-reports.md)



## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





