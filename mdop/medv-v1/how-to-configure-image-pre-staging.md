---
title: Come configurare la pre-installazione dell'immagine
description: Come configurare la pre-installazione dell'immagine
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826406"
---
# <span data-ttu-id="6a408-103">Come configurare la pre-installazione dell'immagine</span><span class="sxs-lookup"><span data-stu-id="6a408-103">How to Configure Image Pre-staging</span></span>


<span data-ttu-id="6a408-104">**Nota**  La pre-staging delle immagini è utile solo per il download dell'immagine iniziale.</span><span class="sxs-lookup"><span data-stu-id="6a408-104">**Note** Image pre-staging is useful only for the initial image download.</span></span> <span data-ttu-id="6a408-105">Non è supportata per l'aggiornamento delle immagini.</span><span class="sxs-lookup"><span data-stu-id="6a408-105">It is not supported for image update.</span></span>

 

## <span data-ttu-id="6a408-106">Come configurare la pre-installazione dell'immagine</span><span class="sxs-lookup"><span data-stu-id="6a408-106">How to Configure Image Pre-staging</span></span>


**<span data-ttu-id="6a408-107">Per configurare la pre-staging delle immagini</span><span class="sxs-lookup"><span data-stu-id="6a408-107">To configure image pre-staging</span></span>**

1.  <span data-ttu-id="6a408-108">Nel computer client, nella directory dell'archivio immagini, creare una cartella per l'immagine di pre-staging e denominarla *Immagini MED-V*.</span><span class="sxs-lookup"><span data-stu-id="6a408-108">On the client computer, under the image store directory, create a folder for the pre-staging image, and name it *MED-V Images*.</span></span>

    <span data-ttu-id="6a408-109">**Nota**  Questa cartella deve essere denominata *Immagini MED-V*.</span><span class="sxs-lookup"><span data-stu-id="6a408-109">**Note** This folder must be called *MED-V Images*.</span></span>

     

2.  <span data-ttu-id="6a408-110">All'interno della cartella Immagini MED-V creare una sottocartella e denominarla *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="6a408-110">Inside the MED-V Images folder, create a subfolder and name it *PrestagedImages*.</span></span>

    <span data-ttu-id="6a408-111">**Nota**  Questa cartella deve essere denominata *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="6a408-111">**Note** This folder must be called *PrestagedImages*.</span></span>

     

3.  <span data-ttu-id="6a408-112">Per applicare la sicurezza degli elenchi di controllo di accesso (ACL) alla cartella *Immagini MED-V* , impostare l'ACL seguente:</span><span class="sxs-lookup"><span data-stu-id="6a408-112">To apply Access Control Lists (ACL) security to the *MED-V Images* folder, set the following ACL:</span></span>

    **<span data-ttu-id="6a408-113">Utenti di NT AUTHORITY\\Authenticated: (OI) (CI) (accesso speciale:)</span><span class="sxs-lookup"><span data-stu-id="6a408-113">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 <span data-ttu-id="6a408-114">FILE \ _APPEND \ _DATA</span><span class="sxs-lookup"><span data-stu-id="6a408-114">FILE\_APPEND\_DATA</span></span>**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **<span data-ttu-id="6a408-115">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="6a408-115">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="6a408-116">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="6a408-116">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="6a408-117">**Nota**  È consigliabile applicare la sicurezza ACL alla cartella *Immagini MED-V* .</span><span class="sxs-lookup"><span data-stu-id="6a408-117">**Note** It is recommended to apply ACL security to the *MED-V Images* folder.</span></span>

     

