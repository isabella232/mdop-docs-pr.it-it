---
title: Come installare e configurare l'applicazione predefinita
description: Come installare e configurare l'applicazione predefinita
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817366"
---
# Come installare e configurare l'applicazione predefinita


L'applicazione predefinita viene fornita come parte dell'installazione e viene automaticamente copiata nel server di gestione di Microsoft Application Virtualization (App-V) durante l'installazione. Viene usato per verificare che il server di gestione sia stato installato e configurato correttamente, ma deve essere pubblicato nel client Microsoft Application Virtualization (App-V) in modo che l'utente possa accedervi.

Usa le procedure seguenti per pubblicare l'applicazione predefinita e per eseguirne il flusso.

**Per pubblicare l'applicazione predefinita**

1.  Accedere a App-V Management Server usando un account membro del gruppo amministratori App-V specificato durante l'installazione.

2.  Nel server di gestione di App-V fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e quindi fare clic su **Application Virtualization Management Console**.

3.  In App-V Management Console fare clic su **azioni**e quindi su **Connetti a Application Virtualization System**.

4.  Nella pagina **Configura connessione** deselezionare la casella di controllo **Usa connessione sicura** .

5.  Nella casella **nome host servizio Web** Digitare il nome di dominio completo (FQDN) di App-V Management Server e quindi fare clic su **OK**.

    **Nota**  È anche possibile usare **localhost** per il nome host del servizio Web se è installato nel server di gestione.

     

6.  Nella console di gestione di App-V fare clic con il pulsante destro del mouse sul nodo del **Server** e scegliere **Opzioni di sistema**.

7.  Nella scheda **generale** , nella casella **percorso di contenuto predefinito** , immettere il percorso UNC (Universal Naming Convention) della cartella di contenuto creata nel server durante l'installazione. ad esempio, \ \ \ \ \ &lt; nome server &gt; \\Content e quindi fare clic su **OK**.

    **Importante**  Usare l'FQDN per il nome del server in modo che il client possa risolvere correttamente il nome.

     

8.  Nel riquadro di spostamento di App-V Management Console espandere il nodo del **Server** e quindi fare clic su **applicazioni**.

9.  Nel riquadro argomento fare clic su **applicazione predefinita**e quindi, nel riquadro **azioni** , fare clic su **proprietà**.

10. Nella finestra di dialogo **Proprietà** fare clic su **Sfoglia**accanto alla casella **percorso OSD** .

11. Nella finestra di dialogo **Apri** immettere il percorso UNC della cartella di contenuto creata nel server durante l'installazione. ad esempio, \ \ \ \ \ &lt; nome server &gt; \\Content e premere INVIO. È necessario usare il nome del server effettivo e non è possibile usare il **localhost** qui.

    **Importante**  Assicurarsi che i valori nelle caselle **percorso OSD** e **percorso icona** siano in formato UNC, ad esempio \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ &lt; &gt; \\Content\\DefaultApp.ico, e scegliere la cartella di contenuto creata durante l'installazione. Non usare **localhost** o un percorso di file contenente una lettera di unità come c:\\Programmi Files\\.. \\.. Contenuto.

     

12. Selezionare il file file DefaultApp. OSD e fare clic su **Apri**.

13. Ripetere i passaggi precedenti per configurare il percorso dell'icona.

14. Fare clic sulla scheda **autorizzazioni di accesso** e verificare che il gruppo utenti App-V disponga delle autorizzazioni di accesso per l'applicazione.

15. Fare clic sulla scheda **collegamenti** e quindi su **pubblica sul desktop dell'utente**. Fai clic su **OK**.

16. Aprire Esplora risorse e individuare la directory di contenuto.

17. Fare doppio clic sul file file DefaultApp. OSD e aprirlo con il blocco note.

18. Individuare la riga che contiene il tag **href** e modificarla nel codice seguente:

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    In alternativa, se si usa RTSPs:

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. Chiudere il file file DefaultApp. OSD e salvare le modifiche.

**Per eseguire il flusso dell'applicazione predefinita**

1.  Nel computer in cui è installato App-V client eseguire l'accesso come utente membro del gruppo Application Virtualization Users specificato durante l'installazione del server.

2.  Sul desktop viene visualizzato il collegamento predefinito applicazione Application **Virtualization** . Fare doppio clic sul collegamento per avviare l'applicazione.

3.  Una barra di stato, visualizzata sopra l'area di notifica di Windows, segnala l'avvio dell'applicazione. Se l'avvio dell'applicazione è riuscito, viene visualizzata la schermata del titolo per l'applicazione predefinita. Fare clic su **OK** per chiudere la finestra di dialogo. Ora hai confermato che il sistema App-V viene eseguito correttamente.

## Argomenti correlati


[Come configurare i server per la distribuzione basata su server](how-to-configure-servers-for-server-based-deployment.md)

 

 





