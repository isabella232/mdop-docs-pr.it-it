---
title: Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1
description: Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805643"
---
# <span data-ttu-id="9df9c-103">Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9df9c-103">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>


<span data-ttu-id="9df9c-104">Puoi usare una configurazione dinamica per personalizzare un pacchetto di App-V 5,1 per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="9df9c-104">You can use a dynamic configuration to customize an App-V 5.1 package for a specific user.</span></span> <span data-ttu-id="9df9c-105">È tuttavia necessario prima di tutto creare il file di configurazione dinamica degli utenti o il file di configurazione della distribuzione dinamica prima di poter usare i file.</span><span class="sxs-lookup"><span data-stu-id="9df9c-105">However, you must first create the dynamic user configuration (.xml) file or the dynamic deployment configuration file before you can use the files.</span></span> <span data-ttu-id="9df9c-106">La creazione del file è un'operazione manuale avanzata.</span><span class="sxs-lookup"><span data-stu-id="9df9c-106">Creation of the file is an advanced manual operation.</span></span> <span data-ttu-id="9df9c-107">Per informazioni generali sui file di configurazione dinamica degli utenti, vedere informazioni [sulla configurazione dinamica di App-V 5,1](about-app-v-51-dynamic-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="9df9c-107">For general information about dynamic user configuration files, see, [About App-V 5.1 Dynamic Configuration](about-app-v-51-dynamic-configuration.md).</span></span>

<span data-ttu-id="9df9c-108">Usare la procedura seguente per creare un file di configurazione utente dinamico usando la console di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9df9c-108">Use the following procedure to create a Dynamic User Configuration file by using the App-V 5.1 Management console.</span></span>

**<span data-ttu-id="9df9c-109">Per creare un file di configurazione utente dinamico</span><span class="sxs-lookup"><span data-stu-id="9df9c-109">To create a Dynamic User Configuration file</span></span>**

1.  <span data-ttu-id="9df9c-110">Fare clic con il pulsante destro del mouse sul nome del pacchetto che si desidera visualizzare e selezionare **modifica accesso Active Directory** per visualizzare la configurazione assegnata a un gruppo di utenti specificato.</span><span class="sxs-lookup"><span data-stu-id="9df9c-110">Right-click the name of the package that you want to view and select **Edit active directory access** to view the configuration that is assigned to a given user group.</span></span> <span data-ttu-id="9df9c-111">In alternativa, selezionare il pacchetto e fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="9df9c-111">Alternatively, select the package, and click **Edit**.</span></span>

2.  <span data-ttu-id="9df9c-112">Usando l'elenco delle **entità pubblicitarie con Access**, selezionare il gruppo di annunci che si vuole personalizzare.</span><span class="sxs-lookup"><span data-stu-id="9df9c-112">Using the list of **AD Entities with Access**, select the AD group that you want to customize.</span></span> <span data-ttu-id="9df9c-113">Selezionare **personalizzato** nell'elenco a discesa, se non è già selezionato.</span><span class="sxs-lookup"><span data-stu-id="9df9c-113">Select **Custom** from the drop-down list, if it is not already selected.</span></span> <span data-ttu-id="9df9c-114">Verrà visualizzato un collegamento denominato **modifica** .</span><span class="sxs-lookup"><span data-stu-id="9df9c-114">A link named **Edit** will be displayed.</span></span>

3.  <span data-ttu-id="9df9c-115">Fai clic su **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="9df9c-115">Click **Edit**.</span></span> <span data-ttu-id="9df9c-116">Verrà visualizzata la configurazione utente dinamica assegnata al gruppo di annunci.</span><span class="sxs-lookup"><span data-stu-id="9df9c-116">The Dynamic User Configuration that is assigned to the AD Group will be displayed.</span></span>

4.  <span data-ttu-id="9df9c-117">Fare clic su **Avanzate**e quindi su **Esporta configurazione**.</span><span class="sxs-lookup"><span data-stu-id="9df9c-117">Click **Advanced**, and then click **Export Configuration**.</span></span> <span data-ttu-id="9df9c-118">Digitare un nome di file e fare clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="9df9c-118">Type in a filename and click **Save**.</span></span> <span data-ttu-id="9df9c-119">A questo punto è possibile modificare il file per configurare un pacchetto per un utente.</span><span class="sxs-lookup"><span data-stu-id="9df9c-119">Now you can edit the file to configure a package for a user.</span></span>

    **<span data-ttu-id="9df9c-120">Nota</span><span class="sxs-lookup"><span data-stu-id="9df9c-120">Note</span></span>**  
    <span data-ttu-id="9df9c-121">Per esportare una configurazione durante l'esecuzione in Windows Server, è necessario disabilitare "configurazione di sicurezza avanzata di IE".</span><span class="sxs-lookup"><span data-stu-id="9df9c-121">To export a configuration while running on Windows Server, you must disable "IE Enhanced Security Configuration".</span></span> <span data-ttu-id="9df9c-122">Se questa funzionalità è abilitata e impostata su blocca download, non è possibile scaricare nulla dal server App-V.</span><span class="sxs-lookup"><span data-stu-id="9df9c-122">If this is enabled and set to block downloads, you cannot download anything from the App-V Server.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="9df9c-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9df9c-123">Related topics</span></span>


[<span data-ttu-id="9df9c-124">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9df9c-124">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









