---
title: Configurare la notifica di posta elettronica
description: Configurare la notifica di posta elettronica
author: dansimp
ms.assetid: 6e152de0-4376-4963-8d1a-3e7f5866d30f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 46e8d00c2446a0185de30bbd1f39a7e3eaf90080
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818976"
---
# <span data-ttu-id="2a3a4-103">Configurare la notifica di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="2a3a4-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="2a3a4-104">Quando un editor o un revisore tenta di creare, distribuire o eliminare un oggetto Criteri di gruppo, una richiesta di questa azione viene inviata a un indirizzo di posta elettronica o indirizzi designati in modo che un responsabile approvazione possa valutare la richiesta e implementarla o negarla.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="2a3a4-105">Puoi determinare l'indirizzo di posta elettronica o gli indirizzi a cui vengono inviate le notifiche, nonché l'alias da cui vengono inviate le notifiche.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="2a3a4-106">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie per la gestione di criteri di gruppo avanzati.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management is required to complete this procedure.</span></span> <span data-ttu-id="2a3a4-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2a3a4-108">Per configurare la notifica tramite posta elettronica per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="2a3a4-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="2a3a4-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="2a3a4-110">Nel riquadro dei dettagli fare clic sulla scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="2a3a4-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="2a3a4-111">Nel campo **da** Digitare l'alias di posta elettronica per Advanced Group Policy Management da cui inviare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-111">In the **From** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="2a3a4-112">Nel campo **a** Digitare un elenco delimitato da virgole di indirizzi di posta elettronica dei responsabili approvazione che devono ricevere le richieste di approvazione.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-112">In the **To** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="2a3a4-113">Nel campo **server SMTP** Digitare un server di posta SMTP valido.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="2a3a4-114">Nei campi **nome utente** e **password** digitare le credenziali di un utente con accesso al servizio SMTP.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="2a3a4-115">Fai clic su **Applica**.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-115">Click **Apply**.</span></span>

### <span data-ttu-id="2a3a4-116">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="2a3a4-116">Additional considerations</span></span>

-   <span data-ttu-id="2a3a4-117">Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="2a3a4-118">In particolare, devi avere il **contenuto dell'elenco** e modificare le autorizzazioni di **Opzioni** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="2a3a4-119">La notifica tramite posta elettronica per Advanced Group Policy Management è un'impostazione a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="2a3a4-120">È possibile specificare gli indirizzi di posta elettronica di approvazione o gli alias di posta elettronica della gestione avanzata nella scheda **delega** di ogni dominio oppure usare gli stessi indirizzi di posta elettronica in tutto l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="2a3a4-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

### <span data-ttu-id="2a3a4-121">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="2a3a4-121">Additional references</span></span>

-   [<span data-ttu-id="2a3a4-122">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2a3a4-122">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





