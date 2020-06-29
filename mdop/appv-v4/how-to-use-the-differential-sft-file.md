---
title: Come usare il file differenziale SFT
description: Come usare il file differenziale SFT
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816386"
---
# Come usare il file differenziale SFT


Durante la sequenziazione di un'applicazione, Microsoft Application Virtualization (App-V) Sequencer crea i file SFT (. SFT) per archiviare tutti i contenuti e le informazioni di configurazione dell'applicazione virtuale. Nella versione 4.5 di App-V è stato introdotto il file differenziale SFT (. dsft). Dopo aver usato il sequencer per creare un aggiornamento per un pacchetto esistente, puoi scegliere di generare questo file per archiviare solo le differenze tra il pacchetto di applicazione sequenziata originale e la nuova versione. È quindi molto più piccolo del file SFT completo per la nuova versione dell'applicazione e riduce l'impatto dell'invio di aggiornamenti del pacchetto sulle connessioni di rete a larghezza di banda ridotta. Tuttavia, il suo uso è supportato solo in determinate situazioni limitate. Questa caratteristica è stata progettata per essere usata in modo specifico in cui si usa un sistema ESD (Electronic Software Distribution) per gestire un gruppo di utenti con un file server locale tramite una connessione a larghezza di banda ridotta e non si usa App-V Streaming Server.

Non è necessario usare il file differenziale SFT se si usa la configurazione di Manager2007 per gestire gli utenti, perché Configuration Manager supporta le distribuzioni con larghezza di banda ridotta già integrate. Non è inoltre necessario se si usa la gestione di Application Virtualization (App-V) o i server di flusso con aggiornamento attivo, perché il client recupererà solo le differenze tra le versioni precedenti e quelle nuove del pacchetto.

La procedura seguente illustra come usare il mkdiffpkg.exe incluso nell'installazione di Sequencer per creare il file differenziale SFT, dopo aver completato l'aggiornamento del pacchetto di applicazione virtuale e per distribuire il file differenziale SFT. Il completamento di questa procedura consente di verificare che, se il pacchetto viene in qualche modo scaricato dal computer client, la volta successiva che l'utente prova a eseguire l'applicazione, il client ritornerà all'URL di override, che è impostato per trasmettere il pacchetto completo V2. sft dalla condivisione file locale. In questo modo eviterai qualsiasi errore per l'utente durante l'avvio dell'applicazione. Se l'intero client viene danneggiato o viene disinstallato, è consigliabile che il sistema ESD sia configurato per distribuire la versione completa del pacchetto aggiornato, V2. SFT, al client.

Per altre informazioni sull'aggiornamento di un pacchetto, vedere "come aggiornare un'applicazione virtuale esistente" in App-V 4.5 Operations Guide at <https://go.microsoft.com/fwlink/?LinkId=133129>

**Nota**  Come prerequisito, tutti i computer degli utenti a cui viene assegnato l'ESD devono avere il file v1. SFT completamente caricato nella cache locale e il flusso di file deve essere abilitato in tutti i computer.

 

**Per usare il file differenziale SFT**

1.  Accedere al computer sequencer usando un account con diritti di amministratore. Aprire il pacchetto originale (V1) per l'aggiornamento nel sequencer e quindi aggiornare il pacchetto alla nuova versione (v2) e salvarlo come nuovo V2. SFT.

2.  Aprire una finestra di comando nella cartella di installazione dell'App-V 4.5 Sequencer ed eseguire il comando seguente:

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  Usando il sistema ESD o un altro processo di copia di file, copiare il file di contenuto del pacchetto V2 completo, V2. SFT, in una condivisione di file locale accessibile ai computer degli utenti in una connessione di rete ben collegata.

4.  Usando il sistema ESD, inserire una copia del file differenziale SFT, V2. dsft, in ogni computer utente.

5.  Per importare il file V2. dsft, eseguire il comando SFTMIME seguente in ogni computer utente:

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  Eseguire il comando SFTMIME seguente in ogni computer utente per impostare l'URL di override in punto del file V2. SFT:

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**Nota**  
-   I file differenziali SFT devono essere applicati ai client nell'ordine corretto. Ad esempio, V2. dsft deve essere applicato a un'applicazione V1 prima di applicare V3. dsft.

-   La funzionalità **Genera pacchetto di Microsoft Windows Installer (MSI)** nel sequencer non può essere usata con il file differenziale SFT.

 

## Argomenti correlati


[Come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





