---
title: Riquadro Risultati del nodo Applicazioni
description: Riquadro Risultati del nodo Applicazioni
author: dansimp
ms.assetid: 977a4d35-5344-41fa-af66-14957b38ed47
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdabaeee0b9aaa1c96b6ae732ae4bb5b6d63ef3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819495"
---
# Riquadro Risultati del nodo Applicazioni


Nel riquadro **risultati applicazioni** della console di gestione client Application Virtualization viene visualizzato un elenco delle applicazioni disponibili. Gli utenti possono visualizzare un elenco di applicazioni per cui sono stati concessi privilegi di accesso.

Per altre informazioni sulle procedure che è possibile eseguire da questo riquadro, vedere [come gestire le applicazioni nella console di gestione client](how-to-manage-applications-in-the-client-management-console.md).

Fare clic con il pulsante destro del mouse su un'applicazione per visualizzare un menu a comparsa contenente gli elementi seguenti.

<a href="" id="new-shortcut"></a>**Nuovo collegamento**  
Questa voce di menu Visualizza la creazione guidata nuovo collegamento. Questa procedura guidata è costituita da tre pagine:

1.  Selezionare un'icona e specificare un nome per il collegamento:

    1.  **Icona cambia**: Visualizza un browser di icone standard di Windows. Individuare e selezionare l'icona desiderata.

    2.  **Titolo del collegamento**: immettere il nome che si vuole assegnare al collegamento. Questo campo viene impostato come predefinito per il nome e la versione esistenti dell'applicazione.

2.  Determinare la posizione del collegamento pubblicato.

    1.  **Posizione del collegamento**: selezionare una posizione selezionando una delle caselle di controllo. Le posizioni disponibili sono **Desktop**, **barra di avvio veloce**, **menu Invia a**, **menu Start**e **un'altra posizione**.

    2.  **Programmi nel menu Start**: quando si seleziona la casella di controllo **menu Start** , questo campo diventa attivo. Lascia vuoto questo campo per pubblicare il collegamento direttamente nella radice della cartella programmi oppure immetti un nome di cartella o una gerarchia, ad esempio "My \ _Computer applicazioni \\Office". I collegamenti creati in questo modo sono disponibili solo per l'utente corrente.

    3.  **Altro percorso** e pulsante Sfoglia: quando si seleziona la casella di controllo **altro percorso** , questo campo diventa attivo. Immettere una posizione valida nel computer o in qualsiasi percorso UNC (Universal Naming Convention) disponibile (file condiviso o directory in una rete). Il pulsante Sfoglia Visualizza una finestra di dialogo **Apri file** standard di Windows.

3.  Immettere i parametri della riga di comando desiderati e quindi fare clic su **fine** per chiudere la procedura guidata.

<a href="" id="new-association"></a>**Nuova associazione**  
Questa voce di menu Visualizza la procedura guidata nuova associazione. Questa procedura guidata è costituita da due pagine:

1.  Immettere un'estensione del nome file e associare l'estensione a un tipo di file.

    1.  **Estensione**: immettere un'estensione del nome file. Questo campo è vuoto per impostazione predefinita.

    2.  **Creare un nuovo tipo di file con questa descrizione**: selezionare questo pulsante di opzione per immettere una nuova descrizione del tipo di file nel campo attivo. Questo pulsante è selezionato per impostazione predefinita e il campo attivo è vuoto.

    3.  **Applica questo tipo di file a tutti gli utenti**: selezionare questa casella di controllo quando si vuole che l'associazione sia globale per tutti gli utenti. Per impostazione predefinita, questa casella non è selezionata.

    4.  **Collegare questa estensione a un tipo di file esistente**: selezionare questo pulsante di opzione per associare l'estensione a un tipo di file esistente. Scegliere un tipo di file nell'elenco a discesa. Quando si sceglie questa opzione, il **successivo** viene modificato in **fine**.

2.  Selezionare l'applicazione che consente di aprire i file con l'estensione specificata:

    1.  **Aprire i file con l'applicazione selezionata**: selezionare questo pulsante di opzione per aprire il file con un'applicazione esistente. Scegliere un'applicazione nell'elenco a discesa delle applicazioni disponibili.

    2.  **Aprire il file con l'associazione descritta in questo file OSD**: selezionare questo pulsante di opzione per specificare un file OSD (Open Software Descriptor) che determina l'applicazione usata per aprire il file. Usare il pulsante Sfoglia per selezionare una posizione esistente oppure immettere un percorso o un URL in formato HTTP in questo campo.

