---
title: Configurare la sicurezza della posta elettronica per Gestione avanzata Criteri di gruppo
description: Configurare la sicurezza della posta elettronica per Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 4850ed8e-a1c6-43f0-95c5-853aa66a94ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3694662fd0ed81edacd16cf55ac9760b1be2ba97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818986"
---
# <span data-ttu-id="8205e-103">Configurare la sicurezza della posta elettronica per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8205e-103">Configure E-Mail Security for AGPM</span></span>


<span data-ttu-id="8205e-104">Per impostazione predefinita, le notifiche tramite posta elettronica inviate a causa di azioni in Advanced Group Policy Management non vengono crittografate e vengono inviate tramite la porta SMTP 25.</span><span class="sxs-lookup"><span data-stu-id="8205e-104">By default, e-mail notifications sent because of actions in Advanced Group Policy Management (AGPM) are not encrypted and are sent through SMTP port 25.</span></span> <span data-ttu-id="8205e-105">Tuttavia, puoi configurare la sicurezza della posta elettronica per Advanced Group Policy Management usando le impostazioni del registro di sistema per specificare se usare la crittografia SSL (Secure Sockets Layer) e la porta SMTP da usare.</span><span class="sxs-lookup"><span data-stu-id="8205e-105">However, you can configure e-mail security for AGPM by using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span>

<span data-ttu-id="8205e-106">Crittografando le notifiche tramite posta elettronica Advanced Group Policy Management, è possibile proteggere meglio quelle che potrebbero rivelare informazioni riservate sulla sicurezza dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="8205e-106">By encrypting AGPM e-mail notifications, you can better protect those that could reveal sensitive information about your organization’s security.</span></span> <span data-ttu-id="8205e-107">È consigliabile crittografare le notifiche tramite posta elettronica quando vengono inoltrate tramite server di posta remoti e possono essere richieste da alcune normative di conformità.</span><span class="sxs-lookup"><span data-stu-id="8205e-107">Encrypting e-mail notifications is recommended when they are being relayed through remote mail servers, and may be required by some compliance regulations.</span></span>

<span data-ttu-id="8205e-108">**Attenzione**  La modifica in modo non corretto del registro di sistema può danneggiare gravemente il computer.</span><span class="sxs-lookup"><span data-stu-id="8205e-108">**Caution** Incorrectly editing the registry may severely damage your system.</span></span> <span data-ttu-id="8205e-109">Prima di apportare modifiche al registro di sistema, è consigliabile eseguire il backup di tutti i dati valutati nel computer.</span><span class="sxs-lookup"><span data-stu-id="8205e-109">Before making changes to the registry, you should back up any valued data on the computer.</span></span>

 

<span data-ttu-id="8205e-110">Un account utente con il ruolo amministratore Advanced Group Policy Management (controllo completo), l'account utente dell'approvatore che ha creato l'oggetto Criteri di gruppo usato in queste procedure o un account utente che disponga delle autorizzazioni necessarie in Advanced Group Policy Management è necessario per completare queste procedure.</span><span class="sxs-lookup"><span data-stu-id="8205e-110">A user account that has the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account that has the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="8205e-111">Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="8205e-111">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="8205e-112">Per configurare la sicurezza della posta elettronica per Advanced Group Policy con preferenze di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8205e-112">To configure e-mail security for AGPM by using Group Policy preferences</span></span>**

1.  <span data-ttu-id="8205e-113">Nell'albero della **console Gestione criteri di gruppo** modificare un GPO applicato a tutti i server Advanced Group Policy Management per cui si vuole configurare la sicurezza della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="8205e-113">In the **Group Policy Management Console** tree, edit a GPO that is applied to all AGPM Servers for which you want to configure e-mail security.</span></span> <span data-ttu-id="8205e-114">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8205e-114">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

2.  <span data-ttu-id="8205e-115">Nella finestra **Editor gestione criteri di gruppo** espandere la **configurazione del computer**, le **Preferenze**, **le impostazioni di Windows**e le cartelle **del registro di sistema** .</span><span class="sxs-lookup"><span data-stu-id="8205e-115">In the **Group Policy Management Editor** window, expand the **Computer Configuration**, **Preferences**, **Windows Settings**, and **Registry** folders.</span></span>

3.  <span data-ttu-id="8205e-116">Nell'albero della console fare clic con il pulsante destro del mouse su **Registro**, scegliere **nuovo**, fare clic su **elemento raccolta**e quindi digitare **sicurezza della posta elettronica Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="8205e-116">In the console tree, right-click **Registry**, point to **New**, click **Collection Item**, and type **AGPM e-mail security**.</span></span>

