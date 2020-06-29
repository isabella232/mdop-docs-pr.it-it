---
title: Amministrazione delle applicazioni virtuali App-V 5.1 usando la console di gestione
description: Amministrazione delle applicazioni virtuali App-V 5.1 usando la console di gestione
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806046"
---
# <span data-ttu-id="cd876-103">Amministrazione delle applicazioni virtuali App-V 5.1 usando la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-103">Administering App-V 5.1 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="cd876-104">Usare il server di gestione di Microsoft Application Virtualization (App-V) 5,1 per gestire i pacchetti, i gruppi di connessioni e l'accesso ai pacchetti nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="cd876-104">Use the Microsoft Application Virtualization (App-V) 5.1 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="cd876-105">Il server pubblica le icone delle applicazioni, i collegamenti e le associazioni di tipi di file nei computer autorizzati che eseguono il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="cd876-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="cd876-106">Uno o più server di gestione condividono in genere un archivio dati comune per le informazioni di configurazione e pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cd876-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="cd876-107">Il server di gestione usa i gruppi di servizi di dominio Active Directory (AD DS) per gestire l'autorizzazione degli utenti e ha installato SQL Server per gestire il database e l'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="cd876-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="cd876-108">Poiché i server di gestione applicano il flusso delle applicazioni agli utenti finali su richiesta, questi server sono ideali per le configurazioni di sistema con LAN affidabili e a larghezza di banda elevata.</span><span class="sxs-lookup"><span data-stu-id="cd876-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="cd876-109">Il server di gestione è costituito dai componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd876-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="cd876-110">Server di gestione: usare il server di gestione per gestire i pacchetti e i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="cd876-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="cd876-111">Server di pubblicazione: usare il server di pubblicazione per distribuire i pacchetti in computer che eseguono il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="cd876-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.1 client.</span></span>

-   <span data-ttu-id="cd876-112">Database di gestione: usare il database di gestione per gestire l'accesso al pacchetto e pubblicare la sincronizzazione del server con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="cd876-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="cd876-113">Attività della console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-113">Management Console tasks</span></span>


<span data-ttu-id="cd876-114">Le attività più comuni che è possibile eseguire con la console di gestione di App-V 5,1 sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd876-114">The most common tasks that you can perform with the App-V 5.1 Management console are:</span></span>

-   [<span data-ttu-id="cd876-115">Come connettersi alla console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-51.md)

-   [<span data-ttu-id="cd876-116">Come aggiungere o aggiornare pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [<span data-ttu-id="cd876-117">Come configurare l'accesso ai pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [<span data-ttu-id="cd876-118">Come pubblicare un pacchetto tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [<span data-ttu-id="cd876-119">Come eliminare un pacchetto nella console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-51.md)

-   [<span data-ttu-id="cd876-120">Come aggiungere o rimuovere un amministratore tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [<span data-ttu-id="cd876-121">Come registrare e annullare la registrazione di un server di pubblicazione tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [<span data-ttu-id="cd876-122">Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="cd876-122">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [<span data-ttu-id="cd876-123">Come trasferire l'accesso e le configurazioni a un'altra versione di un pacchetto con la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [<span data-ttu-id="cd876-124">Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [<span data-ttu-id="cd876-125">Come visualizzare e configurare applicazioni ed estensioni delle applicazioni virtuali predefinite tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-125">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

<span data-ttu-id="cd876-126">Gli elementi principali della console di gestione di App-V 5,1 sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cd876-126">The main elements of the App-V 5.1 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cd876-127">Scheda console di gestione</span><span class="sxs-lookup"><span data-stu-id="cd876-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="cd876-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd876-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd876-129">Scheda pacchetti</span><span class="sxs-lookup"><span data-stu-id="cd876-129">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd876-130">Usare la <strong> </strong> scheda pacchetti per aggiungere o aggiornare i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="cd876-130">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd876-131">Scheda gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="cd876-131">Connection Groups tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd876-132">Usare la <strong> scheda gruppi </strong> di connessioni per gestire i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="cd876-132">Use the <strong>CONNECTION GROUPS</strong> tab to manage connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cd876-133">Scheda Server</span><span class="sxs-lookup"><span data-stu-id="cd876-133">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd876-134">Usare la <strong> </strong> scheda Server per registrare un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="cd876-134">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="cd876-135">Scheda amministratori</span><span class="sxs-lookup"><span data-stu-id="cd876-135">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="cd876-136">Usare la <strong> </strong> scheda amministratori per registrare, aggiungere o rimuovere gli amministratori nell'ambiente App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="cd876-136">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.1 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cd876-137">**Importante**  JavaScript deve essere abilitato nel browser che apre la console di gestione Web.</span><span class="sxs-lookup"><span data-stu-id="cd876-137">**Important** JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a><span data-ttu-id="cd876-138">Altre risorse per questa implementazione di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="cd876-138">Other resources for this App-V 5.1 deployment</span></span>


-   [<span data-ttu-id="cd876-139">Guida dell'amministratore di Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="cd876-139">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="cd876-140">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="cd876-140">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





