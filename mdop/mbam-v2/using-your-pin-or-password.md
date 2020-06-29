---
title: Uso di PIN o password
description: Uso di PIN o password
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823795"
---
# <span data-ttu-id="65a2c-103">Uso di PIN o password</span><span class="sxs-lookup"><span data-stu-id="65a2c-103">Using Your PIN or Password</span></span>


<span data-ttu-id="65a2c-104">BitLocker consente di proteggere il computer richiedendo un PIN (Personal Identification Number) o una password per sbloccare le informazioni archiviate nel computer.</span><span class="sxs-lookup"><span data-stu-id="65a2c-104">BitLocker helps secure your computer by requiring a personal identification number (PIN) or password to unlock the information that is stored on your computer.</span></span> <span data-ttu-id="65a2c-105">I requisiti di PIN o password sono impostati dall'organizzazione e dipendono dal tipo di unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="65a2c-105">The PIN or password requirements are set by your organization and depend on the kind of drive being encrypted.</span></span> <span data-ttu-id="65a2c-106">I dati delle unità crittografate non possono essere visualizzati senza immettere il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="65a2c-106">Data on the encrypted drives cannot be viewed without entering the PIN or password.</span></span> <span data-ttu-id="65a2c-107">Se l'hardware del computer include un TPM (Trusted Platform Module) abilitato, il chip TPM richiede il PIN prima dell'avvio di Windows nel computer.</span><span class="sxs-lookup"><span data-stu-id="65a2c-107">If your computer hardware includes an enabled Trusted Platform Module (TPM), the TPM chip prompts you for your PIN before Windows starts on your computer.</span></span>

## <span data-ttu-id="65a2c-108">Informazioni sul PIN e le password di BitLocker</span><span class="sxs-lookup"><span data-stu-id="65a2c-108">About Your BitLocker PIN and Passwords</span></span>


<span data-ttu-id="65a2c-109">La tua azienda specifica la complessità necessaria per il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="65a2c-109">Your company specifies the complexity required for your PIN or password.</span></span> <span data-ttu-id="65a2c-110">Questi requisiti per il PIN o la password vengono spiegati durante il processo di configurazione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="65a2c-110">These requirements for your PIN or password are explained during the BitLocker setup process.</span></span>

<span data-ttu-id="65a2c-111">La password viene usata per sbloccare le unità nel computer che non contengono il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="65a2c-111">The password is used to unlock drives on your computer that do not contain the operating system.</span></span> <span data-ttu-id="65a2c-112">BitLocker richiederà la password dopo che il PIN è stato richiesto durante l'avvio.</span><span class="sxs-lookup"><span data-stu-id="65a2c-112">BitLocker will ask for your password after the PIN is requested during startup.</span></span> <span data-ttu-id="65a2c-113">Ogni disco rigido protetto da BitLocker nel computer ha una password univoca.</span><span class="sxs-lookup"><span data-stu-id="65a2c-113">Each BitLocker protected hard disk on your computer has its own unique password.</span></span> <span data-ttu-id="65a2c-114">Non è possibile sbloccare un'unità protetta da BitLocker finché non si specifica la password.</span><span class="sxs-lookup"><span data-stu-id="65a2c-114">You cannot unlock a BitLocker protected drive until you provide your password.</span></span>

<span data-ttu-id="65a2c-115">**Nota**  Il tuo help desk può impostare le unità per l'apertura automatica.</span><span class="sxs-lookup"><span data-stu-id="65a2c-115">**Note** Your Help Desk may set drives to unlock automatically.</span></span> <span data-ttu-id="65a2c-116">In questo articolo viene eliminata la necessità di specificare un PIN o una password per visualizzare le informazioni sulle unità.</span><span class="sxs-lookup"><span data-stu-id="65a2c-116">This eliminates the need to provide a PIN or password to view the information on the drives.</span></span>

 

