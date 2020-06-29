---
title: Riferimento della riga di comando dell'installazione client
description: Riferimento della riga di comando dell'installazione client
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826726"
---
# <span data-ttu-id="87e01-103">Riferimento della riga di comando dell'installazione client</span><span class="sxs-lookup"><span data-stu-id="87e01-103">Client Installation Command Line Reference</span></span>


**<span data-ttu-id="87e01-104">Per installare MED-V dalla riga di comando</span><span class="sxs-lookup"><span data-stu-id="87e01-104">To install MED-V from the command line</span></span>**

1.  <span data-ttu-id="87e01-105">Dalla riga di comando eseguire il pacchetto MED-V. msi seguito da uno dei parametri facoltativi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="87e01-105">From the command line, run the MED-V .msi package followed by any of the optional parameters described in the following table.</span></span>

2.  <span data-ttu-id="87e01-106">Il pacchetto MED-V. msi si chiama *MED-V\_x.msi*, dove *x* corrisponde al numero di versione.</span><span class="sxs-lookup"><span data-stu-id="87e01-106">The MED-V .msi package is called *MED-V\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="87e01-107">Ad esempio, *MED-V\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="87e01-107">For example, *MED-V\_1.0.65.msi*.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="87e01-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="87e01-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="87e01-109">Valore</span><span class="sxs-lookup"><span data-stu-id="87e01-109">Value</span></span></th>
<th align="left"><span data-ttu-id="87e01-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87e01-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87e01-111">/quiet</span><span class="sxs-lookup"><span data-stu-id="87e01-111">/quiet</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="87e01-112">Installazione invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="87e01-112">Silent installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87e01-113">&lt;percorso completo di/log per il file di log&gt;</span><span class="sxs-lookup"><span data-stu-id="87e01-113">/log &lt;full path to log file&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="87e01-114">Percorso completo del file di log.</span><span class="sxs-lookup"><span data-stu-id="87e01-114">The full path to the log file.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87e01-115">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="87e01-115">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="87e01-116">Percorso completo della directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="87e01-116">The full path to the installation directory.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87e01-117">VMSFOLDER</span><span class="sxs-lookup"><span data-stu-id="87e01-117">VMSFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="87e01-118">Percorso completo della cartella della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="87e01-118">The full path to the virtual machine folder.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87e01-119">INSTALL_ADMIN_TOOLS</span><span class="sxs-lookup"><span data-stu-id="87e01-119">INSTALL_ADMIN_TOOLS</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="87e01-120">1,0</span><span class="sxs-lookup"><span data-stu-id="87e01-120">1,0</span></span></strong></p>
<p><span data-ttu-id="87e01-121">Impostazione predefinita: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="87e01-121">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87e01-122">Installa gli strumenti di amministrazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="87e01-122">Installs MED-V administration tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87e01-123">START_AUTOMATICALLY</span><span class="sxs-lookup"><span data-stu-id="87e01-123">START_AUTOMATICALLY</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="87e01-124">1,0</span><span class="sxs-lookup"><span data-stu-id="87e01-124">1,0</span></span></strong></p>
<p><span data-ttu-id="87e01-125">Impostazione predefinita: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="87e01-125">Default: <strong>0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87e01-126">Avvia automaticamente il client MED-V ogni volta che l'utente accede a Windows.</span><span class="sxs-lookup"><span data-stu-id="87e01-126">Automatically starts MED-V client every time the user logs on to Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87e01-127">SERVER_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="87e01-127">SERVER_ADDRESS</span></span></p></td>
<td align="left"><p><span data-ttu-id="87e01-128">nome host o IP</span><span class="sxs-lookup"><span data-stu-id="87e01-128">host name or IP</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87e01-129">SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="87e01-129">SERVER_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="87e01-130">porta</span><span class="sxs-lookup"><span data-stu-id="87e01-130">port</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87e01-131">SERVER_SSL</span><span class="sxs-lookup"><span data-stu-id="87e01-131">SERVER_SSL</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="87e01-132">1,0</span><span class="sxs-lookup"><span data-stu-id="87e01-132">1,0</span></span></strong></p>
<p><span data-ttu-id="87e01-133">per <strong> https </strong> o <strong> http</span><span class="sxs-lookup"><span data-stu-id="87e01-133">for <strong>https</strong> or <strong>http</span></span></strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87e01-134">START_MEDV</span><span class="sxs-lookup"><span data-stu-id="87e01-134">START_MEDV</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="87e01-135">1,0</span><span class="sxs-lookup"><span data-stu-id="87e01-135">1,0</span></span></strong></p>
<p><span data-ttu-id="87e01-136">Impostazione predefinita: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="87e01-136">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87e01-137">Avvia MED-V al completamento dell'installazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="87e01-137">Starts MED-V at the completion of the MED-V installation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="87e01-138">Nota</span><span class="sxs-lookup"><span data-stu-id="87e01-138">Note</span></span></strong><br/><p><span data-ttu-id="87e01-139">È consigliabile impostare START_MEDV = 0 nel caso in cui MED-V sia installato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="87e01-139">It is recommended to set START_MEDV=0 in case MED-V is installed by the system.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87e01-140">DESKTOP_SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="87e01-140">DESKTOP_SHORTCUT</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="87e01-141">1,0</span><span class="sxs-lookup"><span data-stu-id="87e01-141">1,0</span></span></strong></p>
<p><span data-ttu-id="87e01-142">Impostazione predefinita: <strong> 1</span><span class="sxs-lookup"><span data-stu-id="87e01-142">Default: <strong>1</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87e01-143">Crea un collegamento sul desktop, che avvia il client MED-V.</span><span class="sxs-lookup"><span data-stu-id="87e01-143">Creates a shortcut on the desktop, which starts MED-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="87e01-144">MINIMAL_RAM_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="87e01-144">MINIMAL_RAM_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="87e01-145">RAM in MB</span><span class="sxs-lookup"><span data-stu-id="87e01-145">RAM in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="87e01-146">Durante l'installazione di MED-V, controlla se il computer ha la quantità minima di RAM specificata.</span><span class="sxs-lookup"><span data-stu-id="87e01-146">When installing MED-V, checks whether the computer has the minimum amount of RAM specified.</span></span> <span data-ttu-id="87e01-147">In caso contrario, l'installazione viene interrotta.</span><span class="sxs-lookup"><span data-stu-id="87e01-147">If not, installation is aborted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="87e01-148">SKIP_OS_CHECK</span><span class="sxs-lookup"><span data-stu-id="87e01-148">SKIP_OS_CHECK</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="87e01-149">1,0</span><span class="sxs-lookup"><span data-stu-id="87e01-149">1,0</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="87e01-150">Omette la convalida del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="87e01-150">Omits the operating system validation.</span></span></p></td>
</tr>
</tbody>
</table>











