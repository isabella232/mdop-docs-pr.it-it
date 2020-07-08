---
title: Nodo Server di pubblicazione
description: Nodo Server di pubblicazione
author: dansimp
ms.assetid: b5823c6c-15bc-4e8d-aeeb-acc366ffedd1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c001e246c63919773d29a2317d5a43937c0813f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815796"
---
# Nodo Server di pubblicazione


Il nodo **server di pubblicazione** è un livello inferiore al nodo **Application Virtualization** nel riquadro **ambito** della console di gestione client di Application Virtualization. Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di server di pubblicazione.

Fare clic con il pulsante destro del mouse sul nodo **Publishing Servers** per visualizzare un menu di scelta rapida che contiene gli elementi seguenti.

<a href="" id="new-server"></a>**Nuovo server**  
Questa voce di menu Visualizza la procedura guidata nuovo server. Questa procedura guidata è costituita da due pagine:

1.  Immettere un nome visualizzato del server e un tipo di server:

    -   **Nome visualizzato**: immettere un nome che si vuole visualizzare per il server. Questo campo è vuoto per impostazione predefinita.

    -   **Tipo**: scegliere il tipo di server nell'elenco a discesa dei tipi di server.

2.  Specificare le impostazioni di connessione per il server:

    -   **Host name**: immettere il nome o l'indirizzo IP per il server.

    -   **Porta**: immettere un valore numerico corrispondente al numero di porta. Il valore predefinito è 554 se il tipo di server è "Application Virtualization Server" e 80 se il tipo di server è "server HTTP standard".

    -   **Path**: questo campo viene impostato su "/" ed è di sola lettura quando il tipo di server è "Application Virtualization Server" o "Enhanced Security Application Virtualization Server". Quando il tipo di server è "server HTTP standard" o "server HTTP di sicurezza avanzato", anche il campo **path** è modificabile.

<a href="" id="new-window-from-here"></a>**Nuova finestra da qui**  
Selezionare questa voce di menu per aprire una nuova console di gestione con il nodo selezionato come nodo radice.

<a href="" id="export-list"></a>**Esporta elenco**  
Puoi usare questa voce di menu per creare un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** . Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.

<a href="" id="view"></a>**Visualizza**  
Questo elenco popup di voci di menu consente di modificare l'aspetto e il contenuto del riquadro **risultati** .

<a href="" id="refresh"></a>**Aggiorna**  
Selezionare questa voce per aggiornare la console di gestione.

<a href="" id="help"></a>**Help**  
Questo elemento Visualizza il sistema della Guida per la console di gestione.

## Argomenti correlati


[Riquadro Risultati del nodo Server di pubblicazione](publishing-servers-results-pane.md)

[Colonne del riquadro Risultati del nodo Server di pubblicazione](publishing-servers-results-pane-columns.md)

 

 





