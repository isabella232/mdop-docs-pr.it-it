---
title: Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.0
description: Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.0
author: dansimp
ms.assetid: 0d1f6768-be30-4682-8eeb-aa95918b24c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d54e68caa380025b2ff6f3ea79d30f275b589b30
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805644"
---
# <span data-ttu-id="7e3b4-103">Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="7e3b4-103">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>


<span data-ttu-id="7e3b4-104">Puoi usare una configurazione dinamica per personalizzare un pacchetto di App-V 5,0 per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-104">You can use a dynamic configuration to customize an App-V 5.0 package for a specific user.</span></span> <span data-ttu-id="7e3b4-105">È tuttavia necessario prima di tutto creare il file di configurazione dinamica degli utenti o il file di configurazione della distribuzione dinamica prima di poter usare i file.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="7e3b4-106">La creazione del file è un'operazione manuale avanzata.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="7e3b4-107">Per informazioni generali sui file di configurazione dinamica degli utenti, vedere informazioni [sulla configurazione dinamica di App-V 5,0](about-app-v-50-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="7e3b4-107">For general information about dynamic user configuration files, see, [About App-V 5.0 Dynamic Configuration](about-app-v-50-dynamic-configuration.md).</span></span>

<span data-ttu-id="7e3b4-108">Usare la procedura seguente per creare un file di configurazione utente dinamico usando la console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.0 Management console.</span></span>

**<span data-ttu-id="7e3b4-109">Per creare un file di configurazione utente dinamico</span><span class="sxs-lookup"><span data-stu-id="7e3b4-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="7e3b4-110">Fare clic con il pulsante destro del mouse sul nome del pacchetto che si desidera visualizzare e selezionare **modifica accesso Active Directory** per visualizzare la configurazione assegnata a un gruppo di utenti specificato.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="7e3b4-111">In alternativa, selezionare il pacchetto e fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="7e3b4-112">Usando l'elenco delle **entità pubblicitarie con Access**, selezionare il gruppo di annunci che si vuole personalizzare.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="7e3b4-113">Selezionare **personalizzato** nell'elenco a discesa, se non è già selezionato.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="7e3b4-114">Verrà visualizzato un collegamento denominato **modifica** .</span><span class="sxs-lookup"><span data-stu-id="7e3b4-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="7e3b4-115">Fai clic su **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-115">Click **Edit**.</span></span> <span data-ttu-id="7e3b4-116">Verrà visualizzata la configurazione utente dinamica assegnata al gruppo di annunci.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="7e3b4-117">Fare clic su **Avanzate**e quindi su **Esporta configurazione**.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="7e3b4-118">Digitare un nome di file e fare clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="7e3b4-119">A questo punto è possibile modificare il file per configurare un pacchetto per un utente.</span><span class="sxs-lookup"><span data-stu-id="7e3b4-119">Now you can edit the file to configure a package for a user.</span></span>

    <span data-ttu-id="7e3b4-120">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="7e3b4-120">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="7e3b4-121">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="7e3b4-121">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="7e3b4-122">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="7e3b4-122">Got an App-V issue?</span></span>** <span data-ttu-id="7e3b4-123">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="7e3b4-123">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="7e3b4-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e3b4-124">Related topics</span></span>


[<span data-ttu-id="7e3b4-125">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="7e3b4-125">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