4.  <span data-ttu-id="6a408-118">Per applicare la sicurezza ACL alla cartella *PrestagedImages* , impostare l'ACL seguente:</span><span class="sxs-lookup"><span data-stu-id="6a408-118">To apply ACL security to the *PrestagedImages* folder, set the following ACL:</span></span>

    **<span data-ttu-id="6a408-119">Utenti di NT AUTHORITY\\Authenticated: (OI) (CI) (accesso speciale:)</span><span class="sxs-lookup"><span data-stu-id="6a408-119">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

    **<span data-ttu-id="6a408-120">LEGGI \ _CONTROL</span><span class="sxs-lookup"><span data-stu-id="6a408-120">READ\_CONTROL</span></span>**

    **<span data-ttu-id="6a408-121">SINCRONIZZARE</span><span class="sxs-lookup"><span data-stu-id="6a408-121">SYNCHRONIZE</span></span>**

    **<span data-ttu-id="6a408-122">FILE \ _GENERIC \ _READ</span><span class="sxs-lookup"><span data-stu-id="6a408-122">FILE\_GENERIC\_READ</span></span>**

    **<span data-ttu-id="6a408-123">FILE \ _READ \ _DATA</span><span class="sxs-lookup"><span data-stu-id="6a408-123">FILE\_READ\_DATA</span></span>**

    **<span data-ttu-id="6a408-124">FILE \ _READ \ _EA</span><span class="sxs-lookup"><span data-stu-id="6a408-124">FILE\_READ\_EA</span></span>**

    **<span data-ttu-id="6a408-125">FILE \ _READ \ _ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="6a408-125">FILE\_READ\_ATTRIBUTES</span></span>**

    **<span data-ttu-id="6a408-126">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="6a408-126">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="6a408-127">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="6a408-127">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="6a408-128">**Nota**  È consigliabile applicare la sicurezza ACL alla cartella *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="6a408-128">**Note** It is recommended to apply ACL security to the *PrestagedImages* folder.</span></span>

     

5.  <span data-ttu-id="6a408-129">Premere i file di immagine (CKM e INDEX files) nella cartella *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="6a408-129">Push the image files (CKM and INDEX files) to the *PrestagedImages* folder.</span></span>

    <span data-ttu-id="6a408-130">**Nota**  Dopo che i file di immagine sono stati spostati nella cartella pre-stage, è consigliabile eseguire un controllo di integrità dei dati e contrassegnare i file come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6a408-130">**Note** After the image files have been pushed to the pre-stage folder, it is recommended to run a data integrity check and to mark the files as read-only.</span></span>

     

6.  <span data-ttu-id="6a408-131">Includere il parametro seguente nell'installazione del client MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V images"*.</span><span class="sxs-lookup"><span data-stu-id="6a408-131">Include the following parameter in the MED-V client installation: *Client.MSI VMSFOLDER=”C:\\MED-V Images”*.</span></span>

## <span data-ttu-id="6a408-132">Come aggiornare la posizione pre-stage</span><span class="sxs-lookup"><span data-stu-id="6a408-132">How to Update the Pre-stage Location</span></span>


**<span data-ttu-id="6a408-133">Per aggiornare la posizione pre-stage</span><span class="sxs-lookup"><span data-stu-id="6a408-133">To update the pre-stage location</span></span>**

1.  <span data-ttu-id="6a408-134">La chiave del registro di sistema *PrestagedImagesPath*indica la posizione predefinita dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="6a408-134">The registry key, *PrestagedImagesPath*, points to the default image location.</span></span> <span data-ttu-id="6a408-135">Si trova nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="6a408-135">It is located in the following directory:</span></span>

    -   <span data-ttu-id="6a408-136">In un x86-</span><span class="sxs-lookup"><span data-stu-id="6a408-136">On an x86 -</span></span> `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   <span data-ttu-id="6a408-137">In un x64-</span><span class="sxs-lookup"><span data-stu-id="6a408-137">On an x64 -</span></span> `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  <span data-ttu-id="6a408-138">Se l'immagine si trova in un percorso diverso, modificare il percorso.</span><span class="sxs-lookup"><span data-stu-id="6a408-138">If the image is in a different location, change the path.</span></span>

 

 





