---
title: Panoramica di uno scenario basato sulla distribuzione elettronica del software
description: Panoramica di uno scenario basato sulla distribuzione elettronica del software
author: dansimp
ms.assetid: e9e94b8a-6cba-4de8-9b57-73897796b6a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cfbdf40f5ac0f61721c05d0da5cd49e910b16154
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821596"
---
# Panoramica di uno scenario basato sulla distribuzione elettronica del software


Se si prevede di usare una soluzione ESD (Electronic Software Distribution) per distribuire applicazioni virtuali, è importante comprendere i fattori che entrano e sono interessati da tale decisione. Questo argomento descrive i vantaggi derivanti dall'uso di uno scenario basato su ESD e fornisce informazioni sui metodi di pubblicazione e flusso di pacchetti che è necessario considerare mentre si procede alla distribuzione.

**Importante**  Qualsiasi soluzione ESD si usi, è necessario avere familiarità con i requisiti della soluzione specifica. Se si usa Microsoft endpoint Configuration Manager, vedere la documentazione di Configuration Manager in <https://go.microsoft.com/fwlink/?LinkId=66999> .

 

L'uso di un sistema ESD esistente offre i vantaggi seguenti:

-   Elimina le infrastrutture di gestione duale

-   Riduce il costo di hardware aggiuntivo

-   Riduce il costo delle licenze aggiuntive per il sistema operativo e il database

## Metodi di pubblicazione


Quando si usa uno scenario basato su ESD, sono disponibili le opzioni seguenti per pubblicare l'applicazione nei client:

-   **Windows Installer autonomo.** Il file di Windows Installer contiene il manifesto e i file OSD e ICO che i client usano per configurare un pacchetto. Il file di Windows Installer copia anche il file SFT nel client perché questo scenario non usa un server.

-   **Windows Installer con il manifesto del pacchetto.** Il file di Windows Installer contiene il manifesto e i file OSD e ICO che i client usano per configurare un pacchetto. Il file SFT è archiviato in un server. Un parametro della riga di comando indirizza il client alla posizione del file SFT.

-   **Comandi di SFTMIME.** I comandi di SFTMIME vengono usati con i file manifest, OSD, ICO e SFT per aggiungere pacchetti al client. Il file manifesto deve essere nel computer client oppure deve essere accessibile tramite un percorso UNC. A seconda della configurazione del client e delle opzioni della riga di comando, i file OSD, ICO e SFT possono essere presenti nel computer client o in un server.

Per informazioni più dettagliate sui metodi di pubblicazione precedenti, vedere [determinare il metodo di pubblicazione](determine-your-publishing-method.md).

## Metodi di flusso del pacchetto


Dovrai determinare il metodo che il sistema di virtualizzazione dell'applicazione userà per trasmettere i pacchetti di applicazioni virtuali o i file SFT dal server ai client. Sono disponibili le opzioni di flusso seguenti:

-   **Application Virtualization Streaming Server.** Se usi una Application Virtualization Streaming Server nella tua configurazione, i file SFT vengono trasmessi ai client da tale server usando i protocolli RTSP o RTSPs. È necessario installare il software server in un computer ed è necessario configurarlo tramite il registro di sistema, ma questa configurazione non dipende da servizi come SQL o servizi di dominio Active Directory. I file SFT sono archiviati nel server in una posizione accessibile dai client. Le informazioni di pubblicazione possono essere distribuite ai client tramite qualsiasi meccanismo di distribuzione. Tuttavia, quando è configurato, il client riceve gli aggiornamenti del pacchetto automaticamente e l'aggiornamento attivo è supportato.

-   **Application Virtualization Management Server.** Se usi un Application Virtualization Management Server nella tua configurazione, i file SFT vengono trasmessi ai client da tale server usando i protocolli RTSP o RTSPs. Puoi gestire questo server tramite la console di gestione di Application Virtualization. Questa configurazione usa un database SQL e servizi Active Directory. Il server può distribuire le informazioni di pubblicazione ai client, quindi non sono necessari meccanismi di pubblicazione aggiuntivi.

-   **File server.** Se si usa un file server nella configurazione, i file SFT vengono trasmessi agli altri computer client usando i protocolli SMB. I file server usati in questa configurazione vengono gestiti creando elenchi di controllo di accesso (ACL) nei file condivisioni e SFT. È necessario prestare attenzione per indirizzare i client ai file corretti nel file server.

-   **Server IIS.** Se si usa un server IIS nella propria configurazione, i file SFT vengono trasmessi ai client da tale server usando i protocolli HTTP o HTTPS. Il server IIS è facile da configurare e gestire. È necessario prestare attenzione per indirizzare i client ai file corretti nel server IIS.

Per informazioni più dettagliate sui metodi di flusso precedenti, vedere [determinare il metodo di flusso](determine-your-streaming-method.md).

## Argomenti correlati


[Parametri della riga di comando del programma di installazione di Application Virtualization Client](application-virtualization-client-installer-command-line-parameters.md)

[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Determinare il metodo di pubblicazione](determine-your-publishing-method.md)

[Determinare il metodo di streaming](determine-your-streaming-method.md)

[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





