---
title: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1
description: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1
author: dansimp
ms.assetid: 91835bf8-e53c-4202-986e-8d37050d1267
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff9ce0405df766aef9b30e67d07ceb579c4fa89f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818535"
---
# <span data-ttu-id="d082e-103">Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="d082e-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP1</span></span>


<span data-ttu-id="d082e-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="d082e-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="d082e-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft Advanced Group Policy Management (Advanced Manager criteri di gruppo) 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d082e-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM) 4.0 SP1.</span></span> <span data-ttu-id="d082e-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente Advanced Policy Management Pack-4,0 SP1 e contengono informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d082e-106">These release notes contain information that is required to successfully install AGPM 4.0 SP1 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="d082e-107">Se c'è una differenza tra queste note sulla versione e altra documentazione per Advanced Group Policy Management, la modifica più recente deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="d082e-107">If there is a difference between these release notes and other AGPM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d082e-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="d082e-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="d082e-109">Problemi noti di Advanced Group Policy Management 4,0</span><span class="sxs-lookup"><span data-stu-id="d082e-109">AGPM 4.0 SP1 known issues</span></span>


<span data-ttu-id="d082e-110">Questa sezione contiene le note sulla versione per Advanced Group Policy Management 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d082e-110">This section contains release notes for AGPM 4.0 SP1.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="d082e-111">Lo strumento "Disinstalla" del pannello di controllo potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="d082e-111">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="d082e-112">Lo strumento nel pannello di controllo che consente di disinstallare o modificare un programma potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="d082e-112">The tool in Control Panel that lets you uninstall or change a program may not work when you try to change AGPM server settings.</span></span>

<span data-ttu-id="d082e-113">SOLUZIONE alternativa: prima di provare a modificare le impostazioni del server Advanced Group Policy Management tramite il pannello di controllo, creare una copia della cartella di archivio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="d082e-113">WORKAROUND: Before you try to change AGPM server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="d082e-114">È quindi possibile usare Setup.exe per reinstallare il server Advanced Group Policy Management e scegliere i parametri di configurazione desiderati.</span><span class="sxs-lookup"><span data-stu-id="d082e-114">You can then use Setup.exe to reinstall the AGPM server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="d082e-115">I report non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="d082e-115">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="d082e-116">Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d082e-116">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="d082e-117">SOLUZIONE alternativa: per visualizzare i collegamenti nei report, selezionare l'oggetto Criteri di gruppo in console Gestione criteri di raggruppamento e fare clic sulla scheda **Impostazioni** nel riquadro destro.</span><span class="sxs-lookup"><span data-stu-id="d082e-117">WORKAROUND: To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and click the **Settings** tab in the right pane.</span></span>

### <a href="" id="reports-do-not-display-all--choice-options-properties--settings"></a><span data-ttu-id="d082e-118">I report non visualizzano tutte le impostazioni "Proprietà opzioni scelte"</span><span class="sxs-lookup"><span data-stu-id="d082e-118">Reports do not display all “Choice Options Properties” settings</span></span>

<span data-ttu-id="d082e-119">Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano tutte le impostazioni selezionate nella finestra Proprietà opzioni scelta nell'Editor oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d082e-119">The AGPM settings and difference reports do not display all of the settings that were selected on the Choice Options Properties window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="d082e-120">SOLUZIONE alternativa: usare la GPMC per visualizzare le impostazioni delle proprietà delle opzioni di scelta selezionate nei report.</span><span class="sxs-lookup"><span data-stu-id="d082e-120">WORKAROUND: Use the GPMC to view the selected Choice Options Properties settings in the reports.</span></span>

### <span data-ttu-id="d082e-121">I report non visualizzano le schede Mostra e Nascondi in alcuni browser</span><span class="sxs-lookup"><span data-stu-id="d082e-121">Reports do not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="d082e-122">Quando si visualizzano i report in Google Chrome o Mozilla Firefox, le schede Mostra e Nascondi, visualizzate sul lato destro delle impostazioni di Advanced Group Policy Management e dei report differenze, non vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="d082e-122">The Show and Hide tabs, shown on the right side of the AGPM settings and difference reports, are not displayed when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="d082e-123">SOLUZIONE alternativa: visualizzare i report usando Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d082e-123">WORKAROUND: View the reports by using Internet Explorer.</span></span>

