---
title: Come recuperare un'unità danneggiata
description: Come recuperare un'unità danneggiata
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822555"
---
# <span data-ttu-id="8046c-103">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="8046c-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="8046c-104">È possibile usare questa procedura con il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per recuperare un'unità danneggiata protetta da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8046c-104">You can use this procedure with the Administration and Monitoring Website (also referred to as the Help Desk) Website to recover a corrupted drive that is protected by BitLocker.</span></span> <span data-ttu-id="8046c-105">A questo scopo, verranno completate le attività descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8046c-105">To do this, you will complete the tasks outlined in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8046c-106">Attività</span><span class="sxs-lookup"><span data-stu-id="8046c-106">Task</span></span></th>
<th align="left"><span data-ttu-id="8046c-107">Dettagli e altre informazioni</span><span class="sxs-lookup"><span data-stu-id="8046c-107">Details and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8046c-108">Creare un file di pacchetto chiave di ripristino accedendo all' <strong> area recupero unità </strong> del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="8046c-108">Create a recovery key package file by accessing the <strong>Drive Recovery</strong> area of the Administration and Monitoring Website.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8046c-109">Per accedere all' <strong> area di ripristino dell'unità </strong> , è necessario essere assegnati al ruolo degli utenti di mbam helpdesk o al ruolo di utenti avanzati helpdesk di mbam.</span><span class="sxs-lookup"><span data-stu-id="8046c-109">To access the <strong>Drive Recovery</strong> area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="8046c-110">Quando sono stati creati, è possibile che siano stati assegnati nomi diversi a questi ruoli.</span><span class="sxs-lookup"><span data-stu-id="8046c-110">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="8046c-111">Per altre informazioni, Vedi <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> pianificazione per i gruppi e gli account di MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="8046c-111">For more information, see <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)">Planning for MBAM 2.5 Groups and Accounts</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8046c-112">Copiare il file del pacchetto nel computer che contiene l'unità danneggiata.</span><span class="sxs-lookup"><span data-stu-id="8046c-112">Copy the package file to the computer that contains the corrupted drive.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8046c-113">Usare il <code>repair-bde</code> comando per completare il processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8046c-113">Use the <code>repair-bde</code> command to complete the recovery process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8046c-114">Per evitare una potenziale perdita di dati, è consigliabile rivedere il <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> comando Manage-bde prima di </a> usarlo.</span><span class="sxs-lookup"><span data-stu-id="8046c-114">To avoid a potential loss of data, it is strongly recommended that you review the <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)">Manage-bde</a> command before using it.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="8046c-115">Per recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="8046c-115">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="8046c-116">Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.</span><span class="sxs-lookup"><span data-stu-id="8046c-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="8046c-117">Nel riquadro sinistro selezionare unità di **ripristino** per aprire la pagina **Recupera accesso a una unità crittografata** .</span><span class="sxs-lookup"><span data-stu-id="8046c-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="8046c-118">Immettere il dominio di accesso e il nome utente di Windows dell'utente finale, il motivo per cui è stato sbloccato l'unità e l'ID password di ripristino dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="8046c-118">Enter the end user’s Windows log-on domain and user name, the reason for unlocking the drive, and the end user’s recovery password ID.</span></span>

    <span data-ttu-id="8046c-119">**Nota**  Se si è un membro del gruppo di Access per utenti avanzati helpdesk, non è necessario immettere il nome di dominio o il nome utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8046c-119">**Note** If you are a member of the Advanced Helpdesk Users access group, you do not have to enter the user’s domain name or user name.</span></span>

     

4.  <span data-ttu-id="8046c-120">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="8046c-120">Click **Submit**.</span></span> <span data-ttu-id="8046c-121">Verrà visualizzata la chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8046c-121">The recovery key will be displayed.</span></span>

5.  <span data-ttu-id="8046c-122">Fare clic su **Salva**e quindi selezionare **pacchetto chiave di ripristino**.</span><span class="sxs-lookup"><span data-stu-id="8046c-122">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="8046c-123">Il pacchetto chiave di ripristino verrà creato nel computer.</span><span class="sxs-lookup"><span data-stu-id="8046c-123">The recovery key package will be created on your computer.</span></span>

6.  <span data-ttu-id="8046c-124">Copiare il pacchetto della chiave di ripristino nel computer in cui è presente l'unità danneggiata.</span><span class="sxs-lookup"><span data-stu-id="8046c-124">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

7.  <span data-ttu-id="8046c-125">Apri una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="8046c-125">Open an elevated command prompt.</span></span> <span data-ttu-id="8046c-126">A tale scopo, fare clic sul pulsante **Start** e digitare `cmd` nella casella di testo **Cerca programmi e file** .</span><span class="sxs-lookup"><span data-stu-id="8046c-126">To do this, click **Start** and type `cmd` in the **Search programs and files** text box.</span></span> <span data-ttu-id="8046c-127">Fare clic con il pulsante destro del mouse su **cmd.exe**e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="8046c-127">Right-click **cmd.exe**, and select **Run as Administrator**.</span></span>

8.  <span data-ttu-id="8046c-128">Al prompt dei comandi digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="8046c-128">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="8046c-129">**Nota**  Sostituire &lt; l' *unità fissa* &gt; con un'unità disco rigido disponibile che disponga di spazio libero uguale o maggiore rispetto ai dati nell'unità danneggiata.</span><span class="sxs-lookup"><span data-stu-id="8046c-129">**Note** Replace &lt;*fixed drive*&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="8046c-130">I dati dell'unità danneggiata vengono recuperati e spostati nell'unità disco rigido specificata.</span><span class="sxs-lookup"><span data-stu-id="8046c-130">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     


## <span data-ttu-id="8046c-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8046c-131">Related topics</span></span>


[<span data-ttu-id="8046c-132">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8046c-132">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="8046c-133">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="8046c-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8046c-134">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8046c-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8046c-135">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8046c-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





