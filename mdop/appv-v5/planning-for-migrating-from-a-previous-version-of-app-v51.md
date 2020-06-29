---
title: Pianificazione per la migrazione da una versione precedente di App-V
description: Pianificazione per la migrazione da una versione precedente di App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805001"
---
# <span data-ttu-id="57670-103">Pianificazione per la migrazione da una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="57670-103">Planning for Migrating from a Previous Version of App-V</span></span>


<span data-ttu-id="57670-104">Usare le informazioni seguenti per pianificare come eseguire la migrazione a Microsoft Application Virtualization (App-V) 5,1 dalle versioni precedenti di App-V.</span><span class="sxs-lookup"><span data-stu-id="57670-104">Use the following information to plan how to migrate to Microsoft Application Virtualization (App-V) 5.1 from previous versions of App-V.</span></span>

## <span data-ttu-id="57670-105">Requisiti di migrazione</span><span class="sxs-lookup"><span data-stu-id="57670-105">Migration requirements</span></span>


<span data-ttu-id="57670-106">Prima di iniziare gli aggiornamenti, esaminare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="57670-106">Before you start any upgrades, review the following requirements:</span></span>

-   <span data-ttu-id="57670-107">Se si esegue l'aggiornamento da una versione precedente a App-V 4,6 SP2, eseguire l'aggiornamento alla versione App-V 4,6 SP3 prima di eseguire l'aggiornamento a App-V 5,1 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57670-107">If you are upgrading from a version earlier than App-V 4.6 SP2, upgrade to version App-V 4.6 SP3 first before upgrading to App-V 5.1 or later.</span></span> <span data-ttu-id="57670-108">In questo scenario aggiornare innanzitutto i client App-V e quindi aggiornare i componenti del server.</span><span class="sxs-lookup"><span data-stu-id="57670-108">In this scenario, upgrade the App-V clients first, and then upgrade the server components.</span></span>
<span data-ttu-id="57670-109">**Nota:** App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="57670-109">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

-   <span data-ttu-id="57670-110">App-V 5,1 supporta solo i pacchetti creati con App-V 5,0 o App-V 5,1 o i pacchetti che sono stati convertiti nel formato **appv** .</span><span class="sxs-lookup"><span data-stu-id="57670-110">App-V 5.1 supports only packages that are created using App-V 5.0 or App-V 5.1, or packages that have been converted to the **.appv** format.</span></span>

-   <span data-ttu-id="57670-111">Se si sta aggiornando l'App-V Server da App-V 5,0 SP1, vedere [informazioni su App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) per istruzioni.</span><span class="sxs-lookup"><span data-stu-id="57670-111">If you are upgrading the App-V Server from App-V 5.0 SP1, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51) for instructions.</span></span>

## <span data-ttu-id="57670-112">Eseguire il client App-V 5,1 in concomitanza con l'App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="57670-112">Running the App-V 5.1 client concurrently with App-V 4.6</span></span>


<span data-ttu-id="57670-113">Puoi eseguire il client App-V 5,1 contemporaneamente nello stesso computer con il client App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="57670-113">You can run the App-V 5.1 client concurrently on the same computer with the App-V4.6SP3 client.</span></span>

<span data-ttu-id="57670-114">Quando si eseguono i client App-V coesistenti, è possibile:</span><span class="sxs-lookup"><span data-stu-id="57670-114">When you run coexisting App-V clients, you can:</span></span>

-   <span data-ttu-id="57670-115">Convertire un pacchetto App-V 4,6 SP3 nel formato App-V 5,1 e pubblicare entrambi i pacchetti, quando sono in uso entrambi i client.</span><span class="sxs-lookup"><span data-stu-id="57670-115">Convert an App-V 4.6 SP3 package to the App-V 5.1 format and publish both packages, when you have both clients running.</span></span>

