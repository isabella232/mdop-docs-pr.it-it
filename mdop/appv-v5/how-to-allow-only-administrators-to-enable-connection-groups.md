---
title: Come consentire solo agli amministratori l'abilitazione dei gruppi di connessione
description: Come consentire solo agli amministratori l'abilitazione dei gruppi di connessione
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805745"
---
# <span data-ttu-id="31536-103">Come consentire solo agli amministratori l'abilitazione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="31536-103">How to Allow Only Administrators to Enable Connection Groups</span></span>


<span data-ttu-id="31536-104">Puoi configurare il client App-V in modo che solo gli amministratori (non gli utenti finali) possano abilitare o disabilitare i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="31536-104">You can configure the App-V client so that only administrators (not end users) can enable or disable connection groups.</span></span> <span data-ttu-id="31536-105">Nelle versioni precedenti di App-V non è stato possibile impedire agli utenti finali di eseguire queste attività.</span><span class="sxs-lookup"><span data-stu-id="31536-105">In earlier versions of App-V, you could not prevent end users from performing these tasks.</span></span>

<span data-ttu-id="31536-106">**Nota** 
 **Questa funzionalità è supportata a partire da App-V 5,0 SP3.**</span><span class="sxs-lookup"><span data-stu-id="31536-106">**Note**
**This feature is supported starting in App-V 5.0 SP3.**</span></span>

 

<span data-ttu-id="31536-107">Usa uno dei metodi seguenti per consentire solo agli amministratori di abilitare o disabilitare i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="31536-107">Use one of the following methods to allow only administrators to enable or disable connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="31536-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="31536-108">Method</span></span></th>
<th align="left"><span data-ttu-id="31536-109">Passaggi</span><span class="sxs-lookup"><span data-stu-id="31536-109">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="31536-110">Impostazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="31536-110">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="31536-111">Abilitare l'impostazione di criteri di gruppo "Richiedi pubblica come amministratore", disponibile nel nodo oggetto Criteri di gruppo seguente:</span><span class="sxs-lookup"><span data-stu-id="31536-111">Enable the “Require publish as administrator” Group Policy setting, which is located in the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="31536-112">Criteri di configurazione del computer &gt; &gt; modelli amministrativi &gt; &gt; App-V &gt; Publishing</span><span class="sxs-lookup"><span data-stu-id="31536-112">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="31536-113">Cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="31536-113">PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="31536-114">Eseguire il <strong> cmdlet Set-AppvClientConfiguration </strong> con il <strong> parametro – RequirePublishAsAdmin </strong> .</span><span class="sxs-lookup"><span data-stu-id="31536-114">Run the <strong>Set-AppvClientConfiguration</strong> cmdlet with the <strong>–RequirePublishAsAdmin</strong> parameter.</span></span></p>
<p><span data-ttu-id="31536-115">Valori dei parametri:</span><span class="sxs-lookup"><span data-stu-id="31536-115">Parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="31536-116">0-falso</span><span class="sxs-lookup"><span data-stu-id="31536-116">0 - False</span></span></p></li>
<li><p><span data-ttu-id="31536-117">1-vero</span><span class="sxs-lookup"><span data-stu-id="31536-117">1 - True</span></span></p></li>
</ul>
<p><strong><span data-ttu-id="31536-118">Esempio: </strong> : set-AppvClientConfiguration-RequirePublishAsAdmin1</span><span class="sxs-lookup"><span data-stu-id="31536-118">Example:</strong>: Set-AppvClientConfiguration –RequirePublishAsAdmin1</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="31536-119">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="31536-119">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="31536-120">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="31536-120">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="31536-121">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="31536-121">Got an App-V issue?</span></span>** <span data-ttu-id="31536-122">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="31536-122">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="31536-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31536-123">Related topics</span></span>


[<span data-ttu-id="31536-124">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="31536-124">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





