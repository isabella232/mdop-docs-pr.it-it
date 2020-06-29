---
title: Come recuperare un'unità in modalità di ripristino
description: Come recuperare un'unità in modalità di ripristino
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804612"
---
# <span data-ttu-id="7d736-103">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="7d736-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="7d736-104">Microsoft BitLocker Administration and Monitoring (MBAM) include funzionalità crittografate per il ripristino delle unità.</span><span class="sxs-lookup"><span data-stu-id="7d736-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes Encrypted Drive Recovery features.</span></span> <span data-ttu-id="7d736-105">Queste funzionalità garantiscono l'acquisizione e l'archiviazione dei dati e la disponibilità di strumenti necessari per accedere a un volume protetto da BitLocker quando BitLocker inserisce tale volume in modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d736-105">These features ensure the capture and storage of data and availability of tools that are required to access a BitLocker-protected volume when BitLocker puts that volume into recovery mode.</span></span> <span data-ttu-id="7d736-106">Un volume protetto da BitLocker entra in modalità di ripristino quando un PIN o una password viene persa o dimenticata oppure quando il chip TPM (Trusted Module Platform) rileva una modifica del BIOS o dei file di avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="7d736-106">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects a change to the computer's BIOS or startup files.</span></span>

<span data-ttu-id="7d736-107">Questa procedura consente di accedere al sistema di dati di ripristino della chiave centralizzata in grado di fornire una password di ripristino quando viene fornito un ID password di ripristino e un Identificativo utente associato.</span><span class="sxs-lookup"><span data-stu-id="7d736-107">Use this procedure to access the centralized Key Recovery data system that can provide a recovery password when a recovery password ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="7d736-108">**Importante**  MBAM genera chiavi di ripristino monouso.</span><span class="sxs-lookup"><span data-stu-id="7d736-108">**Important** MBAM generates single-use recovery keys.</span></span> <span data-ttu-id="7d736-109">In questa limitazione, una chiave di ripristino può essere usata una sola volta e quindi non è più valida.</span><span class="sxs-lookup"><span data-stu-id="7d736-109">Under this limitation, a recovery key can be used only once and then it is no longer valid.</span></span> <span data-ttu-id="7d736-110">L'uso singolo di una password di ripristino viene applicato automaticamente alle unità del sistema operativo e alle unità fisse.</span><span class="sxs-lookup"><span data-stu-id="7d736-110">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="7d736-111">In unità rimovibili, il singolo uso viene applicato quando l'unità viene rimossa e quindi reinserita e sbloccata in un computer in cui sono attivate le impostazioni dei criteri di gruppo per gestire le unità rimovibili.</span><span class="sxs-lookup"><span data-stu-id="7d736-111">On removable drives, the single use is applied when the drive is removed and then re-inserted and unlocked on a computer that has the group policy settings activated to manage removable drives.</span></span>

 

**<span data-ttu-id="7d736-112">Per recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="7d736-112">To recover a drive in Recovery Mode</span></span>**

1.  <span data-ttu-id="7d736-113">Aprire il sito Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7d736-113">Open the MBAM website.</span></span>

2.  <span data-ttu-id="7d736-114">Nel riquadro di spostamento fare clic su **ripristino unità**.</span><span class="sxs-lookup"><span data-stu-id="7d736-114">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="7d736-115">Viene visualizzata la pagina Web **Recupera accesso a un'unità crittografata** .</span><span class="sxs-lookup"><span data-stu-id="7d736-115">The **Recover access to an encrypted drive** webpage opens.</span></span>

3.  <span data-ttu-id="7d736-116">Immettere il dominio di accesso di Windows e il nome utente dell'utente e le prime otto cifre dell'ID chiave di ripristino per ricevere un elenco di possibili chiavi di ripristino corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="7d736-116">Enter the user's Windows Logon domain and user name and the first eight digits of the recovery key ID, to receive a list of possible matching recovery keys.</span></span> <span data-ttu-id="7d736-117">In alternativa, immettere l'intero ID chiave di ripristino per ricevere l'esatta chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d736-117">Alternatively, enter the entire recovery key ID to receive the exact recovery key.</span></span> <span data-ttu-id="7d736-118">Selezionare una delle opzioni predefinite nell'elenco a discesa **motivo per l'unità di sblocco** e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="7d736-118">Select one of the predefined options in the **Reason for Drive Unlock** drop-down list, and then click **Submit**.</span></span>

    <span data-ttu-id="7d736-119">**Nota**  Se si è un utente di MBAM Advanced helpdesk, le voci di dominio utente e ID utente non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="7d736-119">**Note** If you are an MBAM Advanced Helpdesk User, the user domain and user ID entries are not required.</span></span>

     

4.  <span data-ttu-id="7d736-120">MBAM restituisce il seguente:</span><span class="sxs-lookup"><span data-stu-id="7d736-120">MBAM returns the following:</span></span>

    1.  <span data-ttu-id="7d736-121">Messaggio di errore se non viene trovata una password di ripristino corrispondente</span><span class="sxs-lookup"><span data-stu-id="7d736-121">An error message if no matching recovery password is found</span></span>

    2.  <span data-ttu-id="7d736-122">Più possibili corrispondenze se l'utente ha più password di ripristino corrispondenti</span><span class="sxs-lookup"><span data-stu-id="7d736-122">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    3.  <span data-ttu-id="7d736-123">La password di ripristino e il pacchetto di ripristino per l'utente inviato</span><span class="sxs-lookup"><span data-stu-id="7d736-123">The recovery password and recovery package for the submitted user</span></span>

        <span data-ttu-id="7d736-124">**Nota**  Se si sta recuperando un'unità danneggiata, l'opzione pacchetto di ripristino fornisce a BitLocker le informazioni critiche necessarie per tentare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d736-124">**Note** If you are recovering a damaged drive, the recovery package option provides BitLocker with the critical information necessary to attempt the recovery.</span></span>

         

5.  <span data-ttu-id="7d736-125">Dopo aver recuperato la password di ripristino e il pacchetto di ripristino, viene visualizzata la password di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7d736-125">After the recovery password and recovery package are retrieved, the recovery password is displayed.</span></span> <span data-ttu-id="7d736-126">Per copiare la password, fare clic su **copia chiave**e quindi incollare la password di ripristino in un messaggio di posta elettronica o in un altro file di testo per lo spazio di archiviazione temporaneo.</span><span class="sxs-lookup"><span data-stu-id="7d736-126">To copy the password, click **Copy Key**, and then paste the recovery password into an email or other text file for temporary storage.</span></span> <span data-ttu-id="7d736-127">In alternativa, per salvare la password di ripristino in un file, fare clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="7d736-127">Or, to save the recovery password to a file, click **Save**.</span></span>

6.  <span data-ttu-id="7d736-128">Quando l'utente digita la password di ripristino nel sistema o usa il pacchetto di ripristino, l'unità viene sbloccata.</span><span class="sxs-lookup"><span data-stu-id="7d736-128">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="7d736-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7d736-129">Related topics</span></span>


[<span data-ttu-id="7d736-130">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="7d736-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





