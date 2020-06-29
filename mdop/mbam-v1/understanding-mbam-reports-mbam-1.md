---
title: Informazioni sui report di MBAM
description: Informazioni sui report di MBAM
author: dansimp
ms.assetid: 34e4aaeb-7f89-41a1-b816-c6fe8397b060
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa64a4724c87a42774e569b556013bfec2ed5514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822866"
---
# Informazioni sui report di MBAM


Microsoft BitLocker Administration and Monitoring (MBAM) genera diversi report per monitorare l'uso e la conformità di BitLocker. Questo argomento descrive i report di MBAM per conformità aziendali, singoli computer, compatibilità hardware e attività di ripristino delle chiavi.

## Informazioni sui report


Per accedere alla caratteristica report di MBAM, aprire il sito Web di amministrazione MBAM. Selezionare **report** nel riquadro di spostamento. Nel riquadro contenuto principale fare clic sulla scheda relativa al tipo di report: **report conformità aziendale**, report **conformità computer**, **report controllo hardware**o **rapporto di controllo del ripristino**.

### Report conformità aziendale

Un report di conformità aziendale fornisce informazioni sulla conformità complessiva di BitLocker nell'organizzazione. I filtri disponibili per questo report consentono di limitare i risultati della ricerca in base allo stato di conformità e allo stato di errore. Questo report viene eseguito ogni sei ore.

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
<td align="left"><p>Il nome DNS specificato dall'utente gestito da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome di dominio</p></td>
<td align="left"><p>Il nome di dominio completo in cui risiede il computer client e viene gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Lo stato di conformità per il computer, in base ai criteri specificati per il computer. Gli stati possibili non sono conformi e conforme. Per altre informazioni, vedere Stati di conformità del report conformità aziendale in questo argomento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Lo stato dell'hardware del computer per determinare l'identificazione del tipo di hardware e se il computer è esentato dai criteri. Ci sono tre possibili stati: hardware sconosciuto (il tipo di hardware non è stato identificato da MBAM), l'hardware è esentato (il tipo di hardware è stato identificato ed è stato contrassegnato come esentato dai criteri di MBAM) e non è esentato (l'hardware è stato identificato e non è esentato dai criteri).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utenti di dispositivi</p></td>
<td align="left"><p>Utenti noti nel computer gestito da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato relativi allo stato di conformità del computer in base ai criteri specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ultimo contatto</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. Questa volta è configurabile. Vedi impostazioni dei criteri di MBAM.</p></td>
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
<td align="left"><p>Il computer non è conforme ai criteri specificati e il tipo di hardware non è stato indicato come esenti da criteri.</p></td>
<td align="left"><p>Fare clic su <strong> nome computer </strong> per espandere il report conformità computer e determinare se lo stato di ogni unità è conforme ai criteri specificati. Se lo stato di crittografia indica che il computer non è crittografato, la crittografia potrebbe essere ancora in corso oppure potrebbe esserci un errore nel computer. Se non è presente alcun errore, la causa probabile è che il computer sia ancora in fase di connessione o di determinazione dello stato di crittografia. Controllare più avanti per determinare se lo stato cambia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Non esenti</p></td>
<td align="left"><p>Il computer è conforme ai criteri specificati.</p></td>
<td align="left"><p>Non è necessaria alcuna azione. Facoltativamente, è possibile visualizzare il report conformità computer per confermare lo stato del computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Componenti hardware esenti</p></td>
<td align="left"><p>Se il tipo di hardware è esonerato. Indipendentemente dal modo in cui è impostato il criterio o dallo stato individuale di ogni disco rigido, lo stato complessivo viene considerato conforme.</p></td>
<td align="left"><p>Non è necessaria alcuna azione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Conformi</p></td>
<td align="left"><p>Hardware sconosciuto</p></td>
<td align="left"><p>MBAM riconosce il tipo di hardware, ma MBAM non sa se è esentasse o non è esonerato. Questo problema si verifica se l'amministratore non ha impostato lo stato compatibile per l'hardware. Di conseguenza, MBAM ripristina lo stato di conformità per impostazione predefinita.</p></td>
<td align="left"><p>Questo è lo stato iniziale di un client MBAM appena distribuito. Si tratta in genere solo di uno stato temporaneo. Anche se l'amministratore ha contrassegnato l'hardware come compatibile, può essere necessario un ritardo significativo o un tempo di attesa configurabile prima che il computer client ritorni. Prendere nota dell'ora dell'ultimo contatto ed eseguire di nuovo il check-in dopo l'intervallo specificato per verificare se lo stato è stato modificato. Se lo stato non è stato modificato, potrebbe essersi verificato un errore per il computer o il tipo di hardware.</p></td>
</tr>
</tbody>
</table>

 

