---
title: Come configurare le autorizzazioni utente
description: Come configurare le autorizzazioni utente
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817735"
---
# <span data-ttu-id="2ca1d-103">Come configurare le autorizzazioni utente</span><span class="sxs-lookup"><span data-stu-id="2ca1d-103">How to Configure User Permissions</span></span>


<span data-ttu-id="2ca1d-104">È possibile abilitare e disabilitare alcune azioni per gli utenti che non hanno diritti amministrativi modificando i valori chiave nella chiave del registro di sistema **delle autorizzazioni** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions).</span><span class="sxs-lookup"><span data-stu-id="2ca1d-104">You can enable and disable some actions for users who do not have administrative rights by editing the key values under the **Permissions** registry key (HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions).</span></span> <span data-ttu-id="2ca1d-105">Questa chiave è progettata principalmente per impedire agli utenti di commettere errori anziché fornire una sicurezza speciale, perché gli utenti con diritti amministrativi possono modificare uno di questi valori chiave.</span><span class="sxs-lookup"><span data-stu-id="2ca1d-105">This key is primarily designed to help prevent users from making mistakes rather than to provide any special security, because users with administrative rights can edit any of these key values.</span></span> <span data-ttu-id="2ca1d-106">Le procedure seguenti sono esempi di come modificare i valori di chiave.</span><span class="sxs-lookup"><span data-stu-id="2ca1d-106">The following procedures are examples of how to change the key values.</span></span> <span data-ttu-id="2ca1d-107">Per altre informazioni sulle chiavi e i valori del registro di sistema client Application Virtualization (App-V), vedere <https://go.microsoft.com/fwlink/?LinkId=121528> .</span><span class="sxs-lookup"><span data-stu-id="2ca1d-107">For more information about the Application Virtualization (App-V) Client registry keys and values, see <https://go.microsoft.com/fwlink/?LinkId=121528>.</span></span>

**<span data-ttu-id="2ca1d-108">Per modificare le autorizzazioni utente</span><span class="sxs-lookup"><span data-stu-id="2ca1d-108">To change user permissions</span></span>**

1.  <span data-ttu-id="2ca1d-109">Per consentire agli utenti di scegliere di eseguire il client in modalità offline, impostare il valore della chiave seguente su 1:</span><span class="sxs-lookup"><span data-stu-id="2ca1d-109">To enable the users to choose to run the client in offline mode, set the following key value to 1:</span></span>

    <span data-ttu-id="2ca1d-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="2ca1d-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span></span>

2.  <span data-ttu-id="2ca1d-111">Per consentire agli utenti di visualizzare tutte le applicazioni tramite l'interfaccia utente, impostare il valore della chiave seguente su 1.</span><span class="sxs-lookup"><span data-stu-id="2ca1d-111">To enable the users to view all applications through the user interface, set the following key value to 1.</span></span> <span data-ttu-id="2ca1d-112">L'impostazione del valore su 0 (zero) consente agli utenti di visualizzare solo le applicazioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="2ca1d-112">Setting the value to 0 (zero) allows the users to see only the applications that are available to them.</span></span>

    <span data-ttu-id="2ca1d-113">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="2ca1d-113">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span></span>

## <span data-ttu-id="2ca1d-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ca1d-114">Related topics</span></span>


[<span data-ttu-id="2ca1d-115">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="2ca1d-115">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[<span data-ttu-id="2ca1d-116">Autorizzazioni di accesso utente in Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="2ca1d-116">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





