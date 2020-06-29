---
title: Migrazione da una versione precedente
description: Migrazione da una versione precedente
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805067"
---
# <span data-ttu-id="947d9-103">Migrazione da una versione precedente</span><span class="sxs-lookup"><span data-stu-id="947d9-103">Migrating from a Previous Version</span></span>


<span data-ttu-id="947d9-104">Con App-V 5,0 puoi eseguire la migrazione dell'infrastruttura App-V 4,6 esistente a quella più flessibile, integrata e più facile da gestire dell'infrastruttura App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="947d9-104">With App-V 5.0 you can migrate your existing App-V 4.6 infrastructure to the more flexible, integrated, and easier to manage App-V 5.0 infrastructure.</span></span>

<span data-ttu-id="947d9-105">Quando si pianifica la strategia di migrazione, prendere in considerazione le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="947d9-105">Consider the following sections when you plan your migration strategy:</span></span>

<span data-ttu-id="947d9-106">**Nota**  Per altre informazioni sulle differenze tra App-V 4,6 e App-V 5,0, Vedi le **differenze tra la sezione App-v 4,6 e App-v 5,0** di [About app-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="947d9-106">**Note** For more information about the differences between App-V 4.6 and App-V 5.0, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <span data-ttu-id="947d9-107">Conversione di pacchetti creati con una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="947d9-107">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="947d9-108">Usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni precedenti di App-V.</span><span class="sxs-lookup"><span data-stu-id="947d9-108">Use the package converter utility to upgrade virtual application packages created using previous versions of App-V.</span></span> <span data-ttu-id="947d9-109">Il convertitore di pacchetti usa PowerShell per convertire i pacchetti e può aiutare a automatizzare il processo se sono presenti molti pacchetti che richiedono la conversione.</span><span class="sxs-lookup"><span data-stu-id="947d9-109">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="947d9-110">**Importante**  Dopo aver convertito un pacchetto esistente, è consigliabile testare il pacchetto prima di distribuire il pacchetto per verificare che il processo di conversione abbia avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="947d9-110">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="947d9-111">Informazioni utili prima di convertire i pacchetti esistenti</span><span class="sxs-lookup"><span data-stu-id="947d9-111">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="947d9-112">Problema</span><span class="sxs-lookup"><span data-stu-id="947d9-112">Issue</span></span></th>
<th align="left"><span data-ttu-id="947d9-113">Soluzione alternativa</span><span class="sxs-lookup"><span data-stu-id="947d9-113">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="947d9-114">Gli script di pacchetto non vengono convertiti.</span><span class="sxs-lookup"><span data-stu-id="947d9-114">Package scripts are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="947d9-115">Testare il pacchetto convertito.</span><span class="sxs-lookup"><span data-stu-id="947d9-115">Test the converted package.</span></span> <span data-ttu-id="947d9-116">Se necessario, convertire lo script.</span><span class="sxs-lookup"><span data-stu-id="947d9-116">If necessary convert the script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="947d9-117">Le override dell'impostazione del registro di sistema non vengono convertite.</span><span class="sxs-lookup"><span data-stu-id="947d9-117">Package registry setting overrides are not converted.</span></span></p></td>
<td align="left"><p><span data-ttu-id="947d9-118">Testare il pacchetto convertito.</span><span class="sxs-lookup"><span data-stu-id="947d9-118">Test the converted package.</span></span> <span data-ttu-id="947d9-119">Se necessario, aggiungere di nuovo gli override del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="947d9-119">If necessary, re-add registry overrides.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="947d9-120">I pacchetti virtuali che usano DSC non sono collegati dopo la conversione.</span><span class="sxs-lookup"><span data-stu-id="947d9-120">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="947d9-121">Collegare i pacchetti usando i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="947d9-121">Link the packages using connection groups.</span></span> <span data-ttu-id="947d9-122">Vedere <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> gestione dei gruppi di connessioni </a> .</span><span class="sxs-lookup"><span data-stu-id="947d9-122">See <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="947d9-123">I conflitti di variabili di ambiente vengono rilevati durante la conversione.</span><span class="sxs-lookup"><span data-stu-id="947d9-123">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="947d9-124">Risolvere i conflitti nel <strong> file OSD associato </strong> .</span><span class="sxs-lookup"><span data-stu-id="947d9-124">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="947d9-125">I percorsi hardcoded vengono rilevati durante la conversione.</span><span class="sxs-lookup"><span data-stu-id="947d9-125">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="947d9-126">I percorsi hardcoded sono difficili da convertire correttamente.</span><span class="sxs-lookup"><span data-stu-id="947d9-126">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="947d9-127">Il convertitore di pacchetti rileverà e restituirà pacchetti con file che contengono percorsi hardcoded.</span><span class="sxs-lookup"><span data-stu-id="947d9-127">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="947d9-128">Visualizzare il file con il percorso hardcoded e determinare se il pacchetto richiede il file.</span><span class="sxs-lookup"><span data-stu-id="947d9-128">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="947d9-129">In questo caso, è consigliabile ripetere la sequenza del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="947d9-129">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="947d9-130">Quando si converte un pacchetto, verificare la mancanza di file o tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="947d9-130">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="947d9-131">Individuare l'elemento nel pacchetto App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="947d9-131">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="947d9-132">Potrebbe essere un percorso hardcoded.</span><span class="sxs-lookup"><span data-stu-id="947d9-132">It could possibly be hard-coded path.</span></span> <span data-ttu-id="947d9-133">Convertire il percorso.</span><span class="sxs-lookup"><span data-stu-id="947d9-133">Convert the path.</span></span>

<span data-ttu-id="947d9-134">**Nota**  È consigliabile usare il sequencer App-V 5,0 per la conversione di applicazioni o applicazioni critiche che devono sfruttare le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="947d9-134">**Note** It is recommended that you use the App-V 5.0 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="947d9-135">Vedere [come sequenziare una nuova applicazione con App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="947d9-135">See, [How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).</span></span>

<span data-ttu-id="947d9-136">Se un pacchetto convertito non si apre dopo averlo convertito, è anche consigliabile ripetere la sequenza dell'applicazione usando il sequencer App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="947d9-136">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.0 sequencer.</span></span>

 

[<span data-ttu-id="947d9-137">Come convertire un pacchetto creato in una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="947d9-137">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## <span data-ttu-id="947d9-138">Migrazione dei client</span><span class="sxs-lookup"><span data-stu-id="947d9-138">Migrating Clients</span></span>


<span data-ttu-id="947d9-139">Nella tabella seguente viene visualizzato il metodo consigliato per l'aggiornamento dei client.</span><span class="sxs-lookup"><span data-stu-id="947d9-139">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="947d9-140">Attività</span><span class="sxs-lookup"><span data-stu-id="947d9-140">Task</span></span></th>
<th align="left"><span data-ttu-id="947d9-141">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="947d9-141">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="947d9-142">Aggiornare l'ambiente a App-V 4.6 SP2</span><span class="sxs-lookup"><span data-stu-id="947d9-142">Upgrade your environment to App-V4.6SP2</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="947d9-143">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</span><span class="sxs-lookup"><span data-stu-id="947d9-143">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="947d9-144">Installare il client App-V 5,0 con la coesistenza abilitata.</span><span class="sxs-lookup"><span data-stu-id="947d9-144">Install the App-V 5.0 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)"><span data-ttu-id="947d9-145">Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer </a> .</span><span class="sxs-lookup"><span data-stu-id="947d9-145">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="947d9-146">Sequenziare e distribuire pacchetti App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="947d9-146">Sequence and roll out App-V 5.0 packages.</span></span> <span data-ttu-id="947d9-147">Se necessario, Annulla la pubblicazione di pacchetti App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="947d9-147">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)"><span data-ttu-id="947d9-148">Come sequenziare una nuova applicazione con App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="947d9-148">How to Sequence a New Application with App-V 5.0</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="947d9-149">**Importante**  È necessario eseguire App-V 4.6 SP3 per usare la modalità di coesistenza.</span><span class="sxs-lookup"><span data-stu-id="947d9-149">**Important** You must be running App-V4.6SP3 to use coexistence mode.</span></span> <span data-ttu-id="947d9-150">Inoltre, quando si sequenzia un pacchetto, è necessario configurare l'impostazione dell'autorità di gestione, che si trova nella **Configurazione utente** nella sezione **Configurazione utente** .</span><span class="sxs-lookup"><span data-stu-id="947d9-150">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="947d9-151">Migrazione dell'infrastruttura completa del server App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="947d9-151">Migrating the App-V 5.0 Server Full Infrastructure</span></span>


<span data-ttu-id="947d9-152">Non esiste un metodo diretto per eseguire l'aggiornamento a un'infrastruttura App-V 5,0 completa.</span><span class="sxs-lookup"><span data-stu-id="947d9-152">There is no direct method to upgrade to a full App-V 5.0 infrastructure.</span></span> <span data-ttu-id="947d9-153">Usare le informazioni nella sezione seguente per informazioni sull'aggiornamento del server App-V.</span><span class="sxs-lookup"><span data-stu-id="947d9-153">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="947d9-154">Attività</span><span class="sxs-lookup"><span data-stu-id="947d9-154">Task</span></span></th>
<th align="left"><span data-ttu-id="947d9-155">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="947d9-155">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="947d9-156">Aggiornare l'ambiente in App-V 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="947d9-156">Upgrade your environment to App-V4.6SP3.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="947d9-157">Considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni </a> .</span><span class="sxs-lookup"><span data-stu-id="947d9-157">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="947d9-158">Distribuire App-V 5,0 versione del client.</span><span class="sxs-lookup"><span data-stu-id="947d9-158">Deploy App-V 5.0 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="947d9-159">Come distribuire il client App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="947d9-159">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="947d9-160">Installare App-V 5,0 Server.</span><span class="sxs-lookup"><span data-stu-id="947d9-160">Install App-V 5.0 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="947d9-161">Come distribuire il server App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="947d9-161">How to Deploy the App-V 5.0 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="947d9-162">Eseguire la migrazione dei pacchetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="947d9-162">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="947d9-163">Vedere i <strong> pacchetti di conversione creati con una versione precedente della sezione App-V </strong> di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="947d9-163">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="947d9-164">Altre attività di migrazione</span><span class="sxs-lookup"><span data-stu-id="947d9-164">Additional Migration tasks</span></span>


<span data-ttu-id="947d9-165">È anche possibile eseguire altre attività di migrazione, come la riconfigurazione dei punti finali e l'apertura di un pacchetto creato con una versione precedente in un computer che esegue il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="947d9-165">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.0 client.</span></span> <span data-ttu-id="947d9-166">I collegamenti seguenti includono ulteriori informazioni sull'esecuzione di queste attività.</span><span class="sxs-lookup"><span data-stu-id="947d9-166">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="947d9-167">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="947d9-167">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="947d9-168">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="947d9-168">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[<span data-ttu-id="947d9-169">Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="947d9-169">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="947d9-170">Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="947d9-170">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="947d9-171">Altre risorse per l'esecuzione di attività di migrazione App-V</span><span class="sxs-lookup"><span data-stu-id="947d9-171">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="947d9-172">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="947d9-172">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

[<span data-ttu-id="947d9-173">Procedura di aggiornamento del server di gestione di Microsoft App-V 5,1 semplificata</span><span class="sxs-lookup"><span data-stu-id="947d9-173">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