### Report conformità computer

Il report conformità computer Visualizza le informazioni specifiche di un computer o un utente.

Il report conformità computer offre informazioni dettagliate sulla crittografia e i criteri applicabili per ogni unità di un computer, incluse le unità del sistema operativo e le unità dati fisse. Per visualizzare questo tipo di report, fare clic sul nome del computer nel report conformità aziendale oppure digitare il nome del computer nel report conformità computer. Per visualizzare i dettagli di ogni unità, espandere la voce nome computer.

**Nota**  Questo report non offre lo stato di crittografia per i volumi di dati rimovibili.

 

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
<td align="left"><p>Il nome del computer DNS specificato dall'utente gestito da MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome di dominio</p></td>
<td align="left"><p>Il nome di dominio completo in cui risiede il computer client e viene gestito da MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di computer</p></td>
<td align="left"><p>Tipo di portabilità del computer. I tipi validi non sono portatili e portatili.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistema operativo</p></td>
<td align="left"><p>Tipo di sistema operativo installato nel computer client gestito MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Lo stato di conformità complessivo del computer gestito da MBAM. Gli stati validi sono conformi e conformi. Mentre è possibile avere unità conformi e non conformi nello stesso computer, questo campo indica la conformità complessiva del computer per ogni criterio specificato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Forza di Cypher dei criteri</p></td>
<td align="left"><p>La forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM. Ad esempio, 128 bit con il diffusore</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unità del sistema operativo dei criteri</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'O/S e il tipo di protezione, se applicabile.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unità dati fissata per i criteri</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'unità fissa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Unità dati rimovibili dei criteri</p></td>
<td align="left"><p>Indica se è necessaria la crittografia per l'unità rimovibile.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utenti di dispositivi</p></td>
<td align="left"><p>Fornisce l'identità degli utenti noti nel computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esenzione</p></td>
<td align="left"><p>Indica se il tipo di hardware del computer è riconosciuto da MBAM e, se noto, se il computer è stato indicato come esenti da criteri. Ci sono tre stati: hardware sconosciuto (il tipo di hardware non è stato identificato da MBAM); Hardware esenti (il tipo di hardware è stato identificato ed è stato contrassegnato come esenti dai criteri di MBAM); e non esenti (l'hardware è stato identificato e non è esentato dai criteri).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Produttore</p></td>
<td align="left"><p>Nome del produttore del computer come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modello</p></td>
<td align="left"><p>Nome del modello di produttore del computer come viene visualizzato nel BIOS del computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Messaggi di errore e di stato dello stato di conformità del computer in conformità con i criteri specificati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ultimo contatto</p></td>
<td align="left"><p>Data e ora in cui il computer ha contattato l'ultima volta il server per segnalare lo stato di conformità. T</p></td>
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
<td align="left"><p>Lettera dell'unità del computer assegnata a questa specifica unità dall'utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo di unità</p></td>
<td align="left"><p>Tipo di unità. I valori validi sono unità di sistema operativo e unità dati fissa. Si tratta di unità fisiche anziché di volumi logici.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Forza di cifratura</p></td>
<td align="left"><p>Forza di cifratura selezionata dall'amministratore durante la specifica dei criteri di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Tipo di protezione</p></td>
<td align="left"><p>Tipo di protezione selezionata tramite criteri usati per crittografare un sistema operativo o un volume fisso. I tipi di protezione validi in un'unità del sistema operativo sono TPM o TPM + PIN. L'unico tipo di protezione valido per un volume di dati fisso è la password.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato Protector</p></td>
<td align="left"><p>Questo campo indica se il computer ha abilitato il tipo di protezione specificato nel criterio. Gli stati validi sono attivato o disattivato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Stato di crittografia</p></td>
<td align="left"><p>Questo è lo stato di crittografia corrente dell'unità. Gli stati validi sono crittografati, non crittografati e crittografati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Stato conformità</p></td>
<td align="left"><p>Indica se l'unità è conforme ai criteri. Gli Stati non sono conformi e conforme.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dettagli sullo stato di conformità</p></td>
<td align="left"><p>Contiene messaggi di errore e di stato relativi allo stato di conformità del computer.</p></td>
</tr>
</tbody>
</table>

 

### Report di controllo hardware

Questo report consente di controllare le modifiche apportate allo stato di compatibilità hardware di specifiche funzionalità e modelli di computer. Per limitare i risultati della ricerca, questo report include l'applicazione di filtri ai criteri, ad esempio il tipo di modifica e l'ora dell'occorrenza. Ogni modifica dello stato viene rilevata dall'utente e dalla data e dall'ora. Il tipo di hardware viene automaticamente compilato dall'agente MBAM che viene eseguito nel computer client. Questo report consente di tenere traccia delle modifiche apportate dall'utente alle informazioni raccolte direttamente da MBAM Managed computer. Una tipica modifica amministrativa cambia da compatibile a non compatibile. Tuttavia, l'amministratore può anche rivedere qualsiasi campo.

**Campi rapporto di controllo hardware**

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
<td align="left"><p>Data e ora</p></td>
<td align="left"><p>Data e ora in cui è stata apportata una modifica al tipo di hardware. Tieni presente che ogni tipo di hardware univoco viene assegnato ad almeno una voce.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utente</p></td>
<td align="left"><p>Utente amministrativo che ha apportato la modifica per la voce specifica.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di modifica</p></td>
<td align="left"><p>Tipo di modifica apportata alle informazioni sul tipo di hardware. I valori validi sono addizione (nuova voce), aggiornamento (modifica voce esistente) o eliminazione (Rimuovi voce esistente).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Valore originale</p></td>
<td align="left"><p>Valore della specifica del tipo di hardware prima che venisse apportata la modifica.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Valore corrente</p></td>
<td align="left"><p>Valore della specifica del tipo di hardware dopo che è stata apportata la modifica.</p></td>
</tr>
</tbody>
</table>

 

### Report di controllo del ripristino

Il report di controllo del recupero consente di controllare gli utenti che hanno richiesto l'accesso alle chiavi di ripristino. I criteri di filtro per questo report includono il tipo di utente che effettua la richiesta, il tipo di chiave richiesta, l'ora dell'occorrenza, l'esito positivo o negativo, l'ora dell'occorrenza e il tipo di richiesta dell'utente (Help desk, utente finale). Questo report consente agli amministratori di produrre report contestuali in base alle esigenze.

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
<td align="left"><p>La data e l'ora in cui una richiesta di recupero tasti è stata effettuata da un utente finale o da un utente dell'help desk.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Stato della richiesta</p></td>
<td align="left"><p>Stato della richiesta. Gli stati validi hanno esito positivo (la chiave è stata recuperata) o non è riuscito (la chiave non è stata recuperata).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Utente helpdesk</p></td>
<td align="left"><p>L'utente dell'help desk che ha avviato la richiesta di recupero tasti. Se l'utente dell'help desk recupera la chiave per conto di un utente finale, il campo utente finale sarà vuoto.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utente</p></td>
<td align="left"><p>L'utente finale che ha avviato la richiesta di recupero tasti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tipo di chiave</p></td>
<td align="left"><p>Il tipo di chiave richiesto. MBAM raccoglie tre tipi di chiave: password chiave di ripristino (per il ripristino di un computer in modalità di ripristino); ID chiave di ripristino (per recuperare un computer in modalità di ripristino per conto di un altro utente); e hash della password Trusted Platform Module (TPM) (per recuperare un computer con un TPM bloccato).</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione motivo</p></td>
<td align="left"><p>Il motivo per cui è stato richiesto il tipo di chiave specificato. I motivi sono specificati nelle funzionalità di recupero unità e Gestisci TPM del sito Web amministrativo. Le voci valide includono il testo immesso dall'utente o uno dei codici motivo seguenti:</p>
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
</ul>
<p></p></td>
</tr>
</tbody>
</table>

 

**Nota**  Per salvare i risultati del report in un file, fare clic sul pulsante **Esporta** nella barra dei menu report.

 

## Argomenti correlati


[Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





