---
title: Come aggiungere o aggiornare pacchetti tramite la console di gestione
description: Come aggiungere o aggiornare pacchetti tramite la console di gestione
author: dansimp
ms.assetid: 62417b63-06b2-437c-8584-523e1dea97c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4ac458a5e33b83e19d72fee39cf837aa6bd57bc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805763"
---
# <span data-ttu-id="9676c-103">Come aggiungere o aggiornare pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="9676c-103">How to Add or Upgrade Packages by Using the Management Console</span></span>


<span data-ttu-id="9676c-104">È possibile eseguire la procedura seguente per aggiungere o aggiornare un pacchetto alla console di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9676c-104">You can the following procedure to add or upgrade a package to the App-V 5.1 Management Console.</span></span> <span data-ttu-id="9676c-105">Per aggiornare un pacchetto già esistente nella console di gestione, eseguire la procedura seguente e importare il pacchetto aggiornato usando lo stesso **nome**del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9676c-105">To upgrade a package that already exists in the Management Console, use the following steps and import the upgraded package using the same package **Name**.</span></span>

**<span data-ttu-id="9676c-106">Per aggiungere un pacchetto alla console di gestione</span><span class="sxs-lookup"><span data-stu-id="9676c-106">To add a package to the Management Console</span></span>**

1.  <span data-ttu-id="9676c-107">Fare clic sulla scheda **pacchetti** nel riquadro di spostamento della visualizzazione della console di gestione.</span><span class="sxs-lookup"><span data-stu-id="9676c-107">Click the **Packages** tab in the navigation pane of the Management Console display.</span></span>

    <span data-ttu-id="9676c-108">Nella console viene visualizzato l'elenco dei pacchetti che sono stati aggiunti al server insieme alle informazioni sullo stato di ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9676c-108">The console displays the list of packages that have been added to the server along with status information about each package.</span></span> <span data-ttu-id="9676c-109">Quando si seleziona un pacchetto, nel riquadro **pacchetti** vengono visualizzate informazioni dettagliate sul pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9676c-109">When a package is selected, detailed information about the package is displayed in the **PACKAGES** pane.</span></span>

    <span data-ttu-id="9676c-110">Fare clic sulla casella di riepilogo a discesa non **raggruppata** e specificare la modalità di visualizzazione dei pacchetti nella console.</span><span class="sxs-lookup"><span data-stu-id="9676c-110">Click the **Ungrouped** drop-down list box and specify how the packages are to be displayed in the console.</span></span> <span data-ttu-id="9676c-111">È anche possibile fare clic sull'intestazione di colonna associata per ordinare i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9676c-111">You can also click the associated column header to sort the packages.</span></span>

2.  <span data-ttu-id="9676c-112">Per specificare il pacchetto che si vuole aggiungere, fare clic su **Aggiungi o Aggiorna pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="9676c-112">To specify the package you want to add, click **Add or Upgrade Packages**.</span></span>

3.  <span data-ttu-id="9676c-113">Digitare il percorso completo del pacchetto che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="9676c-113">Type the full path to the package that you want to add.</span></span> <span data-ttu-id="9676c-114">Usare il formato percorso UNC o HTTP, ad esempio **\\\\servername\\sharename\\foldername\\packagename.AppV** o **http://server.1234/file.appv** , e quindi fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="9676c-114">Use the UNC or HTTP path format, for example **\\\\servername\\sharename\\foldername\\packagename.appv** or **http://server.1234/file.appv**, and then click **Add**.</span></span>

    <span data-ttu-id="9676c-115">**Importante**  Devi selezionare un pacchetto con l'estensione di file **appv** .</span><span class="sxs-lookup"><span data-stu-id="9676c-115">**Important** You must select a package with the **.appv** file name extension.</span></span>

     

4.  <span data-ttu-id="9676c-116">Nella pagina viene visualizzato il messaggio di stato che \*\*aggiunge &lt; PackageName &gt; \*\*.</span><span class="sxs-lookup"><span data-stu-id="9676c-116">The page displays the status message **Adding &lt;Packagename&gt;**.</span></span> <span data-ttu-id="9676c-117">Fare clic su **Importa stato** per controllare lo stato di un pacchetto importato.</span><span class="sxs-lookup"><span data-stu-id="9676c-117">Click **IMPORT STATUS** to check the status of a package that you have imported.</span></span>

    <span data-ttu-id="9676c-118">Fare clic su **OK** per aggiungere il pacchetto e chiudere la pagina **Aggiungi pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="9676c-118">Click **OK** to add the package and close the **Add Package** page.</span></span> <span data-ttu-id="9676c-119">Se durante l'importazione si è verificato un errore, fare clic su **Dettagli** nella pagina **importazione pacchetto** per altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9676c-119">If there was an error during the import, click **Detail** on the **Package Import** page for more information.</span></span> <span data-ttu-id="9676c-120">Il pacchetto appena aggiunto è ora disponibile nel riquadro **pacchetti** .</span><span class="sxs-lookup"><span data-stu-id="9676c-120">The newly added package is now available in the **PACKAGES** pane.</span></span>

5.  <span data-ttu-id="9676c-121">Fare clic su **Chiudi** per chiudere la pagina **Add o upgrade packages** .</span><span class="sxs-lookup"><span data-stu-id="9676c-121">Click **Close** to close the **Add or Upgrade Packages** page.</span></span>

    <span data-ttu-id="9676c-122">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="9676c-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9676c-123">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9676c-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9676c-124">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="9676c-124">Got an App-V issue?</span></span>** <span data-ttu-id="9676c-125">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9676c-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9676c-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9676c-126">Related topics</span></span>


[<span data-ttu-id="9676c-127">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9676c-127">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





