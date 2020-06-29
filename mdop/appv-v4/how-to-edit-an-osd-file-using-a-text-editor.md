---
title: Come modificare un file OSD usando un editor di testo
description: Come modificare un file OSD usando un editor di testo
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817445"
---
# <span data-ttu-id="974d3-103">Come modificare un file OSD usando un editor di testo</span><span class="sxs-lookup"><span data-stu-id="974d3-103">How to Edit an OSD File Using a Text Editor</span></span>


<span data-ttu-id="974d3-104">Usare la procedura seguente per modificare un file OSD (Open Software Descriptor) usando un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="974d3-104">Use the following procedure to edit an Open Software Descriptor (OSD) file by using a text editor.</span></span>

**<span data-ttu-id="974d3-105">Per modificare un file OSD usando un editor di testo</span><span class="sxs-lookup"><span data-stu-id="974d3-105">To edit an OSD file by using a text editor</span></span>**

1.  <span data-ttu-id="974d3-106">Aprire il file OSD usando qualsiasi editor di testo XML o ASCII, ad esempio Blocco note Microsoft.</span><span class="sxs-lookup"><span data-stu-id="974d3-106">Open the OSD file using any XML or ASCII text editor—for example, Microsoft Notepad.</span></span>

    <span data-ttu-id="974d3-107">**Nota**  Prima di modificare il file OSD, leggere lo schema prescritto dal file XSD nella directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="974d3-107">**Note** Before modifying the OSD file, read the schema prescribed by the XSD file in the install directory.</span></span> <span data-ttu-id="974d3-108">Se non si riesce a seguire questo schema, è possibile che vengano introdotti errori che impediscono l'avvio di un'applicazione sequenziale.</span><span class="sxs-lookup"><span data-stu-id="974d3-108">Failing to follow this schema might introduce errors that prevent a sequenced application from starting successfully.</span></span>

     

2.  <span data-ttu-id="974d3-109">Modificare il file OSD usando l'editor di testo XML o ASCII di scelta, aderendo allo schema prescritto e alle linee guida seguenti:</span><span class="sxs-lookup"><span data-stu-id="974d3-109">Edit the OSD file using your XML or ASCII text editor of choice, adhering to the prescribed schema and the following guidelines:</span></span>

    1.  <span data-ttu-id="974d3-110">Assicurati che gli elementi denominati siano annidati all'interno dell' &lt; &gt; elemento radice SOFTPKG.</span><span class="sxs-lookup"><span data-stu-id="974d3-110">Ensure that named elements are nested within the &lt;SOFTPKG&gt; root element.</span></span>

    2.  <span data-ttu-id="974d3-111">Verificare che i nomi degli elementi siano in lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="974d3-111">Ensure that element names are in all uppercase letters.</span></span>

    3.  <span data-ttu-id="974d3-112">Tieni presente che i valori degli attributi sono maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="974d3-112">Be aware that attribute values are case sensitive.</span></span>

    4.  <span data-ttu-id="974d3-113">Digitare con attenzione e osservare le specifiche XML.</span><span class="sxs-lookup"><span data-stu-id="974d3-113">Type carefully, and observe the XML specifications.</span></span>

## <span data-ttu-id="974d3-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="974d3-114">Related topics</span></span>


[<span data-ttu-id="974d3-115">Informazioni sulla scheda OSD</span><span class="sxs-lookup"><span data-stu-id="974d3-115">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="974d3-116">Come modificare un File OSD</span><span class="sxs-lookup"><span data-stu-id="974d3-116">How to Edit an OSD File</span></span>](how-to-edit-an-osd-file.md)

[<span data-ttu-id="974d3-117">Elementi di file OSD</span><span class="sxs-lookup"><span data-stu-id="974d3-117">OSD File Elements</span></span>](osd-file-elements.md)

 

 





