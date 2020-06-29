---
title: Gestione delle impostazioni di configurazione dell'area di lavoro MED-V
description: Gestione delle impostazioni di configurazione dell'area di lavoro MED-V
author: dansimp
ms.assetid: 517d04de-c31f-4b50-b2b3-5f8c312ed37b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97add695f605b71547b564789cce07a1d58763f2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826156"
---
# Gestione delle impostazioni di configurazione dell'area di lavoro MED-V


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 archivia le impostazioni di configurazione nel registro di sistema. Le informazioni che includiamo qui per il registro di sistema possono aiutare a gestire meglio i servizi MED-V.

MED-V usa il percorso di ricerca seguente quando si cercano i valori di impostazioni risultante:

MED-V analizza prima di tutto i criteri del computer.

Se il valore non viene trovato, MED-V analizza il criterio utente.

Se il valore non viene trovato, MED-V cerca nell'hive HKEY \ _LOCAL \ _MACHINE \\System.

Se il valore non viene trovato, MED-V cerca nell'hive del registro di sistema HKEY \ _CURRENT utente.

Se il valore non viene ancora trovato, MED-V utilizzerà l'impostazione predefinita.

Una procedura consigliata generale consiste nell'impostare il valore nell'hive HKEY \ _LOCAL \ _MACHINE \\System o nei criteri del computer. Ma se si vuole che l'utente finale possa configurare una determinata impostazione, è consigliabile lasciarla fuori.

**Nota**  
Prima di distribuire le aree di lavoro MED-V, è possibile usare un editor di script per modificare lo script di Windows PowerShell (file con estensione ps1) creato dal Packager dell'area di lavoro MED-V. Per altre informazioni, vedere [configurazione delle impostazioni avanzate tramite Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

Dopo aver distribuito le aree di lavoro MED-V, è possibile modificare alcune impostazioni di configurazione di MED-V modificando le voci del registro di sistema.



Questa sezione elenca tutte le chiavi del registro di sistema MED-V configurabili e spiega i loro usi.

## Tasto di diagnostica


La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Diagnostics.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati/impostazione predefinita </th>
<th align="left">Descrizione </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EventLogLevel </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 3</p></td>
<td align="left"><p>Tipo di informazioni registrate nel log eventi. I livelli includono i seguenti: 0 (nessuno), 1 (errore), 2 (avviso), 3 (informazioni), 4 (debug).</p></td>
</tr>
</tbody>
</table>



## Tasto FTS


