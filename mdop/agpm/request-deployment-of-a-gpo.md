---
title: Richiedere la distribuzione di un oggetto Criteri di gruppo
description: Richiedere la distribuzione di un oggetto Criteri di gruppo
author: dansimp
ms.assetid: 9aa9af29-4754-4f72-b624-bb3e1087cbe1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a9e5fdbbd352adb6d542932c7180c513cfac8b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820376"
---
# <span data-ttu-id="9fc15-103">Richiedere la distribuzione di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="9fc15-103">Request Deployment of a GPO</span></span>


<span data-ttu-id="9fc15-104">Dopo aver modificato e archiviato un oggetto Criteri di gruppo, distribuire il GPO, in modo che diventi effettivo nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="9fc15-104">After you have modified and checked in a Group Policy object (GPO), deploy the GPO, so it will take effect in the production environment.</span></span>

<span data-ttu-id="9fc15-105">Per completare questa procedura è necessario un account utente con il ruolo di editor o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="9fc15-105">A user account with the Editor role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="9fc15-106">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="9fc15-106">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9fc15-107">Per richiedere la distribuzione di un GPO all'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="9fc15-107">To request the deployment of a GPO to the production environment</span></span>**

1.  <span data-ttu-id="9fc15-108">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="9fc15-108">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9fc15-109">Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **controllati** per visualizzare gli oggetti Criteri di controllo controllati.</span><span class="sxs-lookup"><span data-stu-id="9fc15-109">On the **Contents** tab in the details pane, click the **Controlled** tab to display the controlled GPOs.</span></span>

3.  <span data-ttu-id="9fc15-110">Fare clic con il pulsante destro del mouse sull'oggetto Criteri di distribuzione e quindi scegliere **Distribuisci**.</span><span class="sxs-lookup"><span data-stu-id="9fc15-110">Right-click the GPO to be deployed, and then click **Deploy**.</span></span>

4.  <span data-ttu-id="9fc15-111">A meno che non si sia un approvatore o un amministratore della Advanced Group Policy Management o si disponga di autorizzazioni speciali per distribuire GPO, è necessario inviare una richiesta di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9fc15-111">Unless you are an Approver or AGPM Administrator or have special permission to deploy GPOs, you must submit a request for deployment.</span></span> <span data-ttu-id="9fc15-112">Per ricevere una copia della richiesta, digitare l'indirizzo di posta elettronica nel campo **CC** .</span><span class="sxs-lookup"><span data-stu-id="9fc15-112">To receive a copy of the request, type your e-mail address in the **Cc** field.</span></span> <span data-ttu-id="9fc15-113">Digitare un commento da visualizzare nella **cronologia** per il GPO e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="9fc15-113">Type a comment to be displayed in the **History** for the GPO, and then click **Submit**.</span></span>

5.  <span data-ttu-id="9fc15-114">Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="9fc15-114">When the **Progress** window indicates that overall progress is complete, click **Close**.</span></span> <span data-ttu-id="9fc15-115">Il GPO viene visualizzato nell'elenco dei GPO nella scheda **in sospeso** . Quando un responsabile approvazione ha approvato la richiesta, il GPO verrà spostato dalla scheda **in sospeso** alla scheda **controllata** e sarà distribuito.</span><span class="sxs-lookup"><span data-stu-id="9fc15-115">The GPO is displayed on the list of GPOs on the **Pending** tab. When an Approver has approved your request, the GPO will be moved from the **Pending** tab to the **Controlled** tab and be deployed.</span></span>

### <span data-ttu-id="9fc15-116">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="9fc15-116">Additional considerations</span></span>

-   <span data-ttu-id="9fc15-117">Per impostazione predefinita, è necessario essere un editor per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="9fc15-117">By default, you must be an Editor to perform this procedure.</span></span> <span data-ttu-id="9fc15-118">In particolare, devi avere le autorizzazioni di **elenco** e **Modifica impostazioni** per l'oggetto Criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9fc15-118">Specifically, you must have **List Contents** and **Edit Settings** permissions for the GPO.</span></span>

-   <span data-ttu-id="9fc15-119">Per ritirare la richiesta prima che sia stata approvata, fare clic sulla scheda **in sospeso** . fare clic con il pulsante destro del mouse sul GPO e quindi scegliere **ritira**.</span><span class="sxs-lookup"><span data-stu-id="9fc15-119">To withdraw your request before it has been approved, click the **Pending** tab. Right-click the GPO, and then click **Withdraw**.</span></span> <span data-ttu-id="9fc15-120">Il GPO verrà restituito alla scheda **controllato** .</span><span class="sxs-lookup"><span data-stu-id="9fc15-120">The GPO will be returned to the **Controlled** tab.</span></span>

### <span data-ttu-id="9fc15-121">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="9fc15-121">Additional references</span></span>

-   [<span data-ttu-id="9fc15-122">Modifica di un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="9fc15-122">Editing a GPO</span></span>](editing-a-gpo.md)

 

 





