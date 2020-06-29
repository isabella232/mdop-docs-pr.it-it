---
title: Come usare il portale self-service per riottenere l'accesso a un computer
description: Come usare il portale self-service per riottenere l'accesso a un computer
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826076"
---
# <span data-ttu-id="f0e3c-103">Come usare il portale self-service per riottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="f0e3c-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="f0e3c-104">Se gli utenti finali vengono bloccati da Windows da BitLocker perché hanno dimenticato la password o il PIN oppure perché hanno modificato i file del sistema operativo o hanno modificato il BIOS o il Trusted Platform Module (TPM), possono usare il portale self-service per ottenere l'accesso a Windows senza dover chiedere assistenza al proprio help desk.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-104">If end users get locked out of Windows by BitLocker because they forgot their password or PIN, or because they changed operating system files or changed the BIOS or the Trusted Platform Module (TPM), they can use the Self-Service Portal to regain access to Windows without having to ask their Help Desk for assistance.</span></span>

<span data-ttu-id="f0e3c-105">**Nota**  Se l'amministratore IT ha configurato un timeout per lo stato sessione di IIS, viene visualizzato un messaggio di 60 secondi prima del timeout.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-105">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed 60 seconds prior to the time-out.</span></span>

 

<span data-ttu-id="f0e3c-106">**Nota**  Queste istruzioni sono scritte per e dal punto di vista degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-106">**Note** These instructions are written for and from the perspective of end users.</span></span>

 

**<span data-ttu-id="f0e3c-107">Per usare il portale self-service per ottenere l'accesso a un computer</span><span class="sxs-lookup"><span data-stu-id="f0e3c-107">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="f0e3c-108">Nel campo **Recovery keyId** immettere un minimo di otto dell'ID della chiave bitlocker di 32 cifre visualizzato nella schermata di ripristino di BitLocker del computer.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-108">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span>

    <span data-ttu-id="f0e3c-109">**Nota**  Se le prime otto cifre corrispondono a più tasti, viene visualizzato un messaggio che richiede l'immissione di tutte le cifre di 32 dell'ID chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-109">**Note** If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

     

2.  <span data-ttu-id="f0e3c-110">Nel campo **motivo** selezionare un motivo per la richiesta per il tasto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-110">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="f0e3c-111">Fare clic su **Ottieni chiave**.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-111">Click **Get Key**.</span></span> <span data-ttu-id="f0e3c-112">La chiave di ripristino di BitLocker viene visualizzata nel campo "chiave di ripristino di BitLocker".</span><span class="sxs-lookup"><span data-stu-id="f0e3c-112">Your BitLocker recovery key is displayed in the “Your BitLocker Recovery Key” field.</span></span>

4.  <span data-ttu-id="f0e3c-113">Immettere il codice a 48 cifre nella schermata di ripristino di BitLocker nel computer per ottenere l'accesso al computer.</span><span class="sxs-lookup"><span data-stu-id="f0e3c-113">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>

## <span data-ttu-id="f0e3c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0e3c-114">Related topics</span></span>


[<span data-ttu-id="f0e3c-115">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="f0e3c-115">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





