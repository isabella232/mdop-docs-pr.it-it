---
title: Come aggiungere manualmente un'applicazione
description: Come aggiungere manualmente un'applicazione
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817096"
---
# <span data-ttu-id="de50d-103">Come aggiungere manualmente un'applicazione</span><span class="sxs-lookup"><span data-stu-id="de50d-103">How to Manually Add an Application</span></span>


<span data-ttu-id="de50d-104">Quando si aggiunge un'applicazione all'Application Virtualization Management Server, è consigliabile importarla.</span><span class="sxs-lookup"><span data-stu-id="de50d-104">When adding an application to the Application Virtualization Management Server, it is recommended that you import it.</span></span> <span data-ttu-id="de50d-105">È possibile aggiungere manualmente un'applicazione, ma è necessario specificare le informazioni precise e dettagliate sull'applicazione richiesta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="de50d-105">You can add an application manually, but you must provide the precise, detailed information about the application called for in this section.</span></span>

**<span data-ttu-id="de50d-106">Per aggiungere manualmente una nuova applicazione</span><span class="sxs-lookup"><span data-stu-id="de50d-106">To manually add a new application</span></span>**

1.  <span data-ttu-id="de50d-107">Nel riquadro sinistro fare clic con il pulsante destro del mouse sul nodo **applicazioni** e scegliere **nuova applicazione**.</span><span class="sxs-lookup"><span data-stu-id="de50d-107">In the left pane, right-click the **Applications** node and choose **New Application**.</span></span>

2.  <span data-ttu-id="de50d-108">Nella **procedura guidata nuova applicazione**completare la finestra di dialogo **informazioni generali** :</span><span class="sxs-lookup"><span data-stu-id="de50d-108">In the **New Application Wizard**, complete the **General Information** dialog box:</span></span>

    1.  <span data-ttu-id="de50d-109">**Nome applicazione**: digitare il nome che si desidera venga visualizzato dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="de50d-109">**Application Name**—Type the name you want the users to see.</span></span>

    2.  <span data-ttu-id="de50d-110">**Versione**: digitare la versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de50d-110">**Version**—Type the application version.</span></span>

    3.  <span data-ttu-id="de50d-111">**Enabled**: questa casella deve essere selezionata per eseguire il flusso dell'applicazione dopo averla creata.</span><span class="sxs-lookup"><span data-stu-id="de50d-111">**Enabled**—This box must be selected to stream the application after you create it.</span></span>

    4.  <span data-ttu-id="de50d-112">**Descrizione**: digitare una descrizione facoltativa per l'uso amministrativo.</span><span class="sxs-lookup"><span data-stu-id="de50d-112">**Description**—Type an optional description for administrative use.</span></span>

    5.  <span data-ttu-id="de50d-113">**Percorso OSD**: esplorare la rete in un file OSD (Open Software Descriptor) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de50d-113">**OSD Path**—Browse the network to the application's Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="de50d-114">Questo file deve trovarsi in una cartella di rete condivisa.</span><span class="sxs-lookup"><span data-stu-id="de50d-114">This file must be in a shared network folder.</span></span>

    6.  <span data-ttu-id="de50d-115">**Percorso icona**: individuare il file ico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de50d-115">**Icon Path**—Browse to the application's ICO file.</span></span>

    7.  <span data-ttu-id="de50d-116">**Gruppo di licenze applicative**: se sono stati configurati gruppi di licenze, è possibile assegnare l'applicazione a uno selezionandolo nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="de50d-116">**Application License Group**—If you have set up license groups, you can assign the application to one by selecting it in the pull-down list.</span></span>

    8.  <span data-ttu-id="de50d-117">**Gruppo Server**: se si hanno più server di virtualizzazione delle applicazioni, è possibile assegnarlo a uno selezionando l'applicazione nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="de50d-117">**Server Group**—If you have multiple Application Virtualization Servers, you can assign the application to one by selecting it in the pull-down list.</span></span>

3.  <span data-ttu-id="de50d-118">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="de50d-118">Click **Next**.</span></span>

4.  <span data-ttu-id="de50d-119">Nella finestra di dialogo **Seleziona pacchetto** selezionare il pacchetto correlato e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="de50d-119">In the **Select Package** dialog box, select the related package and click **Next**.</span></span>

5.  <span data-ttu-id="de50d-120">Nella schermata **collegamenti pubblicati** selezionare le caselle relative alle posizioni in cui si desidera visualizzare i tasti di scelta rapida dell'applicazione nei computer client e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="de50d-120">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers and click **Next**.</span></span>

6.  <span data-ttu-id="de50d-121">Nella schermata **associazioni di file** è possibile aggiungere nuove associazioni di tipi di file a questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="de50d-121">In the **File Associations** screen, you can add new type file associations to this application.</span></span> <span data-ttu-id="de50d-122">A tale scopo, fare clic su **Aggiungi**, immettere l'estensione (senza un punto precedente), immettere una descrizione e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="de50d-122">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

7.  <span data-ttu-id="de50d-123">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="de50d-123">Click **Next**.</span></span>

8.  <span data-ttu-id="de50d-124">Nella finestra di dialogo **autorizzazioni di accesso** fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="de50d-124">In the **Access Permissions** dialog box, click **Add**.</span></span>

9.  <span data-ttu-id="de50d-125">Nella finestra di dialogo **Aggiungi/modifica gruppo utenti** passare al gruppo utenti.</span><span class="sxs-lookup"><span data-stu-id="de50d-125">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="de50d-126">È anche possibile immettere il dominio e il gruppo digitando le informazioni nei rispettivi campi.</span><span class="sxs-lookup"><span data-stu-id="de50d-126">You can also enter the domain and group by typing the information in the respective fields.</span></span> <span data-ttu-id="de50d-127">Al termine, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="de50d-127">When you finish, click **OK**.</span></span> <span data-ttu-id="de50d-128">È possibile aggiungere altri gruppi con le stesse pagine.</span><span class="sxs-lookup"><span data-stu-id="de50d-128">You can add other groups with the same pages.</span></span>

10. <span data-ttu-id="de50d-129">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="de50d-129">Click **Next**.</span></span>

11. <span data-ttu-id="de50d-130">Nella schermata **Riepilogo** è possibile rivedere le impostazioni di importazione.</span><span class="sxs-lookup"><span data-stu-id="de50d-130">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="de50d-131">Fare clic su **fine** per aggiungere l'applicazione, fare clic su **Torna** per modificare le informazioni o su **Annulla**.</span><span class="sxs-lookup"><span data-stu-id="de50d-131">Click **Finish** to add the application, click **Back** to change the information, or click **Cancel**.</span></span>

## <span data-ttu-id="de50d-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de50d-132">Related topics</span></span>


[<span data-ttu-id="de50d-133">Come gestire le applicazioni in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="de50d-133">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





