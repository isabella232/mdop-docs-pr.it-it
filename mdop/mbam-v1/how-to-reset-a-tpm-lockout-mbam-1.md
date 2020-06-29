---
title: Come ripristinare un blocco del TPM
description: Come ripristinare un blocco del TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804588"
---
# <span data-ttu-id="915ed-103">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="915ed-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="915ed-104">La caratteristica di ripristino delle unità crittografata di Microsoft BitLocker Administration and Monitoring (MBAM) include sia l'acquisizione che l'archiviazione dei dati e la disponibilità per gli strumenti necessari per la gestione del TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="915ed-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are required to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="915ed-105">Questo argomento illustra come accedere al sistema di dati di ripristino centralizzato delle chiavi nel sito Web di bit \ _admmon \ _tlanextref amministrazione.</span><span class="sxs-lookup"><span data-stu-id="915ed-105">This topic covers how to access the centralized Key Recovery data system in the bit\_admmon\_tlanextref administration website.</span></span> <span data-ttu-id="915ed-106">Il sistema di dati di ripristino della chiave può fornire un file di password del proprietario del TPM quando viene fornita l'identità del computer e l'identificatore dell'utente associato.</span><span class="sxs-lookup"><span data-stu-id="915ed-106">The Key Recovery data system can provide a TPM owner password file when the computer identity and the associated user identifier are supplied.</span></span>

<span data-ttu-id="915ed-107">Se un utente immette un PIN errato troppo spesso, può verificarsi un blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="915ed-107">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="915ed-108">Numero di volte in cui un utente può immettere un PIN errato prima che il blocco TPM sia basato sulla specifica del produttore del computer.</span><span class="sxs-lookup"><span data-stu-id="915ed-108">The number of times that a user can enter an incorrect PIN before the TPM lockout is based on the computer manufacturer's specification.</span></span>

**<span data-ttu-id="915ed-109">Per reimpostare un blocco TPM</span><span class="sxs-lookup"><span data-stu-id="915ed-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="915ed-110">Aprire il sito Web di amministrazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="915ed-110">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="915ed-111">Nel riquadro di spostamento selezionare **Gestisci TPM**.</span><span class="sxs-lookup"><span data-stu-id="915ed-111">In the navigation pane, select **Manage TPM**.</span></span> <span data-ttu-id="915ed-112">Verrà aperta la pagina **Manage TPM** .</span><span class="sxs-lookup"><span data-stu-id="915ed-112">This opens the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="915ed-113">Immettere il nome di dominio completo (FQDN) per il computer e il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="915ed-113">Enter the fully qualified domain name (FQDN) for the computer and the computer name.</span></span> <span data-ttu-id="915ed-114">Immettere il dominio di accesso di Windows dell'utente e il nome utente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="915ed-114">Enter the user’s Windows Logon domain and the user’s user name.</span></span> <span data-ttu-id="915ed-115">Selezionare una delle opzioni predefinite nel **motivo per richiedere** il menu a discesa file di password del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="915ed-115">Select one of the predefined options in the **Reason for requesting TPM owner password file** drop-down menu.</span></span> <span data-ttu-id="915ed-116">Fai clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="915ed-116">Click **Submit**.</span></span>

4.  <span data-ttu-id="915ed-117">MBAM restituirà una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="915ed-117">MBAM will return one of the following:</span></span>

    -   <span data-ttu-id="915ed-118">Messaggio di errore se non viene trovato un file di password del proprietario del TPM corrispondente</span><span class="sxs-lookup"><span data-stu-id="915ed-118">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="915ed-119">File di password del proprietario del TPM per il computer inviato</span><span class="sxs-lookup"><span data-stu-id="915ed-119">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="915ed-120">**Nota**  Se si è un utente di helpdesk avanzato, il dominio utente e i campi ID utente non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="915ed-120">**Note** If you are an Advanced Helpdesk User, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="915ed-121">Al momento del recupero viene visualizzata la password del proprietario.</span><span class="sxs-lookup"><span data-stu-id="915ed-121">Upon retrieval, the owner password is displayed.</span></span> <span data-ttu-id="915ed-122">Per salvare la password in un file con estensione TPM, fare clic sul pulsante **Salva** .</span><span class="sxs-lookup"><span data-stu-id="915ed-122">To save this password to a .tpm file, click the **Save** button.</span></span>

6.  <span data-ttu-id="915ed-123">L'utente eseguirà la console di gestione TPM e selezionerà l'opzione **Reimposta il blocco TPM** e fornirà il file della password del proprietario del TPM per reimpostare il blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="915ed-123">The user will run the TPM management console and select the **Reset TPM lockout** option and provide the TPM owner password file to reset the TPM lockout.</span></span>

## <span data-ttu-id="915ed-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="915ed-124">Related topics</span></span>


[<span data-ttu-id="915ed-125">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="915ed-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





