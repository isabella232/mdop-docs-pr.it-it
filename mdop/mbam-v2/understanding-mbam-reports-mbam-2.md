---
title: Informazioni sui report di MBAM
description: Informazioni sui report di MBAM
author: dansimp
ms.assetid: 8778f333-760e-4f26-acb4-4e73b6fbb536
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3c3ca5e4da4cbcea80c87520f0ecd05e1e7d6be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823815"
---
# Informazioni sui report di MBAM


Se si è scelta la topologia autonoma quando è stato installato Microsoft BitLocker Administration and Monitoring (MBAM), è possibile eseguire report diversi in MBAM per monitorare l'uso e la conformità di BitLocker. MBAM riporta la conformità e altre informazioni su tutti i computer e i dispositivi gestiti. Le informazioni contenute in questo argomento possono essere usate per comprendere i report di amministrazione e monitoraggio di Microsoft BitLocker per le aziende e la conformità dei singoli computer e per l'attività di ripristino delle chiavi.

**Nota**  Se si è scelta la topologia di Configuration Manager quando è stato installato Microsoft BitLocker Administration and Monitoring (MBAM), i report vengono generati da Configuration Manager invece che da MBAM. Per altre informazioni sui report eseguiti da Configuration Manager, vedere Concetti relativi [ai report di mbam in Configuration Manager](understanding-mbam-reports-in-configuration-manager.md).

 

## Informazioni sui report


Per accedere alla caratteristica report di amministrazione e monitoraggio di Microsoft BitLocker, aprire un Web browser e aprire il sito Web di amministrazione e monitoraggio. Selezionare **report** nella barra dei menu a sinistra e quindi selezionare una delle opzioni che si desidera generare nella barra del menu superiore.

### Report conformità aziendale

Usare questo tipo di report per raccogliere informazioni sulla conformità complessiva di BitLocker nell'organizzazione. Puoi usare filtri diversi per limitare i risultati della ricerca allo stato di conformità e allo stato di errore. Le informazioni del report vengono aggiornate ogni sei ore.

**Campi rapporto conformità aziendale**

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
<td align="left"><p>Stato di conformità per il computer, in base ai criteri specificati per il computer. Gli Stati non sono conformi e conforme. Per altre informazioni su come interpretare gli Stati di conformità, vedere la tabella Stati di conformità del report conformità aziendale.</p></td>
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

 

**Stati di conformità del report conformità aziendale**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Stato conformità</th>
<th align="left">Esenzione</th>
<th align="left">Descrizione</th>
<th align="left">Azione utente</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Non conforme</p></td>
<td align="left"><p>Non esenti</p></td>
<td align="left"><p>Il computer non è conforme, in base ai criteri specificati.</p></td>
<td align="left"><p>Espandere i dettagli del report di conformità del computer facendo clic su <strong> nome computer </strong> e determinare se lo stato di ogni unità è conforme ai criteri specificati. Se lo stato di crittografia indica che il computer non è crittografato, è possibile che la crittografia sia in corso oppure si verifichi un errore nel computer. Se non è presente alcun errore, la causa probabile è che il computer sia ancora in fase di connessione o di determinazione dello stato di crittografia. Controllare più avanti per determinare se lo stato cambia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Non esenti</p></td>
<td align="left"><p>Il computer è conforme, in base ai criteri specificati.</p></td>
<td align="left"><p>Nessuna azione necessaria; lo stato del computer può essere confermato visualizzando il report conformità computer.</p></td>
</tr>
</tbody>
</table>

 

### Report conformità computer

Usare questo tipo di report per raccogliere informazioni specifiche per un computer o un utente.

Questo report può essere visualizzato facendo clic sul nome del computer nel report conformità aziendale oppure digitando il nome del computer nel report conformità computer. Il report conformità computer fornisce informazioni dettagliate sulla crittografia per ogni unità (sistema operativo e unità dati fisse) in un computer e anche un'indicazione dei criteri applicati a ogni tipo di unità nel computer. Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.

**Nota**  Lo stato di crittografia dei volumi di dati rimovibili non verrà visualizzato nel report.

 

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
<td align="left"><p>Nome di dominio completo, in cui risiede il computer client ed è gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di computer</p></td>
<td align="left"><p>Tipo di computer. I tipi validi non sono portatili e portatili.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operativo</p></td>
<td align="left"><p>Tipo di sistema operativo disponibile nel computer client di MBAM-Managed.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Stato complessivo di conformità del computer gestito da MBAM. Gli stati validi sono conformi e conformi. Si noti che lo stato di conformità per unità (vedere la tabella seguente) può indicare stati di conformità diversi. Tuttavia, questo campo rappresenta lo stato di conformità, in base ai criteri specificati.</p></td>
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
<td align="left"><p>Produttore</p></td>
<td align="left"><p>Nome del produttore del computer, come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modello</p></td>
<td align="left"><p>Nome del modello del produttore del computer, come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato dello stato di conformità del computer, in conformità con i criteri specificati.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ultimo contatto</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. La frequenza di contatto è configurabile (Vedi impostazioni dei criteri di MBAM).</p></td>
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
<td align="left"><p>Tipo di protezione selezionata tramite il criterio usato per crittografare un sistema operativo o un volume di dati fisso.</p></td>
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

 

### Report di controllo del ripristino

Usare questo tipo di report per controllare gli utenti che hanno richiesto l'accesso alle chiavi di ripristino. Il report offre diversi filtri in base ai criteri di filtro desiderati. Gli utenti possono filtrare in base a un tipo specifico di utente, un utente dell'help desk o un utente finale, se la richiesta non è riuscita o ha avuto esito positivo, il tipo specifico di chiave richiesta e un intervallo di date durante il quale si è verificato il recupero. L'amministratore può produrre report contestuali in base alle esigenze.

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
<td align="left"><p>Stato della richiesta</p></td>
<td align="left"><p>Stato della richiesta. Gli stati validi hanno esito positivo (la chiave è stata recuperata) o non è riuscito (la chiave non è stata recuperata).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utente helpdesk</p></td>
<td align="left"><p>Utente dell'help desk che ha avviato la richiesta di recupero tasti. Nota: se l'utente dell'help desk recupera la chiave per conto di un utente finale, il campo utente finale sarà vuoto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utente</p></td>
<td align="left"><p>Utente finale che ha avviato la richiesta di recupero tasti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di chiave</p></td>
<td align="left"><p>Tipo di chiave richiesto dall'utente dell'help desk o dall'utente finale. I tre tipi di chiavi che MBAM raccoglie sono: password chiave di ripristino (usata per il ripristino di un computer in modalità di ripristino), ID chiave di ripristino (usata per recuperare un computer in modalità di ripristino per conto di un altro utente) e hash della password del TPM (usato per recuperare un computer con un TPM bloccato).</p></td>
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

 

**Nota**  I risultati del report possono essere salvati in un file facendo clic sul pulsante **Esporta** nella barra dei menu report. Per altre informazioni su come eseguire i report di MBAM, vedere [come generare report di mbam](how-to-generate-mbam-reports-mbam-2.md).

 

## Argomenti correlati


[Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





