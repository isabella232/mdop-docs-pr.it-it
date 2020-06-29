---
title: Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione
description: Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione
author: dansimp
ms.assetid: 4f249ee3-cc2d-4b1e-afe5-d1cbf9cabd88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57ce4b82cc552e0a4adc2272f849111d8da0be71
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805589"
---
# <span data-ttu-id="20920-103">Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="20920-103">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>


<span data-ttu-id="20920-104">Usare la procedura seguente per personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="20920-104">Use the following procedure to customize the virtual application extensions for an Active Directory (AD) group.</span></span>

**<span data-ttu-id="20920-105">Per personalizzare le estensioni delle applicazioni virtuali per un gruppo di annunci</span><span class="sxs-lookup"><span data-stu-id="20920-105">To customize virtual applications extensions for an AD group</span></span>**

1.  <span data-ttu-id="20920-106">Per visualizzare il pacchetto che si vuole configurare, aprire la console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="20920-106">To view the package that you want to configure, open the App-V 5.0 Management Console.</span></span> <span data-ttu-id="20920-107">Per visualizzare la configurazione assegnata a un gruppo di utenti specifico, selezionare il pacchetto e fare clic con il pulsante destro del mouse sul nome del pacchetto e scegliere **modifica Active Directory Access**.</span><span class="sxs-lookup"><span data-stu-id="20920-107">To view the configuration that is assigned to a given user group, select the package, and right-click the package name and select **Edit active directory access**.</span></span> <span data-ttu-id="20920-108">In alternativa, selezionare il pacchetto e fare clic su **modifica** nel riquadro di **accesso ad** .</span><span class="sxs-lookup"><span data-stu-id="20920-108">Alternatively, select the package and click **EDIT** in the **AD ACCESS** pane.</span></span>

2.  <span data-ttu-id="20920-109">Per personalizzare un gruppo di annunci, puoi trovare il gruppo nell'elenco delle **entità pubblicitarie con Access**.</span><span class="sxs-lookup"><span data-stu-id="20920-109">To customize an AD group, you can find the group from the list of **AD Entities with Access**.</span></span> <span data-ttu-id="20920-110">Quindi, usando la casella di menu a discesa nel riquadro **configurazione assegnata** , selezionare **personalizzato**e quindi fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="20920-110">Then, using the drop-down box in the **Assigned Configuration** pane, select **Custom**, and then click **EDIT**.</span></span>

3.  <span data-ttu-id="20920-111">Per disabilitare tutte le estensioni per una determinata applicazione, deselezionare **Abilita**.</span><span class="sxs-lookup"><span data-stu-id="20920-111">To disable all extensions for a given application, clear **ENABLE**.</span></span>

    <span data-ttu-id="20920-112">Per aggiungere un nuovo collegamento per l'applicazione selezionata, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Aggiungi nuovo collegamento**.</span><span class="sxs-lookup"><span data-stu-id="20920-112">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane, and select **Add new shortcut**.</span></span> <span data-ttu-id="20920-113">Per rimuovere un collegamento, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Rimuovi collegamento**.</span><span class="sxs-lookup"><span data-stu-id="20920-113">To remove a shortcut, right-click the application in the **SHORTCUTS** pane, and select **Remove Shortcut**.</span></span> <span data-ttu-id="20920-114">Per modificare un collegamento esistente, fare clic con il pulsante destro del mouse sull'applicazione e scegliere **Modifica collegamento**.</span><span class="sxs-lookup"><span data-stu-id="20920-114">To edit an existing shortcut, right-click the application, and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="20920-115">Per visualizzare le altre estensioni dell'applicazione, fare clic su **Avanzate**e quindi su **Esporta configurazione**.</span><span class="sxs-lookup"><span data-stu-id="20920-115">To view any other application extensions, click **Advanced**, and click **Export Configuration**.</span></span> <span data-ttu-id="20920-116">Digitare un nome di file e fare clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="20920-116">Type in a filename and click **Save**.</span></span> <span data-ttu-id="20920-117">Puoi visualizzare tutte le estensioni dell'applicazione associate al pacchetto usando il file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="20920-117">You can view all application extensions that are associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="20920-118">Per modificare altre estensioni dell'applicazione, modificare il file di configurazione e fare clic su **Importa e Sovrascrivi questa configurazione**.</span><span class="sxs-lookup"><span data-stu-id="20920-118">To edit additional application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="20920-119">Selezionare il file modificato e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="20920-119">Select the modified file and click **Open**.</span></span> <span data-ttu-id="20920-120">Nella finestra di dialogo fare clic su **Sovrascrivi** per completare il processo.</span><span class="sxs-lookup"><span data-stu-id="20920-120">In the dialog, click **Overwrite** to complete the process.</span></span>

    <span data-ttu-id="20920-121">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="20920-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="20920-122">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="20920-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="20920-123">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="20920-123">Got an App-V issue?</span></span>** <span data-ttu-id="20920-124">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="20920-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="20920-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20920-125">Related topics</span></span>


[<span data-ttu-id="20920-126">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="20920-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





