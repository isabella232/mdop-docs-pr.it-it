---
title: Come usare Dynamic Suite Composition
description: Come usare Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816416"
---
# <span data-ttu-id="d5ca5-103">Come usare Dynamic Suite Composition</span><span class="sxs-lookup"><span data-stu-id="d5ca5-103">How To Use Dynamic Suite Composition</span></span>


<span data-ttu-id="d5ca5-104">La composizione delle suite dinamiche nella virtualizzazione delle applicazioni consente di definire un'applicazione dipendente da un'altra applicazione, ad esempio middleware o plug-in.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-104">Dynamic Suite Composition in Application Virtualization enables you to define an application as being dependent on another application, such as middleware or a plug-in.</span></span> <span data-ttu-id="d5ca5-105">In questo modo l'applicazione può interagire con il middleware o il plug-in nell'ambiente virtuale, dove in genere questa operazione viene impedita.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-105">This enables the application to interact with the middleware or plug-in in the virtual environment, where typically this is prevented.</span></span> <span data-ttu-id="d5ca5-106">Ciò è utile perché un pacchetto di applicazione secondario può essere usato con diverse altre applicazioni, dette le *applicazioni principali*, che consentono a ogni applicazione principale di fare riferimento allo stesso pacchetto secondario.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-106">This is useful because a secondary application package can be used with several other applications, referred to as the *primary applications*, which enables each primary application to reference the same secondary package.</span></span>

<span data-ttu-id="d5ca5-107">Quando si sequenziano applicazioni che dipendono da plug-in come controlli ActiveX o da applicazioni che dipendono da middleware come OLE DB o Java Runtime Environment (JRE), è possibile usare la composizione di una famiglia di prodotti dinamici.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-107">You can use Dynamic Suite Composition when you sequence applications that depend on plug-ins such as ActiveX controls or for applications that depend on middleware such as OLE DB or the Java Runtime Environment (JRE).</span></span> <span data-ttu-id="d5ca5-108">Se ogni applicazione che ha usato questi componenti dipendenti richiede la sequenziazione, inclusi i componenti, gli aggiornamenti di questi componenti richiedono la risequenziazione di tutte le applicazioni principali.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-108">If each application that used these dependent components required sequencing, including the components, updates to those components would require re-sequencing all the primary applications.</span></span> <span data-ttu-id="d5ca5-109">Se si sequenziano le applicazioni primarie senza i componenti e quindi si sequenzia il middleware o il plug-in come pacchetto secondario, è necessario aggiornare solo il pacchetto secondario.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-109">If you sequence the primary applications without the components and then sequence the middleware or plug-in as a secondary package, then only the secondary package must be updated.</span></span>

<span data-ttu-id="d5ca5-110">Un vantaggio di questo approccio è che riduce le dimensioni dei pacchetti principali.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-110">One advantage of this approach is that it reduces the size of the primary packages.</span></span> <span data-ttu-id="d5ca5-111">Un altro vantaggio è che offre un migliore controllo delle autorizzazioni di accesso per le applicazioni secondarie.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-111">Another advantage is that it provides you with better control of access permissions on the secondary applications.</span></span> <span data-ttu-id="d5ca5-112">Tieni presente che l'applicazione secondaria può essere in streaming in modo normale e che non deve essere completamente memorizzata nella cache per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-112">Note that the secondary application can be streamed in the regular way and does not have to be fully cached to run.</span></span>

<span data-ttu-id="d5ca5-113">Un pacchetto principale può avere più di un pacchetto secondario.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-113">A primary package can have more than one secondary package.</span></span> <span data-ttu-id="d5ca5-114">Tuttavia, è supportato un solo livello di dipendenza, quindi non è possibile definire un pacchetto secondario come dipendente da un altro pacchetto secondario.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-114">However, only one level of dependency is supported, so you cannot define a secondary package as dependent on another secondary package.</span></span> <span data-ttu-id="d5ca5-115">Anche l'applicazione secondaria può essere solo un middleware o un plug-in e non può essere un altro prodotto software completo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-115">Also the secondary application can only be middleware or a plug-in and cannot be another full software product.</span></span>

<span data-ttu-id="d5ca5-116">Se si prevede di fare in modo che diverse applicazioni primarie dipendano da un singolo prodotto middleware, verificare di aver testato questa configurazione per determinare l'effetto potenziale sulle prestazioni del sistema prima di distribuirlo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-116">If you plan to make several primary applications dependent on a single middleware product, make sure that you test this configuration to determine the potential effect on system performance before you deploy it.</span></span>

<span data-ttu-id="d5ca5-117">**Importante**  Le dipendenze del pacchetto possono essere specificate come obbligatorie per un'applicazione principale.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-117">**Important** Package dependencies can be specified as mandatory for a primary application.</span></span> <span data-ttu-id="d5ca5-118">Se un pacchetto secondario viene contrassegnato come obbligatorio e non è possibile accedervi per qualche motivo durante il caricamento, il caricamento del pacchetto secondario non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-118">If a secondary package is flagged as mandatory and it cannot be accessed for some reason during loading, the load of the secondary package will fail.</span></span> <span data-ttu-id="d5ca5-119">Inoltre, l'applicazione principale non riesce quando l'utente tenta di avviarlo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-119">Also, the primary application will fail when the user tries to start it.</span></span>

 