## <span data-ttu-id="65a2c-117">Sbloccare il computer se si dimentica il PIN o la password</span><span class="sxs-lookup"><span data-stu-id="65a2c-117">Unlocking Your Computer if You Forget Your PIN or Password</span></span>


<span data-ttu-id="65a2c-118">Se si dimentica il PIN o la password, il proprio help desk può aiutarti a sbloccare le unità protette da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="65a2c-118">If you forget your PIN or password, your Help Desk can help you unlock BitLocker protected drives.</span></span> <span data-ttu-id="65a2c-119">Per sbloccare un'unità protetta con BitLocker, contattare il supporto tecnico se serve assistenza.</span><span class="sxs-lookup"><span data-stu-id="65a2c-119">To unlock a drive protected with BitLocker, contact your Help Desk if you need help.</span></span>

**<span data-ttu-id="65a2c-120">Come sbloccare il computer se si dimentica il PIN o la password</span><span class="sxs-lookup"><span data-stu-id="65a2c-120">How to unlock your computer if you forget your PIN or password</span></span>**

1.  <span data-ttu-id="65a2c-121">Quando si contatta il proprio help desk, sarà necessario fornirle le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="65a2c-121">When you contact your Help Desk, you will need to provide them with the following information:</span></span>

    -   <span data-ttu-id="65a2c-122">Nome utente</span><span class="sxs-lookup"><span data-stu-id="65a2c-122">Your user name</span></span>

    -   <span data-ttu-id="65a2c-123">Il dominio</span><span class="sxs-lookup"><span data-stu-id="65a2c-123">Your domain</span></span>

    -   <span data-ttu-id="65a2c-124">Le prime otto cifre dell'ID chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="65a2c-124">The first eight digits of your recovery key ID.</span></span> <span data-ttu-id="65a2c-125">Si tratta di un codice a 32 cifre che verrà visualizzato da BitLocker se si dimentica il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="65a2c-125">This is a 32-digit code that BitLocker will display if you forget your PIN or password.</span></span>

        -   <span data-ttu-id="65a2c-126">Se si dimentica il PIN, sarà necessario immettere le prime otto cifre dell'ID chiave di ripristino, che verrà visualizzato nella console di ripristino di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="65a2c-126">If you forget your PIN, you will have to enter the first eight digits of the recovery key ID, which will appear in the BitLocker Recovery console.</span></span> <span data-ttu-id="65a2c-127">La console di ripristino di BitLocker è una schermata precedente a Windows che verrà visualizzata se non si immette il PIN corretto.</span><span class="sxs-lookup"><span data-stu-id="65a2c-127">The BitLocker Recovery console is a pre-Windows screen that will be displayed if you do not enter the correct PIN.</span></span>

        -   <span data-ttu-id="65a2c-128">Se si dimentica la password, cercare l'ID chiave di ripristino nell'applicazione del pannello di controllo opzioni di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="65a2c-128">If you forget your password, look for the recovery key ID in the BitLocker Encryption Options Control Panel application.</span></span> <span data-ttu-id="65a2c-129">Selezionare **Sblocca unità** e quindi fare clic su **non ricordo la password**.</span><span class="sxs-lookup"><span data-stu-id="65a2c-129">Select **Unlock Drive** and then click **I cannot remember my password**.</span></span> <span data-ttu-id="65a2c-130">L'applicazione opzioni di crittografia BitLocker visualizzerà quindi un ID chiave di ripristino che fornisci per il supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="65a2c-130">The BitLocker Encryption Options application will then display a recovery key ID that you provide to Help Desk.</span></span>

