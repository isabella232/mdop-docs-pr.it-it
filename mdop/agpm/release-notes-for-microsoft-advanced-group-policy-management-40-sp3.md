---
title: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP3
description: Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP3
author: dansimp
ms.assetid: 955d7674-a8d9-4fc5-b18a-5a1639e38014
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 6e0da04d67b3d29135071e0bc82b8e01789e4e81
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818525"
---
# <span data-ttu-id="f7715-103">Note sulla versione per Gestione avanzata Criteri di gruppo Microsoft 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="f7715-103">Release Notes for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>


<span data-ttu-id="f7715-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="f7715-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="f7715-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft Advanced Group Policy Management (Advanced Pack3) 4.0 Service (SP3).</span><span class="sxs-lookup"><span data-stu-id="f7715-105">Read these release notes thoroughly before you install Microsoft Advanced Group Policy Management (AGPM)4.0 Service Pack3 (SP3).</span></span> <span data-ttu-id="f7715-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente Advanced Group Policy Management 4.0 SP3 e contengono informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="f7715-106">These release notes contain information that is required to successfully install AGPM4.0 SP3 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="f7715-107">Se c'è una differenza tra queste note sulla versione e altre documentazioni di Advanced Group Policy Management, considerare l'ultima modifica autorevole.</span><span class="sxs-lookup"><span data-stu-id="f7715-107">If there is a difference between these release notes and other AGPM documentation, consider the latest change authoritative.</span></span> <span data-ttu-id="f7715-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="f7715-108">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="f7715-109">Problemi noti di Advanced Group Policy Management 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="f7715-109">AGPM4.0 SP3 known issues</span></span>


<span data-ttu-id="f7715-110">In questa sezione vengono descritti i problemi noti per Advanced Group Policy Management SP3 4,0.</span><span class="sxs-lookup"><span data-stu-id="f7715-110">This section describes the known issues for AGPM 4.0 SP3.</span></span>

### <span data-ttu-id="f7715-111">L'installazione di Advanced Group Policy non riesce in Windows 10</span><span class="sxs-lookup"><span data-stu-id="f7715-111">AGPM installation fails in Windows 10</span></span>

<span data-ttu-id="f7715-112">Advanced Group Policy Management Abilita internamente la funzionalità Windows Communication Foundation (WCF)-non HTTP-Activation durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f7715-112">AGPM internally enables the Windows Communication Foundation (WCF)-NonHTTP-Activation feature during installation.</span></span> <span data-ttu-id="f7715-113">In Windows 10, WCF ora include un requisito per riavviare Windows dopo l'abilitazione della caratteristica WCF non HTTP-Activation.</span><span class="sxs-lookup"><span data-stu-id="f7715-113">In Windows 10, WCF now includes a requirement to restart Windows after enabling the WCF NonHTTP-Activation feature.</span></span> <span data-ttu-id="f7715-114">Tuttavia, il codice di installazione della Advanced Group Policy Management corrente non gestisce questo requisito di riavvio e smette di rispondere mentre attende che il servizio venga attivato.</span><span class="sxs-lookup"><span data-stu-id="f7715-114">However, the current AGPM installer code does not handle this restart requirement and stops responding while it waits for the service to be activated.</span></span>

<span data-ttu-id="f7715-115">**Soluzione alternativa:** Prima di eseguire il programma di installazione di Advanced Group Policy Management, abilitare la caratteristica di attivazione non HTTP di WCF e quindi riavviare Windows.</span><span class="sxs-lookup"><span data-stu-id="f7715-115">**Workaround:** Before you run the AGPM installer, enable the WCF Non-HTTP Activation feature and then restart Windows.</span></span>

### <a href="" id="control-panel-s--uninstall--tool-may-not-work-when-you-try-to-change-agpm-server-settings"></a><span data-ttu-id="f7715-116">Lo strumento "Disinstalla" del pannello di controllo potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f7715-116">Control Panel’s “Uninstall” tool may not work when you try to change AGPM Server settings</span></span>

<span data-ttu-id="f7715-117">Lo strumento nel pannello di controllo usato per disinstallare o modificare un programma potrebbe non funzionare quando si prova a modificare le impostazioni del server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f7715-117">The tool in Control Panel that you use to uninstall or change a program may not work when you try to change AGPM Server settings.</span></span>

