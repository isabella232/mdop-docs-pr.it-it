---
title: Configurare le applicazioni e le estensioni delle applicazioni virtuali predefinite nel sistema di gestione
description: Come visualizzare e configurare applicazioni ed estensioni delle applicazioni virtuali predefinite tramite la console di gestione
author: dansimp
ms.assetid: 1e1941d3-fb22-4077-8ec6-7a0cb80335d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2019
ms.openlocfilehash: 7c29ba0e40cf1adbc2b2297124cfb245a65a7ffe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805926"
---
#   <span data-ttu-id="c8455-103">Configurare le applicazioni e le estensioni delle applicazioni virtuali predefinite nel sistema di gestione</span><span class="sxs-lookup"><span data-stu-id="c8455-103">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>

<span data-ttu-id="c8455-104">Usare la procedura seguente per *visualizzare* e *configurare* le estensioni predefinite del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c8455-104">Use the following procedure to *view* and *configure* default package extensions.</span></span>

**<span data-ttu-id="c8455-105">Per visualizzare e configurare le estensioni delle applicazioni virtuali predefinite</span><span class="sxs-lookup"><span data-stu-id="c8455-105">To view and configure default virtual application extensions</span></span>**

1.  <span data-ttu-id="c8455-106">Per visualizzare il pacchetto che si vuole configurare, aprire la console di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="c8455-106">To view the package that you want to configure, open the App-V 5.1 Management Console.</span></span> <span data-ttu-id="c8455-107">Selezionare il pacchetto che si desidera configurare, fare clic con il pulsante destro del mouse sul nome del pacchetto e scegliere **modifica configurazione predefinita**.</span><span class="sxs-lookup"><span data-stu-id="c8455-107">Select the package that you want to configure, right-click the package name and select **edit default configuration**.</span></span>

2.  <span data-ttu-id="c8455-108">Per visualizzare le applicazioni contenute nel pacchetto specificato, nel riquadro **configurazione predefinita** fare clic su **applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="c8455-108">To view the applications contained in the specified package, in the **Default Configuration** pane, click **Applications**.</span></span> <span data-ttu-id="c8455-109">Per visualizzare i tasti di scelta rapida per il pacchetto, fare clic su **scelte rapide**.</span><span class="sxs-lookup"><span data-stu-id="c8455-109">To view the shortcuts for that package, click **Shortcuts**.</span></span> <span data-ttu-id="c8455-110">Per visualizzare le associazioni dei tipi di file per il pacchetto, fare clic su **tipi di file**.</span><span class="sxs-lookup"><span data-stu-id="c8455-110">To view the file type associations for that package, click **File Types**.</span></span>

3.  <span data-ttu-id="c8455-111">Per abilitare le estensioni dell'applicazione, selezionare **Abilita**.</span><span class="sxs-lookup"><span data-stu-id="c8455-111">To enable the application extensions, select **ENABLE**.</span></span>

    <span data-ttu-id="c8455-112">Per abilitare i tasti di scelta rapida, selezionare **attiva collegamenti**.</span><span class="sxs-lookup"><span data-stu-id="c8455-112">To enable shortcuts, select **ENABLE SHORTCUTS**.</span></span> <span data-ttu-id="c8455-113">Per aggiungere un nuovo collegamento per l'applicazione selezionata, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Aggiungi nuovo collegamento**.</span><span class="sxs-lookup"><span data-stu-id="c8455-113">To add a new shortcut for the selected application, right-click the application in the **SHORTCUTS** pane and select **Add new shortcut**.</span></span> <span data-ttu-id="c8455-114">Per rimuovere un collegamento, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Rimuovi collegamento**.</span><span class="sxs-lookup"><span data-stu-id="c8455-114">To remove a shortcut, right-click the application in the **SHORTCUTS** pane and select **Remove Shortcut**.</span></span> <span data-ttu-id="c8455-115">Per modificare un collegamento esistente, fare clic con il pulsante destro del mouse sull'applicazione e scegliere **Modifica collegamento**.</span><span class="sxs-lookup"><span data-stu-id="c8455-115">To edit an existing shortcut, right-click the application and select **Edit Shortcut**.</span></span>

4.  <span data-ttu-id="c8455-116">Per visualizzare le altre estensioni dell'applicazione, fare clic su **Avanzate** e quindi su **Esporta configurazione**.</span><span class="sxs-lookup"><span data-stu-id="c8455-116">To view any other application extensions, click **Advanced** and click **Export Configuration**.</span></span> <span data-ttu-id="c8455-117">Digitare un nome di file e fare clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="c8455-117">Type in a filename and click **Save**.</span></span> <span data-ttu-id="c8455-118">Puoi visualizzare tutte le estensioni dell'applicazione associate al pacchetto usando il file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c8455-118">You can view all application extensions associated with the package using the configuration file.</span></span>

5.  <span data-ttu-id="c8455-119">Per modificare altre estensioni dell'applicazione, modificare il file di configurazione e fare clic su **Importa e Sovrascrivi questa configurazione**.</span><span class="sxs-lookup"><span data-stu-id="c8455-119">To edit other application extensions, modify the configuration file and click **Import and Overwrite this Configuration**.</span></span> <span data-ttu-id="c8455-120">Selezionare il file modificato e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="c8455-120">Select the modified file and click **Open**.</span></span> <span data-ttu-id="c8455-121">Nella finestra di dialogo fare clic su **Sovrascrivi** per completare il processo.</span><span class="sxs-lookup"><span data-stu-id="c8455-121">In the dialog box, click **Overwrite** to complete the process.</span></span>

><span data-ttu-id="c8455-122">**Nota** Se il caricamento non riesce e le dimensioni del file di configurazione sono superiori a 4 MB, sarà necessario aumentare le dimensioni massime dei file consentite dal server.</span><span class="sxs-lookup"><span data-stu-id="c8455-122">**Note** If the upload fails and the size of your configuration file is above 4MB, you will need to increase the maximum file size allowed by the server.</span></span> <span data-ttu-id="c8455-123">Questa operazione può essere eseguita aggiungendo l'attributo maxRequestLength con un valore maggiore della dimensione del file di configurazione (in KB) all'elemento httpRuntime sulla linea 26 di `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config` .</span><span class="sxs-lookup"><span data-stu-id="c8455-123">This can be done by adding the maxRequestLength attribute with a value greater than the size of your configuration file (in KB) to the httpRuntime element on line 26 of `C:\Program Files\Microsoft Application Virtualization Server\ManagementService\Web.config`.</span></span>  
<span data-ttu-id="c8455-124">Ad esempio, la modifica in modo da `<httpRuntime targetFramework="4.5"/>` `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` aumentare la dimensione massima a 8MB</span><span class="sxs-lookup"><span data-stu-id="c8455-124">For example, changing `<httpRuntime targetFramework="4.5"/>` to `<httpRuntime targetFramework="4.5" maxRequestLength="8192"/>` will increase the maximum size to 8MB</span></span>


<span data-ttu-id="c8455-125">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="c8455-125">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c8455-126">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c8455-126">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c8455-127">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="c8455-127">Got an App-V issue?</span></span>** <span data-ttu-id="c8455-128">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c8455-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c8455-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8455-129">Related topics</span></span>


[<span data-ttu-id="c8455-130">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c8455-130">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





