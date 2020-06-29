---
title: Cercare e filtrare l'elenco di oggetti Criteri di gruppo
description: Cercare e filtrare l'elenco di oggetti Criteri di gruppo
author: dansimp
ms.assetid: 1bc58a38-033c-4aed-9eb4-c239827f5501
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5646a51a37a4ca9195fb9ef858e8c5920ca7738a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820265"
---
# <span data-ttu-id="a772e-103">Cercare e filtrare l'elenco di oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="a772e-103">Search and Filter the List of GPOs</span></span>


<span data-ttu-id="a772e-104">In Advanced Group Policy Management è possibile eseguire una ricerca nell'elenco degli oggetti Criteri di gruppo e dei relativi attributi per filtrare l'elenco dei GPO visualizzati.</span><span class="sxs-lookup"><span data-stu-id="a772e-104">In Advanced Group Policy Management (AGPM), you can search the list of Group Policy Objects (GPOs) and their attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="a772e-105">Ad esempio, puoi cercare gli oggetti Criteri di ricerca con un nome, uno stato o un commento specifico.</span><span class="sxs-lookup"><span data-stu-id="a772e-105">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="a772e-106">È anche possibile cercare gli oggetti Criteri di gruppo modificati per l'ultima volta da un determinato amministratore dei criteri di raggruppamento o in una data specifica.</span><span class="sxs-lookup"><span data-stu-id="a772e-106">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

## <span data-ttu-id="a772e-107">Esecuzione di una ricerca complessa</span><span class="sxs-lookup"><span data-stu-id="a772e-107">Performing a complex search</span></span>


<span data-ttu-id="a772e-108">È possibile eseguire una ricerca complessa usando il formato *attributo GPO 1: stringa di ricerca 1 attributo GPO 2: stringa di ricerca 2... stringhe di ricerca in tutte le colonne*.</span><span class="sxs-lookup"><span data-stu-id="a772e-108">You can perform a complex search by using the format *GPO attribute 1: search string 1 GPO attribute 2: search string 2…all-column search strings*.</span></span> <span data-ttu-id="a772e-109">La ricerca non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a772e-109">The search is not case-sensitive.</span></span>

-   <span data-ttu-id="a772e-110">**Attributo GPO:** Qualsiasi intestazione di colonna nell'elenco di GPO in Advanced Group Policy Management diverso da **versione computer** o **versione utente**.</span><span class="sxs-lookup"><span data-stu-id="a772e-110">**GPO attribute:** Any column heading in the list of GPOs in AGPM other than **Computer Version** or **User Version**.</span></span> <span data-ttu-id="a772e-111">Gli attributi GPO includono il nome del GPO, lo stato, l'utente che ha modificato di recente il GPO, la data e l'ora in cui l'oggetto Criteri di stato è stato modificato più di recente, commento, stato GPO e filtro WMI applicato all'oggetto Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="a772e-111">GPO attributes include the GPO name, state, user who most recently changed the GPO, date and time when the GPO was most recently changed, comment, GPO status, and WMI filter applied to the GPO.</span></span>

-   <span data-ttu-id="a772e-112">**Stringa di ricerca:** Testo per cui eseguire la ricerca nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="a772e-112">**Search string:** Text for which to search in the specified column.</span></span> <span data-ttu-id="a772e-113">Se una stringa include spazi, è necessario racchiuderla tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="a772e-113">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

-   <span data-ttu-id="a772e-114">**Stringhe di ricerca in tutte le colonne:** Testo per il quale eseguire la ricerca in tutte le colonne dell'elenco di GPO in Advanced Group Policy Management diverse dalla versione **computer** e **dall'utente**.</span><span class="sxs-lookup"><span data-stu-id="a772e-114">**All-column search strings:** Text for which to search in all columns in the list of GPOs in AGPM other than **Computer Version** and **User Version**.</span></span> <span data-ttu-id="a772e-115">Puoi includere più stringhe separate da spazi.</span><span class="sxs-lookup"><span data-stu-id="a772e-115">You can include multiple strings separated by spaces.</span></span> <span data-ttu-id="a772e-116">Se una stringa include spazi, è necessario racchiuderla tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="a772e-116">If a string includes spaces, you must enclose the string with quotation marks.</span></span>

