---
title: Configurazione del centro impostazioni società per UE-V 2. x
description: Configurazione del centro impostazioni società per UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823295"
---
# <span data-ttu-id="f2cdc-103">Configurazione del centro impostazioni società per UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="f2cdc-103">Configuring the Company Settings Center for UE-V 2.x</span></span>


<span data-ttu-id="f2cdc-104">Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 includono una nuova applicazione, il centro impostazioni società, che consente agli utenti di gestire le impostazioni per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 include a new application, the Company Settings Center, which helps users manage settings to synchronize.</span></span> <span data-ttu-id="f2cdc-105">Il centro impostazioni società viene installato con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-105">The Company Settings Center is installed by using the UE-V Agent.</span></span> <span data-ttu-id="f2cdc-106">Gli utenti accedono al centro impostazioni società nel pannello di controllo, nel menu **Start** o nella schermata **Start** e tramite l'icona dell'area di notifica UE-V.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-106">Users access the Company Settings Center in Control Panel, in the **Start** menu or on the **Start** screen, and via the UE-V notification area icon.</span></span> <span data-ttu-id="f2cdc-107">Il centro impostazioni società Visualizza le impostazioni sincronizzate e consente agli utenti di visualizzare lo stato di sincronizzazione di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-107">Company Settings Center displays which settings are synchronized and helps users see the synchronization status of UE-V.</span></span> <span data-ttu-id="f2cdc-108">Gli utenti possono usare il centro impostazioni società per selezionare le applicazioni o le funzionalità di Windows che sincronizzano le impostazioni tra i computer.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-108">Users can use the Company Settings Center to select which applications or Windows features synchronize their settings between computers.</span></span> <span data-ttu-id="f2cdc-109">Possono anche fare clic sul pulsante **Sincronizza ora** per sincronizzare tutte le impostazioni immediatamente.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-109">They can also click the **Sync Now** button to synchronize all settings immediately.</span></span> <span data-ttu-id="f2cdc-110">L'amministratore può anche includere un collegamento per il supporto nel centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-110">The administrator can also include a link for support in the Company Settings Center.</span></span>

## <span data-ttu-id="f2cdc-111">Informazioni sul centro impostazioni società</span><span class="sxs-lookup"><span data-stu-id="f2cdc-111">About the Company Settings Center</span></span>


<span data-ttu-id="f2cdc-112">L'applicazione desktop del centro impostazioni società offre agli utenti informazioni sulla sincronizzazione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-112">The Company Settings Center desktop application provides users with information about UE-V settings synchronization.</span></span> <span data-ttu-id="f2cdc-113">Il centro impostazioni società è accessibile in diversi modi:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-113">The Company Settings Center is accessible in several different ways:</span></span>

-   <span data-ttu-id="f2cdc-114">Icona dell'area di notifica con l'impostazione di criteri di gruppo **icona vassoio** o configurazione di Windows PowerShell attivata, nell'area di notifica viene visualizzata l'icona UE-V.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-114">Notification area icon – With the **Tray Icon** Group Policy setting or Windows PowerShell configuration enabled, the UE-V icon appears in the notification area.</span></span> <span data-ttu-id="f2cdc-115">Fare clic sull'icona UE-V per aprire il centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-115">Click the UE-V icon to open the Company Settings Center.</span></span>

    <span data-ttu-id="f2cdc-116">**Nota**  L'icona dell'area di notifica può essere disabilitata usando le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-116">**Note** The notification area icon can be disabled by using the following settings:</span></span>

    -   <span data-ttu-id="f2cdc-117">Impostazione di criteri di gruppo:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-117">Group Policy setting:</span></span> `Policy Tray Icon`

    -   <span data-ttu-id="f2cdc-118">Cmdlet di Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-118">Windows PowerShell cmdlet:</span></span> `TrayIconEnabled`

    -   <span data-ttu-id="f2cdc-119">Elemento di configurazione nel pacchetto di configurazione UE-V per SystemCenter2012 ConfigurationManager:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-119">Configuration item in the UE-V Configuration Pack for SystemCenter2012 ConfigurationManager:</span></span> `Tray icon enabled`

     

-   <span data-ttu-id="f2cdc-120">Applicazione Pannello di controllo: nel pannello di controllo passare a **aspetto e personalizzazione**e quindi fare clic su **centro impostazioni società**.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-120">Control Panel application – In Control Panel, browse to **Appearance and Personalization**, and then click **Company Settings Center**.</span></span>

-   <span data-ttu-id="f2cdc-121">Notifica primo utilizzo-se non disabilitato, l'agente UE-V avvisa l'utente che le impostazioni sono ora sincronizzate quando l'agente UE-V viene eseguito per la prima volta in un computer.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-121">First use notification – Unless disabled, the UE-V Agent alerts the user that settings are now synchronized when the UE-V agent runs for the first time on a computer.</span></span> <span data-ttu-id="f2cdc-122">Fare clic sulla finestra di dialogo notifica per aprire il centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-122">Click the notification dialog box to open the Company Settings Center.</span></span>

-   <span data-ttu-id="f2cdc-123">La schermata **Start** o il menu **Start** include un collegamento al centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-123">The **Start** screen or **Start** menu includes a link to the Company Settings Center.</span></span> <span data-ttu-id="f2cdc-124">Una ricerca per il centro impostazioni società trova l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-124">A search for Company Settings Center finds the application.</span></span>

