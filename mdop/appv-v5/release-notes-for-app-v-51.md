---
title: Note sulla versione per App-V 5.1
description: Note sulla versione per App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804881"
---
# Note sulla versione per App-V 5.1


Di seguito sono riportati i problemi noti di Microsoft Application Virtualization (App-V) 5,1.

## Si verifica un errore durante l'aggiornamento della pubblicazione tra App-V 5,0 SP3 Management Server e client App-V 5,1 in Windows 10


Quando si sincronizzano i pacchetti dal server di gestione SP3 App-V 5,0 a un client App-V 5,1 in Windows 10, viene generato un errore durante l'aggiornamento della pubblicazione. Questo errore si verifica perché il server App-V 5,0 SP3 non comprende il sistema operativo Windows 10 specificato nell'URL di pubblicazione. Il problema è risolto per il server di pubblicazione App-V 5,1, ma non viene convertito in versioni di App-V 5,0 SP3 o versione precedente.

**Soluzione alternativa**: aggiornare il server di gestione di App-v 5,0 al server di gestione di App-v 5,1 per i client Windows 10.

## Le configurazioni personalizzate non vengono applicate per i pacchetti che verranno pubblicati globalmente se impostati tramite il server App-V 5,1


Se si assegna un pacchetto a un gruppo di annunci che contiene gli account del computer e si applica una configurazione personalizzata a tale gruppo usando App-V Server, la configurazione personalizzata non verrà applicata a tali computer. Il client App-V 5,1 pubblicherà i pacchetti assegnati a un account del computer a livello globale. Tuttavia, archivia i file di configurazione personalizzati per ogni utente nel profilo di ogni utente. I pacchetti pubblicati globalmente non avranno accesso a questa configurazione personalizzata.

**Soluzione alternativa**: eseguire una delle operazioni seguenti:

-   Assegnare il pacchetto ai gruppi che contengono solo gli account utente. In questo modo, la configurazione personalizzata del pacchetto verrà archiviata nel profilo di ogni utente e verrà applicata correttamente.

-   Creare un file di configurazione della distribuzione personalizzato e applicarlo al pacchetto nel client usando il cmdlet Add-AppvClientPackage con il parametro – DynamicDeploymentConfiguration. Per altre informazioni, vedere [informazioni sulla configurazione dinamica di App-V 5,1](about-app-v-51-dynamic-configuration.md) .

-   Creare un nuovo pacchetto con la configurazione personalizzata usando l'App-V 5,1 Sequencer.

## File del server non eliminati dopo l'installazione del nuovo App-V 5,1 server


Se si disinstalla il server App-V 5,0 SP1 e quindi si installa il server App-V 5,1, l'installazione non riesce, viene installata la versione errata del server di gestione e viene restituito un messaggio di errore. Il problema si verifica perché i file del server non vengono eliminati quando si disinstalla l'App-V 5,0 SP1, quindi il processo di installazione esegue un aggiornamento anziché una nuova installazione.

**Soluzione alternativa**: eliminare la chiave del registro di sistema prima di iniziare l'installazione di App-V 5,1:

In HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall individuare ed eliminare la chiave GUID di installazione che contiene il valore DWORD "DisplayName" con i dati di valore "Microsoft Application Virtualization (App-V) Server". Questa è l'unica chiave che deve essere eliminata.

## Le associazioni di tipi di file aggiunte manualmente non vengono salvate correttamente


Le associazioni di tipi di file aggiunte manualmente a un pacchetto dell'applicazione con i tasti di scelta rapida e la scheda accordi alla fine della procedura guidata di aggiornamento delle applicazioni non vengono salvate correttamente. Non saranno disponibili per il client App-V o per il sequencer durante l'aggiornamento del pacchetto salvato.

**Soluzione alternativa**: per aggiungere un'associazione di tipi di file, aprire il pacchetto per la modifica ed eseguire la procedura guidata di aggiornamento. Durante il passaggio di installazione, aggiungere la nuova associazione del tipo di file tramite il sistema operativo. Il sequencer rileverà la nuova associazione nel registro di sistema e la aggiungerà al registro virtuale del pacchetto, dove sarà disponibile per il client.

## Quando si esegue lo streaming di pacchetti nella modalità SCS (Shared Content Store) a un client gestito anche da AppLocker, nel disco locale vengono scritti dati aggiuntivi.


Per ridurre la quantità di dati scritti nel disco locale di un client, è possibile abilitare la modalità SCS nel client App-V 5,1 per trasmettere il contenuto di un pacchetto su richiesta. Tuttavia, se AppLocker gestisce un'applicazione all'interno del pacchetto, alcuni dati potrebbero essere scritti nel disco locale del client che altrimenti non verranno scritti.

**Soluzione alternativa**: None

## Nella finestra di dialogo Aggiungi pacchetto della console di gestione il pulsante Sfoglia non è disponibile quando si usa Chrome o Firefox


Nella pagina pacchetti della console di gestione, se si fa clic su **Aggiungi o aggiorna** nell'angolo in basso a destra, viene visualizzata la finestra di dialogo **Aggiungi pacchetto** . Se si accede alla console di gestione usando Chrome o Firefox come browser, non sarà possibile passare alla posizione del pacchetto.

**Soluzione alternativa**: digitare o copiare e incollare il percorso del pacchetto nel campo **Aggiungi pacchetto** di input. Se la console di gestione ha accesso a questo percorso, sarà possibile aggiungere il pacchetto. Se il pacchetto si trova in una condivisione di rete, è possibile passare alla posizione usando Esplora file eseguendo questa procedura:

1.  Tenendo premuto **MAIUSC**, fare clic con il pulsante destro del mouse sul file del pacchetto

