---
title: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1
description: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818535"
---
# Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1


Per cercare queste note sulla versione, premere CTRL + F.

Leggere accuratamente queste note sulla versione prima di installare Microsoft Advanced Group Policy Management (Advanced Manager criteri di gruppo) 4,0 SP1. Queste note sulla versione contengono informazioni necessarie per installare correttamente Advanced Policy Management Pack-4,0 SP1 e contengono informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altra documentazione per Advanced Group Policy Management, la modifica più recente deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Problemi noti di Advanced Group Policy Management 4,0


Questa sezione contiene le note sulla versione per Advanced Group Policy Management 4,0 SP1.

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a>Lo strumento "Disinstalla" del pannello di controllo potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management

Lo strumento nel pannello di controllo che consente di disinstallare o modificare un programma potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management.

SOLUZIONE alternativa: prima di provare a modificare le impostazioni del server Advanced Group Policy Management tramite il pannello di controllo, creare una copia della cartella di archivio Advanced Group Policy Management. È quindi possibile usare Setup.exe per reinstallare il server Advanced Group Policy Management e scegliere i parametri di configurazione desiderati.

### I report non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo

Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo.

SOLUZIONE alternativa: per visualizzare i collegamenti nei report, selezionare l'oggetto Criteri di gruppo in console Gestione criteri di raggruppamento e fare clic sulla scheda **Impostazioni** nel riquadro destro.

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a>I report non visualizzano tutte le impostazioni "Proprietà opzioni scelte"

Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano tutte le impostazioni selezionate nella finestra Proprietà opzioni scelta nell'Editor oggetti Criteri di gruppo.

SOLUZIONE alternativa: usare la GPMC per visualizzare le impostazioni delle proprietà delle opzioni di scelta selezionate nei report.

### I report non visualizzano le schede Mostra e Nascondi in alcuni browser

Quando si visualizzano i report in Google Chrome o Mozilla Firefox, le schede Mostra e Nascondi, visualizzate sul lato destro delle impostazioni di Advanced Group Policy Management e dei report differenze, non vengono visualizzate.

SOLUZIONE alternativa: visualizzare i report usando Internet Explorer.

### Le impostazioni Advanced Group Policy Management e i report differenze possono mostrare contenuto diverso dai report di GPMC

Le impostazioni Advanced Group Policy Management e i report differenze potrebbero non mostrare lo stesso contenuto dei report nella console Gestione criteri di gruppo.

SOLUZIONE alternativa: usare la GPMC per visualizzare i report di Advanced Group Policy Management.

### Il servizio Advanced Group Policy Management non si avvia se il controller di dominio non è online

Quando il servizio Advanced Group Policy Management viene installato in un controller di dominio in Windows 8, il servizio non si avvia se il controller di dominio non è online.

SOLUZIONE alternativa: avviare manualmente il servizio Advanced Group Policy Management dopo che il controller di dominio è online.

### L'aggiornamento del server Advanced Group Policy Management a Advanced Group Policy Management 4,0 SP1 viene bloccato quando si esegue l'aggiornamento dalla versione Advanced Group Policy 4,0 Management

Se si tenta di aggiornare il server Advanced Group Policy Management a Advanced Group Policy Management 4,0. SP1 dopo l'installazione di Advanced Group Policy Management 4,0 e l'installazione dell'hotfix Advanced Group Policy Management (vedere l'articolo della Knowledge base [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), l'aggiornamento non riesce e non può essere completato

SOLUZIONE alternativa: disinstallare il server Advanced 4,0 Group Policy Management e quindi installare Advanced Group Policy Management 4,0 SP1.

### I report non visualizzano i collegamenti delle unità organizzative

Se si collega un oggetto Criteri di gruppo non controllato a un'unità organizzativa e quindi si controlla tale oggetto Criteri di gruppo tramite Advanced Group Policy Management, i report delle impostazioni e delle differenze della gestione avanzata non visualizzeranno i collegamenti dell'unità organizzativa.

SOLUZIONE alternativa: nella scheda **controllo** del nodo **Cambia impostazioni** fare clic con il pulsante destro del mouse sull'oggetto Criteri di dialogo e scegliere **Impostazioni** e quindi fare clic su **collegamenti GPO** per visualizzare i collegamenti dell'organizzazione. In alternativa, puoi usare la GPMC per visualizzare i collegamenti a un GPO dalla scheda **ambito** .

## Argomenti correlati


[Gestione avanzata Criteri di gruppo](index.md)

[Novità di Gestione avanzata Criteri di gruppo 4.0 SP1](whats-new-in-agpm-40-sp1.md)

 

 





