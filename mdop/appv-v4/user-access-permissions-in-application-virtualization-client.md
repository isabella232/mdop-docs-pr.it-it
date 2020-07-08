---
title: Autorizzazioni di accesso utente in Application Virtualization Client
description: Autorizzazioni di accesso utente in Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815116"
---
# Autorizzazioni di accesso utente in Application Virtualization Client


Nella scheda **autorizzazioni** della finestra di dialogo **Proprietà** , accessibile facendo clic con il pulsante destro del mouse sul nodo **Application Virtualization** in Application Virtualization Client Management Console, gli amministratori possono concedere agli utenti le autorizzazioni per l'utilizzo delle varie funzioni client.

**Nota**  Prima di modificare le autorizzazioni degli utenti, verificare che le modifiche apportate alle autorizzazioni siano coerenti con le linee guida dell'organizzazione per la concessione delle autorizzazioni utente.

 

La tabella seguente elenca e descrive le autorizzazioni che possono essere concesse agli utenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome autorizzazione</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aggiungere applicazioni</p></td>
<td align="left"><p>Registrare nuove applicazioni passando un nuovo file OSD al client usando sfttray.exe, sftmime.exe o MMC.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modificare le dimensioni della cache del file System</p></td>
<td align="left"><p>Aumentare le dimensioni della cache del file System.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cambiare l'unità del file System</p></td>
<td align="left"><p>Selezionare una lettera di unità preferita diversa per il file System.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modificare le impostazioni del log</p></td>
<td align="left"><p>Modificare il livello di log o il percorso del log per il file di log del client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Modificare i file OSD</p></td>
<td align="left"><p>Modificare i file OSD per le applicazioni registrate e passarli al client. Questo non ha alcun effetto sull'aggiornamento della pubblicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cancellare le impostazioni dell'applicazione</p></td>
<td align="left"><p>Eliminare tipi di file, tasti di scelta rapida e qualsiasi configurazione per l'utente corrente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Eliminare le applicazioni</p></td>
<td align="left"><p>Rimuovere tutti i riferimenti a un'applicazione dal file System e dalla cache OSD per tutti gli utenti del computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Importare applicazioni nella cache</p></td>
<td align="left"><p>Caricare i dati dell'applicazione direttamente da un file SFT specificato nella cache del file System. Questo problema interessa tutti gli utenti.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Caricare le applicazioni nella cache</p></td>
<td align="left"><p>Avviare un caricamento del file SFT per un'applicazione dall'origine configurata, ad esempio un App-V Streaming Server. In questo articolo viene caricata l'applicazione per tutti gli utenti del computer.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Bloccare e sbloccare le applicazioni nella cache</p></td>
<td align="left"><p>Impedire o consentire la scaricamento delle applicazioni dalla cache del file System. Questo problema interessa tutti gli utenti del computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestire le associazioni di tipi di file</p></td>
<td align="left"><p>Aggiungere, modificare o eliminare associazioni di tipi di file solo per l'utente corrente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestire le impostazioni di aggiornamento della pubblicazione</p></td>
<td align="left"><p>Modificare le impostazioni che controllano l'intervallo di pubblicazione degli aggiornamenti per tutti gli utenti del computer.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestire i server di pubblicazione</p></td>
<td align="left"><p>Aggiungere, modificare o eliminare i server di pubblicazione per tutti gli utenti del computer. Questa autorizzazione include implicitamente le autorizzazioni per la gestione delle impostazioni di aggiornamento della pubblicazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pubblicare i tasti di scelta rapida</p></td>
<td align="left"><p>Creare nuovi collegamenti alle applicazioni registrate. L'utente deve anche avere l'autorizzazione per creare file nel file system locale.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ripristinare le applicazioni</p></td>
<td align="left"><p>Rimuovere le configurazioni specifiche dell'applicazione per l'utente corrente senza rimuovere i collegamenti o le associazioni di tipi di file.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Avviare un aggiornamento della pubblicazione</p></td>
<td align="left"><p>Avviare un aggiornamento della pubblicazione non pianificato per l'utente corrente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Attivare o disattivare la modalità offline</p></td>
<td align="left"><p>Cambiare l'intero client dalla modalità online a quella offline per tutti gli utenti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scaricare le applicazioni dalla cache</p></td>
<td align="left"><p>Cancellare i dati dell'applicazione dalla cache del file System per tutti gli utenti senza rimuovere le impostazioni specifiche per l'utente, i collegamenti o le associazioni di tipi di file.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Visualizzare tutte le applicazioni</p></td>
<td align="left"><p>Consentire all'utente di visualizzare le applicazioni virtuali per tutti gli utenti registrati nel computer.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Come modificare le autorizzazioni di accesso utente](how-to-change-user-access-permissions.md)

 

 





