---
title: Come pubblicare i collegamenti dell'applicazione
description: Come pubblicare i collegamenti dell'applicazione
author: dansimp
ms.assetid: fc5efe86-1bbe-438b-b7d8-4f9b815cc58e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eafdb85414a1a6cf3e1072fdc5532bcd04699653
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816845"
---
# <span data-ttu-id="71a03-103">Come pubblicare i collegamenti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="71a03-103">How to Publish Application Shortcuts</span></span>


<span data-ttu-id="71a03-104">Puoi usare la procedura seguente per pubblicare i collegamenti a un'applicazione direttamente dal riquadro dei **risultati** del nodo dell' **applicazione** nella console di gestione client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="71a03-104">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="71a03-105">Per pubblicare i collegamenti alle applicazioni</span><span class="sxs-lookup"><span data-stu-id="71a03-105">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="71a03-106">Posizionare il cursore nel riquadro **dei risultati** , fare clic con il pulsante destro del mouse sull'applicazione desiderata e scegliere **nuovo collegamento** dal menu a comparsa per visualizzare la creazione guidata nuovo collegamento.</span><span class="sxs-lookup"><span data-stu-id="71a03-106">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="71a03-107">Nella prima pagina della creazione guidata nuovo collegamento selezionare un'icona e specificare un nome per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="71a03-107">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="71a03-108">**Icona cambia**: Visualizza un browser di icone standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="71a03-108">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="71a03-109">Individuare e selezionare l'icona desiderata.</span><span class="sxs-lookup"><span data-stu-id="71a03-109">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="71a03-110">**Titolo del collegamento**: immettere il nome che si vuole assegnare al collegamento.</span><span class="sxs-lookup"><span data-stu-id="71a03-110">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="71a03-111">Questo campo viene impostato come predefinito per il nome e la versione esistenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="71a03-111">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="71a03-112">Nella seconda pagina della procedura guidata determinare la posizione del collegamento pubblicato.</span><span class="sxs-lookup"><span data-stu-id="71a03-112">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="71a03-113">**Desktop**: selezionare questa casella di controllo per pubblicare il collegamento sul desktop.</span><span class="sxs-lookup"><span data-stu-id="71a03-113">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="71a03-114">**Barra di avvio veloce**: selezionare questa casella di controllo per pubblicare il collegamento sulla barra di avvio veloce.</span><span class="sxs-lookup"><span data-stu-id="71a03-114">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="71a03-115">**Menu Invia a**: selezionare questa casella di controllo per pubblicare il collegamento al menu **Invia a** .</span><span class="sxs-lookup"><span data-stu-id="71a03-115">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="71a03-116">**Programmi nel menu Start**: quando si seleziona la casella di controllo **menu Start** , questo campo diventa attivo.</span><span class="sxs-lookup"><span data-stu-id="71a03-116">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="71a03-117">Lascia vuoto questo campo per pubblicare il collegamento direttamente nella radice della cartella programmi oppure immetti un nome di cartella o una gerarchia, ad esempio "My \ _Computer applicazioni \\Office".</span><span class="sxs-lookup"><span data-stu-id="71a03-117">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="71a03-118">I collegamenti creati in questo modo sono disponibili solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="71a03-118">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="71a03-119">**Altro percorso** e pulsante **Sfoglia** : quando si seleziona la casella di controllo **altro percorso** , questo campo diventa attivo.</span><span class="sxs-lookup"><span data-stu-id="71a03-119">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="71a03-120">Immettere una posizione valida nel computer o in qualsiasi percorso UNC disponibile (file condiviso o directory in una rete).</span><span class="sxs-lookup"><span data-stu-id="71a03-120">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="71a03-121">Il pulsante **Sfoglia** Visualizza una finestra di dialogo **Apri file** standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="71a03-121">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="71a03-122">Nella terza pagina della procedura guidata Immetti i parametri della riga di comando desiderati.</span><span class="sxs-lookup"><span data-stu-id="71a03-122">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="71a03-123">Fare clic su **fine** per pubblicare i tasti di scelta rapida e quindi uscire dal riquadro **risultati** .</span><span class="sxs-lookup"><span data-stu-id="71a03-123">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="71a03-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71a03-124">Related topics</span></span>


[<span data-ttu-id="71a03-125">Come aggiungere un'associazione del tipo di file</span><span class="sxs-lookup"><span data-stu-id="71a03-125">How to Add a File Type Association</span></span>](how-to-add-a-file-type-association.md)

[<span data-ttu-id="71a03-126">Come aggiungere un'applicazione</span><span class="sxs-lookup"><span data-stu-id="71a03-126">How to Add an Application</span></span>](how-to-add-an-application.md)

[<span data-ttu-id="71a03-127">Come eliminare un'associazione del tipo di file</span><span class="sxs-lookup"><span data-stu-id="71a03-127">How to Delete a File Type Association</span></span>](how-to-delete-a-file-type-association.md)

 

 





