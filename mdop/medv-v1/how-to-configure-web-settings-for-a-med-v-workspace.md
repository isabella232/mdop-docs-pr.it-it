---
title: Come configurare le impostazioni Web per un'area di lavoro MED-V
description: Come configurare le impostazioni Web per un'area di lavoro MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827066"
---
# <span data-ttu-id="97ba1-103">Come configurare le impostazioni Web per un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="97ba1-103">How to Configure Web Settings for a MED-V Workspace</span></span>


<span data-ttu-id="97ba1-104">I siti Web che possono essere visualizzati solo nelle versioni precedenti di Internet Explorer e che non sono presenti nel sistema operativo host possono essere visualizzati in versioni precedenti di Internet Explorer all'interno dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="97ba1-104">Web sites that can only be displayed in older versions of Internet Explorer and that do not exist in the host operating system can be viewed in older versions of Internet Explorer within the MED-V workspace.</span></span> <span data-ttu-id="97ba1-105">L'utente non deve aprire un browser nell'area di lavoro MED-V per visualizzare i siti Web specificati.</span><span class="sxs-lookup"><span data-stu-id="97ba1-105">The user does not need to open a browser in the MED-V workspace to view the specified Web sites.</span></span> <span data-ttu-id="97ba1-106">L'utente può aprire un browser nell'host e reindirizzarlo automaticamente all'area di lavoro MED-V e viceversa.</span><span class="sxs-lookup"><span data-stu-id="97ba1-106">The user can open a browser on the host and automatically be redirected to the MED-V workspace and vice versa.</span></span>

<span data-ttu-id="97ba1-107">Le procedure seguenti descrivono come è possibile impostare un elenco di regole di esplorazione Web per un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="97ba1-107">The following procedures describe how you can set a list of Web browsing rules for a MED-V workspace.</span></span> <span data-ttu-id="97ba1-108">Tutti i siti inclusi nelle regole possono essere visualizzati nell'area di lavoro MED-V o nell'host, come definito dall'amministratore.</span><span class="sxs-lookup"><span data-stu-id="97ba1-108">All sites included in the rules can be browsed either in the MED-V workspace or on the host, as defined by the administrator.</span></span> <span data-ttu-id="97ba1-109">Tutti i siti non definiti nelle regole vengono visualizzati dall'ambiente in cui sono stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="97ba1-109">All sites not defined within the rules are browsed from the environment in which they were requested.</span></span> <span data-ttu-id="97ba1-110">Tuttavia, è possibile configurarli anche come gruppo, per essere visualizzati nell'area di lavoro MED-V o nell'host.</span><span class="sxs-lookup"><span data-stu-id="97ba1-110">However, you can configure them as a group as well, to be browsed in the MED-V workspace or the host.</span></span>

**<span data-ttu-id="97ba1-111">Nota</span><span class="sxs-lookup"><span data-stu-id="97ba1-111">Note</span></span>**  
<span data-ttu-id="97ba1-112">Le impostazioni Web vengono applicate solo a Internet Explorer e a nessun altro browser.</span><span class="sxs-lookup"><span data-stu-id="97ba1-112">Web settings are applied only to Internet Explorer and to no other browsers.</span></span>



<span data-ttu-id="97ba1-113">Tutte le impostazioni Web sono configurate nel modulo **criteri** , nella scheda **Web** .</span><span class="sxs-lookup"><span data-stu-id="97ba1-113">All Web settings are configured in the **Policy** module, on the **Web** tab.</span></span>

## <span data-ttu-id="97ba1-114">Come configurare le impostazioni Web per l'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="97ba1-114">How to Configure Web Settings for the MED-V Workspace</span></span>


**<span data-ttu-id="97ba1-115">Per configurare le impostazioni Web per l'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="97ba1-115">To configure Web settings for the MED-V workspace</span></span>**

1.  <span data-ttu-id="97ba1-116">Fare clic sull'area di lavoro MED-V da configurare.</span><span class="sxs-lookup"><span data-stu-id="97ba1-116">Click the MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="97ba1-117">Selezionare la casella di controllo **Sfoglia l'elenco degli URL definiti nella tabella seguente** per reindirizzare l'utente a un browser all'interno dell'area di lavoro o dell'host MED-V, quando l'utente accede a un URL conforme alle regole Web specificate.</span><span class="sxs-lookup"><span data-stu-id="97ba1-117">Select the **Browse the list of URLs defined in the following table** check box to redirect the user to a browser within the MED-V workspace or host, when the user browses to a URL that conforms to the Web rules specified.</span></span>

3.  <span data-ttu-id="97ba1-118">Fare clic su una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="97ba1-118">Click one of the following:</span></span>

    -   <span data-ttu-id="97ba1-119">**Nell'area di lavoro**: reindirizza a un browser nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="97ba1-119">**In the Workspace**—Redirect to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="97ba1-120">**Nell'host**: reindirizza a un browser nell'host.</span><span class="sxs-lookup"><span data-stu-id="97ba1-120">**In the host**—Redirect to a browser on the host.</span></span>

4.  <span data-ttu-id="97ba1-121">Selezionare la casella di controllo **Sfoglia tutti gli altri URL** per reindirizzare tutti gli URL esclusi dalle regole Web all'area di lavoro host o MED-V.</span><span class="sxs-lookup"><span data-stu-id="97ba1-121">Select the **Browse all other URLs** check box to redirect all URLs excluded from the Web rules to the host or MED-V workspace.</span></span>

