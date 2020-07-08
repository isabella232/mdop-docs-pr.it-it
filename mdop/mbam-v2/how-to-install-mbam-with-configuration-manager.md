---
title: Come installare MBAM con Configuration Manager
description: Come installare MBAM con Configuration Manager
author: dansimp
ms.assetid: fd0832e4-3b79-4e56-9550-d2f396be6d09
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a556ce961e6a423caecdd0766cf8623383897b58
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825126"
---
# Come installare MBAM con Configuration Manager


Questa sezione descrive i passaggi per installare MBAM con Configuration Manager usando la configurazione consigliata, illustrata in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). I passaggi sono suddivisi nelle attività seguenti:

-   Installare e configurare MBAM nel server Configuration Manager

-   Installare i database di ripristino e controllo nel server di database

-   Installare le caratteristiche del server di amministrazione e monitoraggio nel server di amministrazione e monitoraggio

Prima di iniziare l'installazione, verificare di aver modificato o creato i file MOF necessari. Per istruzioni, vedere [come creare o modificare i file MOF](how-to-create-or-edit-the-mof-files.md).

**Importante**  Se si usa un'istanza di SQL Server Reporting Services (SSRS) non predefinita, è necessario avviare la configurazione di MBAM usando la riga di comando seguente per specificare l'istanza denominata SSRS:

`MbamSetup.exe CM_SSRS_INSTANCE_NAME=<NamedInstance>`

 

**Per installare MBAM nel server Configuration Manager**

1.  Nel server Configuration Manager eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.

    **Nota**  Per ottenere i file di log di configurazione, è necessario usare il pacchetto msiexec e l'opzione **/l** &lt; location &gt; per installare Configuration Manager. I file di log vengono creati nella posizione specificata.

    I file di log di installazione aggiuntivi vengono creati nella cartella% Temp% nel computer dell'utente che sta installando Configuration Manager.

     

2.  Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** selezionare **integrazione di System Center Configuration Manager**e quindi fare clic su **Avanti**.

5.  Nella pagina **selezionare le caratteristiche da installare** selezionare **System Center Configuration Manager Integration**.

    **Nota**  Nella pagina **Verifica prerequisiti** fare clic su **Avanti** dopo che l'installazione guidata controlla i prerequisiti per l'installazione e conferma che non sono mancanti. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti.**

     

6.  Specificare se usare gli aggiornamenti Microsoft per proteggere il computer e quindi fare clic su **Avanti**. L'uso di Microsoft Updates non consente di attivare gli aggiornamenti automatici in Windows.

7.  Fai clic su **Next** per continuare.

8.  Nella pagina **Riepilogo installazione** esaminare l'elenco delle caratteristiche che verranno installate e fare clic su **Installa** per avviare l'installazione delle funzionalità di mbam. Fare clic su **Torna** per tornare alla procedura guidata se è necessario rivedere o modificare le impostazioni di installazione oppure fare clic su **Annulla** per uscire dalla configurazione. Il programma di installazione installa le caratteristiche di MBAM e informa che l'installazione è stata completata.

9.  Fare clic su **fine** per chiudere la procedura guidata.

**Per installare i database di ripristino e controllo nel server di database**

1.  Nel server database eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.

2.  Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** selezionare la topologia di **integrazione di System Center Configuration Manager** e quindi fare clic su **Avanti**.

5.  Dall'elenco delle caratteristiche da installare selezionare database di **ripristino** e **database di controllo**e deselezionare le caratteristiche rimanenti.

    **Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti. Se tutti i prerequisiti sono soddisfatti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.

     

6.  Nella pagina **Configura database di ripristino** specificare i nomi dei computer in cui verrà eseguita la funzionalità di amministrazione e monitoraggio Server. Dopo la distribuzione della funzionalità di amministrazione e monitoraggio del server, usa il proprio account di dominio per connettersi al database.

7.  Fai clic su **Next** per continuare.

8.  Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di ripristino. È inoltre necessario specificare sia la posizione in cui si trova il database, sia dove verranno individuate le informazioni sul log.

9.  Fare clic su **Avanti** per continuare con l'installazione guidata di mbam setup.

10. Nella pagina **Configura database di controllo** specificare l'account utente che verrà usato per accedere al database per i report.

11. Specificare i nomi di computer dei computer in cui verranno eseguiti il server di amministrazione e monitoraggio e i report di controllo. Dopo la distribuzione delle funzionalità Amministrazione e monitoraggio e report di controllo, gli account di dominio verranno usati per la connessione ai database.

    **Nota**  Se si sta installando il database di controllo senza la caratteristica rapporti di controllo, è necessario aggiungere un'eccezione nel computer del database di controllo per abilitare il traffico in ingresso nella porta di Microsoft SQL Server. Il numero di porta predefinito è 1433.

     

12. Specificare il nome dell'istanza di SQL Server e il nome del database in cui verranno archiviati i dati di controllo. Devi anche specificare la posizione in cui verranno individuate le informazioni sul database e sul log.

13. Fare clic su **Installa** per avviare l'installazione e quindi fare clic su **fine** per completare l'installazione.

**Per installare le funzionalità di amministrazione e monitoraggio del server nel server di amministrazione e monitoraggio**

1.  Nel server di amministrazione e monitoraggio eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.

2.  Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.

3.  Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.

4.  Nella pagina **Selezione topologia** selezionare la topologia di **integrazione di System Center Configuration Manager** e quindi fare clic su **Avanti**.

5.  Dall'elenco delle caratteristiche da installare selezionare **amministrazione e monitoraggio del server** e del **portale self-service**e deselezionare le caratteristiche rimanenti.

    **Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti. Se tutti i prerequisiti sono soddisfatti, l'installazione continua. Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**. Se tutti i prerequisiti vengono soddisfatti questa volta, l'installazione riprende.

     

6.  Installare il portale self-service seguendo la procedura descritta nella sezione **per installare il portale self-service** in [come installare e configurare mbam nei server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

    **Nota**  Se i computer client non avranno accesso alla rete di distribuzione dei contenuti Microsoft (CDN), che fornisce al portale self-service l'accesso necessario a determinati file JavaScript, completare i passaggi descritti in **per configurare il portale self-service quando gli utenti finali non possono accedere alla sezione della rete di distribuzione dei contenuti Microsoft** [come installare e configurare mbam nei server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md) per configurare il portale self-service per fare riferimento ai file JavaScript da un'origine accessibile.

     

7.  Installare le funzionalità di amministrazione e monitoraggio del server eseguendo la procedura descritta nella sezione **per installare la caratteristica del server di amministrazione e monitoraggio** in [come installare e configurare mbam nei server distribuiti](how-to-install-and-configure-mbam-on-distributed-servers-mbam-2.md).

8.  Fare clic su **fine** per completare l'installazione.

## Argomenti correlati


[Come convalidare l'installazione di MBAM con Configuration Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

[Distribuzione di MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





