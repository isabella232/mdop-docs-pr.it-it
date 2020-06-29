---
title: Come usare la funzionalità di gestione dello spazio della cache
description: Come usare la funzionalità di gestione dello spazio della cache
author: dansimp
ms.assetid: 60965660-c015-46a8-88ac-54cbc050fe33
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fcb9cc4bc076e1acf52fb1c03797384c45b82f7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816406"
---
# <span data-ttu-id="41771-103">Come usare la funzionalità di gestione dello spazio della cache</span><span class="sxs-lookup"><span data-stu-id="41771-103">How to Use the Cache Space Management Feature</span></span>


<span data-ttu-id="41771-104">La funzionalità di gestione dello spazio della cache di FileSystem usa un algoritmo LRU (least used) ed è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="41771-104">The FileSystem cache space management feature uses a Least Recently Used (LRU) algorithm and is enabled by default.</span></span> <span data-ttu-id="41771-105">Se lo spazio necessario per un nuovo pacchetto supererà lo spazio disponibile nella cache, il client di Application Virtualization (App-V) utilizzerà questa caratteristica per determinare i pacchetti esistenti che possono essere eliminati dalla cache per creare spazio per il nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="41771-105">If the space that is required for a new package would exceed the available free space in the cache, the Application Virtualization (App-V) Client uses this feature to determine which, if any, existing packages it can delete from the cache to make room for the new package.</span></span> <span data-ttu-id="41771-106">Il client elimina il pacchetto con la data di accesso ultimo meno recente, se è precedente al valore specificato nel valore del registro di sistema MinPkgAge.</span><span class="sxs-lookup"><span data-stu-id="41771-106">The client deletes the package with the oldest last-accessed date if it is older than the value specified in the MinPkgAge registry value.</span></span> <span data-ttu-id="41771-107">L'uso della funzionalità di gestione dello spazio della cache di FileSystem può anche evitare problemi di spazio nella cache Bassi.</span><span class="sxs-lookup"><span data-stu-id="41771-107">Use of the FileSystem cache space management feature can also help to avoid low cache space problems.</span></span>

<span data-ttu-id="41771-108">Se necessario, viene eliminato più di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="41771-108">More than one package is deleted if necessary.</span></span> <span data-ttu-id="41771-109">I pacchetti bloccati non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="41771-109">Packages that are locked are not deleted.</span></span>

<span data-ttu-id="41771-110">**Nota**  Per assicurarti che la cache disponga di spazio sufficiente per tutti i pacchetti che potrebbero essere distribuiti, usa l'impostazione **USA soglia di spazio libero su disco** quando configuri il client in modo che la cache possa crescere in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="41771-110">**Note** To ensure that the cache has sufficient space allocated for all packages that might be deployed, use the **Use free disk space threshold** setting when you configure the client so that the cache can grow as needed.</span></span> <span data-ttu-id="41771-111">In alternativa, determinare in anticipo la quantità di spazio su disco necessaria per la cache di App-V e, al momento dell'installazione, impostare le dimensioni della cache di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="41771-111">Alternatively, determine in advance how much disk space will be needed for the App-V cache, and at installation time, set the cache size accordingly.</span></span>

 

<span data-ttu-id="41771-112">La caratteristica di gestione dello spazio della cache è controllata dal valore del registro di sistema UnloadLeastRecentlyUsed.</span><span class="sxs-lookup"><span data-stu-id="41771-112">The cache space management feature is controlled by the UnloadLeastRecentlyUsed registry value.</span></span> <span data-ttu-id="41771-113">Il valore 1 Abilita la caratteristica e il valore 0 (zero) lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="41771-113">A value of 1 enables the feature, and a value of 0 (zero) disables it.</span></span>

**<span data-ttu-id="41771-114">Per abilitare o disabilitare la funzionalità di gestione dello spazio della cache</span><span class="sxs-lookup"><span data-stu-id="41771-114">To enable or disable the cache space management feature</span></span>**

-   <span data-ttu-id="41771-115">Imposta il valore del registro di sistema seguente su 1 per abilitare l'algoritmo LRU.</span><span class="sxs-lookup"><span data-stu-id="41771-115">Set the following registry value to 1 to enable the LRU algorithm.</span></span> <span data-ttu-id="41771-116">Impostarla su 0 (zero) per disabilitare la caratteristica.</span><span class="sxs-lookup"><span data-stu-id="41771-116">Set it to 0 (zero) to disable the feature.</span></span>

    <span data-ttu-id="41771-117">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span><span class="sxs-lookup"><span data-stu-id="41771-117">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\UnloadLeastRecentlyUsed</span></span>

**<span data-ttu-id="41771-118">Per controllare i pacchetti che possono essere eliminati</span><span class="sxs-lookup"><span data-stu-id="41771-118">To control which packages can be discarded</span></span>**

-   <span data-ttu-id="41771-119">Per determinare quando il pacchetto può essere selezionato per la disattivazione, imposta il valore del registro di sistema seguente per uguagliare il numero minimo di giorni che vuoi trascorrere dopo l'ultimo accesso al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="41771-119">To determine when the package can be selected for discard, set the following registry value to equal the minimum number of days you want to elapse since the package was last accessed.</span></span> <span data-ttu-id="41771-120">I pacchetti che sono stati usati più di recente non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="41771-120">Packages that have been used more recently are not discarded.</span></span>

    <span data-ttu-id="41771-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span><span class="sxs-lookup"><span data-stu-id="41771-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\MinPkgAge</span></span>

    <span data-ttu-id="41771-122">**Attenzione**  Il valore massimo per questa chiave del registro di sistema è 0x00011111.</span><span class="sxs-lookup"><span data-stu-id="41771-122">**Caution** The maximum value for this registry key is 0x00011111.</span></span> <span data-ttu-id="41771-123">I valori più grandi impediscono il corretto funzionamento della funzionalità di gestione dello spazio della cache.</span><span class="sxs-lookup"><span data-stu-id="41771-123">Larger values will prevent the correct operation of the cache space management feature.</span></span>

     

## <span data-ttu-id="41771-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41771-124">Related topics</span></span>


[<span data-ttu-id="41771-125">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="41771-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