<span data-ttu-id="f7715-118">**Soluzione alternativa:** Prima di provare a modificare le impostazioni del server Advanced Group Policy Management tramite il pannello di controllo, creare una copia della cartella di archivio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f7715-118">**Workaround:** Before you try to change AGPM Server settings by using Control Panel, make a copy of the AGPM Archive folder.</span></span> <span data-ttu-id="f7715-119">È quindi possibile usare Setup.exe per reinstallare il server Advanced Group Policy Management e scegliere i parametri di configurazione desiderati.</span><span class="sxs-lookup"><span data-stu-id="f7715-119">You can then use Setup.exe to reinstall the AGPM Server and choose the configuration parameters that you want.</span></span>

### <span data-ttu-id="f7715-120">I report non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f7715-120">Reports do not display the links that were added to a Group Policy Object</span></span>

<span data-ttu-id="f7715-121">Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano i collegamenti aggiunti a un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f7715-121">The AGPM settings and difference reports do not display the links that were added to a Group Policy Object (GPO).</span></span>

<span data-ttu-id="f7715-122">**Soluzione alternativa:** Per visualizzare i collegamenti nei report, selezionare l'oggetto Criteri di gruppo nella console Gestione criteri di Group (GPMC) e quindi fare clic sulla scheda **Impostazioni** nel riquadro destro.</span><span class="sxs-lookup"><span data-stu-id="f7715-122">**Workaround:** To view the links in the reports, select the GPO in the Group Policy Management Console (GPMC), and then click the **Settings** tab in the right pane.</span></span>

### <span data-ttu-id="f7715-123">I report non visualizzano tutte le impostazioni delle proprietà delle opzioni di scelta</span><span class="sxs-lookup"><span data-stu-id="f7715-123">Reports do not display all Choice Options Properties settings</span></span>

<span data-ttu-id="f7715-124">Le impostazioni Advanced Group Policy Management e i report differenze non visualizzano tutte le impostazioni selezionate nella finestra **Proprietà opzioni scelta** nell'Editor oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f7715-124">The AGPM settings and difference reports do not display all of the settings that were selected in the **Choice Options Properties** window in the Group Policy Object Editor.</span></span>

<span data-ttu-id="f7715-125">**Soluzione alternativa:** Usare la GPMC per visualizzare le impostazioni delle **proprietà delle opzioni di scelta** selezionate nei report.</span><span class="sxs-lookup"><span data-stu-id="f7715-125">**Workaround:** Use the GPMC to view the selected **Choice Options Properties** settings in the reports.</span></span>

### <span data-ttu-id="f7715-126">I report potrebbero non visualizzare le schede Mostra e Nascondi in alcuni browser</span><span class="sxs-lookup"><span data-stu-id="f7715-126">Reports may not display the Show and Hide tabs in certain browsers</span></span>

<span data-ttu-id="f7715-127">Quando si visualizzano i report in Google Chrome o Mozilla Firefox, le schede **Mostra** e **Nascondi** , sul lato destro delle impostazioni di Advanced Group Policy Management e dei report di differenza, potrebbero non essere visualizzate.</span><span class="sxs-lookup"><span data-stu-id="f7715-127">The **Show** and **Hide** tabs, on the right side of the AGPM settings and difference reports, may not appear when you view the reports in Google Chrome or Mozilla Firefox.</span></span>

<span data-ttu-id="f7715-128">**Soluzione alternativa:** Visualizzare i report usando il browser Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f7715-128">**Workaround:** View the reports by using the Internet Explorer browser.</span></span>

### <span data-ttu-id="f7715-129">Le impostazioni Advanced Group Policy Management e i report differenze possono mostrare contenuto diverso dai report di GPMC</span><span class="sxs-lookup"><span data-stu-id="f7715-129">AGPM settings and difference reports may show different content from GPMC reports</span></span>

<span data-ttu-id="f7715-130">Le impostazioni Advanced Group Policy Management e i report differenze potrebbero non mostrare lo stesso contenuto dei report in GPMC.</span><span class="sxs-lookup"><span data-stu-id="f7715-130">The AGPM settings and difference reports may not show the same content as reports in the GPMC.</span></span>

<span data-ttu-id="f7715-131">**Soluzione alternativa:** Usare la GPMC per visualizzare i report di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="f7715-131">**Workaround:** Use the GPMC to view the AGPM reports.</span></span>

