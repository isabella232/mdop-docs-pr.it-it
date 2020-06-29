---
title: Come pubblicare un'applicazione virtuale nel client
description: Come pubblicare un'applicazione virtuale nel client
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816875"
---
# <span data-ttu-id="64341-103">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="64341-103">How to Publish a Virtual Application on the Client</span></span>


<span data-ttu-id="64341-104">Quando si distribuisce la virtualizzazione delle applicazioni usando un sistema di distribuzione elettronica del software, è possibile usare una delle procedure seguenti per pubblicare un pacchetto di applicazione per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="64341-104">When you deploy Application Virtualization by using an electronic software distribution system, you can use one of the following procedures to publish an application package to your users.</span></span>

**<span data-ttu-id="64341-105">Per pubblicare un pacchetto usando un file autonomo di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="64341-105">To publish a package using a stand-alone Windows Installer file</span></span>**

1.  <span data-ttu-id="64341-106">Il client deve essere installato con il parametro *RequireAuthorizationIfCached* impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="64341-106">The client should be installed with the *REQUIREAUTHORIZATIONIFCACHED* parameter set to 0 (zero).</span></span> <span data-ttu-id="64341-107">Per altre informazioni sull'impostazione di questo parametro, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="64341-107">For more information about setting this parameter, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md)</span></span>

2.  <span data-ttu-id="64341-108">Copiare il file di Windows Installer e il file SFT nella stessa cartella nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="64341-108">Copy the Windows Installer file and the SFT file to same folder on the target computer.</span></span>

3.  <span data-ttu-id="64341-109">Eseguire il comando seguente nel computer:</span><span class="sxs-lookup"><span data-stu-id="64341-109">Run the following command on the computer:</span></span>

    `Msiexec.exe /I "packagename.msi" /q`

**<span data-ttu-id="64341-110">Per pubblicare un pacchetto con Windows Installer e il manifesto del pacchetto</span><span class="sxs-lookup"><span data-stu-id="64341-110">To publish a package using Windows Installer and the package manifest</span></span>**

1.  <span data-ttu-id="64341-111">Copiare il file di Windows Installer nel computer di destinazione e il file SFT nella condivisione contenuto nel server di streaming.</span><span class="sxs-lookup"><span data-stu-id="64341-111">Copy the Windows Installer file to the target computer and the SFT file to the CONTENT share on the streaming server.</span></span>

2.  <span data-ttu-id="64341-112">Eseguire il comando seguente nel computer di ogni utente:</span><span class="sxs-lookup"><span data-stu-id="64341-112">Run the following command on each user’s computer:</span></span>

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    <span data-ttu-id="64341-113">**Importante**  Per OVERRIDEURL tutti i caratteri della barra rovesciata devono essere sfuggiti usando una barra rovesciata precedente o il percorso di OVERRIDEURL non verrà analizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="64341-113">**Important** For OVERRIDEURL all backslash characters must be escaped using a preceding backslash, or the OVERRIDEURL path will not be parsed correctly.</span></span> <span data-ttu-id="64341-114">Inoltre, le proprietà e i valori devono essere immessi in maiuscolo, ad eccezione del caso in cui il valore è un percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="64341-114">Also, properties and values must be entered as uppercase except where the value is a path to a file.</span></span>

     

**<span data-ttu-id="64341-115">Per pubblicare un pacchetto con SFTMIME</span><span class="sxs-lookup"><span data-stu-id="64341-115">To publish a package using SFTMIME</span></span>**

-   <span data-ttu-id="64341-116">Per un esempio di come pubblicare un'applicazione per tutti gli utenti in un computer, eseguire il comando seguente nel computer dell'utente:</span><span class="sxs-lookup"><span data-stu-id="64341-116">For an example of how to publish an application for all users on a computer, run the following command on the user’s computer:</span></span>

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    <span data-ttu-id="64341-117">Per altre informazioni su questi e altri comandi di SFTMIME, Vedi [riferimento al comando SFTMIME](sftmime--command-reference.md).</span><span class="sxs-lookup"><span data-stu-id="64341-117">For additional details about these and other SFTMIME commands, see [SFTMIME Command Reference](sftmime--command-reference.md).</span></span>

## <span data-ttu-id="64341-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64341-118">Related topics</span></span>


[<span data-ttu-id="64341-119">Determinare il metodo di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="64341-119">Determine Your Publishing Method</span></span>](determine-your-publishing-method.md)

[<span data-ttu-id="64341-120">Scenario basato sulla distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="64341-120">Electronic Software Distribution-Based Scenario</span></span>](electronic-software-distribution-based-scenario.md)

[<span data-ttu-id="64341-121">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="64341-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

[<span data-ttu-id="64341-122">Scenario di recapito autonomo per i Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="64341-122">Stand-Alone Delivery Scenario for Application Virtualization Clients</span></span>](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