4.  <span data-ttu-id="8205e-117">Creare un elemento preferenza del registro di sistema per attivare la crittografia:</span><span class="sxs-lookup"><span data-stu-id="8205e-117">Create a Registry preference item to turn on encryption:</span></span>

    1.  <span data-ttu-id="8205e-118">Nell'albero della console fare clic con il pulsante destro del mouse sulla **sicurezza della posta elettronica avanzata**, scegliere **nuovo**e quindi **elemento del registro di sistema**.</span><span class="sxs-lookup"><span data-stu-id="8205e-118">In the console tree, right-click **AGPM e-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="8205e-119">Nella finestra di dialogo **nuove proprietà del registro di sistema** selezionare l'azione di **aggiornamento** .</span><span class="sxs-lookup"><span data-stu-id="8205e-119">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="8205e-120">Per **hive**selezionare **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="8205e-120">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="8205e-121">Per il **percorso chiave**digitare **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="8205e-121">For **Key Path**, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="8205e-122">Per **nome valore**digitare **EncryptSmtp**.</span><span class="sxs-lookup"><span data-stu-id="8205e-122">For **Value name**, type **EncryptSmtp**.</span></span>

    6.  <span data-ttu-id="8205e-123">Per **tipo di valore**selezionare **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="8205e-123">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="8205e-124">Per **base**selezionare **decimale**e per **i dati di valore**digitare **1** per usare la crittografia SSL oppure **0** per consentire l'invio della posta elettronica senza crittografia.</span><span class="sxs-lookup"><span data-stu-id="8205e-124">For **Base**, select **Decimal**, and for **Value data**, type **1** to use SSL encryption, or **0** to let e-mail to be sent without encryption.</span></span> <span data-ttu-id="8205e-125">Per impostazione predefinita, il messaggio di posta elettronica viene inviato senza crittografia.</span><span class="sxs-lookup"><span data-stu-id="8205e-125">By default, e-mail is sent without encryption.</span></span>

    8.  <span data-ttu-id="8205e-126">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8205e-126">Click **OK**.</span></span>

5.  <span data-ttu-id="8205e-127">Creare un elemento preferenza del registro di sistema per specificare la porta SMTP:</span><span class="sxs-lookup"><span data-stu-id="8205e-127">Create a Registry preference item to specify the SMTP port:</span></span>

    1.  <span data-ttu-id="8205e-128">Nell'albero della console fare clic con il pulsante destro del mouse sulla **sicurezza della posta elettronica avanzata**, scegliere **nuovo**e quindi **elemento del registro di sistema**.</span><span class="sxs-lookup"><span data-stu-id="8205e-128">In the console tree, right-click **AGPM E-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="8205e-129">Nella finestra di dialogo **nuove proprietà del registro di sistema** selezionare l'azione di **aggiornamento** .</span><span class="sxs-lookup"><span data-stu-id="8205e-129">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="8205e-130">Per **hive**selezionare **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="8205e-130">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="8205e-131">Per la finestra di dialogo **percorso chiave** digitare **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="8205e-131">For **Key Path** dialog box, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="8205e-132">Per **nome valore**digitare **SmtpPort**.</span><span class="sxs-lookup"><span data-stu-id="8205e-132">For **Value name**, type **SmtpPort**.</span></span>

    6.  <span data-ttu-id="8205e-133">Per **tipo di valore**selezionare **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="8205e-133">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="8205e-134">Per **base**selezionare **decimale**e per i **dati di valore**digitare un numero di porta per la porta SMTP.</span><span class="sxs-lookup"><span data-stu-id="8205e-134">For **Base**, select **Decimal**, and for **Value data**, type a port number for the SMTP port.</span></span> <span data-ttu-id="8205e-135">Per impostazione predefinita, la porta SMTP è la porta 25 se la crittografia non è abilitata o porta 587 se è abilitata la crittografia SSL.</span><span class="sxs-lookup"><span data-stu-id="8205e-135">By default, the SMTP port is port 25 if encryption is not enabled or port 587 if SSL encryption is enabled.</span></span>

    8.  <span data-ttu-id="8205e-136">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="8205e-136">Click **OK**.</span></span>

6.  <span data-ttu-id="8205e-137">Chiudere la finestra **Editor gestione criteri di gruppo** e quindi archiviare e distribuire il GPO.</span><span class="sxs-lookup"><span data-stu-id="8205e-137">Close the **Group Policy Management Editor** window, and then check in and deploy the GPO.</span></span> <span data-ttu-id="8205e-138">Per altre informazioni, vedere [distribuire un oggetto Criteri](deploy-a-gpo-agpm30ops.md)di ricerca.</span><span class="sxs-lookup"><span data-stu-id="8205e-138">For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="8205e-139">Considerazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="8205e-139">Additional considerations</span></span>

-   <span data-ttu-id="8205e-140">È necessario essere in grado di modificare e distribuire un oggetto Criteri di gruppo per configurare le impostazioni del registro di sistema usando le preferenze dei criteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="8205e-140">You must be able to edit and deploy a GPO to configure registry settings by using Group Policy Preferences.</span></span> <span data-ttu-id="8205e-141">Per altre informazioni, vedere [modifica di un oggetto Criteri](editing-a-gpo-agpm30ops.md) di ricerca e [distribuzione di un GPO](deploy-a-gpo-agpm30ops.md) .</span><span class="sxs-lookup"><span data-stu-id="8205e-141">See [Editing a GPO](editing-a-gpo-agpm30ops.md) and [Deploy a GPO](deploy-a-gpo-agpm30ops.md) for additional detail.</span></span>

### <span data-ttu-id="8205e-142">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="8205e-142">Additional references</span></span>

-   [<span data-ttu-id="8205e-143">Configurazione di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8205e-143">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





