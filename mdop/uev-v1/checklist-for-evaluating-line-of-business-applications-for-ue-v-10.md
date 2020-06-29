---
title: Elenco di controllo per valutare le applicazioni line-of-business per UE-V 1.0
description: Elenco di controllo per valutare le applicazioni line-of-business per UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826456"
---
# <span data-ttu-id="dca3b-103">Elenco di controllo per valutare le applicazioni line-of-business per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="dca3b-103">Checklist for Evaluating Line-of-Business Applications for UE-V 1.0</span></span>


<span data-ttu-id="dca3b-104">Per valutare le applicazioni line-of-business da includere nella distribuzione UE-V, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="dca3b-104">To evaluate which line-of-business applications should be included in your UE-V deployment, consider the following:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="dca3b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca3b-105">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dca3b-106">Questa applicazione contiene le impostazioni che l'utente può personalizzare?</span><span class="sxs-lookup"><span data-stu-id="dca3b-106">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dca3b-107">È importante per l'utente che queste impostazioni si aggirano?</span><span class="sxs-lookup"><span data-stu-id="dca3b-107">Is it important for the user that these settings roam?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dca3b-108">Queste impostazioni utente sono già gestite da una soluzione dei criteri di gestione o impostazioni delle applicazioni?</span><span class="sxs-lookup"><span data-stu-id="dca3b-108">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="dca3b-109">UE-V applica le impostazioni dell'applicazione all'avvio dell'applicazione e alle impostazioni di Windows agli eventi logon, Unlock o Connect remoto.</span><span class="sxs-lookup"><span data-stu-id="dca3b-109">UE-V applies application settings at application launch and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="dca3b-110">Se si usa UE-V con altre soluzioni per i criteri di impostazioni, gli utenti potrebbero riscontrare incongruenze tra le impostazioni in roaming.</span><span class="sxs-lookup"><span data-stu-id="dca3b-110">If you use UE-V with other settings policy solutions, users might experience inconsistency across roamed settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dca3b-111">Le impostazioni dell'applicazione sono specifiche per il computer?</span><span class="sxs-lookup"><span data-stu-id="dca3b-111">Are the application settings specific to the computer?</span></span> <span data-ttu-id="dca3b-112">Le preferenze e le personalizzazioni delle applicazioni associate all'hardware o alle configurazioni di computer specifiche non si aggirano in modo coerente tra le sessioni e possono causare un'esperienza di applicazione insufficiente.</span><span class="sxs-lookup"><span data-stu-id="dca3b-112">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently roam across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dca3b-113">Le impostazioni dell'archivio applicazioni si trovano nella directory Program Files o nella directory di file che si trova nella <strong> Directory Users </strong> \ [user name] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ?</span><span class="sxs-lookup"><span data-stu-id="dca3b-113">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong> \ [User name] \ <strong>AppData</strong> \ <strong>LocalLow</strong> directory?</span></span> <span data-ttu-id="dca3b-114">I dati dell'applicazione archiviati in uno di questi percorsi in genere non devono essere spostati con l'utente, perché questi dati sono specifici del computer o perché i dati sono troppo grandi per spostarsi in roaming.</span><span class="sxs-lookup"><span data-stu-id="dca3b-114">Application data that is stored in either of these locations usually should not roam with the user, because this data is specific to the computer or because the data is too large to roam.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dca3b-115">L'applicazione archivia le impostazioni in un file che contiene altri dati dell'applicazione che non devono essere spostati?</span><span class="sxs-lookup"><span data-stu-id="dca3b-115">Does the application store any settings in a file that contains other application data that should not roam?</span></span> <span data-ttu-id="dca3b-116">UE-V sincronizza i file come unità singola.</span><span class="sxs-lookup"><span data-stu-id="dca3b-116">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="dca3b-117">Se le impostazioni sono archiviate in file che includono dati dell'applicazione diversi dalle impostazioni, la sincronizzazione di questi dati aggiuntivi può causare un'esperienza di applicazione insufficiente.</span><span class="sxs-lookup"><span data-stu-id="dca3b-117">If settings are stored in files that include application data other than settings, then synchronizing this additional data may cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="dca3b-118">Dimensioni dei file che contengono le impostazioni</span><span class="sxs-lookup"><span data-stu-id="dca3b-118">How large are the files that contain the settings?</span></span> <span data-ttu-id="dca3b-119">Le prestazioni della sincronizzazione delle impostazioni possono essere influenzate da file di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="dca3b-119">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="dca3b-120">L'inclusione di file di grandi dimensioni può influire sulle prestazioni della sincronizzazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="dca3b-120">Including large files can impact the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="dca3b-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dca3b-121">Related topics</span></span>


[<span data-ttu-id="dca3b-122">Pianificazione per i metodi di configurazione di UE-V</span><span class="sxs-lookup"><span data-stu-id="dca3b-122">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

[<span data-ttu-id="dca3b-123">Pianificazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="dca3b-123">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

 

 





