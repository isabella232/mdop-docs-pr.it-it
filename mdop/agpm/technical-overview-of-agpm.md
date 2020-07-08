---
title: Panoramica tecnica di Gestione avanzata Criteri di gruppo
description: Panoramica tecnica di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818296"
---
# Panoramica tecnica di Gestione avanzata Criteri di gruppo


Microsoft Advanced Group Policy Management è un'applicazione client/server. Il server Advanced Group Policy Management archivia gli oggetti Criteri di gruppo (GPO) offline nell'archivio creato da Advanced Group Policy Management nel file System del server. Gli amministratori dei criteri di gruppo usano lo snap-in gestione avanzata Criteri di gruppo per gestire la console di Group Policy Management (GPMC) per il funzionamento con gli oggetti GPO nel server che ospita l'archivio. Informazioni sulle parti di Advanced Group Policy Management e sugli elementi correlati, sulla modalità di archiviazione degli oggetti Criteri di gruppo nel file System e sul modo in cui le autorizzazioni controllano le azioni disponibili per ogni ruolo utente possono migliorare l'efficacia degli amministratori dei criteri di raggruppamento con Advanced

## Terminologia


Di seguito vengono illustrati i termini di base per la gestione avanzata.

-   **Client Advanced Group Policy Management:** Computer che esegue lo snap-in Advanced Group Policy Management per la console Gestione criteri di gruppo e da cui gli amministratori dei criteri di gruppo gestiscono GPO.

-   **Snap-in Advanced Group Policy Management:** Il componente software di Advanced Group Policy Management installato nei client Advanced Group Policy Management per poter gestire gli oggetti Criteri di gestione.

-   **Server Advanced Group Policy Management:** Un server che esegue il servizio Advanced Group Policy Management e gestisce un archivio. Ogni server Advanced Group Policy Management può gestire un solo archivio, ma un server Advanced Group Policy Management può gestire i dati di archiviazione per più domini in un unico archivio. Un archivio può essere ospitato in un computer diverso da un server Advanced Group Policy Management.

-   **Servizio Advanced Group Policy:** Il componente software di Advanced Group Policy Management eseguito in un server Advanced Group Policy Management come servizio. Il servizio gestisce i GPO nell'archivio e nell'ambiente di produzione in tale foresta.

-   **Archivio:** In Advanced Group Policy Management, un archivio centrale che contiene i GPO controllati gestiti dal server Advanced Group Policy Management, oltre alla cronologia di ognuno di questi GPO. Include tutte le versioni precedenti controllate di ogni oggetto Criteri di controllo. Un archivio è costituito da un file di indice di archiviazione e da dati di archiviazione associati che potrebbero includere dati per gli oggetti Criteri di gruppo in più domini. Un archivio può essere ospitato in un computer diverso da un server Advanced Group Policy Management.

-   **GPO controllato:** Un GPO gestito da Advanced Group Policy Management. Advanced Group Policy Management gestisce la cronologia e le autorizzazioni degli oggetti Criteri di controllo, che vengono archiviati nell'archivio.

-   **GPO non controllato:** Un GPO nell'ambiente di produzione per un dominio e non gestito da Advanced Group Policy Management.

## Quali Advanced Group Policy Management installa, crea e influenza


In un server Advanced Group Policy Management il programma di configurazione Advanced Group Policy Management installa il servizio Advanced Group Policy. Advanced Group Policy Management non modifica il servizio directory® Active Directory o lo schema. Per impostazione predefinita, i file di programma del server Advanced Group Policy Management sono installati in%ProgramFiles%\\Microsoft\\AGPM\\Server. È possibile installare il servizio Advanced Group Policy Management su un controller di dominio, se necessario; Tuttavia, è consigliabile installare il servizio Advanced Group Policy Management in un server membro.

