---
title: Come installare il servizio Gestione Web
description: Come installare il servizio Gestione Web
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817276"
---
# <span data-ttu-id="558d3-103">Come installare il servizio Gestione Web</span><span class="sxs-lookup"><span data-stu-id="558d3-103">How to Install the Management Web Service</span></span>


<span data-ttu-id="558d3-104">Usare la procedura seguente per installare il servizio Web Application Virtualization Management in un computer di destinazione in rete, con un account di accesso con privilegi amministrativi locali.</span><span class="sxs-lookup"><span data-stu-id="558d3-104">Use the following procedure to install the Application Virtualization Management Web Service on a target computer on the network, with a logon account having local administrative privileges.</span></span> <span data-ttu-id="558d3-105">Anche se non è necessario, è consigliabile installare questo componente nel server Web.</span><span class="sxs-lookup"><span data-stu-id="558d3-105">Although it is not required, we recommended that you install this component on your Web server.</span></span>

**<span data-ttu-id="558d3-106">Per installare il servizio Web di gestione</span><span class="sxs-lookup"><span data-stu-id="558d3-106">To install the Management Web Service</span></span>**

1.  <span data-ttu-id="558d3-107">Verificare che nel computer di destinazione non siano installate versioni precedenti del servizio Web Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="558d3-107">Verify that no previous versions of the Application Virtualization Web Service are installed on your target computer.</span></span>

2.  <span data-ttu-id="558d3-108">Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic su **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="558d3-108">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="558d3-109">Dopo l'apertura della procedura guidata, nella pagina **iniziale** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-109">After the Installation Wizard opens, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="558d3-110">Nella pagina **contratto di licenza** , per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-110">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="558d3-111">Nella pagina **informazioni di registrazione** specificare il **nome utente** e le informazioni sull'organizzazione e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-111">On the **Registration Information** page, specify the **User Name** and organization information, and then click **Next**.</span></span>

6.  <span data-ttu-id="558d3-112">Nella pagina **tipo di installazione** fare clic su **personalizzato**e quindi su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-112">On the **Setup Type** page, click **Custom**, and then click **Next**.</span></span>

    <span data-ttu-id="558d3-113">**Nota**  Se non si tratta del primo componente installato nel computer, verrà visualizzata la pagina **manutenzione programmi** .</span><span class="sxs-lookup"><span data-stu-id="558d3-113">**Note** If this is not the first component you installed on this computer, the **Program Maintenance** page is displayed.</span></span> <span data-ttu-id="558d3-114">Nella pagina **Manutenzione programma** fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="558d3-114">On the **Program Maintenance** page, click **Modify**.</span></span>

     

7.  <span data-ttu-id="558d3-115">Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema per la virtualizzazione delle applicazioni tranne il **servizio di gestione virt app**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-115">On the **Custom Setup** page, clear all Application Virtualization System components except **App Virt Management Service**, and then click **Next**.</span></span>

    <span data-ttu-id="558d3-116">**Nota**  Se un componente è già installato nel computer, deselezionarlo nella pagina **configurazione personalizzata** , lo si disinstalla automaticamente.</span><span class="sxs-lookup"><span data-stu-id="558d3-116">**Note** If a component is already installed on the computer, by clearing it on the **Custom Setup** page, you will automatically uninstall it.</span></span>

     

8.  <span data-ttu-id="558d3-117">Nella pagina **server database** fare clic su **Connetti a database disponibile**e quindi su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-117">On the **Database Server** page, click **Connect to available database**, and then click **Next**.</span></span>

    <span data-ttu-id="558d3-118">**Nota**  In un ambiente di produzione, Microsoft presuppone che si collegherà a un database esistente.</span><span class="sxs-lookup"><span data-stu-id="558d3-118">**Note** In a production environment, Microsoft assumes that you will connect to an existing database.</span></span> <span data-ttu-id="558d3-119">Se si vuole installare un database, vedere [come installare un database](how-to-install-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="558d3-119">If you want to install a database, see [How to Install a Database](how-to-install-a-database.md).</span></span> <span data-ttu-id="558d3-120">Dopo aver installato il database, procedere con il passaggio 13.</span><span class="sxs-lookup"><span data-stu-id="558d3-120">After installing the database, continue with step 13.</span></span>

     

9.  <span data-ttu-id="558d3-121">Nella pagina **tipo di server database** selezionare un tipo di database nell'elenco e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-121">On the **Database Server Type** page, select a database type from the list, and then click **Next**.</span></span>

10. <span data-ttu-id="558d3-122">Nella pagina **percorso del server di database** selezionare un server di database nell'elenco dei server disponibili o aggiungere un server selezionando la casella di controllo **Usa il nome host seguente** e immettendo le informazioni nelle caselle **nome server** e **numero di porta** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-122">On the **Database Server Location** page, select a database server from the list of available servers or add a server by selecting the **Use the following host name** check box and entering information in the **Server Name** and **Port Number** boxes, and then click **Next**.</span></span>

11. <span data-ttu-id="558d3-123">Nella pagina **Seleziona database** selezionare il database desiderato e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-123">On the **Select Database** page, select the database you want, and then click **Next**.</span></span>

12. <span data-ttu-id="558d3-124">Nella pagina **Configurazione utente database** immettere le credenziali che verranno usate dal servizio Web di gestione per accedere all'archivio dati e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="558d3-124">On the **Database User Configuration** page, enter the credentials that the Management Web Service will use to access the data store, and then click **Next**.</span></span>

13. <span data-ttu-id="558d3-125">Nella pagina **pronto per la modifica del programma** fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="558d3-125">On the **Ready to Modify the Program** page, click **Install**.</span></span>

    <span data-ttu-id="558d3-126">**Nota**  Se si tratta del primo componente installato, verrà visualizzata la pagina **pronto per l'installazione** .</span><span class="sxs-lookup"><span data-stu-id="558d3-126">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="558d3-127">Nella pagina fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="558d3-127">On the page, click **Install**.</span></span>

     

14. <span data-ttu-id="558d3-128">Nella pagina **installazione guidata completare** fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="558d3-128">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

## <span data-ttu-id="558d3-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="558d3-129">Related topics</span></span>


[<span data-ttu-id="558d3-130">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="558d3-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





