---
title: Pianificazione per la sicurezza dei client
description: Pianificazione per la sicurezza dei client
author: dansimp
ms.assetid: 4840a60f-4c91-489c-ad0b-6671882abf9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0038f7cbc8592d6c7fcdfa485111da88c17791d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815935"
---
# Pianificazione per la sicurezza dei client


Il client App-V offre diversi miglioramenti della sicurezza non presenti nelle versioni precedenti del prodotto. Queste modifiche garantiscono una maggiore sicurezza dopo l'installazione e la successiva configurazione delle impostazioni client. Questo argomento descrive alcuni di questi miglioramenti e identifica alcune importanti impostazioni di configurazione correlate alla sicurezza da tenere in considerazione durante il processo di pianificazione. È importante ricordare che le applicazioni virtuali sono ancora eseguibili, quindi devi assicurarti che questi asset non vengano manomessi da persone non autorizzate. Per questo motivo, la cache dei file OSD (Open Software Descriptor) è protetta come descritto più avanti in questo argomento e ti consigliamo vivamente di usare RTSPs, HTTPS e IPsec per proteggere la pubblicazione e il flusso.

## App-V Client Security


Per impostazione predefinita, durante l'installazione, il client App-V è configurato con le autorizzazioni minime necessarie per consentire a un utente di eseguire un aggiornamento della pubblicazione e avviare le applicazioni. Altri miglioramenti della sicurezza forniti nel client App-V includono i seguenti:

-   Per impostazione predefinita, la cache dei file OSD può essere aggiornata solo dagli amministratori e usando il processo di aggiornamento della pubblicazione.

-   Il file di log (sftlog.txt) è accessibile solo dagli account con accesso amministrativo locale al client.

-   Il file di log ha ora una dimensione massima.

### Associazioni di tipi di file

Per impostazione predefinita, l'installazione del client registra le associazioni di tipi di file (accordi) per i file OSD, che consente agli utenti di avviare le applicazioni direttamente dai file OSD anziché dai collegamenti pubblicati. Se un utente con diritti di amministratore locale riceve un file OSD contenente codice malevolo, tramite posta elettronica o scaricato da un sito Web, l'utente può aprire il file OSD e avviare l'applicazione anche se il client è stato impostato per limitare l'autorizzazione **Aggiungi applicazione** . Puoi annullare la registrazione di accordi per l'OSD per ridurre questo rischio. Puoi anche bloccare questa estensione nel sistema di posta elettronica e nel firewall. Per altre informazioni sulla configurazione di Outlook per bloccare le estensioni, vedere <https://go.microsoft.com/fwlink/?LinkId=133278> .

**Nota sulla sicurezza:**

A partire da App-V versione 4.6, l'associazione tipo di file non viene più creata per i file OSD durante una nuova installazione del client, anche se le impostazioni esistenti verranno mantenute durante un aggiornamento dalla versione 4,2 o 4,5 del client App-V. Se per qualsiasi motivo è essenziale creare l'associazione di tipi di file, è possibile creare le chiavi del registro di sistema seguenti e impostarne i valori come illustrato di seguito:

    Create HKEY\_CLASSES\_ROOT\\.osd with a default value of SoftGrid.osd.File

    Under HKEY\_LOCAL\_MACHINE\\software\\classes\\Softgrid.osd.file, create a string value named AppUserModelID with a data value of Microsoft.AppV.Client.Tray

### Autorizzazione

Durante l'installazione, puoi usare il parametro **RequireAuthorizationIfCached** per configurare il client per richiedere l'autorizzazione dal server quando l'utente tenta di avviare un'applicazione. Dovresti considerare attentamente come impostare questo parametro. Se l'App-V Server non è disponibile per qualsiasi motivo, l'applicazione utilizzerà lo stato archiviato più recente di questo parametro per controllare l'accesso degli utenti all'applicazione. Se l'utente non ha avviato l'applicazione con successo prima che l'App-V Server diventi non disponibile, non sarà in grado di avviare l'applicazione finché non potrà comunicare con il server e ricevere l'autorizzazione. Tuttavia, se si imposta il parametro in modo che il client non richieda l'autorizzazione e se il server non è disponibile, è possibile che tutte le applicazioni precedentemente memorizzate nella cache possano essere avviate o meno. Inoltre, se l'utente ha l'autorizzazione per cambiare il client per lavorare in modalità offline tramite le autorizzazioni o se l'utente è un amministratore locale, l'utente potrà aprire tutti i pacchetti memorizzati nella cache come se l'infrastruttura di App-V non fosse disponibile.

### Analisi antivirus

