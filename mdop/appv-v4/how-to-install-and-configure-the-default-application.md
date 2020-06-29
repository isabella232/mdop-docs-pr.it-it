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
# <span data-ttu-id="c9919-103">Come installare e configurare l'applicazione predefinita</span><span class="sxs-lookup"><span data-stu-id="c9919-103">How to Install and Configure the Default Application</span></span>


<span data-ttu-id="c9919-104">L'applicazione predefinita viene fornita come parte dell'installazione e viene automaticamente copiata nel server di gestione di Microsoft Application Virtualization (App-V) durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c9919-104">The default application is provided as part of the installation and is automatically copied to the Microsoft Application Virtualization (App-V) Management Server during installation.</span></span> <span data-ttu-id="c9919-105">Viene usato per verificare che il server di gestione sia stato installato e configurato correttamente, ma deve essere pubblicato nel client Microsoft Application Virtualization (App-V) in modo che l'utente possa accedervi.</span><span class="sxs-lookup"><span data-stu-id="c9919-105">It is used to verify that the Management Server was installed and configured correctly, but it has to be published to the Microsoft Application Virtualization (App-V) Client so that the user can access it.</span></span>

<span data-ttu-id="c9919-106">Usa le procedure seguenti per pubblicare l'applicazione predefinita e per eseguirne il flusso.</span><span class="sxs-lookup"><span data-stu-id="c9919-106">Use the following procedures to publish the default application and to stream it.</span></span>

**<span data-ttu-id="c9919-107">Per pubblicare l'applicazione predefinita</span><span class="sxs-lookup"><span data-stu-id="c9919-107">To publish the default application</span></span>**

1.  <span data-ttu-id="c9919-108">Accedere a App-V Management Server usando un account membro del gruppo amministratori App-V specificato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c9919-108">Log on to the App-V Management Server by using an account that is a member of the App-V Administrators group specified during installation.</span></span>

2.  <span data-ttu-id="c9919-109">Nel server di gestione di App-V fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e quindi fare clic su **Application Virtualization Management Console**.</span><span class="sxs-lookup"><span data-stu-id="c9919-109">On the App-V Management Server, click **Start**, click **Administrative Tools**, and then click **Application Virtualization Management Console**.</span></span>

3.  <span data-ttu-id="c9919-110">In App-V Management Console fare clic su **azioni**e quindi su **Connetti a Application Virtualization System**.</span><span class="sxs-lookup"><span data-stu-id="c9919-110">In the App-V Management Console, click **Actions**, and then click **Connect to Application Virtualization System**.</span></span>

4.  <span data-ttu-id="c9919-111">Nella pagina **Configura connessione** deselezionare la casella di controllo **Usa connessione sicura** .</span><span class="sxs-lookup"><span data-stu-id="c9919-111">On the **Configure Connection** page, clear the **Use Secure Connection** check box.</span></span>

5.  <span data-ttu-id="c9919-112">Nella casella **nome host servizio Web** Digitare il nome di dominio completo (FQDN) di App-V Management Server e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9919-112">In the **Web Service Host Name** box, type the fully qualified domain name (FQDN) of the App-V Management Server, and then click **OK**.</span></span>

    <span data-ttu-id="c9919-113">**Nota**  È anche possibile usare **localhost** per il nome host del servizio Web se è installato nel server di gestione.</span><span class="sxs-lookup"><span data-stu-id="c9919-113">**Note** You can also use **localhost** for the Web Service Host name if it is installed on the Management Server.</span></span>

     

6.  <span data-ttu-id="c9919-114">Nella console di gestione di App-V fare clic con il pulsante destro del mouse sul nodo del **Server** e scegliere **Opzioni di sistema**.</span><span class="sxs-lookup"><span data-stu-id="c9919-114">In the App-V Management Console, right-click the **Server** node, and click **System Options**.</span></span>

7.  <span data-ttu-id="c9919-115">Nella scheda **generale** , nella casella **percorso di contenuto predefinito** , immettere il percorso UNC (Universal Naming Convention) della cartella di contenuto creata nel server durante l'installazione. ad esempio, \ \ \ \ \ &lt; nome server &gt; \\Content e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9919-115">On the **General** tab, in the **Default Content Path** box, enter the Universal Naming Convention (UNC) path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and then click **OK**.</span></span>

    <span data-ttu-id="c9919-116">**Importante**  Usare l'FQDN per il nome del server in modo che il client possa risolvere correttamente il nome.</span><span class="sxs-lookup"><span data-stu-id="c9919-116">**Important** Use the FQDN for the server name so that the client can resolve the name correctly.</span></span>

     

8.  <span data-ttu-id="c9919-117">Nel riquadro di spostamento di App-V Management Console espandere il nodo del **Server** e quindi fare clic su **applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="c9919-117">In the App-V Management Console, in the navigation pane, expand the **Server** node, and then click **Applications**.</span></span>

9.  <span data-ttu-id="c9919-118">Nel riquadro argomento fare clic su **applicazione predefinita**e quindi, nel riquadro **azioni** , fare clic su **proprietà**.</span><span class="sxs-lookup"><span data-stu-id="c9919-118">In the topic pane, click **Default Application**, and then, in the **Actions** pane, click **Properties**.</span></span>

10. <span data-ttu-id="c9919-119">Nella finestra di dialogo **Proprietà** fare clic su **Sfoglia**accanto alla casella **percorso OSD** .</span><span class="sxs-lookup"><span data-stu-id="c9919-119">In the **Properties** dialog box, next to the **OSD Path** box, click **Browse**.</span></span>

