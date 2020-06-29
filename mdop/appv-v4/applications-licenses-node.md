---
title: Nodo Licenze applicazione
description: Nodo Licenze applicazione
author: dansimp
ms.assetid: 2b8752ff-aa56-483e-b844-966941af2d94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 720de1860e72ae2c71298f93e9b346afd66da569
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819515"
---
# Nodo Licenze applicazione


Il nodo **licenze per le applicazioni** è un livello inferiore al nodo Application Virtualization System nel riquadro **ambito** della console di gestione di Application Virtualization Server. Quando si seleziona questo nodo, nel riquadro dei **risultati** viene visualizzato un elenco di licenze e gruppi di licenze. Sono disponibili i tipi di licenza seguenti:

-   **Licenza illimitata**: consente di accedere a qualsiasi numero di utenti simultanei. Questo metodo di gestione delle licenze è appropriato quando si vuole associare una licenza a livello aziendale a un'applicazione.

-   **Licenza simultanea**: consente di definire il numero massimo di utenti simultanei autorizzati a usare l'applicazione.

-   **Licenza denominata**: consente di assegnare una licenza a un singolo utente. Una licenza denominata può essere usata per garantire che un determinato utente sia sempre in grado di eseguire l'applicazione.

**Nota**  Puoi combinare licenze simultanee e denominate per la stessa applicazione.

 

Fare clic con il pulsante destro del mouse sul nodo **licenze applicazioni** per visualizzare un menu a comparsa contenente gli elementi seguenti.

<a href="" id="new-unlimited-license"></a>**Nuova licenza illimitata**  
Visualizza la procedura guidata nuova licenza illimitata. Questa procedura guidata è composta dalle pagine seguenti:

1.  Immettere il nome del gruppo di licenze nel campo **nome del gruppo di licenze** per le applicazioni e immettere un valore (in minuti) nel campo **Avviso scadenza licenza** . È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.

2.  Immettere un breve testo descrittivo nel campo **Descrizione licenza** e selezionare la casella di controllo **abilitata** per abilitare la licenza.

    Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza. È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.

3.  Fare clic su **fine** per aggiungere la nuova licenza.

<a href="" id="new-concurrent-license"></a>**Nuova licenza concorrente**  
Visualizza la creazione guidata nuova licenza simultanea. Questa procedura guidata è composta dalle tre pagine seguenti ed è quasi identica alla nuova procedura guidata licenza illimitata:

1.  Immettere il nome del gruppo di licenze nel campo **nome del gruppo di licenze** per le applicazioni e immettere un valore (in minuti) nel campo **Avviso scadenza licenza** . È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.

2.  Immettere un breve testo descrittivo nel campo **Descrizione licenza** e immettere un valore nel campo **quantità licenza simultanea** .

    È anche possibile usare le frecce su e giù per specificare il numero di licenze simultanee. Selezionare la casella di controllo **abilitata** per abilitare la licenza.

    Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza. È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.

3.  Fare clic su **fine** per aggiungere le nuove licenze.

<a href="" id="new-named-license"></a>**Nuova licenza denominata**  
Visualizza la procedura guidata nuova licenza denominata. Questa procedura guidata è composta dalle quattro pagine seguenti:

1.  Immettere il nome del gruppo di licenze nel campo **nome del gruppo di licenze** per le applicazioni e immettere un valore (in minuti) nel campo **Avviso scadenza licenza** . È possibile immettere qualsiasi valore compreso tra 0 e 100. È anche possibile usare le frecce su e giù per selezionare il numero di minuti.

2.  Immettere un breve testo descrittivo nel campo **Descrizione licenza** e selezionare la casella di controllo **abilitata** per abilitare la licenza.

    Facoltativamente, è possibile usare il campo **Data di scadenza** per specificare una data di scadenza per la licenza. È possibile selezionare la casella di controllo per usare la data di scadenza visualizzata oppure usare l'utilità calendario per passare alla data di scadenza desiderata.

3.  Fare clic su **Aggiungi**, **modifica**o **Rimuovi** utenti denominati.

4.  Fare clic su **fine** per aggiungere la nuova licenza.

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

Se si fa clic su un gruppo di licenze o una licenza visualizzata sotto il nodo **licenze applicazione** nel riquadro **ambito** , sono disponibili gli elementi seguenti.

<a href="" id="view"></a>**Visualizza**  
Modifica l'aspetto e il contenuto del riquadro dei **risultati** .

<a href="" id="new-window-from-here"></a>**Nuova finestra da qui**  
Apre una nuova console di gestione con il nodo selezionato come nodo radice.

<a href="" id="delete"></a>**Delete**  
Elimina un pacchetto dal riquadro **risultati** .

<a href="" id="rename"></a>**Rename**  
Modifica il nome di un pacchetto nel riquadro **dei risultati** .

<a href="" id="export-list"></a>**Esporta elenco**  
Crea un file di testo delimitato da tabulazioni contenente il contenuto del riquadro **risultati** . Questo elemento Visualizza una finestra di dialogo di **salvataggio file** standard in cui è possibile specificare la posizione del file di testo da creare.

<a href="" id="properties"></a>**Proprietà**  
Visualizza la finestra di dialogo **Proprietà** per il gruppo di licenze selezionato. La scheda **generale** della finestra di dialogo **Proprietà** consente di visualizzare le informazioni sul gruppo di licenze e di modificare il valore dell'ora nel campo **Avviso scadenza licenza** . Nella scheda **applicazioni** viene visualizzato l'elenco delle applicazioni associate al gruppo di licenze.

<a href="" id="help"></a>**Help**  
Visualizza il sistema della Guida per Application Virtualization Server Management Console.

## Argomenti correlati


[Informazioni sulle licenze dell'applicazione](about-application-licensing.md)

[Come gestire le licenze dell'applicazione in Server Management Console](how-to-manage-application-licenses-in-the-server-management-console.md)

[Server Management Console: Nodo Licenze applicazione](server-management-console-application-licenses-node.md)

 

 