### <span data-ttu-id="f7715-132">Il servizio Advanced Group Policy Management non si avvia se il controller di dominio è offline</span><span class="sxs-lookup"><span data-stu-id="f7715-132">AGPM Service does not start if the domain controller is offline</span></span>

<span data-ttu-id="f7715-133">Quando il servizio Advanced Group Policy Management viene installato in un controller di dominio nei sistemi operativi Windows® 8 o versioni successive, il servizio non si avvia se il controller di dominio è offline.</span><span class="sxs-lookup"><span data-stu-id="f7715-133">When the AGPM Service is installed on a domain controller on the Windows® 8 operating systems or later operating systems, the service does not start if the domain controller is offline.</span></span>

<span data-ttu-id="f7715-134">**Soluzione alternativa:** Avviare manualmente il servizio Advanced Group Policy Management dopo che il controller di dominio è online.</span><span class="sxs-lookup"><span data-stu-id="f7715-134">**Workaround:** Manually start the AGPM Service after the domain controller is online.</span></span>

### <span data-ttu-id="f7715-135">L'aggiornamento di Advanced Group Policy Management a Advanced Group Policy Management 4.0 SP2 viene bloccato quando si esegue l'aggiornamento da Advanced Group Policy Management 4.0 Release Plus Hotfix1</span><span class="sxs-lookup"><span data-stu-id="f7715-135">Upgrade of AGPM Server to AGPM4.0 SP2 is blocked when you upgrade from the AGPM4.0 release plus hotfix1</span></span>

<span data-ttu-id="f7715-136">Se si tenta di aggiornare il server Advanced Group Policy Management a Advanced Group Policy Management 4,0.</span><span class="sxs-lookup"><span data-stu-id="f7715-136">If you try to upgrade the AGPM server to AGPM 4.0.</span></span> <span data-ttu-id="f7715-137">SP2 dopo l'installazione di Advanced Group Policy Management Server 4,0 e quindi l'installazione dell'hotfix di Advanced Group Policy Management denominato Advanced Management Packers 4,0 segnala le differenze non corrette nel report HTML (vedere l'articolo della Knowledge base [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), l'aggiornamento non viene completato</span><span class="sxs-lookup"><span data-stu-id="f7715-137">SP2 after installing AGPM 4.0 Server and then installing the AGPM hotfix named AGPM 4.0 reports incorrect differences in the HTML report (see Knowledge Base article [2643502](https://go.microsoft.com/fwlink/?LinkId=254474)), the upgrade fails and cannot be completed.</span></span>

<span data-ttu-id="f7715-138">**Soluzione alternativa:** Disinstallare il server Advanced Group Policy Management e quindi installare Advanced Group Policy Management 4,0 4,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="f7715-138">**Workaround:** Uninstall the AGPM 4.0 Server and then install AGPM 4.0 SP2.</span></span>

### <span data-ttu-id="f7715-139">I report non visualizzano i collegamenti delle unità organizzative</span><span class="sxs-lookup"><span data-stu-id="f7715-139">Reports do not display organizational unit links</span></span>

<span data-ttu-id="f7715-140">Se si collega un oggetto Criteri di gruppo non controllato a un'unità organizzativa e quindi si controlla tale oggetto Criteri di gruppo tramite Advanced Group Policy Management, i report delle impostazioni e delle differenze della gestione avanzata non visualizzeranno i collegamenti dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="f7715-140">If you link an uncontrolled GPO to an organizational unit and then control that GPO by using AGPM, the AGPM settings and difference reports do not display the organizational unit links.</span></span>

<span data-ttu-id="f7715-141">**Soluzione alternativa:** Nella scheda **controllo** del nodo **Cambia impostazioni** fare clic con il pulsante destro del mouse sull'oggetto Criteri di dialogo, scegliere **Impostazioni**e quindi fare clic su **collegamenti GPO** per visualizzare i collegamenti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f7715-141">**Workaround:** On the **Controlled** tab of the **Change Settings** node, right-click the GPO, click **Settings**, and then click **GPO Links** to view the organizational links.</span></span> <span data-ttu-id="f7715-142">In alternativa, puoi usare la GPMC per visualizzare i collegamenti a un GPO dalla scheda **ambito** .</span><span class="sxs-lookup"><span data-stu-id="f7715-142">Alternatively, you can use the GPMC to view the links to a GPO from the **Scope** tab.</span></span>

