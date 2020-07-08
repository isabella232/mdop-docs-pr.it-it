---
title: Come configurare i server di pubblicazione
description: Come configurare i server di pubblicazione
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816526"
---
# Come configurare i server di pubblicazione


È possibile usare le procedure seguenti per aggiungere e configurare i server di virtualizzazione delle applicazioni direttamente dalla console di gestione client.

**Per aggiungere un server di pubblicazione delle applicazioni**

1.  Nel riquadro **dei risultati** fare clic con il pulsante destro del mouse e scegliere **nuovo server** dal menu a comparsa per avviare la procedura guidata nuovo Application Virtualization Server o in alternativa, fare clic con il pulsante destro del mouse sul nodo del **server di pubblicazione** e scegliere **nuovo server** dal menu a comparsa.

2.  Nella pagina uno della procedura guidata immettere il nome del server nel campo **nome visualizzato** e selezionare il tipo di server nell'elenco a discesa **tipo** . È possibile scegliere **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **standard HTTP server**o **Enhanced Security http server** dall'elenco a discesa dei tipi di server.

3.  Fai clic su **Avanti**.

4.  Nella pagina due della procedura guidata digitare le informazioni appropriate nei campi **nome host** e **porta** . Il campo **path** non è modificabile per i server di virtualizzazione dell'applicazione. È necessario immettere un percorso per un server HTTP standard o un server HTTP di sicurezza avanzato.

5.  Fare clic su **fine** per aggiungere il server.

**Per configurare un server di pubblicazione delle applicazioni**

1.  Nel riquadro **risultati** fare clic con il pulsante destro del mouse sul server desiderato e scegliere **Proprietà** dal menu a comparsa.

2.  Fare clic sulla scheda **generale** , in cui è possibile modificare il nome del server, selezionare un tipo nell'elenco a discesa dei tipi di server e specificare il nome host e la porta. Quando il tipo di server è un server HTTP standard o un server HTTP di sicurezza avanzato, anche il campo **path** è modificabile.

3.  Fare clic sulla scheda **Aggiorna** , in cui la casella di controllo **Aggiorna pubblicazione per l'accesso dell'utente** è selezionata per impostazione predefinita. Per modificare la frequenza di aggiornamento, selezionare la casella di controllo **Aggiorna pubblicazione ogni** e immettere un numero che rappresenti la frequenza nel campo. Quindi selezionare **minuti**, **ore**e **giorni** dal menu a discesa. (Il periodo di tempo minimo che puoi immettere è 30 minuti).

4.  Fare clic su **applica** per modificare la configurazione.

5.  Dopo aver completato la pubblicazione, fare clic su **OK** per uscire dalla finestra di dialogo e tornare alla console di gestione client.

## Argomenti correlati


[Come disabilitare o modificare le impostazioni della modalità di operazioni senza connessione](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