La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\Fts.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Dati/impostazione predefinita</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddUserToAdminGroupEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se la configurazione per la prima volta aggiunge automaticamente l'utente finale al gruppo amministratore&#39;s. 0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: la prima volta che la configurazione non aggiunge automaticamente l'utente finale al gruppo amministratore&#39;s.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vero: la configurazione iniziale aggiunge automaticamente l'utente finale al gruppo Administrator&#39;s.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ComputerNameMask </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>MEDV </p></td>
<td align="left"><p>Maschera nome computer usata per creare la macchina virtuale Guest&#39;il nome del computer s.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>La maschera può contenere un tag% nomeutente% per inserire il nome utente come parte del computer. Analogamente, il tag% hostname% inserisce il nome del computer host.</p>
<p>Ogni &quot; # &quot; carattere della maschera viene sostituito da una cifra casuale. Un carattere asterisco (*) alla fine della maschera viene sostituito da caratteri alfanumerici casuali.</p>
<p>Un numero specifico di caratteri da% hostname% e% nomeutente% può essere acquisito usando parentesi quadre. Ad esempio, &quot; % nomeutente% [3] &quot; utilizzerebbe i primi tre caratteri del nome utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeleteVMStateTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 90</p></td>
<td align="left"><p>Valore di timeout, in secondi, quando la configurazione per la prima volta prova ad eliminare la macchina virtuale. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DetachVfdTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 120</p></td>
<td align="left"><p>Valore di timeout, in secondi, quando la configurazione per la prima volta prova a scollegare il disco floppy virtuale dalla macchina virtuale. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogUrl </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>URL personalizzabile che si collega alla pagina Web interna e viene visualizzato dai messaggi di dialogo configurazione per la prima volta. </p></td>
</tr>
<tr class="odd">
<td align="left"><p>ExplorerTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 900</p></td>
<td align="left"><p>Il valore di timeout, in secondi, che attende l'installazione per la prima volta per Windows Explorer. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FailureDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Il messaggio si trova nel file di risorse </p></td>
<td align="left"><p>Messaggio personalizzabile visualizzato all'utente finale quando non è possibile completare la configurazione per la prima volta.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GiveUserGroupRightsMaxRetryCount </p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 3</p></td>
<td align="left"><p>Numero massimo di volte in cui MED-V cerca di assegnare diritti a un gruppo di utenti finali. Il superamento del valore di tentativo specificato senza la possibilità di assegnare correttamente i diritti di un gruppo di utenti finali causa probabilmente un errore di preparazione della macchina virtuale che viene quindi soggetto al valore MaxRetryCount. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GiveUserGroupRightsTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 300</p></td>
<td align="left"><p>Valore di timeout, in secondi, quando si assegnano i diritti di un gruppo di utenti. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LogFilePaths </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Elenco dei percorsi di file di log raccolti da MED-V durante la configurazione per la prima volta. </p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPostponeTime </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 120</p></td>
<td align="left"><p>Il numero massimo di ore per cui la configurazione per la prima volta può essere rinviata dall'utente finale. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxRetryCount </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 3</p></td>
<td align="left"><p>Numero massimo di tentativi di preparazione di una macchina virtuale da parte di MED-V se ogni tentativo termina in un errore diverso da quello di un software. Quando la preparazione della macchina virtuale non riesce e viene superato il numero di tentativi di configurazione per la prima volta, MED-V informa l'utente finale dell'errore e non dà l'opzione di riprovare. Il conteggio viene reimpostato ogni volta che viene avviato MED-V. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Modalità </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Impostazione predefinita = automatica</p></td>
<td align="left"><p>Configura il modo in cui la configurazione per la prima volta interagisce con l'utente. I valori possibili sono i seguenti:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Partecipato.</strong> L'utente finale deve immettere le informazioni durante la configurazione per la prima volta.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se è stato creato il file Sysprep. inf in modo che la configurazione minima richiedesse l'input dell'utente per il completamento, è necessario selezionare la <strong> modalità assistita </strong> o potrebbero verificarsi problemi durante la configurazione per la prima volta.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Automatica </strong> . La macchina virtuale non viene visualizzata all'utente finale durante la configurazione per la prima volta, ma l'utente finale viene richiesto prima dell'avvio della configurazione iniziale.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Silent </strong> . La macchina virtuale non viene visualizzata all'utente finale durante la configurazione per la prima volta.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NonInteractiveRetryTimeoutInc </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 15</p></td>
<td align="left"><p>Il valore di timeout, in minuti, per la prima volta che la configurazione deve essere completata nella prima configurazione in modalità interattiva durante il tentativo di eseguire nuovamente la configurazione. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NonInteractiveTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 45</p></td>
<td align="left"><p>Il valore di timeout, in minuti, che la prima configurazione deve essere completata nella prima configurazione della modalità interattiva per la prima volta. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PostponeUtcDateTimeLimit </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Data e ora, in formato DateTime UTC, che la configurazione per la prima volta può essere rinviata. Immettere il formato &quot; aaaa-mm-dd HH: mm &quot; con le ore specificate usando lo standard dell'orologio a 24 ore.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RetryDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Il messaggio si trova nel file di risorse </p></td>
<td align="left"><p>Messaggio personalizzabile visualizzato all'utente finale quando la configurazione per la prima volta deve ripetere il tentativo di configurazione.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetComputerNameEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se la voce nomecomputer nella sezione [UserData] del file Sysprep. inf nel guest deve essere aggiornata in base al valore di ComputerNameMask specificato.   0 = false; 1 = vero.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: la voce nomecomputer nel file Sysprep. inf non viene aggiornata in base a ComputerNameMask.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: la voce nomecomputer nel file Sysprep. inf viene aggiornata in base a ComputerNameMask.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetJoinDomainEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se l'impostazione JoinDomain nella sezione [Identification] del file Sysprep. inf nel guest deve essere aggiornata in base alle impostazioni dell'host.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: l'impostazione JoinDomain nel file Sysprep. inf non viene aggiornata in base alle impostazioni dell'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: l'impostazione JoinDomain nel file Sysprep. inf viene aggiornata in base alle impostazioni dell'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetMachineObjectOUEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se l'impostazione MachineObjectOU nella sezione [Identification] del file Sysprep. inf nel guest viene aggiornata in base all'host.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: l'impostazione MachineObjectOU nel file Sysprep. inf non viene aggiornata in base alle impostazioni dell'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: l'impostazione MachineObjectOU nel file Sysprep. inf viene aggiornata in base alle impostazioni dell'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SetRegionalSettingsEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se le impostazioni nella sezione [RegionalSettings] del file Sysprep. inf nel guest vengono aggiornate in base all'host.  0 = false; 1 = vero.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Per impostazione predefinita, l'impostazione per il fuso orario nel Guest è sempre sincronizzata con l'impostazione TimeZone nell'host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: le impostazioni nella sezione [RegionalSettings] del file Sysprep. inf nel guest non vengono aggiornate in base all'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: le impostazioni nella sezione [RegionalSettings] del file Sysprep. inf nel guest vengono aggiornate in base all'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SetUserDataEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se le impostazioni FullName e OrgName nella sezione [UserData] del file Sysprep. inf nel guest vengono aggiornate in base alle impostazioni dell'host.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: le impostazioni FullName e OrgName nel file Sysprep. inf non vengono aggiornate in base alle impostazioni dell'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: le impostazioni FullName e OrgName nel file Sysprep. inf vengono aggiornate in base alle impostazioni dell'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartDialogMsg </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Il messaggio si trova nel file di risorse </p></td>
<td align="left"><p>Messaggio personalizzabile visualizzato all'utente finale quando la configurazione per la prima volta è pronta per iniziare. </p></td>
</tr>
<tr class="even">
<td align="left"><p>TaskCancelTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 30</p></td>
<td align="left"><p>Il valore di timeout, in secondi, che la configurazione per la prima volta attende una risposta dalla macchina virtuale per un'operazione di annullamento. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskVMTurnOffTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 60</p></td>
<td align="left"><p>Il valore di timeout, in secondi, che la prima volta che viene eseguita la configurazione della macchina virtuale si arresta. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="even">
<td align="left"><p>UpgradeTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 600</p></td>
<td align="left"><p>L'ora, in secondi, prima che venga tentato l'aggiornamento del software agente guest MED-V. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
</tbody>
</table>



