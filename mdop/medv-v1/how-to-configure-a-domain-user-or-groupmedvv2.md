---
title: Come configurare un utente o un gruppo di dominio
description: Come configurare un utente o un gruppo di dominio
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827196"
---
# <span data-ttu-id="67836-103">Come configurare un utente o un gruppo di dominio</span><span class="sxs-lookup"><span data-stu-id="67836-103">How to Configure a Domain User or Group</span></span>


<span data-ttu-id="67836-104">Le impostazioni di distribuzione consentono di controllare gli utenti o i gruppi che possono accedere all'area di lavoro MED-V, nonché per quanto tempo può essere utilizzata l'area di lavoro MED-V e se può essere usata offline.</span><span class="sxs-lookup"><span data-stu-id="67836-104">The deployment settings enable you to control which users or groups can access the MED-V workspace, as well as how long the MED-V workspace can be utilized and whether it can be used offline.</span></span> <span data-ttu-id="67836-105">È anche possibile configurare altre regole per controllare l'accesso tra l'area di lavoro MED-V e l'host.</span><span class="sxs-lookup"><span data-stu-id="67836-105">You can also configure additional rules to control access between the MED-V workspace and the host.</span></span>

<span data-ttu-id="67836-106">Tutte le autorizzazioni dell'area di lavoro MED-V sono configurate nel modulo **criteri** nella scheda **distribuzione** .</span><span class="sxs-lookup"><span data-stu-id="67836-106">All MED-V workspace permissions are configured in the **Policy** module, on the **Deployment** tab.</span></span>

<span data-ttu-id="67836-107">Per consentire agli utenti di usare l'area di lavoro MED-V, è necessario prima di tutto aggiungere utenti o gruppi di dominio alle autorizzazioni dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67836-107">To allow users to utilize the MED-V workspace, you must first add domain users or groups to the MED-V workspace permissions.</span></span> <span data-ttu-id="67836-108">Puoi quindi impostare le autorizzazioni per ogni utente o gruppo.</span><span class="sxs-lookup"><span data-stu-id="67836-108">You can then set permissions for each user or group.</span></span>

## <span data-ttu-id="67836-109">Come aggiungere un utente o un gruppo di dominio</span><span class="sxs-lookup"><span data-stu-id="67836-109">How to Add a Domain User or Group</span></span>


**<span data-ttu-id="67836-110">Per aggiungere un utente o un gruppo di dominio</span><span class="sxs-lookup"><span data-stu-id="67836-110">To add a domain user or group</span></span>**

1.  <span data-ttu-id="67836-111">Nella finestra **utenti/gruppi** fare clic su **Aggiungi.**</span><span class="sxs-lookup"><span data-stu-id="67836-111">In the **Users / Groups** window, click **Add.**</span></span>

2.  <span data-ttu-id="67836-112">Nella finestra di dialogo **Immetti nomi utente o di gruppo** selezionare utenti o gruppi di dominio eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="67836-112">In the **Enter User or Group names** dialog box, select domain users or groups by doing one of the following:</span></span>

    -   <span data-ttu-id="67836-113">Nel campo **Immetti nomi utente o gruppo** Digitare un utente o un gruppo esistente nel dominio o come utente o gruppo locale nel computer.</span><span class="sxs-lookup"><span data-stu-id="67836-113">In the **Enter User or Group names** field, type a user or group that exists in the domain or as a local user or group on the computer.</span></span> <span data-ttu-id="67836-114">Quindi fare clic su **Controlla nomi** per risolverlo con il nome completo esistente.</span><span class="sxs-lookup"><span data-stu-id="67836-114">Then click **Check Names** to resolve it to the full existent name.</span></span>

    -   <span data-ttu-id="67836-115">Fare clic su **trova** per aprire la finestra di dialogo standard **Seleziona utenti o gruppi** .</span><span class="sxs-lookup"><span data-stu-id="67836-115">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="67836-116">Quindi Seleziona utenti o gruppi di dominio.</span><span class="sxs-lookup"><span data-stu-id="67836-116">Then select domain users or groups.</span></span>

