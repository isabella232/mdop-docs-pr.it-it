---
title: Uso di un ambiente di test
description: Uso di un ambiente di test
author: dansimp
ms.assetid: fc5fcc7c-1ac8-483a-a6bd-2279ae2ee3fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fc3ad91747c755efe0576cc62473848094b72ed1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818175"
---
# <span data-ttu-id="ef34c-103">Uso di un ambiente di test</span><span class="sxs-lookup"><span data-stu-id="ef34c-103">Using a Test Environment</span></span>


<span data-ttu-id="ef34c-104">Prima di richiedere l'implementazione di un oggetto Criteri di gruppo (GPO) nell'ambiente di produzione, è consigliabile testare l'oggetto GPO in un ambiente lab.</span><span class="sxs-lookup"><span data-stu-id="ef34c-104">Before you request that a Group Policy Object (GPO) be deployed to the production environment, you should test the GPO in a lab environment.</span></span> <span data-ttu-id="ef34c-105">Se si sviluppa l'oggetto Criteri di un dominio in una foresta di test, è possibile esportare il GPO in un file e importare il file in un dominio della foresta di produzione.</span><span class="sxs-lookup"><span data-stu-id="ef34c-105">If you develop the GPO in a domain in a test forest, you can export the GPO to a file and import the file to a domain in the production forest.</span></span> <span data-ttu-id="ef34c-106">Puoi quindi testare l'oggetto Criteri di gruppo tramite il collegamento a un'unità organizzativa che contiene computer e utenti di test.</span><span class="sxs-lookup"><span data-stu-id="ef34c-106">You can then test the GPO by linking it to an organizational unit (OU) that contains test computers and users.</span></span>

-   [<span data-ttu-id="ef34c-107">Esportare un oggetto Criteri di gruppo in un file</span><span class="sxs-lookup"><span data-stu-id="ef34c-107">Export a GPO to a File</span></span>](export-a-gpo-to-a-file.md)

-   [<span data-ttu-id="ef34c-108">Importare un oggetto Criteri di gruppo da un file</span><span class="sxs-lookup"><span data-stu-id="ef34c-108">Import a GPO from a File</span></span>](import-a-gpo-from-a-file-ed.md)

-   [<span data-ttu-id="ef34c-109">Testare un oggetto Criteri di gruppo in un'unità organizzativa separata</span><span class="sxs-lookup"><span data-stu-id="ef34c-109">Test a GPO in a Separate Organizational Unit</span></span>](test-a-gpo-in-a-separate-organizational-unit-agpm40.md)

<span data-ttu-id="ef34c-110">**Nota**  Puoi anche importare un GPO dall'ambiente di produzione del dominio.</span><span class="sxs-lookup"><span data-stu-id="ef34c-110">**Note** You can also import a GPO from the production environment of the domain.</span></span> <span data-ttu-id="ef34c-111">Per altre informazioni, vedere [importare un GPO dalla produzione](import-a-gpo-from-production-agpm40-ed.md).</span><span class="sxs-lookup"><span data-stu-id="ef34c-111">For more information, see [Import a GPO from Production](import-a-gpo-from-production-agpm40-ed.md).</span></span>

 

 

 





