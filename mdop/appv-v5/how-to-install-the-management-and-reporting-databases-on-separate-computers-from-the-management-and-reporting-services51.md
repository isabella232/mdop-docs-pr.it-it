---
title: Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report
description: Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report
author: dansimp
ms.assetid: 2a67402e-3119-40ea-a247-24d166af1ced
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2332f674f10a9b60aa1cee814c6eac4ddbe4f5af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805422"
---
# Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report

Usare la procedura seguente per installare il server di database e il server di gestione in computer diversi. Il computer in cui si prevede di installare il server di database deve eseguire una versione supportata di Microsoft SQL o l'installazione avrà esito negativo.

> [!NOTE]
> Dopo aver completato la distribuzione, il nome di **Microsoft SQL Server**, il nome dell' **istanza** e il nome del **database** verranno richiesti dall'amministratore che installa il servizio per potersi connettere a questi database.

## Per installare il database di gestione e il server di gestione in computer separati

1. Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo. Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore. Fai clic su **Installa**.
1. Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.
1. In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).** Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**. Fai clic su **Avanti**.
1. Nella pagina **Selezione funzionalità** selezionare i componenti che si desidera installare selezionando la casella di **controllo database server di gestione** e fare clic su **Avanti**.
1. Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.
1. Nella **pagina Crea nuovo database del server di gestione**iniziale accettare le selezioni predefinite, se necessario, e fare clic su **Avanti**.

    Se si usa un'istanza di SQL Server personalizzata, selezionare **Usa un'istanza personalizzata** e digitare il nome dell'istanza. \
    Se si usa un nome di database personalizzato, selezionare **configurazione personalizzata** e digitare il nome del database.

1. Nella pagina **Crea nuovo database del server di gestione** selezionare **Usa un computer remoto**e digitare l'account del computer remoto usando il formato seguente: **Domain\\MachineAccount**.

    > [!NOTE]
    > Se si prevede di distribuire il server di gestione nello stesso computer, è necessario selezionare **Usa questo computer locale**.

1. Specificare il nome utente per l'amministratore di **installazione** del server di gestione con il formato seguente: **Domain\\AdministratorLoginName**. Fai clic su **Avanti**.
1. Per avviare l'installazione, fare clic su **Installa**.

## Per installare il database delle relazioni e il server di report in computer separati

1. Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo. Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore. Fai clic su **Installa**.
1. Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.
1. In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).** Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**. Fai clic su **Avanti**.
1. Nella pagina **Selezione funzionalità** selezionare i componenti da installare selezionando la casella di controllo **database server report** e fare clic su **Avanti**.
1. Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.
1. Nella pagina iniziale **Crea nuovo database del server di Reporting** accettare le selezioni predefinite, se necessario, e fare clic su **Avanti**.

    Se si usa un'istanza di SQL Server personalizzata, selezionare **Usa un'istanza personalizzata** e digitare il nome dell'istanza.
    Se si usa un nome di database personalizzato, selezionare **configurazione personalizzata** e digitare il nome del database.

1. Nella pagina **Crea nuovo database del server di Reporting** selezionare **Usa un computer remoto**e digitare l'account del computer remoto usando il formato seguente: **Domain\\MachineAccount**.

    > [!NOTE]
    > Se si prevede di distribuire il server di report nello stesso computer, è necessario selezionare **Usa questo computer locale**.

1. Specificare il nome utente per l'amministratore dell' **installazione** di Reporting Server con il formato seguente: **Domain\\AdministratorLoginName**. Fai clic su **Avanti**.
1. Per avviare l'installazione, fare clic su **Installa**.

## Per installare i database di gestione e Reporting usando gli script di database di App-V 5,1

1. Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo.
1. Per estrarre gli script di database di App-V 5,1, aprire un prompt dei comandi e specificare il percorso in cui vengono salvati i file di installazione ed eseguire il comando seguente:

    **appv\_server\_setup.exe** **/layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.

1. Dopo aver completato l'estrazione, per accedere agli script di database di App-V 5,1 e al file Leggimi delle istruzioni:

    - Gli script di database di gestione di App-V 5,1 e le istruzioni Leggimi si trovano nella cartella seguente: database di gestione degli script di database **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Management Database**.
    - I file di script e istruzioni del database di report App-V 5,1 si trovano nella cartella seguente: database di report degli script di database **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Reporting Database**.

1. Per ogni database, copiare gli script in una condivisione e modificarli seguendo le istruzioni nel file Leggimi.

    > [!NOTE]
    > Per altre informazioni sulla modifica dei SID necessari contenuti negli script, vedere [come installare i database di App-V e convertire gli identificatori di sicurezza associati tramite PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md).

1. Eseguire gli script nel computer che esegue Microsoft SQL Server.

**Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati

[Distribuzione di App-V 5.1](deploying-app-v-51.md)
