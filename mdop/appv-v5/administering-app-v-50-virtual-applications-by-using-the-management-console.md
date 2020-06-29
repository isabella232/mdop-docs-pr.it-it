---
title: Amministrazione delle applicazioni virtuali App-V 5.0 usando la console di gestione
description: Amministrazione delle applicazioni virtuali App-V 5.0 usando la console di gestione
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806051"
---
# <span data-ttu-id="6cd80-103">Amministrazione delle applicazioni virtuali App-V 5.0 usando la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-103">Administering App-V 5.0 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="6cd80-104">Usare il server di gestione di Microsoft Application Virtualization (App-V) 5,0 per gestire i pacchetti, i gruppi di connessioni e l'accesso ai pacchetti nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="6cd80-104">Use the Microsoft Application Virtualization (App-V) 5.0 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="6cd80-105">Il server pubblica le icone delle applicazioni, i collegamenti e le associazioni di tipi di file nei computer autorizzati che eseguono il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6cd80-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="6cd80-106">Uno o più server di gestione condividono in genere un archivio dati comune per le informazioni di configurazione e pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6cd80-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="6cd80-107">Il server di gestione usa i gruppi di servizi di dominio Active Directory (AD DS) per gestire l'autorizzazione degli utenti e ha installato SQL Server per gestire il database e l'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="6cd80-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="6cd80-108">Poiché i server di gestione applicano il flusso delle applicazioni agli utenti finali su richiesta, questi server sono ideali per le configurazioni di sistema con LAN affidabili e a larghezza di banda elevata.</span><span class="sxs-lookup"><span data-stu-id="6cd80-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="6cd80-109">Il server di gestione è costituito dai componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="6cd80-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="6cd80-110">Server di gestione: usare il server di gestione per gestire i pacchetti e i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6cd80-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="6cd80-111">Server di pubblicazione: usare il server di pubblicazione per distribuire i pacchetti in computer che eseguono il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6cd80-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.0 client.</span></span>

-   <span data-ttu-id="6cd80-112">Database di gestione: usare il database di gestione per gestire l'accesso al pacchetto e pubblicare la sincronizzazione del server con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="6cd80-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="6cd80-113">Attività della console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-113">Management Console tasks</span></span>


<span data-ttu-id="6cd80-114">Le attività più comuni che è possibile eseguire con la console di gestione di App-V 5,0 sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="6cd80-114">The most common tasks that you can perform with the App-V 5.0 Management console are:</span></span>

-   [<span data-ttu-id="6cd80-115">Come connettersi alla console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-beta.md)

-   [<span data-ttu-id="6cd80-116">Come aggiungere o aggiornare pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [<span data-ttu-id="6cd80-117">Come configurare l'accesso ai pacchetti tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [<span data-ttu-id="6cd80-118">Come pubblicare un pacchetto tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [<span data-ttu-id="6cd80-119">Come eliminare un pacchetto nella console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-beta.md)

-   [<span data-ttu-id="6cd80-120">Come aggiungere o rimuovere un amministratore tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [<span data-ttu-id="6cd80-121">Come registrare e annullare la registrazione di un server di pubblicazione tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [<span data-ttu-id="6cd80-122">Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6cd80-122">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [<span data-ttu-id="6cd80-123">Come trasferire l'accesso e le configurazioni a un'altra versione di un pacchetto con la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [<span data-ttu-id="6cd80-124">Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [<span data-ttu-id="6cd80-125">Configurare le applicazioni e le estensioni delle applicazioni virtuali predefinite nel sistema di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-125">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

<span data-ttu-id="6cd80-126">Gli elementi principali della console di gestione di App-V 5,0 sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6cd80-126">The main elements of the App-V 5.0 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6cd80-127">Scheda console di gestione</span><span class="sxs-lookup"><span data-stu-id="6cd80-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="6cd80-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cd80-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cd80-129">Panoramica</span><span class="sxs-lookup"><span data-stu-id="6cd80-129">Overview</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><strong><span data-ttu-id="6cd80-130">App-V Sequencer </strong> - selezionare questa opzione per visualizzare informazioni generali sull'uso del sequencer App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="6cd80-130">App-V Sequencer</strong> - Select this option to review general information about using the App-V 5.0 sequencer.</span></span></p></li>
<li><p><strong><span data-ttu-id="6cd80-131">Raccolta pacchetti applicazione </strong> : selezionare questa opzione per aprire la <strong> </strong> pagina pacchetti della console di gestione.</span><span class="sxs-lookup"><span data-stu-id="6cd80-131">Application Packages Library</strong> – Select this option to open the <strong>PACKAGES</strong> page of the Management Console.</span></span> <span data-ttu-id="6cd80-132">Usare questa pagina per rivedere i pacchetti che sono stati aggiunti al server.</span><span class="sxs-lookup"><span data-stu-id="6cd80-132">Use this page to review packages that have been added to the server.</span></span> <span data-ttu-id="6cd80-133">È anche possibile gestire i gruppi di connessioni, nonché aggiungere o aggiornare i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6cd80-133">You can also manage the connection groups, as well as add or upgrade packages.</span></span></p></li>
<li><p><strong><span data-ttu-id="6cd80-134">Server </strong> : selezionare questa opzione per aprire la <strong> </strong> pagina server della console di gestione.</span><span class="sxs-lookup"><span data-stu-id="6cd80-134">SERVERS</strong> – Select this option to open the <strong>SERVERS</strong> page of the Management Console.</span></span> <span data-ttu-id="6cd80-135">Usare questa pagina per esaminare l'elenco dei server registrati con l'infrastruttura dell'App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6cd80-135">Use this page to review the list of servers that have been registered with your App-V 5.0 infrastructure.</span></span></p></li>
<li><p><strong><span data-ttu-id="6cd80-136">CLIENT </strong> : selezionare questa opzione per visualizzare informazioni generali sui client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6cd80-136">CLIENTS</strong> – Select this option to review general information about App-V 5.0 clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cd80-137">Scheda pacchetti</span><span class="sxs-lookup"><span data-stu-id="6cd80-137">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cd80-138">Usare la <strong> </strong> scheda pacchetti per aggiungere o aggiornare i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="6cd80-138">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span> <span data-ttu-id="6cd80-139">È anche possibile gestire i gruppi di connessioni facendo clic su <strong> gruppi di connessioni </strong> .</span><span class="sxs-lookup"><span data-stu-id="6cd80-139">You can also manage connection groups by clicking <strong>CONNECTION GROUPS</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6cd80-140">Scheda Server</span><span class="sxs-lookup"><span data-stu-id="6cd80-140">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cd80-141">Usare la <strong> </strong> scheda Server per registrare un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="6cd80-141">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6cd80-142">Scheda amministratori</span><span class="sxs-lookup"><span data-stu-id="6cd80-142">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6cd80-143">Usare la <strong> </strong> scheda amministratori per registrare, aggiungere o rimuovere gli amministratori nell'ambiente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6cd80-143">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.0 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a><span data-ttu-id="6cd80-144">Altre risorse per questa implementazione di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="6cd80-144">Other resources for this App-V 5.0 deployment</span></span>


-   [<span data-ttu-id="6cd80-145">Guida dell'amministratore di Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="6cd80-145">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="6cd80-146">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6cd80-146">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





