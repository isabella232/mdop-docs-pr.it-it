---
title: Impostazioni di visibilità delle funzionalità
description: Impostazioni di visibilità delle funzionalità
author: dansimp
ms.assetid: 9db2ba03-fb75-4f95-9138-ec89b9fc8d01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 26f19895d0a9163885779688ba7d89f6d16f2a17
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820806"
---
# <span data-ttu-id="bcb0f-103">Impostazioni di visibilità delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="bcb0f-103">Feature Visibility Settings</span></span>


<span data-ttu-id="bcb0f-104">Le impostazioni del modello amministrativo per gestione avanzata Criteri di gruppo consentono di configurare centralmente la visibilità del nodo di **controllo delle modifiche** e della scheda **cronologia** per gli amministratori dei criteri di gruppo a cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure the visibility of the **Change Control** node and **History** tab for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="bcb0f-105">Le impostazioni seguenti sono disponibili in utenti Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console \ \ Restricted/consentiti degli snap-in Snap-ins\\Extension nell' **Editor oggetti Criteri di gruppo** durante la modifica di un oggetto Criteri di gruppo in console Gestione criteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\Microsoft Management Console\\Restricted/Permitted Snap-ins\\Extension Snap-ins in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="bcb0f-106">Se il percorso non è visibile, fare clic con il pulsante destro del mouse su **modelli amministrativi**e quindi aggiungere il modello Advanced Group Policy Management. admx o Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bcb0f-107">Impostazione</span><span class="sxs-lookup"><span data-stu-id="bcb0f-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="bcb0f-108">Effetto</span><span class="sxs-lookup"><span data-stu-id="bcb0f-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bcb0f-109">Controllo delle modifiche per Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="bcb0f-109">AGPM Change Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bcb0f-110">Se abilitato o non configurato, il <strong> nodo cambia controllo </strong> è visibile in GPMC.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-110">If enabled or not configured, the <strong>Change Control</strong> node is visible in the GPMC.</span></span></p>
<p><span data-ttu-id="bcb0f-111">Se disabilitato, il <strong> nodo cambia controllo </strong> non è visibile in GPMC.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-111">If disabled, the <strong>Change Control</strong> node is not visible in the GPMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="bcb0f-112">Estensione del collegamento Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="bcb0f-112">AGPM Link Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bcb0f-113">Se abilitata o non configurata, <strong> </strong> nella GPMC per ogni GPO collegato viene visualizzata una scheda cronologia.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-113">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each linked GPO.</span></span></p>
<p><span data-ttu-id="bcb0f-114">Se disabilitata, <strong> la </strong> scheda cronologia non è visibile per i GPO collegati.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-114">If disabled, the <strong>History</strong> tab is not visible for linked GPOs.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bcb0f-115">Estensione GPO in Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="bcb0f-115">AGPM GPO Extension</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bcb0f-116">Se abilitata o non configurata, <strong> </strong> nella GPMC per ogni GPO viene visualizzata una scheda cronologia.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-116">If enabled or not configured, a <strong>History</strong> tab appears in the GPMC for each GPO.</span></span></p>
<p><span data-ttu-id="bcb0f-117">Se disabilitata, <strong> la </strong> scheda cronologia non è visibile per gli oggetti Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="bcb0f-117">If disabled, the <strong>History</strong> tab is not visible for GPOs.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="bcb0f-118">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="bcb0f-118">Additional references</span></span>

-   [<span data-ttu-id="bcb0f-119">Impostazioni del modello amministrativo</span><span class="sxs-lookup"><span data-stu-id="bcb0f-119">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





