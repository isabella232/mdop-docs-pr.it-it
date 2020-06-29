---
title: Come gestire la compatibilità hardware
description: Come gestire la compatibilità hardware
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804636"
---
# <span data-ttu-id="af8aa-103">Come gestire la compatibilità hardware</span><span class="sxs-lookup"><span data-stu-id="af8aa-103">How to Manage Hardware Compatibility</span></span>


<span data-ttu-id="af8aa-104">Microsoft BitLocker Administration and Monitoring (MBAM) può raccogliere informazioni sul produttore e sul modello di computer client dopo la distribuzione dei criteri di gruppo Verifica compatibilità hardware.</span><span class="sxs-lookup"><span data-stu-id="af8aa-104">Microsoft BitLocker Administration and Monitoring (MBAM) can collect information about the manufacturer and model of client computers after you deploy the Allow Hardware Compatibility Checking Group Policy.</span></span> <span data-ttu-id="af8aa-105">Se si configura questo criterio, l'agente di MBAM riporta il computer e le informazioni sul modello al server MBAM quando il client MBAM viene distribuito in un computer client.</span><span class="sxs-lookup"><span data-stu-id="af8aa-105">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

<span data-ttu-id="af8aa-106">La funzionalità compatibilità hardware è utile quando l'organizzazione ha hardware o computer meno recenti che non supportano i chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="af8aa-106">The Hardware Compatibility feature is helpful when your organization has older computer hardware or computers that do not support Trusted Platform Module (TPM) chips.</span></span> <span data-ttu-id="af8aa-107">In questi casi, è possibile usare la caratteristica compatibilità hardware per verificare che la crittografia BitLocker venga applicata solo ai modelli di computer che la supportano.</span><span class="sxs-lookup"><span data-stu-id="af8aa-107">In these cases, you can use the Hardware Compatibility feature to ensure that BitLocker encryption is applied only to computer models that support it.</span></span> <span data-ttu-id="af8aa-108">Se tutti i computer dell'organizzazione supportano BitLocker, non è necessario usare la funzionalità compatibilità hardware.</span><span class="sxs-lookup"><span data-stu-id="af8aa-108">If all computers in your organization will support BitLocker, you do not have to use the Hardware Compatibility feature.</span></span>