<span data-ttu-id="a772e-117">Ogni coppia di attributi GPO e stringa di ricerca e ogni stringa di ricerca di tutte le colonne vengono combinati usando un'operazione logica e.</span><span class="sxs-lookup"><span data-stu-id="a772e-117">Each GPO attribute and search string pair and each all-column search string are combined by using a logical AND operation.</span></span> <span data-ttu-id="a772e-118">Il risultato è un elenco di tutti gli oggetti Criteri di gruppo per cui ogni attributo specificato include la stringa di ricerca specificata e per cui tutte le stringhe di ricerca di tutte le colonne vengono visualizzate in almeno una colonna.</span><span class="sxs-lookup"><span data-stu-id="a772e-118">The result is a list of all GPOs for which each specified attribute includes the specified search string and for which any all-column search strings appear in at least one column.</span></span> <span data-ttu-id="a772e-119">La ricerca restituisce eventuali corrispondenze parziali per le stringhe, in modo che sia possibile immettere parte di un nome di oggetto o di un nome utente e visualizzare un elenco di tutti i GPO che includono il testo nel nome.</span><span class="sxs-lookup"><span data-stu-id="a772e-119">The search returns any partial matches for strings so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="a772e-120">Di seguito sono riportati alcuni esempi di ricerche:</span><span class="sxs-lookup"><span data-stu-id="a772e-120">The following are examples of searches:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a772e-121">Descrizione del risultato della ricerca</span><span class="sxs-lookup"><span data-stu-id="a772e-121">Description of search result</span></span></th>
<th align="left"><span data-ttu-id="a772e-122">Query di ricerca</span><span class="sxs-lookup"><span data-stu-id="a772e-122">Search query</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a772e-123">Tutti i GPO con nomi che includono la <strong> sicurezza del testo </strong> e il <strong> Nord America </strong> .</span><span class="sxs-lookup"><span data-stu-id="a772e-123">All GPOs with names that include the text <strong>security</strong> and <strong>North America</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a772e-124">Nome: </strong><strong> </strong><strong> nome sicurezza: </strong> &quot; <strong> Nord America</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="a772e-124">name:</strong><strong>security</strong><strong>name:</strong>&quot;<strong>North America</strong>&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a772e-125">Tutti i GPO estratti.</span><span class="sxs-lookup"><span data-stu-id="a772e-125">All checked out GPOs.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a772e-126">stato: </strong> &quot; <strong> Estratto</strong>&quot;</span><span class="sxs-lookup"><span data-stu-id="a772e-126">state:</strong>&quot;<strong>checked out</strong>&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a772e-127">Tutti i GPO modificati di recente dall'utente <strong> Administrator </strong> e modificati di recente nel mese precedente.</span><span class="sxs-lookup"><span data-stu-id="a772e-127">All GPOs most recently changed by the user named <strong>Administrator</strong> and most recently changed within the previous month.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a772e-128">modificato da: </strong><strong> </strong><strong> modifica data amministratore: </strong><strong> lastmonth</span><span class="sxs-lookup"><span data-stu-id="a772e-128">changed by:</strong><strong>Administrator</strong><strong>change date:</strong><strong>lastmonth</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a772e-129">Tutti i GPO in cui <strong> </strong> è incluso il firewall di Word nel commento più recente e in cui la parola <strong> sicurezza </strong> viene visualizzata in qualsiasi colonna.</span><span class="sxs-lookup"><span data-stu-id="a772e-129">All GPOs in which the word <strong>firewall</strong> is included in the most recent comment and in which the word <strong>security</strong> appears in any column.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a772e-130">Commento: </strong><strong> </strong><strong> sicurezza firewall</span><span class="sxs-lookup"><span data-stu-id="a772e-130">comment:</strong><strong>firewall</strong><strong>security</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a772e-131">Tutti i GPO che hanno lo stato di <strong> tutte le impostazioni disabilitate </strong> .</span><span class="sxs-lookup"><span data-stu-id="a772e-131">All GPOs that have a status of <strong>All Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a772e-132">stato GPO: </strong><strong> tutto</span><span class="sxs-lookup"><span data-stu-id="a772e-132">gpo status:</strong><strong>all</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a772e-133">Tutti i GPO a cui è applicato un filtro WMI denominato <strong> filtro WMI </strong> e che hanno lo stato delle <strong> impostazioni di configurazione utente disabilitate </strong> .</span><span class="sxs-lookup"><span data-stu-id="a772e-133">All GPOs that have a WMI filter named <strong>My WMI Filter</strong> applied and that have a status of <strong>User Configuration Settings Disabled</strong>.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="a772e-134">filtro WMI: </strong> &quot; <strong> </strong> &quot; <strong> stato GPO filtro WMI: </strong><strong> utente</span><span class="sxs-lookup"><span data-stu-id="a772e-134">wmi filter:</strong>&quot;<strong>My WMI Filter</strong>&quot;<strong>gpo status:</strong><strong>user</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a772e-135">Specifica delle date</span><span class="sxs-lookup"><span data-stu-id="a772e-135">Specifying dates</span></span>