## Tasto UserExperience


La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\UserExperience e alla chiave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\UserExperience.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Dati/impostazione predefinita</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AppPublishingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se la pubblicazione dell'applicazione dall'ospite all'host è abilitata.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Disabilita la pubblicazione dell'applicazione dall'ospite all'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: consente la pubblicazione dell'applicazione dall'ospite all'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AudioSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se la condivisione del dispositivo di I/O audio tra il Guest e l'host è abilitata.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Disabilita la condivisione del dispositivo di I/O audio tra Guest e host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: consente la condivisione del dispositivo i/O audio tra l'ospite e l'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClipboardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se la condivisione degli Appunti tra l'ospite e l'host è abilitata.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Disabilita la condivisione degli Appunti tra l'ospite e l'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: consente la condivisione degli Appunti tra l'ospite e l'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DialogTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 300</p></td>
<td align="left"><p>L'ora, in secondi, prima della data di inizio della prima configurazione di avvio della finestra di dialogo. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HideVmTimeout</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 30</p></td>
<td align="left"><p>Valore di timeout, in minuti, che la finestra della macchina virtuale a schermo intero è nascosta dall'utente finale durante un tentativo di accesso lungo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LogonStartEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se il guest deve essere avviato quando l'utente finale accede al desktop o quando viene avviata la prima applicazione Guest.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: il Guest viene avviato quando viene avviata la prima applicazione Guest.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vero: l'ospite viene avviato quando l'utente finale accede al desktop.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PrinterSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se la condivisione delle stampanti tra Guest e host è abilitata.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: disattiva la condivisione delle stampanti tra Guest e host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: consente la condivisione di stampanti tra Guest e host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>RebootAbsoluteDelayTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1440</p></td>
<td align="left"><p>Valore di timeout, in minuti, che la prima volta che l'installazione attende un riavvio. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>RedirectUrls </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>Elenco URL specificato</p></td>
<td align="left"><p>Specifica un elenco di URL da reindirizzare dall'host al Guest. </p></td>
</tr>
<tr class="even">
<td align="left"><p>SmartCardLogonEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se le smart card possono essere usate per autenticare gli utenti in MED-V. 0 = false; 1 = vero.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: non consente alle smart card di eseguire l'autenticazione degli utenti finali in MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vero: consente alle smart card di autenticare gli utenti finali in MED-V.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Se SmartCardLogonEnabled e CredentialCacheEnabled sono entrambi abilitati, SmartCardLogonEnabled esegue l'override di CredentialCacheEnabled.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>SmartCardSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se la condivisione delle smart card tra l'ospite e l'host è abilitata.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: Disabilita la condivisione delle smart card tra il Guest e l'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: consente la condivisione di smart card tra l'ospite e l'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>USBDeviceSharingEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se è abilitata la condivisione di dispositivi USB tra Guest e host.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: disattiva la condivisione dei dispositivi USB tra Guest e host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: consente la condivisione di dispositivi USB tra Guest e host.</p></td>
</tr>
</tbody>
</table>



