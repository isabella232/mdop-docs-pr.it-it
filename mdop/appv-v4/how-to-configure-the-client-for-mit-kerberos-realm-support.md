---
title: Come configurare il client per il supporto per le aree di autenticazione MIT Kerberos
description: Come configurare il client per il supporto per le aree di autenticazione MIT Kerberos
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817815"
---
# <span data-ttu-id="311ae-103">Come configurare il client per il supporto per le aree di autenticazione MIT Kerberos</span><span class="sxs-lookup"><span data-stu-id="311ae-103">How to Configure the Client for MIT Kerberos Realm Support</span></span>


<span data-ttu-id="311ae-104">In Application Virtualization (App-V) 4,5 SP1 è stato aggiunto il supporto per gli ambiti di autenticazione Kerberos MIT.</span><span class="sxs-lookup"><span data-stu-id="311ae-104">In Application Virtualization (App-V) 4.5 SP1, support was added for MIT Kerberos realms.</span></span> <span data-ttu-id="311ae-105">Questo argomento fornisce informazioni dettagliate su come abilitare tale supporto.</span><span class="sxs-lookup"><span data-stu-id="311ae-105">This topic provides detailed information on how to enable that support.</span></span>

**<span data-ttu-id="311ae-106">Per abilitare il supporto per gli ambiti di autenticazione Kerberos MIT</span><span class="sxs-lookup"><span data-stu-id="311ae-106">To enable support for MIT Kerberos Realms</span></span>**

-   <span data-ttu-id="311ae-107">Creare una nuova chiave del registro di sistema denominata **UseMITKerberos** di tipo DWORD, come indicato di seguito, quindi impostarla su un valore pari a 1.</span><span class="sxs-lookup"><span data-stu-id="311ae-107">Create a new registry key named **UseMitKerberos** of type DWORD, as follows, and then set it to a value of 1.</span></span>

    <span data-ttu-id="311ae-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span><span class="sxs-lookup"><span data-stu-id="311ae-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span></span>

 

 





