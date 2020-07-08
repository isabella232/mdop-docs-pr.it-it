---
title: Come installare il servizio Gestione Web
description: Come installare il servizio Gestione Web
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817276"
---
# Come installare il servizio Gestione Web


Usare la procedura seguente per installare il servizio Web Application Virtualization Management in un computer di destinazione in rete, con un account di accesso con privilegi amministrativi locali. Anche se non è necessario, è consigliabile installare questo componente nel server Web.

**Per installare il servizio Web di gestione**

1.  Verificare che nel computer di destinazione non siano installate versioni precedenti del servizio Web Application Virtualization.

2.  Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic su **Setup.exe**.

3.  Dopo l'apertura della procedura guidata, nella pagina **iniziale** fare clic su **Avanti**.

4.  Nella pagina **contratto di licenza** , per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**e quindi fare clic su **Avanti**.

5.  Nella pagina **informazioni di registrazione** specificare il **nome utente** e le informazioni sull'organizzazione e quindi fare clic su **Avanti**.

6.  Nella pagina **tipo di installazione** fare clic su **personalizzato**e quindi su **Avanti**.

    **Nota**  Se non si tratta del primo componente installato nel computer, verrà visualizzata la pagina **manutenzione programmi** . Nella pagina **Manutenzione programma** fare clic su **modifica**.

     

7.  Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema per la virtualizzazione delle applicazioni tranne il **servizio di gestione virt app**e quindi fare clic su **Avanti**.

    **Nota**  Se un componente è già installato nel computer, deselezionarlo nella pagina **configurazione personalizzata** , lo si disinstalla automaticamente.

     

8.  Nella pagina **server database** fare clic su **Connetti a database disponibile**e quindi su **Avanti**.

    **Nota**  In un ambiente di produzione, Microsoft presuppone che si collegherà a un database esistente. Se si vuole installare un database, vedere [come installare un database](how-to-install-a-database.md). Dopo aver installato il database, procedere con il passaggio 13.

     

9.  Nella pagina **tipo di server database** selezionare un tipo di database nell'elenco e quindi fare clic su **Avanti**.

10. Nella pagina **percorso del server di database** selezionare un server di database nell'elenco dei server disponibili o aggiungere un server selezionando la casella di controllo **Usa il nome host seguente** e immettendo le informazioni nelle caselle **nome server** e **numero di porta** e quindi fare clic su **Avanti**.

11. Nella pagina **Seleziona database** selezionare il database desiderato e quindi fare clic su **Avanti**.

12. Nella pagina **Configurazione utente database** immettere le credenziali che verranno usate dal servizio Web di gestione per accedere all'archivio dati e quindi fare clic su **Avanti**.

13. Nella pagina **pronto per la modifica del programma** fare clic su **Installa**.

    **Nota**  Se si tratta del primo componente installato, verrà visualizzata la pagina **pronto per l'installazione** . Nella pagina fare clic su **Installa**.

     

14. Nella pagina **installazione guidata completare** fare clic su **fine**.

## Argomenti correlati


[Come installare i server e i componenti del sistema](how-to-install-the-servers-and-system-components.md)

 

 





