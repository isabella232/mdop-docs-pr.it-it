---
title: Come configurare i server di pubblicazione
description: Come configurare i server di pubblicazione
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816526"
---
# <span data-ttu-id="a7548-103">Come configurare i server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="a7548-103">How to Set Up Publishing Servers</span></span>


<span data-ttu-id="a7548-104">È possibile usare le procedure seguenti per aggiungere e configurare i server di virtualizzazione delle applicazioni direttamente dalla console di gestione client.</span><span class="sxs-lookup"><span data-stu-id="a7548-104">You can use the following procedures to add and configure Application Virtualization Servers directly from the Client Management Console.</span></span>

**<span data-ttu-id="a7548-105">Per aggiungere un server di pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="a7548-105">To add an application publishing server</span></span>**

1.  <span data-ttu-id="a7548-106">Nel riquadro **dei risultati** fare clic con il pulsante destro del mouse e scegliere **nuovo server** dal menu a comparsa per avviare la procedura guidata nuovo Application Virtualization Server o in alternativa, fare clic con il pulsante destro del mouse sul nodo del **server di pubblicazione** e scegliere **nuovo server** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="a7548-106">In the **Results** pane, right-click and select **New Server** from the pop-up-menu to start the New Application Virtualization Server Wizard, or alternatively, right-click the **Publishing Server** node and select **New Server** from the pop-up-menu.</span></span>

2.  <span data-ttu-id="a7548-107">Nella pagina uno della procedura guidata immettere il nome del server nel campo **nome visualizzato** e selezionare il tipo di server nell'elenco a discesa **tipo** .</span><span class="sxs-lookup"><span data-stu-id="a7548-107">On page one of the wizard, enter the name of the server in the **Display Name** field and select the server type from the **Type** drop-down list.</span></span> <span data-ttu-id="a7548-108">È possibile scegliere **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **standard HTTP server**o **Enhanced Security http server** dall'elenco a discesa dei tipi di server.</span><span class="sxs-lookup"><span data-stu-id="a7548-108">You can choose **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**, or **Enhanced Security HTTP Server** from the drop-down list of server types.</span></span>

3.  <span data-ttu-id="a7548-109">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="a7548-109">Click **Next**.</span></span>

4.  <span data-ttu-id="a7548-110">Nella pagina due della procedura guidata digitare le informazioni appropriate nei campi **nome host** e **porta** .</span><span class="sxs-lookup"><span data-stu-id="a7548-110">On page two of the wizard, type the appropriate information into the **Host Name** and **Port** fields.</span></span> <span data-ttu-id="a7548-111">Il campo **path** non è modificabile per i server di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7548-111">The **Path** field is not editable for Application Virtualization Servers.</span></span> <span data-ttu-id="a7548-112">È necessario immettere un percorso per un server HTTP standard o un server HTTP di sicurezza avanzato.</span><span class="sxs-lookup"><span data-stu-id="a7548-112">You must enter a path for Standard HTTP Server or Enhanced Security HTTP Server.</span></span>

5.  <span data-ttu-id="a7548-113">Fare clic su **fine** per aggiungere il server.</span><span class="sxs-lookup"><span data-stu-id="a7548-113">Click **Finish** to add the server.</span></span>

**<span data-ttu-id="a7548-114">Per configurare un server di pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="a7548-114">To set up an application publishing server</span></span>**

1.  <span data-ttu-id="a7548-115">Nel riquadro **risultati** fare clic con il pulsante destro del mouse sul server desiderato e scegliere **Proprietà** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="a7548-115">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="a7548-116">Fare clic sulla scheda **generale** , in cui è possibile modificare il nome del server, selezionare un tipo nell'elenco a discesa dei tipi di server e specificare il nome host e la porta.</span><span class="sxs-lookup"><span data-stu-id="a7548-116">Click the **General** tab, where you can change the server name, select a type from the drop-down list of server types, and specify the host name and port.</span></span> <span data-ttu-id="a7548-117">Quando il tipo di server è un server HTTP standard o un server HTTP di sicurezza avanzato, anche il campo **path** è modificabile.</span><span class="sxs-lookup"><span data-stu-id="a7548-117">When the server type is Standard HTTP Server or Enhanced Security HTTP Server, the **Path** field is also editable.</span></span>

3.  <span data-ttu-id="a7548-118">Fare clic sulla scheda **Aggiorna** , in cui la casella di controllo **Aggiorna pubblicazione per l'accesso dell'utente** è selezionata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a7548-118">Click the **Refresh** tab, where the **Refresh publishing on user login** check box is selected by default.</span></span> <span data-ttu-id="a7548-119">Per modificare la frequenza di aggiornamento, selezionare la casella di controllo **Aggiorna pubblicazione ogni** e immettere un numero che rappresenti la frequenza nel campo.</span><span class="sxs-lookup"><span data-stu-id="a7548-119">To change the refresh rate, select the **Refresh publishing every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="a7548-120">Quindi selezionare **minuti**, **ore**e **giorni** dal menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="a7548-120">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span> <span data-ttu-id="a7548-121">(Il periodo di tempo minimo che puoi immettere è 30 minuti).</span><span class="sxs-lookup"><span data-stu-id="a7548-121">(The minimum amount of time you can enter is 30 minutes.)</span></span>

4.  <span data-ttu-id="a7548-122">Fare clic su **applica** per modificare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="a7548-122">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="a7548-123">Dopo aver completato la pubblicazione, fare clic su **OK** per uscire dalla finestra di dialogo e tornare alla console di gestione client.</span><span class="sxs-lookup"><span data-stu-id="a7548-123">When you are finished publishing, click **OK** to exit the dialog box and return to the Client Management Console.</span></span>

## <span data-ttu-id="a7548-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7548-124">Related topics</span></span>


[<span data-ttu-id="a7548-125">Come disabilitare o modificare le impostazioni della modalità di operazioni senza connessione</span><span class="sxs-lookup"><span data-stu-id="a7548-125">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





