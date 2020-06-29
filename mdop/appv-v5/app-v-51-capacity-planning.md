---
title: Pianificazione della capacità di App-V 5.1
description: Pianificazione della capacità di App-V 5.1
author: dansimp
ms.assetid: 7a98062f-5a60-49d6-ab40-dc6057e1dd5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b152536b3c61e47f3fda84489b1e102c285e01c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805986"
---
# <span data-ttu-id="edba7-103">Pianificazione della capacità di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="edba7-103">App-V 5.1 Capacity Planning</span></span>


<span data-ttu-id="edba7-104">I suggerimenti seguenti possono essere usati come previsione per determinare informazioni sulla pianificazione della capacità appropriate per l'infrastruttura dell'App-V 5,1 dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-104">The following recommendations can be used as a baseline to help determine capacity planning information that is appropriate to your organization’s App-V 5.1 infrastructure.</span></span>

<span data-ttu-id="edba7-105">**Importante**  Usare le informazioni in questa sezione solo come guida generale per la pianificazione della distribuzione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="edba7-105">**Important** Use the information in this section only as a general guide for planning your App-V 5.1 deployment.</span></span> <span data-ttu-id="edba7-106">I requisiti di capacità del sistema dipendono dai dettagli specifici dell'ambiente hardware e dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-106">Your system capacity requirements will depend on the specific details of your hardware and application environment.</span></span> <span data-ttu-id="edba7-107">Inoltre, i numeri di prestazioni visualizzati in questo documento sono esempi e i risultati possono variare.</span><span class="sxs-lookup"><span data-stu-id="edba7-107">Additionally, the performance numbers displayed in this document are examples and your results may vary.</span></span>

 

## <span data-ttu-id="edba7-108">Determinare l'ambito del progetto</span><span class="sxs-lookup"><span data-stu-id="edba7-108">Determine the Project Scope</span></span>


<span data-ttu-id="edba7-109">Prima di progettare l'infrastruttura App-V 5,1, devi determinare l'ambito del progetto.</span><span class="sxs-lookup"><span data-stu-id="edba7-109">Before you design the App-V 5.1 infrastructure, you must determine the project’s scope.</span></span> <span data-ttu-id="edba7-110">L'ambito è costituito dalla determinazione delle applicazioni che saranno disponibili virtualmente e per identificare anche gli utenti di destinazione e le rispettive posizioni.</span><span class="sxs-lookup"><span data-stu-id="edba7-110">The scope consists of determining which applications will be available virtually and to also identify the target users, and their locations.</span></span> <span data-ttu-id="edba7-111">Queste informazioni consentiranno di determinare il tipo di infrastruttura App-V 5,1 da implementare.</span><span class="sxs-lookup"><span data-stu-id="edba7-111">This information will help determine what type of App-V 5.1 infrastructure should be implemented.</span></span> <span data-ttu-id="edba7-112">Le decisioni relative all'ambito del progetto devono essere basate sulle esigenze specifiche dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-112">Decisions about the scope of the project must be based on the specific needs of your organization.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-113">Attività</span><span class="sxs-lookup"><span data-stu-id="edba7-113">Task</span></span></th>
<th align="left"><span data-ttu-id="edba7-114">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="edba7-114">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-115">Determinare l'ambito dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="edba7-115">Determine Application Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-116">A seconda delle applicazioni da virtualizzare, l'infrastruttura App-V 5,1 può essere configurata in modi diversi.</span><span class="sxs-lookup"><span data-stu-id="edba7-116">Depending on the applications to be virtualized, the App-V 5.1 infrastructure can be set up in different ways.</span></span> <span data-ttu-id="edba7-117">La prima attività consiste nel definire le applicazioni che si desidera virtualizzare.</span><span class="sxs-lookup"><span data-stu-id="edba7-117">The first task is to define what applications you want to virtualize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-118">Determinare l'ambito della posizione</span><span class="sxs-lookup"><span data-stu-id="edba7-118">Determine Location Scope</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-119">L'ambito della posizione si riferisce alle posizioni fisiche, ad esempio a livello aziendale o a una specifica posizione geografica, in cui si prevede di eseguire le applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="edba7-119">Location scope refers to the physical locations (for example, enterprise-wide or a specific geographic location) where you plan to run the virtualized applications.</span></span> <span data-ttu-id="edba7-120">Può anche riferirsi alla popolazione degli utenti, ad esempio un singolo reparto, che eseguirà le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="edba7-120">It can also refer to the user population (for example, a single department) who will run the virtual applications.</span></span> <span data-ttu-id="edba7-121">Devi ottenere una mappa di rete che includa i percorsi di connessione e la larghezza di banda disponibile per ogni posizione e il numero di utenti che usano applicazioni virtualizzate e la velocità di collegamento WAN.</span><span class="sxs-lookup"><span data-stu-id="edba7-121">You should obtain a network map that includes the connection paths as well as available bandwidth to each location and the number of users using virtualized applications and the WAN link speed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="edba7-122">Determinare l'infrastruttura di App-V 5,1 necessaria</span><span class="sxs-lookup"><span data-stu-id="edba7-122">Determine Which App-V 5.1 Infrastructure is Required</span></span>


<span data-ttu-id="edba7-123">**Importante**  Entrambi i modelli seguenti richiedono l'installazione del client App-V 5,1 nel computer in cui si prevede di eseguire applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="edba7-123">**Important** Both of the following models require the App-V 5.1 client to be installed on the computer where you plan to run virtual applications.</span></span>

<span data-ttu-id="edba7-124">Puoi anche gestire l'ambiente App-V 5,1 usando una soluzione ESD (Electronic Software Distribution), come Microsoft Systems Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="edba7-124">You can also manage your App-V 5.1 environment using an Electronic Software Distribution (ESD) solution such as Microsoft Systems Center Configuration Manager.</span></span> <span data-ttu-id="edba7-125">Per altre informazioni [, Vedi come distribuire pacchetti App-V 5,1 usando la distribuzione elettronica del software](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span><span class="sxs-lookup"><span data-stu-id="edba7-125">For more information see [How to deploy App-V 5.1 Packages Using Electronic Software Distribution](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).</span></span>

 

