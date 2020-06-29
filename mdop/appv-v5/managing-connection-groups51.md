---
title: Gestione dei gruppi di connessione
description: Gestione dei gruppi di connessione
author: dansimp
ms.assetid: 22c9d3cb-7246-4173-9742-4ba1c24b0a6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c89fab70fa13a66c2c27b8d014a5bac034f21bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805079"
---
# <span data-ttu-id="ea3a3-103">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="ea3a3-103">Managing Connection Groups</span></span>


<span data-ttu-id="ea3a3-104">I gruppi di connessioni consentono alle applicazioni all'interno di un pacchetto di interagire tra loro nell'ambiente virtuale, pur rimanendo isolate dal resto del sistema.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="ea3a3-105">Usando i gruppi di connessioni, gli amministratori possono gestire i pacchetti in modo indipendente e possono evitare di dover aggiungere più volte la stessa applicazione a un computer client.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="ea3a3-106">**Nota**  In alcune versioni precedenti di App-V i gruppi di connessioni venivano definiti composizione della famiglia dinamica.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-106">**Note** In some previous versions of App-V, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="ea3a3-107">In questo argomento:</span><span class="sxs-lookup"><span data-stu-id="ea3a3-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment51.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment51.md)"><span data-ttu-id="ea3a3-108">Informazioni sull'ambiente virtuale del gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="ea3a3-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ea3a3-109">Descrive l'ambiente virtuale del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file51.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file51.md)"><span data-ttu-id="ea3a3-110">Informazioni sul file del gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="ea3a3-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ea3a3-111">Descrive il file del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group51.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group51.md)"><span data-ttu-id="ea3a3-112">Come creare un gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="ea3a3-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ea3a3-113">Spiega come creare un nuovo gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md)"><span data-ttu-id="ea3a3-114">Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente</span><span class="sxs-lookup"><span data-stu-id="ea3a3-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ea3a3-115">Spiega come creare un nuovo gruppo di connessioni che contiene una combinazione di pacchetti che vengono pubblicati per l'utente e pubblicati globalmente.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group51.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group51.md)"><span data-ttu-id="ea3a3-116">Come eliminare un gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="ea3a3-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ea3a3-117">Spiega come eliminare un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group51.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group51.md)"><span data-ttu-id="ea3a3-118">Come pubblicare un gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="ea3a3-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ea3a3-119">Spiega come pubblicare un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="ea3a3-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="ea3a3-120">Altre risorse per i gruppi di connessioni App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="ea3a3-120">Other resources for App-V 5.1 connection groups</span></span>


-   [<span data-ttu-id="ea3a3-121">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ea3a3-121">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