## Chiave VM


La tabella seguente contiene informazioni sui valori del registro di sistema associati alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\VM e alla chiave HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\Medv\\v2\\VM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Tipo</th>
<th align="left">Dati/impostazione predefinita</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CloseAction </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Impostazione predefinita = Hibernate</p></td>
<td align="left"><p>L'azione eseguita dalla macchina virtuale dopo l'ultima applicazione in esecuzione viene chiusa. Questa impostazione viene ignorata se il valore di LogonStartEnabled è abilitato. Le opzioni possibili sono le seguenti:</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Hibernate </strong> . Questa opzione rilascia tutte le risorse fisiche che la macchina virtuale USA, ad esempio memoria e CPU, e salva lo stato di tutte le applicazioni e le operazioni in uso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>ARRESTO </strong> . Questa opzione arresta in modo sicuro il sistema operativo guest e rilascia tutte le risorse fisiche che la macchina virtuale USA, ad esempio memoria e CPU.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>disattivazione </strong> . Questa opzione può causare la perdita di dati perché è la stessa cosa di disattivare il pulsante di alimentazione o estrarre il cavo di alimentazione in un computer fisico. Usare questa opzione solo se non è possibile usare una delle altre due opzioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestMemFromHostMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>378, 512, 1024, 1536, 2048 </p></td>
<td align="left"><p>Un elenco di valori di memoria (MB) per l'ospite. Questo valore viene usato per determinare la quantità di RAM disponibile per l'ospite. In combinazione con HostMemToGuestMem, viene creata una tabella di ricerca per determinare la quantità di RAM da allocare nella macchina virtuale guest. I valori possibili possono essere compresi tra 128 e 3712.</p></td>
</tr>
<tr class="even">
<td align="left"><p>GuestUpdateDuration </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 240</p></td>
<td align="left"><p>Numero di minuti che MED-V deve mantenere l'ospite sveglio per l'aggiornamento automatico, a partire dall'ora specificata nel valore GuestUpdateTime. Intervallo compreso tra 0 e 1440. L'impostazione di questo valore su zero (0) Disabilita la funzionalità di patch Guest.</p>
<p>Per altre informazioni sulle patch Guest per l'aggiornamento automatico, vedere <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestione degli aggiornamenti automatici per le aree di lavoro MED-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GuestUpdateTime </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Impostazione predefinita = 00:00</p></td>
<td align="left"><p>L'ora e il minuto ogni giorno in cui MED-V deve riattivare l'ospite per l'aggiornamento automatico, usando lo standard di 24 ore. Specificare l'ora nel formato HH: MM  </p>
<p>Per altre informazioni sulle patch Guest per l'aggiornamento automatico, vedere <a href="managing-automatic-updates-for-med-v-workspaces.md" data-raw-source="[Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md)"> gestione degli aggiornamenti automatici per le aree di lavoro MED-V </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>HostMemToGuestMem </p></td>
<td align="left"><p>MULTI_SZ</p></td>
<td align="left"><p>1024, 2048, 4096, 8192, 16384 </p></td>
<td align="left"><p>Un elenco di valori di memoria (MB) per il Guest, determinato dalla RAM disponibile nell'host. In combinazione con GuestMemFromHostMem, viene creata una tabella di ricerca per determinare la quantità di RAM da allocare nella macchina virtuale guest. I valori possibili possono essere compresi tra 1024 e 16384.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HostMemToGuestMemCalcEnabled</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 1</p></td>
<td align="left"><p>Configura se la memoria allocata per il Guest viene calcolata dalla memoria presente nell'host.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: la memoria allocata per il Guest non viene calcolata dalla memoria presente nell'host.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = vero: la memoria allocata per il Guest viene calcolata dalla memoria presente nell'host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Memoria </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 512</p></td>
<td align="left"><p>RAM (MB) che deve essere allocata per la macchina virtuale guest. Questa impostazione viene ignorata se l'impostazione HostMemToGuestMemEnabled è abilitata. Intervallo = 128 a 2048.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MultiUserEnabled </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 0</p></td>
<td align="left"><p>Configura se più utenti condividono la stessa area di lavoro MED-V.  0 = false; 1 = vero.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>0 = false: più utenti non condividono la stessa area di lavoro MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>1 = true: più utenti condividono la stessa area di lavoro MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>NetworkingMode </p></td>
<td align="left"><p>SZ</p></td>
<td align="left"><p>Impostazione predefinita = NAT</p></td>
<td align="left"><p>Tipo di connessione di rete usata nell'ospite. I valori possibili sono i seguenti:</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>Bridged </strong> . MED-V ha un proprio indirizzo di rete, in genere ottenuto tramite DHCP.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><strong>NAT </strong> . MED-V USA NAT (Network Address Translation) per condividere il IP dell'host&#39;s per il traffico in uscita.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>TaskTimeout </p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>Impostazione predefinita = 600</p></td>
<td align="left"><p>Un valore di timeout generale, in secondi, in cui MED-V attende che un'attività venga completata, ad esempio il riavvio e la chiusura. Intervallo compreso tra 0 e 2147483647.</p></td>
</tr>
</tbody>
</table>



