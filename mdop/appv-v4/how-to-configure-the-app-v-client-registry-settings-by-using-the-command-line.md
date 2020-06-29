---
title: Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando
description: Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817896"
---
# <span data-ttu-id="fe185-103">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="fe185-103">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>


<span data-ttu-id="fe185-104">Dopo la distribuzione e la configurazione del client Application Virtualization (App-V) durante l'installazione tramite la riga di comando, potrebbe essere necessario modificare una o più impostazioni di configurazione del client.</span><span class="sxs-lookup"><span data-stu-id="fe185-104">After the Application Virtualization (App-V) Client has been deployed and configured during the installation by using the command line, it might be necessary to change one or more client configuration settings.</span></span> <span data-ttu-id="fe185-105">Questa operazione viene eseguita modificando le chiavi del registro di sistema appropriate, usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe185-105">This is accomplished by editing the appropriate registry keys, using one of the following methods:</span></span>

-   <span data-ttu-id="fe185-106">Uso diretto dell'editor del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="fe185-106">Using the Registry Editor directly</span></span>

-   <span data-ttu-id="fe185-107">Uso di un file reg</span><span class="sxs-lookup"><span data-stu-id="fe185-107">Using a .reg file</span></span>

-   <span data-ttu-id="fe185-108">Uso di un linguaggio di scripting come VBScript o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fe185-108">Using a scripting language such as VBScript or Windows PowerShell</span></span>

<span data-ttu-id="fe185-109">È anche possibile usare un modello ADM.</span><span class="sxs-lookup"><span data-stu-id="fe185-109">There is also an ADM template that you can use.</span></span> <span data-ttu-id="fe185-110">Per altre informazioni sul modello ADM, vedere <https://go.microsoft.com/fwlink/?LinkId=121835> .</span><span class="sxs-lookup"><span data-stu-id="fe185-110">For more information about the ADM template, see <https://go.microsoft.com/fwlink/?LinkId=121835>.</span></span>

<span data-ttu-id="fe185-111">**Attenzione**  Prestare attenzione quando si modifica il registro di sistema perché gli errori possono uscire dal computer in uno stato non utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="fe185-111">**Caution** Use care when you edit the registry because errors can leave the computer in an unusable state.</span></span> <span data-ttu-id="fe185-112">Assicurati di seguire le procedure aziendali standard correlate alle modifiche del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fe185-112">Be sure to follow your standard business practices that relate to registry edits.</span></span> <span data-ttu-id="fe185-113">Verificare accuratamente tutte le modifiche proposte in un ambiente di test prima di distribuirle ai computer di produzione.</span><span class="sxs-lookup"><span data-stu-id="fe185-113">Thoroughly test all proposed changes in a test environment before you deploy them to production computers.</span></span>

 

## <span data-ttu-id="fe185-114">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="fe185-114">In This Section</span></span>


<span data-ttu-id="fe185-115">**Importante**  In un computer a 64 bit le chiavi e i valori descritti nelle sezioni seguenti saranno in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="fe185-115">**Important** On a 64-bit computer, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[<span data-ttu-id="fe185-116">Come reimpostare la cache di FileSystem</span><span class="sxs-lookup"><span data-stu-id="fe185-116">How to Reset the FileSystem Cache</span></span>](how-to-reset-the-filesystem-cache.md)  
<span data-ttu-id="fe185-117">Fornisce le informazioni necessarie per reimpostare la cache del FileSystem.</span><span class="sxs-lookup"><span data-stu-id="fe185-117">Provides the information that is required to reset the FileSystem cache.</span></span>

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[<span data-ttu-id="fe185-118">Come modificare le dimensioni della cache di FileSystem</span><span class="sxs-lookup"><span data-stu-id="fe185-118">How to Change the Size of the FileSystem Cache</span></span>](how-to-change-the-size-of-the-filesystem-cache.md)  
<span data-ttu-id="fe185-119">Spiega come modificare le dimensioni della cache.</span><span class="sxs-lookup"><span data-stu-id="fe185-119">Explains how you can change the size of the cache.</span></span>

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[<span data-ttu-id="fe185-120">Come usare la funzionalità di gestione dello spazio della cache</span><span class="sxs-lookup"><span data-stu-id="fe185-120">How to Use the Cache Space Management Feature</span></span>](how-to-use-the-cache-space-management-feature.md)  
<span data-ttu-id="fe185-121">Descrive come configurare la funzionalità di gestione dello spazio della cache.</span><span class="sxs-lookup"><span data-stu-id="fe185-121">Describes how you can configure the cache space management feature.</span></span>

<a href="" id="how-to-configure-the-client-log-file"></a>[<span data-ttu-id="fe185-122">Come configurare il file di registro del client</span><span class="sxs-lookup"><span data-stu-id="fe185-122">How to Configure the Client Log File</span></span>](how-to-configure-the-client-log-file.md)  
<span data-ttu-id="fe185-123">Descrive i vari valori della chiave del registro di sistema che controllano il file di log del client e come è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="fe185-123">Describes the various registry key values that control the client log file and how you can change them.</span></span>

<a href="" id="how-to-configure-user-permissions"></a>[<span data-ttu-id="fe185-124">Come configurare le autorizzazioni utente</span><span class="sxs-lookup"><span data-stu-id="fe185-124">How to Configure User Permissions</span></span>](how-to-configure-user-permissions.md)  
<span data-ttu-id="fe185-125">Identifica la chiave del registro di sistema che controlla le autorizzazioni utente e fornisce esempi di come modificare alcune autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="fe185-125">Identifies the registry key that controls the user permissions and gives examples of how you can change some permissions.</span></span>

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[<span data-ttu-id="fe185-126">Come configurare il client per il recupero del pacchetto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="fe185-126">How to Configure the Client for Application Package Retrieval</span></span>](how-to-configure-the-client-for-application-package-retrieval.md)  
<span data-ttu-id="fe185-127">Spiega come configurare il client per recuperare il contenuto del pacchetto, le icone e le associazioni di tipi di file da origini diverse e fornisce diversi esempi del formato di percorso corretto.</span><span class="sxs-lookup"><span data-stu-id="fe185-127">Explains how to configure the client to retrieve package content, icons, and file type associations from different sources, and provides several examples of the correct path format.</span></span>

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[<span data-ttu-id="fe185-128">Come configurare il client per la modalità di operazioni senza connessione</span><span class="sxs-lookup"><span data-stu-id="fe185-128">How to Configure the Client for Disconnected Operation Mode</span></span>](how-to-configure-the-client-for-disconnected-operation-mode.md)  
<span data-ttu-id="fe185-129">Vengono fornite informazioni su come configurare le varie impostazioni associate alla modalità operazioni disconnesse.</span><span class="sxs-lookup"><span data-stu-id="fe185-129">Provides information about how to configure the various settings associated with disconnected operations mode.</span></span>

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[<span data-ttu-id="fe185-130">Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti</span><span class="sxs-lookup"><span data-stu-id="fe185-130">How to Configure Shortcut and File Type Association Behavior</span></span>](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
<span data-ttu-id="fe185-131">Descrive i valori della chiave del registro di sistema che controllano le scelte rapide e le associazioni di tipi di file nel client App-V e fornisce informazioni dettagliate su come configurarle.</span><span class="sxs-lookup"><span data-stu-id="fe185-131">Describes the registry key values that control shortcuts and file type associations in the App-V client, and provides details on how to configure them.</span></span>

## <span data-ttu-id="fe185-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe185-132">Related topics</span></span>


[<span data-ttu-id="fe185-133">Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="fe185-133">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





