---
title: Nodo Criteri dei provider
description: Nodo Criteri dei provider
author: dansimp
ms.assetid: 89b47076-7732-4128-93cc-8e6d5b671c8e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221171b22471a4a8614b13023b24dd21fd571dd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815835"
---
# Nodo Criteri dei provider


Il nodo **criteri provider** è un livello inferiore al nodo Application Virtualization System nel riquadro **ambito** della console di gestione di Application Virtualization Server. Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di criteri per il provider. Fare clic con il pulsante destro del mouse sul nodo **criteri provider** per visualizzare un menu a comparsa contenente gli elementi seguenti.

<a href="" id="new-provider-policy"></a>**Nuovi criteri per i provider**  
Visualizza la creazione guidata nuovo criterio provider. Questa procedura guidata è composta dalle pagine seguenti:

1.  Immettere un nome nel campo **Nome criterio provider** . Selezionare la casella di controllo **Gestisci desktop client tramite la console di gestione** se si vuole che tale funzionalità. Selezionare una o entrambe le caselle di controllo seguenti se si vuole eseguire la funzionalità associata:

    -   **Aggiornare la configurazione di pubblicazione quando un utente accede**

    -   **Aggiornare la configurazione ogni**. Dopo aver selezionato questa opzione, immettere un numero e selezionare l'unità dal menu a discesa. Le voci valide variano da un minimo di **30 minuti** a un massimo di **999 giorni**.

2.  Fare clic su **Aggiungi** o **Rimuovi** per aggiungere o rimuovere un'assegnazione di gruppo. Usare la finestra di dialogo Esplora **Windows** standard per trovare un gruppo di utenti.

3.  Selezionare una delle caselle di controllo seguenti nella finestra di dialogo **configurazione pipeline provider** per abilitare la caratteristica associata:

    -   **Autenticazione**: selezionare il tipo di autenticazione nell'elenco a discesa.

    -   **Applicare le impostazioni di autorizzazione di accesso**

    -   **Informazioni sull'utilizzo del log**

    -   **Licenze**: selezionare uno schema di imposizione dall'elenco a discesa.

4.  Fare clic su **fine** per aggiungere i nuovi criteri del provider.

<a href="" id="view"></a>**Visualizza**  
Modifica l'aspetto e il contenuto del riquadro dei **risultati** .

<a href="" id="new-window-from-here"></a>**Nuova finestra da qui**  
Apre una nuova console di gestione con il nodo selezionato come nodo radice.

<a href="" id="refresh"></a>**Aggiorna**  
Aggiorna la visualizzazione del server.

<a href="" id="export-list"></a>**Esporta elenco**  
Crea un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** . Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.

<a href="" id="help"></a>**Help**  
Visualizza il sistema della Guida per Application Virtualization Server Management Console.

## Argomenti correlati


[Server Management Console: Nodo Criteri dei provider](server-management-console-provider-policies-node.md)

 

 