3.  <span data-ttu-id="67836-117">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="67836-117">Click **OK**.</span></span>

    <span data-ttu-id="67836-118">Gli utenti o i gruppi di dominio vengono aggiunti.</span><span class="sxs-lookup"><span data-stu-id="67836-118">The domain users or groups are added.</span></span>

    **<span data-ttu-id="67836-119">Nota</span><span class="sxs-lookup"><span data-stu-id="67836-119">Note</span></span>**  
    <span data-ttu-id="67836-120">Gli utenti provenienti da domini attendibili devono essere aggiunti manualmente.</span><span class="sxs-lookup"><span data-stu-id="67836-120">Users from trusted domains should be added manually.</span></span>



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## <span data-ttu-id="67836-121">Come rimuovere un utente o un gruppo di dominio</span><span class="sxs-lookup"><span data-stu-id="67836-121">How to Remove a Domain User or Group</span></span>


**<span data-ttu-id="67836-122">Per rimuovere un utente o un gruppo di dominio</span><span class="sxs-lookup"><span data-stu-id="67836-122">To remove a domain user or group</span></span>**

1.  <span data-ttu-id="67836-123">Nella finestra **utenti/gruppi** selezionare un utente o un gruppo.</span><span class="sxs-lookup"><span data-stu-id="67836-123">In the **Users / Groups** window, select a user or group.</span></span>

2.  <span data-ttu-id="67836-124">Fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="67836-124">Click **Remove**.</span></span>

    <span data-ttu-id="67836-125">L'utente o il gruppo viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="67836-125">The user or group is deleted.</span></span>

## <span data-ttu-id="67836-126">Come impostare le autorizzazioni per un utente o un gruppo</span><span class="sxs-lookup"><span data-stu-id="67836-126">How to Set Permissions for a User or a Group</span></span>


**<span data-ttu-id="67836-127">Per impostare le autorizzazioni per un utente o un gruppo</span><span class="sxs-lookup"><span data-stu-id="67836-127">To set permissions for a user or a group</span></span>**

1.  <span data-ttu-id="67836-128">Fare clic sull'utente o sul gruppo per cui si stanno impostando le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="67836-128">Click the user or group for which you are setting the permissions.</span></span>

2.  <span data-ttu-id="67836-129">Configurare le proprietà dell'area di lavoro MED-V come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="67836-129">Configure the MED-V workspace properties as described in the following table.</span></span>

3.  <span data-ttu-id="67836-130">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="67836-130">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="67836-131">Proprietà di distribuzione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="67836-131">Workspace Deployment Properties</span></span>**

<span data-ttu-id="67836-132">Descrizione *generale* della proprietà</span><span class="sxs-lookup"><span data-stu-id="67836-132">Property Description *General*</span></span>

<span data-ttu-id="67836-133">Abilitare l'area di lavoro per l' &lt; utente o il gruppo&gt;</span><span class="sxs-lookup"><span data-stu-id="67836-133">Enable Workspace for &lt;user or group&gt;</span></span>

<span data-ttu-id="67836-134">Selezionare questa casella di controllo per abilitare l'area di lavoro MED-V per l'utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="67836-134">Select this check box to enable the MED-V workspace for this user or group.</span></span>

<span data-ttu-id="67836-135">L'area di lavoro scade in questa data</span><span class="sxs-lookup"><span data-stu-id="67836-135">Workspace expires on this date</span></span>

<span data-ttu-id="67836-136">Selezionare questa casella di controllo per assegnare una data di scadenza per il set di autorizzazioni per l'utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="67836-136">Select this check box to assign an expiration date for the permissions set for this user or group.</span></span>

<span data-ttu-id="67836-137">Quando l'opzione è selezionata, la casella Data è abilitata.</span><span class="sxs-lookup"><span data-stu-id="67836-137">When selected, the date box is enabled.</span></span> <span data-ttu-id="67836-138">Impostare la data e le autorizzazioni scadono alla fine della data specificata.</span><span class="sxs-lookup"><span data-stu-id="67836-138">Set the date, and permissions will expire at the end of the date specified.</span></span>

<span data-ttu-id="67836-139">Il lavoro offline è limitato a</span><span class="sxs-lookup"><span data-stu-id="67836-139">Offline work is restricted to</span></span>

