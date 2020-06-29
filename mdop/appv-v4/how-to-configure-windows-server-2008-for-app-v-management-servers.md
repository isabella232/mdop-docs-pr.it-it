---
title: Come configurare Windows Server 2008 per i server di gestione di App-V
description: Come configurare Windows Server 2008 per i server di gestione di App-V
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817725"
---
# Come configurare Windows Server 2008 per i server di gestione di App-V


Il server Windows Server 2008 in cui si installa il servizio Web di gestione di Microsoft Application Virtualization (App-V) richiede l'installazione di Internet Information Services (IIS) come ruolo nel server. Usare la procedura seguente per configurare Windows Server 2008 per supportare l'installazione di app-Vserver.

**Per installare IIS in un computer Windows Server2008**

1.  Nel computer Windows Server2008 fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **strumenti di amministrazione**e quindi fare clic su **Gestione server** per avviare Server Manager. In Server Manager fare clic con il pulsante destro del mouse sul nodo **ruoli** e scegliere **Aggiungi ruoli** per avviare la **procedura guidata Aggiungi ruoli**.

2.  Nella pagina **Selezione ruoli server** della **procedura guidata Aggiungi ruoli**selezionare **Web Server (IIS)**. Quando richiesto, fare clic su **Aggiungi caratteristiche necessarie** per aggiungere le caratteristiche dipendenti.

3.  Nella pagina **Selezione ruoli server** fare clic su **Avanti**e quindi di nuovo su **Avanti** .

4.  Nella pagina **Seleziona servizi ruolo** della **procedura guidata Aggiungi ruoli**:

    1.  In **sviluppo applicazione**selezionare **ASP.NET** e, quando richiesto, fare clic su **Aggiungi servizi ruolo necessari** per aggiungere i servizi e le funzionalità dei ruoli dipendenti.

    2.  In **sicurezza**selezionare **autenticazione di Windows**.

    3.  Nel nodo **strumenti di gestione** selezionare **script e strumenti di gestione di IIS**. In **compatibilità**con la gestione di IIS6 verificare che sia selezionata la compatibilità della **metabase IIS6** e la **Compatibilità WMI di IIS6** e quindi fare clic su **Avanti**.

5.  Nella pagina **Conferma selezioni installazione** fare clic su **Installa**e quindi completare il resto della procedura guidata.

6.  Fare clic su **Chiudi** per uscire dalla **procedura guidata Aggiungi ruoli**e quindi chiudere Gestione server.

## Argomenti correlati


[Requisiti per la distribuzione di Application Virtualization](application-virtualization-deployment-requirements.md)

[Elenchi di controllo per la distribuzione e l'aggiornamento di Application Virtualization](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





