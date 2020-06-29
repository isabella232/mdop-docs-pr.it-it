---
title: Come configurare l'aggiornamento periodico per la pubblicazione
description: Come configurare l'aggiornamento periodico per la pubblicazione
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816555"
---
# Come configurare l'aggiornamento periodico per la pubblicazione


È possibile usare la procedura seguente per configurare il client per aggiornare periodicamente le informazioni di pubblicazione dai server App-V. Dopo aver configurato il client, l'operazione di aggiornamento è automatica. Queste impostazioni configurano le impostazioni predefinite per il client in modo che tutti gli utenti di questo computer visualizzino le stesse impostazioni.

**Nota**  Dopo aver eseguito questa procedura, le informazioni di pubblicazione verranno aggiornate in base alle nuove impostazioni dopo il primo aggiornamento all'accesso. Quando si verifica questo primo aggiornamento, il server può eseguire l'override delle impostazioni del computer con impostazioni diverse, a seconda del modo in cui è configurato. La scheda **Aggiorna** nella finestra di dialogo **Proprietà** Mostra le impostazioni del computer client configurate localmente e le impostazioni eventualmente configurate per l'utente dal server di pubblicazione.

 

**Per aggiornare periodicamente le informazioni di pubblicazione dall'Application Virtualization Server**

1.  Fare clic su **server di pubblicazione** nel riquadro **ambito** .

2.  Nel riquadro **risultati** fare clic con il pulsante destro del mouse sul server desiderato e scegliere **Proprietà** dal menu a comparsa.

3.  Nella scheda **Aggiorna** della finestra di dialogo **Proprietà** selezionare la casella di controllo **Aggiorna configurazione ogni** e immettere un numero che rappresenti la frequenza nel campo. Quindi selezionare **minuti**, **ore**e **giorni** dal menu a discesa.

    **Nota**  Questa impostazione farà sì che il client aggiorni le informazioni di pubblicazione ogni volta che il periodo configurato trascorre. Se l'utente non ha effettuato l'accesso quando è il momento di eseguire l'aggiornamento, l'aggiornamento avverrà quando l'utente esegue l'accesso. Il timer viene quindi riavviato per il periodo successivo.

     

4.  Fare clic su **applica** per modificare la configurazione.

5.  Al termine della configurazione del server, fare clic su **OK** per uscire dalla finestra di dialogo e tornare alla console di gestione client Application Virtualization.

## Argomenti correlati


[Come configurare il client in Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





