---
title: Come configurare o disabilitare la creazione di report di utilizzo
description: Come configurare o disabilitare la creazione di report di utilizzo
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816546"
---
# <span data-ttu-id="0ad58-103">Come configurare o disabilitare la creazione di report di utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ad58-103">How to Set Up or Disable Usage Reporting</span></span>


<span data-ttu-id="0ad58-104">È possibile usare le procedure seguenti nella console di gestione di Application Virtualization Server per specificare la durata (in mesi) delle informazioni sull'uso del sistema di virtualizzazione delle applicazioni che si desidera archiviare nel database.</span><span class="sxs-lookup"><span data-stu-id="0ad58-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the duration (in months) of Application Virtualization System usage information you want to store in the database.</span></span>

<span data-ttu-id="0ad58-105">**Nota**  Per archiviare le informazioni sull'utilizzo, è necessario selezionare la casella di controllo **registra informazioni sull'utilizzo** nella scheda **Pipeline provider** . Per visualizzare questa scheda, fare clic con il pulsante destro del mouse sui criteri del provider nel riquadro **dei risultati dei criteri del provider** e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="0ad58-105">**Note** To store usage information, you must select the **Log Usage Information** check box on the **Provider Pipeline** tab. To display this tab, right-click the provider policy in the **Provider Policies Results** pane and select **Properties**.</span></span>

 

**<span data-ttu-id="0ad58-106">Per configurare la creazione di report sull'utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ad58-106">To set up usage reporting</span></span>**

1.  <span data-ttu-id="0ad58-107">Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro sinistro e scegliere **Opzioni di sistema**.</span><span class="sxs-lookup"><span data-stu-id="0ad58-107">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="0ad58-108">Selezionare la scheda **database** .</span><span class="sxs-lookup"><span data-stu-id="0ad58-108">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="0ad58-109">Selezionare il pulsante **di opzione Mantieni l'utilizzo per (mesi)** o **Mantieni tutto l'uso** .</span><span class="sxs-lookup"><span data-stu-id="0ad58-109">Select the **Keep Usage For (Months)** or **Keep All Usage** radio button.</span></span>

4.  <span data-ttu-id="0ad58-110">Se si sceglie di specificare la durata dell'utilizzo in mesi, immettere un numero da 1 a 120 (il valore predefinito è di 6 mesi).</span><span class="sxs-lookup"><span data-stu-id="0ad58-110">If you choose to specify usage duration in months, enter a number from 1 to 120 (default value is 6 months).</span></span> <span data-ttu-id="0ad58-111">Se si seleziona **Mantieni tutto l'utilizzo**, il database si svilupperà fino a raggiungere il limite di dimensioni specificato.</span><span class="sxs-lookup"><span data-stu-id="0ad58-111">If you select **Keep All Usage**, the database will grow until it reaches the specified size limit.</span></span>

5.  <span data-ttu-id="0ad58-112">Fare clic su **applica** o **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ad58-112">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="0ad58-113">Per disabilitare la creazione di report sull'utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ad58-113">To disable usage reporting</span></span>**

1.  <span data-ttu-id="0ad58-114">Fare clic sul nodo **criteri provider** .</span><span class="sxs-lookup"><span data-stu-id="0ad58-114">Click the **Provider Policies** node.</span></span>

2.  <span data-ttu-id="0ad58-115">Fare clic con il pulsante destro del mouse su **criteri provider** e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="0ad58-115">Right-click **Provider Policy** and select **Properties**.</span></span>

3.  <span data-ttu-id="0ad58-116">Selezionare la scheda **Pipeline provider** .</span><span class="sxs-lookup"><span data-stu-id="0ad58-116">Select the **Provider Pipeline** tab.</span></span>

4.  <span data-ttu-id="0ad58-117">Deselezionare la casella di controllo **registra informazioni sull'utilizzo** .</span><span class="sxs-lookup"><span data-stu-id="0ad58-117">Clear the **Log Usage Information** check box.</span></span>

5.  <span data-ttu-id="0ad58-118">Fare clic su **applica** o **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ad58-118">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="0ad58-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ad58-119">Related topics</span></span>


[<span data-ttu-id="0ad58-120">Come personalizzare un sistema di Application Virtualization in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="0ad58-120">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="0ad58-121">Come configurare o disabilitare le dimensioni dei database</span><span class="sxs-lookup"><span data-stu-id="0ad58-121">How to Set Up or Disable Database Size</span></span>](how-to-set-up-or-disable-database-size.md)

 

 