### <span data-ttu-id="f7715-143">Advanced Group Policy Management Visualizza un errore se si fa clic sul pulsante Back della finestra di dialogo modifica, ripristina o Rimuovi client Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="f7715-143">AGPM displays an error if you click the Back button from the Change, Repair, or Remove AGPM Client dialog box</span></span>

<span data-ttu-id="f7715-144">Se si passa a **programmi e funzionalità** nel pannello di controllo e quindi si seleziona **Gestione criteri di gruppo avanzati Microsoft-client**, Advanced Group Policy Management Visualizza un errore se si fa clic su **modifica** e quindi sul pulsante **Torna** nella finestra di dialogo **modifica, ripristina o Rimuovi client Advanced Group Policy** Management.</span><span class="sxs-lookup"><span data-stu-id="f7715-144">If you browse to **Programs and Features** in Control Panel and then select **Microsoft Advanced Group Policy Management – Client**, AGPM displays an error if you click **Modify** and then click the **Back** button in the **Change, Repair, or Remove AGPM Client** dialog box.</span></span>

<span data-ttu-id="f7715-145">**Soluzione alternativa:** Fare clic su **Annulla** per cancellare l'errore e quindi riavviare di nuovo il processo.</span><span class="sxs-lookup"><span data-stu-id="f7715-145">**Workaround:** Click **Cancel** to clear the error, and then start the process again.</span></span> <span data-ttu-id="f7715-146">Non fare clic sul pulsante **Avanti** dopo aver fatto clic su **modifica** .</span><span class="sxs-lookup"><span data-stu-id="f7715-146">Do not click the **Back** button after you click **Modify** .</span></span>

### <span data-ttu-id="f7715-147">Il commento non viene visualizzato nella finestra cronologia quando l'approvatore distribuisce un GPO e immette un commento</span><span class="sxs-lookup"><span data-stu-id="f7715-147">Comment fails to appear in the History window when the Approver deploys a GPO and enters a comment</span></span>

<span data-ttu-id="f7715-148">Se un utente che ha il ruolo di editor invia una richiesta di distribuzione di un oggetto Criteri di stato e l'utente che ha il ruolo di responsabile approvazione distribuisce il GPO e immette un commento, il commento non viene visualizzato nella finestra **cronologia** .</span><span class="sxs-lookup"><span data-stu-id="f7715-148">If a user who has the Editor role submits a request to deploy a GPO, and the user who has the Approver role then deploys the GPO and enters a comment, the comment fails to appear in the **History** window.</span></span>

<span data-ttu-id="f7715-149">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="f7715-149">**Workaround:** None.</span></span>

### <span data-ttu-id="f7715-150">Meccanismo aggiunto per l'override del comportamento predefinito di Advanced Group Policy per la rimozione delle modifiche alle autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="f7715-150">Added mechanism to override AGPM default behavior of removing GPO permission changes</span></span>

<span data-ttu-id="f7715-151">A partire da HF02, Advanced Group Policy Management ha aggiunto una chiave del registro di sistema per consentire l'override del comportamento predefinito dell'autorizzazione GPO.</span><span class="sxs-lookup"><span data-stu-id="f7715-151">As of HF02, AGPM has added a registry key to enable overriding the default AGPM GPO permission behavior.</span></span> <span data-ttu-id="f7715-152">Per altre informazioni, vedere [le modifiche apportate alle autorizzazioni degli oggetti Criteri di gruppo tramite Advanced Group Policy Management](https://support.microsoft.com/kb/3174540)</span><span class="sxs-lookup"><span data-stu-id="f7715-152">For more information, please see [Changes to Group Policy object permissions through AGPM are ignored](https://support.microsoft.com/kb/3174540)</span></span>

## <span data-ttu-id="f7715-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7715-153">Related topics</span></span>


[<span data-ttu-id="f7715-154">Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f7715-154">Advanced Group Policy Management</span></span>](index.md)

[<span data-ttu-id="f7715-155">Novità di Gestione avanzata Criteri di gruppo 4.0 SP3</span><span class="sxs-lookup"><span data-stu-id="f7715-155">What's New in AGPM 4.0 SP3</span></span>](whats-new-in-agpm-40-sp3.md)

 

 





