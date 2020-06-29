---
title: Come installare un database
description: Come installare un database
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817376"
---
# <span data-ttu-id="85b6b-103">Come installare un database</span><span class="sxs-lookup"><span data-stu-id="85b6b-103">How to Install a Database</span></span>


<span data-ttu-id="85b6b-104">Per installare un database per la distribuzione basata su server della virtualizzazione delle applicazioni, è possibile usare la procedura seguente se non è già disponibile un database.</span><span class="sxs-lookup"><span data-stu-id="85b6b-104">You can use the following procedure to install a database for your server-based deployment of Application Virtualization if a database is not already available.</span></span> <span data-ttu-id="85b6b-105">In genere, in un ambiente di produzione, ci si connette a un database esistente.</span><span class="sxs-lookup"><span data-stu-id="85b6b-105">Typically, in a production environment, you will connect to an existing database.</span></span>

<span data-ttu-id="85b6b-106">**Importante**  Per installare il database, è necessario usare un account di rete con le autorizzazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="85b6b-106">**Important** To install the database, you must use a network account with the appropriate permissions.</span></span> <span data-ttu-id="85b6b-107">Se l'organizzazione richiede che solo gli amministratori di database siano autorizzati a creare e gestire gli aggiornamenti del database, gli script sono disponibili per consentire l'esecuzione di questa attività.</span><span class="sxs-lookup"><span data-stu-id="85b6b-107">If your organization requires that only database administrators are allowed to create and conduct database upgrades, scripts are available that allow this task to be performed.</span></span>

 

**<span data-ttu-id="85b6b-108">Per installare un database</span><span class="sxs-lookup"><span data-stu-id="85b6b-108">To install a database</span></span>**

1.  <span data-ttu-id="85b6b-109">Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic su **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-109">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

2.  <span data-ttu-id="85b6b-110">Nella **pagina di benvenuto**fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-110">On the **Welcome Page**, click **Next**.</span></span>

3.  <span data-ttu-id="85b6b-111">Nella pagina **contratto di licenza** , per accettare il contratto di licenza, selezionare **Accetto le condizioni di licenza**e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-111">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and click **Next**.</span></span>

4.  <span data-ttu-id="85b6b-112">Nella pagina **registrazione informazioni** specificare il **nome utente** e le informazioni sull' **organizzazione** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-112">On the **Registering Information** page, specify the **User Name** and **Organization** information, and then click **Next**.</span></span>

5.  <span data-ttu-id="85b6b-113">Nella pagina **tipo di installazione** selezionare **personalizzato** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-113">On the **Setup Type** page, select **Custom** and then click **Next**.</span></span>

6.  <span data-ttu-id="85b6b-114">Nella pagina **configurazione personalizzata** deselezionare tutti i componenti di sistema di virtualizzazione delle applicazioni eccetto **Application Virtualization Server**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-114">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    <span data-ttu-id="85b6b-115">**Nota**  Se un componente è già installato nel computer, deselezionarlo nella schermata di **configurazione personalizzata** verrà disinstallato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="85b6b-115">**Note** If a component is already installed on the computer, by deselecting it on the **Custom Setup** screen it will automatically be uninstalled.</span></span>

     

7.  <span data-ttu-id="85b6b-116">Nella pagina **server database** Digitare le password, assegnare un percorso di installazione, salvare le informazioni e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-116">On the **Database Server** page, type the passwords, assign an installation path, save the information, and click **Next**.</span></span>

