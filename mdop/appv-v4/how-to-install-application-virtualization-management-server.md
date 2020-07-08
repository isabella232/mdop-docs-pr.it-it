---
title: Come installare il server di gestione di Application Virtualization
description: Come installare il server di gestione di Application Virtualization
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817365"
---
# Come installare il server di gestione di Application Virtualization


L'Application Virtualization Management Server pubblica le proprie applicazioni ai client. In un ambiente con bilanciamento del carico, tipico delle distribuzioni di grandi dimensioni, tutti i server di un gruppo di server devono eseguire il flusso delle stesse applicazioni. Se i server di gestione della virtualizzazione dell'applicazione devono pubblicare applicazioni diverse, assegnare i server a gruppi di server diversi. In questo caso, potresti anche dover aumentare la capacità di un gruppo di server.

Se è stato designato un computer di destinazione nella rete, con un account di accesso con privilegi di amministratore locale, è possibile usare la procedura seguente per installare l'Application Virtualization Management Server e assegnarlo al gruppo di server appropriato.

**Nota**  
La procedura guidata di installazione può creare un record di gruppo di server, se non esiste, nonché un record dell'appartenenza dell'Application Virtualization Management Server in questo gruppo.



Dopo aver completato il processo di installazione, riavviare il server.

**Per installare un Application Virtualization Management Server**

1.  Verificare e, se necessario, disinstallare le versioni precedenti del server di gestione della virtualizzazione delle applicazioni installate nel computer di destinazione.

2.  Per aprire l' **installazione guidata di Microsoft Application Virtualization Management Server** , passare alla posizione del programma Application virtualization System **setup.exe** nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic sul file di **Setup.exe** .

3.  Nella pagina di **benvenuto** fare clic su **Avanti**.

4.  Nella pagina **contratto di licenza** leggere il contratto di licenza e, per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**. Fai clic su **Avanti**.

5.  Nella pagina **registrazione delle informazioni** è necessario immettere il nome utente e l' **organizzazione**. Fai clic su **Avanti**.

6.  Nella pagina **tipo di installazione** selezionare **personalizzato**. Fai clic su **Avanti**. Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema di virtualizzazione delle applicazioni eccetto **Application Virtualization Server**e quindi fare clic su **Avanti**.

    **Attenzione**  
    Se un componente è già installato nel computer, quando lo si deseleziona nella finestra di **configurazione personalizzata** , il componente viene disinstallato automaticamente.



7.  Nella pagina **database di configurazione** selezionare un server di database dall'elenco dei server disponibili o aggiungere un server selezionando **Usa il nome host seguente** e specificando il **nome del server** e i dati del numero di **porta** . Fai clic su **Avanti**.

    **Nota**  
    L'Application Virtualization Management Server non supporta SQL con distinzione tra maiuscole e minuscole.



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. Nella pagina **modalità di sicurezza della connessione** selezionare il certificato desiderato nell'elenco a discesa. Fai clic su **Avanti**.

   **Nota**  
   L'impostazione **modalità di connessione sicura** richiede al server di eseguire il provisioning di un certificato server da un'infrastruttura a chiave pubblica. Se nel server non è installato un certificato del server, questa opzione non è disponibile e non può essere selezionata. È necessario concedere all'account del servizio di rete l'accesso in lettura al certificato in uso.



9. Nella pagina di **configurazione della porta TCP** , per usare la porta predefinita (554), selezionare **Usa porta predefinita (554)**. Per specificare una porta personalizzata, selezionare **Usa porta personalizzata** e specificare il numero di porta che verrà usato. Fai clic su **Avanti**.

   **Nota**  
   Quando si installa il server in un ambiente non sicuro, è possibile usare la porta predefinita (554) oppure definire una porta personalizzata.



10. Nella pagina del **gruppo amministratore** specificare il nome del gruppo di sicurezza autorizzato per la gestione del server in **nome gruppo**. Fai clic su **Avanti**. Confermare il gruppo specificato e fare clic su **Avanti**.

11. Nella pagina del **gruppo provider predefinito** specificare il nome del gruppo di provider predefinito e quindi fare clic su **Avanti**.

12. Nella pagina **percorso contenuto** specificare la posizione nel computer di destinazione in cui verranno salvati i file SFT e quindi fare clic su **Avanti**.

   **Nota**  
   Se la porta HTTP o RTSP per il server di gestione è già allocata, verrà richiesto di scegliere una nuova porta. Selezionare la porta desiderata e quindi fare clic su **Avanti**.



13. Nella pagina **pronto per l'installazione del programma** , per installare Application Virtualization Management Server, fare clic su **Installa**.

   **Nota**  
   Se quando si prova a completare questo passaggio viene visualizzato l'errore 25120, è necessario abilitare **gli strumenti e gli script di gestione di**IIS. Per abilitare questa funzionalità di Windows, aprire il pannello di controllo **programmi e funzionalità** , selezionare **attiva o disattiva le funzionalità di Windows**e passare a **Internet Information Services.**

   In **strumenti di gestione Web**abilitare **gli script e gli strumenti di gestione di IIS**.



14. Nella schermata di **installazione guidata completata** , per chiudere la procedura guidata, fare clic su **fine**.

   **Importante**  
   L'installazione può richiedere alcuni minuti per terminare. Un messaggio di stato lampeggerà sopra l'area di notifica desktop di Windows, indicando che l'installazione è riuscita.

   Quando richiesto, non è necessario riavviare il computer. Tuttavia, per ottimizzare le prestazioni del sistema, è consigliabile un riavvio.



## Argomenti correlati


[Come installare i server e i componenti del sistema](how-to-install-the-servers-and-system-components.md)









