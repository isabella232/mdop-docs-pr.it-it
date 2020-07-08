---
title: Panoramica di sicurezza e protezione
description: Panoramica di sicurezza e protezione
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815656"
---
# Panoramica di sicurezza e protezione


Microsoft Application Virtualization 4.5 offre le caratteristiche di sicurezza avanzate seguenti per pianificare e implementare una strategia di distribuzione più sicura:

-   La virtualizzazione delle applicazioni ora supporta TLS (Transport Layer Security) con certificati X. 509 v3. A condizione che sia stato effettuato il provisioning di un certificato server per l'Application Virtualization Management o lo streaming server previsto, l'installazione sarà predefinita per la sicurezza, usando il protocollo RTSPs sulla porta 322. L'uso di RTSPs garantisce che la comunicazione tra i server di virtualizzazione dell'applicazione e i client di virtualizzazione dell'applicazione sia firmata e crittografata Se al server non viene assegnato un certificato durante l'installazione di Application Virtualization Server, la comunicazione verrà impostata su RTSP sulla porta 554.

    **Nota sulla sicurezza:**

    Per fornire una configurazione sicura del server, è necessario assicurarsi che le porte RTSP siano disabilitate anche se tutti i pacchetti sono configurati per l'uso di RTSPs.

    Se si aggiungono certificati di sicurezza al server dopo l'installazione del server, è possibile che il server non rilevi i certificati. Per garantire il rilevamento del certificato di sicurezza, riavviare il server dopo l'aggiunta dei certificati.

-   Il client deve essere configurato per l'uso dello stesso protocollo e della stessa porta del server oppure non sarà in grado di comunicare con il server. Il client deve considerare attendibile anche l'autorità emittente del certificato e le navi con diversi provider primari nell'archivio radice attendibile. È possibile usare certificati autofirmati, ma sarà necessario aggiornare i client.

-   Quando si configurano i server IIS per l'uso del protocollo HTTPS per lo streaming, è necessario configurare Secure Sockets Layer (SSL) nel server IIS e eseguire il provisioning del certificato per il server. Anche i client dovranno essere configurati per considerare attendibile l'autorità di certificazione radice che ha emesso il certificato del server.

-   L'autenticazione Kerberos è stata aggiunta a Microsoft Application Virtualization come meccanismo di autenticazione predefinito. Le versioni precedenti si basavano su NTLM v2 per l'autenticazione. L'uso dell'autenticazione Kerberos rafforza la sicurezza delle comunicazioni tra il client e il server di virtualizzazione dell'applicazione. Quando una connessione è stata avviata dal client, il server di virtualizzazione dell'applicazione verifica il ticket di sessione con il centro distribuzione chiavi (KDC).

-   Dato il supporto per l'uso dei certificati server e l'uso dei protocolli RTSPs o HTTPS, ora è possibile supportare i client all'esterno della rete aziendale. In questo modo è possibile eliminare la necessità per gli utenti di dispositivi mobili di configurare una connessione sicura alla rete aziendale (VPN, RAS e così via) prima di avviare applicazioni di Application Virtualization provisioning.

Altre importanti considerazioni sulla sicurezza da tenere in considerazione includono le seguenti:

-   Mantenere sempre i server completamente aggiornati e protetti.

-   Per aggiungere un certificato per consentire comunicazioni più sicure all'Application Virtualization Management Server, è necessario che siano soddisfatti i criteri seguenti:

    -   L'utente che aggiungerà il certificato deve essere un amministratore nel server in cui si trova l'archivio certificati.

    -   Il servizio Server deve essere avviato.

    -   La porta 139 nel server di gestione deve essere aperta al servizio Web server'sIP.

-   USA gli elenchi di controllo di accesso (ACL) per verificare che i pacchetti dell'applicazione e tutti i file di pacchetto siano protetti e non vengano manomessi. Gli ACL limitano l'accesso alla posizione o alla cartella in cui vengono archiviati i pacchetti, consentendo l'accesso solo a determinati account.

-   Verificare che il canale tra l'Application Virtualization Management Server e il database sia protetto, ad esempio tramite IPsec.

-   Se i pacchetti sono archiviati in una SAN o NAS, verificare che la connessione tra il dispositivo di archiviazione centrale e i server di virtualizzazione dell'applicazione sia protetta.

-   Tutti i canali di comunicazione al client devono essere protetti, incluse le connessioni al server di pubblicazione, l'Application Virtualization Server e il percorso dei file OSD e ICO, usando un protocollo come HTTPS o IPsec. 

-   Le autorizzazioni client devono essere configurate per evitare che i pacchetti vengano manomessi dagli utenti. È particolarmente importante non concedere agli utenti l'autorizzazione per l'aggiunta o l'aggiornamento di pacchetti su sistemi, ad esempio i server Host sessione Desktop remoto (host RDSession) condivisi con più utenti.

-   L'autenticazione Kerberos deve essere consentita in ambienti di dominio o di foresta per consentire il corretto funzionamento della console di gestione del server.

-   Questa versione del software non supporta l'hosting di un server RTSP basato su Kerberos e di un server IIS basato solo su Microsoft NTLM nello stesso computer. Per ospitare un server RTSP e un server IIS nello stesso computer, rimuovere l'SPN dal server IIS e usare l'autenticazione NTLM.

## Argomenti correlati


[Pianificazione della distribuzione del sistema Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 





