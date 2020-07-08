---
title: Come configurare la sicurezza di Management Server dopo l'installazione
description: Come configurare la sicurezza di Management Server dopo l'installazione
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817936"
---
# Come configurare la sicurezza di Management Server dopo l'installazione


Usare la console di gestione di App-V per aggiungere il certificato e configurare App-V Management Server per una maggiore sicurezza. Per configurare la sicurezza post-installazione, è possibile usare la procedura seguente.

**Per configurare la sicurezza del server di gestione dopo l'installazione**

1.  Aprire la console di gestione di App-V e connettersi al **servizio di gestione** con i privilegi di amministratore di App-v.

2.  Espandere il server, espandere **gruppi di server**e quindi selezionare il gruppo di server appropriato con cui è stato registrato il server di gestione.

3.  Fare clic con il pulsante destro del mouse sull'oggetto server di gestione e scegliere **Proprietà**.

4.  Nella scheda **porte** fare clic su **certificato server** e completare la procedura guidata per selezionare il certificato correttamente provisioning.

    **Nota**  Se non vengono visualizzati certificati nella procedura guidata, non è stato effettuato il provisioning di un certificato o il certificato soddisfa i requisiti di App-V.

     

5.  Fare clic su **Avanti** per passare alla pagina della **procedura guidata benvenuto in certificato** .

6.  Selezionare il certificato corretto nella schermata **certificati disponibili** .

7.  Fai clic su **Fine**.

8.  Dopo aver completato la procedura guidata, deselezionare **RTSP** come porta di ascolto disponibile. In questo modo viene impedito l'effettuazione di connessioni su un canale di comunicazione non sicuro.

9.  Fare clic su **applica**e riavviare il servizio **Microsoft Virtual Application Server** . Per eseguire questa attività, USA lo snap-in MMC del servizio.

## Argomenti correlati


[Come configurare la sicurezza di Streaming Server dopo l'installazione](how-to-configure-streaming-server-security-post-installation.md)

[Risoluzione dei problemi di autorizzazione dei certificati](troubleshooting-certificate-permission-issues.md)

 

 