Il software antivirus in uso in un computer client App-V può rilevare e segnalare un file infetto nell'ambiente virtuale. Tuttavia, non può disinfettare il file. Se un virus viene rilevato nell'ambiente virtuale, il software antivirus eseguirebbe l'operazione di quarantena o riparazione configurata nella cache, non nel pacchetto effettivo. Configurare il software antivirus con un'eccezione per il file Sftfs. FSD. Questo file è il file della cache che archivia i pacchetti nel client App-V.

**Nota sulla sicurezza:**

Se un virus viene rilevato in un'applicazione o in un pacchetto distribuito nell'ambiente di produzione, sostituire l'applicazione o il pacchetto con una versione priva di virus.

## Comunicazione tra client e server


Gli aggiornamenti per la pubblicazione e il flusso di pacchetti sono anche aree in cui le considerazioni sulla sicurezza relative alla comunicazione client-server sono importanti.

### Aggiornamento pubblicazione

Quando il client comunica con il server per eseguire un aggiornamento della pubblicazione, USA le credenziali dell'utente connesso per richiedere informazioni sui pacchetti dell'applicazione. È consigliabile proteggere la comunicazione che si verifica tra App-V client e App-V Management Server per assicurarsi che nessuna delle informazioni di pubblicazione possa essere manomessa in transito. Questa operazione viene eseguita usando l'opzione sicurezza avanzata, che utilizzerà RTSPs/HTTPS. La comunicazione tra il client e la posizione in cui sono archiviati i file ICO e OSD deve usare IPsec per le condivisioni SMB/CIFS e HTTPS per un server IIS.

**Nota**  Se si usa IIS per pubblicare i file ICO e OSD, configurare un tipo MIME per OSD = TXT; in caso contrario, IIS rifiuterà di servire i file ICO e OSD ai client.

 

### Flusso del pacchetto

Quando un utente avvia un'applicazione per la prima volta o se nel client sono stati impostati parametri di caricamento automatico, il pacchetto dell'applicazione viene trasmesso da un server alla cache del client. Questo processo supporta i protocolli RTSP/RTSPs, HTTP/HTTPS e SMB/CIFS. I file OSD controllano i protocolli usati, a meno che l'impostazione **ApplicationSourceRoot** o **OVERRIDEURL** non sia stata configurata nei client. È consigliabile configurare la comunicazione per l'utente su RTSPs, HTTPS o IPsec per SMB/CIFS per ottenere livelli di sicurezza più alti. Per altre informazioni sulla scelta del metodo di comunicazione da usare, vedere la guida alla pianificazione e distribuzione di App-V <https://go.microsoft.com/fwlink/?LinkId=122063> .

**Nota**  Se si usa IIS per pubblicare i pacchetti (file SFT), configurare un tipo MIME per SFT = Binary; in caso contrario, IIS rifiuterà di servire i file SFT ai client.

 

### Profili mobili e reindirizzamento delle cartelle

Il sistema App-V archivia le modifiche specifiche degli utenti ai pacchetti nel file usrvol \ _sftfs \ _v1. pkg. Questo file si trova nella cartella dati applicazione del profilo di un utente. Poiché il profilo o una cartella di dati dell'applicazione reindirizzata viene trasferita tra il client e il server, usare IPsec per proteggere la comunicazione.

## Considerazioni per i client che si affacciano su Internet


Per i client con accesso a Internet, è importante valutare se il client è collegato al dominio o non è stato aggiunto un dominio.

### Client di dominio aggiunto

Per impostazione predefinita, i client App-V usano i ticket Kerberos emessi da servizi di dominio Active Directory per l'autenticazione e l'autorizzazione nella Intranet. Questi ticket Kerberos sono validi per 10 ore per impostazione predefinita. Il client utilizzerà questo ticket per accedere all'App-V Server per tutto il tempo in cui il ticket è valido, anche se il computer non è in grado di connettersi al controller di dominio per aggiornare il ticket. Se il ticket Kerberos scade, il client App-V tornerà all'autenticazione NTLM e userà le credenziali memorizzate nella cache dell'utente.

### Client non appartenente a un dominio

Se un utente è basato su Home e il computer non è collegato al dominio della società, App-V può comunque supportare le applicazioni di distribuzione. Per eseguire l'autenticazione e l'autorizzazione di un utente per l'esecuzione di un aggiornamento della pubblicazione e per avviare le applicazioni, configurare l'account utente nel computer client per archiviare il nome utente e la password che hanno accesso all'ambiente App-V e per specificare le autorizzazioni appropriate per le applicazioni.

## Argomenti correlati


[Pianificazione per sicurezza e protezione](planning-for-security-and-protection.md)

 

 





