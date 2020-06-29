---
title: Configurare registrazione e traccia
description: Configurare registrazione e traccia
author: dansimp
ms.assetid: 419231f9-e9db-4f91-a7cf-a0a73db25256
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa3dfa71edb25f6641ade595cd4469e846410ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818975"
---
# Configurare registrazione e traccia


È possibile configurare centralmente la registrazione e la traccia facoltative per Advanced Group Policy Management (Advanced criteri di gruppo) usando modelli amministrativi.

Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie per la gestione dei criteri di raggruppamento avanzati è necessario per completare queste procedure. Inoltre, è necessario un account utente con accesso al server Advanced Group Policy Management per avviare la registrazione nel server Advanced Group Policy Management. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per configurare la registrazione e la traccia per Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento per cui si vuole attivare la registrazione e la traccia. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md)di ricerca.

2.  Nell' **Editor oggetti Criteri di gruppo**fare clic su **Configurazione computer**, **modelli amministrativi**e **componenti di Windows**.

3.  Se **Advanced Group Policy Management** non è elencato in **componenti di Windows**:

    1.  Fare clic con il pulsante destro del mouse su **modelli amministrativi** e scegliere **Aggiungi/Rimuovi modelli**.

    2.  Fare clic su **Aggiungi**, selezionare **Advanced Group Policy Management. admx** o **Advanced Group Policy Management. adm**, fare clic su **Apri**e quindi su **Chiudi**.

4.  In **componenti di Windows**fare doppio clic su **Advanced Group Policy Management**.

5.  Nel riquadro dei dettagli fare doppio clic su **registrazione Advanced Group Policy Management**.

6.  Nella finestra **Proprietà registrazione Advanced Group Policy Management** fare clic su **Enabled**e configurare il livello di dettaglio da registrare nei registri.

7.  Fai clic su **OK**.

8.  Chiudere l' **Editor oggetti Criteri di gruppo**. Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo.md)di ricerca. Dopo l'aggiornamento dei criteri di gruppo, è necessario riavviare il servizio Advanced Group Policy Management per iniziare la registrazione nel server Advanced Group Policy Management. Gli amministratori dei criteri di gruppo devono chiudere e riavviare la GPMC per iniziare la registrazione nei propri computer.

    **Percorsi dei file di traccia**:

    -   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Considerazioni aggiuntive

-   È necessario essere in grado di modificare e distribuire un GPO per configurare la registrazione e la traccia di Advanced Group Policy Management. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo.md) .

### Riferimenti aggiuntivi

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks.md)

 

 