-   <span data-ttu-id="57670-116">Definire i criteri di migrazione per il pacchetto convertito, che consente al pacchetto convertito App-V 5,1 di assumere le associazioni di tipi di file e le scelte rapide dal pacchetto App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="57670-116">Define the migration policy for the converted package, which allows the converted App-V 5.1 package to assume the file type associations and shortcuts from the App-V 4.6 package.</span></span>

### <span data-ttu-id="57670-117">Scenari di coesistenza supportati</span><span class="sxs-lookup"><span data-stu-id="57670-117">Supported coexistence scenarios</span></span>

<span data-ttu-id="57670-118">La tabella seguente Mostra gli scenari di coesistenza di App-V supportati.</span><span class="sxs-lookup"><span data-stu-id="57670-118">The following table shows the supported App-V coexistence scenarios.</span></span> <span data-ttu-id="57670-119">È consigliabile installare gli aggiornamenti disponibili più recenti di una determinata versione quando si esegue client coesistenti.</span><span class="sxs-lookup"><span data-stu-id="57670-119">We recommend that you install the latest available updates of a given release when you are running coexisting clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57670-120">Tipo di client App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="57670-120">App-V 4.6 client type</span></span></th>
<th align="left"><span data-ttu-id="57670-121">Tipo di client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="57670-121">App-V 5.1 client type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57670-122">App-V 4,6 SP3</span><span class="sxs-lookup"><span data-stu-id="57670-122">App-V 4.6 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="57670-123">App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="57670-123">App-V 5.1</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57670-124">App-V 4,6 SP3 RDS</span><span class="sxs-lookup"><span data-stu-id="57670-124">App-V 4.6 SP3 RDS</span></span></p></td>
<td align="left"><p><span data-ttu-id="57670-125">App-V 5,1 RDS</span><span class="sxs-lookup"><span data-stu-id="57670-125">App-V 5.1 RDS</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="57670-126">Requisiti per l'uso di client coesistenti</span><span class="sxs-lookup"><span data-stu-id="57670-126">Requirements for running coexisting clients</span></span>

<span data-ttu-id="57670-127">Per eseguire i client coesistenti, è necessario:</span><span class="sxs-lookup"><span data-stu-id="57670-127">To run coexisting clients, you must:</span></span>

-   <span data-ttu-id="57670-128">Installare il client App-V 4.6 prima di installare il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57670-128">Install the App-V4.6 client before you install the App-V 5.1 client.</span></span>

-   <span data-ttu-id="57670-129">Abilitare l'impostazione attiva criteri di gruppo **modalità di migrazione** , che si trova nel nodo di coesistenza client **App-V** &gt; **Client Coexistence** .</span><span class="sxs-lookup"><span data-stu-id="57670-129">Enable the **Enable Migration Mode** Group Policy setting, which is in the **App-V** &gt; **Client Coexistence** node.</span></span> <span data-ttu-id="57670-130">Per distribuire il modello con estensione ADMX, vedere [come scaricare e distribuire i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="57670-130">To deploy the .admx template, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

<span data-ttu-id="57670-131">**Nota**  I pacchetti App-V 5,1 possono essere eseguiti affiancati con i pacchetti App-V 4,6 Se si hanno installazioni coesistenti di App-V 5,1 e 4,6.</span><span class="sxs-lookup"><span data-stu-id="57670-131">**Note** App-V 5.1 packages can run side by side with App-V 4.6 packages if you have coexisting installations of App-V 5.1 and 4.6.</span></span> <span data-ttu-id="57670-132">Tuttavia, i pacchetti App-V 5,1 non possono interagire con i pacchetti App-V 4,6 nello stesso ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="57670-132">However, App-V 5.1 packages cannot interact with App-V 4.6 packages in the same virtual environment.</span></span>

 

### <span data-ttu-id="57670-133">Download e documentazione client</span><span class="sxs-lookup"><span data-stu-id="57670-133">Client downloads and documentation</span></span>

