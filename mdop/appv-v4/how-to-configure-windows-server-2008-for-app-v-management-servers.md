---
title: Come configurare Windows Server 2008 per i server di gestione di App-V
description: Come configurare Windows Server 2008 per i server di gestione di App-V
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817725"
---
# <span data-ttu-id="ad544-103">Come configurare Windows Server 2008 per i server di gestione di App-V</span><span class="sxs-lookup"><span data-stu-id="ad544-103">How to Configure Windows Server 2008 for App-V Management Servers</span></span>


<span data-ttu-id="ad544-104">Il server Windows Server 2008 in cui si installa il servizio Web di gestione di Microsoft Application Virtualization (App-V) richiede l'installazione di Internet Information Services (IIS) come ruolo nel server.</span><span class="sxs-lookup"><span data-stu-id="ad544-104">The Windows Server 2008 server on which you install the Microsoft Application Virtualization (App-V) Management Web Service requires Internet Information Services (IIS) to be installed as a role on the server.</span></span> <span data-ttu-id="ad544-105">Usare la procedura seguente per configurare Windows Server 2008 per supportare l'installazione di app-Vserver.</span><span class="sxs-lookup"><span data-stu-id="ad544-105">Use the following procedure to configure Windows Server 2008 to support App-Vserver installation.</span></span>

**<span data-ttu-id="ad544-106">Per installare IIS in un computer Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="ad544-106">To install IIS on a Windows Server2008 computer</span></span>**

1.  <span data-ttu-id="ad544-107">Nel computer Windows Server2008 fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **strumenti di amministrazione**e quindi fare clic su **Gestione server** per avviare Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ad544-107">On the Windows Server2008 computer, click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Server Manager** to start Server Manager.</span></span> <span data-ttu-id="ad544-108">In Server Manager fare clic con il pulsante destro del mouse sul nodo **ruoli** e scegliere **Aggiungi ruoli** per avviare la **procedura guidata Aggiungi ruoli**.</span><span class="sxs-lookup"><span data-stu-id="ad544-108">In Server Manager, right-click the **Roles** node, and click **Add Roles** to start the **Add Roles Wizard**.</span></span>

2.  <span data-ttu-id="ad544-109">Nella pagina **Selezione ruoli server** della **procedura guidata Aggiungi ruoli**selezionare **Web Server (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="ad544-109">In the **Add Roles Wizard**, on the **Select Server Roles** page, select **Web Server (IIS)**.</span></span> <span data-ttu-id="ad544-110">Quando richiesto, fare clic su **Aggiungi caratteristiche necessarie** per aggiungere le caratteristiche dipendenti.</span><span class="sxs-lookup"><span data-stu-id="ad544-110">When prompted, click **Add Required Features** to add the dependent features.</span></span>

3.  <span data-ttu-id="ad544-111">Nella pagina **Selezione ruoli server** fare clic su **Avanti**e quindi di nuovo su **Avanti** .</span><span class="sxs-lookup"><span data-stu-id="ad544-111">On the **Select Server Roles** page, Click **Next**, and then click **Next** again.</span></span>

4.  <span data-ttu-id="ad544-112">Nella pagina **Seleziona servizi ruolo** della **procedura guidata Aggiungi ruoli**:</span><span class="sxs-lookup"><span data-stu-id="ad544-112">In the **Add Roles Wizard**, on the **Select Role Services** page:</span></span>

    1.  <span data-ttu-id="ad544-113">In **sviluppo applicazione**selezionare **ASP.NET** e, quando richiesto, fare clic su **Aggiungi servizi ruolo necessari** per aggiungere i servizi e le funzionalità dei ruoli dipendenti.</span><span class="sxs-lookup"><span data-stu-id="ad544-113">Under **Application Development**, select **ASP.NET** and, when prompted, click **Add Required Role Services** to add the dependent roles services and features.</span></span>

    2.  <span data-ttu-id="ad544-114">In **sicurezza**selezionare **autenticazione di Windows**.</span><span class="sxs-lookup"><span data-stu-id="ad544-114">Under **Security**, select **Windows Authentication**.</span></span>

    3.  <span data-ttu-id="ad544-115">Nel nodo **strumenti di gestione** selezionare **script e strumenti di gestione di IIS**.</span><span class="sxs-lookup"><span data-stu-id="ad544-115">In the **Management Tools** node, select **IIS Management Scripts and Tools**.</span></span> <span data-ttu-id="ad544-116">In **compatibilità**con la gestione di IIS6 verificare che sia selezionata la compatibilità della **metabase IIS6** e la **Compatibilità WMI di IIS6** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="ad544-116">Under **IIS6 Management Compatibility**, ensure that both **IIS6 Metabase Compatibility** and **IIS6 WMI Compatibility** are selected, and then click **Next**.</span></span>

5.  <span data-ttu-id="ad544-117">Nella pagina **Conferma selezioni installazione** fare clic su **Installa**e quindi completare il resto della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="ad544-117">On the **Confirm Installation Selections** page, click **Install**, and then complete the rest of the wizard.</span></span>

6.  <span data-ttu-id="ad544-118">Fare clic su **Chiudi** per uscire dalla **procedura guidata Aggiungi ruoli**e quindi chiudere Gestione server.</span><span class="sxs-lookup"><span data-stu-id="ad544-118">Click **Close** to exit the **Add Roles Wizard**, and then close Server Manager.</span></span>

## <span data-ttu-id="ad544-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad544-119">Related topics</span></span>


[<span data-ttu-id="ad544-120">Requisiti per la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ad544-120">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="ad544-121">Elenchi di controllo per la distribuzione e l'aggiornamento di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ad544-121">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