<span data-ttu-id="67836-140">Selezionare questa casella di controllo per assegnare un periodo di tempo in cui il criterio deve essere aggiornato per l'utente o il gruppo.</span><span class="sxs-lookup"><span data-stu-id="67836-140">Select this check box to assign a time period in which the policy must be refreshed for this user or group.</span></span> <span data-ttu-id="67836-141">Quando l'opzione è selezionata, la casella periodo di tempo è abilitata.</span><span class="sxs-lookup"><span data-stu-id="67836-141">When selected, the time period box is enabled.</span></span> <span data-ttu-id="67836-142">Impostare il numero di giorni o ore e alla fine del periodo di tempo specificato l'utente o il gruppo non sarà in grado di connettersi se il criterio non viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="67836-142">Set the number of days or hours, and at the end of the specified time period, the user or group will not be able to connect if the policy is not refreshed.</span></span>

<span data-ttu-id="67836-143">Opzioni di eliminazione dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="67836-143">Workspace deletion options</span></span>

<span data-ttu-id="67836-144">Fare clic per impostare le opzioni di eliminazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67836-144">Click to set the MED-V workspace deletion options.</span></span> <span data-ttu-id="67836-145">Per altre informazioni, vedere [come impostare le opzioni di eliminazione dell'area di lavoro MED-V](how-to-set-med-v-workspace-deletion-options.md).</span><span class="sxs-lookup"><span data-stu-id="67836-145">For more information, see [How to Set MED-V Workspace Deletion Options](how-to-set-med-v-workspace-deletion-options.md).</span></span>

*<span data-ttu-id="67836-146">Trasferimento dati</span><span class="sxs-lookup"><span data-stu-id="67836-146">Data Transfer</span></span>*

<span data-ttu-id="67836-147">Supporto degli Appunti tra host e area di lavoro</span><span class="sxs-lookup"><span data-stu-id="67836-147">Support clipboard between host and Workspace</span></span>

<span data-ttu-id="67836-148">Selezionare questa casella di controllo per abilitare la copia e l'incollatura tra l'host e l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67836-148">Select this check box to enable copying and pasting between the host and the MED-V workspace.</span></span>

<span data-ttu-id="67836-149">Supporto del trasferimento di file tra l'host e l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="67836-149">Support file transfer between the host and Workspace</span></span>

<span data-ttu-id="67836-150">Selezionare questa casella di controllo per consentire il trasferimento di file tra l'area di lavoro host e MED-V.</span><span class="sxs-lookup"><span data-stu-id="67836-150">Select this check box to enable transferring files between the host and MED-V workspace.</span></span> <span data-ttu-id="67836-151">Nella casella **trasferimento file** selezionare una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="67836-151">Select one of the following options from the **File Transfer** box:</span></span>

-   <span data-ttu-id="67836-152">**Entrambi**: Abilita il trasferimento di file tra l'host e l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67836-152">**Both**—Enable transferring files between the host and the MED-V workspace.</span></span>

-   <span data-ttu-id="67836-153">**Host to Workspace**: consente di trasferire file dall'host all'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67836-153">**Host to Workspace**—Enable transferring files from the host to the MED-V workspace.</span></span>

-   <span data-ttu-id="67836-154">**Area di lavoro da ospitare**: consente di trasferire file dall'area di lavoro MED-V all'host.</span><span class="sxs-lookup"><span data-stu-id="67836-154">**Workspace to Host**—Enable transferring files from the MED-V workspace to the host.</span></span>

**<span data-ttu-id="67836-155">Nota</span><span class="sxs-lookup"><span data-stu-id="67836-155">Note</span></span>**  
<span data-ttu-id="67836-156">Se un utente senza autorizzazioni tenta di trasferire i file, verrà visualizzata una finestra che chiede di immettere le credenziali di un utente con le autorizzazioni necessarie per eseguire il trasferimento di file.</span><span class="sxs-lookup"><span data-stu-id="67836-156">If a user without permissions attempts to transfer files, a window will appear prompting him to enter the credentials of a user with permissions to perform the file transfer.</span></span>



