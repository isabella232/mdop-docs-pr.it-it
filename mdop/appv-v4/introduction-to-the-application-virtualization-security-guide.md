---
title: Introduzione alla Guida alla sicurezza di Application Virtualization
description: Introduzione alla Guida alla sicurezza di Application Virtualization
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
ms.openlocfilehash: 82914de48a5a5777f6ce4b50fe3e8af34dd82494
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910781"
---
# <a name="introduction-to-the-application-virtualization-security-guide"></a>Introduzione alla Guida alla sicurezza di Application Virtualization


Questa guida alla sicurezza di Microsoft Application Virtualization (App-V) fornisce istruzioni agli amministratori responsabili della configurazione delle funzionalità di sicurezza selezionate per la distribuzione di App-V.

**Nota**  
In questa documentazione non vengono fornite indicazioni per la scelta delle opzioni di sicurezza specifiche. Queste informazioni sono disponibili nel white paper Sulle procedure consigliate per la sicurezza di App-V disponibile all'indirizzo <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

Gli amministratori di App-V che usano questa guida devono avere familiarità con le tecnologie correlate alla sicurezza seguenti:

-   Active Directory Domain Services

-   Infrastruttura a chiave pubblica (PKI)

-   IPsec (Internet Protocol Security)

-   Criteri di gruppo

-   Internet Information Services (IIS)

## <a name="app-v-infrastructure-components"></a>Componenti dell'infrastruttura APP-V


Quando si pianifica un ambiente App-V di sicurezza avanzata, è possibile prendere in considerazione diversi modelli di infrastruttura.

**Nota**  
Per ulteriori informazioni sui modelli di infrastruttura App-V, vedere la documentazione seguente:

-   [Guida alla pianificazione e alla distribuzione di App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Serie di guide alla pianificazione e alla progettazione dell'infrastruttura](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Questi modelli utilizzano alcuni, ma probabilmente non tutti i componenti di App-V illustrati nella figura seguente.

![diagramma della succursale app-v.](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Server di gestione Application Virtualization (App-V)  
Il server di gestione App-V consente di trasmettere il contenuto del pacchetto e pubblica i collegamenti e le associazioni di tipi di file nel client App-V. Il server di gestione App-V supporta inoltre l'aggiornamento attivo, la gestione delle licenze e un database che può essere usato per la creazione di report.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Application Virtualization (App-V) Streaming Server  
Il server di streaming App-V ospita i pacchetti per lo streaming ai client App-V in ambienti come le succursali, in cui la larghezza di banda della connessione al server di gestione App-V non è sufficiente per lo streaming del contenuto del pacchetto ai client. Il server di streaming contiene solo funzionalità di streaming e non fornisce la console di gestione di App-V o il servizio Web di gestione app-V.

<a href="" id="application-virtualization--app-v--data-store"></a>Archivio dati di Application Virtualization (App-V)  
L'archivio dati App-V, nel database SQL, conserva le informazioni relative all'infrastruttura App-V. Le informazioni nell'archivio dati di App-V includono tutti i record dell'applicazione, le assegnazioni delle applicazioni e i gruppi che gestiscono l'ambiente Application Virtualization.

<a href="" id="application-virtualization--app-v--management-service"></a>Servizio di gestione Application Virtualization (App-V)  
Il servizio di gestione App-V comunica le richieste di lettura/scrittura all'archivio dati di Application Virtualization. Questo componente può essere installato nello stesso computer del server di gestione App-V o in un computer separato in cui è installato IIS.

<a href="" id="application-virtualization--app-v--management-console"></a>Console di gestione di Application Virtualization (App-V)  
App-V Management Console è un'utilità di gestione degli snap-in per l'amministrazione di App-V Server. Questo componente può essere installato nello stesso computer di App-V Server o in una workstation separata in cui sono installati MMC 3.0 e .NET 2.0.

<a href="" id="application-virtualization--app-v--sequencer"></a>Application Virtualization (App-V) Sequencer  
App-V Sequencer monitora e acquisisce l'installazione delle applicazioni e crea pacchetti di applicazioni virtuali. L'output di Sequencer è costituito dall'icona dell'applicazione, dal file OSD contenente le informazioni sulla definizione dell'applicazione, da un file manifesto del pacchetto e da un file SFT contenente i file di contenuto dell'applicazione. Facoltativamente, è possibile creare Windows installer per l'installazione del pacchetto senza usare l'infrastruttura App-V.

<a href="" id="application-virtualization--app-v--client"></a>Application Virtualization (App-V) Client  
Il client App-V viene installato nel computer client Desktop App-V o nel computer client di Servizi terminal App-V. Fornisce l'ambiente virtuale per i pacchetti dell'applicazione virtuale. Il client App-V gestisce il flusso del pacchetto nella cache, l'aggiornamento della pubblicazione di applicazioni virtuali e l'interazione con Application Virtualization Server.

 

 