In un client Advanced Group Policy Management, il programma di configurazione Advanced Group Policy Management installa lo snap-in Advanced Group Policy Management, aggiungendo una cartella del **controllo di modifica** a ogni dominio visualizzato in GPMC. Per impostazione predefinita, i file di programma client Advanced Group Policy Management vengono installati in%ProgramFiles%\\Microsoft\\AGPM\\Client.

La tabella 1 descrive sia gli elementi installati o creati da Advanced Group Policy che le parti del sistema operativo che influiscono sull'operazione Advanced Group Policy Management.

**Tabella 1: elementi installati, creati o interessati da Advanced Group Policy Management**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servizio Advanced Group Policy</p></td>
<td align="left"><p>Il servizio Advanced Group Policy Management viene eseguito nel server Advanced Group Policy Management. Il servizio gestisce l'archivio, che contiene GPO offline e i GPO controllati nell'ambiente di produzione. La configurazione predefinita del servizio Advanced Group Policy Management è la seguente:</p>
<ul>
<li><p><strong>Nome servizio: </strong> Servizio Advanced Group Policy Management</p></li>
<li><p><strong>Nome visualizzato: </strong> Servizio Advanced Group Policy Management</p></li>
<li><p><strong>Percorso del file eseguibile: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</p></li>
<li><p><strong>Avvio: </strong> automatico</p></li>
<li><p><strong>Accedere come: </strong> account del servizio Advanced Group Policy Management specificato durante l'installazione del server Advanced Group Policy Management, che può essere modificato usando <strong> programmi e funzionalità </strong> nel <strong> Pannello di controllo </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Archivio Advanced Group Policy</p></td>
<td align="left"><p>Per impostazione predefinita, Advanced Group Policy Management crea l'archivio in%ProgramData%\Microsoft\AGPM nel server Advanced Group Policy Management. L'archivio fornisce spazio di archiviazione per gli oggetti Criteri di gruppo offline e può archiviare più versioni di ogni oggetto Criteri di gruppo. Le modifiche apportate da Advanced Group Policy Management agli oggetti Criteri di gruppo nell'archivio non influiscono sull'ambiente di produzione finché un amministratore o un responsabile della gestione avanzata non distribuisce il GPO all'ambiente di produzione e collega il GPO a un'unità organizzativa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Firewall</p></td>
<td align="left"><p>Durante l'installazione, Advanced Group Policy Management consente una regola Windows Firewall in ingresso che consente al client Advanced Group Policy Management di comunicare con il server Advanced Group Policy Management. La regola predefinita di Windows Firewall è la seguente:</p>
<ul>
<li><p><strong>Nome: </strong> Servizio Advanced Group Policy Management</p></li>
<li><p><strong>Azione: </strong> Consenti la connessione</p></li>
<li><p><strong>Programmi: </strong> tutti i programmi che soddisfano le condizioni specificate</p></li>
<li><p><strong>Tipo di protocollo: </strong> TCP</p></li>
<li><p><strong>Porta locale: </strong> 4600</p></li>
<li><p><strong>Porta remota: </strong> tutte le porte</p></li>
<li><p><strong>Indirizzo IP locale: </strong> qualsiasi</p></li>
<li><p><strong>Indirizzo IP remoto: </strong> qualsiasi</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Server di posta elettronica</p></td>
<td align="left"><p>Advanced Group Policy Management usa SMTP (Simple Mail Transfer Protocol) per inviare richieste di posta elettronica agli indirizzi configurati nella <strong> scheda delega del dominio </strong> . Ad esempio, quando un editor richiede la creazione di un nuovo GPO, Advanced Group Policy Management informa ogni indirizzo di posta elettronica specificato nella <strong> scheda delega del dominio </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Snap-in Advanced Group Policy Management</p></td>
<td align="left"><p>Lo snap-in Advanced Group Policy Management per GPMC viene eseguito nei client Advanced Group Policy Management e viene usato dagli amministratori dei criteri di gruppo per gestire i GPO. Lo snap-in viene visualizzato nella cartella GPMC come <strong> controllo </strong> di modifica in ogni dominio.</p></td>
</tr>
</tbody>
</table>

 