8.  <span data-ttu-id="85b6b-117">Selezionare un nome per il database e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-117">Select a name for the database, and then click **Next**.</span></span>

    <span data-ttu-id="85b6b-118">**Nota**  Se viene visualizzato il messaggio di errore 25109 quando si prova a completare questo passaggio, le autorizzazioni necessarie per l'installazione del database non sono impostate in modo errato.</span><span class="sxs-lookup"><span data-stu-id="85b6b-118">**Note** If error 25109 is displayed when you try to complete this step, you have incorrectly set up the permissions necessary to install the database.</span></span> <span data-ttu-id="85b6b-119">Per informazioni dettagliate sulla configurazione delle autorizzazioni SQL necessarie, vedere <https://go.microsoft.com/fwlink/?LinkId=132144> .</span><span class="sxs-lookup"><span data-stu-id="85b6b-119">For details on setting up the necessary SQL permissions, please see <https://go.microsoft.com/fwlink/?LinkId=132144>.</span></span>

     

9.  <span data-ttu-id="85b6b-120">Nella schermata del **server di directory** immettere un nome di dominio e le credenziali che i server di virtualizzazione dell'applicazione e il servizio Web di gestione utilizzeranno per accedere al controller di dominio, salvare queste informazioni e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-120">On the **Directory Server** screen, enter a domain name and credentials that Application Virtualization Servers and the Management Web Service will use to access your domain controller, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="85b6b-121">**Nota**  L'installazione verrà predefinita per il dominio del computer corrente.</span><span class="sxs-lookup"><span data-stu-id="85b6b-121">**Note** The installation will default to the domain of the current computer.</span></span>

     

10. <span data-ttu-id="85b6b-122">Nella pagina **gruppo amministratore** immettere il nome di un gruppo che avrà privilegi di amministratore, salvare queste informazioni e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-122">On the **Administrator Group** page, enter the name of a group that will have Administrator privileges, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="85b6b-123">**Nota**  È anche possibile immettere i primi caratteri del nome di un gruppo che avrà privilegi di amministratore, fare clic su **Avanti**e nella schermata **selezione gruppo di amministratori** Selezionare il gruppo nell'elenco risultante.</span><span class="sxs-lookup"><span data-stu-id="85b6b-123">**Note** You can also enter the first few characters of the name of a group that will have Administration privileges, click **Next**, and on the **Select Administrator Group** screen, select the group from the resulting list.</span></span> <span data-ttu-id="85b6b-124">Quindi Salva queste informazioni e fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-124">Then save this information and click **Next**.</span></span>

     

11. <span data-ttu-id="85b6b-125">Nella pagina del **gruppo provider predefinito** immettere il nome completo di un gruppo che controllerà l'accesso alle applicazioni, salvare queste informazioni e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-125">On the **Default Provider Group** page, enter the complete name of a group that will control access to applications, save this information, and then click **Next**.</span></span>

    <span data-ttu-id="85b6b-126">**Nota**  È anche possibile immettere i primi caratteri del nome di un gruppo che controlla l'accesso alle applicazioni, fare clic su **Avanti**e quindi selezionare il gruppo nell'elenco nella schermata **selezione gruppo provider predefinito** .</span><span class="sxs-lookup"><span data-stu-id="85b6b-126">**Note** You can also enter the first few characters of the name of a group that will control access to applications, click **Next**, and on the **Select Default Provider Group** screen, select the group in the list.</span></span> <span data-ttu-id="85b6b-127">Quindi Salva queste informazioni e fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-127">Then save this information and click **Next**.</span></span>

     

12. <span data-ttu-id="85b6b-128">Nella pagina **installazione guidata completare** , per chiudere la procedura guidata, fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="85b6b-128">On the **Installation Wizard Completed** page, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="85b6b-129">**Importante**  L'installazione può richiedere alcuni minuti per terminare.</span><span class="sxs-lookup"><span data-stu-id="85b6b-129">**Important** The installation can take a few minutes to finish.</span></span> <span data-ttu-id="85b6b-130">Un messaggio di stato lampeggerà sopra l'area di notifica desktop di Windows, indicando se l'installazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="85b6b-130">A status message will flash above the Windows desktop notification area, indicating whether the installation succeeded.</span></span>

     

## <span data-ttu-id="85b6b-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85b6b-131">Related topics</span></span>


[<span data-ttu-id="85b6b-132">Come installare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="85b6b-132">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





