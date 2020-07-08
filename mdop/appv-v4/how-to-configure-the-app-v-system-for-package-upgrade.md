---
title: Come configurare il sistema App-V per l'aggiornamento del pacchetto
description: Come configurare il sistema App-V per l'aggiornamento del pacchetto
author: dansimp
ms.assetid: de133898-f887-46c1-9bc9-fbb03feac66a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5056f923c61aff39d9bd6e1d26f071177f7c12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817846"
---
# Come configurare il sistema App-V per l'aggiornamento del pacchetto


Quando si distribuisce una nuova versione di un pacchetto di applicazione esistente che è stato aggiornato in App-V Sequencer, è possibile distribuirlo in modo che i client App-V riflussino automaticamente la nuova versione nella cache locale. A seconda della soluzione di flusso che si usa, sono disponibili diverse procedure per la configurazione dell'aggiornamento del pacchetto. Le sezioni seguenti descrivono gli scenari più comuni per la pubblicazione e lo streaming e includono le procedure necessarie per configurare l'aggiornamento del pacchetto per ogni scenario.

## Uso di un server di gestione per la pubblicazione e lo streaming


In questo scenario, viene usato un singolo server di gestione di App-V per la pubblicazione e lo streaming di pacchetti e applicazioni e il protocollo RTSP (S) è obbligatorio. Quando il pacchetto originale viene importato in App-V Management Server, l'amministratore copia la cartella del pacchetto contenente i file creati dal sequencer nella cartella contenuto, ad esempio in \\\\server\\CONTENT\\packagename. L'amministratore modifica anche la voce HREF nel file OSD per posizionare il puntatore del file SFT nella cartella del pacchetto e quindi importa il pacchetto nel server.

Quando un utente viene autenticato dal server di gestione, il server pubblica le applicazioni dell'utente inviando il file applist.xml al client. Il client recupera quindi i file OSD e le icone per le applicazioni dal server di gestione. Quando l'utente fa doppio clic sull'icona di un'applicazione, il contenuto dell'applicazione viene trasmesso alla cache del client dal percorso specificato nel file OSD e l'applicazione viene avviata.

### Per aggiornare il pacchetto

Per aggiungere una nuova versione di un'applicazione aggiornata in App-V Sequencer, l'amministratore deve copiare il nuovo file SFT e gli eventuali altri file modificati nella stessa cartella della versione originale dell'applicazione. L'amministratore utilizzerà quindi **Aggiungi versione** nella console di gestione server per aggiungere la nuova versione del pacchetto.

Quando l'utente avvia l'applicazione, il server trasmette automaticamente la nuova versione al client. Questo metodo specifico per l'aggiornamento di un pacchetto era in precedenza noto come aggiornamento attivo.

## Uso di un server di gestione per la pubblicazione e di un server di flusso per lo streaming


In questo scenario, il server di gestione di App-V viene usato per la pubblicazione dei pacchetti e il server di streaming viene usato per i pacchetti e le applicazioni in streaming. È necessario il protocollo RTSP (S). Quando il pacchetto originale viene importato nel server di gestione, l'amministratore copia la cartella del pacchetto contenente i file creati dal sequencer nella cartella contenuto, ad esempio in \\\\server\\CONTENT\\packagename. L'amministratore modifica la voce HREF nel file OSD per posizionare il puntatore del file SFT nel server di flusso e quindi importa il pacchetto nel server di gestione.

Per configurare il server di flusso, l'amministratore copia la cartella del pacchetto dal server di gestione alla cartella contenuto nel server di flusso. Questa cartella deve avere lo stesso nome e il relativo percorso nella cartella contenuto del server di flusso come nel server di gestione, ad esempio \\\\streamingserver\\CONTENT\\packagename.

Se l'impostazione radice dell'origine dell'applicazione del client (ASR) è configurata in base al server di flusso, il client utilizzerà questa impostazione anziché il nome del server nella voce HREF nel file OSD. I campi ISR e PPR del client possono essere facoltativamente configurati in modo che puntino al server di gestione o al server di streaming, a seconda dell'architettura di sistema specifica usata.

Quando un utente viene autenticato dal server di gestione, il server pubblica le applicazioni dell'utente inviando il file applist.xml al client. Il client recupera i file OSD e le icone per le applicazioni dal server di flusso o dal server di gestione, a seconda delle impostazioni dei campi PPR e ISR.

