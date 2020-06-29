---
title: Come ripristinare un blocco del TPM
description: Come ripristinare un blocco del TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825055"
---
# <span data-ttu-id="8b7e8-103">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="8b7e8-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="8b7e8-104">La caratteristica di ripristino delle unità crittografata di Microsoft BitLocker Administration and Monitoring (MBAM) include sia l'acquisizione che l'archiviazione dei dati e la disponibilità per gli strumenti necessari per gestire il TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="8b7e8-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are needed to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="8b7e8-105">Questo argomento illustra come accedere al sistema di dati di ripristino della chiave centralizzata nel sito Web di amministrazione e monitoraggio, che può fornire un file di password del proprietario del TPM quando viene fornito un ID computer e un Identificativo utente associato.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-105">This topic covers how to access the centralized Key Recovery data system in the Administration and Monitoring website, which can provide a TPM owner password file when a computer ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="8b7e8-106">Se un utente immette il PIN errato troppe volte, può verificarsi un blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-106">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="8b7e8-107">Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino da produttore a produttore.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-107">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="8b7e8-108">È possibile reimpostare un blocco TPM solo se MBAM è proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-108">You can reset a TPM lockout only if MBAM owns the TPM.</span></span>

**<span data-ttu-id="8b7e8-109">Per reimpostare un blocco TPM</span><span class="sxs-lookup"><span data-stu-id="8b7e8-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="8b7e8-110">Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-110">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="8b7e8-111">Nel riquadro di spostamento sinistro selezionare **Gestisci TPM** per aprire la pagina **Manage TPM** .</span><span class="sxs-lookup"><span data-stu-id="8b7e8-111">In the left navigation pane, select **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="8b7e8-112">Immettere il nome di dominio completo per il computer e il nome del computer e immettere il dominio di accesso di Windows dell'utente e il nome utente dell'utente per recuperare il file della password del proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-112">Enter the fully qualified domain name for the computer and the computer name, and enter the user’s Windows logon domain and the user’s user name to retrieve the TPM owner password file.</span></span>

4.  <span data-ttu-id="8b7e8-113">Dal **motivo per richiedere** l'elenco dei file di password del proprietario del TPM selezionare un motivo per la richiesta e fare clic su **Invia**.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-113">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="8b7e8-114">MBAM restituisce una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b7e8-114">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="8b7e8-115">Messaggio di errore, se non viene trovato un file di password del proprietario del TPM corrispondente</span><span class="sxs-lookup"><span data-stu-id="8b7e8-115">An error message, if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="8b7e8-116">File di password del proprietario del TPM per il computer inviato</span><span class="sxs-lookup"><span data-stu-id="8b7e8-116">The TPM owner password file for the submitted computer</span></span>

    **<span data-ttu-id="8b7e8-117">Nota</span><span class="sxs-lookup"><span data-stu-id="8b7e8-117">Note</span></span>**  
    <span data-ttu-id="8b7e8-118">Se si è un utente di helpdesk avanzato, il dominio utente e i campi ID utente non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-118">If you are an Advanced Helpdesk user, the user domain and user ID fields are not required.</span></span>



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. <span data-ttu-id="8b7e8-119">Per salvare la password in un file con estensione TPM, fare clic sul pulsante **Salva** .</span><span class="sxs-lookup"><span data-stu-id="8b7e8-119">To save the password to a .tpm file, click the **Save** button.</span></span>

   <span data-ttu-id="8b7e8-120">L'utente eseguirà la console di gestione TPM, selezionerà l'opzione **Reimposta il blocco TPM** e fornirà il file della password del proprietario del TPM per reimpostare il blocco TPM.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-120">The user will run the TPM management console, select the **Reset TPM lockout** option, and provide the TPM owner password file to reset the TPM lockout.</span></span>

   **<span data-ttu-id="8b7e8-121">Importante</span><span class="sxs-lookup"><span data-stu-id="8b7e8-121">Important</span></span>**  
   <span data-ttu-id="8b7e8-122">Gli amministratori del supporto tecnico non devono assegnare al file di password del valore hash TPM o del proprietario del TPM agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-122">Help Desk administrators should not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="8b7e8-123">Le informazioni sul TPM non cambiano, quindi potrebbero rappresentare un rischio per la sicurezza se il file viene assegnato agli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="8b7e8-123">The TPM information does not change, so it could pose a security risk if the file is given to end users.</span></span>



## <span data-ttu-id="8b7e8-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b7e8-124">Related topics</span></span>


[<span data-ttu-id="8b7e8-125">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="8b7e8-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









