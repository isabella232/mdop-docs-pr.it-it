---
title: Configurare la notifica di posta elettronica
description: Configurare la notifica di posta elettronica
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819005"
---
# <span data-ttu-id="777e5-103">Configurare la notifica di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="777e5-103">Configure E-Mail Notification</span></span>


<span data-ttu-id="777e5-104">Quando un editor o un revisore tenta di creare, distribuire o eliminare un oggetto Criteri di gruppo, una richiesta di questa azione viene inviata a un indirizzo di posta elettronica o indirizzi designati in modo che un responsabile approvazione possa valutare la richiesta e implementarla o negarla.</span><span class="sxs-lookup"><span data-stu-id="777e5-104">When an Editor or a Reviewer attempts to create, deploy, or delete a Group Policy Object (GPO), a request for this action is sent to a designated e-mail address or addresses so that an Approver can evaluate the request and implement or deny it.</span></span> <span data-ttu-id="777e5-105">Puoi determinare l'indirizzo di posta elettronica o gli indirizzi a cui vengono inviate le notifiche, nonché l'alias da cui vengono inviate le notifiche.</span><span class="sxs-lookup"><span data-stu-id="777e5-105">You determine the e-mail address or addresses to which notifications are sent, as well as the alias from which notifications are sent.</span></span>

<span data-ttu-id="777e5-106">Per completare questa procedura è necessario un account utente con il ruolo amministratore Advanced Group Policy Manager (controllo completo) o le autorizzazioni necessarie in Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="777e5-106">A user account with the AGPM Administrator (Full Control) role or necessary permissions in Advanced Group Policy Management (AGPM) is required to complete this procedure.</span></span> <span data-ttu-id="777e5-107">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="777e5-107">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="777e5-108">Per configurare la notifica tramite posta elettronica per Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="777e5-108">To configure e-mail notification for AGPM</span></span>**

1.  <span data-ttu-id="777e5-109">Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.</span><span class="sxs-lookup"><span data-stu-id="777e5-109">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="777e5-110">Nel riquadro dei dettagli fare clic sulla scheda **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="777e5-110">In the details pane, click the **Domain Delegation** tab.</span></span>

3.  <span data-ttu-id="777e5-111">Nel campo **da indirizzo di posta elettronica** Digitare l'alias di posta elettronica per Advanced Group Policy Management da cui inviare le notifiche.</span><span class="sxs-lookup"><span data-stu-id="777e5-111">In the **From e-mail address** field, type the e-mail alias for AGPM from which notifications should be sent.</span></span>

4.  <span data-ttu-id="777e5-112">Nel campo **indirizzo di posta elettronica** Digitare un elenco delimitato da virgole di indirizzi di posta elettronica dei responsabili approvazione che devono ricevere le richieste di approvazione.</span><span class="sxs-lookup"><span data-stu-id="777e5-112">In the **To e-mail address** field, type a comma-delimited list of e-mail addresses of Approvers who should receive requests for approval.</span></span>

5.  <span data-ttu-id="777e5-113">Nel campo **server SMTP** Digitare un server di posta SMTP valido.</span><span class="sxs-lookup"><span data-stu-id="777e5-113">In the **SMTP server** field, type a valid SMTP mail server.</span></span>

6.  <span data-ttu-id="777e5-114">Nei campi **nome utente** e **password** digitare le credenziali di un utente con accesso al servizio SMTP.</span><span class="sxs-lookup"><span data-stu-id="777e5-114">In the **User name** and **Password** fields, type the credentials of a user with access to the SMTP service.</span></span>

7.  <span data-ttu-id="777e5-115">Fai clic su **Applica**.</span><span class="sxs-lookup"><span data-stu-id="777e5-115">Click **Apply**.</span></span>

### <span data-ttu-id="777e5-116">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="777e5-116">Additional considerations</span></span>

-   <span data-ttu-id="777e5-117">Per impostazione predefinita, è necessario essere un amministratore Advanced Group Policy Management (controllo completo) per eseguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="777e5-117">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="777e5-118">In particolare, devi avere il **contenuto dell'elenco** e modificare le autorizzazioni di **Opzioni** per il dominio.</span><span class="sxs-lookup"><span data-stu-id="777e5-118">Specifically, you must have **List Contents** and **Modify Options** permissions for the domain.</span></span>

-   <span data-ttu-id="777e5-119">La notifica tramite posta elettronica per Advanced Group Policy Management è un'impostazione a livello di dominio.</span><span class="sxs-lookup"><span data-stu-id="777e5-119">E-mail notification for AGPM is a domain-level setting.</span></span> <span data-ttu-id="777e5-120">È possibile specificare gli indirizzi di posta elettronica di approvazione o gli alias di posta elettronica della gestione avanzata nella scheda **delega** di ogni dominio oppure usare gli stessi indirizzi di posta elettronica in tutto l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="777e5-120">You can provide different Approver e-mail addresses or AGPM e-mail aliases on each domain's **Domain Delegation** tab, or use the same e-mail addresses throughout your environment.</span></span>

-   <span data-ttu-id="777e5-121">Per impostazione predefinita, i messaggi di posta elettronica inviati come risultato di azioni in Advanced Group Policy Management non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="777e5-121">By default, e-mail messages sent as a result of actions in Advanced Group Policy Management (AGPM) are not encrypted.</span></span> <span data-ttu-id="777e5-122">Puoi tuttavia configurare la sicurezza della posta elettronica per Advanced Group Policy Management usando le impostazioni del registro di sistema per specificare se usare la crittografia SSL (Secure Sockets Layer) e la porta SMTP da usare.</span><span class="sxs-lookup"><span data-stu-id="777e5-122">However, you can configure e-mail security for AGPM using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span> <span data-ttu-id="777e5-123">Per altre informazioni, vedere [configurare la sicurezza della posta elettronica per Advanced Group Policy Management](configure-e-mail-security-for-agpm-agpm30ops.md)</span><span class="sxs-lookup"><span data-stu-id="777e5-123">For more information, see [Configure E-Mail Security for AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)</span></span>

### <span data-ttu-id="777e5-124">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="777e5-124">Additional references</span></span>

-   [<span data-ttu-id="777e5-125">Configurazione di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="777e5-125">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