### Riferimenti aggiuntivi

Per altre informazioni sui file installati da Advanced Group Policy Management, vedere la [Guida alla pianificazione per Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=160060).

## Archive


Per impostazione predefinita, il processo di installazione del server Advanced Group Policy Management crea l'archivio nel disco rigido locale del server Advanced Group Policy Management su%ProgramData%\\Microsoft\\AGPM. Tuttavia, è possibile modificare il percorso durante l'installazione e persino creare l'archivio in un server diverso da quello della Advanced Group Policy Management.

L'archivio contiene una sottocartella per ogni versione di ogni GPO che contiene l'archivio. Il nome di ogni sottocartella è un GUID che identifica una versione dell'oggetto Criteri di controllo.

Il file gpostate.xml registra lo stato di ogni oggetto Criteri di stato nell'archivio. Il file è un manifesto che descrive il contenuto dell'archivio. Ad esempio, un GPO può avere molte versioni e ogni versione si trova nella sottocartella dell'archivio. Il file gpostate.xml indica le sottocartelle che contengono versioni diverse di un singolo oggetto Criteri di gruppo. Inoltre, i modelli GPO hanno sottocartelle nell'archivio, ma gpostate.xml indica che si tratta di modelli e GPO non controllati. Allo stesso modo, quando gli amministratori di criteri di gruppo eliminano i GPO, Advanced Group Policy Management cambia gli stati in gpostate.xml per indicare che si trovano nel **Cestino** , ma non rimuovono effettivamente le sottocartelle degli oggetti GPO dall'archivio.

**Attenzione**  Non modificare manualmente gpostate.xml o i GPO che contiene l'archivio. Queste informazioni vengono fornite solo per migliorare la comprensione dell'Archivio Advanced Group Policy Management. USA invece lo snap-in Advanced Group Policy Management per modificare i GPO.

 

Quando Advanced Group Policy Management crea l'archivio, fornisce il controllo completo a sistema, agli amministratori e all'account del servizio Advanced Group Policy Management (specificato nella configurazione del server Advanced Group Policy Management). La modifica delle autorizzazioni tramite l'interfaccia utente di Advanced Group Policy Management nello snap-in Advanced Group Policy Management non modifica le autorizzazioni per l'archivio, perché l'account del servizio Advanced Group Policy Management esegue tutte le operazioni per conto dell'utente connesso.

### Riferimenti aggiuntivi

Per informazioni su come eseguire il backup dell'archivio, ripristinare l'archivio da un backup o trasferire sia il server Advanced Group Policy Management che l'archivio, vedere la sezione "esecuzione di attività di amministratore Advanced Group Policy Management" nella [Guida alle operazioni per Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=160061).

## Ruoli e autorizzazioni


I ruoli semplificano la delega. Invece di assegnare autorizzazioni dettagliate agli amministratori dei criteri di gruppo, gli amministratori della Advanced Group Policy Management possono assegnare uno dei quattro ruoli agli amministratori dei criteri di gruppo per consentire loro di eseguire il lavoro correlato a tale ruolo:

-   **Amministratore Advanced Group Policy Management:** Gli amministratori dei criteri di gruppo assegnati al ruolo amministratore Advanced Group Policy Management (controllo completo) possono eseguire qualsiasi attività in Advanced Group Policy Management. Gli amministratori della gestione avanzata Criteri di amministrazione possono configurare opzioni a livello di dominio e delega ad altri amministratori di criteri di gruppo.

-   **Approvatore:** Gli amministratori dei criteri di gruppo assegnati al ruolo approvazione possono distribuire GPO nell'ambiente di produzione per un dominio. I responsabili approvazione possono anche creare ed eliminare GPO e approvare o rifiutare le richieste dagli editori. I responsabili approvazione possono visualizzare l'elenco degli oggetti Criteri di dominio, visualizzare le impostazioni dei criteri in GPO e creare e visualizzare i report delle impostazioni di criteri in un GPO. Non è possibile modificare le impostazioni dei criteri in GPO a meno che non venga assegnato anche il ruolo di editor.

