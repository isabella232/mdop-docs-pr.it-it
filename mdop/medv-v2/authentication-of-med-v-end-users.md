---
title: Autenticazione degli utenti finali MED-V
description: Autenticazione degli utenti finali MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824886"
---
# Autenticazione degli utenti finali MED-V


L'autenticazione degli utenti finali di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 è un problema di sicurezza molto importante. In questo contesto, l'autenticazione fa riferimento alla verifica dell'identità dell'utente finale MED-V.

La sezione seguente contiene informazioni e indicazioni sull'autenticazione degli utenti finali in MED-V.

## Autenticazione utente in MED-V


L'autenticazione in MED-V si verifica in genere a due livelli: quando un utente accede prima a MED-V e ogni volta che cambia la password.

A seconda di come sono state configurate le impostazioni di MED-V per l'autenticazione, l'utente finale viene in genere richiesto ad un certo punto per immettere la propria password, ovvero la prima volta che viene avviato MED-V o la prima volta che provano ad aprire un'applicazione pubblicata.

Esistono diversi aspetti dell'autenticazione dell'utente finale che è possibile controllare, inclusi i seguenti:

Se le credenziali immessi dall'utente finale sono archiviate in Gestione credenziali

In che modo viene presentato l'utente finale con l'opzione di immissione e salvataggio della password

In base al processo preferito della società per la gestione dell'autenticazione degli utenti finali, è possibile specificare se si verifica la memorizzazione delle credenziali per una specifica area di lavoro MED-V. La memorizzazione nella cache delle credenziali di un utente finale è utile perché viene richiesto solo una volta per la password. Se l'utente finale non è autorizzato a salvare la password o decide di non farlo, ogni volta che avvia una nuova sessione MED-V, deve immetterla di nuovo. Ad esempio, se MED-V è configurato per l'avvio quando l'utente finale accede all'host ma l'autenticazione è disabilitata, l'utente finale viene richiesto solo una volta durante l'accesso. In questo caso, le credenziali sono valide finché l'utente finale non si disconnette dall'host.

Se necessario, è possibile usare Gestione credenziali per rimuovere eventuali credenziali degli utenti finali archiviate.

Per impostazione predefinita, l'archiviazione delle credenziali è disabilitata, ma è possibile modificare questa impostazione con uno dei metodi seguenti:

**Durante la creazione del pacchetto area di lavoro MED-V**. Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).

**Dopo aver distribuito l'area di lavoro MED-V**. Modificare il parametro UxCredentialCacheEnabled del cmdlet MED-V per impostare la chiave del registro di sistema Servizi terminal. Per altre informazioni, vedere Guida di Windows PowerShell.

Dopo la distribuzione dell'area di lavoro MED-V, è possibile impostare la preferenza per l'autenticazione dell'utente finale modificando il criterio Servizi terminal denominato DisablePasswordSaving. DisablePasswordSaving controlla se la casella di controllo salvataggio password viene visualizzata nella finestra di dialogo client RDP e se viene visualizzata la richiesta di credenziale MED-V.

Di seguito è riportato il percorso dei criteri per il criterio Servizi terminal denominato DisablePasswordSaving.

**Regedit**

HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving

**Nota**  
Le modifiche apportate a DisablePasswordSaving influenzano solo il prompt RDP in una macchina virtuale.



La tabella seguente elenca i diversi modi in cui è possibile configurare le impostazioni per l'archiviazione delle credenziali e gli effetti delle diverse configurazioni:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Configurazione</th>
<th align="left">Risultato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Disabilitato</strong></p></td>
<td align="left"><p>Viene presentato il prompt di MED-V e una casella di controllo accetta è disponibile e deselezionata. Se l'utente finale seleziona la casella di controllo, le credenziali vengono memorizzate nella cache per un uso successivo. L'utente finale ha anche il vantaggio di essere richiesto solo quando la password scade.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Se l'utente finale non seleziona la casella di controllo, viene visualizzata la richiesta client di connessione Desktop remoto (RDC) al posto del prompt di MED-V e la casella di controllo accetta è deselezionata. Se l'utente finale seleziona la casella di controllo, la credenziale del client RDC viene archiviata per un uso successivo.</p>
<div class="alert">
<strong>Importante</strong><br/><p>RDC non convalida le credenziali quando l'utente finale li immette. Se l'utente finale memorizza nella cache le credenziali tramite il prompt della tecnologia RDC, esiste il rischio che vengano archiviate credenziali non corrette. In questo caso, le credenziali non corrette devono essere eliminate in Gestione credenziali di Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Abilitato</strong></p></td>
<td align="left"><div class="alert">
<strong>Nota</strong><br/><p>Questa configurazione è più sicura perché non consente la memorizzazione nella cache delle credenziali degli utenti finali.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Per impostazione predefinita, l'installazione di MED-V imposta una chiave del registro di sistema nel guest per eliminare il prompt "password che sta per scadere". L'utente finale viene richiesto solo per la modifica di una password nell'host. Le credenziali aggiornate nell'host vengono passate al Guest.

**Attenzione**  
Se si usano criteri di gruppo nell'ambiente, verificare che sia possibile eseguire l'override della chiave del registro di sistema causando la ricomparsa delle richieste di password da parte del Guest.



### Problemi di sicurezza con l'autenticazione

Anche se la memorizzazione nella cache delle credenziali dell'utente finale offre la migliore esperienza utente, è necessario essere consapevoli dei rischi.

Quando la cache delle credenziali è abilitata, le credenziali di dominio dell'utente finale vengono archiviate in un formato reversibile all'interno di Windows Credential Manager. Di conseguenza, un utente malintenzionato potrebbe scrivere uno strumento che viene eseguito sia come processo a livello di sistema che come processo utente finale e che recupera le credenziali dell'utente finale. Puoi ridurre questo rischio solo impostando DisablePasswordSaving su **Enabled**.

Questa stessa preoccupazione esiste quando l'autenticazione MED-V è disabilitata, ma l'impostazione dei criteri Servizi terminal è abilitata.

## Argomenti correlati


[Procedure consigliate per le operazioni MED-V](security-best-practices-for-med-v-operations.md)









