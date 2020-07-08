---
title: Come installare il server di gestione in un computer autonomo e connetterlo al database
description: Come installare il server di gestione in un computer autonomo e connetterlo al database
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805409"
---
# Come installare il server di gestione in un computer autonomo e connetterlo al database


Usare la procedura seguente per installare il server di gestione in un computer autonomo e connetterlo al database.

**Per installare il server di gestione in un computer autonomo e connetterlo al database**

1.  Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo. Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore. Fai clic su **Installa**.

2.  Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.

3.  In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).** Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**. Fai clic su **Avanti**.

4.  Nella pagina **Selezione funzionalità** selezionare la casella di **controllo server di gestione** e fare clic su **Avanti**.

5.  Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.

6.  Nella pagina **Configura database di gestione esistente** selezionare **Usa un server SQL remoto**e digitare il nome del computer che ha eseguito Microsoft SQL SQL, ad esempio **SqlServerMachine**.

    **Nota**  
    Se Microsoft SQL Server è distribuito nello stesso server, selezionare **Usa SQL Server locale**.



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. Nella pagina **configura configurazione server di gestione** specificare il gruppo di annunci o l'account che si connetterà alla console di gestione per scopi amministrativi, ad esempio **MyDomain\\MyUser** o **MyDomain\\AdminGroup**. L'account o il gruppo di annunci specificato verrà abilitato per la gestione del server tramite la console di gestione. Dopo l'installazione, è possibile aggiungere altri utenti o gruppi tramite la console di gestione

   Specificare il **nome del sito Web** che si vuole usare per il servizio di gestione. Accettare l'impostazione predefinita se non si dispone di un nome personalizzato. Per il **Binding della porta**, specificare un numero di porta univoco da usare, ad esempio **12345**.

8. Fai clic su **Installa**.

9. Per verificare che il programma di installazione sia stato completato correttamente, aprire un Web browser e digitare l'URL seguente: http://managementserver:portnumber/Console . Se l'installazione è stata eseguita correttamente, la **console di gestione** verrà visualizzata senza messaggi di errore o avvisi visualizzati.

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Distribuzione di App-V 5.1](deploying-app-v-51.md)