### <span data-ttu-id="d082e-124">Le impostazioni Advanced Group Policy Management e i report differenze possono mostrare contenuto diverso dai report di GPMC</span><span class="sxs-lookup"><span data-stu-id="d082e-124">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="d082e-125">Le impostazioni Advanced Group Policy Management e i report differenze potrebbero non mostrare lo stesso contenuto dei report nella console Gestione criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d082e-125">The AGPM settings and difference reports may not show the same content as reports in the Group Policy Management Console (GPMC).</span></span>

<span data-ttu-id="d082e-126">SOLUZIONE alternativa: usare la GPMC per visualizzare i report di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="d082e-126">WORKAROUND: Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="d082e-127">Il servizio Advanced Group Policy Management non si avvia se il controller di dominio non è online</span><span class="sxs-lookup"><span data-stu-id="d082e-127">AGPM Service does not start if the domain controller is not online</span></span>

<span data-ttu-id="d082e-128">Quando il servizio Advanced Group Policy Management viene installato in un controller di dominio in Windows 8, il servizio non si avvia se il controller di dominio non è online.</span><span class="sxs-lookup"><span data-stu-id="d082e-128">When the AGPM Service is installed on a domain controller on Windows 8, the Service does not start if the domain controller is not online.</span></span>

<span data-ttu-id="d082e-129">SOLUZIONE alternativa: avviare manualmente il servizio Advanced Group Policy Management dopo che il controller di dominio è online.</span><span class="sxs-lookup"><span data-stu-id="d082e-129">WORKAROUND: Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="d082e-130">L'aggiornamento del server Advanced Group Policy Management a Advanced Group Policy Management 4,0 SP1 viene bloccato quando si esegue l'aggiornamento dalla versione Advanced Group Policy 4,0 Management</span><span class="sxs-lookup"><span data-stu-id="d082e-130">Upgrade of AGPM Server to AGPM 4.0 SP1 is blocked when you upgrade from the AGPM 4.0 release plus the hotfix</span></span>

<span data-ttu-id="d082e-131">Se si tenta di aggiornare il server Advanced Group Policy Management a Advanced Group Policy Management 4,0.</span><span class="sxs-lookup"><span data-stu-id="d082e-131">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="d082e-132">SP1 dopo l'installazione di Advanced Group Policy Management 4,0 e l'installazione dell'hotfix Advanced Group Policy Management (vedere l'articolo della Knowledge base [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), l'aggiornamento non riesce e non può essere completato</span><span class="sxs-lookup"><span data-stu-id="d082e-132">SP1 after installing AGPM 4.0 and then installing the AGPM hotfix (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="d082e-133">SOLUZIONE alternativa: disinstallare il server Advanced 4,0 Group Policy Management e quindi installare Advanced Group Policy Management 4,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="d082e-133">WORKAROUND: Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP1.</span></span>

### <span data-ttu-id="d082e-134">I report non visualizzano i collegamenti delle unità organizzative</span><span class="sxs-lookup"><span data-stu-id="d082e-134">Reports do not display organizational unit links</span></span>

<span data-ttu-id="d082e-135">Se si collega un oggetto Criteri di gruppo non controllato a un'unità organizzativa e quindi si controlla tale oggetto Criteri di gruppo tramite Advanced Group Policy Management, i report delle impostazioni e delle differenze della gestione avanzata non visualizzeranno i collegamenti dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="d082e-135">If you link an uncontrolled GPO to an organizational unit and then control that GPO using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="d082e-136">SOLUZIONE alternativa: nella scheda **controllo** del nodo **Cambia impostazioni** fare clic con il pulsante destro del mouse sull'oggetto Criteri di dialogo e scegliere **Impostazioni** e quindi fare clic su **collegamenti GPO** per visualizzare i collegamenti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d082e-136">WORKAROUND: From the **Controlled** tab of the **Change Settings** node, right-click the GPO and click **Settings** and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="d082e-137">In alternativa, puoi usare la GPMC per visualizzare i collegamenti a un GPO dalla scheda **ambito** .</span><span class="sxs-lookup"><span data-stu-id="d082e-137">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

## <span data-ttu-id="d082e-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d082e-138">Related topics</span></span>


[<span data-ttu-id="d082e-139">Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="d082e-139">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="d082e-140">Novità di Gestione avanzata Criteri di gruppo 4.0 SP1</span><span class="sxs-lookup"><span data-stu-id="d082e-140">What's New in AGPM 4.0 SP1</span></span>](whats-new-in-agpm-40-sp1.md)

 

 