<span data-ttu-id="d5ca5-120">Puoi usare le procedure seguenti per creare un pacchetto secondario, sia per un componente plug-in che middleware, e quindi puoi usare la procedura finale per definire la dipendenza nel file OSD del pacchetto secondario.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-120">You can use the following procedures to create a secondary package, for either a plug-in or a middleware component, and then you can use the final procedure to define the dependency in the OSD file of the secondary package.</span></span>

**<span data-ttu-id="d5ca5-121">Per creare un pacchetto secondario per un plug-in tramite la composizione della famiglia di prodotti dinamici</span><span class="sxs-lookup"><span data-stu-id="d5ca5-121">To create a secondary package for a plug-in by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="d5ca5-122">In un computer di sequenziazione configurato con un'immagine pulita, installare Application Virtualization Sequencer e salvare lo stato del computer.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-122">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="d5ca5-123">Sequenziare l'applicazione principale e salvare il pacchetto nella cartella contenuto nel server.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-123">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

3.  <span data-ttu-id="d5ca5-124">Ripristinare il computer di sequenziazione nello stato salvato dal passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-124">Restore the sequencing computer to its saved state from step 1.</span></span>

4.  <span data-ttu-id="d5ca5-125">Installare e configurare l'applicazione principale localmente nel computer di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-125">Install and configure the primary application locally on the sequencing computer.</span></span>

    <span data-ttu-id="d5ca5-126">**Importante**  Devi specificare una nuova radice del pacchetto per il pacchetto secondario.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-126">**Important** You must specify a new package root for the secondary package.</span></span>

     

5.  <span data-ttu-id="d5ca5-127">Avviare la fase di monitoraggio del sequencer.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-127">Start the sequencer monitoring phase.</span></span>

6.  <span data-ttu-id="d5ca5-128">Installare il plug-in nel computer di sequenziazione e configurarlo in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-128">Install the plug-in on the sequencing computer and configure it as needed.</span></span>

7.  <span data-ttu-id="d5ca5-129">Aprire l'applicazione principale e verificare che il plug-in funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-129">Open the primary application, and confirm that the plug-in is working correctly.</span></span>

8.  <span data-ttu-id="d5ca5-130">Nella console sequencer creare un'applicazione fittizia per rappresentare il pacchetto secondario che conterrà il plug-in e selezionare un'icona.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-130">In the sequencer console, create a dummy application to represent the secondary package that will contain the plug-in and select an icon.</span></span>

9.  <span data-ttu-id="d5ca5-131">Salvare il pacchetto nella cartella contenuto nel server.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-131">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="d5ca5-132">**Nota**  Per facilitare la gestione dei pacchetti secondari, è consigliabile che il nome del pacchetto includa il termine "pacchetto secondario" per sottolineare che si tratta di un pacchetto che non funzionerà come applicazione autonoma, ad esempio **\ [plug in Name \] pacchetto secondario**.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-132">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Plug In Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="d5ca5-133">Per creare un pacchetto secondario per middleware usando la composizione della famiglia di prodotti dinamici</span><span class="sxs-lookup"><span data-stu-id="d5ca5-133">To create a secondary package for middleware by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="d5ca5-134">In un computer di sequenziazione configurato con un'immagine pulita, installare Application Virtualization Sequencer e salvare lo stato del computer.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-134">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="d5ca5-135">Installare il middleware localmente nel computer di sequenziazione e configurarlo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-135">Install the middleware locally on the sequencing computer, and configure it.</span></span>

3.  <span data-ttu-id="d5ca5-136">Sequenziare l'applicazione principale e salvare il pacchetto nella cartella contenuto nel server.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-136">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

4.  <span data-ttu-id="d5ca5-137">Ripristinare il computer di sequenziazione nello stato salvato dal passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-137">Restore the sequencing computer to its saved state from step 1.</span></span>

5.  <span data-ttu-id="d5ca5-138">Avviare il sequencer per creare un nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-138">Start the sequencer to create a new package.</span></span>

6.  <span data-ttu-id="d5ca5-139">Avviare la fase di monitoraggio del sequencer.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-139">Start the sequencer monitoring phase.</span></span>

7.  <span data-ttu-id="d5ca5-140">Installare l'applicazione middleware nel computer di sequenziazione e configurarla come in un'installazione tipica.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-140">Install the middleware application on the sequencing computer, and configure it as in a typical installation.</span></span>

8.  <span data-ttu-id="d5ca5-141">Completare il processo di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-141">Complete the sequencing process.</span></span>

