---
title: Esaminare le impostazioni dell'oggetto Criteri di gruppo
description: Esaminare le impostazioni dell'oggetto Criteri di gruppo
author: dansimp
ms.assetid: e82570b2-d8ce-4bf0-8ad7-8910409f3041
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 681492f423266ce3722bb1a657ee93527c6bdd7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818335"
---
# <span data-ttu-id="d9483-103">Esaminare le impostazioni dell'oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="d9483-103">Review GPO Settings</span></span>


<span data-ttu-id="d9483-104">Puoi generare report basati su HTML e basato su XML per la revisione delle impostazioni in qualsiasi versione di un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d9483-104">You can generate HTML-based and XML-based reports for reviewing settings within any version of a Group Policy object (GPO).</span></span>

<span data-ttu-id="d9483-105">Per completare questa procedura è necessario un account utente con il ruolo di revisore, editor, approvatore o amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="d9483-105">A user account with the Reviewer, Editor, Approver, or AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="d9483-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="d9483-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="d9483-107">Per rivedere le impostazioni in qualsiasi versione di un GPO</span><span class="sxs-lookup"><span data-stu-id="d9483-107">To review settings in any version of a GPO</span></span>**

1.  <span data-ttu-id="d9483-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="d9483-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="d9483-109">Nella scheda **contenuto** del riquadro dei dettagli fare clic su una scheda per visualizzare gli oggetti Criteri di stato.</span><span class="sxs-lookup"><span data-stu-id="d9483-109">On the **Contents** tab in the details pane, click a tab to display GPOs.</span></span>

3.  <span data-ttu-id="d9483-110">Fare doppio clic sul GPO per visualizzarne la cronologia.</span><span class="sxs-lookup"><span data-stu-id="d9483-110">Double-click the GPO to display its history.</span></span>

4.  <span data-ttu-id="d9483-111">Fare clic con il pulsante destro del mouse sulla versione del GPO per la quale rivedere le impostazioni, fare clic su **Impostazioni**e quindi su **report HTML** o **report XML** per visualizzare un riepilogo delle impostazioni del GPO.</span><span class="sxs-lookup"><span data-stu-id="d9483-111">Right-click the GPO version for which to review the settings, click **Settings**, and then click **HTML Report** or **XML Report** to display a summary of the GPO's settings.</span></span>

### <span data-ttu-id="d9483-112">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="d9483-112">Additional considerations</span></span>

-   <span data-ttu-id="d9483-113">Per impostazione predefinita, per eseguire questa procedura è necessario essere un revisore, un editor, un approvatore o un amministratore Advanced Group Policy Management (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="d9483-113">By default, you must be a Reviewer, an Editor, an Approver, or an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="d9483-114">In particolare, è necessario disporre delle autorizzazioni per il **contenuto dell'elenco** e per le **impostazioni di lettura** per il GPO.</span><span class="sxs-lookup"><span data-stu-id="d9483-114">Specifically, you must have **List Contents** and **Read Settings** permissions for the GPO.</span></span> <span data-ttu-id="d9483-115">Inoltre, per visualizzare l'elenco degli oggetti Criteri di ricerca, è necessario avere l'autorizzazione **contenuto elenco** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="d9483-115">Also, to display the list of GPOs, you must have **List Contents** permission for the domain.</span></span>

### <span data-ttu-id="d9483-116">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="d9483-116">Additional references</span></span>

-   [<span data-ttu-id="d9483-117">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="d9483-117">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 