2.  <span data-ttu-id="65a2c-131">Una volta che il tuo help desk riceve le informazioni necessarie, ti fornirà una chiave di ripristino tramite telefono o tramite posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="65a2c-131">Once your Help Desk receives the necessary information, it will provide you with a recovery key over the phone or through e-mail.</span></span>

    -   <span data-ttu-id="65a2c-132">Se si è dimenticato il PIN, immettere il codice di ripristino nella console di ripristino di BitLocker per sbloccare il computer.</span><span class="sxs-lookup"><span data-stu-id="65a2c-132">If you forgot your PIN, enter the recovery key in the BitLocker Recovery console to unlock your computer.</span></span>

    -   <span data-ttu-id="65a2c-133">Se si è dimenticata la password, immettere la chiave di ripristino nell'applicazione del pannello di controllo opzioni di crittografia BitLocker, nella stessa posizione in cui è stato trovato l'ID chiave di ripristino in precedenza.</span><span class="sxs-lookup"><span data-stu-id="65a2c-133">If you forgot your password, enter the recovery key in the BitLocker Encryption Options Control Panel application, in the same location where you found the recovery key ID earlier.</span></span> <span data-ttu-id="65a2c-134">Verrà sbloccato il disco rigido protetto.</span><span class="sxs-lookup"><span data-stu-id="65a2c-134">This will unlock the protected hard drive.</span></span>

## <span data-ttu-id="65a2c-135">Cambiare il PIN o la password</span><span class="sxs-lookup"><span data-stu-id="65a2c-135">Changing your PIN or Password</span></span>


<span data-ttu-id="65a2c-136">Prima di poter modificare la password in un'unità protetta da BitLocker, è necessario sbloccare l'unità.</span><span class="sxs-lookup"><span data-stu-id="65a2c-136">Before you can change the password on a BitLocker protected drive, you must unlock the drive.</span></span> <span data-ttu-id="65a2c-137">Se l'unità non è sbloccata, selezionare **Sblocca unità**e quindi immettere la password corrente.</span><span class="sxs-lookup"><span data-stu-id="65a2c-137">If the drive is not unlocked, select **Unlock Drive**, and then enter your current password.</span></span> <span data-ttu-id="65a2c-138">Non appena l'unità è sbloccata, è possibile selezionare **Gestisci la password** per cambiare la password corrente.</span><span class="sxs-lookup"><span data-stu-id="65a2c-138">As soon as the drive is unlocked, you can select **Manage your Password** to change your current password.</span></span>

**<span data-ttu-id="65a2c-139">Come cambiare il PIN o la password</span><span class="sxs-lookup"><span data-stu-id="65a2c-139">How to Change your PIN or password</span></span>**

1.  <span data-ttu-id="65a2c-140">Fare clic sul pulsante **Start**e quindi selezionare **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="65a2c-140">Click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="65a2c-141">Il pannello di controllo viene aperto in una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="65a2c-141">Control Panel opens in a new window.</span></span>

2.  <span data-ttu-id="65a2c-142">Selezionare **sistema e sicurezza**e quindi selezionare le **Opzioni di crittografia BitLocker**.</span><span class="sxs-lookup"><span data-stu-id="65a2c-142">Select **System and Security**, and then select **BitLocker Encryption Options**.</span></span>

    -   <span data-ttu-id="65a2c-143">Per cambiare il PIN, selezionare **Gestisci il pin**.</span><span class="sxs-lookup"><span data-stu-id="65a2c-143">To change your PIN, select **Manage Your PIN**.</span></span> <span data-ttu-id="65a2c-144">Digitare il nuovo PIN in entrambi i campi e selezionare **Reimposta PIN**.</span><span class="sxs-lookup"><span data-stu-id="65a2c-144">Type your new PIN into both fields and select **Reset PIN**.</span></span>

    -   <span data-ttu-id="65a2c-145">Per cambiare la password, selezionare **Gestisci la password**.</span><span class="sxs-lookup"><span data-stu-id="65a2c-145">To change your password, select **Manage Your Password**.</span></span> <span data-ttu-id="65a2c-146">Immettere la nuova password in entrambi i campi e selezionare **Reimposta password**.</span><span class="sxs-lookup"><span data-stu-id="65a2c-146">Enter your new password into both fields and select **Reset Password**.</span></span>

 

 





