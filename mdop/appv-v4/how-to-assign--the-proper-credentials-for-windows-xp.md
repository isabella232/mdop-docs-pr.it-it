---
title: Come assegnare le credenziali appropriate per Windows XP
description: Come assegnare le credenziali appropriate per Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819325"
---
# <span data-ttu-id="e36ff-103">Come assegnare le credenziali appropriate per Windows XP</span><span class="sxs-lookup"><span data-stu-id="e36ff-103">How to Assign the Proper Credentials for Windows XP</span></span>


<span data-ttu-id="e36ff-104">Usare la procedura seguente per configurare il client Desktop App-V per le credenziali WindowsXP appropriate.</span><span class="sxs-lookup"><span data-stu-id="e36ff-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsXP credentials.</span></span>

<span data-ttu-id="e36ff-105">**Nota**  Dopo aver completato questa procedura, il client non collegato al dominio può eseguire un aggiornamento della pubblicazione senza essere associato a un dominio.</span><span class="sxs-lookup"><span data-stu-id="e36ff-105">**Note** After finishing this procedure, the non-domain joined client can perform a publishing refresh without being joined to a domain.</span></span>

 

**<span data-ttu-id="e36ff-106">Per assegnare le credenziali appropriate per i client App-V in cui è in uso WindowsXP</span><span class="sxs-lookup"><span data-stu-id="e36ff-106">To assign the proper credentials for App-V clients running WindowsXP</span></span>**

1.  <span data-ttu-id="e36ff-107">Con i privilegi di amministratore nel client App-V in cui è in uso WindowsXP, aprire il pannello di controllo **degli account utente** (pannello di controllo classico).</span><span class="sxs-lookup"><span data-stu-id="e36ff-107">With administrator privileges on the App-V Client running WindowsXP, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="e36ff-108">Fare clic sulla **scheda Avanzate**e selezionare **Gestisci password**.</span><span class="sxs-lookup"><span data-stu-id="e36ff-108">Click the **Advanced Tab**, and select **Manage Passwords**.</span></span>

3.  <span data-ttu-id="e36ff-109">Nella schermata **archiviazione nomi utente e password** fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="e36ff-109">On the **Stored User Names and Passwords** screen, click **Add**.</span></span>

4.  <span data-ttu-id="e36ff-110">Nella schermata **Proprietà informazioni di accesso** compilare i campi seguenti con le informazioni dell'infrastruttura App-V:</span><span class="sxs-lookup"><span data-stu-id="e36ff-110">On the **Logon Information Properties** screen, fill out the following fields with information from the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="e36ff-111">**Server:** Nome del nome del server di pubblicazione esterno.</span><span class="sxs-lookup"><span data-stu-id="e36ff-111">**Server:** Name of publishing server external name.</span></span>

    2.  <span data-ttu-id="e36ff-112">**Nome utente:** Nome utente per utenti esterni nel modulo Domain\\username.</span><span class="sxs-lookup"><span data-stu-id="e36ff-112">**User name:** User name for external user in the form Domain\\username.</span></span>

    3.  <span data-ttu-id="e36ff-113">**Password:** Password per l'account utente immesso nel campo **nome utente** .</span><span class="sxs-lookup"><span data-stu-id="e36ff-113">**Password:** Password for the user account entered in the **User name** field.</span></span>

5.  <span data-ttu-id="e36ff-114">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e36ff-114">Click **OK**.</span></span> <span data-ttu-id="e36ff-115">Le credenziali verranno archiviate nel client.</span><span class="sxs-lookup"><span data-stu-id="e36ff-115">The credentials will be stored on the client.</span></span>

## <span data-ttu-id="e36ff-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e36ff-116">Related topics</span></span>


[<span data-ttu-id="e36ff-117">Client aggiunti e non aggiunti a un dominio</span><span class="sxs-lookup"><span data-stu-id="e36ff-117">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="e36ff-118">Come assegnare le credenziali appropriate per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e36ff-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





