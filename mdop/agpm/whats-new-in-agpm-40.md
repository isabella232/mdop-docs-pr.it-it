---
title: Novità di Gestione avanzata Criteri di gruppo 4.0
description: Novità di Gestione avanzata Criteri di gruppo 4.0
author: dansimp
ms.assetid: 31775f7f-a59c-4e64-a875-0adc9f5bc835
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 82b4445a7d22fb7c1ef4f42d896f11908a22f2f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820105"
---
# <span data-ttu-id="cbda4-103">Novità di Gestione avanzata Criteri di gruppo 4.0</span><span class="sxs-lookup"><span data-stu-id="cbda4-103">What's New in AGPM 4.0</span></span>


<span data-ttu-id="cbda4-104">Gestione avanzata Criteri di gruppo di Microsoft (Advanced Group Policy Management) 4.0 include nuove funzionalità che consentono di cercare oggetti Criteri di gruppo, filtrare l'elenco dei GPO visualizzati, esportare e importare un GPO in un'altra foresta e installare Advanced Group Policy Manager nei computer che eseguono Windows7 e Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="cbda4-104">Microsoft Advanced Group Policy Management (AGPM)4.0 includes new features that let you search for Group Policy Objects (GPOs), filter the list of GPOs displayed, export and import a GPO to a different forest, and install AGPM on computers running Windows7 and Windows Server2008R2.</span></span>

## <span data-ttu-id="cbda4-105">Cercare e filtrare gli oggetti Criteri di ricerca</span><span class="sxs-lookup"><span data-stu-id="cbda4-105">Search and filter GPOs</span></span>


<span data-ttu-id="cbda4-106">In Advanced Group Policy Management 4,0 è possibile eseguire una ricerca nell'elenco di GPO per individuare attributi specifici per filtrare l'elenco dei GPO visualizzati.</span><span class="sxs-lookup"><span data-stu-id="cbda4-106">In AGPM 4.0, you can search the list of GPOs for specific attributes to filter the list of GPOs displayed.</span></span> <span data-ttu-id="cbda4-107">Ad esempio, puoi cercare gli oggetti Criteri di ricerca con un nome, uno stato o un commento specifico.</span><span class="sxs-lookup"><span data-stu-id="cbda4-107">For example, you can search for GPOs with a particular name, state, or comment.</span></span> <span data-ttu-id="cbda4-108">È anche possibile cercare gli oggetti Criteri di gruppo modificati per l'ultima volta da un determinato amministratore dei criteri di raggruppamento o in una data specifica.</span><span class="sxs-lookup"><span data-stu-id="cbda4-108">You can also search for GPOs that were last changed by a particular Group Policy administrator or on a particular date.</span></span>

<span data-ttu-id="cbda4-109">Puoi creare una stringa di ricerca complessa usando il formato *attributo GPO 1: ricerca testo 1 attributo GPO 2: ricerca testo 2...*, dove un attributo GPO è qualsiasi intestazione di colonna nell'elenco di GPO in Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="cbda4-109">You can create a complex search string by using the format *GPO attribute 1: search text 1 GPO attribute 2: search text 2…*, where a GPO attribute is any column heading in the list of GPOs in AGPM.</span></span> <span data-ttu-id="cbda4-110">Ad esempio, per cercare tutti i GPO con nomi che includono il testo "MioGPO" che sono stati archiviati e modificati per l'ultima volta dall'utente Editor03, digitare quanto segue nella casella di ricerca: **Nome: MioGPO stato:\*\*\*\*archiviato\*\*\*\*modificato da: Editor03**.</span><span class="sxs-lookup"><span data-stu-id="cbda4-110">For example, to search for all GPOs with names including the text "MyGPO" that are checked in and were last changed by the user Editor03, you would type the following in the Search box: **name: MyGPO state:\*\*\*\*checked in\*\*\*\*changed by: Editor03**.</span></span> <span data-ttu-id="cbda4-111">La ricerca restituisce le corrispondenze parziali in modo che sia possibile immettere parte di un nome di oggetto o di un nome utente e visualizzare un elenco di tutti i GPO che includono il testo nel nome.</span><span class="sxs-lookup"><span data-stu-id="cbda4-111">The search returns partial matches so that you can enter part of a GPO name or user name and view a list of all GPOs that include that text in their name.</span></span>

