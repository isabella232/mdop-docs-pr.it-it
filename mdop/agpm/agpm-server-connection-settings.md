---
title: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
description: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804665"
---
# <span data-ttu-id="458ae-103">Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="458ae-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="458ae-104">È possibile usare le impostazioni dei modelli amministrativi per la gestione avanzata dei criteri di gruppo per configurare centralmente le connessioni del server Advanced Group Policy Management per gli amministratori dei criteri di gruppo a cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="458ae-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="458ae-105">Le impostazioni seguenti sono disponibili in utenti Configuration\\Administrative Templates\\Windows Components\\AGPM durante la modifica di un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="458ae-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span> <span data-ttu-id="458ae-106">Se il percorso non è visibile, fare clic con il pulsante destro del mouse su **modelli amministrativi**e quindi aggiungere il modello Advanced Group Policy Management. admx o Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="458ae-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="458ae-107">Impostazione</span><span class="sxs-lookup"><span data-stu-id="458ae-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="458ae-108">Effetto</span><span class="sxs-lookup"><span data-stu-id="458ae-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="458ae-109">Server Advanced Group Policy Management (tutti i domini)</span><span class="sxs-lookup"><span data-stu-id="458ae-109">AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="458ae-110">Se abilitata, questa impostazione Configura centralmente una connessione al server Advanced Group Policy per l'uso da parte di tutti i domini e Disabilita le impostazioni nella <strong> scheda Server Advanced Group Policy Management </strong> per gli amministratori dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="458ae-110">If enabled, this setting centrally configures one AGPM Server connection for use by all domains and disables the settings on the <strong>AGPM Server</strong> tab for Group Policy administrators.</span></span> <span data-ttu-id="458ae-111">Per più server Advanced Group Policy Management, configurare questa impostazione con un server predefinito e quindi configurare l' <strong> impostazione del server Advanced Group Policy Management </strong> nel modello amministrativo per eseguire l'override di questo server per altri domini.</span><span class="sxs-lookup"><span data-stu-id="458ae-111">For multiple AGPM Servers, configure this setting with a default server and then configure the <strong>AGPM Server</strong> setting in the Administrative template to override this server for other domains.</span></span></p>
<p><span data-ttu-id="458ae-112">Se disabilitata o non configurata, ogni amministratore dei criteri di gruppo deve selezionare il server Advanced Group Policy Management da visualizzare per ogni dominio nella <strong> scheda Server Advanced Group Policy Management </strong></span><span class="sxs-lookup"><span data-stu-id="458ae-112">If disabled or not configured, each Group Policy administrator must select the AGPM Server to display for each domain on the <strong>AGPM Server</strong> tab in AGPM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="458ae-113">Server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="458ae-113">AGPM Server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="458ae-114">Se abilitata, questa impostazione Configura centralmente più server di Advanced Group Policy Management specifici del dominio, eseguendo l'override del <strong> server Advanced Group Policy Management (tutti i domini) </strong> nel modello amministrativo.</span><span class="sxs-lookup"><span data-stu-id="458ae-114">If enabled, this setting centrally configures multiple domain-specific AGPM Servers, overriding the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span> <span data-ttu-id="458ae-115">Se l'ambiente richiede solo un singolo server Advanced Group Policy Management, usare solo l' <strong> impostazione server Advanced Group Policy Management (tutti i domini) </strong> nel modello amministrativo.</span><span class="sxs-lookup"><span data-stu-id="458ae-115">If your environment requires only a single AGPM Server, use only the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span></p>
<p><span data-ttu-id="458ae-116">Se disabilitata o non configurata, l' <strong> impostazione del server Advanced Group Policy Management (tutti i domini) </strong> nel modello amministrativo configura la connessione al server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="458ae-116">If disabled or not configured, the <strong>AGPM Server (all domains)</strong> setting in the Administrative template configures the AGPM Server connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="458ae-117">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="458ae-117">Additional references</span></span>

-   [<span data-ttu-id="458ae-118">Impostazioni del modello amministrativo</span><span class="sxs-lookup"><span data-stu-id="458ae-118">Administrative Template Settings</span></span>](administrative-template-settings.md)

-   [<span data-ttu-id="458ae-119">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="458ae-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





