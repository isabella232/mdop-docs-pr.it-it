---
title: Come aggiungere o rimuovere un amministratore tramite la console di gestione
description: Come aggiungere o rimuovere un amministratore tramite la console di gestione
author: dansimp
ms.assetid: 7ff8c436-9d2e-446a-9ea2-bbab7e25bf21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8fbc1a532a39c8688b99c28a2e23b713b348967c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805769"
---
# <span data-ttu-id="5b2b4-103">Come aggiungere o rimuovere un amministratore tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="5b2b4-103">How to Add or Remove an Administrator by Using the Management Console</span></span>


<span data-ttu-id="5b2b4-104">Usare le procedure seguenti per aggiungere o rimuovere un amministratore nel server di Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-104">Use the following procedures to add or remove an administrator on the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

**<span data-ttu-id="5b2b4-105">Per aggiungere un amministratore tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="5b2b4-105">To add an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="5b2b4-106">Aprire la console di gestione di Microsoft Application Virtualization (App-V) 5,1 e fare clic su **amministratori** nel riquadro di spostamento.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-106">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="5b2b4-107">Nel riquadro di spostamento viene visualizzato un elenco di utenti e gruppi di Access directory (AD) che attualmente hanno accesso amministrativo al server Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-107">The navigation pane displays a list of Access Directory (AD) users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="5b2b4-108">Per aggiungere un nuovo amministratore, fare clic su **Aggiungi amministratore** Digitare il nome dell'amministratore che si vuole aggiungere nel campo **nome Active Directory** .</span><span class="sxs-lookup"><span data-stu-id="5b2b4-108">To add a new administrator, click **Add Administrator** Type the name of the administrator that you want to add in the **Active Directory Name** field.</span></span> <span data-ttu-id="5b2b4-109">Assicurati di specificare il nome di dominio dell'account utente associato.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-109">Ensure you provide the associated user account domain name.</span></span> <span data-ttu-id="5b2b4-110">Ad esempio, **Domain**  \\  **nome utente**di dominio.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-110">For example, **Domain** \\ **UserName**.</span></span>

3.  <span data-ttu-id="5b2b4-111">Selezionare l'account che si vuole aggiungere e fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-111">Select the account that you want to add and click **Add**.</span></span> <span data-ttu-id="5b2b4-112">Il nuovo account viene visualizzato nell'elenco degli amministratori del server.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-112">The new account is displayed in the list of server administrators.</span></span>

**<span data-ttu-id="5b2b4-113">Per rimuovere un amministratore tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="5b2b4-113">To remove an administrator using the Management Console</span></span>**

1.  <span data-ttu-id="5b2b4-114">Aprire la console di gestione di Microsoft Application Virtualization (App-V) 5,1 e fare clic su **amministratori** nel riquadro di spostamento.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-114">Open the Microsoft Application Virtualization (App-V) 5.1 Management Console and click **Administrators** in the navigation pane.</span></span> <span data-ttu-id="5b2b4-115">Nel riquadro di spostamento viene visualizzato un elenco di utenti e gruppi di annunci che attualmente hanno accesso amministrativo al server Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-115">The navigation pane displays a list of AD users and groups that currently have administrative access to the Microsoft Application Virtualization (App-V) 5.1 server.</span></span>

2.  <span data-ttu-id="5b2b4-116">Fare clic con il pulsante destro del mouse sull'account da rimuovere dall'elenco di amministratori e scegliere **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="5b2b4-116">Right-click the account to be removed from the list of administrators and select **Remove**.</span></span>

    <span data-ttu-id="5b2b4-117">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="5b2b4-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="5b2b4-118">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="5b2b4-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="5b2b4-119">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="5b2b4-119">Got an App-V issue?</span></span>** <span data-ttu-id="5b2b4-120">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5b2b4-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5b2b4-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b2b4-121">Related topics</span></span>


[<span data-ttu-id="5b2b4-122">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5b2b4-122">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