<span data-ttu-id="a772e-136">È possibile cercare i GPO modificati in una data specifica, in un momento specifico o durante un periodo di tempo usando gli stessi termini speciali disponibili durante la ricerca in Windows.</span><span class="sxs-lookup"><span data-stu-id="a772e-136">You can search for GPOs changed on a specific date, at a specific time, or during a span of time by using the same special terms available when you search in Windows.</span></span> <span data-ttu-id="a772e-137">Se si immette una data o un'ora specifica, è necessario usare il formato usato nella colonna **Cambia data** .</span><span class="sxs-lookup"><span data-stu-id="a772e-137">If entering a specific date or time, you must use the format that is used in the **Change Date** column.</span></span> <span data-ttu-id="a772e-138">Di seguito sono riportati alcuni esempi di ricerche della colonna **Cambia data** :</span><span class="sxs-lookup"><span data-stu-id="a772e-138">The following are examples of searches of the **Change Date** column:</span></span>

-   <span data-ttu-id="a772e-139">**modifica data:\*\*\*\*10/10/2009**</span><span class="sxs-lookup"><span data-stu-id="a772e-139">**change date:\*\*\*\*10/10/2009**</span></span>

-   <span data-ttu-id="a772e-140">**modifica data:\*\*\*\*10/10/2009 9:00:00 AM**</span><span class="sxs-lookup"><span data-stu-id="a772e-140">**change date:\*\*\*\*10/10/2009 9:00:00 AM**</span></span>

-   <span data-ttu-id="a772e-141">**modifica data:\*\*\*\*ThisWeek**</span><span class="sxs-lookup"><span data-stu-id="a772e-141">**change date:\*\*\*\*thisweek**</span></span>

<span data-ttu-id="a772e-142">Quando si esegue una ricerca nella colonna **modifica data** , è possibile usare i termini speciali seguenti, che non fanno distinzione tra maiuscole e minuscole:</span><span class="sxs-lookup"><span data-stu-id="a772e-142">You can use the following special terms, which are not case-sensitive, when you search the **Change Date** column:</span></span>

-   **<span data-ttu-id="a772e-143">Today</span><span class="sxs-lookup"><span data-stu-id="a772e-143">Today</span></span>**

-   **<span data-ttu-id="a772e-144">Ieri</span><span class="sxs-lookup"><span data-stu-id="a772e-144">Yesterday</span></span>**

-   **<span data-ttu-id="a772e-145">ThisWeek</span><span class="sxs-lookup"><span data-stu-id="a772e-145">ThisWeek</span></span>**

-   **<span data-ttu-id="a772e-146">LastWeek</span><span class="sxs-lookup"><span data-stu-id="a772e-146">LastWeek</span></span>**

-   **<span data-ttu-id="a772e-147">ThisMonth</span><span class="sxs-lookup"><span data-stu-id="a772e-147">ThisMonth</span></span>**

-   **<span data-ttu-id="a772e-148">LastMonth</span><span class="sxs-lookup"><span data-stu-id="a772e-148">LastMonth</span></span>**

-   **<span data-ttu-id="a772e-149">TwoMonths</span><span class="sxs-lookup"><span data-stu-id="a772e-149">TwoMonths</span></span>**

-   **<span data-ttu-id="a772e-150">ThreeMonths</span><span class="sxs-lookup"><span data-stu-id="a772e-150">ThreeMonths</span></span>**

-   **<span data-ttu-id="a772e-151">ThisYear</span><span class="sxs-lookup"><span data-stu-id="a772e-151">ThisYear</span></span>**

-   **<span data-ttu-id="a772e-152">LastYear</span><span class="sxs-lookup"><span data-stu-id="a772e-152">LastYear</span></span>**

### <span data-ttu-id="a772e-153">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a772e-153">Additional considerations</span></span>

-   <span data-ttu-id="a772e-154">Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="a772e-154">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="a772e-155">In particolare, devi avere l'autorizzazione **contenuto elenco** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="a772e-155">Specifically, you must have **List Contents** permission for the domain.</span></span>

-   <span data-ttu-id="a772e-156">Per altre informazioni sugli attributi degli oggetti Criteri di ricerca, vedere [caratteristiche della scheda Sommario](contents-tab-features-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="a772e-156">For more information about GPO attributes, see [Contents Tab Features](contents-tab-features-agpm40.md).</span></span>

### <span data-ttu-id="a772e-157">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="a772e-157">Additional references</span></span>

-   [<span data-ttu-id="a772e-158">Gestione avanzata Criteri di gruppo 4.0</span><span class="sxs-lookup"><span data-stu-id="a772e-158">Advanced Group Policy Management 4.0</span></span>](advanced-group-policy-management-40.md)

 

 





