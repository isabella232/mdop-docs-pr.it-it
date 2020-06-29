---
title: Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti
description: Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817915"
---
# <span data-ttu-id="c837d-103">Come configurare il comportamento per l'associazione del tipo di file e dei collegamenti</span><span class="sxs-lookup"><span data-stu-id="c837d-103">How to Configure Shortcut and File Type Association Behavior</span></span>


<span data-ttu-id="c837d-104">I criteri di pubblicazione di collegamento e di associazione dei tipi di file (FTA) sono definiti e controllati dal file XML di pubblicazione, che viene inviato ai client da un server di pubblicazione durante un'operazione di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c837d-104">Shortcut and File Type Association (FTA) publishing policy is defined and controlled by the publishing XML file, which is sent to clients by a publishing server during a publishing refresh operation.</span></span> <span data-ttu-id="c837d-105">Quando il client riceve queste informazioni, aggiunge tutti i dati appena pubblicati relativi alle applicazioni, ad esempio le icone e accordi.</span><span class="sxs-lookup"><span data-stu-id="c837d-105">When the client receives this information, it adds any newly published data about applications such as the icons and FTAs.</span></span> <span data-ttu-id="c837d-106">Vengono quindi rimossi tutti i dati di pubblicazione obsoleti.</span><span class="sxs-lookup"><span data-stu-id="c837d-106">Then, it removes any outdated publishing data.</span></span>

<span data-ttu-id="c837d-107">In App-V versione 4,6 sono stati definiti due valori della chiave del registro di sistema per consentire agli amministratori di controllare questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="c837d-107">In App-V version 4.6, two registry key values have been defined to enable administrators to control this behavior.</span></span> <span data-ttu-id="c837d-108">Per impostazione predefinita, i tasti di scelta rapida creati localmente tramite la console client vengono ora mantenuti.</span><span class="sxs-lookup"><span data-stu-id="c837d-108">By default, shortcuts that are created locally by using the client console are now retained.</span></span>

## <span data-ttu-id="c837d-109">Come modificare il collegamento e il comportamento FTA</span><span class="sxs-lookup"><span data-stu-id="c837d-109">How to Change Shortcut and FTA Behavior</span></span>


<span data-ttu-id="c837d-110">Sono stati definiti due nuovi valori del registro di sistema DWORD per la chiave del registro di sistema client Configuration, "FileTypePolicy" e "ShortcutPolicy".</span><span class="sxs-lookup"><span data-stu-id="c837d-110">Two new DWORD registry values have been defined for the client Configuration registry key, “FileTypePolicy” and “ShortcutPolicy”.</span></span> <span data-ttu-id="c837d-111">Questi valori del registro di sistema DWORD non sono presenti per impostazione predefinita, ma possono essere aggiunti manualmente.</span><span class="sxs-lookup"><span data-stu-id="c837d-111">These DWORD registry values are not present by default, but they can be added manually.</span></span> <span data-ttu-id="c837d-112">La chiave del registro di configurazione si trova in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="c837d-112">The Configuration registry key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span></span>

<span data-ttu-id="c837d-113">Nella tabella seguente sono definiti quattro valori di criteri che si applicano a entrambi i valori della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c837d-113">There are four policy values defined in the following table and these apply to both registry key values.</span></span> <span data-ttu-id="c837d-114">L'elenco seguente mostra i valori numerici per le impostazioni del registro di sistema e il comportamento applicato ai tipi di file o ai tasti di scelta rapida in un'operazione di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c837d-114">The following list shows the numeric values for the registry settings, and the behavior applied to file types or shortcuts on a publishing refresh operation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c837d-115">Nome</span><span class="sxs-lookup"><span data-stu-id="c837d-115">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="c837d-116">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-117">Dati (esempi)</span><span class="sxs-lookup"><span data-stu-id="c837d-117">Data (Examples)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c837d-118">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c837d-119">FileTypePolicy</span><span class="sxs-lookup"><span data-stu-id="c837d-119">FileTypePolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-120">DWORD</span><span class="sxs-lookup"><span data-stu-id="c837d-120">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-121">Impostazione predefinita = 0x2 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="c837d-121">Default=0x2 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-122">(0x0)-"ClientOnly"-rimuovere eventuali elementi esistenti dalla stessa origine informazioni di pubblicazione e conservare solo gli elementi aggiunti localmente</span><span class="sxs-lookup"><span data-stu-id="c837d-122">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items that are added locally</span></span></p>
<p><span data-ttu-id="c837d-123">(0x1)-"ServerOnly"-rimuove gli elementi obsoleti della stessa origine informazioni di pubblicazione e gli elementi aggiunti localmente e aggiunge i nuovi elementi</span><span class="sxs-lookup"><span data-stu-id="c837d-123">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items that are added locally, and add the new items</span></span></p>
<p><span data-ttu-id="c837d-124">(0x2)-"ClientAndServer"-rimuovere gli elementi obsoleti dalla stessa origine informazioni di pubblicazione, conservare gli elementi aggiunti localmente e aggiungere i nuovi elementi (impostazione predefinita, se non presente per l'App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="c837d-124">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present for App-V 4.6)</span></span></p>
<p><span data-ttu-id="c837d-125">(0x3)-"NoChange"-non apportare modifiche ai tipi di file o alle scelte rapide da tastiera</span><span class="sxs-lookup"><span data-stu-id="c837d-125">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c837d-126">ShortcutPolicy</span><span class="sxs-lookup"><span data-stu-id="c837d-126">ShortcutPolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-127">DWORD</span><span class="sxs-lookup"><span data-stu-id="c837d-127">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-128">Impostazione predefinita = 0x2</span><span class="sxs-lookup"><span data-stu-id="c837d-128">Default=0x2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c837d-129">(0x0)-"ClientOnly"-rimuovere eventuali elementi esistenti dalla stessa origine informazioni di pubblicazione e conservare solo gli elementi aggiunti localmente</span><span class="sxs-lookup"><span data-stu-id="c837d-129">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items added locally</span></span></p>
<p><span data-ttu-id="c837d-130">(0x1)-"ServerOnly"-Rimuovi gli elementi obsoleti dalla stessa origine informazioni di pubblicazione e gli elementi aggiunti localmente e Aggiungi i nuovi elementi</span><span class="sxs-lookup"><span data-stu-id="c837d-130">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items added locally, and add the new items</span></span></p>
<p><span data-ttu-id="c837d-131">(0x2)-"ClientAndServer"-rimuovere gli elementi obsoleti dalla stessa origine informazioni di pubblicazione, conservare gli elementi aggiunti localmente e aggiungere i nuovi elementi (impostazione predefinita, se non presente)</span><span class="sxs-lookup"><span data-stu-id="c837d-131">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present)</span></span></p>
<p><span data-ttu-id="c837d-132">(0x3)-"NoChange"-non apportare modifiche ai tipi di file o alle scelte rapide da tastiera</span><span class="sxs-lookup"><span data-stu-id="c837d-132">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c837d-133">**Nota**  I valori di testo fanno riferimento ai valori degli attributi XML nel file XML di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c837d-133">**Note** The text values refer to the values for the XML attributes in the publishing XML file.</span></span><span data-ttu-id="c837d-134">È possibile impostare questi valori manualmente se è stata implementata una soluzione di pubblicazione HTTP personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c837d-134"> You can set these values manually if you have implemented a custom HTTP publishing solution.</span></span>

 

 

 