-   **Editor:** Gli amministratori dei criteri di gruppo assegnati al ruolo dell'editor possono visualizzare l'elenco degli oggetti GPO in un dominio, visualizzare le impostazioni dei criteri in GPO, modificare le impostazioni dei criteri in GPO e creare e visualizzare i report delle impostazioni di criteri in un GPO. A meno che non sia anche assegnato il ruolo di approvatore, gli editor non possono creare, distribuire o eliminare GPO. Tuttavia, possono richiedere che i GPO vengano creati, distribuiti o eliminati.

-   **Revisore:** Gli amministratori dei criteri di gruppo assegnati al ruolo revisore possono visualizzare l'elenco dei GPO in un dominio e creare e visualizzare i report delle impostazioni dei criteri in un GPO. A meno che non sia anche assegnato il ruolo di editor, non possono modificare le impostazioni dei criteri in un oggetto Criteri di stato.

Advanced Group Policy Management offre agli amministratori della gestione avanzata la flessibilità di configurare le autorizzazioni a un livello più dettagliato rispetto ai ruoli usando lo snap-in Advanced Group Policy Management. La tabella 2 descrive queste autorizzazioni e indica le autorizzazioni concesse a ogni ruolo per impostazione predefinita.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Autorizzazione</th>
<th align="left">Descrizione</th>
<th align="left">Amministratore della Advanced Group Policy</th>
<th align="left">Responsabile approvazione</th>
<th align="left">Editor</th>
<th align="left">Revisore</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Controllo completo</strong></p></td>
<td align="left"><p>Avere tutte le autorizzazioni.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Creare un oggetto Criteri di stato</strong></p></td>
<td align="left"><p>Creare GPO in un dominio.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Contenuto dell'elenco</strong></p></td>
<td align="left"><p>Elencare i GPO in un dominio.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Impostazioni di lettura</strong></p></td>
<td align="left"><p>Leggere le impostazioni dei criteri in un GPO.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificare le impostazioni</strong></p></td>
<td align="left"><p>Modificare le impostazioni dei criteri in un GPO.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Elimina GPO</strong></p></td>
<td align="left"><p>Eliminare un oggetto Criteri di stato.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificare la sicurezza</strong></p></td>
<td align="left"><p>Delegare l'accesso a livello di dominio, delegare l'accesso a un singolo GPO e delegare l'accesso all'ambiente di produzione.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Distribuire un oggetto Criteri di stato</strong></p></td>
<td align="left"><p>Distribuire un GPO dall'archivio all'ambiente di produzione.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Creare un modello</strong></p></td>
<td align="left"><p>Creare un modello di GPO in Advanced Group Policy Management.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Opzioni di modifica</strong></p></td>
<td align="left"><p>Configurare la notifica tramite posta elettronica Advanced Group Policy e limitare le versioni di GPO archiviate nell'archivio.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Esporta GPO</strong></p></td>
<td align="left"><p>Esportare un oggetto Criteri di stato in un file.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Importa oggetto Criteri di stato</strong></p></td>
<td align="left"><p>Importare un GPO da un file.</p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sì</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Nota** 
 Le autorizzazioni **Esporta** GPO e **Importa GPO** non sono disponibili in advanced Group policy Management 3,0 o 2,5.

La possibilità di delegare l'accesso a GPO nell'ambiente di produzione per un dominio e la possibilità di limitare il numero di versioni degli oggetti Criteri di archiviazione non sono disponibili in Advanced Group Policy Management 2,5.

 

### Riferimenti aggiuntivi

Per informazioni sulle attività che possono essere eseguite dagli amministratori dei criteri di gruppo assegnati a un determinato ruolo o sulle autorizzazioni necessarie per eseguire un'attività specifica, vedere la [Guida alle operazioni per Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=160061).

 

 





