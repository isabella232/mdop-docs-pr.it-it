---
title: Informazioni sulla scheda Registro virtuale
description: Informazioni sulla scheda Registro virtuale
author: dansimp
ms.assetid: ca8d837f-8218-4f86-95fd-13a44dccd022
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 77decee4a8e07333b466db0a1bd0513efe859c9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819895"
---
# <span data-ttu-id="a78c0-103">Informazioni sulla scheda Registro virtuale</span><span class="sxs-lookup"><span data-stu-id="a78c0-103">About the Virtual Registry Tab</span></span>


<span data-ttu-id="a78c0-104">Durante la sequenziazione viene creato un registro di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a78c0-104">A virtual registry is created during sequencing.</span></span> <span data-ttu-id="a78c0-105">Nella scheda **Registro di sistema virtuale** vengono visualizzate tutte le chiavi del registro di sistema e i valori necessari per l'esecuzione di un pacchetto di applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="a78c0-105">The **Virtual Registry** tab displays all the registry keys and values that are required for a sequenced application package to run.</span></span> <span data-ttu-id="a78c0-106">Usare questa scheda per aggiungere, modificare ed eliminare le chiavi del registro di sistema e i valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a78c0-106">Use this tab to add, edit, and delete registry keys and registry values.</span></span>

<span data-ttu-id="a78c0-107">È anche possibile scegliere di ignorare le chiavi del sistema di hosting selezionando **Sostituisci chiave locale**oppure è possibile creare una visualizzazione unita della chiave dall'ambiente virtuale selezionando **Unisci con chiave locale**.</span><span class="sxs-lookup"><span data-stu-id="a78c0-107">You can also choose to ignore the hosting system’s keys by selecting **Override Local Key**, or you can create a merged view of the key from within the virtual environment by selecting **Merge with Local Key**.</span></span>

<span data-ttu-id="a78c0-108">Le modifiche apportate alla scheda **Impostazioni** del registro di sistema virtuale influiscono sulle applicazioni che fanno parte del pacchetto di applicazione sequenziata specifico, ma non influiscono sul funzionamento di altre applicazioni in streaming o installate localmente nel client Desktop Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="a78c0-108">The changes to the virtual registry **Settings** tab affect applications that are part of the specific sequenced application package, but they do not affect the operation of other applications that are streamed to or locally installed on the Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="a78c0-109">**Nota**  Prestare attenzione quando si modificano i valori e le chiavi del registro di sistema virtuali.</span><span class="sxs-lookup"><span data-stu-id="a78c0-109">**Note** Exercise caution when changing virtual registry keys and values.</span></span> <span data-ttu-id="a78c0-110">La modifica di queste chiavi e valori potrebbe rendere inutilizzabile il pacchetto di applicazioni sequenziate.</span><span class="sxs-lookup"><span data-stu-id="a78c0-110">Changing these keys and values might render your sequenced application package inoperable.</span></span>

 

<span data-ttu-id="a78c0-111">Nel riquadro sinistro della scheda **Registro di sistema virtuale** viene visualizzato l'elenco completo dei registri virtuali creati durante la sequenziazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a78c0-111">The left pane of the **Virtual Registry** tab displays the full list of virtual registries created during the sequencing of an application.</span></span>

## <span data-ttu-id="a78c0-112">Colonne</span><span class="sxs-lookup"><span data-stu-id="a78c0-112">Columns</span></span>


<a href="" id="name"></a>**<span data-ttu-id="a78c0-113">Nome</span><span class="sxs-lookup"><span data-stu-id="a78c0-113">Name</span></span>**  
<span data-ttu-id="a78c0-114">Nome per la voce nel registro di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a78c0-114">The name for the entry in the virtual registry.</span></span>

<a href="" id="type"></a>**<span data-ttu-id="a78c0-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="a78c0-115">Type</span></span>**  
<span data-ttu-id="a78c0-116">Modalità di archiviazione dei dati da parte della voce.</span><span class="sxs-lookup"><span data-stu-id="a78c0-116">How the entry stores its data.</span></span>

<a href="" id="data"></a>**<span data-ttu-id="a78c0-117">Dati</span><span class="sxs-lookup"><span data-stu-id="a78c0-117">Data</span></span>**  
<span data-ttu-id="a78c0-118">Valore archiviato dalla voce.</span><span class="sxs-lookup"><span data-stu-id="a78c0-118">The value stored by the entry.</span></span>

<a href="" id="attributes"></a>**<span data-ttu-id="a78c0-119">Attributi</span><span class="sxs-lookup"><span data-stu-id="a78c0-119">Attributes</span></span>**  
<span data-ttu-id="a78c0-120">Visualizza gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="a78c0-120">Displays the file attributes.</span></span>

## <span data-ttu-id="a78c0-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a78c0-121">Related topics</span></span>


[<span data-ttu-id="a78c0-122">Come modificare le informazioni sulla chiave del Registro di sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="a78c0-122">How to Modify Virtual Registry Key Information</span></span>](how-to-modify-virtual-registry-key-information.md)

[<span data-ttu-id="a78c0-123">Console di Sequencer</span><span class="sxs-lookup"><span data-stu-id="a78c0-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





