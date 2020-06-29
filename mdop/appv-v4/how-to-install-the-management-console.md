---
title: Come installare la console di gestione
description: Come installare la console di gestione
author: dansimp
ms.assetid: 586d99c8-bca6-42e2-a39c-a696053142f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 48f4f69753794cf8099df36828e0502e98414b31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817305"
---
# <span data-ttu-id="60e16-103">Come installare la console di gestione</span><span class="sxs-lookup"><span data-stu-id="60e16-103">How to Install the Management Console</span></span>


<span data-ttu-id="60e16-104">Per installare la console di gestione della virtualizzazione dell'applicazione in un computer di destinazione della rete, è possibile usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="60e16-104">You can use the following procedure to install the Application Virtualization Management Console on a target computer on the network.</span></span> <span data-ttu-id="60e16-105">È necessario usare un account di rete con privilegi di amministratore nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="60e16-105">You must use a network account that has administrator privileges on the target computer.</span></span> <span data-ttu-id="60e16-106">Puoi usare la console per configurare e gestire la piattaforma di sistema di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60e16-106">You can use the console to configure and manage the Application Virtualization System Platform.</span></span>

<span data-ttu-id="60e16-107">Prima di poter eseguire questa procedura, è necessario installare il servizio Web Application Virtualization Management in questo o in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="60e16-107">Before you can complete this procedure, you must install the Application Virtualization Management Web Service on this or a different computer.</span></span> <span data-ttu-id="60e16-108">Il servizio Web di gestione consente di accedere all'archivio dati e al controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="60e16-108">The Management Web Service allows you to access the data store and the domain controller.</span></span> <span data-ttu-id="60e16-109">Per altre informazioni sull'installazione del servizio Web, vedere [come installare il servizio Web di gestione](how-to-install-the-management-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="60e16-109">For more information about installing the Web service, see [How to Install the Management Web Service](how-to-install-the-management-web-service.md).</span></span>

**<span data-ttu-id="60e16-110">Per installare la console di gestione</span><span class="sxs-lookup"><span data-stu-id="60e16-110">To install the Management Console</span></span>**

1.  <span data-ttu-id="60e16-111">Verificare che nel computer di destinazione non siano installate versioni precedenti della console di gestione.</span><span class="sxs-lookup"><span data-stu-id="60e16-111">Verify that no previous versions of the Management Console are installed on the target computer.</span></span>

2.  <span data-ttu-id="60e16-112">Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic su **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="60e16-112">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="60e16-113">Nella **pagina di benvenuto**fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="60e16-113">On the **Welcome Page**, click **Next**.</span></span>

4.  <span data-ttu-id="60e16-114">Nella pagina **contratto di licenza** , per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="60e16-114">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="60e16-115">Nella pagina **informazioni di registrazione** specificare il **nome utente** e le informazioni sull' **organizzazione** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="60e16-115">On the **Registration Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

6.  <span data-ttu-id="60e16-116">Nella pagina **tipo di installazione** fare clic su **personalizzato** e quindi su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="60e16-116">On the **Setup Type** page, click **Custom** and then click **Next**.</span></span>

7.  <span data-ttu-id="60e16-117">Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema di virtualizzazione delle applicazioni eccetto **console di gestione**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="60e16-117">On the **Custom Setup** page, deselect all Application Virtualization System components except **Management Console**, and then click **Next**.</span></span>

    <span data-ttu-id="60e16-118">**Nota**  Se un componente è già installato nel computer, deselezionarlo nella schermata di configurazione personalizzata verrà disinstallato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="60e16-118">**Note** If a component is already installed on the computer, by deselecting it on the Custom Setup screen, it will automatically be uninstalled.</span></span>

     

8.  <span data-ttu-id="60e16-119">Nella schermata **pronto per la modifica dello** schermo fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="60e16-119">On the **Ready to Modify the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="60e16-120">**Nota**  Se si tratta del primo componente installato, verrà visualizzata la pagina **pronto per l'installazione** .</span><span class="sxs-lookup"><span data-stu-id="60e16-120">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="60e16-121">Per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="60e16-121">To start the installation, click **Install**.</span></span>

     

9.  <span data-ttu-id="60e16-122">Nella schermata **installazione guidata completata** fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="60e16-122">On the **Installation Wizard Completed** screen, click **Finish**.</span></span> <span data-ttu-id="60e16-123">Fare clic su **OK** per riavviare il computer e completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="60e16-123">Click **Okay** to restart the computer and complete the installation.</span></span>

10. <span data-ttu-id="60e16-124">Nel pannello di controllo di Windows fare doppio clic su **strumenti di amministrazione** e quindi su **Application Virtualization Management Console** per visualizzare la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="60e16-124">In the Windows Control Panel, double-click **Administrative Tools** and then click **Application Virtualization Management Console** to display the Management Console.</span></span>

11. <span data-ttu-id="60e16-125">Fai clic sull'icona **Connetti** oppure fai clic con il pulsante destro del mouse sul contenitore **Application Virtualization Systems** e quindi fai clic su **Connetti a Application Virtualization System**.</span><span class="sxs-lookup"><span data-stu-id="60e16-125">Click the **Connect** icon, or right-click the **Application Virtualization Systems** container, and then click **Connect to Application Virtualization System**.</span></span>

12. <span data-ttu-id="60e16-126">Nella schermata **Connetti a Application Virtualization System** immettere il nome host e la porta del computer del servizio Web di gestione, modificare le informazioni di sicurezza e le credenziali di accesso, se necessario, e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="60e16-126">On the **Connect to Application Virtualization System** screen, enter the host name and port of the Management Web Service computer, change the security information and login credentials if necessary, and then click **OK**.</span></span>

13. <span data-ttu-id="60e16-127">Dopo aver effettuato la connessione al computer del servizio Web di gestione, fare clic su **file** dal menu **console** e quindi su **Esci**.</span><span class="sxs-lookup"><span data-stu-id="60e16-127">After connecting to the Management Web Service computer, click **File** on the **Console** menu, and then click **Exit**.</span></span> <span data-ttu-id="60e16-128">Fare clic su **Sì** per salvare le impostazioni della console.</span><span class="sxs-lookup"><span data-stu-id="60e16-128">Click **Yes** to save console settings.</span></span>

## <span data-ttu-id="60e16-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60e16-129">Related topics</span></span>


[<span data-ttu-id="60e16-130">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="60e16-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





