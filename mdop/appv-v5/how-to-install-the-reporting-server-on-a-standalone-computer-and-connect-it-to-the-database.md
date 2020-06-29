---
title: Come installare il server di report in un computer autonomo e connetterlo al database
description: Come installare il server di report in un computer autonomo e connetterlo al database
author: dansimp
ms.assetid: d186bdb7-e522-4124-bc6d-7d5a41ba8266
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f20f1ce16c3f0168d1c797efd816d4125c0f1f53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805386"
---
# Come installare il server di report in un computer autonomo e connetterlo al database


Usare la procedura seguente per installare il server di report in un computer autonomo e connetterlo al database.

**Importante**  
Prima di eseguire la procedura seguente, è necessario leggere e comprendere [informazioni sui report di App-V 5,0](about-app-v-50-reporting.md).



**Per installare il server di report in un computer autonomo e connetterlo al database**

1.  Copiare i file di installazione del server App-V 5,0 nel computer in cui si vuole installarlo. Per avviare l'installazione del server App-V 5,0, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore. Fai clic su **Installa**.

2.  Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.

3.  In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).** Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**. Fai clic su **Avanti**.

4.  Nella pagina **Selezione funzionalità** selezionare la casella di controllo del **Server dei report** e fare clic su **Avanti**.

5.  Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.

6.  Nella pagina **Configura database di report esistente** selezionare **Usa un server SQL remoto**e digitare il nome del computer che ha eseguito Microsoft SQL Server, ad esempio **SqlServerMachine**.

    **Nota**  
    Se Microsoft SQL Server è distribuito nello stesso server, selezionare **Usa SQL Server locale**.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.
~~~

7. Nella pagina **configura configurazione del server di Reporting** .

   -   Specificare il nome del sito Web che si vuole usare per il servizio di creazione di report. Se non si ha un nome personalizzato, lasciarlo invariato.

   -   Per il **Binding della porta**, specifica un numero di porta univoco che verrà usato da App-V 5,0, ad esempio **55555**. Devi anche assicurarti che la porta specificata non venga usata da un altro sito Web.

8. Fai clic su **Installa**.

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Informazioni sulla creazione di report in App-V 5.0](about-app-v-50-reporting.md)

[Distribuzione di App-V 5.0](deploying-app-v-50.md)

[Come abilitare la creazione di report nel client App-V 5.0 con PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)









