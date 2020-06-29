---
title: Come ripristinare un blocco del TPM
description: Come ripristinare un blocco del TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823325"
---
# <span data-ttu-id="87069-103">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="87069-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="87069-104">Questo argomento illustra come usare il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per reimpostare un blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="87069-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to reset a TPM lockout.</span></span> <span data-ttu-id="87069-105">I blocchi TPM possono verificarsi se un utente finale immette il PIN errato troppo spesso.</span><span class="sxs-lookup"><span data-stu-id="87069-105">TPM lockouts can occur if an end user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="87069-106">Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino da produttore a produttore.</span><span class="sxs-lookup"><span data-stu-id="87069-106">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="87069-107">Nell'area **Manage TPM** del sito Web amministrazione e monitoraggio è possibile accedere al sistema di dati di ripristino della chiave centralizzata, che fornisce un file di password del proprietario del TPM quando si specifica un ID computer e un identificatore utente associato.</span><span class="sxs-lookup"><span data-stu-id="87069-107">From the **Manage TPM** area of the Administration and Monitoring Website, you can access the centralized Key Recovery data system, which provides a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

<span data-ttu-id="87069-108">Per accedere all'area manage TPM del sito Web di amministrazione e monitoraggio, è necessario essere assegnati al ruolo degli utenti di MBAM helpdesk o al ruolo di utenti avanzati helpdesk di MBAM.</span><span class="sxs-lookup"><span data-stu-id="87069-108">To access the Manage TPM area of the Administration and Monitoring Website, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="87069-109">Questi ruoli sono gruppi creati dagli amministratori in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="87069-109">These roles are groups that administrators create in Active Directory.</span></span> <span data-ttu-id="87069-110">Puoi usare qualsiasi nome per questi gruppi.</span><span class="sxs-lookup"><span data-stu-id="87069-110">You can use any name for these groups.</span></span> <span data-ttu-id="87069-111">Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="87069-111">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="87069-112">Per informazioni su MBAM e la proprietà TPM, vedere [considerazioni sulla sicurezza di mbam 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="87069-112">For information about MBAM and TPM ownership, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

**<span data-ttu-id="87069-113">Per reimpostare un blocco TPM</span><span class="sxs-lookup"><span data-stu-id="87069-113">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="87069-114">Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.</span><span class="sxs-lookup"><span data-stu-id="87069-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="87069-115">Nel riquadro sinistro fare clic su **Gestisci TPM** per aprire la pagina **Manage TPM** .</span><span class="sxs-lookup"><span data-stu-id="87069-115">In the left pane, click **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="87069-116">Immettere il nome di dominio completo per il computer e il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="87069-116">Enter the fully qualified domain name for the computer and the computer name.</span></span>

4.  <span data-ttu-id="87069-117">Immettere il dominio di log-in Windows dell'utente finale e il nome utente per recuperare il file della password del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="87069-117">Enter the end user’s Windows log-on domain and user name to retrieve the TPM owner password file.</span></span>

    <span data-ttu-id="87069-118">**Nota**  Se ci si trova nel gruppo MBAM Advanced helpdesk Users, il dominio utente e i campi ID utente non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="87069-118">**Note** If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="87069-119">Dal **motivo per richiedere** l'elenco dei file di password del proprietario del TPM selezionare un motivo per la richiesta e fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="87069-119">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="87069-120">MBAM restituisce una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="87069-120">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="87069-121">Messaggio di errore se non viene trovato un file di password del proprietario del TPM corrispondente</span><span class="sxs-lookup"><span data-stu-id="87069-121">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="87069-122">File di password del proprietario del TPM per il computer inviato</span><span class="sxs-lookup"><span data-stu-id="87069-122">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="87069-123">Dopo aver recuperato la password del proprietario del TPM, viene visualizzata la password del proprietario.</span><span class="sxs-lookup"><span data-stu-id="87069-123">After the TPM owner password is retrieved, the owner password is displayed.</span></span>

6.  <span data-ttu-id="87069-124">Per salvare la password in un file con estensione TPM, fare clic sul pulsante **Salva** .</span><span class="sxs-lookup"><span data-stu-id="87069-124">To save the password to a .tpm file, click the **Save** button.</span></span>

7.  <span data-ttu-id="87069-125">Nell'area **Manage TPM** del **sito Web amministrazione e monitoraggio**selezionare l'opzione **Reimposta il blocco TPM** e specificare il file della password del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="87069-125">In the **Manage TPM** area of the **Administration and Monitoring Website**, select the **Reset TPM lockout** option and provide the TPM owner password file.</span></span>

    <span data-ttu-id="87069-126">Il blocco TPM viene reimpostato e l'accesso dell'utente finale viene ripristinato.</span><span class="sxs-lookup"><span data-stu-id="87069-126">The TPM lockout is reset and the end user’s access is restored.</span></span>

    <span data-ttu-id="87069-127">**Importante**  Non assegnare il valore hash TPM o il file della password del proprietario del TPM agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="87069-127">**Important** Do not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="87069-128">Dato che le informazioni sul TPM non cambiano, il file viene creato dagli utenti finali per creare un rischio per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="87069-128">Because the TPM information does not change, giving the file to end users creates a security risk.</span></span>

     



## <span data-ttu-id="87069-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87069-129">Related topics</span></span>


[<span data-ttu-id="87069-130">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="87069-130">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="87069-131">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="87069-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="87069-132">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="87069-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="87069-133">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="87069-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