<span data-ttu-id="cbda4-112">Inoltre, puoi usare gli stessi termini speciali disponibili durante la ricerca in Windows per cercare gli oggetti Criteri di ricerca modificati in una data o un intervallo di date specifico.</span><span class="sxs-lookup"><span data-stu-id="cbda4-112">Additionally, you can use the same special terms available when you search in Windows to search for GPOs changed on a specific date or range of dates.</span></span> <span data-ttu-id="cbda4-113">Ad esempio, **Cambia Data:\*\*\*\*lastmonth** o **modifica data:\*\*\*\*ThisWeek**.</span><span class="sxs-lookup"><span data-stu-id="cbda4-113">For example, **change date:\*\*\*\*lastmonth** or **change date:\*\*\*\*thisweek**.</span></span>

## <span data-ttu-id="cbda4-114">Esportare e importare GPO in foreste diverse</span><span class="sxs-lookup"><span data-stu-id="cbda4-114">Export and import GPOs to different forests</span></span>


<span data-ttu-id="cbda4-115">Usando Advanced Group Policy Management 4,0, è possibile copiare un oggetto Criteri di campo controllato da un dominio in una foresta in un dominio in una seconda foresta.</span><span class="sxs-lookup"><span data-stu-id="cbda4-115">Using AGPM 4.0, you can copy a controlled GPO from a domain in one forest to a domain in a second forest.</span></span> <span data-ttu-id="cbda4-116">Ad esempio, è possibile esportare un oggetto Criteri di stato da un dominio in una foresta in un file CAB tramite Advanced Group Policy Management, copiare il file CAB in un'unità USB, collegare l'unità USB a un computer di un dominio in una seconda foresta e importare l'oggetto Criteri di ricerca in Advanced Group Policy in un dominio della seconda foresta.</span><span class="sxs-lookup"><span data-stu-id="cbda4-116">For example, you can export a GPO from a domain in one forest to a CAB file by using AGPM, copy that CAB file to a USB drive, plug the USB drive into a computer in a domain in a second forest, and import the GPO into AGPM in a domain in the second forest.</span></span> <span data-ttu-id="cbda4-117">Puoi importare l'oggetto Criteri di controllo come nuovo GPO controllato oppure importarlo per sostituire le impostazioni di un oggetto Criteri di controllo esistente Estratto.</span><span class="sxs-lookup"><span data-stu-id="cbda4-117">You can either import the GPO as a new controlled GPO, or import it to replace the settings of an existing GPO that is checked out.</span></span>

## <span data-ttu-id="cbda4-118">Supporto per Windows Server 2008 R2 e Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbda4-118">Support for Windows Server 2008 R2 and Windows 7</span></span>


<span data-ttu-id="cbda4-119">Advanced Group Policy Management 4,0 supporta Windows Server2008R2 e Windows7, ma supporta ancora Windows Server2008 e WindowsVista® con Service Pack1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cbda4-119">AGPM 4.0 supports Windows Server2008R2 and Windows7, yet still supports Windows Server2008 and WindowsVista® with Service Pack1 (SP1).</span></span> <span data-ttu-id="cbda4-120">Esistono tuttavia limitazioni in un ambiente misto che include sia i sistemi operativi più recenti che quelli più vecchi, come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="cbda4-120">However, there are limitations in a mixed environment that includes both the newer and older operating systems, as indicated in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cbda4-121">Sistema operativo in cui viene eseguito Advanced Server Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="cbda4-121">Operating system on which AGPM Server 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="cbda4-122">Sistema operativo in cui viene eseguito il client Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="cbda4-122">Operating system on which AGPM Client 4.0 runs</span></span></th>
<th align="left"><span data-ttu-id="cbda4-123">Stato del supporto per Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="cbda4-123">Status of AGPM 4.0 support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbda4-124">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="cbda4-124">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-125">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="cbda4-125">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-126">Supportato</span><span class="sxs-lookup"><span data-stu-id="cbda4-126">Supported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbda4-127">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="cbda4-127">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-128">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="cbda4-128">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-129">Supportato, ma non è possibile modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="cbda4-129">Supported, but cannot edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cbda4-130">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="cbda4-130">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-131">Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="cbda4-131">Windows Server2008R2 or Windows7</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-132">File modifiche disco non supportato</span><span class="sxs-lookup"><span data-stu-id="cbda4-132">Unsupported</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cbda4-133">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="cbda4-133">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-134">Windows Server2008 o Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="cbda4-134">Windows Server2008 or Windows Vista with SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="cbda4-135">Supportato, ma non può segnalare o modificare le impostazioni dei criteri o gli elementi delle preferenze esistenti solo in Windows Server2008R2 o Windows7</span><span class="sxs-lookup"><span data-stu-id="cbda4-135">Supported, but cannot report or edit policy settings or preference items that exist only in Windows Server2008R2 or Windows7</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 