<span data-ttu-id="af8aa-109">**Nota**  Per impostazione predefinita, la caratteristica compatibilità hardware di MBAM non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="af8aa-109">**Note** By default, MBAM Hardware Compatibility feature is not enabled.</span></span> <span data-ttu-id="af8aa-110">Per abilitarlo, selezionare la caratteristica **compatibilità hardware** sotto la caratteristica di **amministrazione e monitoraggio del server** durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="af8aa-110">To enable it, select the **Hardware Compatibility** feature under the **Administration and Monitoring Server** feature during setup.</span></span> <span data-ttu-id="af8aa-111">Per altre informazioni su come impostare e configurare la compatibilità hardware, vedere [distribuzione dell'infrastruttura del server MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="af8aa-111">For more information about how to set up and configure Hardware Compatibility, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

<span data-ttu-id="af8aa-112">La funzionalità compatibilità hardware funziona nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="af8aa-112">The Hardware Compatibility feature works in the following way.</span></span>

****

1.  <span data-ttu-id="af8aa-113">L'agente client MBAM individua le informazioni di base sul computer, come produttore, modello, BIOS Maker, versione del BIOS, creatore TPM e versione TPM, quindi passa queste informazioni al server MBAM.</span><span class="sxs-lookup"><span data-stu-id="af8aa-113">The MBAM client agent discovers basic computer information such as manufacturer, model, BIOS maker, BIOS version, TPM maker, and TPM version, and then passes this information to the MBAM server.</span></span>

2.  <span data-ttu-id="af8aa-114">Il server MBAM genera un elenco di modelli di computer client che consente di distinguere tra quelli che possono o non possono supportare BitLocker</span><span class="sxs-lookup"><span data-stu-id="af8aa-114">The MBAM server generates a list of client computer makes and models to enable you to differentiate between those that can or cannot support BitLocker</span></span>

3.  <span data-ttu-id="af8aa-115">Gli agenti client MBAM distribuiti nell'organizzazione aggiornano automaticamente questo elenco con tutte le nuove funzionalità e i modelli di computer individuati con uno stato **sconosciuto**.</span><span class="sxs-lookup"><span data-stu-id="af8aa-115">The MBAM client agents that are deployed in the enterprise automatically update this list with all new computer makes and models that are discovered with a state of **Unknown**.</span></span> <span data-ttu-id="af8aa-116">Un amministratore può quindi usare il sito Web di amministrazione di MBAM per modificare le voci di elenco in modo da specificare un determinato tipo di computer e modello come **compatibile** o **incompatibile**.</span><span class="sxs-lookup"><span data-stu-id="af8aa-116">An administrator can then use the MBAM administration website to change list entries to specify a particular computer make and model as **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="af8aa-117">Prima che l'agente client MBAM inizi a crittografare un'unità, l'agente verifica prima di tutto la compatibilità con crittografia BitLocker dell'hardware in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="af8aa-117">Before the MBAM client agent begins encrypting a drive, the agent first verifies the BitLocker encryption compatibility of the hardware it is running on.</span></span>

    -   <span data-ttu-id="af8aa-118">Se l'hardware è contrassegnato come compatibile, viene avviato il processo di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af8aa-118">If the hardware is marked as compatible, the BitLocker encryption process starts.</span></span> <span data-ttu-id="af8aa-119">MBAM riverificherà anche lo stato di compatibilità hardware del computer una volta al giorno.</span><span class="sxs-lookup"><span data-stu-id="af8aa-119">MBAM will also recheck the hardware compatibility status of the computer one time per day.</span></span>

    -   <span data-ttu-id="af8aa-120">Se l'hardware è contrassegnato come non compatibile, l'agente registra un evento e passa uno stato "esonerato dall'hardware" come parte del report di conformità.</span><span class="sxs-lookup"><span data-stu-id="af8aa-120">If the hardware is marked as incompatible, the agent logs an event and passes a “hardware exempted” state as part of compliance reporting.</span></span> <span data-ttu-id="af8aa-121">L'agente controlla ogni sette giorni per verificare se lo stato è stato modificato in "compatibile".</span><span class="sxs-lookup"><span data-stu-id="af8aa-121">The agent checks every seven days to see whether the state has changed to “compatible.”</span></span>

    -   <span data-ttu-id="af8aa-122">Se l'hardware è contrassegnato come sconosciuto, il processo di crittografia di BitLocker non inizierà.</span><span class="sxs-lookup"><span data-stu-id="af8aa-122">If the hardware is marked as unknown, the BitLocker encryption process will not begin.</span></span> <span data-ttu-id="af8aa-123">L'agente client MBAM verificherà nuovamente lo stato di compatibilità hardware del computer una volta al giorno.</span><span class="sxs-lookup"><span data-stu-id="af8aa-123">The MBAM client agent will recheck the hardware compatibility status of the computer one time per day.</span></span>

<span data-ttu-id="af8aa-124">**Avviso**  Se l'agente client MBAM prova a crittografare un computer che non supporta la crittografia unità BitLocker, è possibile che il computer venga danneggiato.</span><span class="sxs-lookup"><span data-stu-id="af8aa-124">**Warning** If the MBAM client agent tries to encrypt a computer that does not support BitLocker drive encryption, there is a possibility that the computer will become corrupted.</span></span> <span data-ttu-id="af8aa-125">Verificare che la funzionalità compatibilità hardware sia configurata correttamente quando l'organizzazione ha un hardware meno recente che non supporta BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af8aa-125">Ensure that the hardware compatibility feature is correctly configured when your organization has older hardware that does not support BitLocker.</span></span>

 

**<span data-ttu-id="af8aa-126">Per gestire la compatibilità hardware</span><span class="sxs-lookup"><span data-stu-id="af8aa-126">To manage hardware compatibility</span></span>**

1.  <span data-ttu-id="af8aa-127">Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="af8aa-127">Open a web browser and navigate to the Microsoft BitLocker Administration and Monitoring website.</span></span> <span data-ttu-id="af8aa-128">Selezionare **hardware** nella barra dei menu a sinistra.</span><span class="sxs-lookup"><span data-stu-id="af8aa-128">Select **Hardware** in the left menu bar.</span></span>

2.  <span data-ttu-id="af8aa-129">Nel riquadro destro fare clic su **ricerca avanzata**e quindi filtrare per visualizzare un elenco di tutti i modelli di computer con uno **Capability** stato di funzionalità **sconosciuto**.</span><span class="sxs-lookup"><span data-stu-id="af8aa-129">On the right pane, click **Advanced Search**, and then filter to display a list of all computer models that have a **Capability** status of **Unknown**.</span></span> <span data-ttu-id="af8aa-130">Viene visualizzato un elenco di modelli di computer corrispondenti ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="af8aa-130">A list of computer models matching the search criteria is displayed.</span></span> <span data-ttu-id="af8aa-131">Gli amministratori possono aggiungere, modificare o rimuovere nuovi tipi di computer da questa pagina.</span><span class="sxs-lookup"><span data-stu-id="af8aa-131">Administrators can add, edit, or remove new computer types from this page.</span></span>

3.  <span data-ttu-id="af8aa-132">Esaminare ogni configurazione hardware sconosciuta per determinare se la configurazione deve essere impostata su **compatibile** o non **compatibile**.</span><span class="sxs-lookup"><span data-stu-id="af8aa-132">Review each unknown hardware configuration to determine whether the configuration should be set to **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="af8aa-133">Selezionare una o più righe e quindi fare clic su **imposta compatibile** o **imposta non compatibile** per impostare la compatibilità di BitLocker, in base alle esigenze, per i modelli di computer selezionati.</span><span class="sxs-lookup"><span data-stu-id="af8aa-133">Select one or more rows, and then click either **Set Compatible** or **Set Incompatible** to set the BitLocker compatibility, as appropriate, for the selected computer models.</span></span> <span data-ttu-id="af8aa-134">Se impostato su **compatible**, BitLocker cerca di applicare i criteri di crittografia unità nei computer che corrispondono al modello supportato.</span><span class="sxs-lookup"><span data-stu-id="af8aa-134">If set to **Compatible**, BitLocker tries to enforce drive encryption policy on computers that match the supported model.</span></span> <span data-ttu-id="af8aa-135">Se impostato su non **compatibile**, BitLocker non applica i criteri di crittografia unità in tali computer.</span><span class="sxs-lookup"><span data-stu-id="af8aa-135">If set to **Incompatible**, BitLocker will not enforce drive encryption policy on those computers.</span></span>

    <span data-ttu-id="af8aa-136">**Nota**  Dopo aver impostato un modello di computer come compatibile, possono essere necessarie più di ventiquattro ore perché il client MBAM inizi la crittografia BitLocker nei computer che corrispondono al modello hardware.</span><span class="sxs-lookup"><span data-stu-id="af8aa-136">**Note** After you set a computer model as compatible, it can take more than twenty-four hours for the MBAM Client to begin BitLocker encryption on the computers matching that hardware model.</span></span>

     

5.  <span data-ttu-id="af8aa-137">Gli amministratori dovrebbero monitorare regolarmente l'elenco compatibilità hardware per esaminare i nuovi modelli scoperti dall'agente MBAM e quindi aggiornare l'impostazione di compatibilità in modo che sia **compatibile** o non **compatibile** .</span><span class="sxs-lookup"><span data-stu-id="af8aa-137">Administrators should regularly monitor the hardware compatibility list to review new models that are discovered by the MBAM agent, and then update their compatibility setting to **Compatible** or **Incompatible** as appropriate.</span></span>

## <span data-ttu-id="af8aa-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af8aa-138">Related topics</span></span>


[<span data-ttu-id="af8aa-139">Amministrazione delle funzionalità di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="af8aa-139">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





