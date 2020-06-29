---
title: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP2
description: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP2
author: dansimp
ms.assetid: 0593cd11-3308-4942-bf19-8a7bb9447f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 736eb8d41cbb72b274a2941c60b0357bbc948c9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820386"
---
# Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP2


Per cercare queste note sulla versione, premere CTRL + F.

Leggere accuratamente queste note sulla versione prima di installare Microsoft Advanced Group Policy Management (Advanced Pack2) 4.0 Service (SP2). Queste note sulla versione contengono informazioni necessarie per installare correttamente Advanced Group Policy Management 4.0 SP2 e contengono informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di Advanced Group Policy Management, considerare l'ultima modifica autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Problemi noti di Advanced Group Policy Management 4.0 SP2


In questa sezione vengono descritti i problemi noti per Advanced Group Policy Management SP2 4,0.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>Lo strumento "Disinstalla" del pannello di controllo potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management

Lo strumento nel pannello di controllo usato per disinstallare o modificare un programma potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management.

**Soluzione alternativa:** Prima di provare a modificare le impostazioni del server Advanced Group Policy Management tramite il pannello di controllo, creare una copia della cartella di archivio Advanced Group Policy Management. È quindi possibile usare Setup.exe per reinstallare il server Advanced Group Policy Management e scegliere i parametri di configurazione desiderati.

### I report non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo

Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo.

**Soluzione alternativa:** Per visualizzare i collegamenti nei report, selezionare l'oggetto Criteri di gruppo nella console Gestione criteri di Group (GPMC) e quindi fare clic sulla scheda **Impostazioni** nel riquadro destro.

### I report non visualizzano tutte le impostazioni delle proprietà delle opzioni di scelta

Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano tutte le impostazioni selezionate nella finestra **Proprietà opzioni scelta** nell'Editor oggetti Criteri di gruppo.

**Soluzione alternativa:** Usare la GPMC per visualizzare le impostazioni delle **proprietà delle opzioni di scelta** selezionate nei report.

### I report potrebbero non visualizzare le schede Mostra e Nascondi in alcuni browser

Quando si visualizzano i report in Google Chrome o Mozilla Firefox, le schede **Mostra** e **Nascondi** , sul lato destro delle impostazioni di Advanced Group Policy Management e dei report di differenza, potrebbero non essere visualizzate.

**Soluzione alternativa:** Visualizzare i report usando il browser Internet Explorer.

### Le impostazioni Advanced Group Policy Management e i report differenze possono mostrare contenuto diverso dai report di GPMC

Le impostazioni Advanced Group Policy Management e i report differenze potrebbero non mostrare lo stesso contenuto dei report in GPMC.

**Soluzione alternativa:** Usare la GPMC per visualizzare i report di Advanced Group Policy Management.

### Il servizio Advanced Group Policy Management non si avvia se il controller di dominio è offline

Quando il servizio Advanced Group Policy Management viene installato in un controller di dominio nei sistemi operativi Windows® 8 o versioni successive, il servizio non si avvia se il controller di dominio è offline.

**Soluzione alternativa:** Avviare manualmente il servizio Advanced Group Policy Management dopo che il controller di dominio è online.

### L'aggiornamento di Advanced Group Policy Management a Advanced Group Policy Management 4.0 SP2 viene bloccato quando si esegue l'aggiornamento da Advanced Group Policy Management 4.0 Release Plus Hotfix1

Se si tenta di aggiornare il server Advanced Group Policy Management a Advanced Group Policy Management 4,0. SP2 dopo l'installazione di Advanced Group Policy Management Server 4,0 e quindi l'installazione dell'hotfix di Advanced Group Policy Management denominato Advanced Management Packers 4,0 segnala le differenze non corrette nel report HTML (vedere l'articolo della Knowledge base [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), l'aggiornamento non viene completato

**Soluzione alternativa:** Disinstallare il server Advanced Group Policy Management e quindi installare Advanced Group Policy Management 4,0 4,0 SP2.

### I report non visualizzano i collegamenti delle unità organizzative

Se si collega un oggetto Criteri di gruppo non controllato a un'unità organizzativa e quindi si controlla tale oggetto Criteri di gruppo tramite Advanced Group Policy Management, i report delle impostazioni e delle differenze della gestione avanzata non visualizzeranno i collegamenti dell'unità organizzativa.

**Soluzione alternativa:** Nella scheda **controllo** del nodo **Cambia impostazioni** fare clic con il pulsante destro del mouse sull'oggetto Criteri di dialogo, scegliere **Impostazioni**e quindi fare clic su **collegamenti GPO** per visualizzare i collegamenti dell'organizzazione. In alternativa, puoi usare la GPMC per visualizzare i collegamenti a un GPO dalla scheda **ambito** .

### Advanced Group Policy Management Visualizza un errore se si fa clic sul pulsante Back della finestra di dialogo modifica, ripristina o Rimuovi client Advanced Group Policy Management

Se si passa a **programmi e funzionalità** nel pannello di controllo e quindi si seleziona **Gestione criteri di gruppo avanzati Microsoft-client**, Advanced Group Policy Management Visualizza un errore se si fa clic su **modifica** e quindi sul pulsante **Torna** nella finestra di dialogo **modifica, ripristina o Rimuovi client Advanced Group Policy** Management.

**Soluzione alternativa:** Fare clic su **Annulla** per cancellare l'errore e quindi riavviare di nuovo il processo. Non fare clic sul pulsante **Avanti** dopo aver fatto clic su **modifica** .

### Il commento non viene visualizzato nella finestra cronologia quando l'approvatore distribuisce un GPO e immette un commento

Se un utente che ha il ruolo di editor invia una richiesta di distribuzione di un oggetto Criteri di stato e l'utente che ha il ruolo di responsabile approvazione distribuisce il GPO e immette un commento, il commento non viene visualizzato nella finestra **cronologia** .

**Soluzione alternativa:** Nessuno.

## Argomenti correlati


[Gestione avanzata Criteri di gruppo](index.md)

[Novità di Gestione avanzata Criteri di gruppo 4.0 SP2](whats-new-in-agpm-40-sp2.md)

 

 





