---
title: Panoramica di Application Virtualization Sequencer Console
description: Panoramica di Application Virtualization Sequencer Console
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822195"
---
# Panoramica di Application Virtualization Sequencer Console


Application Virtualization (App-V) Sequencer crea applicazioni in modo che possano essere eseguite in un ambiente virtuale, come applicazioni virtuali. Dopo che un'applicazione è stata sequenziata, può essere eseguita da un server App-V per indirizzare i computer che eseguono il client Desktop App-V o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal) usando un processo denominato flusso. App-V Sequencer monitora il processo di installazione e configurazione per le applicazioni e registra tutte le informazioni necessarie per l'esecuzione dell'applicazione nell'ambiente virtuale. Questo processo determina anche i file e le configurazioni applicabili a tutti gli utenti e alle configurazioni che gli utenti possono personalizzare. Le applicazioni virtuali vengono eseguite nei computer di destinazione e non hanno alcun effetto sul sistema operativo in esecuzione nel computer di destinazione o in tutte le applicazioni installate nel computer di destinazione.

## Considerazioni sulla sicurezza di Application Virtualization Sequencer


App-V Sequencer esegue tutti i servizi rilevati in fase di sequenziazione usando l'account di sistema locale e non applica i descrittori di sicurezza sulle richieste di controllo del servizio. Se il servizio è stato installato con un account utente diverso o se i descrittori di sicurezza hanno lo scopo di concedere autorizzazioni di servizio specifiche per gruppi di utenti diversi, valutare attentamente se il servizio deve essere virtualizzato. In alcuni casi, è necessario installare il servizio localmente per verificare che la sicurezza del servizio prevista venga mantenuta.

## Opzioni del menu console di Application Virtualization Sequencer


Le voci di menu seguenti sono disponibili nella console App-V Sequencer:

-   **File**: contiene vari comandi per facilitare la creazione, l'apertura, la modifica e la salvataggio di applicazioni sequenziate.

-   **Modifica**: contiene vari comandi per la modifica delle applicazioni virtuali esistenti.

-   **Visualizzazione**: contiene vari comandi per la visualizzazione delle proprietà di un'applicazione virtuale.

-   **Tools**: contiene vari strumenti e diagnostica per la configurazione delle applicazioni virtuali.

## Opzioni della barra degli strumenti console di Application Virtualization Sequencer


I pulsanti della barra degli strumenti seguenti sono disponibili nella console App-V Sequencer:

-   **Nuovo pacchetto**: fare clic per creare una nuova applicazione sequenziata.

-   **Apri**: fare clic per aprire un pacchetto di applicazione sequenziata nella console App-V Sequencer.

-   **Apri per l'aggiornamento**: fare clic per aprire un'applicazione sequenziata per aggiornare o applicare un aggiornamento.

-   **Salva**: fare clic per salvare un'applicazione virtuale sequenziata.

-   **Sequenziazione guidata**: fare clic per aprire la procedura guidata di sequenziazione. Questo pulsante deve essere usato per avviare la sequenziazione guidata se si apportano modifiche nella scheda **generale** in **Tools**  /  **Opzioni**strumenti.

## Schede delle applicazioni virtuali


Le schede seguenti vengono visualizzate quando si visualizza un'applicazione virtuale nella console App-V Sequencer:

-   **Proprietà**: Visualizza le informazioni sull'applicazione virtuale selezionata. È possibile aggiornare il **nome del pacchetto** e i **Commenti** associati all'applicazione virtuale.

-   **Distribuzione**: Visualizza le informazioni sul modo in cui l'applicazione virtuale sarà accessibile dai computer di destinazione. Puoi configurare il metodo di recapito dell'applicazione virtuale ed è possibile configurare i sistemi operativi che devono essere in esecuzione nel computer di destinazione. È anche possibile configurare le opzioni di output associate. Se si prevede che i client accedano a un'applicazione virtuale da un file, usare il formato seguente quando si specifica il percorso: **file://server/share/Path/.SFT**. Selezionare **applica descrittori di sicurezza** per mantenere la sicurezza associata al pacchetto durante un aggiornamento o le autorizzazioni verranno reimpostate durante l'aggiornamento.

-   **Modifica cronologia**: Visualizza le informazioni sugli aggiornamenti apportati all'applicazione virtuale.

-   **File**: Visualizza i file associati all'applicazione virtuale selezionata. Puoi apportare piccole revisioni alle proprietà del file associate usando i campi appropriati.

-   **Registro di sistema virtuale**: Visualizza il registro di sistema virtuale associato all'applicazione virtuale selezionata. È possibile aggiungere o eliminare le chiavi del registro di sistema facendo clic con il pulsante destro del mouse sulla voce appropriata.

-   **File system virtuale**: Visualizza i sistemi di file virtuali associati all'applicazione virtuale selezionata. È possibile aggiungere, eliminare o modificare le voci di file System in questa scheda facendo clic con il pulsante destro del mouse sulla voce appropriata e scegliendo l'opzione.

-   **Servizi virtuali**: Visualizza i servizi associati all'applicazione virtuale selezionata.

-   **OSD**: Visualizza informazioni sul descrittore software aperto (OSD) associato all'applicazione virtuale. È possibile aggiornare i file associati al file OSD facendo clic con il pulsante destro del mouse sulla voce appropriata e selezionando l'azione desiderata.

## Argomenti correlati


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





