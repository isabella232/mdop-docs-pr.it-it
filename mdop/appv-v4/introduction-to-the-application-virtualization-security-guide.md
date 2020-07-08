---
title: Introduzione alla guida alla sicurezza della virtualizzazione dell'applicazione
description: Introduzione alla guida alla sicurezza della virtualizzazione dell'applicazione
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816266"
---
# Introduzione alla guida alla sicurezza della virtualizzazione dell'applicazione


Questa guida alla sicurezza di Microsoft Application Virtualization (App-V) offre istruzioni per gli amministratori responsabili della configurazione delle funzionalità di sicurezza selezionate per la distribuzione di App-V.

**Nota**  Questa documentazione non fornisce indicazioni per la scelta delle opzioni di sicurezza specifiche. Queste informazioni sono disponibili nel white paper sulle procedure consigliate per l'App-V Security Best Practices <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

L'amministratore di App-V che usa questa guida deve avere familiarità con le tecnologie correlate alla sicurezza seguenti:

-   Active Directory Domain Services

-   Infrastruttura a chiave pubblica (PKI)

-   IPsec (Internet Protocol Security)

-   Criteri di gruppo

-   Internet Information Services (IIS)

## Componenti dell'infrastruttura APP-V


Quando si pianifica un ambiente App-V di sicurezza avanzato, è possibile considerare diversi modelli di infrastruttura.

**Nota**  Per altre informazioni sui modelli di infrastruttura di App-V, vedere la documentazione seguente:

-   [Guida alla pianificazione e distribuzione di App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Serie di guide di progettazione e pianificazione delle infrastrutture](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Questi modelli usano alcuni ma forse non tutti i componenti App-V descritti nella figura seguente.

![diagramma di Office Branch App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Application Virtualization (App-V) Management Server  
App-V Management Server trasmette il contenuto del pacchetto e pubblica i collegamenti e le associazioni di tipi di file al client App-V. App-V Management Server supporta inoltre l'aggiornamento attivo, la gestione delle licenze e un database che può essere usato per la creazione di report.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Application Virtualization (App-V) streaming server  
App-V Streaming Server ospita i pacchetti per lo streaming in client App-V in ambienti come le succursali, in cui la larghezza di banda della connessione al server di gestione di App-V è insufficiente per il flusso di contenuto del pacchetto nei client. Il server di streaming contiene solo funzionalità di flusso e non fornisce la console di gestione di App-V o il servizio Web di gestione App-V.

<a href="" id="application-virtualization--app-v--data-store"></a>Archivio dati Application Virtualization (App-V)  
L'App-V Data Store, nel database SQL, mantiene le informazioni correlate all'infrastruttura App-V. Le informazioni nell'archivio dati di App-V includono tutti i record delle applicazioni, le assegnazioni delle applicazioni e i gruppi che gestiscono l'ambiente di virtualizzazione dell'applicazione.

<a href="" id="application-virtualization--app-v--management-service"></a>Servizio di gestione di Application Virtualization (App-V)  
Il servizio di gestione App-V comunica le richieste di lettura/scrittura all'archivio dati della virtualizzazione dell'applicazione. Questo componente può essere installato nello stesso computer del server di gestione App-V o in un computer separato con IIS installato.

<a href="" id="application-virtualization--app-v--management-console"></a>Console di gestione di Application Virtualization (App-V)  
App-V Management Console è un'utilità di gestione dello snap-in per l'amministrazione di App-V Server. Questo componente può essere installato nello stesso computer del server App-V o in una workstation separata con MMC 3.0 e. NET 2.0 installato.

<a href="" id="application-virtualization--app-v--sequencer"></a>Application Virtualization (App-V) Sequencer  
App-V Sequencer monitora e acquisisce l'installazione delle applicazioni e crea pacchetti di applicazioni virtuali. L'output del sequencer è costituito dall'icona dell'applicazione, dal file OSD che contiene le informazioni sulla definizione dell'applicazione, da un file manifesto del pacchetto e da un file SFT contenente i file di contenuto dell'applicazione. Facoltativamente, è possibile creare un file di Windows Installer per l'installazione del pacchetto senza usare l'infrastruttura App-V.

<a href="" id="application-virtualization--app-v--client"></a>Client di Application Virtualization (App-V)  
Il client App-V è installato nel computer client Desktop App-V o nel computer client di Servizi terminal App-V. Fornisce l'ambiente virtuale per i pacchetti di applicazioni virtuali. Il client App-V gestisce il flusso del pacchetto nella cache, nell'aggiornamento della pubblicazione delle applicazioni virtuali e nell'interazione con i server di virtualizzazione dell'applicazione.

 

 





