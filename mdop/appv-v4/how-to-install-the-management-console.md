---
title: Come installare la console di gestione
description: Come installare la console di gestione
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817305"
---
# Come installare la console di gestione


Per installare la console di gestione della virtualizzazione dell'applicazione in un computer di destinazione della rete, è possibile usare la procedura seguente. È necessario usare un account di rete con privilegi di amministratore nel computer di destinazione. Puoi usare la console per configurare e gestire la piattaforma di sistema di virtualizzazione dell'applicazione.

Prima di poter eseguire questa procedura, è necessario installare il servizio Web Application Virtualization Management in questo o in un altro computer. Il servizio Web di gestione consente di accedere all'archivio dati e al controller di dominio. Per altre informazioni sull'installazione del servizio Web, vedere [come installare il servizio Web di gestione](how-to-install-the-management-web-service.md).

**Per installare la console di gestione**

1.  Verificare che nel computer di destinazione non siano installate versioni precedenti della console di gestione.

2.  Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic su **Setup.exe**.

3.  Nella **pagina di benvenuto**fare clic su **Avanti**.

4.  Nella pagina **contratto di licenza** , per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**e quindi fare clic su **Avanti**.

5.  Nella pagina **informazioni di registrazione** specificare il **nome utente** e le informazioni sull' **organizzazione** e quindi fare clic su **Avanti**.

6.  Nella pagina **tipo di installazione** fare clic su **personalizzato** e quindi su **Avanti**.

7.  Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema di virtualizzazione delle applicazioni eccetto **console di gestione**e quindi fare clic su **Avanti**.

    **Nota**  Se un componente è già installato nel computer, deselezionarlo nella schermata di configurazione personalizzata verrà disinstallato automaticamente.

     

8.  Nella schermata **pronto per la modifica dello** schermo fare clic su **Installa**.

    **Nota**  Se si tratta del primo componente installato, verrà visualizzata la pagina **pronto per l'installazione** . Per avviare l'installazione, fare clic su **Installa**.

     

9.  Nella schermata **installazione guidata completata** fare clic su **fine**. Fare clic su **OK** per riavviare il computer e completare l'installazione.

10. Nel pannello di controllo di Windows fare doppio clic su **strumenti di amministrazione** e quindi su **Application Virtualization Management Console** per visualizzare la console di gestione.

11. Fai clic sull'icona **Connetti** oppure fai clic con il pulsante destro del mouse sul contenitore **Application Virtualization Systems** e quindi fai clic su **Connetti a Application Virtualization System**.

12. Nella schermata **Connetti a Application Virtualization System** immettere il nome host e la porta del computer del servizio Web di gestione, modificare le informazioni di sicurezza e le credenziali di accesso, se necessario, e quindi fare clic su **OK**.

13. Dopo aver effettuato la connessione al computer del servizio Web di gestione, fare clic su **file** dal menu **console** e quindi su **Esci**. Fare clic su **Sì** per salvare le impostazioni della console.

## Argomenti correlati


[Come installare i server e i componenti del sistema](how-to-install-the-servers-and-system-components.md)

 

 