## Impostazioni del registro di sistema Guest


Questa sezione elenca le chiavi del registro di sistema guest MED-V configurabili e spiega i loro usi.

### V2

La tabella seguente contiene informazioni sul valore del registro di sistema guest associato alla chiave HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Medv\\v2\\.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome </th>
<th align="left">Tipo </th>
<th align="left">Dati/impostazione predefinita </th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>EnableGPWorkarounds</p></td>
<td align="left"><p>DWORD </p></td>
<td align="left"><p>Impostazione predefinita = 1 </p></td>
<td align="left"><p>Configura il modo in cui MED-V gestisce le chiavi BufferPolicyReads e GroupPolicyMinTransferRate.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Per impostazione predefinita, MED-V imposta questi tasti come segue:</p>
<p>BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0.</p>
<p>Creare la chiave EnableGPWorkarounds, se necessario, e impostare la chiave su zero se non si vuole che MED-V modifichi le impostazioni predefinite di BufferPolicyReads e GroupPolicyMinTransferRate.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se l'area di lavoro MED-V è in uso in modalità NAT, EnableGPWorkarounds influisce sulle chiavi del registro di sistema BufferPolicyReads e GroupPolicyMinTransferRate. Se l'area di lavoro MED-V è in modalità BRIDGEd, EnableGPWorkarounds interessa solo la chiave del registro di sistema BufferPolicyReads.</p>
</div>
<div>

</div>
<p>1 = vero: MED-V imposta le chiavi BufferPolicyReads = 1 e GroupPolicyMinTransferRate = 0 (se in uso in modalità NAT) o solo BufferPolicyReads = 1 (se in modalità BRIDGEd).</p>
<p>0 = false: MED-V non apporta alcuna modifica alle chiavi BufferPolicyReads e GroupPolicyMinTransferRate.</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Gestire le applicazioni nell'area di lavoro MED-V](manage-med-v-workspace-applications.md)

[Gestire il reindirizzamento URL in MED-V](manage-med-v-url-redirection.md)

[Gestire le impostazioni dell'area di lavoro MED-V](manage-med-v-workspace-settings.md)









