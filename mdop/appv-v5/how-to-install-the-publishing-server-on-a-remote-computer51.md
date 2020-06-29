---
title: Come installare il server di pubblicazione in un computer remoto
description: Come installare il server di pubblicazione in un computer remoto
author: dansimp
ms.assetid: 1c903f78-0558-458d-a149-d5f6fb55aefb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a085d68305057538228599e35dd9500957342ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805385"
---
# Come installare il server di pubblicazione in un computer remoto


Usare la procedura seguente per installare il server di pubblicazione in un computer separato. Prima di eseguire la procedura seguente, verificare che il database e il server di gestione siano disponibili.

**Per installare il server di pubblicazione in un computer separato**

1. Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo. Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore. Fai clic su **Installa**.

2. Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.

3. In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).** Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**. Fai clic su **Avanti**.

4. Nella pagina **Selezione funzionalità** selezionare la casella di controllo **server di pubblicazione** e fare clic su **Avanti**.

5. Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.

6. Nella pagina **configura configurazione server di pubblicazione** specificare gli elementi seguenti:

   -   URL per il servizio di gestione a cui il server di pubblicazione si connette. Ad esempio, **http://ManagementServerName:12345** .

   -   Specificare il nome del sito Web che si vuole usare per il servizio di pubblicazione. Accettare l'impostazione predefinita se non si dispone di un nome personalizzato.

   -   Per il **Binding della porta**, specifica un numero di porta univoco che verrà usato da App-V 5,1, ad esempio **54321**.

7. Nella pagina **pronto per l'installazione** fare clic su **Installa**.

8. Al termine dell'installazione, il server di pubblicazione deve essere registrato con il server di gestione. Nella console di gestione di App-V 5,1, eseguire la procedura seguente per registrare il server:

   1.  Aprire la console del server di gestione di App-V 5,1.

   2.  Nel riquadro sinistro selezionare **Server**e quindi **Registra nuovo server**.

   3.  Digitare il nome del server e una descrizione (se necessario) e fare clic su **Aggiungi**.

9. Per verificare se il server di pubblicazione è in uso correttamente, è consigliabile importare un pacchetto nel server di gestione, autorizzare il pacchetto a un gruppo di annunci e pubblicare il pacchetto. Con un browser Internet aprire l'URL seguente: <strong> http://publishingserver:pubport </strong> . Se il server sta eseguendo correttamente le informazioni simili a quelle seguenti verranno visualizzate:

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Distribuzione di App-V 5.1](deploying-app-v-51.md)

 

 





