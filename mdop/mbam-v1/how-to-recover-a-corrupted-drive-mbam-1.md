---
title: Come recuperare un'unità danneggiata
description: Come recuperare un'unità danneggiata
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804606"
---
# <span data-ttu-id="ba810-103">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="ba810-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="ba810-104">Per recuperare un'unità danneggiata protetta da BitLocker, un utente dell'help desk di amministrazione e monitoraggio di Microsoft BitLocker deve creare un file di pacchetto chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ba810-104">To recover a corrupted drive that has been protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) help desk user must create a recovery key package file.</span></span> <span data-ttu-id="ba810-105">Questo file di pacchetto può essere copiato nel computer che contiene l'unità danneggiata e quindi usato per recuperare l'unità.</span><span class="sxs-lookup"><span data-stu-id="ba810-105">This package file can be copied to the computer that contains the corrupted drive and then used to recover the drive.</span></span> <span data-ttu-id="ba810-106">Per eseguire questa operazione, usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="ba810-106">To accomplish this, use the following procedure.</span></span>

**<span data-ttu-id="ba810-107">Per recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="ba810-107">To Recover a Corrupted Drive</span></span>**

1.  <span data-ttu-id="ba810-108">Aprire il sito Web di amministrazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="ba810-108">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="ba810-109">Selezionare **ripristino unità** dal riquadro di spostamento.</span><span class="sxs-lookup"><span data-stu-id="ba810-109">Select **Drive Recovery** from the navigation pane.</span></span> <span data-ttu-id="ba810-110">Immettere il nome di dominio e il nome utente dell'utente, il motivo per cui è stato sbloccato l'unità e l'ID password di ripristino dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ba810-110">Enter the user’s domain name and user name, the reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="ba810-111">**Nota**  Se si è membri del ruolo Help desk Administrators, non è necessario immettere il nome di dominio o il nome utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ba810-111">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="ba810-112">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="ba810-112">Click **Submit**.</span></span> <span data-ttu-id="ba810-113">Verrà visualizzata la chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ba810-113">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="ba810-114">Fare clic su **Salva**e quindi selezionare **pacchetto chiave di ripristino**.</span><span class="sxs-lookup"><span data-stu-id="ba810-114">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="ba810-115">Il pacchetto chiave di ripristino verrà creato nel computer.</span><span class="sxs-lookup"><span data-stu-id="ba810-115">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="ba810-116">Copiare il pacchetto della chiave di ripristino nel computer in cui è presente l'unità danneggiata.</span><span class="sxs-lookup"><span data-stu-id="ba810-116">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="ba810-117">Apri una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="ba810-117">Open an elevated command prompt.</span></span> <span data-ttu-id="ba810-118">A tale scopo, fare clic su **Avvia** e digitare `cmd` nella casella **Cerca programmi e file** .</span><span class="sxs-lookup"><span data-stu-id="ba810-118">To do this, click **Start** and type `cmd` in the **Search programs and files** box.</span></span> <span data-ttu-id="ba810-119">Nell'elenco dei risultati della ricerca fare clic con il pulsante destro del mouse **cmd.exe** e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="ba810-119">In the search results list, right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="ba810-120">Al prompt dei comandi digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ba810-120">At the command prompt, type the following:</span></span>

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="ba810-121">**Nota**  Per l' &lt; unità fissa &gt; nel comando, specificare un dispositivo di archiviazione disponibile che disponga di spazio libero uguale o maggiore rispetto ai dati nell'unità danneggiata.</span><span class="sxs-lookup"><span data-stu-id="ba810-121">**Note** For the &lt;fixed drive&gt; in the command, specify an available storage device that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="ba810-122">I dati dell'unità danneggiata vengono recuperati e spostati nell'unità fissa specificata.</span><span class="sxs-lookup"><span data-stu-id="ba810-122">Data on the corrupted drive is recovered and moved to the specified fixed drive.</span></span>

     

## <span data-ttu-id="ba810-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba810-123">Related topics</span></span>


[<span data-ttu-id="ba810-124">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="ba810-124">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





