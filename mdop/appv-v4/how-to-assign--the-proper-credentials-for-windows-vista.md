---
title: Come assegnare le credenziali appropriate per Windows Vista
description: Come assegnare le credenziali appropriate per Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821366"
---
# <span data-ttu-id="e6ca6-103">Come assegnare le credenziali appropriate per Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6ca6-103">How to Assign the Proper Credentials for Windows Vista</span></span>


<span data-ttu-id="e6ca6-104">Usare la procedura seguente per configurare il client desktop di App-V per le credenziali di WindowsVista appropriate.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsVista credentials.</span></span>

<span data-ttu-id="e6ca6-105">**Nota**  Questa procedura deve essere completata in ogni computer non appartenente a un dominio.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-105">**Note** This procedure must be completed on each non-domain joined computer.</span></span> <span data-ttu-id="e6ca6-106">A seconda del numero di computer non appartenenti a un dominio nell'ambiente, potrebbe trattarsi di un'operazione molto noiosa.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-106">Depending on the number of non-domain joined computers in your environment, this could be a very tedious operation.</span></span> <span data-ttu-id="e6ca6-107">Puoi usare gli script e l'interfaccia della riga di comando per Gestione credenziali per consentire agli amministratori di automatizzare questo processo.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-107">You can use scripts and the command-line interface for Credential Manager to help administrators automate this process.</span></span>

 

**<span data-ttu-id="e6ca6-108">Per assegnare le credenziali appropriate per i client App-V che utilizzano Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6ca6-108">To assign the proper credentials for App-V clients running Windows Vista</span></span>**

1.  <span data-ttu-id="e6ca6-109">Con i privilegi di amministratore sul client Desktop App-V che utilizza Windows Vista, aprire il pannello di controllo **degli account utente** (pannello di controllo classico).</span><span class="sxs-lookup"><span data-stu-id="e6ca6-109">With administrator privileges on the App-V Desktop Client running Windows Vista, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="e6ca6-110">Selezionare **Gestisci le password di rete** dagli **account utente** nel riquadro attività a sinistra.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-110">Select **Manage your network passwords** from **User Accounts** in the left tasks pane.</span></span>

3.  <span data-ttu-id="e6ca6-111">Selezionare **Aggiungi** nella schermata **archivia nomi utente e password** .</span><span class="sxs-lookup"><span data-stu-id="e6ca6-111">Select **Add** on the **Stored User Names and Passwords** screen.</span></span>

4.  <span data-ttu-id="e6ca6-112">Nella schermata **Proprietà credenziali archiviate** fornisci le informazioni per l'infrastruttura App-V:</span><span class="sxs-lookup"><span data-stu-id="e6ca6-112">On the **Stored Credential Properties** screen, provide the information for the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="e6ca6-113">**Accedere a:** Nome esterno del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-113">**Log on to:** External name of the publishing server.</span></span>

    2.  <span data-ttu-id="e6ca6-114">**Nome utente:** Nome utente per l'utente esterno nel formato Domain\\Username.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-114">**User name:** User name for the external user in the form Domain\\Username.</span></span>

    3.  <span data-ttu-id="e6ca6-115">**Password:** Password per l'account utente immesso nel campo **nome utente** .</span><span class="sxs-lookup"><span data-stu-id="e6ca6-115">**Password:** Password for the user account entered in the **User name** field.</span></span>

    4.  <span data-ttu-id="e6ca6-116">Uscire dal **tipo di credenziali** selezionato e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-116">Leave **Credential Type** selected, and click **OK**.</span></span>

5.  <span data-ttu-id="e6ca6-117">Fai clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-117">Click **Close**.</span></span> <span data-ttu-id="e6ca6-118">Le credenziali sono archiviate nell'archivio credenziali per l'autenticazione corretta per l'infrastruttura App-V.</span><span class="sxs-lookup"><span data-stu-id="e6ca6-118">The credentials are stored in the credential store for proper authentication to the App-V infrastructure.</span></span>

## <span data-ttu-id="e6ca6-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6ca6-119">Related topics</span></span>


[<span data-ttu-id="e6ca6-120">Client aggiunti e non aggiunti a un dominio</span><span class="sxs-lookup"><span data-stu-id="e6ca6-120">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="e6ca6-121">Come assegnare le credenziali appropriate per Windows XP</span><span class="sxs-lookup"><span data-stu-id="e6ca6-121">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