## <span data-ttu-id="f2cdc-125">Configurazione del collegamento supporto nel centro impostazioni società</span><span class="sxs-lookup"><span data-stu-id="f2cdc-125">Configuring the support link in the Company Settings Center</span></span>


<span data-ttu-id="f2cdc-126">Il centro impostazioni società può includere un collegamento ipertestuale che gli utenti possono fare clic per ottenere supporto con i problemi di sincronizzazione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-126">The Company Settings Center can include a hyperlink that users can click to get support with UE-V settings synchronization problems.</span></span> <span data-ttu-id="f2cdc-127">Questo collegamento può aprire qualsiasi protocollo URL valido, ad esempio http://per una pagina Web o mailto://per un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-127">This link can open any valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span> <span data-ttu-id="f2cdc-128">Il collegamento supporto può essere configurato tramite criteri di gruppo, Windows PowerShell o il pacchetto di configurazione di System Center 2012 Configuration Manager UE-V.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-128">The support link can be configured by using Group Policy, Windows PowerShell, or the System Center 2012 Configuration Manager UE-V Configuration Pack.</span></span>

**<span data-ttu-id="f2cdc-129">Come configurare il collegamento supporto per il centro impostazioni società</span><span class="sxs-lookup"><span data-stu-id="f2cdc-129">How to configure the Company Settings Center support link</span></span>**

1.  <span data-ttu-id="f2cdc-130">Aprire lo strumento di gestione preferito:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-130">Open your preferred management tool:</span></span>

    -   <span data-ttu-id="f2cdc-131">**Criteri di gruppo** : se non è già stato fatto, scaricare il modello ADMX per la versione UE-V 2 da [modelli amministrativi di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span><span class="sxs-lookup"><span data-stu-id="f2cdc-131">**Group Policy** - If you have not already done so, download the ADMX template for UE-V 2 from [MDOP Administrative Templates](https://go.microsoft.com/fwlink/p/?LinkId=393941).</span></span>

    -   <span data-ttu-id="f2cdc-132">**Windows PowerShell** : in un computer con l'agente UE-V installato aprire **Windows PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-132">**Windows PowerShell** – On a computer with the UE-V Agent installed, open **Windows PowerShell**.</span></span> <span data-ttu-id="f2cdc-133">Per altre informazioni sull'amministrazione di UE-V tramite Windows PowerShell, vedere [amministrazione di UE-v 2. x con Windows PowerShell e WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="f2cdc-133">For more information about administering UE-V by using Windows PowerShell, see [Administering UE-V 2.x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).</span></span>

    -   <span data-ttu-id="f2cdc-134">**System Center 2012 Configuration Pack per Microsoft User Experience Virtualization (UE-v)** -importare il pacchetto di configurazione UE-v e seguire la documentazione del pacchetto di configurazione per creare elementi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-134">**System Center 2012 Configuration Pack for Microsoft User Experience Virtualization (UE-V)** – Import the UE-V Configuration Pack and follow the Configuration Pack documentation to create configuration items.</span></span> <span data-ttu-id="f2cdc-135">Per altre informazioni sul pacchetto di configurazione UE-V, vedere [configurazione di UE-v 2. x con System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="f2cdc-135">For more information about the UE-V Configuration Pack, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

2.  <span data-ttu-id="f2cdc-136">Modificare le impostazioni per i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-136">Edit the settings for the following policies:</span></span>

    -   <span data-ttu-id="f2cdc-137">**Contattare il testo del collegamento it** -questa impostazione specifica il testo del collegamento ipertestuale URL contatto nel centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-137">**Contact IT Link Text** - This setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span> <span data-ttu-id="f2cdc-138">Se si abilita questa impostazione, il centro impostazioni società Visualizza il testo specificato nel collegamento all'URL del contatto.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-138">If you enable this setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span>

        -   <span data-ttu-id="f2cdc-139">Impostazioni di criteri di gruppo:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-139">Group Policy settings:</span></span> `Contact IT Link Text`

        -   <span data-ttu-id="f2cdc-140">Cmdlet di Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-140">Windows PowerShell cmdlet:</span></span> `ContactITDescription`

        -   <span data-ttu-id="f2cdc-141">Elemento di configurazione del pacchetto di configurazione:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-141">Configuration Pack configuration item:</span></span> `IT contact descriptive text`

    -   <span data-ttu-id="f2cdc-142">**URL del contatto it** -questa impostazione specifica l'URL per il collegamento contatto it nel centro impostazioni società in un protocollo URL valido, ad esempio http://per una pagina web o mailto://per un messaggio di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-142">**Contact IT URL** - This setting specifies the URL for the Contact IT link in the Company Settings Center in a valid URL protocol, such as http:// for a webpage or mailto:// for an email.</span></span>

        -   <span data-ttu-id="f2cdc-143">Impostazioni di criteri di gruppo:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-143">Group Policy settings:</span></span> `Contact IT URL`

        -   <span data-ttu-id="f2cdc-144">Cmdlet di Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-144">Windows PowerShell cmdlet:</span></span> `ContactITUrl`

        -   <span data-ttu-id="f2cdc-145">Elemento di configurazione del pacchetto di configurazione:</span><span class="sxs-lookup"><span data-stu-id="f2cdc-145">Configuration Pack configuration item:</span></span> `IT contact URL`

3.  <span data-ttu-id="f2cdc-146">Distribuire le impostazioni ai computer degli utenti usando lo strumento di gestione.</span><span class="sxs-lookup"><span data-stu-id="f2cdc-146">Deploy settings to users’ computers by using the management tool.</span></span>






 

 





