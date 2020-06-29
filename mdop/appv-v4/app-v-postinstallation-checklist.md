---
title: Elenco di controllo post-installazione di App-V
description: Elenco di controllo post-installazione di App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819805"
---
# <span data-ttu-id="d0619-103">Elenco di controllo post-installazione di App-V</span><span class="sxs-lookup"><span data-stu-id="d0619-103">App-V Postinstallation Checklist</span></span>


<span data-ttu-id="d0619-104">L'elenco di controllo seguente offre un alto livello di elementi da tenere in considerazione e descrive i passaggi da seguire dopo aver completato l'installazione di Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server e del client Desktop App-V.</span><span class="sxs-lookup"><span data-stu-id="d0619-104">The following checklist provides a high-level list of items to consider and outlines the steps you should take after you have completed the installation of the Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server, and the App-V Desktop Client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d0619-105">Passaggio</span><span class="sxs-lookup"><span data-stu-id="d0619-105">Step</span></span></th>
<th align="left"><span data-ttu-id="d0619-106">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d0619-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0619-107">Creare eccezioni del firewall per l'App-V Management Server o i servizi di streaming server.</span><span class="sxs-lookup"><span data-stu-id="d0619-107">Create firewall exceptions for the App-V Management Server or Streaming Server services.</span></span></p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)"><span data-ttu-id="d0619-108">Configurazione del firewall per i server App-V</span><span class="sxs-lookup"><span data-stu-id="d0619-108">Configuring the Firewall for the App-V Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0619-109">Verificare che il sistema App-V funzioni correttamente pubblicando, eseguendo il flusso e testando l'applicazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d0619-109">Verify that the App-V system is functioning correctly by publishing, streaming, and testing the default application.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)"><span data-ttu-id="d0619-110">Come installare e configurare l'applicazione predefinita</span><span class="sxs-lookup"><span data-stu-id="d0619-110">How to Install and Configure the Default Application</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0619-111">Configura il client App-V per usare l'App-V Streaming Server o un altro server per lo streaming tramite le <strong> impostazioni di ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> e <strong> OSDSourceRoot </strong> .</span><span class="sxs-lookup"><span data-stu-id="d0619-111">Configure the App-V Client to use the App-V Streaming Server or other server for streaming by means of the <strong>ApplicationSourceRoot</strong>, <strong>IconSourceRoot</strong>, and <strong>OSDSourceRoot</strong> settings.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)"><span data-ttu-id="d0619-112">Come configurare il client per il recupero del pacchetto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="d0619-112">How to Configure the Client for Application Package Retrieval</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d0619-113">Informazioni su come usare la versione del file MSI dei pacchetti di applicazioni sequenziate per la distribuzione offline.</span><span class="sxs-lookup"><span data-stu-id="d0619-113">Understand how to use the .msi file version of sequenced application packages for offline deployment.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)"><span data-ttu-id="d0619-114">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="d0619-114">How to Publish a Virtual Application on the Client</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d0619-115">Opzionale Configurare il mirroring del database di SQL Server per il database App-V.</span><span class="sxs-lookup"><span data-stu-id="d0619-115">(Optional) Configure SQL Server database mirroring for the App-V database.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)"><span data-ttu-id="d0619-116">Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V</span><span class="sxs-lookup"><span data-stu-id="d0619-116">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d0619-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0619-117">Related topics</span></span>


[<span data-ttu-id="d0619-118">Elenchi di controllo per la distribuzione e l'aggiornamento di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="d0619-118">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





