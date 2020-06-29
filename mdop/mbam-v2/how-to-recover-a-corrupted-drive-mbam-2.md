---
title: Come recuperare un'unità danneggiata
description: Come recuperare un'unità danneggiata
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822875"
---
# <span data-ttu-id="6c690-103">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="6c690-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="6c690-104">Per recuperare un'unità danneggiata protetta da BitLocker, un utente dell'help desk di amministrazione e monitoraggio di Microsoft BitLocker dovrà creare un file di pacchetto chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6c690-104">To recover a corrupted drive protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) Help Desk user will need to create a recovery key package file.</span></span> <span data-ttu-id="6c690-105">Questo file di pacchetto può quindi essere copiato nel computer che contiene l'unità danneggiata e quindi usato per recuperare l'unità.</span><span class="sxs-lookup"><span data-stu-id="6c690-105">This package file can then be copied to the computer that contains the corrupted drive, and then used to recover the drive.</span></span> <span data-ttu-id="6c690-106">Usare la procedura seguente per i passaggi necessari per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6c690-106">Use the following procedure for the steps needed to do this.</span></span>

<span data-ttu-id="6c690-107">**Importante**  Per evitare una potenziale perdita di dati, è consigliabile leggere la guida "Repair-bde" e capire chiaramente come usare il comando prima di completare le istruzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c690-107">**Important** To avoid a potential loss of data, it is strongly recommended that you read the “repair-bde” help and clearly understand how to use the command before completing the following instructions.</span></span>

 

**<span data-ttu-id="6c690-108">Per recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="6c690-108">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="6c690-109">Per creare il pacchetto chiave di ripristino necessario per recuperare un'unità danneggiata, avviare un Web browser e aprire il sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="6c690-109">To create the recovery key package necessary to recover a corrupted drive, start a web browser and open the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="6c690-110">Selezionare **ripristino unità** dal riquadro di spostamento sinistro.</span><span class="sxs-lookup"><span data-stu-id="6c690-110">Select **Drive Recovery** from the left navigation pane.</span></span> <span data-ttu-id="6c690-111">Immettere il nome di dominio dell'utente, il nome utente, il motivo per sbloccare l'unità e l'ID password di ripristino dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6c690-111">Enter the user’s domain name, user name, reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="6c690-112">**Nota**  Se si è membri del ruolo Help desk Administrators, non è necessario immettere il nome di dominio o il nome utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6c690-112">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="6c690-113">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="6c690-113">Click **Submit**.</span></span> <span data-ttu-id="6c690-114">Verrà visualizzata la chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6c690-114">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="6c690-115">Fare clic su **Salva**e quindi selezionare **pacchetto chiave di ripristino**.</span><span class="sxs-lookup"><span data-stu-id="6c690-115">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="6c690-116">Il pacchetto chiave di ripristino verrà creato nel computer.</span><span class="sxs-lookup"><span data-stu-id="6c690-116">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="6c690-117">Copiare il pacchetto della chiave di ripristino nel computer in cui è presente l'unità danneggiata.</span><span class="sxs-lookup"><span data-stu-id="6c690-117">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="6c690-118">Apri una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="6c690-118">Open an elevated command prompt.</span></span> <span data-ttu-id="6c690-119">A tale scopo, fare clic su **Avvia** e digitare `cmd` nella **casella Cerca programmi e file**.</span><span class="sxs-lookup"><span data-stu-id="6c690-119">To do this, click **Start** and type `cmd` in the **Search programs and files box**.</span></span> <span data-ttu-id="6c690-120">Fare clic con il pulsante destro del mouse **cmd.exe** e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="6c690-120">Right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="6c690-121">Al prompt dei comandi digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="6c690-121">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="6c690-122">**Nota**  Sostituire &lt; l'unità fissa &gt; con un'unità disco rigido disponibile che disponga di spazio libero uguale o maggiore rispetto ai dati nell'unità danneggiata.</span><span class="sxs-lookup"><span data-stu-id="6c690-122">**Note** Replace &lt;fixed drive&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="6c690-123">I dati dell'unità danneggiata vengono recuperati e spostati nell'unità disco rigido specificata.</span><span class="sxs-lookup"><span data-stu-id="6c690-123">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     

## <span data-ttu-id="6c690-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6c690-124">Related topics</span></span>


[<span data-ttu-id="6c690-125">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="6c690-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