Quando l'utente fa doppio clic sull'icona di un'applicazione, il client usa il percorso del file di contenuto del pacchetto (SFT) contenuto nell'elemento HREF del file OSD. Se l'ASR viene usato, il client sostituisce il nome del server (e la porta e il protocollo, se usato) nell'elemento HREF con il percorso del server di flusso specificato nell'ASR. L'applicazione viene quindi trasmessa dal server di flusso alla cache del client e viene avviata.

### Per aggiornare il pacchetto

Per aggiungere una nuova versione di un'applicazione aggiornata in App-V Sequencer, l'amministratore deve copiare la nuova versione del file SFT e gli eventuali altri file modificati nella stessa cartella della versione originale dell'applicazione nel server di flusso.

Per coerenza, è consigliabile copiare i nuovi file nella cartella anche nel server di gestione. In particolare, se si usano i campi PPR o ISR del client, copiare il file OSD e le icone aggiornati nel server specificato nei campi PPR e ISR.

Dopo che il server di flusso ha rilevato la nuova versione, la volta successiva che l'utente avvia l'applicazione, il server trasmette automaticamente la nuova versione al client.

## Uso di un server di gestione per la pubblicazione e di un server IIS per lo streaming


In questo scenario, il server di gestione di App-V viene usato per la pubblicazione dei pacchetti e il server IIS viene usato per i pacchetti e le applicazioni in streaming. Quando il pacchetto originale viene importato nel server di gestione, l'amministratore copia la cartella del pacchetto contenente i file creati dal sequencer nella cartella contenuto, ad esempio in \\\\server\\CONTENT\\packagename. L'amministratore modifica la voce HREF nel file OSD in modo che punti al file SFT nel server IIS e quindi importi il pacchetto nel server di gestione.

Per configurare il server IIS per il flusso, l'amministratore copia la cartella del pacchetto dal server di gestione alla cartella contenuto nel server IIS. Questa cartella deve avere lo stesso nome e il relativo percorso nella cartella di contenuto Web del server IIS come nel server di gestione; ad esempio, è possibile accedere all'URL del server IIS usando http://IISserver/CONTENT/packagename o https://IISserver/CONTENT/packagename .

Se l'impostazione radice dell'origine dell'applicazione del client (ASR) è configurata in base al server IIS, il client usa l'ASR anziché il nome del server nella voce HREF nel file OSD. Puoi facoltativamente configurare i campi ISR e PPR nel client in modo che puntino al server di gestione o al server IIS, a seconda dell'architettura di sistema specifica che usi.

Quando il server di gestione autentica l'utente, il server pubblica le applicazioni dell'utente inviando il file applist.xml al client. Il client recupera i file OSD e le icone per le applicazioni dal server IIS o dal server di gestione, a seconda delle impostazioni dei campi ISR e PPR.

Quando l'utente fa doppio clic sull'icona di un'applicazione, il client usa il percorso del file di contenuto del pacchetto (SFT) contenuto nell'elemento HREF del file OSD. Se l'ASR viene usato, il client sostituisce il nome del server (e la porta e il protocollo, se usato) nell'elemento HREF con il percorso del server IIS specificato nell'ASR. L'applicazione viene quindi trasmessa dal server IIS alla cache client tramite il protocollo HTTP (S) e viene avviata.

### Per aggiornare il pacchetto

La procedura per l'aggiornamento del pacchetto è la seguente:

-   Copiare la nuova versione del file OSD nella cartella della versione originale nella cartella contenuto del server di gestione, ad esempio \\\\server\\CONTENT\\packagename, e sostituire il file OSD esistente. Per coerenza, copiare anche eventuali altri file modificati. Se vengono usati i campi PPR o ISR del client, copiare anche il file OSD aggiornato e le icone nel server specificato nei campi PPR e ISR.

-   Copiare la nuova versione del file SFT nella cartella del pacchetto sotto la cartella contenuto Web nel server IIS; ad esempio, è possibile accedere all'URL del server IIS usando http://IISserver/CONTENT/packagename o https://IISserver/CONTENT/packagename .

Al successivo aggiornamento della pubblicazione, il client viene aggiornato con la nuova versione del file OSD. Questo file punta ora alla nuova versione del file SFT; di conseguenza, quando l'utente fa doppio clic sull'icona di un'applicazione, viene avviata la nuova versione.

## Uso di un server di gestione per la pubblicazione e una condivisione file per il flusso


