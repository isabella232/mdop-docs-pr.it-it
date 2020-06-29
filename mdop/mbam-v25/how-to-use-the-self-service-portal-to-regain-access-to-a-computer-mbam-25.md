---
title: Come usare il portale self-service per riottenere l'accesso a un computer
description: Come usare il portale self-service per riottenere l'accesso a un computer
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826705"
---
# <span data-ttu-id="8e45e-103">Come usare il portale self-service per riottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="8e45e-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="8e45e-104">Il portale self-service è un sito Web che gli amministratori IT configurano come parte della propria distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="8e45e-104">The Self-Service Portal is a website that IT administrators configure as part of their Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 deployment.</span></span> <span data-ttu-id="8e45e-105">Il sito Web consente agli utenti finali di recuperare in modo indipendente l'accesso ai propri computer se vengono bloccati da Windows.</span><span class="sxs-lookup"><span data-stu-id="8e45e-105">The website enables end users to independently regain access to their computers if they get locked out of Windows.</span></span> <span data-ttu-id="8e45e-106">Il portale self-service non richiede assistenza dal personale dell'help desk.</span><span class="sxs-lookup"><span data-stu-id="8e45e-106">The Self-Service Portal requires no assistance from Help Desk staff.</span></span>

<span data-ttu-id="8e45e-107">Le istruzioni seguenti vengono scritte dal punto di vista degli utenti finali, ma le informazioni potrebbero essere utili per gli amministratori IT.</span><span class="sxs-lookup"><span data-stu-id="8e45e-107">The following instructions are written from the perspective of end users, but the information may be useful for IT administrators to understand.</span></span>

<span data-ttu-id="8e45e-108">**Importante**  Un utente finale deve avere eseguito fisicamente l'accesso al computer (non in remoto) almeno una volta con successo per poter recuperare la chiave usando il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="8e45e-108">**Important** An end user must have physically logged on to the computer (not remotely) at least one time successfully to be able to recover their key using the Self-Service Portal.</span></span> <span data-ttu-id="8e45e-109">In caso contrario, deve usare il portale helpdesk per il ripristino della chiave.</span><span class="sxs-lookup"><span data-stu-id="8e45e-109">Otherwise, they must use the Helpdesk Portal for key recovery.</span></span>

 

<span data-ttu-id="8e45e-110">Gli utenti finali possono verificare i blocchi se:</span><span class="sxs-lookup"><span data-stu-id="8e45e-110">End users may experience lockouts if they:</span></span>

-   <span data-ttu-id="8e45e-111">Dimenticare la password o il PIN</span><span class="sxs-lookup"><span data-stu-id="8e45e-111">Forget their password or PIN</span></span>

-   <span data-ttu-id="8e45e-112">Modificare i file di sistema operativo, il BIOS o il Trusted Platform Module (TPM)</span><span class="sxs-lookup"><span data-stu-id="8e45e-112">Change operating system files, the BIOS, or the Trusted Platform Module (TPM)</span></span>

<span data-ttu-id="8e45e-113">**Nota**  Se l'amministratore IT ha configurato un timeout per lo stato sessione di IIS, viene visualizzato un messaggio nel portale self-service 60 secondi prima del timeout.</span><span class="sxs-lookup"><span data-stu-id="8e45e-113">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed in the Self-Service Portal 60 seconds prior to the time-out.</span></span>

 

**<span data-ttu-id="8e45e-114">Per usare il portale self-service per ottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="8e45e-114">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="8e45e-115">Nel campo **Recovery keyId** immettere un minimo di otto dell'ID della chiave bitlocker di 32 cifre visualizzato nella schermata di ripristino di BitLocker del computer.</span><span class="sxs-lookup"><span data-stu-id="8e45e-115">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span> <span data-ttu-id="8e45e-116">Se le prime otto cifre corrispondono a più tasti, viene visualizzato un messaggio che richiede l'immissione di tutte le cifre di 32 dell'ID chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8e45e-116">If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

2.  <span data-ttu-id="8e45e-117">Nel campo **motivo** selezionare un motivo per la richiesta per il tasto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8e45e-117">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="8e45e-118">Fare clic su **Ottieni chiave**.</span><span class="sxs-lookup"><span data-stu-id="8e45e-118">Click **Get Key**.</span></span> <span data-ttu-id="8e45e-119">La chiave di ripristino di BitLocker viene visualizzata nel campo **chiave di ripristino di BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="8e45e-119">Your BitLocker recovery key is displayed in the **Your BitLocker Recovery Key** field.</span></span>

4.  <span data-ttu-id="8e45e-120">Immettere il codice a 48 cifre nella schermata di ripristino di BitLocker nel computer per ottenere l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="8e45e-120">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>



## <span data-ttu-id="8e45e-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e45e-121">Related topics</span></span>


[<span data-ttu-id="8e45e-122">Gestione di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8e45e-122">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="8e45e-123">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="8e45e-123">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8e45e-124">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8e45e-124">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8e45e-125">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8e45e-125">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





