---
title: Come eseguire il backup e ripristinare un server MED-V
description: Come eseguire il backup e ripristinare un server MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823086"
---
# <span data-ttu-id="edffa-103">Come eseguire il backup e ripristinare un server MED-V</span><span class="sxs-lookup"><span data-stu-id="edffa-103">How to Back Up and Restore a MED-V Server</span></span>


<span data-ttu-id="edffa-104">I file XML che si trovano nel server possono essere sottoposti a backup e quindi ripristinati in caso di perdita di dati nel server.</span><span class="sxs-lookup"><span data-stu-id="edffa-104">XML files located on the server can be backed up and then restored in case of loss of data on the server.</span></span>

**<span data-ttu-id="edffa-105">Per eseguire il backup di un server MED-V</span><span class="sxs-lookup"><span data-stu-id="edffa-105">To back up a MED-V server</span></span>**

-   <span data-ttu-id="edffa-106">Eseguire il backup dei file seguenti, che si trovano in \* &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer\*:</span><span class="sxs-lookup"><span data-stu-id="edffa-106">Back up the following files, located in *&lt;InstallDir&gt;\\Servers\\ConfigurationServer*:</span></span>

    <span data-ttu-id="edffa-107">**Nota**  Se la configurazione è stata modificata rispetto all'impostazione predefinita, i file potrebbero essere archiviati in una posizione diversa.</span><span class="sxs-lookup"><span data-stu-id="edffa-107">**Note** If the configuration has been changed from the default, the files might be stored in a different location.</span></span>

     

    -   <span data-ttu-id="edffa-108">ClientPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="edffa-108">ClientPolicy.xml</span></span>

    -   <span data-ttu-id="edffa-109">ClientSettings.xml</span><span class="sxs-lookup"><span data-stu-id="edffa-109">ClientSettings.xml</span></span>

    -   <span data-ttu-id="edffa-110">ConfigurationFiles.xml</span><span class="sxs-lookup"><span data-stu-id="edffa-110">ConfigurationFiles.xml</span></span>

    -   <span data-ttu-id="edffa-111">OrganizationPolicy.xml</span><span class="sxs-lookup"><span data-stu-id="edffa-111">OrganizationPolicy.xml</span></span>

    -   <span data-ttu-id="edffa-112">WorkspaceKeys.xml</span><span class="sxs-lookup"><span data-stu-id="edffa-112">WorkspaceKeys.xml</span></span>

    <span data-ttu-id="edffa-113">**Nota**  È anche possibile eseguire il backup del file ServerSettings.xml.</span><span class="sxs-lookup"><span data-stu-id="edffa-113">**Note** The ServerSettings.xml file can be backed up as well.</span></span> <span data-ttu-id="edffa-114">Tuttavia, se è stata modificata una configurazione specifica, ad esempio nel server originale, la directory di VM MED-V si trova in "*C:\\Vms*" e tale directory non esiste nel nuovo server, può causare un errore.</span><span class="sxs-lookup"><span data-stu-id="edffa-114">However, if a specific configuration has been changed (for example, on the original server, the MED-V VMS directory is located in "*C:\\Vms*" and such a directory does not exist on the new server), it can cause an error.</span></span>

     

**<span data-ttu-id="edffa-115">Per ripristinare un server MED-V</span><span class="sxs-lookup"><span data-stu-id="edffa-115">To restore a MED-V server</span></span>**

1.  <span data-ttu-id="edffa-116">Installare un nuovo server MED-V.</span><span class="sxs-lookup"><span data-stu-id="edffa-116">Install a new MED-V server.</span></span>

2.  <span data-ttu-id="edffa-117">Copiare i file di backup nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="edffa-117">Copy the backup files to the following directory:</span></span>

    *<span data-ttu-id="edffa-118">&lt;InstallDir &gt; \\Servers\\ConfigurationServer</span><span class="sxs-lookup"><span data-stu-id="edffa-118">&lt;InstallDir&gt;\\Servers\\ConfigurationServer</span></span>*

3.  <span data-ttu-id="edffa-119">Riavviare il servizio MED-V.</span><span class="sxs-lookup"><span data-stu-id="edffa-119">Restart the MED-V service.</span></span>

 

 