11. <span data-ttu-id="c9919-120">Nella finestra di dialogo **Apri** immettere il percorso UNC della cartella di contenuto creata nel server durante l'installazione. ad esempio, \ \ \ \ \ &lt; nome server &gt; \\Content e premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="c9919-120">In the **Open** dialog box, enter the UNC path to the Content folder you created on the server during installation; for example, \\\\&lt;Server Name&gt;\\Content, and press ENTER.</span></span> <span data-ttu-id="c9919-121">È necessario usare il nome del server effettivo e non è possibile usare il **localhost** qui.</span><span class="sxs-lookup"><span data-stu-id="c9919-121">You must use the actual server name and cannot use the **localhost** here.</span></span>

    <span data-ttu-id="c9919-122">**Importante**  Assicurarsi che i valori nelle caselle **percorso OSD** e **percorso icona** siano in formato UNC, ad esempio \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ &lt; &gt; \\Content\\DefaultApp.ico, e scegliere la cartella di contenuto creata durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c9919-122">**Important** Ensure that the values in both the **OSD Path** and **Icon Path** boxes are in UNC format (for example, \\\\&lt;Server Name&gt;\\Content\\DefaultApp.ico), and point to the Content folder you created when installing the server.</span></span> <span data-ttu-id="c9919-123">Non usare **localhost** o un percorso di file contenente una lettera di unità come c:\\Programmi Files\\.. \\.. Contenuto.</span><span class="sxs-lookup"><span data-stu-id="c9919-123">Do not use **localhost** or a file path containing a drive letter such as C:\\Program Files\\..\\..\\Content.</span></span>

     

12. <span data-ttu-id="c9919-124">Selezionare il file file DefaultApp. OSD e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="c9919-124">Select the DefaultApp.osd file, and click **Open**.</span></span>

13. <span data-ttu-id="c9919-125">Ripetere i passaggi precedenti per configurare il percorso dell'icona.</span><span class="sxs-lookup"><span data-stu-id="c9919-125">Repeat the previous steps to configure the icon path.</span></span>

14. <span data-ttu-id="c9919-126">Fare clic sulla scheda **autorizzazioni di accesso** e verificare che il gruppo utenti App-V disponga delle autorizzazioni di accesso per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9919-126">Click the **Access Permissions** tab, and confirm that the App-V Users group has access permissions to the application.</span></span>

15. <span data-ttu-id="c9919-127">Fare clic sulla scheda **collegamenti** e quindi su **pubblica sul desktop dell'utente**.</span><span class="sxs-lookup"><span data-stu-id="c9919-127">Click the **Shortcuts** tab, and then click **Publish to User’s Desktop**.</span></span> <span data-ttu-id="c9919-128">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9919-128">Click **OK**.</span></span>

16. <span data-ttu-id="c9919-129">Aprire Esplora risorse e individuare la directory di contenuto.</span><span class="sxs-lookup"><span data-stu-id="c9919-129">Open Windows Explorer, and locate the Content directory.</span></span>

17. <span data-ttu-id="c9919-130">Fare doppio clic sul file file DefaultApp. OSD e aprirlo con il blocco note.</span><span class="sxs-lookup"><span data-stu-id="c9919-130">Double-click the DefaultApp.osd file, and open it with Notepad.</span></span>

18. <span data-ttu-id="c9919-131">Individuare la riga che contiene il tag **href** e modificarla nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="c9919-131">Locate the line that contains the **HREF** tag, and change it to the following code:</span></span>

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    <span data-ttu-id="c9919-132">In alternativa, se si usa RTSPs:</span><span class="sxs-lookup"><span data-stu-id="c9919-132">Or, if you are using RTSPS:</span></span>

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. <span data-ttu-id="c9919-133">Chiudere il file file DefaultApp. OSD e salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="c9919-133">Close the DefaultApp.osd file, and save the changes.</span></span>

**<span data-ttu-id="c9919-134">Per eseguire il flusso dell'applicazione predefinita</span><span class="sxs-lookup"><span data-stu-id="c9919-134">To stream the default application</span></span>**

1.  <span data-ttu-id="c9919-135">Nel computer in cui è installato App-V client eseguire l'accesso come utente membro del gruppo Application Virtualization Users specificato durante l'installazione del server.</span><span class="sxs-lookup"><span data-stu-id="c9919-135">On the computer that has the App-V Client installed, log on as a user who is a member of the Application Virtualization Users group specified during server installation.</span></span>

2.  <span data-ttu-id="c9919-136">Sul desktop viene visualizzato il collegamento predefinito applicazione Application **Virtualization** .</span><span class="sxs-lookup"><span data-stu-id="c9919-136">On the desktop, the **Default Application Virtualization Application** shortcut appears.</span></span> <span data-ttu-id="c9919-137">Fare doppio clic sul collegamento per avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9919-137">Double-click the shortcut to start the application.</span></span>

3.  <span data-ttu-id="c9919-138">Una barra di stato, visualizzata sopra l'area di notifica di Windows, segnala l'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9919-138">A status bar, displayed above the Windows notification area, reports that the application is starting.</span></span> <span data-ttu-id="c9919-139">Se l'avvio dell'applicazione è riuscito, viene visualizzata la schermata del titolo per l'applicazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c9919-139">If the application startup is successful, the title screen for the default application is displayed.</span></span> <span data-ttu-id="c9919-140">Fare clic su **OK** per chiudere la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c9919-140">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="c9919-141">Ora hai confermato che il sistema App-V viene eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c9919-141">You have now confirmed that the App-V system is running correctly.</span></span>

## <span data-ttu-id="c9919-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9919-142">Related topics</span></span>


[<span data-ttu-id="c9919-143">Come configurare i server per la distribuzione basata su server</span><span class="sxs-lookup"><span data-stu-id="c9919-143">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

 

 





