---
title: Informazioni sulle fasi di sequenziazione
description: Informazioni sulle fasi di sequenziazione
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820005"
---
# Informazioni sulle fasi di sequenziazione


La sequenziazione è il processo con cui crei un pacchetto di applicazione sequenziale usando Microsoft Application Virtualization (App-V) Sequencer. Durante la sequenziazione, il sequencer monitora e registra tutti i processi di installazione e configurazione per un'applicazione e crea i file seguenti: ICO, OSD, SFT e SPRJ. Questi file contengono tutte le informazioni necessarie su un'applicazione e consentono l'esecuzione dell'applicazione in un ambiente virtuale.

Le quattro fasi per la sequenziazione di un'applicazione e la creazione di un pacchetto di applicazione virtuale sono installazione, avvio, personalizzazione e salvataggio. L'elenco seguente fornisce informazioni su ognuna delle fasi:

1.  **Fase di installazione**: durante la fase di installazione, specificare il nome del pacchetto e un commento associato facoltativo che verrà associato al pacchetto. È anche possibile configurare le opzioni di monitoraggio avanzato durante questa fase. Le opzioni di monitoraggio avanzate includono la specifica della dimensione del blocco e se si installeranno gli aggiornamenti automatici durante il monitoraggio. Il sequencer registra tutte le informazioni e le configurazioni necessarie per creare un pacchetto di applicazione virtuale e le impostazioni del file e del registro di sistema associate.

    **Importante**  Per visualizzare le opzioni avanzate, selezionare **Mostra opzioni di monitoraggio avanzato** nella pagina **informazioni pacchetto** .

     

2.  **Fase di avvio**: durante la fase di avvio, è possibile specificare le associazioni di file e i descrittori di sicurezza necessari che devono essere configurati con il pacchetto. È necessario aprire l'applicazione tutte le volte necessarie per garantire la funzionalità e la stabilità delle applicazioni.

3.  **Fase di personalizzazione**: durante la fase di personalizzazione è possibile configurare il pacchetto usando i file OSD associati. Puoi specificare se gli script associati devono essere eseguiti all'interno o all'esterno dell'ambiente virtuale, specificare altre azioni che devono essere eseguite, specificare la modalità di esecuzione degli script associati (in modo sincrono o asincrono) e specificare gli eventuali script aggiuntivi da eseguire nel contesto utente.

4.  **Fase di salvataggio**: durante la fase di salvataggio vengono creati tutti i file necessari per il pacchetto dell'applicazione virtuale. I file creati sono. sprj,. SFT,. OSD,. ico,. XML manifest e il file Windows Installer (. msi).

## Argomenti correlati


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





