---
title: Come installare il server di report in un computer autonomo e connetterlo al database
description: Come installare il server di report in un computer autonomo e connetterlo al database
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805379"
---
# Come installare il server di report in un computer autonomo e connetterlo al database

Usare la procedura seguente per installare il server di report in un computer autonomo e connetterlo al database.

**Importante** Prima di eseguire la procedura seguente, è necessario leggere e comprendere [informazioni sui report di App-V 5,1](about-app-v-51-reporting.md).

## Per installare il server di report in un computer autonomo e connetterlo al database

1. Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo. Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore. Fai clic su **Installa**.

2. Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.

3. In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).** Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**. Fai clic su **Avanti**.

4. Nella pagina **Selezione funzionalità** selezionare la casella di controllo del **Server dei report** e fare clic su **Avanti**.

5. Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.

6. Nella pagina **Configura database di report esistente** selezionare **Usa un server SQL remoto**e digitare il nome del computer che ha eseguito Microsoft SQL Server, ad esempio **SqlServerMachine**.

    > [!NOTE]
    > Se Microsoft SQL Server è distribuito nello stesso server, selezionare **Usa SQL Server locale**.

    Per l'istanza di SQL Server, selezionare **Usa l'istanza predefinita**. Se si usa un'istanza di Microsoft SQL Server personalizzata, è necessario selezionare **Usa un'istanza personalizzata** e quindi digitare il nome dell'istanza.

    Specificare il **nome del database di SQL Server** che verrà usato da questo server di report, ad esempio **AppvReporting**.

7. Nella pagina **configura configurazione del server di Reporting** .

   - Specificare il nome del sito Web che si vuole usare per il servizio di creazione di report. Se non si ha un nome personalizzato, lasciarlo invariato.

   - Per il **Binding della porta**, specifica un numero di porta univoco che verrà usato da App-V 5,1, ad esempio **55555**. Devi anche assicurarti che la porta specificata non venga usata da un altro sito Web.

8. Fai clic su **Installa**.

**Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati

[Informazioni sulla creazione di report in App-V 5.1](about-app-v-51-reporting.md)

[Distribuzione di App-V 5.1](deploying-app-v-51.md)

[Come abilitare la creazione di report nel client App-V 5.1 con PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
