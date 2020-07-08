---
title: Risoluzione dei problemi di MED-V
description: Risoluzione dei problemi di MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825865"
---
# Risoluzione dei problemi di MED-V


Questa sezione contiene informazioni utili per risolvere i problemi generali di Microsoft Enterprise Desktop Virtualization (MED-V).

## Se si modifica la risoluzione dell'host e quindi si massimizza l'area di lavoro MED-V, il desktop viene visualizzato in nero


Quando si lavora in modalità desktop completo, se si modifica la risoluzione dell'host e quindi si ingrandisce la finestra dell'area di lavoro MED-V, il desktop viene visualizzato in nero e l'area di lavoro MED-V potrebbe non rispondere.

### Soluzione

Arrestare e quindi avviare l'area di lavoro MED-V.

## L'avvio di un'area di lavoro MED-V con una scheda di rete è disabilitata e in seguito l'abilitazione della scheda non ripristina la connettività di rete


Se si configura un'area di lavoro MED-V in modalità Bridge e quindi si avvia l'area di lavoro MED-V mentre una scheda di rete è disabilitata, se l'adapter viene abilitato in seguito, la connettività di rete tramite tale adapter non viene ripristinata.

### Soluzione

Arrestare e quindi avviare l'area di lavoro MED-V.

## Un'immagine può essere usata da un solo utente Windows per computer


Un'immagine dell'area di lavoro MED-V può essere usata solo dall'utente di Windows che ha scaricato o importato l'immagine. Questo utente è l'unico utente a parte gli amministratori che hanno le autorizzazioni per la cartella in cui si trovano le immagini scaricate.

### Soluzione

Modificare manualmente l'elenco di controllo di accesso (ACL) nell'archivio immagini.

## Durante l'installazione di MED-V tramite Configuration Manager con i diritti degli utenti abilitati, la disinstallazione non riesce


Se MED-V viene installato con Microsoft System Center Configuration Manager e la modalità di esecuzione del pacchetto è impostata su diritti degli utenti, la disinstallazione non riesce con un messaggio di errore che indica che solo gli utenti amministrativi possono disinstallare MED-V.

### Soluzione

Quando si crea un pacchetto di Configuration Manager per MED-V, impostare la modalità di esecuzione su diritti amministrativi.

## Quando si installa MED-V usando un sistema di distribuzione aziendale, in cui l'installazione è configurata per l'esecuzione del client dopo l'installazione, non è possibile eseguire il client


Se MED-V viene installato usando un sistema di distribuzione aziendale e il pacchetto di installazione è configurato per l'esecuzione del client MED-V dopo l'installazione, dopo che il client è in esecuzione con l'account di sistema, non è possibile vedere che il client è in esecuzione (eccetto nell'area di notifica) e non è possibile interagire con esso.

### Soluzione

Quando si installa MED-V usando un sistema di distribuzione aziendale, usare il parametro *Start \ _MEDV = 0* . msi.

## Impossibile avviare l'immagine di test MED-V


Se un'immagine di test MED-V non viene avviata, non si recupererà mai e tutti gli avvii futuri non riusciranno con il messaggio di errore "Impossibile caricare GINA".

### Soluzione

Elimina l'immagine di test esistente e quindi ricreala di nuovo.

## Dopo aver tentato di partecipare a un dominio con le credenziali errate, l'immagine non riesce mai a partecipare al dominio


Se è presente un errore di configurazione nel blocco predefinito di join Domain, che fa parte dello script di configurazione iniziale della macchina virtuale, l'area di lavoro MED-V non riesce quando si tenta di partecipare a un dominio. Dopo il corretto errore di configurazione, l'immagine inclusa nell'area di lavoro MED-V non può accedere al dominio.

### Soluzione

Se l'immagine è stata distribuita, ridistribuire l'immagine. Se l'immagine è un'immagine di test, ricrea l'immagine.

## MED-V non supporta più monitor


MED-V non supporta la visualizzazione delle applicazioni pubblicate su più monitor. Le applicazioni pubblicate e altre finestre client potrebbero essere visualizzate nella schermata sbagliata e, a volte, dopo la disconnessione di una schermata, MED-V tenterà di inviare lo schermo al monitor in modo che il monitor connesso venga visualizzato in bianco.

### Soluzione

Scollegare la schermata aggiuntiva e riavviare il client.

