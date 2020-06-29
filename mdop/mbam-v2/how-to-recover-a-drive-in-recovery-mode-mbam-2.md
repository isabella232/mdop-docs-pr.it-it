---
title: Come recuperare un'unità in modalità di ripristino
description: Come recuperare un'unità in modalità di ripristino
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825056"
---
# <span data-ttu-id="2231f-103">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="2231f-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="2231f-104">Le funzionalità di ripristino delle unità crittografate di Microsoft BitLocker Administration and Monitoring (MBAM) garantiscono l'acquisizione e l'archiviazione dei dati e la disponibilità degli strumenti necessari per accedere a un volume protetto da BitLocker quando BitLocker entra in modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2231f-104">The encrypted drive recovery features of Microsoft BitLocker Administration and Monitoring (MBAM) ensure the capture and storage of data and availability of tools required to access a BitLocker-protected volume when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="2231f-105">Un volume protetto da BitLocker entra in modalità di ripristino quando un PIN o una password viene persa o dimenticata oppure quando il chip TPM (Trusted Module Platform) rileva le modifiche apportate al BIOS o ai file di avvio di un computer.</span><span class="sxs-lookup"><span data-stu-id="2231f-105">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="2231f-106">Questa procedura consente di accedere al sistema di dati di ripristino centralizzato delle chiavi, che può fornire una password di ripristino se viene fornito un ID password di ripristino e un Identificativo utente associato.</span><span class="sxs-lookup"><span data-stu-id="2231f-106">Use this procedure to access the centralized key recovery data system, which can provide a recovery password if a recovery password ID and associated user identifier are supplied.</span></span>

**<span data-ttu-id="2231f-107">Importante</span><span class="sxs-lookup"><span data-stu-id="2231f-107">Important</span></span>**  
<span data-ttu-id="2231f-108">L'amministrazione e il monitoraggio di Microsoft BitLocker usano chiavi di ripristino monouso che scadono al momento dell'uso.</span><span class="sxs-lookup"><span data-stu-id="2231f-108">Microsoft BitLocker Administration and Monitoring uses single-use recovery keys that expire upon use.</span></span> <span data-ttu-id="2231f-109">L'uso singolo di una password di ripristino viene applicato automaticamente alle unità del sistema operativo e alle unità fisse.</span><span class="sxs-lookup"><span data-stu-id="2231f-109">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="2231f-110">In unità rimovibili viene applicata quando l'unità viene rimossa e quindi reinserita e sbloccata in un computer in cui sono attivate le impostazioni dei criteri di gruppo per gestire le unità rimovibili.</span><span class="sxs-lookup"><span data-stu-id="2231f-110">On removable drives, it is applied when the drive is removed and then re-inserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="2231f-111">Per recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="2231f-111">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="2231f-112">Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="2231f-112">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="2231f-113">Nel riquadro di spostamento fare clic su **ripristino unità**.</span><span class="sxs-lookup"><span data-stu-id="2231f-113">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="2231f-114">Verrà visualizzata la pagina Web "Recupera accesso a un'unità crittografata".</span><span class="sxs-lookup"><span data-stu-id="2231f-114">The “Recover access to an encrypted drive” webpage opens.</span></span>

3.  <span data-ttu-id="2231f-115">Immettere il dominio di accesso di Windows e il nome utente dell'utente per visualizzare le informazioni di ripristino e le prime otto cifre dell'ID chiave di ripristino per ricevere un elenco di possibili chiavi di ripristino corrispondenti o dell'intero ID chiave di ripristino per ricevere l'esatta chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2231f-115">Enter the Windows Logon domain and user name of the user to view recovery information and the first eight digits of the recovery key ID to receive a list of possible matching recovery keys or the entire recovery key ID to receive the exact recovery key.</span></span>

4.  <span data-ttu-id="2231f-116">Selezionare una delle opzioni predefinite dall'elenco **motivo per l'unità di sblocco** e quindi fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="2231f-116">Select one of the predefined options from the **Reason for Drive Unlock** list, and then click **Submit**.</span></span>

    **<span data-ttu-id="2231f-117">Nota</span><span class="sxs-lookup"><span data-stu-id="2231f-117">Note</span></span>**  
    <span data-ttu-id="2231f-118">Se si è un utente di MBAM Advanced helpdesk, le voci di dominio utente e ID utente non sono necessarie.</span><span class="sxs-lookup"><span data-stu-id="2231f-118">If you are an MBAM Advanced Helpdesk user, the user domain and user ID entries are not required.</span></span>



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. <span data-ttu-id="2231f-119">Per copiare la password, fare clic su **copia chiave**e quindi incollare la password di ripristino in un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2231f-119">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="2231f-120">In alternativa, fare clic su **Salva** per salvare la password di ripristino in un file.</span><span class="sxs-lookup"><span data-stu-id="2231f-120">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="2231f-121">Quando l'utente digita la password di ripristino nel sistema o usa il pacchetto di ripristino, l'unità viene sbloccata.</span><span class="sxs-lookup"><span data-stu-id="2231f-121">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="2231f-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2231f-122">Related topics</span></span>


[<span data-ttu-id="2231f-123">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="2231f-123">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









