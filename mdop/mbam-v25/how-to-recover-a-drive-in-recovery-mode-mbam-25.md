---
title: Come recuperare un'unità in modalità di ripristino
description: Come recuperare un'unità in modalità di ripristino
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823366"
---
# <span data-ttu-id="28710-103">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="28710-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="28710-104">Questo argomento spiega come usare il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per ottenere una password di ripristino da assegnare agli utenti finali se l'unità protetta da BitLocker entra in modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="28710-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to get a recovery password to give to end users if their BitLocker-protected drive goes into recovery mode.</span></span> <span data-ttu-id="28710-105">Le unità entrano in modalità di ripristino se gli utenti perdono o dimenticano il PIN o la password o se il chip TPM (Trusted Module Platform) rileva le modifiche apportate al BIOS o ai file di avvio di un computer.</span><span class="sxs-lookup"><span data-stu-id="28710-105">Drives go into recovery mode if users lose or forget their PIN or password or if the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="28710-106">Per ottenere una password di ripristino, usare l'area di **recupero unità** del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="28710-106">To get a recovery password, use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="28710-107">Per accedere all'area del sito Web, è necessario essere assegnati al ruolo degli utenti di MBAM helpdesk o al ruolo degli utenti dell'helpdesk Advanced.</span><span class="sxs-lookup"><span data-stu-id="28710-107">You must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role to access this area of the website.</span></span>

**<span data-ttu-id="28710-108">Nota</span><span class="sxs-lookup"><span data-stu-id="28710-108">Note</span></span>**  
<span data-ttu-id="28710-109">Quando sono stati creati, è possibile che siano stati assegnati nomi diversi a questi ruoli.</span><span class="sxs-lookup"><span data-stu-id="28710-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="28710-110">Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="28710-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>



**<span data-ttu-id="28710-111">Importante</span><span class="sxs-lookup"><span data-stu-id="28710-111">Important</span></span>**  
<span data-ttu-id="28710-112">Le password di ripristino scadono dopo un singolo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="28710-112">Recovery passwords expire after a single use.</span></span> <span data-ttu-id="28710-113">Nelle unità del sistema operativo e nelle unità dati fisse viene applicata automaticamente la regola di uso singolo.</span><span class="sxs-lookup"><span data-stu-id="28710-113">On operating system drives and fixed data drives, the single-use rule is applied automatically.</span></span> <span data-ttu-id="28710-114">In unità rimovibili viene applicata quando l'unità viene rimossa e quindi reinserita e sbloccata in un computer in cui sono attivate le impostazioni dei criteri di gruppo per gestire le unità rimovibili.</span><span class="sxs-lookup"><span data-stu-id="28710-114">On removable drives, it is applied when the drive is removed and then reinserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="28710-115">Per recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="28710-115">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="28710-116">Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.</span><span class="sxs-lookup"><span data-stu-id="28710-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="28710-117">Nel riquadro sinistro selezionare unità di **ripristino** per aprire la pagina **Recupera accesso a una unità crittografata** .</span><span class="sxs-lookup"><span data-stu-id="28710-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="28710-118">Immettere il dominio di log-in Windows dell'utente finale e il nome utente per visualizzare le informazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="28710-118">Enter the end user’s Windows log-on domain and user name to view recovery information.</span></span>

    **<span data-ttu-id="28710-119">Nota</span><span class="sxs-lookup"><span data-stu-id="28710-119">Note</span></span>**  
    <span data-ttu-id="28710-120">Se ci si trova nel gruppo MBAM Advanced helpdesk Users, il dominio utente e i campi ID utente non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="28710-120">If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>



4.  <span data-ttu-id="28710-121">Immettere le prime otto cifre dell'ID chiave di ripristino per visualizzare un elenco di possibili chiavi di ripristino corrispondenti oppure immettere l'intero ID chiave di ripristino per ottenere la chiave di ripristino esatta.</span><span class="sxs-lookup"><span data-stu-id="28710-121">Enter the first eight digits of the recovery key ID to see a list of possible matching recovery keys, or enter the entire recovery key ID to get the exact recovery key.</span></span>

5.  <span data-ttu-id="28710-122">Dall'elenco **motivo per l'unità di sblocco** selezionare una delle opzioni predefinite e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="28710-122">From the **Reason for Drive Unlock** list, select one of the predefined options, and then click **Submit**.</span></span>

    <span data-ttu-id="28710-123">MBAM restituisce il seguente:</span><span class="sxs-lookup"><span data-stu-id="28710-123">MBAM returns the following:</span></span>

    -   <span data-ttu-id="28710-124">Messaggio di errore se non viene trovata una password di ripristino corrispondente</span><span class="sxs-lookup"><span data-stu-id="28710-124">An error message if no matching recovery password is found</span></span>

    -   <span data-ttu-id="28710-125">Più possibili corrispondenze se l'utente ha più password di ripristino corrispondenti</span><span class="sxs-lookup"><span data-stu-id="28710-125">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    -   <span data-ttu-id="28710-126">La password di ripristino e il pacchetto di ripristino per l'utente inviato</span><span class="sxs-lookup"><span data-stu-id="28710-126">The recovery password and recovery package for the submitted user</span></span>

        **<span data-ttu-id="28710-127">Nota</span><span class="sxs-lookup"><span data-stu-id="28710-127">Note</span></span>**  
        <span data-ttu-id="28710-128">Se si sta recuperando un'unità danneggiata, l'opzione pacchetto di ripristino fornisce a BitLocker le informazioni critiche necessarie per recuperare l'unità.</span><span class="sxs-lookup"><span data-stu-id="28710-128">If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.</span></span>



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. <span data-ttu-id="28710-129">Per copiare la password, fare clic su **copia chiave**e quindi incollare la password di ripristino in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="28710-129">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="28710-130">In alternativa, fare clic su **Salva** per salvare la password di ripristino in un file.</span><span class="sxs-lookup"><span data-stu-id="28710-130">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="28710-131">Quando l'utente digita la password di ripristino nel sistema o usa il pacchetto di ripristino, l'unità viene sbloccata.</span><span class="sxs-lookup"><span data-stu-id="28710-131">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>



## <span data-ttu-id="28710-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28710-132">Related topics</span></span>


[<span data-ttu-id="28710-133">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="28710-133">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)



## <span data-ttu-id="28710-134">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="28710-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="28710-135">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="28710-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="28710-136">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="28710-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





