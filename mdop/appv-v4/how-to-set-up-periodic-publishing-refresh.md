---
title: Come configurare l'aggiornamento periodico per la pubblicazione
description: Come configurare l'aggiornamento periodico per la pubblicazione
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816555"
---
# <span data-ttu-id="d39fd-103">Come configurare l'aggiornamento periodico per la pubblicazione</span><span class="sxs-lookup"><span data-stu-id="d39fd-103">How to Set Up Periodic Publishing Refresh</span></span>


<span data-ttu-id="d39fd-104">È possibile usare la procedura seguente per configurare il client per aggiornare periodicamente le informazioni di pubblicazione dai server App-V.</span><span class="sxs-lookup"><span data-stu-id="d39fd-104">You can use the following procedure to configure the client to periodically refresh the publishing information from the App-V servers.</span></span> <span data-ttu-id="d39fd-105">Dopo aver configurato il client, l'operazione di aggiornamento è automatica.</span><span class="sxs-lookup"><span data-stu-id="d39fd-105">After the client is configured, the refresh operation is automatic.</span></span> <span data-ttu-id="d39fd-106">Queste impostazioni configurano le impostazioni predefinite per il client in modo che tutti gli utenti di questo computer visualizzino le stesse impostazioni.</span><span class="sxs-lookup"><span data-stu-id="d39fd-106">These settings configure the default settings for the client so that all users on this computer will see the same settings.</span></span>

<span data-ttu-id="d39fd-107">**Nota**  Dopo aver eseguito questa procedura, le informazioni di pubblicazione verranno aggiornate in base alle nuove impostazioni dopo il primo aggiornamento all'accesso.</span><span class="sxs-lookup"><span data-stu-id="d39fd-107">**Note** After you have performed this procedure, the publishing information will be refreshed according to the new settings after the first refresh at login.</span></span> <span data-ttu-id="d39fd-108">Quando si verifica questo primo aggiornamento, il server può eseguire l'override delle impostazioni del computer con impostazioni diverse, a seconda del modo in cui è configurato.</span><span class="sxs-lookup"><span data-stu-id="d39fd-108">When this first refresh occurs, the server might override the computer settings with different settings, depending on how it is configured.</span></span> <span data-ttu-id="d39fd-109">La scheda **Aggiorna** nella finestra di dialogo **Proprietà** Mostra le impostazioni del computer client configurate localmente e le impostazioni eventualmente configurate per l'utente dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="d39fd-109">The **Refresh** tab in the **Properties** dialog box shows the locally configured client computer settings and any settings that might have been configured for the user by the publishing server.</span></span>

 

**<span data-ttu-id="d39fd-110">Per aggiornare periodicamente le informazioni di pubblicazione dall'Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="d39fd-110">To periodically refresh the publishing information from the Application Virtualization Servers</span></span>**

1.  <span data-ttu-id="d39fd-111">Fare clic su **server di pubblicazione** nel riquadro **ambito** .</span><span class="sxs-lookup"><span data-stu-id="d39fd-111">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="d39fd-112">Nel riquadro **risultati** fare clic con il pulsante destro del mouse sul server desiderato e scegliere **Proprietà** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="d39fd-112">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="d39fd-113">Nella scheda **Aggiorna** della finestra di dialogo **Proprietà** selezionare la casella di controllo **Aggiorna configurazione ogni** e immettere un numero che rappresenti la frequenza nel campo.</span><span class="sxs-lookup"><span data-stu-id="d39fd-113">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="d39fd-114">Quindi selezionare **minuti**, **ore**e **giorni** dal menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="d39fd-114">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span>

    <span data-ttu-id="d39fd-115">**Nota**  Questa impostazione farà sì che il client aggiorni le informazioni di pubblicazione ogni volta che il periodo configurato trascorre.</span><span class="sxs-lookup"><span data-stu-id="d39fd-115">**Note** This setting will cause the client to refresh publishing information every time the configured period elapses.</span></span> <span data-ttu-id="d39fd-116">Se l'utente non ha effettuato l'accesso quando è il momento di eseguire l'aggiornamento, l'aggiornamento avverrà quando l'utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="d39fd-116">If the user is not logged in when it's time to do a refresh, the refresh will take place when the user next logs in.</span></span> <span data-ttu-id="d39fd-117">Il timer viene quindi riavviato per il periodo successivo.</span><span class="sxs-lookup"><span data-stu-id="d39fd-117">The timer is then started again for the next period.</span></span>

     

4.  <span data-ttu-id="d39fd-118">Fare clic su **applica** per modificare la configurazione.</span><span class="sxs-lookup"><span data-stu-id="d39fd-118">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="d39fd-119">Al termine della configurazione del server, fare clic su **OK** per uscire dalla finestra di dialogo e tornare alla console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="d39fd-119">When you finish configuring the server, click **OK** to exit the dialog box and return to the Application Virtualization Client Management Console.</span></span>

## <span data-ttu-id="d39fd-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d39fd-120">Related topics</span></span>


[<span data-ttu-id="d39fd-121">Come configurare il client in Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="d39fd-121">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