2.  Selezionare **copia come percorso**

3.  Incollare il percorso nel campo di input della finestra di dialogo **Aggiungi pacchetto**

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a>L'aggiornamento di App-V Management Server a 5,1 talvolta non riesce con il messaggio "si è verificato un errore di database"


Se si installa il server di gestione SP1 App-V 5,0 e quindi si prova a eseguire l'aggiornamento a App-V 5,1 server quando più gruppi di connessioni sono configurati e abilitati, viene visualizzato l'errore seguente: "si è verificato un errore di database. Motivo: "nome di colonna non valido" PackageOptional ". Nome di colonna non valido "VersionOptional". "

**Soluzione alternativa**: eseguire questo comando nel database SQL:

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

dove "AppVManagement" è il nome del database.

## Gli utenti non possono aprire un pacchetto in un gruppo di connessioni pubblicato dall'utente se si aggiunge o si rimuove un pacchetto facoltativo


Negli ambienti in cui è in uso il client RDS o con più utenti simultanei per ogni computer, gli utenti connessi non possono aprire applicazioni in pacchetti che si trovano in un gruppo di connessioni pubblicato dall'utente se un pacchetto facoltativo viene aggiunto o rimosso dal gruppo di connessioni.

**Soluzione alternativa**: gli utenti disconnettersi e quindi eseguire il log-in.

## Il messaggio di errore viene visualizzato erroneamente quando il gruppo di connessioni viene pubblicato solo per l'utente


Quando si esegue Repair-AppvClientConnectionGroup, viene visualizzato il messaggio di errore seguente, anche quando il gruppo di connessioni viene pubblicato solo all'utente: "Internal App-V Integration Error: pacchetto non integrato per l'utente. Assicurati che il pacchetto venga aggiunto al computer e pubblicato nell'utente. "

**Soluzione alternativa**: eseguire una delle operazioni seguenti:

-   Pubblicare tutti i pacchetti in un gruppo di connessioni.

    Il problema si verifica quando il gruppo di connessioni da riparare contiene pacchetti mancanti o non disponibili per l'utente, ovvero non pubblicati a livello globale o per l'utente. Tuttavia, il ripristino funzionerà se sono disponibili tutti i pacchetti del gruppo di connessioni, quindi assicurati che tutti i pacchetti vengano pubblicati.

-   Ripristinare i pacchetti singolarmente usando il comando Repair-AppvClientPackage invece del comando Repair-AppvClientConnectionGroup.

    Determinare i pacchetti disponibili per gli utenti e quindi eseguire il comando Repair-AppvClientPackage una volta per ogni pacchetto. Usare i cmdlet di PowerShell per eseguire le operazioni seguenti:

    1.  Ottenere tutti i pacchetti in un gruppo di connessioni.

    2.  Verificare se ogni pacchetto è attualmente pubblicato.

    3.  Se il pacchetto è attualmente pubblicato, eseguire Repair-AppvClientPackage su tale pacchetto.

## Icone non visualizzate correttamente in sequencer


Le icone nella scheda associazioni e tipi di file non vengono visualizzate correttamente quando si modifica un pacchetto in App-V Sequencer. Questo problema si verifica quando le dimensioni delle icone non sono 16x16 o 32x32.

**Soluzione alternativa**: usare solo le icone 16x16 o 32x32.

## Lo script InsertVersionInfo. SQL non è più necessario per il database di gestione


Lo script InsertVersionInfo. SQL non è necessario per le versioni del database di gestione di App-V più avanti rispetto all'App-V 5,0 SP3.

Lo script Permissions. SQL deve essere aggiornato in base al **passaggio 2** nell' [articolo 3031340 della KB](https://support.microsoft.com/kb/3031340).

**Importante** 
 Il **passaggio 1** non è necessario per le versioni di App-v successive all'app-v 5,0 SP3.

 

## Microsoft Visual Studio 2012 non è supportato


App-V 5,1 non supporta Visual Studio 2012.

**Soluzione alternativa**: None

## Limitazioni del nome del file dell'applicazione per il sequencer App-V 5. x


Il sequencer App-V 5. x non può sequenziare le applicazioni con nomi di file corrispondenti "CO_ &lt; x &gt; " dove x è un numero qualsiasi. Verrà generato l'errore 0x8007139F.

**Soluzione alternativa**: usare un nome di file diverso

## Errore "file non trovato" intermittente durante il montaggio di un pacchetto


Occasionalmente, quando si monta un pacchetto, viene generato un errore "file non trovato" (0x80070002). In genere, questo problema si verifica quando una cartella in un pacchetto di App-V contiene molti file (ad esempio 20.000 o più). In questo modo, il flusso può richiedere più tempo del previsto e il timeout genera l'errore "file non trovato".

**Soluzione alternativa**: a partire da HF06, è stata introdotta una nuova chiave del registro di sistema per consentire l'estensione del periodo di timeout.

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left">Percorso</td>
<td align="left">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</td>
</tr>
<tr>
<td align="left">Impostazione</td>
<td align="left">StreamResponseWaitTimeout</td>
</tr>
<tr>
<td align="left">TipoDati</td>
<td align="left">DWORD</td>
</tr>
<tr>
<td align="left">Unità</td>
<td align="left">Secondi</td>
</tr>
<tr>
<td align="left">Default</td>
<td align="left">5<br />
<strong>Nota </strong> : questo valore è l'impostazione predefinita se la chiave del registro di sistema non è definita o &lt; viene specificato un valore = 5.
</td>
</tr>
</tbody>
</table>






## Argomenti correlati


[Informazioni su App-V 5.1](about-app-v-51.md)

 

 