## Impossibile avviare l'area di lavoro MED-V se l'host si arresta in modo anomalo durante l'avvio dell'area di lavoro MED V


Se l'host si arresta in modo anomalo durante il processo di avvio dell'area di lavoro MED-V e viene visualizzato un messaggio di errore che indica che l'elemento radice non è presente, l'area di lavoro MED-V potrebbe aggiungere dati a un file di configurazione della macchina virtuale (VMC) vuoto, in modo che il processo di avvio non riesca.

### Soluzione

Sostituire il file VMC vuoto con un file VMC dall'immagine di base.

## La tastiera non risponde nelle finestre delle applicazioni pubblicate


In un'area di lavoro MED-V, se si preme il tasto Windows quando un'applicazione pubblicata è in stato attivo, la tastiera non risponde più nelle finestre delle applicazioni pubblicate.

### Soluzione

Premere il tasto Windows mentre è attiva un'applicazione pubblicata.

## Un'area di lavoro Domain MED-V non aggiorna le credenziali di dominio


Quando si usa un'area di lavoro MED-V persistente in un ambiente di dominio, se si modifica la password del dominio, il client MED-V non aggiorna le credenziali del dominio dell'area di lavoro MED-V. Quando un'applicazione pubblicata cerca di accedere a una risorsa di rete, viene visualizzato un messaggio di errore che informa che le credenziali sono scadute.

### Soluzione

Riavviare il sistema operativo di area di lavoro MED-V.

## Le finestre delle applicazioni pubblicate ingrandite coprono la barra delle applicazioni host


Se si massimizza una finestra dell'applicazione pubblicata a schermo intero, potrebbe essere relativa alla barra delle applicazioni dell'host.

### Soluzione

Effettua una delle seguenti operazioni:

Ridurre a icona la finestra dell'applicazione pubblicata per ottenere l'accesso all'area di notifica e riavviare lo spazio di lavoro MED-V.

Ridurre a icona la finestra dell'applicazione pubblicata e quindi ripristinare lo stato ingrandito della finestra.

## L'aggiunta di utenti o gruppi in Gestione configurazione server MED-V non funziona


Quando si aggiungono utenti o gruppi nella finestra di dialogo **Seleziona utenti o gruppi** , gli utenti o i gruppi selezionati non vengono aggiunti all'elenco di controllo di Access in Gestione configurazione server MED-V.

### Soluzione

Aggiungere utenti o gruppi tramite la finestra di dialogo **Immetti nomi utente o di gruppo** . Per informazioni dettagliate, vedere [come installare e configurare il componente server MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).

## MED-V non funziona nei computer con Windows Virtual PC per Windows 7 installato


MED-V richiede Windows Virtual PC2007. Non è possibile installare Windows Virtual PC per Windows7 e Virtual PC2007 SP1 nello stesso computer.

### Soluzione

Disinstallare Virtual PC per Windows7 prima di installare Virtual PC2007 SP1 e MED-V.

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a>MED-V non supporta le immagini di Virtual PC e modalità WindowsXP


MED-V 1.0 SP1 non supporta le immagini create da Windows Virtual PC per Windows7. Se si usa un'immagine PC virtuale per Windows7, il client non riesce durante l'avvio.

### Soluzione

Creare immagini MED-V tramite Virtual PC2007 SP1.

## Windows Firewall blocca l'attività di rete Virtual PC2007 SP1


Per impostazione predefinita, Windows Firewall blocca l'attività di rete Virtual PC2007 SP1 e, quando si avvia Virtual PC2007 SP1 nel computer client, viene visualizzato un messaggio di firewall che blocca la sequenza di avvio e tutto l'accesso alla rete.

### Soluzione

Aggiornare l'eccezione del firewall usando criteri di gruppo prima che l'utente finale usi MED-V.

## Quando si aggiorna il client viene visualizzato un messaggio di errore


Quando si esegue l'aggiornamento del client da MED-V 1.0 a MED-V 1.0 SP1, potrebbe essere visualizzato un messaggio che informa che non è stata definita alcuna area di lavoro MED-V.

### Soluzione

Chiudere il client e riavviarlo.

## Argomenti correlati


[Note sulla versione di MED-V 1.0](med-v-10-release-notesmedv-10.md)

[Note sulla versione di MED-V 1.0 SP1 e SP2](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





