---
title: Monitoraggio di Application Virtualization Server
description: Monitoraggio di Application Virtualization Server
author: dansimp
ms.assetid: d84355ae-4fe4-41d9-ac3a-3eaa32d9a61f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a53c0c37ca609c701727a7f4e18019a9f20110ed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816145"
---
# Monitoraggio di Application Virtualization Server


Per semplificare la gestione del server Application Virtualization (App-V), è possibile usare System Center Operations Manager2007 Management Pack. Questo Management Pack supporta solo i server di 4,5 Application Virtualization (App-V); non supporta versioni precedenti del server. Il Management Pack massimizza la disponibilità di App-V Server per la gestione delle richieste client App-V.

## Indicatori di stato


Gli indicatori di stato di integrità di App-V Server sono contraddistinti da colori. I colori rappresentano i valori di stato seguenti:

-   Nessun colore indica che il server è in uso senza errori non risolvibili.

-   Giallo indica che uno dei componenti non funziona correttamente. La funzionalità complessiva del server è degradata, ma il server è ancora disponibile.

-   Rosso indica che il server non è disponibile e che non può concedere servizi chiave o comunicare con le dipendenze del servizio esterno.

## Criteri di monitoraggio


Il Management Pack monitora gli aspetti seguenti dell'integrità del server:

-   Stato server: monitora gli eventi del server per verificare che il server stia fornendo i servizi previsti.

-   Accesso all'archivio dati: consente di tenere traccia della capacità di uno o più server di gestione di App-V di accedere e comunicare con l'App-V Data Store.

-   Accesso ai dati del contenuto: consente di monitorare l'accesso alla directory \\Content, che potrebbe essere una directory locale o una condivisione di rete, nonché la possibilità di leggere i file richiesti.

-   Sicurezza: segnala gli errori relativi al certificato e alle comunicazioni sicure del server App-V.

-   Gestione delle richieste client: monitora la capacità di uno o più server App-V di gestire e rispondere correttamente alle richieste del client. Queste richieste includono la pubblicazione di elementi come le richieste di configurazione, le richieste di caricamento dei pacchetti e le richieste fuori sequenza.

-   Configurazione server: consente di controllare le impostazioni di configurazione del server App-V. Queste impostazioni di configurazione includono le impostazioni nel registro di sistema e nell'archivio dati App-V.

## Differenze tra server


Le principali differenze tra App-V Management Server e App-V Streaming Server sono le seguenti:

-   I server di gestione di App-V possono creare servizi di pubblicazione, streaming, gestione e Reporting. Di conseguenza, il Management Pack può gestire più aspetti del server di gestione di App-V che può gestire in App-V Streaming Server, che fornisce solo il flusso di pacchetti.

-   App-V Streaming Server non ha un archivio dati App-V, quindi l'accesso all'archivio dati non viene monitorato. Le informazioni di configurazione per l'App-V Streaming Server vengono gestite nel registro di sistema.

-   App-V Streaming Server non usa l'interfaccia della console di gestione di App-V Server; usare altri strumenti per gestire la configurazione.

## Argomenti correlati


[Application Virtualization Server](application-virtualization-server.md)

 

 