<span data-ttu-id="57670-134">La tabella seguente fornisce collegamenti ai download client App-V 4,6 e alla documentazione di TechNet sulle versioni.</span><span class="sxs-lookup"><span data-stu-id="57670-134">The following table provides links to the App-V 4.6 client downloads and to the TechNet documentation about the releases.</span></span> <span data-ttu-id="57670-135">I download includono i client App-V "regolari" e RDS.</span><span class="sxs-lookup"><span data-stu-id="57670-135">The downloads include the App-V “regular” and RDS clients.</span></span> <span data-ttu-id="57670-136">La documentazione di TechNet relativa al client App-V si applica a entrambi i client, se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="57670-136">The TechNet documentation about the App-V client applies to both clients, unless stated otherwise.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57670-137">Versione App-V</span><span class="sxs-lookup"><span data-stu-id="57670-137">App-V version</span></span></th>
<th align="left"><span data-ttu-id="57670-138">Collegamento alla documentazione di TechNet</span><span class="sxs-lookup"><span data-stu-id="57670-138">Link to TechNet documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57670-139">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="57670-139">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)"><span data-ttu-id="57670-140">Informazioni su Microsoft Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="57670-140">About Microsoft Application Virtualization 4.6 SP3</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57670-141">App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="57670-141">App-V 4.6SP3</span></span></p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)"><span data-ttu-id="57670-142">Informazioni su Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="57670-142">About Microsoft Application Virtualization 5.1</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="57670-143">Per altre informazioni su come configurare la coesistenza client di App-V 5,1, vedere:</span><span class="sxs-lookup"><span data-stu-id="57670-143">For more information about how to configure App-V 5.1 client coexistence, see:</span></span>

-   [<span data-ttu-id="57670-144">Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="57670-144">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [<span data-ttu-id="57670-145">App-V 5,0 coesistenza e migrazione</span><span class="sxs-lookup"><span data-stu-id="57670-145">App-V 5.0 Coexistence and Migration</span></span>](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a><span data-ttu-id="57670-146">Conversione dei pacchetti "versione precedente" tramite il convertitore di pacchetti</span><span class="sxs-lookup"><span data-stu-id="57670-146">Converting “previous-version” packages using the package converter</span></span>


<span data-ttu-id="57670-147">Prima di eseguire la migrazione di un pacchetto, creato con app-4.6 SP2 o versioni precedenti, in App-V 5,1, esaminare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="57670-147">Before migrating a package, created using App-4.6SP2 or earlier, to App-V 5.1, review the following requirements:</span></span>

-   <span data-ttu-id="57670-148">Devi convertire il pacchetto nel formato di file con **estensione appv** .</span><span class="sxs-lookup"><span data-stu-id="57670-148">You must convert the package to the **.appv** file format.</span></span>

-   <span data-ttu-id="57670-149">Il convertitore di pacchetti supporta solo la conversione diretta dei pacchetti creati usando App-V 4,5 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57670-149">The Package Converter supports only the direct conversion of packages that were created by using App-V 4.5 and later.</span></span> <span data-ttu-id="57670-150">Per usare il convertitore di pacchetti in un pacchetto creato con una versione precedente, devi usare un'app-V 4.5 o una versione successiva del sequencer per aggiornare il pacchetto, quindi puoi eseguire la conversione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="57670-150">To use the package converter on a package that was created using a previous version, you must use an App-V4.5 or later version of the sequencer to upgrade the package, and then you can perform the package conversion.</span></span>

<span data-ttu-id="57670-151">Per altre informazioni sull'uso del convertitore di pacchetti per convertire un pacchetto, vedere [come convertire un pacchetto creato in una versione precedente di App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="57670-151">For more information about using the package converter to convert a package, see [How to Convert a Package Created in a Previous Version of App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md).</span></span> <span data-ttu-id="57670-152">Dopo aver convertito il file, è possibile distribuirlo in computer di destinazione che eseguono il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57670-152">After you convert the file, you can deploy it to target computers that run the App-V 5.1 client.</span></span>






## <span data-ttu-id="57670-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57670-153">Related topics</span></span>


[<span data-ttu-id="57670-154">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="57670-154">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