5.  <span data-ttu-id="97ba1-122">Fare clic su una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="97ba1-122">Click one of the following:</span></span>

    -   <span data-ttu-id="97ba1-123">**Nell'area di lavoro**: reindirizza tutti gli altri URL in un browser nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="97ba1-123">**In the Workspace**—Redirect all other URLs to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="97ba1-124">**Nell'host**: reindirizza tutti gli altri URL in un browser nell'host.</span><span class="sxs-lookup"><span data-stu-id="97ba1-124">**In the host**—Redirect all other URLs to a browser on the host.</span></span>

6.  <span data-ttu-id="97ba1-125">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="97ba1-125">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="97ba1-126">Come aggiungere una regola Web</span><span class="sxs-lookup"><span data-stu-id="97ba1-126">How to Add a Web Rule</span></span>


**<span data-ttu-id="97ba1-127">Per aggiungere una regola Web</span><span class="sxs-lookup"><span data-stu-id="97ba1-127">To add a Web rule</span></span>**

1.  <span data-ttu-id="97ba1-128">Selezionare la casella di controllo **Sfoglia l'elenco degli URL definiti nella tabella seguente** per abilitare le regole di esplorazione Web.</span><span class="sxs-lookup"><span data-stu-id="97ba1-128">Select the **Browse the list of URLs defined in the following table** check box to enable the Web browsing rules.</span></span>

2.  <span data-ttu-id="97ba1-129">Fai clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="97ba1-129">Click **Add**.</span></span>

    <span data-ttu-id="97ba1-130">Viene aggiunta una nuova regola Web.</span><span class="sxs-lookup"><span data-stu-id="97ba1-130">A new Web rule is added.</span></span>

3.  <span data-ttu-id="97ba1-131">Configurare le proprietà della regola Web come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="97ba1-131">Configure the Web rule properties as described in the following table.</span></span>

4.  <span data-ttu-id="97ba1-132">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="97ba1-132">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="97ba1-133">Proprietà Web dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="97ba1-133">MED-V Workspace Web Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="97ba1-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="97ba1-134">Property</span></span></th>
<th align="left"><span data-ttu-id="97ba1-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97ba1-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97ba1-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="97ba1-136">Type</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="97ba1-137">Suffisso </strong> di dominio: consente di accedere a qualsiasi indirizzo host che termina con il suffisso specificato nella <strong> </strong> proprietà Value e viene impostato in base all'opzione impostata nell' <strong> esplorazione Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="97ba1-137">Domain suffix</strong>—Access to any host address ending with the suffix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="97ba1-138">Prefisso IP </strong> : consente di accedere a qualsiasi indirizzo IP completo o parziale nell'intervallo del prefisso specificato nella <strong> proprietà Value </strong> e viene impostato in base all'opzione impostata nell' <strong> esplorazione Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="97ba1-138">IP Prefix</strong>—Access to any full or partial IP address in the range of the prefix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="97ba1-139">Tutti gli indirizzi locali </strong> : accedere a tutti gli indirizzi senza &#39;. &#39; e viene impostato in base all'opzione impostata in <strong> Web browsing </strong> .</span><span class="sxs-lookup"><span data-stu-id="97ba1-139">All Local Addresses</strong>—Access to all addresses without a &#39;.&#39; and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97ba1-140">Value</span><span class="sxs-lookup"><span data-stu-id="97ba1-140">Value</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="97ba1-141">Se <strong> il suffisso </strong> di dominio è selezionato nella <strong> </strong> proprietà Type, immettere un suffisso di dominio.</span><span class="sxs-lookup"><span data-stu-id="97ba1-141">If <strong>Domain suffix</strong> is selected in the <strong>Type</strong> property, enter a domain suffix.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="97ba1-142">Nota</span><span class="sxs-lookup"><span data-stu-id="97ba1-142">Note</span></span></strong><br/><ul>
<li><p><span data-ttu-id="97ba1-143">Non immettere &quot; \* &quot; prima del suffisso.</span><span class="sxs-lookup"><span data-stu-id="97ba1-143">Do not enter &quot;\*&quot; before the suffix.</span></span></p></li>
<li><p><span data-ttu-id="97ba1-144">I suffissi di dominio supportano anche gli alias.</span><span class="sxs-lookup"><span data-stu-id="97ba1-144">Domain suffixes support aliases as well.</span></span></p></li>
</ul>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="97ba1-145">Se l'opzione prefisso IP è selezionata <strong> nella </strong> Proprietà tipo, immettere un indirizzo IP completo o parziale.</span><span class="sxs-lookup"><span data-stu-id="97ba1-145">If IP Prefix is selected in the <strong>Type</strong> property, enter a full or partial IP address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="97ba1-146">Come eliminare una regola Web</span><span class="sxs-lookup"><span data-stu-id="97ba1-146">How to Delete a Web Rule</span></span>


**<span data-ttu-id="97ba1-147">Per eliminare una regola Web</span><span class="sxs-lookup"><span data-stu-id="97ba1-147">To delete a Web rule</span></span>**

1.  <span data-ttu-id="97ba1-148">Nel riquadro **Web** selezionare la regola Web da eliminare.</span><span class="sxs-lookup"><span data-stu-id="97ba1-148">In the **Web** pane, select the Web rule to delete.</span></span>

2.  <span data-ttu-id="97ba1-149">Fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="97ba1-149">Click **Remove**.</span></span>

    <span data-ttu-id="97ba1-150">La regola Web viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="97ba1-150">The Web rule is deleted.</span></span>

## <span data-ttu-id="97ba1-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97ba1-151">Related topics</span></span>


[<span data-ttu-id="97ba1-152">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="97ba1-152">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="97ba1-153">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="97ba1-153">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