<a href="" id="repair"></a>**Repair**  
Reimposta le impostazioni predefinite dell'applicazione ed Elimina tutte le impostazioni definite dall'utente per l'applicazione selezionata.

<a href="" id="load-or-unload"></a>**Caricare** o **scaricare**  
Carica o Scarica l'applicazione selezionata nella cache. Questo comando non è disponibile se 100% dell'applicazione si trova nella cache.

<a href="" id="clear"></a>**Clear**  
Consente di rimuovere le impostazioni, le scelte rapide e le associazioni di tipi di file dell'utente per l'applicazione selezionata. Questo elemento non è disponibile se un utente ha in uso qualsiasi applicazione da una serie di applicazioni. Visualizza una richiesta di conferma.

<a href="" id="lock-or-unlock"></a>**Bloccare** o **sbloccare**  
Blocca o sblocca un'applicazione nella cache. Quando un'applicazione è bloccata, non può essere eliminata o sovrascritta.

<a href="" id="import"></a>**Import**  
Importa un'applicazione nella cache direttamente da questo comando nel nodo **applicazioni** .

<a href="" id="delete"></a>**Delete**  
Elimina un'applicazione dal riquadro **dei risultati** e dal computer e cancella l'applicazione dalla cache.

<a href="" id="refresh"></a>**Aggiorna**  
Aggiorna il contenuto del riquadro dei **risultati** .

<a href="" id="properties"></a>**Proprietà**  
Visualizza la finestra di dialogo **Proprietà** per l'applicazione selezionata. Questa finestra di dialogo include due schede:

1.  Nella scheda **generale** vengono visualizzate l'icona e il nome dell'applicazione, la posizione in cui è stata trasmessa l'applicazione e il percorso del file OSD locale. Da questa scheda è possibile modificare l'icona dell'applicazione o deselezionare le impostazioni (che rimuove i collegamenti e le associazioni di tipi di file).

2.  La scheda **pacchetto** Visualizza le informazioni sul pacchetto dell'applicazione ed è possibile **bloccare**, **sbloccare**, **caricare**, **scaricare**e **importare** applicazioni.

<a href="" id="help"></a>**Help**  
Visualizza il sistema di guida della console di gestione client.

## Visualizzazione delle opzioni generali per il riquadro risultati


Fare clic con il pulsante destro del mouse in un punto qualsiasi del riquadro **dei risultati** per visualizzare un menu a comparsa contenente gli elementi seguenti.

<a href="" id="new-application"></a>**Nuova applicazione**  
Questa voce di menu Visualizza la creazione guidata nuova applicazione. Questa procedura guidata è costituita da una pagina in cui è possibile selezionare un'icona per l'applicazione e cercare o immettere un URL o un percorso per il file OSD:

1.  **Icona cambia**: Visualizza un browser di icone standard di Windows. Individuare e selezionare l'icona desiderata.

2.  **URL o percorso file OSD**: immettere un percorso assoluto locale, un percorso UNC completo o un URL http.

3.  **... (Pulsante Sfoglia OSD)** -Visualizza la finestra di dialogo standard di Windows **Open file** . Individuare il file desiderato.

<a href="" id="refresh"></a>**Aggiorna**  
Aggiorna il riquadro **dei risultati** .

<a href="" id="export-list"></a>**Esporta elenco**  
Puoi usare questa voce di menu per creare un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** . Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.

<a href="" id="view"></a>**Visualizza**  
Questo elenco popup di voci di menu consente di modificare l'aspetto e il contenuto del riquadro **risultati** .

<a href="" id="arrange-line-up-icons"></a>**Icone disponi/allineati**  
Queste voci di menu possono essere usate per cambiare la modalità di visualizzazione delle icone nel riquadro **dei risultati** .

<a href="" id="help"></a>**Help**  
Visualizza il sistema della Guida per la console di gestione.

## Argomenti correlati


[Nodo Applicazioni](applications-node.md)

[Colonne del riquadro Risultati del nodo Applicazioni](applications-results-pane-columns.md)

[Riferimento per Application Virtualization Client Management Console](application-virtualization-client-management-console-reference.md)

[Come gestire le applicazioni in Client Management Console](how-to-manage-applications-in-the-client-management-console.md)

 

 





