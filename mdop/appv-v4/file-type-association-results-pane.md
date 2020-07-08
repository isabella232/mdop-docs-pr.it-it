---
title: Riquadro Risultati del nodo Associazioni del tipo di file
description: Riquadro Risultati del nodo Associazioni del tipo di file
author: dansimp
ms.assetid: bc5ceb48-1b9f-45d9-a770-1bac90629c76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 73ea8e0e4145aeae309abff362a790287f19f6af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821565"
---
# Riquadro Risultati del nodo Associazioni del tipo di file


Il riquadro **risultati** **associazione file** è un livello sotto il riquadro **sistema** nella console di gestione client Application Virtualization e visualizza un elenco delle associazioni di tipi di file disponibili. Gli utenti possono visualizzare un elenco delle estensioni dei tipi di file e delle applicazioni a cui corrispondono.

Per visualizzare le opzioni specifiche per i tipi di file, fare clic con il pulsante destro del mouse su un'estensione dell'applicazione per visualizzare un menu a comparsa contenente gli elementi seguenti.

<a href="" id="delete"></a>**Delete**  
Elimina l'estensione del nome file dall'elenco e rimuove l'associazione al tipo di file.

<a href="" id="properties"></a>**Proprietà**  
Visualizza la finestra di dialogo **Proprietà** per l'estensione dell'applicazione selezionata. Questa finestra di dialogo include due schede:

-   Nella scheda **generale** vengono visualizzate informazioni generali sull'associazione tipo di file, tra cui l'icona e il nome dell'applicazione:

    -   **Icona**: Visualizza l'icona selezionata per il tipo di file associato.

    -   **Nome associazione**: Visualizza il nome del tipo di file.

    -   **Icona cambia**: fare clic su questo pulsante per modificare l'icona dell'associazione tipo di file.

    -   **Estensione**: Visualizza l'estensione o le estensioni associate a un tipo di file specifico.

    -   **Scollega**: questo pulsante è abilitato quando più di un'estensione è associata a un'applicazione. Fare clic su **Scollega** per gestire l'estensione del tipo di file separatamente dall'estensione a cui è attualmente collegata.

    -   **Applicazione specificata**: selezionare questo pulsante di opzione e scegliere un'applicazione nell'elenco a discesa delle applicazioni disponibili. Si sta modificando l'applicazione usata dall'azione predefinita. È anche possibile cercare un'applicazione se non è disponibile nell'elenco a discesa.

    -   **File OSD**: selezionare questo pulsante di opzione e specificare un percorso per un file OSD (Open Software Descriptor). È anche possibile passare a un file OSD.

-   Nella scheda **Avanzate** vengono visualizzate informazioni dettagliate sull'associazione tipo di file:

    -   **Azione**: Visualizza un elenco delle azioni disponibili per il tipo di file associato.

    -   **Tipo di contenuto**: Visualizza una descrizione del contenuto del tipo di file. Se questo campo viene lasciato vuoto, il client lo riempirà.

    -   **Tipo percepito**: Visualizza il tipo di file. È possibile selezionare una delle opzioni nell'elenco a discesa o aggiungerne una personalizzata.

    -   **Confermare l'apertura dopo il download**: selezionare questa casella di controllo per visualizzare un messaggio di conferma dopo il caricamento di un file. Se questa casella è selezionata, quando si tenta di aprire un file di questo tipo mediante il download in un Web browser, il browser chiede se si vuole salvare il file invece di aprirlo direttamente nel browser senza conferma.

    -   **Mostra sempre estensione**: selezionare questa casella di controllo per specificare che le estensioni devono essere visualizzate anche quando l'utente richiede che il sistema nasconda le estensioni per i tipi di file noti.

    -   **Aggiungi a nuovo menu**: selezionare questa casella di controllo per specificare che l'estensione o le estensioni devono essere elencate nel **nuovo** menu di scelta rapida della shell.

    -   **Applica a tutti gli utenti**: selezionare questa casella di controllo per specificare che le estensioni devono essere disponibili per tutti gli utenti.

<a href="" id="help"></a>**Help**  
Visualizza il sistema di guida della console di gestione client.

Per visualizzare le opzioni generali per il riquadro dei **risultati** , fare clic con il pulsante destro del mouse in un punto qualsiasi del riquadro **dei risultati** per visualizzare un menu a comparsa contenente gli elementi seguenti.

<a href="" id="new-association"></a>**Nuova associazione**  
Questa voce di menu Visualizza la procedura guidata nuova associazione. Questa procedura guidata è costituita da due pagine:

1.  Immettere un'estensione del nome file nuova o esistente e associare l'estensione a un tipo di file:

    -   **Estensione**: immettere una nuova estensione del nome file. Questo campo è vuoto per impostazione predefinita.

    -   **Creare un nuovo tipo di file con questa descrizione**: selezionare questo pulsante di opzione per immettere una nuova descrizione del tipo di file nel campo attivo. Questo pulsante è selezionato per impostazione predefinita e il campo attivo è vuoto.

    -   **Applica questo tipo di file a tutti gli utenti**: selezionare questa casella di controllo quando si vuole che l'associazione sia globale per tutti gli utenti. Per impostazione predefinita, questa casella non è selezionata.

    -   **Collegare questa estensione a un tipo di file esistente**: selezionare questo pulsante di opzione per associare l'estensione a un tipo di file esistente. Selezionare un tipo di file nell'elenco a discesa. Quando si sceglie questa opzione, il **successivo** viene modificato in **fine**.

2.  Selezionare l'applicazione che consente di aprire i file con l'estensione specificata:

    -   **Aprire i file con l'applicazione selezionata**: selezionare questo pulsante di opzione per aprire il file con un'applicazione esistente. Scegliere un'applicazione nell'elenco a discesa delle applicazioni disponibili.

    -   **Aprire il file con l'associazione descritta in questo file OSD**: selezionare questo pulsante di opzione per specificare un file OSD che determina l'applicazione usata per aprire il file. Usare il pulsante Sfoglia per selezionare una posizione esistente oppure immettere un percorso o un URL in formato HTTP in questo campo.

<a href="" id="refresh"></a>**Aggiorna**  
Questo elemento Aggiorna il riquadro **dei risultati** .

<a href="" id="export-list"></a>**Esporta elenco**  
Con questa voce di menu è possibile creare un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** . Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.

<a href="" id="view"></a>**Visualizza**  
Questo elenco popup di voce di menu consente di modificare l'aspetto e il contenuto del riquadro **risultati** .

<a href="" id="arrange-line-up-icons"></a>**Icone disponi/allineati**  
Queste voci di menu possono essere usate per cambiare la modalità di visualizzazione delle icone nel riquadro **dei risultati** .

<a href="" id="help"></a>**Help**  
Questo elemento Visualizza il sistema della Guida per la console di gestione.

## Argomenti correlati


[Come modificare l'icona di un'applicazione](how-to-change-an-application-icon.md)

[Nodo Associazioni del tipo di file](file-type-associations-node-client.md)

[Colonne del riquadro Risultati del nodo Associazioni del tipo di file](file-type-association-results-pane-columns.md)

 

 





