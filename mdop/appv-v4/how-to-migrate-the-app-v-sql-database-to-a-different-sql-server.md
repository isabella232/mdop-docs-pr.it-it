---
title: Come eseguire la migrazione del database SQL di App-V in un server SQL diverso
description: Come eseguire la migrazione del database SQL di App-V in un server SQL diverso
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817075"
---
# Come eseguire la migrazione del database SQL di App-V in un server SQL diverso


Le procedure seguenti descrivono in dettaglio come eseguire la migrazione del database SQL del server di gestione di Microsoft Application Virtualization (App-V) a un server SQL diverso.

**Importante**  Questa procedura richiede che il servizio App-V Server venga interrotto e questo impedirà agli utenti finali di usare le proprie applicazioni.

 

**Per eseguire il backup del database SQL di App-V**

1.  Aprire il programma Services. msc e arrestare il servizio App-V Management Server in tutti i server di gestione che usano il database di cui eseguire la migrazione.

2.  Nel computer in cui si trova il database di App-V aprire SQL Server Management Studio.

3.  Espandere il nodo **database** e individuare il database App-V (il nome predefinito è APPVIRT).

4.  Fare clic con il pulsante destro del mouse sul database e scegliere **attività** e quindi selezionare **backup**.

5.  Verificare che il **modello di recupero** sia impostato su **semplice** e che il **tipo di backup** sia impostato su **completo**. Se necessario, modificare le impostazioni di **set di backup** e di **destinazione** .

6.  Fare clic su **OK** per eseguire il backup del database. Dopo che il backup è stato completato correttamente, fare clic su **OK**.

7.  Aprire Esplora risorse e passare alla cartella che contiene il file di backup del database, ad esempio APPVIRT. BAK. Copiare il file di backup del database nel computer di destinazione in cui è in uso SQL Server.

**Per ripristinare il database SQL di App-V nel computer di destinazione**

1.  Nel computer di destinazione aprire SQL Server Management Studio, fare clic con il pulsante destro del mouse sul nodo **database** e scegliere **Ripristina database**.

2.  In **origine per ripristino**scegliere **da dispositivo** e quindi fare clic su "**...**" .

3.  Nella finestra di dialogo **specifica backup** verificare che il supporto di **backup** sia impostato su **file** e quindi fare clic su **Aggiungi**.

4.  Selezionare il file di backup copiato dal computer originale in cui è in uso SQL Server e quindi fare clic su **OK**.

5.  Fare clic su **OK** e quindi su per selezionare il set di backup da ripristinare.

6.  In **destinazione per il ripristino**fare clic sull'elenco a discesa per il **database** e selezionare il nome del database App-V, ad esempio APPVIRT.

7.  Fare clic su **OK** per avviare il ripristino. Dopo che il ripristino è stato completato correttamente, fare clic su **OK**.

8.  Espandere il nodo di **sicurezza** , fare clic con il pulsante destro del mouse su **account di accesso** e scegliere **nuovo accesso**.

9.  Nel campo **nome login** immettere i dettagli dell'account del servizio di rete per l'App-V Management Server nel formato DOMAIN\\SERVERNAME $.

10. Nella pagina **generale** in **database predefinito** Selezionare il nome del database App-V, ad esempio APPVIRT, quindi fare clic su **OK**.

11. In **Seleziona una pagina**fare clic su per selezionare la pagina di **mapping utente** . In **utenti mappati a questo account di accesso**fare clic sulla casella di controllo nella colonna **mappa** per selezionare il database App-V.

12. In **appartenenza a ruoli del database per: &lt; appvdatabasename &gt; **, fare clic per selezionare **SFTEveryone** e quindi fare clic su **OK**.

13. Assicurarsi che Windows Firewall nel nuovo computer in cui è in corso SQL Server sia configurato per consentire l'accesso al sistema da parte di App-V Management Server. In **strumenti di amministrazione**usare il programma **Windows Firewall con sicurezza avanzata** per creare una **regola in entrata** per la porta utilizzata da SQL Server (il valore predefinito è la porta 1433).

**Per eseguire la migrazione dei processi di SQL Server Agent di App-V**

1.  Nel computer originale in cui è in uso SQL Server, in SQL Server Management Studio espandere il nodo **agente SQL Server** e quindi espandere il nodo **processi** .

2.  Fare clic con il pulsante destro del mouse sui quattro processi di App-V seguenti e scegliere **processo script come | Crea in | File**e salvare ogni script in una cartella e assegnare a ogni script un nome descrittivo.

    -   **Database di SoftGrid (appvdbname) controlla Cronologia utilizzo**

    -   **Database di SoftGrid (appvdbname) Chiudi sessioni orfane**

    -   **Database SoftGrid (appvdbname) applicare il limite di dimensione**

    -   **Database di SoftGrid (appvdbname) monitor Alert/stato processo**

3.  Copiare i quattro file di script (con estensione SQL) nel computer di destinazione in cui è in esecuzione SQL Server e aprire SQL Server Management Studio.

4.  In Esplora risorse fare clic con il pulsante destro del mouse su ogni file con estensione SQL e quindi scegliere **Esegui**. Ogni script viene aperto in una finestra di query in SQL Server Management Studio. Fare clic su **Esegui** per ogni script e verificare che ogni operazione sia stata completata correttamente.

5.  Aggiornare il nodo **processi** nel nodo **agente SQL Server** e verificare che i quattro processi vengano creati correttamente.

**Per aggiornare la configurazione di App-V Management Server**

1.  Nel server di gestione di App-V modificare le chiavi del registro di sistema seguenti:

    -   **Sqlservername**  =  &lt; newservername&gt;

    -   **SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;

    Riavvia quindi il servizio App-V Server.

2.  Individuare il file SftMgmt. udl nella directory di installazione di App-V Management Server (l'impostazione predefinita è C:\\Programmi \\Programmi\\microsoft System Center App Virt Management Server\\App Virt Management Service). Fare clic con il pulsante destro del mouse sul file e scegliere **Apri**.

3.  Nella scheda **connessione** immettere il nome del computer di destinazione in cui è in uso SQL Server e quindi fare clic su **Test connessione**. Quando il test ha esito positivo, fare di nuovo clic su **OK** e quindi su **OK** .

4.  Per le versioni di App-V Management Server prima di 4,5 SP2, è necessario aggiornare le impostazioni di registrazione SQL. In **gruppi di server**fare clic con il pulsante destro del mouse sul gruppo server a cui è associato il server e scegliere **Proprietà**.

5.  Nella scheda **registrazione** fare clic per selezionare la voce del **database SQL** e quindi fare clic su **modifica**.

6.  Cambiare il **nome host DNS** nel nome host del nuovo computer in cui è in uso SQL Server e quindi fare clic su **OK**. Fare clic su **OK** due volte di più e quindi riavviare il servizio App-V Server.

7.  Aprire la console di gestione di App-V, fare clic con il pulsante destro del mouse sul nodo delle **applicazioni** e scegliere **Aggiorna**. L'elenco delle applicazioni deve essere visualizzato come prima.

 

 





