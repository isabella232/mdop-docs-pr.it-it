---
title: Configurare registrazione e traccia
description: Configurare registrazione e traccia
author: dansimp
ms.assetid: 2418cb6a-7189-4080-8fe2-9c8d47dec62c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bfc56d418ae83cbc5db24246bfac057305629df7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818966"
---
# Configurare registrazione e traccia


È possibile configurare centralmente la registrazione e la traccia facoltativa usando i modelli amministrativi. Può essere utile quando si diagnosticano eventuali problemi relativi alla gestione avanzata Criteri di gruppo.

Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente con le autorizzazioni necessarie in Advanced Group Policy Management è necessario per completare queste procedure. Inoltre, è necessario un account utente con accesso al server Advanced Group Policy Management per avviare la registrazione nel server Advanced Group Policy Management. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per configurare la registrazione e la traccia per Advanced Group Policy Management**

1.  Nell'albero della **console di gestione di criteri di gruppo** modificare un oggetto Criteri di gruppo applicato a tutti gli amministratori dei criteri di raggruppamento per cui si vuole attivare la registrazione e la traccia. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm40.md)di ricerca.

2.  Nella finestra **Editor gestione criteri di gruppo** fare clic su **Configurazione computer**, **criteri**, **modelli amministrativi**, **componenti di Windows**e **Advanced Group Policy**Management.

3.  Nel riquadro dei dettagli fare doppio clic su **Advanced Group Policy Management: configurare la registrazione**.

4.  Nella finestra **Proprietà** fare clic su **abilitato**e configurare il livello di dettaglio da registrare nei registri.

5.  Fai clic su **OK**.

6.  Chiudere la finestra **Editor gestione criteri di gruppo** . Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm40.md)di ricerca. Dopo l'aggiornamento dei criteri di gruppo, è necessario riavviare il servizio Advanced Group Policy Management per avviare, modificare o interrompere la registrazione nel server Advanced Group Policy Management. Gli amministratori dei criteri di gruppo devono chiudere e riavviare la console GPMC per avviare, modificare o interrompere la registrazione nei propri computer.

    **Percorsi dei file di traccia**:

    -   Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log

    -   Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log

### Considerazioni aggiuntive

-   È necessario essere in grado di modificare e distribuire un GPO per configurare la registrazione e la traccia di Advanced Group Policy Management. Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm40.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo-agpm40.md) .

### Riferimenti aggiuntivi

-   [Configurazione di Gestione avanzata Criteri di gruppo](configuring-advanced-group-policy-management-agpm40.md)

 

 