9.  <span data-ttu-id="d5ca5-142">Salvare il pacchetto nella cartella contenuto nel server.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-142">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="d5ca5-143">**Nota**  Per facilitare la gestione dei pacchetti secondari, è consigliabile che il nome del pacchetto includa il termine "pacchetto secondario" per sottolineare che si tratta di un pacchetto che non funzionerà come applicazione autonoma, ad esempio **\ [middleware Name \] pacchetto secondario**.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-143">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Middleware Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="d5ca5-144">Per definire la dipendenza nel pacchetto principale</span><span class="sxs-lookup"><span data-stu-id="d5ca5-144">To define the dependency in the primary package</span></span>**

1. <span data-ttu-id="d5ca5-145">Nel server aprire il file OSD del pacchetto secondario per la modifica.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-145">On the server, open the OSD file of the secondary package for editing.</span></span> <span data-ttu-id="d5ca5-146">È consigliabile usare un editor XML per apportare modifiche al file OSD, tuttavia, è possibile usare il blocco note in alternativa.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-146">(It is a good idea to use an XML editor to make changes to the OSD file; however, you can use Notepad as an alternative.)</span></span>

2. <span data-ttu-id="d5ca5-147">Copiare la riga **codebase href** da tale file.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-147">Copy the **CODEBASE HREF** line from that file.</span></span>

3. <span data-ttu-id="d5ca5-148">Aprire il file OSD del pacchetto principale per la modifica.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-148">Open the OSD file of the primary package for editing.</span></span>

4. <span data-ttu-id="d5ca5-149">Inserire il <strong> &lt; tag dipendenze &gt; </strong> dopo la chiusura del tag \*\* &lt; /ENVLIST &gt; \*\* alla fine della sezione \*\* &lt; virtualenv &gt; \*\* appena prima del tag \*\* &lt; /virtualenv &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-149">Insert the <strong>&lt;DEPENDENCIES&gt;</strong>tag after the close of **&lt;/ENVLIST&gt;** tag at the end of the **&lt;VIRTUALENV&gt;** section just before the **&lt;/VIRTUALENV&gt;** tag.</span></span>

5. <span data-ttu-id="d5ca5-150">Incollare la riga **codebase href** dal pacchetto secondario dopo il tag \*\* &lt; &gt; dipendenze\*\* appena creato.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-150">Paste the **CODEBASE HREF** line from the secondary package after the **&lt;DEPENDENCIES&gt;** tag you just created.</span></span>

6. <span data-ttu-id="d5ca5-151">Se il pacchetto secondario è un pacchetto obbligatorio, il che significa che deve essere avviato prima dell'avvio del pacchetto principale, aggiungere la proprietà **obbligatorio = "true"** all'interno del tag **codebase** .</span><span class="sxs-lookup"><span data-stu-id="d5ca5-151">If the secondary package is a mandatory package, which means that it must be started before the primary package is started, add the **MANDATORY=”TRUE”** property inside the **CODEBASE** tag.</span></span> <span data-ttu-id="d5ca5-152">Se non è obbligatorio, la proprietà può essere omessa.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-152">If it is not mandatory, the property can be omitted.</span></span>

7. <span data-ttu-id="d5ca5-153">Chiudere il tag \*\* &lt; Dipendenze &gt; \*\* inserendo i seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="d5ca5-153">Close the **&lt;DEPENDENCIES&gt;** tag by inserting the following:</span></span>

   **<span data-ttu-id="d5ca5-154">&lt;/DEPENDENCIES&gt;</span><span class="sxs-lookup"><span data-stu-id="d5ca5-154">&lt;/DEPENDENCIES&gt;</span></span>**

8. <span data-ttu-id="d5ca5-155">Esaminare le modifiche apportate al file OSD e quindi salvare e chiudere il file.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-155">Review the changes that you made to the OSD file, and then save and close the file.</span></span> <span data-ttu-id="d5ca5-156">L'esempio seguente mostra il modo in cui deve essere visualizzata la sezione aggiunta.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-156">The following example shows how the added section should appear.</span></span> <span data-ttu-id="d5ca5-157">I valori di tag riportati di seguito sono ad esempio solo.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-157">The tag values shown here are for example only.</span></span>

   **<span data-ttu-id="d5ca5-158">&lt;VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="d5ca5-158">&lt;VIRTUALENV&gt;</span></span>**

        **&lt;ENVLIST&gt;**

   **<span data-ttu-id="d5ca5-159">…</span><span class="sxs-lookup"><span data-stu-id="d5ca5-159">…</span></span>**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **<span data-ttu-id="d5ca5-160">&lt;/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="d5ca5-160">&lt;/VIRTUALENV&gt;</span></span>**

9. <span data-ttu-id="d5ca5-161">Se il pacchetto secondario contiene voci nella sezione \*\* &lt; ENVLIST &gt; \*\* del file OSD, è necessario copiare le voci nella stessa sezione del pacchetto principale.</span><span class="sxs-lookup"><span data-stu-id="d5ca5-161">If the secondary package has any entries in the **&lt;ENVLIST&gt;** section of the OSD file, you must copy those entries to the same section in the primary package.</span></span>

## <span data-ttu-id="d5ca5-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5ca5-162">Related topics</span></span>


[<span data-ttu-id="d5ca5-163">Come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer</span><span class="sxs-lookup"><span data-stu-id="d5ca5-163">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





