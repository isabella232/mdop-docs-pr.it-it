---
title: Come negare l'accesso a un'applicazione
description: Come negare l'accesso a un'applicazione
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817516"
---
# <span data-ttu-id="7ba32-103">Come negare l'accesso a un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7ba32-103">How to Deny Access to an Application</span></span>


<span data-ttu-id="7ba32-104">Gli utenti devono essere nell'elenco **delle autorizzazioni di accesso** di un'applicazione per caricare e usare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ba32-104">Users must be in an application's **Access Permissions** list to load and use the application.</span></span> <span data-ttu-id="7ba32-105">Anche se la console di gestione server Application Virtualization non supporta esplicitamente la negazione di un gruppo di utenti per l'accesso a un'applicazione, è possibile rimuovere i gruppi di utenti dalle proprietà di un'applicazione per ottenere questo risultato.</span><span class="sxs-lookup"><span data-stu-id="7ba32-105">Although the Application Virtualization Server Management Console does not support explicitly denying a user group access to an application, you can remove the user groups from an application’s properties to achieve this.</span></span>

**<span data-ttu-id="7ba32-106">Per negare l'accesso a un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7ba32-106">To deny access to an application</span></span>**

1.  <span data-ttu-id="7ba32-107">Per un'applicazione esistente, fare clic sul nodo **applicazioni** nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="7ba32-107">For an existing application, click the **Applications** node in the left pane.</span></span>

2.  <span data-ttu-id="7ba32-108">Fare clic con il pulsante destro del mouse su un'applicazione nel riquadro destro e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="7ba32-108">Right-click an application in the right pane, and choose **Properties**.</span></span> <span data-ttu-id="7ba32-109">Quindi selezionare la scheda **autorizzazioni di accesso** .</span><span class="sxs-lookup"><span data-stu-id="7ba32-109">Then select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="7ba32-110">Per rimuovere l'accesso per un gruppo di utenti, evidenziare il gruppo di utenti e fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="7ba32-110">To remove access for a user group, highlight the user group and click **Remove**.</span></span>

4.  <span data-ttu-id="7ba32-111">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ba32-111">Click **OK**.</span></span>

    <span data-ttu-id="7ba32-112">**Nota**  Per controllare l'accesso alle applicazioni, puoi anche limitare le licenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ba32-112">**Note** To control access to applications, you can also limit the application licenses.</span></span> <span data-ttu-id="7ba32-113">La configurazione dei gruppi di utenti appropriati in servizi di dominio Active Directory offre il modo più semplice per concedere e negare l'accesso a set di utenti specifici.</span><span class="sxs-lookup"><span data-stu-id="7ba32-113">Setting up the proper user groups in Active Directory Domain Services provides the easiest way to grant and deny access to specific sets of users.</span></span>

     

## <span data-ttu-id="7ba32-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ba32-114">Related topics</span></span>


[<span data-ttu-id="7ba32-115">Come concedere l'accesso a un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7ba32-115">How to Grant Access to an Application</span></span>](how-to-grant-access-to-an-application.md)

[<span data-ttu-id="7ba32-116">Come gestire le licenze dell'applicazione in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="7ba32-116">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="7ba32-117">Come gestire le applicazioni in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="7ba32-117">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