**<span data-ttu-id="67836-157">Importante</span><span class="sxs-lookup"><span data-stu-id="67836-157">Important</span></span>**  
<span data-ttu-id="67836-158">Per supportare il trasferimento di file in Windows XP SP3, è necessario disabilitare la sincronizzazione dei file offline modificando il registro di sistema nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="67836-158">To support file transfer in Windows XP SP3, you must disable offline file synchronization by editing the registry as follows:</span></span>

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



<span data-ttu-id="67836-159">Avanzate</span><span class="sxs-lookup"><span data-stu-id="67836-159">Advanced</span></span>

<span data-ttu-id="67836-160">Fare clic per impostare le opzioni avanzate per il trasferimento di file.</span><span class="sxs-lookup"><span data-stu-id="67836-160">Click to set the advanced file transfer options.</span></span> <span data-ttu-id="67836-161">Per altre informazioni, vedere [come impostare le opzioni avanzate per il trasferimento di file](how-to-set-advanced-file-transfer-options.md).</span><span class="sxs-lookup"><span data-stu-id="67836-161">For more information, see [How to Set Advanced File Transfer Options](how-to-set-advanced-file-transfer-options.md).</span></span>

*<span data-ttu-id="67836-162">Controllo dispositivo</span><span class="sxs-lookup"><span data-stu-id="67836-162">Device Control</span></span>*

<span data-ttu-id="67836-163">Abilitare la stampa alle stampanti connesse all'host</span><span class="sxs-lookup"><span data-stu-id="67836-163">Enable printing to printers connected to the host</span></span>

<span data-ttu-id="67836-164">Selezionare questa casella di controllo per consentire agli utenti di stampare dall'area di lavoro MED-V tramite la stampante host.</span><span class="sxs-lookup"><span data-stu-id="67836-164">Select this check box to enable users to print from the MED-V workspace using the host printer.</span></span>

**<span data-ttu-id="67836-165">Nota</span><span class="sxs-lookup"><span data-stu-id="67836-165">Note</span></span>**  
<span data-ttu-id="67836-166">La stampa viene eseguita dalle stampanti definite nell'host.</span><span class="sxs-lookup"><span data-stu-id="67836-166">The printing is performed by the printers defined on the host.</span></span>



<span data-ttu-id="67836-167">Abilitare l'accesso a CD/DVD</span><span class="sxs-lookup"><span data-stu-id="67836-167">Enable access to CD / DVD</span></span>

<span data-ttu-id="67836-168">Selezionare questa casella di controllo per consentire l'accesso a un'unità CD o DVD da questa area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="67836-168">Select this check box to allow access to a CD or DVD drive from this MED-V workspace.</span></span>



**<span data-ttu-id="67836-169">Più appartenenze</span><span class="sxs-lookup"><span data-stu-id="67836-169">Multiple Memberships</span></span>**

1.  <span data-ttu-id="67836-170">Se l'utente fa parte di un gruppo e le autorizzazioni vengono applicate all'utente e al gruppo in cui fanno parte, vengono applicate tutte le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="67836-170">If the user is part of a group and permissions are applied to the user as well as to the group they are part of, all permissions are applied.</span></span>

2.  <span data-ttu-id="67836-171">Se l'utente è un membro di due gruppi diversi, vengono applicate le autorizzazioni meno restrittive.</span><span class="sxs-lookup"><span data-stu-id="67836-171">If the user is a member of two different groups, the least restrictive permissions are applied.</span></span>

## <span data-ttu-id="67836-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67836-172">Related topics</span></span>


[<span data-ttu-id="67836-173">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="67836-173">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="67836-174">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="67836-174">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="67836-175">Come impostare le opzioni di eliminazione nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="67836-175">How to Set MED-V Workspace Deletion Options</span></span>](how-to-set-med-v-workspace-deletion-options.md)

[<span data-ttu-id="67836-176">Come impostare le opzioni avanzate per il trasferimento dei file</span><span class="sxs-lookup"><span data-stu-id="67836-176">How to Set Advanced File Transfer Options</span></span>](how-to-set-advanced-file-transfer-options.md)