-   <span data-ttu-id="edba7-126">**Modello autonomo** : il modello autonomo consente alle applicazioni virtuali di essere abilitate per Windows Installer per la distribuzione senza flusso.</span><span class="sxs-lookup"><span data-stu-id="edba7-126">**Standalone Model** - The standalone model allows virtual applications to be Windows Installer-enabled for distribution without streaming.</span></span> <span data-ttu-id="edba7-127">App-V 5,1 in modalità autonoma è costituito dal sequencer e dal client; non sono necessari componenti aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="edba7-127">App-V 5.1 in Standalone Mode consists of the sequencer and the client; no additional components are required.</span></span> <span data-ttu-id="edba7-128">Le applicazioni vengono preparate per la virtualizzazione usando un processo denominato sequenziamento.</span><span class="sxs-lookup"><span data-stu-id="edba7-128">Applications are prepared for virtualization using a process called sequencing.</span></span> <span data-ttu-id="edba7-129">Per altre informazioni, Vedi [pianificazione per l'App-V 5,1 sequencer e la distribuzione del client](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="edba7-129">For more information see, [Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md).</span></span> <span data-ttu-id="edba7-130">Per gli scenari seguenti è consigliabile il modello autonomo:</span><span class="sxs-lookup"><span data-stu-id="edba7-130">The stand-alone model is recommended for the following scenarios:</span></span>

    -   <span data-ttu-id="edba7-131">Con gli utenti remoti disconnessi che non possono connettersi all'infrastruttura App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="edba7-131">With disconnected remote users who cannot connect to the App-V 5.1 infrastructure.</span></span>

    -   <span data-ttu-id="edba7-132">Quando si esegue un sistema di gestione software, ad esempio Configuration Manager 2012.</span><span class="sxs-lookup"><span data-stu-id="edba7-132">When you are running a software management system, such as Configuration Manager 2012.</span></span>

    -   <span data-ttu-id="edba7-133">Quando limitazioni della larghezza di banda della rete inibiscono la distribuzione elettronica del software.</span><span class="sxs-lookup"><span data-stu-id="edba7-133">When network bandwidth limitations inhibit electronic software distribution.</span></span>

-   <span data-ttu-id="edba7-134">**Modello di infrastruttura completa** : il modello di infrastruttura completa offre funzionalità di distribuzione, gestione e Reporting del software; include anche lo streaming di applicazioni in rete.</span><span class="sxs-lookup"><span data-stu-id="edba7-134">**Full Infrastructure Model** - The full infrastructure model provides for software distribution, management, and reporting capabilities; it also includes the streaming of applications across the network.</span></span> <span data-ttu-id="edba7-135">Il modello di infrastruttura completa App-V 5,1 è costituito da uno o più server di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="edba7-135">The App-V 5.1 Full Infrastructure Model consists of one or more App-V 5.1 management servers.</span></span> <span data-ttu-id="edba7-136">Il server di gestione può essere usato per pubblicare applicazioni in tutti i client.</span><span class="sxs-lookup"><span data-stu-id="edba7-136">The Management Server can be used to publish applications to all clients.</span></span> <span data-ttu-id="edba7-137">Il processo di pubblicazione posiziona le icone e i tasti di scelta rapida dell'applicazione virtuale nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-137">The publishing process places the virtual application icons and shortcuts on the target computer.</span></span> <span data-ttu-id="edba7-138">Può anche eseguire il flusso delle applicazioni agli utenti locali.</span><span class="sxs-lookup"><span data-stu-id="edba7-138">It can also stream applications to local users.</span></span> <span data-ttu-id="edba7-139">Per altre informazioni sull'installazione di server di gestione, vedere [pianificazione per la distribuzione del server App-V 5,1](planning-for-the-app-v-51-server-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="edba7-139">For more information about installing the management server see, [Planning for the App-V 5.1 Server Deployment](planning-for-the-app-v-51-server-deployment.md).</span></span> <span data-ttu-id="edba7-140">Il modello di infrastruttura completa è consigliato per gli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="edba7-140">The full infrastructure model is recommended for the following scenarios:</span></span>

    <span data-ttu-id="edba7-141">**Importante**  Il modello di infrastruttura completa App-V 5,1 richiede che Microsoft SQL Server memorizzi i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-141">**Important** The App-V 5.1 full infrastructure model requires Microsoft SQL Server to store configuration data.</span></span> <span data-ttu-id="edba7-142">Per altre informazioni, Vedi [configurazioni supportate in App-V 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="edba7-142">For more information see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

     

    -   <span data-ttu-id="edba7-143">Quando si vuole usare il server di gestione per pubblicare l'applicazione in computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-143">When you want to use the Management Server to publish the application to target computers.</span></span>

    -   <span data-ttu-id="edba7-144">Per il provisioning rapido delle applicazioni per i computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-144">For rapid provisioning of applications to target computers.</span></span>

    -   <span data-ttu-id="edba7-145">Quando si vuole usare la creazione di report di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="edba7-145">When you want to use App-V 5.1 reporting.</span></span>

## <span data-ttu-id="edba7-146">Linee guida per il ridimensionamento del server end-to-end</span><span class="sxs-lookup"><span data-stu-id="edba7-146">End-to-end Server Sizing Guidance</span></span>


<span data-ttu-id="edba7-147">La sezione seguente contiene informazioni sulle dimensioni e la pianificazione di app end-to-end-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="edba7-147">The following section provides information about end-to-end App-V 5.1 sizing and planning.</span></span> <span data-ttu-id="edba7-148">Per informazioni più specifiche, vedere le sezioni successive.</span><span class="sxs-lookup"><span data-stu-id="edba7-148">For more specific information, refer to the subsequent sections.</span></span>

<span data-ttu-id="edba7-149">**Nota**  Tempo di risposta di andata e ritorno nel client è il tempo impiegato dal computer che ha eseguito il client App-V 5,1 per ricevere una notifica corretta dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-149">**Note** Round trip response time on the client is the time taken by the computer running the App-V 5.1 client to receive a successful notification from the publishing server.</span></span> <span data-ttu-id="edba7-150">Tempo di risposta di andata e ritorno nel server di pubblicazione è il tempo impiegato dal computer che ha eseguito il server di pubblicazione per ricevere un aggiornamento dei metadati del pacchetto riuscito dal server di gestione.</span><span class="sxs-lookup"><span data-stu-id="edba7-150">Round trip response time on the publishing server is the time taken by the computer running the publishing server to receive a successful package metadata update from the management server.</span></span>

 

-   <span data-ttu-id="edba7-151">i client di 20.000 possono essere destinati a un singolo server di pubblicazione per ottenere il pacchetto aggiornato in un periodo di tempo di andata e ritorno accettabile.</span><span class="sxs-lookup"><span data-stu-id="edba7-151">20,000 clients can target a single publishing server to obtain the package refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="edba7-152">( &lt; 3 secondi)</span><span class="sxs-lookup"><span data-stu-id="edba7-152">(&lt;3 seconds)</span></span>

-   <span data-ttu-id="edba7-153">Un singolo server di gestione può supportare fino a 50 server di pubblicazione per l'aggiornamento dei metadati del pacchetto in un periodo di tempo di andata e ritorno accettabile.</span><span class="sxs-lookup"><span data-stu-id="edba7-153">A single management server can support up to 50 publishing servers for package metadata refreshes in an acceptable round trip time.</span></span> <span data-ttu-id="edba7-154">( &lt; 5 secondi)</span><span class="sxs-lookup"><span data-stu-id="edba7-154">(&lt;5 seconds)</span></span>

## <a href="" id="---------app-v-5-1-management-server-capacity-planning-recommendations"></a> <span data-ttu-id="edba7-155">Suggerimenti per la pianificazione della capacità di gestione del server di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="edba7-155">App-V 5.1 Management Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="edba7-156">I server di pubblicazione App-V 5,1 richiedono il server di gestione per le richieste di aggiornamento del pacchetto e le risposte di aggiornamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edba7-156">The App-V 5.1 publishing servers require the management server for package refresh requests and package refresh responses.</span></span> <span data-ttu-id="edba7-157">Il server di gestione invia quindi le informazioni al database di gestione per recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="edba7-157">The management server then sends the information to the management database to retrieve information.</span></span> <span data-ttu-id="edba7-158">Per altre informazioni sulle configurazioni supportate in App-V 5,1, vedere [configurazioni supportate in App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="edba7-158">For more information about App-V 5.1 management server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="edba7-159">**Nota**  Il tempo di aggiornamento predefinito nel server di pubblicazione App-V 5,1 è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="edba7-159">**Note** The default refresh time on the App-V 5.1 publishing server is ten minutes.</span></span>

 

<span data-ttu-id="edba7-160">Quando più server di pubblicazione simultanei contattano un singolo server di gestione per aggiornare i metadati dei pacchetti, i tre fattori seguenti influenzano il tempo di risposta di andata e ritorno sul server di pubblicazione:</span><span class="sxs-lookup"><span data-stu-id="edba7-160">When multiple simultaneous publishing servers contact a single management server for package metadata refreshes, the following three factors influence the round trip response time on the publishing server:</span></span>

1.  <span data-ttu-id="edba7-161">Numero di server di pubblicazione che effettuano richieste simultanee.</span><span class="sxs-lookup"><span data-stu-id="edba7-161">Number of publishing servers making simultaneous requests.</span></span>

2.  <span data-ttu-id="edba7-162">Numero di gruppi di connessioni configurati nel server di gestione.</span><span class="sxs-lookup"><span data-stu-id="edba7-162">Number of connection groups configured on the management server.</span></span>

3.  <span data-ttu-id="edba7-163">Numero di gruppi di Access configurati nel server di gestione.</span><span class="sxs-lookup"><span data-stu-id="edba7-163">Number of access groups configured on the management server.</span></span>

<span data-ttu-id="edba7-164">Nella tabella seguente vengono visualizzate altre informazioni su ogni fattore che impatta sul tempo di andata e ritorno.</span><span class="sxs-lookup"><span data-stu-id="edba7-164">The following table displays more information about each factor that impacts round trip time.</span></span>

<span data-ttu-id="edba7-165">**Nota**  Tempo di risposta di andata e ritorno è il tempo impiegato dal computer che ha eseguito il server di pubblicazione App-V 5,1 per ricevere un aggiornamento dei metadati del pacchetto riuscito dal server di gestione.</span><span class="sxs-lookup"><span data-stu-id="edba7-165">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 publishing server to receive a successful package metadata update from the management server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-166">Fattori che influiscono sul tempo di risposta di round trip</span><span class="sxs-lookup"><span data-stu-id="edba7-166">Factors impacting round trip response time</span></span></th>
<th align="left"><span data-ttu-id="edba7-167">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="edba7-167">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-168">Il numero di server di pubblicazione che richiedono contemporaneamente l'aggiornamento dei metadati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edba7-168">The number of publishing servers simultaneously requesting package metadata refreshes.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-169">Un singolo server di gestione può rispondere a un massimo di 320 server di pubblicazione che richiedono contemporaneamente la pubblicazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="edba7-169">A single management server can respond to up to 320 publishing servers requesting publishing metadata simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="edba7-170">Tempo di risposta di andata e ritorno per i server di 320 pub è di ~ 40 secondi.</span><span class="sxs-lookup"><span data-stu-id="edba7-170">Round trip response time for 320 pub servers is ~40 seconds.</span></span></p></li>
<li><p><span data-ttu-id="edba7-171">Per &lt; i server di pubblicazione di 50 che richiedono metadati contemporaneamente, il tempo di risposta di andata e ritorno è di &lt; 5 secondi.</span><span class="sxs-lookup"><span data-stu-id="edba7-171">For &lt;50 publishing servers requesting metadata simultaneously, the round trip response time is &lt;5 seconds.</span></span></p></li>
<li><p><span data-ttu-id="edba7-172">Da 50 a 320 Publishing Servers, il tempo di risposta aumenta linearmente (circa 2x).</span><span class="sxs-lookup"><span data-stu-id="edba7-172">From 50 to 320 publishing servers, the response time increases linearly (approximately 2x).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-173">Numero di gruppi di connessioni configurati nel server di gestione.</span><span class="sxs-lookup"><span data-stu-id="edba7-173">The number of connection groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-174">Per i gruppi di connessioni fino a 100 non sono presenti cambiamenti significativi nel tempo di risposta di andata e ritorno nel server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-174">For up to 100 connection groups, there is no significant change in the round trip response time on the publishing server.</span></span></p></li>
<li><p><span data-ttu-id="edba7-175">Per i gruppi di connessioni di 100-400, il tempo di risposta di andata e ritorno è minore.</span><span class="sxs-lookup"><span data-stu-id="edba7-175">For 100 - 400 connection groups, there is a minor linear increase in the round trip response time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-176">Numero di gruppi di Access configurati nel server di gestione.</span><span class="sxs-lookup"><span data-stu-id="edba7-176">The number of access groups configured on the management server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-177">Per un massimo di 40 gruppi di Access, c'è un aumento lineare (circa 3x) nel tempo di risposta di andata e ritorno sul server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-177">For up to 40 access groups, there is a linear (approximately 3x) increase in the round trip response time on the publishing server.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="edba7-178">Nella tabella seguente vengono visualizzati i valori di esempio per ognuno dei fattori precedenti.</span><span class="sxs-lookup"><span data-stu-id="edba7-178">The following table displays sample values for each of the previous factors.</span></span> <span data-ttu-id="edba7-179">In ogni variante i pacchetti di 120 vengono aggiornati dal server di gestione di App-V 5.1.</span><span class="sxs-lookup"><span data-stu-id="edba7-179">In each variation, 120 packages are refreshed from the App-V 5.1management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-180">Scenario</span><span class="sxs-lookup"><span data-stu-id="edba7-180">Scenario</span></span></th>
<th align="left"><span data-ttu-id="edba7-181">Variante</span><span class="sxs-lookup"><span data-stu-id="edba7-181">Variation</span></span></th>
<th align="left"><span data-ttu-id="edba7-182">Numero di gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="edba7-182">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="edba7-183">Numero di gruppi di Access</span><span class="sxs-lookup"><span data-stu-id="edba7-183">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="edba7-184">Numero di server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="edba7-184">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="edba7-185">Server di pubblicazione/server di gestione del tipo di connessione di rete</span><span class="sxs-lookup"><span data-stu-id="edba7-185">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="edba7-186">Tempo di risposta di andata e ritorno nel server di pubblicazione (in secondi)</span><span class="sxs-lookup"><span data-stu-id="edba7-186">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="edba7-187">Utilizzo della CPU in server di gestione</span><span class="sxs-lookup"><span data-stu-id="edba7-187">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-188">Server di pubblicazione che contattano simultaneamente server di gestione per la pubblicazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="edba7-188">Publishing servers simultaneously contacting management server for publishing metadata.</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-189">Numero di server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="edba7-189">Number of publishing servers</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-190">0</span><span class="sxs-lookup"><span data-stu-id="edba7-190">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-191">0</span><span class="sxs-lookup"><span data-stu-id="edba7-191">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-192">0</span><span class="sxs-lookup"><span data-stu-id="edba7-192">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-193">0</span><span class="sxs-lookup"><span data-stu-id="edba7-193">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-194">0</span><span class="sxs-lookup"><span data-stu-id="edba7-194">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-195">0</span><span class="sxs-lookup"><span data-stu-id="edba7-195">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-196">1</span><span class="sxs-lookup"><span data-stu-id="edba7-196">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-197">1</span><span class="sxs-lookup"><span data-stu-id="edba7-197">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-198">1</span><span class="sxs-lookup"><span data-stu-id="edba7-198">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-199">1</span><span class="sxs-lookup"><span data-stu-id="edba7-199">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-200">1</span><span class="sxs-lookup"><span data-stu-id="edba7-200">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-201">1</span><span class="sxs-lookup"><span data-stu-id="edba7-201">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-202">50</span><span class="sxs-lookup"><span data-stu-id="edba7-202">50</span></span></p></li>
<li><p><span data-ttu-id="edba7-203">100</span><span class="sxs-lookup"><span data-stu-id="edba7-203">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-204">200</span><span class="sxs-lookup"><span data-stu-id="edba7-204">200</span></span></p></li>
<li><p><span data-ttu-id="edba7-205">300</span><span class="sxs-lookup"><span data-stu-id="edba7-205">300</span></span></p></li>
<li><p><span data-ttu-id="edba7-206">315</span><span class="sxs-lookup"><span data-stu-id="edba7-206">315</span></span></p></li>
<li><p><span data-ttu-id="edba7-207">320</span><span class="sxs-lookup"><span data-stu-id="edba7-207">320</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-208">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-208">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-209">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-209">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-210">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-210">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-211">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-211">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-212">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-212">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-213">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-213">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-214">5</span><span class="sxs-lookup"><span data-stu-id="edba7-214">5</span></span></p></li>
<li><p><span data-ttu-id="edba7-215">10</span><span class="sxs-lookup"><span data-stu-id="edba7-215">10</span></span></p></li>
<li><p><span data-ttu-id="edba7-216">19</span><span class="sxs-lookup"><span data-stu-id="edba7-216">19</span></span></p></li>
<li><p><span data-ttu-id="edba7-217">32</span><span class="sxs-lookup"><span data-stu-id="edba7-217">32</span></span></p></li>
<li><p><span data-ttu-id="edba7-218">30</span><span class="sxs-lookup"><span data-stu-id="edba7-218">30</span></span></p></li>
<li><p><span data-ttu-id="edba7-219">37</span><span class="sxs-lookup"><span data-stu-id="edba7-219">37</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-220">17</span><span class="sxs-lookup"><span data-stu-id="edba7-220">17</span></span></p></li>
<li><p><span data-ttu-id="edba7-221">17</span><span class="sxs-lookup"><span data-stu-id="edba7-221">17</span></span></p></li>
<li><p><span data-ttu-id="edba7-222">17</span><span class="sxs-lookup"><span data-stu-id="edba7-222">17</span></span></p></li>
<li><p><span data-ttu-id="edba7-223">15</span><span class="sxs-lookup"><span data-stu-id="edba7-223">15</span></span></p></li>
<li><p><span data-ttu-id="edba7-224">17</span><span class="sxs-lookup"><span data-stu-id="edba7-224">17</span></span></p></li>
<li><p><span data-ttu-id="edba7-225">15</span><span class="sxs-lookup"><span data-stu-id="edba7-225">15</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-226">I metadati di pubblicazione contengono gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="edba7-226">Publishing metadata contains connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-227">Numero di gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="edba7-227">Number of connection groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-228">10</span><span class="sxs-lookup"><span data-stu-id="edba7-228">10</span></span></p></li>
<li><p><span data-ttu-id="edba7-229">50</span><span class="sxs-lookup"><span data-stu-id="edba7-229">50</span></span></p></li>
<li><p><span data-ttu-id="edba7-230">100</span><span class="sxs-lookup"><span data-stu-id="edba7-230">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-231">150</span><span class="sxs-lookup"><span data-stu-id="edba7-231">150</span></span></p></li>
<li><p><span data-ttu-id="edba7-232">300</span><span class="sxs-lookup"><span data-stu-id="edba7-232">300</span></span></p></li>
<li><p><span data-ttu-id="edba7-233">400</span><span class="sxs-lookup"><span data-stu-id="edba7-233">400</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-234">1</span><span class="sxs-lookup"><span data-stu-id="edba7-234">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-235">1</span><span class="sxs-lookup"><span data-stu-id="edba7-235">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-236">1</span><span class="sxs-lookup"><span data-stu-id="edba7-236">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-237">1</span><span class="sxs-lookup"><span data-stu-id="edba7-237">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-238">1</span><span class="sxs-lookup"><span data-stu-id="edba7-238">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-239">1</span><span class="sxs-lookup"><span data-stu-id="edba7-239">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-240">100</span><span class="sxs-lookup"><span data-stu-id="edba7-240">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-241">100</span><span class="sxs-lookup"><span data-stu-id="edba7-241">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-242">100</span><span class="sxs-lookup"><span data-stu-id="edba7-242">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-243">100</span><span class="sxs-lookup"><span data-stu-id="edba7-243">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-244">100</span><span class="sxs-lookup"><span data-stu-id="edba7-244">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-245">100</span><span class="sxs-lookup"><span data-stu-id="edba7-245">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-246">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-246">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-247">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-247">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-248">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-248">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-249">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-249">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-250">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-250">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-251">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-251">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-252">10</span><span class="sxs-lookup"><span data-stu-id="edba7-252">10</span></span></p></li>
<li><p><span data-ttu-id="edba7-253">11</span><span class="sxs-lookup"><span data-stu-id="edba7-253">11</span></span></p></li>
<li><p><span data-ttu-id="edba7-254">11</span><span class="sxs-lookup"><span data-stu-id="edba7-254">11</span></span></p></li>
<li><p><span data-ttu-id="edba7-255">16</span><span class="sxs-lookup"><span data-stu-id="edba7-255">16</span></span></p></li>
<li><p><span data-ttu-id="edba7-256">22</span><span class="sxs-lookup"><span data-stu-id="edba7-256">22</span></span></p></li>
<li><p><span data-ttu-id="edba7-257">25</span><span class="sxs-lookup"><span data-stu-id="edba7-257">25</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-258">17</span><span class="sxs-lookup"><span data-stu-id="edba7-258">17</span></span></p></li>
<li><p><span data-ttu-id="edba7-259">19</span><span class="sxs-lookup"><span data-stu-id="edba7-259">19</span></span></p></li>
<li><p><span data-ttu-id="edba7-260">22</span><span class="sxs-lookup"><span data-stu-id="edba7-260">22</span></span></p></li>
<li><p><span data-ttu-id="edba7-261">19</span><span class="sxs-lookup"><span data-stu-id="edba7-261">19</span></span></p></li>
<li><p><span data-ttu-id="edba7-262">20</span><span class="sxs-lookup"><span data-stu-id="edba7-262">20</span></span></p></li>
<li><p><span data-ttu-id="edba7-263">20</span><span class="sxs-lookup"><span data-stu-id="edba7-263">20</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-264">I metadati di pubblicazione contengono gruppi di Access</span><span class="sxs-lookup"><span data-stu-id="edba7-264">Publishing metadata contains access groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-265">Numero di gruppi di Access</span><span class="sxs-lookup"><span data-stu-id="edba7-265">Number of access groups</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-266">0</span><span class="sxs-lookup"><span data-stu-id="edba7-266">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-267">0</span><span class="sxs-lookup"><span data-stu-id="edba7-267">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-268">0</span><span class="sxs-lookup"><span data-stu-id="edba7-268">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-269">0</span><span class="sxs-lookup"><span data-stu-id="edba7-269">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-270">1</span><span class="sxs-lookup"><span data-stu-id="edba7-270">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-271">10</span><span class="sxs-lookup"><span data-stu-id="edba7-271">10</span></span></p></li>
<li><p><span data-ttu-id="edba7-272">20</span><span class="sxs-lookup"><span data-stu-id="edba7-272">20</span></span></p></li>
<li><p><span data-ttu-id="edba7-273">40</span><span class="sxs-lookup"><span data-stu-id="edba7-273">40</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-274">100</span><span class="sxs-lookup"><span data-stu-id="edba7-274">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-275">100</span><span class="sxs-lookup"><span data-stu-id="edba7-275">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-276">100</span><span class="sxs-lookup"><span data-stu-id="edba7-276">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-277">100</span><span class="sxs-lookup"><span data-stu-id="edba7-277">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-278">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-278">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-279">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-279">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-280">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-280">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-281">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-281">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-282">10</span><span class="sxs-lookup"><span data-stu-id="edba7-282">10</span></span></p></li>
<li><p><span data-ttu-id="edba7-283">43</span><span class="sxs-lookup"><span data-stu-id="edba7-283">43</span></span></p></li>
<li><p><span data-ttu-id="edba7-284">153</span><span class="sxs-lookup"><span data-stu-id="edba7-284">153</span></span></p></li>
<li><p><span data-ttu-id="edba7-285">535</span><span class="sxs-lookup"><span data-stu-id="edba7-285">535</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-286">17</span><span class="sxs-lookup"><span data-stu-id="edba7-286">17</span></span></p></li>
<li><p><span data-ttu-id="edba7-287">26</span><span class="sxs-lookup"><span data-stu-id="edba7-287">26</span></span></p></li>
<li><p><span data-ttu-id="edba7-288">24</span><span class="sxs-lookup"><span data-stu-id="edba7-288">24</span></span></p></li>
<li><p><span data-ttu-id="edba7-289">24</span><span class="sxs-lookup"><span data-stu-id="edba7-289">24</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="edba7-290">L'utilizzo della CPU del computer che gestisce il server di gestione è di circa il 25%, indipendentemente dal numero di server di pubblicazione che ne fanno riferimento.</span><span class="sxs-lookup"><span data-stu-id="edba7-290">The CPU utilization of the computer running the management server is around 25% irrespective of the number of publishing servers targeting it.</span></span> <span data-ttu-id="edba7-291">Le transazioni del database di Microsoft SQL Server al secondo, le richieste batch/sec e le connessioni utente sono identiche indipendentemente dal numero di server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-291">The Microsoft SQL Server database transactions/sec, batch requests/sec and user connections are identical irrespective of the number of publishing servers.</span></span> <span data-ttu-id="edba7-292">Ad esempio: transazioni/sec è ~ 30, richieste batch ~ 200 e l'utente si connette a ~ 6.</span><span class="sxs-lookup"><span data-stu-id="edba7-292">For example: Transactions/sec is ~30, batch requests ~200, and user connects ~6.</span></span>

<span data-ttu-id="edba7-293">Usando una distribuzione geograficamente distribuita, in cui il server di gestione & i server di pubblicazione utilizzano una rete di collegamento lenta tra di essi, il tempo di risposta di andata e ritorno nei server di pubblicazione è entro limiti di tempo accettabili ( &lt; 5 secondi), anche per le richieste simultanee di 100 su un singolo server di gestione.</span><span class="sxs-lookup"><span data-stu-id="edba7-293">Using a geographically distributed deployment, where the management server & publishing servers utilize a slow link network between them, the round trip response time on the publishing servers is within acceptable time limits (&lt;5 seconds), even for 100 simultaneous requests on a single management server.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-294">Scenario</span><span class="sxs-lookup"><span data-stu-id="edba7-294">Scenario</span></span></th>
<th align="left"><span data-ttu-id="edba7-295">Variante</span><span class="sxs-lookup"><span data-stu-id="edba7-295">Variation</span></span></th>
<th align="left"><span data-ttu-id="edba7-296">Numero di gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="edba7-296">Number of connection groups</span></span></th>
<th align="left"><span data-ttu-id="edba7-297">Numero di gruppi di Access</span><span class="sxs-lookup"><span data-stu-id="edba7-297">Number of access groups</span></span></th>
<th align="left"><span data-ttu-id="edba7-298">Numero di server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="edba7-298">Number of publishing servers</span></span></th>
<th align="left"><span data-ttu-id="edba7-299">Server di pubblicazione/server di gestione del tipo di connessione di rete</span><span class="sxs-lookup"><span data-stu-id="edba7-299">Network connection type publishing server / management server</span></span></th>
<th align="left"><span data-ttu-id="edba7-300">Tempo di risposta di andata e ritorno nel server di pubblicazione (in secondi)</span><span class="sxs-lookup"><span data-stu-id="edba7-300">Round trip response time on the publishing server (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="edba7-301">Utilizzo della CPU in server di gestione</span><span class="sxs-lookup"><span data-stu-id="edba7-301">CPU utilization on management server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-302">Connessione di rete tra il server di pubblicazione e il server di gestione</span><span class="sxs-lookup"><span data-stu-id="edba7-302">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-303">Rete di collegamento lenta di 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="edba7-303">1.5 Mbps Slow link Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-304">0</span><span class="sxs-lookup"><span data-stu-id="edba7-304">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-305">0</span><span class="sxs-lookup"><span data-stu-id="edba7-305">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-306">1</span><span class="sxs-lookup"><span data-stu-id="edba7-306">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-307">1</span><span class="sxs-lookup"><span data-stu-id="edba7-307">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-308">50</span><span class="sxs-lookup"><span data-stu-id="edba7-308">50</span></span></p></li>
<li><p><span data-ttu-id="edba7-309">100</span><span class="sxs-lookup"><span data-stu-id="edba7-309">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-310">Cavo DSL a 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="edba7-310">1.5Mbps Cable DSL</span></span></p></li>
<li><p><span data-ttu-id="edba7-311">Cavo DSL a 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="edba7-311">1.5Mbps Cable DSL</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-312">4</span><span class="sxs-lookup"><span data-stu-id="edba7-312">4</span></span></p></li>
<li><p><span data-ttu-id="edba7-313">5</span><span class="sxs-lookup"><span data-stu-id="edba7-313">5</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-314">1</span><span class="sxs-lookup"><span data-stu-id="edba7-314">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-315">2</span><span class="sxs-lookup"><span data-stu-id="edba7-315">2</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-316">Connessione di rete tra il server di pubblicazione e il server di gestione</span><span class="sxs-lookup"><span data-stu-id="edba7-316">Network connection between the publishing server and management server</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-317">Rete LAN/WIFI</span><span class="sxs-lookup"><span data-stu-id="edba7-317">LAN / WIFI Network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-318">0</span><span class="sxs-lookup"><span data-stu-id="edba7-318">0</span></span></p></li>
<li><p><span data-ttu-id="edba7-319">0</span><span class="sxs-lookup"><span data-stu-id="edba7-319">0</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-320">1</span><span class="sxs-lookup"><span data-stu-id="edba7-320">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-321">1</span><span class="sxs-lookup"><span data-stu-id="edba7-321">1</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-322">100</span><span class="sxs-lookup"><span data-stu-id="edba7-322">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-323">200</span><span class="sxs-lookup"><span data-stu-id="edba7-323">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-324">Wifi</span><span class="sxs-lookup"><span data-stu-id="edba7-324">Wifi</span></span></p></li>
<li><p><span data-ttu-id="edba7-325">Wifi</span><span class="sxs-lookup"><span data-stu-id="edba7-325">Wifi</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-326">11</span><span class="sxs-lookup"><span data-stu-id="edba7-326">11</span></span></p></li>
<li><p><span data-ttu-id="edba7-327">20</span><span class="sxs-lookup"><span data-stu-id="edba7-327">20</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-328">15</span><span class="sxs-lookup"><span data-stu-id="edba7-328">15</span></span></p></li>
<li><p><span data-ttu-id="edba7-329">17</span><span class="sxs-lookup"><span data-stu-id="edba7-329">17</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="edba7-330">Se il server di gestione e i server di pubblicazione sono connessi tramite una rete a collegamento lento o una rete ad alta velocità, il server di gestione può gestire circa 15.000 richieste di aggiornamento dei pacchetti in 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="edba7-330">Whether the management server and publishing servers are connected over a slow link network, or a high speed network, the management server can handle approximately 15,000 package refresh requests in 30 minutes.</span></span>

## <a href="" id="---------app-v-5-1-reporting-server-capacity-planning-recommendations"></a> <span data-ttu-id="edba7-331">Suggerimenti per la pianificazione della capacità di Reporting Server di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="edba7-331">App-V 5.1 Reporting Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="edba7-332">I client App-V 5,1 inviano i dati dei report al server di report.</span><span class="sxs-lookup"><span data-stu-id="edba7-332">App-V 5.1 clients send reporting data to the reporting server.</span></span> <span data-ttu-id="edba7-333">Il server di Reporting registra quindi le informazioni nel database di Microsoft SQL Server e restituisce una notifica corretta al computer che ha eseguito App-V 5,1 client.</span><span class="sxs-lookup"><span data-stu-id="edba7-333">The reporting server then records the information in the Microsoft SQL Server database and returns a successful notification back to the computer running App-V 5.1 client.</span></span> <span data-ttu-id="edba7-334">Per altre informazioni sulle configurazioni supportate in App-V 5,1, vedere [configurazioni supportate in App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="edba7-334">For more information about App-V 5.1 Reporting Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="edba7-335">**Nota**  Tempo di risposta di andata e ritorno è il tempo impiegato dal computer che ha eseguito il client App-V 5,1 per inviare le informazioni di segnalazione al server di report e ricevere una notifica corretta dal server di report.</span><span class="sxs-lookup"><span data-stu-id="edba7-335">**Note** Round trip response time is the time taken by the computer running the App-V 5.1 client to send the reporting information to the reporting server and receive a successful notification from the reporting server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-336">Scenario</span><span class="sxs-lookup"><span data-stu-id="edba7-336">Scenario</span></span></th>
<th align="left"><span data-ttu-id="edba7-337">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="edba7-337">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-338">Più client App-V 5,1 inviano contemporaneamente informazioni di report al server di report.</span><span class="sxs-lookup"><span data-stu-id="edba7-338">Multiple App-V 5.1 clients send reporting information to the reporting server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-339">Il tempo di risposta di andata e ritorno dal server di report è di 2,6 secondi per i client 500.</span><span class="sxs-lookup"><span data-stu-id="edba7-339">Round trip response time from the reporting server is 2.6 seconds for 500 clients.</span></span></p></li>
<li><p><span data-ttu-id="edba7-340">Il tempo di risposta di andata e ritorno dal server di report è di 5,65 secondi per i client 1000.</span><span class="sxs-lookup"><span data-stu-id="edba7-340">Round trip response time from the reporting server is 5.65 seconds for 1000 clients.</span></span></p></li>
<li><p><span data-ttu-id="edba7-341">Il tempo di risposta di andata e ritorno aumenta linearmente a seconda del numero di client.</span><span class="sxs-lookup"><span data-stu-id="edba7-341">Round trip response time increases linearly depending on number of clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-342">Richieste al secondo elaborate dal server di report.</span><span class="sxs-lookup"><span data-stu-id="edba7-342">Requests per second processed by the reporting server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-343">Un singolo server di report e un singolo database possono elaborare un massimo di 139 richieste al secondo.</span><span class="sxs-lookup"><span data-stu-id="edba7-343">A single reporting server and a single database, can process a maximum of 139 requests per second.</span></span> <span data-ttu-id="edba7-344">La media è 121 richieste al secondo.</span><span class="sxs-lookup"><span data-stu-id="edba7-344">The average is 121 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="edba7-345">Se si usano due report server di report nello stesso database di Microsoft SQL Server, la media delle richieste/secondo è simile a un singolo server di report = ~ 127, con un massimo di 278 richieste al secondo.</span><span class="sxs-lookup"><span data-stu-id="edba7-345">Using two reporting servers reporting to the same Microsoft SQL Server database, the average requests/second is similar to a single reporting server = ~127, with a max of 278 requests/second.</span></span></p></li>
<li><p><span data-ttu-id="edba7-346">Un singolo server di report può elaborare connessioni simultanee/attive di 500.</span><span class="sxs-lookup"><span data-stu-id="edba7-346">A single reporting server can process 500 concurrent/active connections.</span></span></p></li>
<li><p><span data-ttu-id="edba7-347">Un singolo server di report può elaborare un massimo di connessioni simultanee di 1500.</span><span class="sxs-lookup"><span data-stu-id="edba7-347">A single reporting server can process a maximum 1500 concurrent connections.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-348">Database di report.</span><span class="sxs-lookup"><span data-stu-id="edba7-348">Reporting Database.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-349">Bloccare il conflitto nel computer che ha eseguito Microsoft SQL Server è il fattore limitante per le richieste al secondo.</span><span class="sxs-lookup"><span data-stu-id="edba7-349">Lock contention on the computer running Microsoft SQL Server is the limiting factor for requests/second.</span></span></p></li>
<li><p><span data-ttu-id="edba7-350">La velocità effettiva e i tempi di risposta sono indipendenti dalle dimensioni del database.</span><span class="sxs-lookup"><span data-stu-id="edba7-350">Throughput and response time are independent of database size.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="edba7-351">**Calcolo del ritardo casuale**:</span><span class="sxs-lookup"><span data-stu-id="edba7-351">**Calculating random delay**:</span></span>

<span data-ttu-id="edba7-352">Il ritardo casuale specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="edba7-352">The random delay specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="edba7-353">Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra **0** e **ReportingRandomDelay** e attenderà la durata specificata prima di inviare i dati.</span><span class="sxs-lookup"><span data-stu-id="edba7-353">When the scheduled task is started, the client generates a random delay between **0** and **ReportingRandomDelay** and will wait the specified duration before sending data.</span></span>

<span data-ttu-id="edba7-354">Ritardo casuale = 4 \ \* numero di richieste client/media al secondo.</span><span class="sxs-lookup"><span data-stu-id="edba7-354">Random delay = 4 \* number of clients / average requests per second.</span></span>

<span data-ttu-id="edba7-355">Esempio: per i client di 500, con 120 richieste al secondo, il ritardo casuale è, 4 \ \* 500/120 = ~ 17 minuti.</span><span class="sxs-lookup"><span data-stu-id="edba7-355">Example: For 500 clients, with 120 requests per second, the Random delay is, 4 \* 500 / 120 = ~17 minutes.</span></span>

## <a href="" id="---------app-v-5-1-publishing-server-capacity-planning-recommendations"></a> <span data-ttu-id="edba7-356">Suggerimenti per la pianificazione della capacità del server di pubblicazione App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="edba7-356">App-V 5.1 Publishing Server Capacity Planning Recommendations</span></span>


<span data-ttu-id="edba7-357">I computer che eseguono il client App-V 5,1 si connettono al server di pubblicazione App-V 5,1 per inviare una richiesta di aggiornamento della pubblicazione e per ricevere una risposta.</span><span class="sxs-lookup"><span data-stu-id="edba7-357">Computers running the App-V 5.1 client connect to the App-V 5.1 publishing server to send a publishing refresh request and to receive a response.</span></span> <span data-ttu-id="edba7-358">Il tempo di risposta di andata e ritorno viene misurato nel computer che gestisce il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="edba7-358">Round trip response time is measured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="edba7-359">Il tempo del processore viene misurato nel server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-359">Processor time is measured on the publishing server.</span></span> <span data-ttu-id="edba7-360">Per altre informazioni sulle configurazioni supportate da App-V 5,1, vedere [configurazioni supportate in App-v 5,1](app-v-51-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="edba7-360">For more information about App-V 5.1 Publishing Server supported configurations see [App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md).</span></span>

<span data-ttu-id="edba7-361">**Importante**  L'elenco seguente mostra i fattori principali da tenere in considerazione durante la configurazione del server di pubblicazione App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="edba7-361">**Important** The following list displays the main factors to consider when setting up the App-V 5.1 publishing server:</span></span>

-   <span data-ttu-id="edba7-362">Numero di client che si connettono contemporaneamente a un singolo server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-362">The number of clients connecting simultaneously to a single publishing server.</span></span>

-   <span data-ttu-id="edba7-363">Numero di pacchetti in ogni aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="edba7-363">The number of packages in each refresh.</span></span>

-   <span data-ttu-id="edba7-364">Larghezza di banda di rete disponibile nell'ambiente tra il client e il server di pubblicazione App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="edba7-364">The available network bandwidth in your environment between the client and the App-V 5.1 publishing server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-365">Scenario</span><span class="sxs-lookup"><span data-stu-id="edba7-365">Scenario</span></span></th>
<th align="left"><span data-ttu-id="edba7-366">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="edba7-366">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-367">Più client App-V 5,1 si connettono contemporaneamente a un singolo server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-367">Multiple App-V 5.1 clients connect to a single publishing server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-368">Un server di pubblicazione che gestisce processori dual core può rispondere alla maggior parte dei client di 5000 che richiedono un aggiornamento simultaneo.</span><span class="sxs-lookup"><span data-stu-id="edba7-368">A publishing server running dual core processors can respond to at most 5000 clients requesting a refresh simultaneously.</span></span></p></li>
<li><p><span data-ttu-id="edba7-369">Per i client di 5000-10000, il server di pubblicazione richiede un quad core minimo.</span><span class="sxs-lookup"><span data-stu-id="edba7-369">For 5000-10000 clients, the publishing server requires a minimum quad core.</span></span></p></li>
<li><p><span data-ttu-id="edba7-370">Per i client di 10000-20000, il server di pubblicazione dovrebbe avere nuclei Quad duali per i tempi di risposta più efficienti.</span><span class="sxs-lookup"><span data-stu-id="edba7-370">For 10000-20000 clients, the publishing server should have dual quad cores for more efficient response times.</span></span></p></li>
<li><p><span data-ttu-id="edba7-371">Un server di pubblicazione con un quad-core può aggiornare fino a 10000 pacchetti entro 3 secondi.</span><span class="sxs-lookup"><span data-stu-id="edba7-371">A publishing server with a quad core can refresh up to 10000 packages within 3 seconds.</span></span> <span data-ttu-id="edba7-372">(Supporto di client simultanei di 10000)</span><span class="sxs-lookup"><span data-stu-id="edba7-372">(Supporting 10000 simultaneous clients)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-373">Numero di pacchetti in ogni aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="edba7-373">Number of packages in each refresh.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-374">Il numero crescente di pacchetti aumenterà il tempo di risposta di ~ 40% (fino a 1000 pacchetti).</span><span class="sxs-lookup"><span data-stu-id="edba7-374">Increasing number of packages will increase response time by ~40% (up to 1000 packages).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-375">Rete tra il client App-V 5,1 e il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="edba7-375">Network between the App-V 5.1 client and the publishing server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-376">In una rete lenta (larghezza di banda di 1,5 Mbps) è aumentato il 97% del tempo di risposta rispetto alla LAN (fino a 1000 utenti).</span><span class="sxs-lookup"><span data-stu-id="edba7-376">Across a slow network (1.5 Mbps bandwidth), there is a 97% increase in response time compared to LAN (up to 1000 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="edba7-377">**Nota**  L'utilizzo della CPU del server di pubblicazione è sempre elevato durante l'intervallo di tempo in cui è necessario elaborare le richieste simultanee ( &gt; 90% nella maggior parte dei casi).</span><span class="sxs-lookup"><span data-stu-id="edba7-377">**Note** The publishing server CPU usage is always high during the time interval when it has to process simultaneous requests (&gt;90% in most cases).</span></span> <span data-ttu-id="edba7-378">Il server di pubblicazione può gestire le richieste client ~ 1500 in un secondo.</span><span class="sxs-lookup"><span data-stu-id="edba7-378">The publishing server can handle ~1500 client requests in 1 second.</span></span>

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-379">Scenario</span><span class="sxs-lookup"><span data-stu-id="edba7-379">Scenario</span></span></th>
<th align="left"><span data-ttu-id="edba7-380">Variante</span><span class="sxs-lookup"><span data-stu-id="edba7-380">Variation</span></span></th>
<th align="left"><span data-ttu-id="edba7-381">Numero di client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="edba7-381">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="edba7-382">Numero di pacchetti</span><span class="sxs-lookup"><span data-stu-id="edba7-382">Number of packages</span></span></th>
<th align="left"><span data-ttu-id="edba7-383">Configurazione del processore nel server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="edba7-383">Processor configuration on the publishing server</span></span></th>
<th align="left"><span data-ttu-id="edba7-384">Tipo di connessione di rete Publishing Server/App-V 5,1 client</span><span class="sxs-lookup"><span data-stu-id="edba7-384">Network connection type publishing server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="edba7-385">Tempo di andata e ritorno nel client App-V 5,1 (in secondi)</span><span class="sxs-lookup"><span data-stu-id="edba7-385">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
<th align="left"><span data-ttu-id="edba7-386">Utilizzo della CPU nel server di pubblicazione (in%)</span><span class="sxs-lookup"><span data-stu-id="edba7-386">CPU utilization on publishing server (in %)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-387">App-V 5,1 client invia la richiesta di aggiornamento della pubblicazione &amp; riceve la risposta, ogni richiesta contenente i pacchetti di 120</span><span class="sxs-lookup"><span data-stu-id="edba7-387">App-V 5.1 client sends publishing refresh request &amp; receives response, each request containing 120 packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-388">Numero di client</span><span class="sxs-lookup"><span data-stu-id="edba7-388">Number of clients</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-389">100</span><span class="sxs-lookup"><span data-stu-id="edba7-389">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-390">1000</span><span class="sxs-lookup"><span data-stu-id="edba7-390">1000</span></span></p></li>
<li><p><span data-ttu-id="edba7-391">5000</span><span class="sxs-lookup"><span data-stu-id="edba7-391">5000</span></span></p></li>
<li><p><span data-ttu-id="edba7-392">10000</span><span class="sxs-lookup"><span data-stu-id="edba7-392">10000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-393">120</span><span class="sxs-lookup"><span data-stu-id="edba7-393">120</span></span></p></li>
<li><p><span data-ttu-id="edba7-394">120</span><span class="sxs-lookup"><span data-stu-id="edba7-394">120</span></span></p></li>
<li><p><span data-ttu-id="edba7-395">120</span><span class="sxs-lookup"><span data-stu-id="edba7-395">120</span></span></p></li>
<li><p><span data-ttu-id="edba7-396">120</span><span class="sxs-lookup"><span data-stu-id="edba7-396">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-397">Dual Core</span><span class="sxs-lookup"><span data-stu-id="edba7-397">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="edba7-398">Dual Core</span><span class="sxs-lookup"><span data-stu-id="edba7-398">Dual Core</span></span></p></li>
<li><p><span data-ttu-id="edba7-399">Quad Core</span><span class="sxs-lookup"><span data-stu-id="edba7-399">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="edba7-400">Quad Core</span><span class="sxs-lookup"><span data-stu-id="edba7-400">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-401">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-401">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-402">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-402">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-403">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-403">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-404">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-404">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-405">1</span><span class="sxs-lookup"><span data-stu-id="edba7-405">1</span></span></p></li>
<li><p><span data-ttu-id="edba7-406">2</span><span class="sxs-lookup"><span data-stu-id="edba7-406">2</span></span></p></li>
<li><p><span data-ttu-id="edba7-407">2</span><span class="sxs-lookup"><span data-stu-id="edba7-407">2</span></span></p></li>
<li><p><span data-ttu-id="edba7-408">3</span><span class="sxs-lookup"><span data-stu-id="edba7-408">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-409">100</span><span class="sxs-lookup"><span data-stu-id="edba7-409">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-410">99</span><span class="sxs-lookup"><span data-stu-id="edba7-410">99</span></span></p></li>
<li><p><span data-ttu-id="edba7-411">89</span><span class="sxs-lookup"><span data-stu-id="edba7-411">89</span></span></p></li>
<li><p><span data-ttu-id="edba7-412">77</span><span class="sxs-lookup"><span data-stu-id="edba7-412">77</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-413">Più pacchetti in ogni aggiornamento</span><span class="sxs-lookup"><span data-stu-id="edba7-413">Multiple packages in each refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-414">Numero di pacchetti</span><span class="sxs-lookup"><span data-stu-id="edba7-414">Number of packages</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-415">1000</span><span class="sxs-lookup"><span data-stu-id="edba7-415">1000</span></span></p></li>
<li><p><span data-ttu-id="edba7-416">1000</span><span class="sxs-lookup"><span data-stu-id="edba7-416">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-417">500</span><span class="sxs-lookup"><span data-stu-id="edba7-417">500</span></span></p></li>
<li><p><span data-ttu-id="edba7-418">1000</span><span class="sxs-lookup"><span data-stu-id="edba7-418">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-419">Quad Core</span><span class="sxs-lookup"><span data-stu-id="edba7-419">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="edba7-420">Quad Core</span><span class="sxs-lookup"><span data-stu-id="edba7-420">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-421">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-421">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-422">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-422">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-423">2</span><span class="sxs-lookup"><span data-stu-id="edba7-423">2</span></span></p></li>
<li><p><span data-ttu-id="edba7-424">3</span><span class="sxs-lookup"><span data-stu-id="edba7-424">3</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-425">92</span><span class="sxs-lookup"><span data-stu-id="edba7-425">92</span></span></p></li>
<li><p><span data-ttu-id="edba7-426">91</span><span class="sxs-lookup"><span data-stu-id="edba7-426">91</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-427">Rete tra il client e il server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="edba7-427">Network between client and publishing server</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-428">rete di collegamento lenta di 1,5 Mbps</span><span class="sxs-lookup"><span data-stu-id="edba7-428">1.5 Mbps Slow link network</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-429">100</span><span class="sxs-lookup"><span data-stu-id="edba7-429">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-430">500</span><span class="sxs-lookup"><span data-stu-id="edba7-430">500</span></span></p></li>
<li><p><span data-ttu-id="edba7-431">1000</span><span class="sxs-lookup"><span data-stu-id="edba7-431">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-432">120</span><span class="sxs-lookup"><span data-stu-id="edba7-432">120</span></span></p></li>
<li><p><span data-ttu-id="edba7-433">120</span><span class="sxs-lookup"><span data-stu-id="edba7-433">120</span></span></p></li>
<li><p><span data-ttu-id="edba7-434">120</span><span class="sxs-lookup"><span data-stu-id="edba7-434">120</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-435">Quad Core</span><span class="sxs-lookup"><span data-stu-id="edba7-435">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="edba7-436">Quad Core</span><span class="sxs-lookup"><span data-stu-id="edba7-436">Quad Core</span></span></p></li>
<li><p><span data-ttu-id="edba7-437">Quad Core</span><span class="sxs-lookup"><span data-stu-id="edba7-437">Quad Core</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-438">1,5 Mbps intra-Continental Network</span><span class="sxs-lookup"><span data-stu-id="edba7-438">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-439">3</span><span class="sxs-lookup"><span data-stu-id="edba7-439">3</span></span></p></li>
<li><p><span data-ttu-id="edba7-440">10 (con tasso di errore 0,2%)</span><span class="sxs-lookup"><span data-stu-id="edba7-440">10 (with 0.2% failure rate)</span></span></p></li>
<li><p><span data-ttu-id="edba7-441">17 (con tasso di errore dell'1%)</span><span class="sxs-lookup"><span data-stu-id="edba7-441">17 (with 1% failure rate)</span></span></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-1-streaming-capacity-planning-recommendations"></a> <span data-ttu-id="edba7-442">Suggerimenti per la pianificazione della capacità di streaming in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="edba7-442">App-V 5.1 Streaming Capacity Planning Recommendations</span></span>


<span data-ttu-id="edba7-443">I computer che eseguono il client App-V 5,1 esegue il flusso del pacchetto dell'applicazione virtuale dal server di streaming.</span><span class="sxs-lookup"><span data-stu-id="edba7-443">Computers running the App-V 5.1 client stream the virtual application package from the streaming server.</span></span> <span data-ttu-id="edba7-444">Il tempo di risposta di andata e ritorno viene misurato nel computer che gestisce il client App-V 5,1 ed è il tempo impiegato per trasmettere l'intero pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edba7-444">Round trip response time is measured on the computer running the App-V 5.1 client, and is the time taken to stream the entire package.</span></span>

<span data-ttu-id="edba7-445">**Importante**  L'elenco seguente identifica i fattori principali da tenere in considerazione durante la configurazione del server di streaming App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="edba7-445">**Important** The following list identifies the main factors to consider when setting up the App-V 5.1 streaming server:</span></span>

-   <span data-ttu-id="edba7-446">Il numero di client che esegue lo streaming di pacchetti di applicazioni contemporaneamente da un singolo server di flusso.</span><span class="sxs-lookup"><span data-stu-id="edba7-446">The number of clients streaming application packages simultaneously from a single streaming server.</span></span>

-   <span data-ttu-id="edba7-447">Dimensioni del pacchetto in streaming.</span><span class="sxs-lookup"><span data-stu-id="edba7-447">The size of the package being streamed.</span></span>

-   <span data-ttu-id="edba7-448">Larghezza di banda di rete disponibile nell'ambiente tra il client e il server di streaming.</span><span class="sxs-lookup"><span data-stu-id="edba7-448">The available network bandwidth in your environment between the client and the streaming server.</span></span>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-449">Scenario</span><span class="sxs-lookup"><span data-stu-id="edba7-449">Scenario</span></span></th>
<th align="left"><span data-ttu-id="edba7-450">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="edba7-450">Summary</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-451">Più client App-V 5,1 lo streaming di applicazioni da un singolo server di flusso simultaneo.</span><span class="sxs-lookup"><span data-stu-id="edba7-451">Multiple App-V 5.1 clients stream applications from a single streaming server simultaneously.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-452">Se il numero di client in streaming simultaneamente dallo stesso server aumenta, esiste una relazione lineare con il tempo di download/flusso del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edba7-452">If the number of clients simultaneously streaming from the same server increases, there is a linear relationship with the package download/streaming time.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-453">Dimensioni del pacchetto in streaming.</span><span class="sxs-lookup"><span data-stu-id="edba7-453">Size of the package being streamed.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-454">Le dimensioni del pacchetto hanno un impatto significativo sul tempo di streaming/download solo per i pacchetti più grandi con una dimensione di ~ 1GB.</span><span class="sxs-lookup"><span data-stu-id="edba7-454">The package size has a significant impact on the streaming/download time only for larger packages with a size ~ 1GB.</span></span> <span data-ttu-id="edba7-455">Per le dimensioni del pacchetto comprese tra 3 MB e 100 MB, il tempo di flusso varia da 20 secondi a 100 secondi, con 100 client simultanei.</span><span class="sxs-lookup"><span data-stu-id="edba7-455">For package sizes ranging from 3 MB to 100 MB, the streaming time ranges from 20 seconds to 100 seconds, with 100 simultaneous clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-456">Rete tra il client App-V 5,1 e il server di streaming.</span><span class="sxs-lookup"><span data-stu-id="edba7-456">Network between the App-V 5.1 client and the streaming server.</span></span></p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-457">In una rete lenta (larghezza di banda di 1,5 Mbps) è aumentato il 70-80% del tempo di risposta rispetto alla LAN (fino a 100 utenti).</span><span class="sxs-lookup"><span data-stu-id="edba7-457">Across a slow network (1.5 Mbps bandwidth), there is a 70-80% increase in response time compared to LAN (up to 100 users).</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="edba7-458">Nella tabella seguente vengono visualizzati i valori di esempio per ogni fattore nell'elenco precedente:</span><span class="sxs-lookup"><span data-stu-id="edba7-458">The following table displays sample values for each of the factors in the previous list:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="edba7-459">Scenario</span><span class="sxs-lookup"><span data-stu-id="edba7-459">Scenario</span></span></th>
<th align="left"><span data-ttu-id="edba7-460">Variante</span><span class="sxs-lookup"><span data-stu-id="edba7-460">Variation</span></span></th>
<th align="left"><span data-ttu-id="edba7-461">Numero di client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="edba7-461">Number of App-V 5.1 clients</span></span></th>
<th align="left"><span data-ttu-id="edba7-462">Dimensioni di ogni pacchetto</span><span class="sxs-lookup"><span data-stu-id="edba7-462">Size of each package</span></span></th>
<th align="left"><span data-ttu-id="edba7-463">Tipo di connessione di rete streaming server/App-V 5,1 client</span><span class="sxs-lookup"><span data-stu-id="edba7-463">Network connection type streaming server / App-V 5.1 client</span></span></th>
<th align="left"><span data-ttu-id="edba7-464">Tempo di andata e ritorno nel client App-V 5,1 (in secondi)</span><span class="sxs-lookup"><span data-stu-id="edba7-464">Round trip time on the App-V 5.1 client (in seconds)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-465">Più client App-V 5,1 in streaming di pacchetti di applicazioni virtuali da un server di streaming.</span><span class="sxs-lookup"><span data-stu-id="edba7-465">Multiple App-V 5.1 clients streaming virtual application packages from a streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-466">Numero di client.</span><span class="sxs-lookup"><span data-stu-id="edba7-466">Number of clients.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-467">100</span><span class="sxs-lookup"><span data-stu-id="edba7-467">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-468">200</span><span class="sxs-lookup"><span data-stu-id="edba7-468">200</span></span></p></li>
<li><p><span data-ttu-id="edba7-469">1000</span><span class="sxs-lookup"><span data-stu-id="edba7-469">1000</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-470">100</span><span class="sxs-lookup"><span data-stu-id="edba7-470">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-471">200</span><span class="sxs-lookup"><span data-stu-id="edba7-471">200</span></span></p></li>
<li><p><span data-ttu-id="edba7-472">1000</span><span class="sxs-lookup"><span data-stu-id="edba7-472">1000</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-473">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-473">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="edba7-474">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-474">3.5 MB</span></span></p></li>
<li><p><span data-ttu-id="edba7-475">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-475">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-476">5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-476">5 MB</span></span></p></li>
<li><p><span data-ttu-id="edba7-477">5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-477">5 MB</span></span></p></li>
<li><p><span data-ttu-id="edba7-478">5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-478">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-479">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-479">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-480">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-480">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-481">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-481">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-482">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-482">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-483">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-483">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-484">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-484">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-485">29</span><span class="sxs-lookup"><span data-stu-id="edba7-485">29</span></span></p></li>
<li><p><span data-ttu-id="edba7-486">39</span><span class="sxs-lookup"><span data-stu-id="edba7-486">39</span></span></p></li>
<li><p><span data-ttu-id="edba7-487">391</span><span class="sxs-lookup"><span data-stu-id="edba7-487">391</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-488">35</span><span class="sxs-lookup"><span data-stu-id="edba7-488">35</span></span></p></li>
<li><p><span data-ttu-id="edba7-489">68</span><span class="sxs-lookup"><span data-stu-id="edba7-489">68</span></span></p></li>
<li><p><span data-ttu-id="edba7-490">461</span><span class="sxs-lookup"><span data-stu-id="edba7-490">461</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="edba7-491">Dimensioni di ogni pacchetto in streaming.</span><span class="sxs-lookup"><span data-stu-id="edba7-491">Size of each package being streamed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-492">Dimensioni di ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="edba7-492">Size of each package.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-493">100</span><span class="sxs-lookup"><span data-stu-id="edba7-493">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-494">200</span><span class="sxs-lookup"><span data-stu-id="edba7-494">200</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-495">100</span><span class="sxs-lookup"><span data-stu-id="edba7-495">100</span></span></p></li>
<li><p><span data-ttu-id="edba7-496">200</span><span class="sxs-lookup"><span data-stu-id="edba7-496">200</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-497">21 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-497">21 MB</span></span></p></li>
<li><p><span data-ttu-id="edba7-498">21 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-498">21 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-499">109</span><span class="sxs-lookup"><span data-stu-id="edba7-499">109</span></span></p></li>
<li><p><span data-ttu-id="edba7-500">109</span><span class="sxs-lookup"><span data-stu-id="edba7-500">109</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-501">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-501">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-502">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-502">LAN</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-503">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-503">LAN</span></span></p></li>
<li><p><span data-ttu-id="edba7-504">LAN</span><span class="sxs-lookup"><span data-stu-id="edba7-504">LAN</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="edba7-505">33</span><span class="sxs-lookup"><span data-stu-id="edba7-505">33</span></span></p>
<p><span data-ttu-id="edba7-506">83</span><span class="sxs-lookup"><span data-stu-id="edba7-506">83</span></span></p>
<p></p>
<p><span data-ttu-id="edba7-507">100</span><span class="sxs-lookup"><span data-stu-id="edba7-507">100</span></span></p>
<p><span data-ttu-id="edba7-508">160</span><span class="sxs-lookup"><span data-stu-id="edba7-508">160</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="edba7-509">Connessione di rete tra client e App-V 5,1 streaming server.</span><span class="sxs-lookup"><span data-stu-id="edba7-509">Network connection between client and App-V 5.1 streaming server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="edba7-510">rete di collegamento lenta di 1,5 Mbps.</span><span class="sxs-lookup"><span data-stu-id="edba7-510">1.5 Mbps Slow link network.</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-511">100</span><span class="sxs-lookup"><span data-stu-id="edba7-511">100</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-512">100</span><span class="sxs-lookup"><span data-stu-id="edba7-512">100</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-513">3,5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-513">3.5 MB</span></span></p></li>
<li><p></p></li>
<li><p><span data-ttu-id="edba7-514">5 MB</span><span class="sxs-lookup"><span data-stu-id="edba7-514">5 MB</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p><span data-ttu-id="edba7-515">1,5 Mbps intra-Continental Network</span><span class="sxs-lookup"><span data-stu-id="edba7-515">1.5 Mbps Intra-Continental Network</span></span></p></li>
</ul></td>
<td align="left"><p></p>
<p><span data-ttu-id="edba7-516">102</span><span class="sxs-lookup"><span data-stu-id="edba7-516">102</span></span></p>
<p></p>
<p><span data-ttu-id="edba7-517">121</span><span class="sxs-lookup"><span data-stu-id="edba7-517">121</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="edba7-518">Ogni app-V 5,1 streaming server dovrebbe essere in grado di gestire almeno 200 client simultaneamente in streaming applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="edba7-518">Each App-V 5.1 streaming server should be able to handle a minimum of 200 clients concurrently streaming virtualized applications.</span></span>

<span data-ttu-id="edba7-519">**Nota**  Il tempo effettivo che verrà impiegato per lo streaming viene determinato principalmente dal numero di client in streaming simultaneamente, dal numero di pacchetti, dalle dimensioni del pacchetto, dall'attività di rete del server e dalle condizioni di rete.</span><span class="sxs-lookup"><span data-stu-id="edba7-519">**Note** The actual time to it will take to stream is determined primarily by the number of clients streaming simultaneously, number of packages, package size, the server’s network activity, and network conditions.</span></span>

 

<span data-ttu-id="edba7-520">Ad esempio, un utente medio può trasmettere un pacchetto di 100 MB in meno di 2 minuti, quando i client simultanei di 100 sono in streaming dal server.</span><span class="sxs-lookup"><span data-stu-id="edba7-520">For example, an average user can stream a 100 MB package in less than 2 minutes, when 100 simultaneous clients are streaming from the server.</span></span> <span data-ttu-id="edba7-521">Tuttavia, un pacchetto di dimensioni da 1 GB può richiedere fino a 30 minuti.</span><span class="sxs-lookup"><span data-stu-id="edba7-521">However, a package of size 1 GB could take up to 30 minutes.</span></span> <span data-ttu-id="edba7-522">Nella maggior parte dei casi reali la richiesta di streaming non viene distribuita in modo uniforme, sarà necessario comprendere i requisiti di picco di flusso approssimativo presenti nell'ambiente per ridimensionare correttamente il numero di server di flusso necessari.</span><span class="sxs-lookup"><span data-stu-id="edba7-522">In most real world environments streaming demand is not uniformly distributed, you will need to understand the approximate peak streaming requirements present in your environment in order to properly size the number of required streaming servers.</span></span>

<span data-ttu-id="edba7-523">Il numero di client che un server di streaming può supportare può essere notevolmente aumentato e i requisiti di flusso di picco sono ridotti se si prememorizzano le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="edba7-523">The number of clients a streaming server can support can be significantly increased and the peak streaming requirements reduced if you pre-cache your applications.</span></span> <span data-ttu-id="edba7-524">Puoi anche aumentare il numero di client che un server di streaming può supportare usando pacchetti di distribuzione su richiesta e flussi ottimizzati.</span><span class="sxs-lookup"><span data-stu-id="edba7-524">You can also increase the number of clients a streaming server can support by using on-demand streaming delivery and stream optimized packages.</span></span>

## <span data-ttu-id="edba7-525">Combinazione dei ruoli del server App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="edba7-525">Combining App-V 5.1 Server Roles</span></span>


<span data-ttu-id="edba7-526">Riduzione dei requisiti di scalabilità e tolleranza d'errore, il numero minimo di server necessari per una posizione con connettività ad Active Directory è uno.</span><span class="sxs-lookup"><span data-stu-id="edba7-526">Discounting scaling and fault-tolerance requirements, the minimum number of servers needed for a location with connectivity to Active Directory is one.</span></span> <span data-ttu-id="edba7-527">Questo server ospiterà il server di gestione, il servizio server di gestione e i ruoli di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="edba7-527">This server will host the management server, management server service, and Microsoft SQL Server roles.</span></span> <span data-ttu-id="edba7-528">I ruoli del server possono quindi essere organizzati in qualsiasi combinazione desiderata, perché non sono in conflitto tra loro.</span><span class="sxs-lookup"><span data-stu-id="edba7-528">Server roles, therefore, can be arranged in any desired combination since they do not conflict with one another.</span></span>

<span data-ttu-id="edba7-529">Ignorando i requisiti di ridimensionamento, il numero minimo di server necessari per l'implementazione a tolleranza d'errore è quattro.</span><span class="sxs-lookup"><span data-stu-id="edba7-529">Ignoring scaling requirements, the minimum number of servers necessary to provide a fault-tolerant implementation is four.</span></span> <span data-ttu-id="edba7-530">Il server di gestione e il supporto dei ruoli di Microsoft SQL Server vengono inseriti nelle configurazioni a tolleranza d'errore.</span><span class="sxs-lookup"><span data-stu-id="edba7-530">The management server, and Microsoft SQL Server roles support being placed in fault-tolerant configurations.</span></span> <span data-ttu-id="edba7-531">Il servizio server di gestione può essere combinato con uno qualsiasi dei ruoli, ma rimane un singolo punto di errore.</span><span class="sxs-lookup"><span data-stu-id="edba7-531">The management server service can be combined with any of the roles, but remains a single point of failure.</span></span>

<span data-ttu-id="edba7-532">Anche se sono disponibili diverse strategie e tecnologie di tolleranza d'errore, non tutte sono applicabili a un servizio specifico.</span><span class="sxs-lookup"><span data-stu-id="edba7-532">Although there are a number of fault-tolerance strategies and technologies available, not all are applicable to a given service.</span></span> <span data-ttu-id="edba7-533">Inoltre, se vengono combinati i ruoli di App-V 5,1, alcune opzioni di tolleranza di errore potrebbero non essere più applicabili a causa di incompatibilità.</span><span class="sxs-lookup"><span data-stu-id="edba7-533">Additionally, if App-V 5.1 roles are combined, certain fault-tolerance options may no longer apply due to incompatibilities.</span></span>






## <span data-ttu-id="edba7-534">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="edba7-534">Related topics</span></span>


[<span data-ttu-id="edba7-535">Configurazioni supportate di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="edba7-535">App-V 5.1 Supported Configurations</span></span>](app-v-51-supported-configurations.md)

[<span data-ttu-id="edba7-536">Pianificazione della disponibilità elevata con App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="edba7-536">Planning for High Availability with App-V 5.1</span></span>](planning-for-high-availability-with-app-v-51.md)

[<span data-ttu-id="edba7-537">Pianificazione della distribuzione di App-V</span><span class="sxs-lookup"><span data-stu-id="edba7-537">Planning to Deploy App-V</span></span>](planning-to-deploy-app-v51.md)

 

 





