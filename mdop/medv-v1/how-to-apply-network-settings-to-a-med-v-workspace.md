---
title: Come applicare le impostazioni di rete a un'area di lavoro MED-V
description: Come applicare le impostazioni di rete a un'area di lavoro MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826516"
---
# <span data-ttu-id="15d2f-103">Come applicare le impostazioni di rete a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="15d2f-103">How to Apply Network Settings to a MED-V Workspace</span></span>


<span data-ttu-id="15d2f-104">Gli amministratori possono definire le impostazioni di rete per ogni area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15d2f-104">Administrators can define the network settings for each MED-V workspace.</span></span>

<span data-ttu-id="15d2f-105">Tutte le impostazioni di rete sono configurate nel modulo **criteri** , nella scheda **rete** .</span><span class="sxs-lookup"><span data-stu-id="15d2f-105">All network settings are configured in the **Policy** module, on the **Network** tab.</span></span>

**<span data-ttu-id="15d2f-106">Per applicare le impostazioni di rete a un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="15d2f-106">To apply network settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="15d2f-107">Fare clic sull'area di lavoro MED-V per configurare.</span><span class="sxs-lookup"><span data-stu-id="15d2f-107">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="15d2f-108">Nel riquadro **rete** configurare le impostazioni come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="15d2f-108">In the **Network** pane, configure the settings as described in the following table.</span></span>

3.  <span data-ttu-id="15d2f-109">Nel menu **criteri** selezionare **commit**.</span><span class="sxs-lookup"><span data-stu-id="15d2f-109">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="15d2f-110">Proprietà di rete dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="15d2f-110">MED-V Workspace Network Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="15d2f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="15d2f-111">Property</span></span></th>
<th align="left"><span data-ttu-id="15d2f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15d2f-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15d2f-113">Proprietà TCP/IP</span><span class="sxs-lookup"><span data-stu-id="15d2f-113">TCP/IP Properties</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="15d2f-114">Usa l'indirizzo IP dell'host (NAT) </strong> : l'area di lavoro utilizzerà NAT per condividere l'IP dell'host per il traffico in uscita.</span><span class="sxs-lookup"><span data-stu-id="15d2f-114">Use host's IP address (NAT)</strong>—The workspace will use NAT to share the host's IP for outgoing traffic.</span></span></p></li>
<li><p><strong><span data-ttu-id="15d2f-115">Usare un indirizzo IP diverso da host (Bridge) </strong> : l'area di lavoro MED-V avrà un proprio indirizzo di rete, in genere ottenuto tramite DHCP.</span><span class="sxs-lookup"><span data-stu-id="15d2f-115">Use different IP address than host (Bridge)</strong>—The MED-V workspace will have its own network address, usually obtained via DHCP.</span></span></p></li>
</ul>
<p><span data-ttu-id="15d2f-116">Selezionare la <strong> casella di controllo associa più adattatori all'area </strong> di lavoro quando nel computer host sono presenti più adapter.</span><span class="sxs-lookup"><span data-stu-id="15d2f-116">Select the <strong>Map multiple adapters into Workspace</strong> check box when the host computer has multiple adapters.</span></span> <span data-ttu-id="15d2f-117">È consigliabile usare questa configurazione quando l'host si sposta tra reti diverse usando diversi adapter.</span><span class="sxs-lookup"><span data-stu-id="15d2f-117">It is recommended to use this configuration when the host moves between different networks using different adapters.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="15d2f-118">Server DNS</span><span class="sxs-lookup"><span data-stu-id="15d2f-118">DNS Server</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="15d2f-119">Non modificare </strong> : le impostazioni DNS impostate nella macchina virtuale dell'area di lavoro MED-V non verranno modificate.</span><span class="sxs-lookup"><span data-stu-id="15d2f-119">Don't change</strong>—DNS settings that are set within the MED-V workspace virtual machine will not be changed.</span></span></p></li>
<li><p><strong><span data-ttu-id="15d2f-120">Usare l'indirizzo DNS dell'host </strong> : le impostazioni DNS dell'area di lavoro MED-V verranno sincronizzate in modo che corrispondano alle impostazioni dell'host.</span><span class="sxs-lookup"><span data-stu-id="15d2f-120">Use Host's DNS address</strong>—MED-V workspace DNS settings will be synchronized to match the host's settings.</span></span> <span data-ttu-id="15d2f-121">La sincronizzazione DNS è dinamica.</span><span class="sxs-lookup"><span data-stu-id="15d2f-121">The DNS synchronization is dynamic.</span></span> <span data-ttu-id="15d2f-122">Viene sincronizzata periodicamente con l'host in modo che, se è stata modificata nell'host, cambierà in modo dinamico nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="15d2f-122">It is synchronized periodically with the host so that if it is changed on the host, it will change dynamically in the MED-V workspace.</span></span></p></li>
<li><p><strong><span data-ttu-id="15d2f-123">Usare indirizzi DNS specifici </strong> : l'area di lavoro MED-V utilizzerà un DNS specifico, come specificato.</span><span class="sxs-lookup"><span data-stu-id="15d2f-123">Use specific DNS addresses</strong>—The MED-V workspace will use a specific DNS, as specified.</span></span></p>
<p><span data-ttu-id="15d2f-124">Nei <strong> campi primari </strong> e <strong> secondari </strong> immettere gli indirizzi DNS primari e secondari.</span><span class="sxs-lookup"><span data-stu-id="15d2f-124">In the <strong>Primary</strong> and <strong>Secondary</strong> fields, enter the primary and secondary DNS addresses.</span></span></p>
<p><span data-ttu-id="15d2f-125">Selezionare la <strong> casella di controllo Accoda indirizzi DNS dell'host </strong> per aggiungere l'host agli indirizzi DNS configurati.</span><span class="sxs-lookup"><span data-stu-id="15d2f-125">Select the <strong>Append Host's DNS addresses</strong> check box to append the host to the configured DNS addresses.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="15d2f-126">Assegnare suffissi DNS</span><span class="sxs-lookup"><span data-stu-id="15d2f-126">Assign DNS Suffixes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="15d2f-127">Assegnare i suffissi seguenti </strong> : selezionare questa casella di controllo per assegnare specifici suffissi DNS; nella casella Immettere un suffisso o più suffissi separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="15d2f-127">Assign the following suffixes</strong>—Select this check box to assign specific DNS suffixes; in the box, enter a suffix or multiple suffixes separated by commas.</span></span></p></li>
<li><p><strong><span data-ttu-id="15d2f-128">Accoda suffissi host </strong> : selezionare questa casella di controllo per accodare i suffissi dell'host all'indirizzo DNS.</span><span class="sxs-lookup"><span data-stu-id="15d2f-128">Append host suffixes</strong>—Select this check box to append the host suffixes to the DNS address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="15d2f-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15d2f-129">Related topics</span></span>


[<span data-ttu-id="15d2f-130">Creazione di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="15d2f-130">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="15d2f-131">Uso dell'interfaccia utente di MED-V Management Console</span><span class="sxs-lookup"><span data-stu-id="15d2f-131">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