In questo scenario, il server di gestione di App-V viene usato per la pubblicazione dei pacchetti e il file server viene usato per i pacchetti e le applicazioni in streaming. Quando il pacchetto originale viene importato nel server di gestione, l'amministratore copia la cartella del pacchetto contenente i file creati dal sequencer nella cartella contenuto, ad esempio in \\\\server\\CONTENT\\packagename. L'amministratore modifica la voce HREF nel file OSD in modo che punti al file SFT nel file server e importi il pacchetto nel server di gestione.

Per configurare il file server per il flusso, l'amministratore copia la cartella del pacchetto dal server di gestione alla cartella contenuto nel file server. Questa cartella deve avere lo stesso nome e il relativo percorso nella cartella del contenuto del file server come nel server di gestione, ad esempio \\\\fileserver\\CONTENT\\packagename.

Se l'impostazione radice dell'origine dell'applicazione del client (ASR) è configurata in maniera che punti al file server usando un percorso UNC, ad esempio \\\\fileserver\\content, il client usa questa impostazione invece del nome del server nella voce HREF nel file OSD. L'amministratore può facoltativamente configurare i campi ISR e PPR nel client in modo che puntino al server di gestione o al file server, a seconda dell'architettura di sistema specifica in uso.

Quando il server di gestione autentica l'utente, il server pubblica le applicazioni dell'utente inviando il file applist.xml al client. Il client recupera i file OSD e le icone per le applicazioni dal file server o dal server di gestione, a seconda delle impostazioni dei campi ISR e PPR.

Quando l'utente fa doppio clic sull'icona di un'applicazione, il client usa il percorso del file di contenuto del pacchetto (SFT) contenuto nell'elemento HREF del file OSD. Se viene usato l'ASR, il client sostituisce il nome del server (e la porta e il protocollo, se usato) nell'elemento HREF con il percorso del file server specificato nell'ASR. L'applicazione viene quindi trasmessa dal file server alla cache del client e viene avviata.

### Per aggiornare il pacchetto

La procedura per l'aggiornamento del pacchetto è la seguente:

-   Copiare la nuova versione del file OSD nella cartella della versione originale nella cartella contenuto del server di gestione, ad esempio \\\\server\\CONTENT\\packagename, sostituendo il file OSD esistente. Qualsiasi altro file modificato deve essere copiato anche per coerenza. Se vengono usati i campi PPR o ISR del client, copiare anche il file OSD aggiornato e le icone nel server specificato nei campi PPR e ISR.

-   Copiare la nuova versione del file SFT nella cartella del pacchetto sotto la cartella contenuto nel file server, ad esempio \\\\fileserver\\CONTENT\\packagename. Copiare il file V2 SFT nella cartella sotto la condivisione di contenuto nel file server, ad esempio \\\\fileserver\\CONTENT\\packagename\\V1.

Al successivo aggiornamento della pubblicazione il client viene aggiornato con la nuova versione del file OSD. Questo file punta ora alla nuova versione del file SFT, quindi quando l'utente fa doppio clic sull'icona di un'applicazione, viene avviata la nuova versione.

## Aggiornamento del pacchetto tramite la modalità di streaming MSI


Quando si genera un file di Windows Installer (MSI) durante la sequenziazione di un pacchetto, il Sequencer crea una. File MSI che contiene tutte le informazioni di pubblicazione necessarie. L'amministratore deve copiare il. File MSI per il client e per. File SFT contenente il contenuto del pacchetto in una condivisione di rete accessibile dal computer client.

Per pubblicare l'applicazione nel client, eseguire il comando seguente nel computer client:

   **Msiexec.exe/i \\\\PathToMsi\\packagename.msi modalità = flusso OVERRIDEURL = \\\\\\\\server\\share\\package.SFT**

Il. Il file MSI pubblica le applicazioni nel client e quindi trasmette il flusso. File SFT nella cache client.

### Per aggiornare il pacchetto

Per aggiungere una nuova versione, un amministratore deve distribuire un nuovo. File MSI per il client e un nuovo. File SFT per la condivisione di rete. L'amministratore deve quindi eseguire lo stesso comando usato per distribuire il pacchetto, ma usare il nuovo. File MSI e il nuovo. File SFT, ad esempio:

   **Msiexec.exe/i \\\\PathToMsi\\packagename\_2.msi modalità = flusso OVERRIDEURL = \\\\\\\\server\\share\\package\_2.SFT**

 

 





