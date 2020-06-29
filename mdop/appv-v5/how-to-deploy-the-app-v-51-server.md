---
title: Come distribuire il server App-V 5.1
description: Come distribuire il server App-V 5.1
author: dansimp
ms.assetid: 4729beda-b98f-481b-ae74-ad71c59b1d69
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4a367be7db4cea1835124657dbdfa3375474228e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805499"
---
# <span data-ttu-id="4f03c-103">Come distribuire il server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4f03c-103">How to Deploy the App-V 5.1 Server</span></span>


<span data-ttu-id="4f03c-104">Usare la procedura seguente per installare il server Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="4f03c-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 server.</span></span> <span data-ttu-id="4f03c-105">Per informazioni sulla distribuzione del server App-V 5,1, vedere [informazioni su App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).</span><span class="sxs-lookup"><span data-stu-id="4f03c-105">For information about deploying the App-V 5.1 Server, see [About App-V 5.1](about-app-v-51.md#bkmk-migrate-to-51).</span></span>

**<span data-ttu-id="4f03c-106">Prima di iniziare:</span><span class="sxs-lookup"><span data-stu-id="4f03c-106">Before you start:</span></span>**

-   <span data-ttu-id="4f03c-107">Verificare di aver installato il software prerequisito.</span><span class="sxs-lookup"><span data-stu-id="4f03c-107">Ensure that you’ve installed prerequisite software.</span></span> <span data-ttu-id="4f03c-108">Vedere [prerequisiti di App-V 5,1](app-v-51-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="4f03c-108">See [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

-   <span data-ttu-id="4f03c-109">Esaminare la sezione server delle [considerazioni sulla sicurezza di App-V 5,1](app-v-51-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="4f03c-109">Review the server section of [App-V 5.1 Security Considerations](app-v-51-security-considerations.md).</span></span>

-   <span data-ttu-id="4f03c-110">Specificare una porta in cui verranno ospitati tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="4f03c-110">Specify a port where each component will be hosted.</span></span>

-   <span data-ttu-id="4f03c-111">Aggiungere regole del firewall per consentire alle richieste in arrivo di accedere alle porte specificate.</span><span class="sxs-lookup"><span data-stu-id="4f03c-111">Add firewall rules to allow incoming requests to access the specified ports.</span></span>

-   <span data-ttu-id="4f03c-112">Se si usano script SQL, invece di Windows Installer, per configurare il database di gestione o il database di report, è necessario eseguire gli script SQL prima di installare il server di gestione o il server di report.</span><span class="sxs-lookup"><span data-stu-id="4f03c-112">If you use SQL scripts, instead of the Windows Installer, to set up the Management database or Reporting database, you must run the SQL scripts before installing the Management Server or Reporting Server.</span></span> <span data-ttu-id="4f03c-113">Informazioni [su come distribuire i database di App-V usando gli script SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span><span class="sxs-lookup"><span data-stu-id="4f03c-113">See [How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).</span></span>

**<span data-ttu-id="4f03c-114">Per installare il server App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="4f03c-114">To install the App-V 5.1 server</span></span>**

1. <span data-ttu-id="4f03c-115">Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="4f03c-115">Copy the App-V 5.1 server installation files to the computer on which you want to install it.</span></span>

2. <span data-ttu-id="4f03c-116">Avviare l'installazione del server App-V 5,1 facendo clic con il pulsante destro del mouse e eseguendo **appv\_server\_setup.exe** come amministratore e quindi fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="4f03c-116">Start the App-V 5.1 server installation by right-clicking and running **appv\_server\_setup.exe** as an administrator, and then click **Install**.</span></span>

3. <span data-ttu-id="4f03c-117">Rivedere e accettare le condizioni di licenza e scegliere se abilitare gli aggiornamenti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4f03c-117">Review and accept the license terms, and choose whether to enable Microsoft updates.</span></span>

4. <span data-ttu-id="4f03c-118">Nella pagina **Selezione funzionalità** selezionare tutti i componenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="4f03c-118">On the **Feature Selection** page, select all of the following components.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="4f03c-119">Componente</span><span class="sxs-lookup"><span data-stu-id="4f03c-119">Component</span></span></th>
   <th align="left"><span data-ttu-id="4f03c-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f03c-120">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="4f03c-121">Server di gestione</span><span class="sxs-lookup"><span data-stu-id="4f03c-121">Management server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-122">Offre funzionalità di gestione complessive per l'infrastruttura App-V.</span><span class="sxs-lookup"><span data-stu-id="4f03c-122">Provides overall management functionality for the App-V infrastructure.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="4f03c-123">Database di gestione</span><span class="sxs-lookup"><span data-stu-id="4f03c-123">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-124">Facilita le predistribuzioni di database per la gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="4f03c-124">Facilitates database predeployments for App-V management.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="4f03c-125">Server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="4f03c-125">Publishing server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-126">Offre funzionalità di hosting e flusso per le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="4f03c-126">Provides hosting and streaming functionality for virtual applications.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="4f03c-127">Server di report</span><span class="sxs-lookup"><span data-stu-id="4f03c-127">Reporting server</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-128">Fornisce l'App-V 5,1 Reporting Services.</span><span class="sxs-lookup"><span data-stu-id="4f03c-128">Provides App-V 5.1 reporting services.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="4f03c-129">Database di report</span><span class="sxs-lookup"><span data-stu-id="4f03c-129">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-130">Facilita le predistribuzioni di database per i report di App-V.</span><span class="sxs-lookup"><span data-stu-id="4f03c-130">Facilitates database predeployments for App-V reporting.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

5. <span data-ttu-id="4f03c-131">Nella pagina **posizione di installazione** accettare il percorso predefinito in cui verranno installati i componenti selezionati oppure modificare la posizione digitando un nuovo percorso nella riga del **percorso di installazione** .</span><span class="sxs-lookup"><span data-stu-id="4f03c-131">On the **Installation Location** page, accept the default location where the selected components will be installed, or change the location by typing a new path on the **Installation Location** line.</span></span>

6. <span data-ttu-id="4f03c-132">Nella pagina iniziale **Crea nuovo database di gestione** configurare l' **istanza di Microsoft SQL Server** e il database del server di **gestione** selezionando l'opzione appropriata di seguito.</span><span class="sxs-lookup"><span data-stu-id="4f03c-132">On the initial **Create New Management Database** page, configure the **Microsoft SQL Server instance** and **Management Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="4f03c-133">Metodo</span><span class="sxs-lookup"><span data-stu-id="4f03c-133">Method</span></span></th>
   <th align="left"><span data-ttu-id="4f03c-134">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="4f03c-134">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="4f03c-135">Si usa un'istanza di Microsoft SQL Server personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4f03c-135">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-136">Selezionare <strong> Usa l'istanza personalizzata </strong> e digitare il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="4f03c-136">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="4f03c-137">Usare il formato <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f03c-137">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="4f03c-138">Il percorso di installazione presupposto è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="4f03c-138">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="4f03c-139">Non supportato: nome di un server che usa <strong> l' </strong> &lt; istanza Strong di format servername &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f03c-139">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="4f03c-140">Si usa un nome di database personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4f03c-140">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-141">Selezionare <strong> configurazione personalizzata </strong> e digitare il nome del database.</span><span class="sxs-lookup"><span data-stu-id="4f03c-141">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="4f03c-142">Il nome del database deve essere univoco oppure l'installazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4f03c-142">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="4f03c-143">Nella pagina **Configura** accettare il valore predefinito **usare questo computer locale**.</span><span class="sxs-lookup"><span data-stu-id="4f03c-143">On the **Configure** page, accept the default value **Use this local computer**.</span></span>

   **<span data-ttu-id="4f03c-144">Nota</span><span class="sxs-lookup"><span data-stu-id="4f03c-144">Note</span></span>**  
   <span data-ttu-id="4f03c-145">Se si sta installando il server di gestione e il database di gestione affiancati, alcune opzioni in questa pagina non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="4f03c-145">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="4f03c-146">In questo caso, le opzioni appropriate sono selezionate per impostazione predefinita e non possono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="4f03c-146">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

8. <span data-ttu-id="4f03c-147">Nella pagina iniziale **Crea nuovo database di report** configurare l' **istanza di Microsoft SQL Server** e il database del server di **Reporting** selezionando l'opzione appropriata di seguito.</span><span class="sxs-lookup"><span data-stu-id="4f03c-147">On the initial **Create New Reporting Database** page, configure the **Microsoft SQL Server instance** and **Reporting Server database** by selecting the appropriate option below.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="4f03c-148">Metodo</span><span class="sxs-lookup"><span data-stu-id="4f03c-148">Method</span></span></th>
   <th align="left"><span data-ttu-id="4f03c-149">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="4f03c-149">What you need to do</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="4f03c-150">Si usa un'istanza di Microsoft SQL Server personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4f03c-150">You are using a custom Microsoft SQL Server instance.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-151">Selezionare <strong> Usa l'istanza personalizzata </strong> e digitare il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="4f03c-151">Select <strong>Use the custom instance</strong>, and type the name of the instance.</span></span></p>
   <p><span data-ttu-id="4f03c-152">Usare il formato <strong> InstanceName </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f03c-152">Use the format <strong>INSTANCENAME</strong>.</span></span> <span data-ttu-id="4f03c-153">Il percorso di installazione presupposto è il computer locale.</span><span class="sxs-lookup"><span data-stu-id="4f03c-153">The assumed installation location is the local computer.</span></span></p>
   <p><span data-ttu-id="4f03c-154">Non supportato: nome di un server che usa <strong> l' </strong> &lt; istanza Strong di format servername &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="4f03c-154">Not supported: A server name using the format <strong>ServerName</strong>&lt;strong&gt;INSTANCE</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="4f03c-155">Si usa un nome di database personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4f03c-155">You are using a custom database name.</span></span></p></td>
   <td align="left"><p><span data-ttu-id="4f03c-156">Selezionare <strong> configurazione personalizzata </strong> e digitare il nome del database.</span><span class="sxs-lookup"><span data-stu-id="4f03c-156">Select <strong>Custom configuration</strong> and type the database name.</span></span></p>
   <p><span data-ttu-id="4f03c-157">Il nome del database deve essere univoco oppure l'installazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4f03c-157">The database name must be unique, or the installation will fail.</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

9. <span data-ttu-id="4f03c-158">Nella pagina **Configura** accettare il valore predefinito: **usare questo computer locale**.</span><span class="sxs-lookup"><span data-stu-id="4f03c-158">On the **Configure** page, accept the default value: **Use this local computer**.</span></span>

   **<span data-ttu-id="4f03c-159">Nota</span><span class="sxs-lookup"><span data-stu-id="4f03c-159">Note</span></span>**  
   <span data-ttu-id="4f03c-160">Se si sta installando il server di gestione e il database di gestione affiancati, alcune opzioni in questa pagina non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="4f03c-160">If you are installing the Management server and Management database side by side, some options on this page are not available.</span></span> <span data-ttu-id="4f03c-161">In questo caso, le opzioni appropriate sono selezionate per impostazione predefinita e non possono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="4f03c-161">In this case, the appropriate options are selected by default and cannot be changed.</span></span>

     

10. <span data-ttu-id="4f03c-162">Nella pagina **Configura** (Management Server Configuration) specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="4f03c-162">On the **Configure** (Management Server Configuration) page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="4f03c-163">Elemento da configurare</span><span class="sxs-lookup"><span data-stu-id="4f03c-163">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="4f03c-164">Descrizione ed esempi</span><span class="sxs-lookup"><span data-stu-id="4f03c-164">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4f03c-165">Digitare il gruppo di annunci con autorizzazioni sufficienti per gestire l'ambiente App-V.</span><span class="sxs-lookup"><span data-stu-id="4f03c-165">Type the AD group with sufficient permissions to manage the App-V environment.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-166">Esempio: MyDomain\MyUser</span><span class="sxs-lookup"><span data-stu-id="4f03c-166">Example: MyDomain\MyUser</span></span></p>
    <p><span data-ttu-id="4f03c-167">Dopo l'installazione, è possibile aggiungere altri utenti o gruppi tramite la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="4f03c-167">After installation, you can add additional users or groups by using the Management console.</span></span> <span data-ttu-id="4f03c-168">Tuttavia, i gruppi di sicurezza globali e i gruppi di distribuzione di servizi di dominio Active Directory (AD DS) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="4f03c-168">However, global security groups and Active Directory Domain Services (AD DS) distribution groups are not supported.</span></span> <span data-ttu-id="4f03c-169"><strong> </strong> Per eseguire questa azione è necessario usare il dominio locale o <strong> </strong> i gruppi universali.</span><span class="sxs-lookup"><span data-stu-id="4f03c-169">You must use <strong>Domain local</strong> or <strong>Universal</strong> groups are required to perform this action.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="4f03c-170">Nome sito Web </strong> : specificare il nome personalizzato che verrà usato per eseguire il servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="4f03c-170">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-171">Se non si dispone di un nome personalizzato, non apportare alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="4f03c-171">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="4f03c-172">Binding della porta </strong> : specificare un numero di porta univoco che verrà usato da App-V.</span><span class="sxs-lookup"><span data-stu-id="4f03c-172">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-173">Esempio: <strong> 12345</span><span class="sxs-lookup"><span data-stu-id="4f03c-173">Example: <strong>12345</span></span></strong></p>
    <p><span data-ttu-id="4f03c-174">Assicurarsi che la porta specificata non venga usata da un altro sito Web.</span><span class="sxs-lookup"><span data-stu-id="4f03c-174">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

11. <span data-ttu-id="4f03c-175">Nella pagina **Configura** **Configurazione server di pubblicazione** specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="4f03c-175">On the **Configure** **Publishing Server Configuration** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="4f03c-176">Elemento da configurare</span><span class="sxs-lookup"><span data-stu-id="4f03c-176">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="4f03c-177">Descrizione ed esempi</span><span class="sxs-lookup"><span data-stu-id="4f03c-177">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="4f03c-178">Specificare l'URL per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="4f03c-178">Specify the URL for the management service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-179">Esempio<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span><span class="sxs-lookup"><span data-stu-id="4f03c-179">Example: <a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</span></span></a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="4f03c-180">Nome sito Web </strong> : specificare il nome personalizzato che verrà usato per eseguire il servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="4f03c-180">Website name</strong>: Specify the custom name that will be used to run the publishing service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-181">Se non si dispone di un nome personalizzato, non apportare alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="4f03c-181">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="4f03c-182">Binding della porta </strong> : specificare un numero di porta univoco che verrà usato da App-V.</span><span class="sxs-lookup"><span data-stu-id="4f03c-182">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-183">Esempio: 54321</span><span class="sxs-lookup"><span data-stu-id="4f03c-183">Example: 54321</span></span></p>
    <p><span data-ttu-id="4f03c-184">Assicurarsi che la porta specificata non venga usata da un altro sito Web.</span><span class="sxs-lookup"><span data-stu-id="4f03c-184">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

12. <span data-ttu-id="4f03c-185">Nella pagina **Reporting Server** specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="4f03c-185">On the **Reporting Server** page, specify the following:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="4f03c-186">Elemento da configurare</span><span class="sxs-lookup"><span data-stu-id="4f03c-186">Item to configure</span></span></th>
    <th align="left"><span data-ttu-id="4f03c-187">Descrizione ed esempi</span><span class="sxs-lookup"><span data-stu-id="4f03c-187">Description and examples</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="4f03c-188">Nome sito Web </strong> : specificare il nome personalizzato che verrà usato per eseguire il servizio di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="4f03c-188">Website name</strong>: Specify the custom name that will be used to run the Reporting Service.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-189">Se non si dispone di un nome personalizzato, non apportare alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="4f03c-189">If you do not have a custom name, do not make any changes.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="4f03c-190">Binding della porta </strong> : specificare un numero di porta univoco che verrà usato da App-V.</span><span class="sxs-lookup"><span data-stu-id="4f03c-190">Port binding</strong>: Specify a unique port number that will be used by App-V.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="4f03c-191">Esempio: 55555</span><span class="sxs-lookup"><span data-stu-id="4f03c-191">Example: 55555</span></span></p>
    <p><span data-ttu-id="4f03c-192">Assicurarsi che la porta specificata non venga usata da un altro sito Web.</span><span class="sxs-lookup"><span data-stu-id="4f03c-192">Ensure that the port specified is not being used by another website.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

13. <span data-ttu-id="4f03c-193">Per avviare l'installazione, fare clic su **Installa** nella pagina **pronto** e quindi fare clic su **Chiudi** nella pagina **finito** .</span><span class="sxs-lookup"><span data-stu-id="4f03c-193">To start the installation, click **Install** on the **Ready** page, and then click **Close** on the **Finished** page.</span></span>

14. <span data-ttu-id="4f03c-194">Per verificare che la configurazione sia stata completata correttamente, aprire un Web browser e digitare l'URL seguente:</span><span class="sxs-lookup"><span data-stu-id="4f03c-194">To verify that the setup completed successfully, open a web browser, and type the following URL:</span></span>

    <span data-ttu-id="4f03c-195">**http:// &lt; Nome computer del server di gestione &gt; : &lt; numero di porta del servizio di gestione &gt; /Console.html**.</span><span class="sxs-lookup"><span data-stu-id="4f03c-195">**http://&lt;Management server machine name&gt;:&lt;Management service port number&gt;/Console.html**.</span></span>

    <span data-ttu-id="4f03c-196">Esempio: **http://localhost:12345/console.html** .</span><span class="sxs-lookup"><span data-stu-id="4f03c-196">Example: **http://localhost:12345/console.html**.</span></span> <span data-ttu-id="4f03c-197">Se l'installazione è riuscita, viene visualizzata la console di gestione di App-V senza errori.</span><span class="sxs-lookup"><span data-stu-id="4f03c-197">If the installation succeeded, the App-V Management console is displayed with no errors.</span></span>

    <span data-ttu-id="4f03c-198">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="4f03c-198">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="4f03c-199">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="4f03c-199">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="4f03c-200">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="4f03c-200">Got an App-V issue?</span></span>** <span data-ttu-id="4f03c-201">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="4f03c-201">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="4f03c-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f03c-202">Related topics</span></span>


[<span data-ttu-id="4f03c-203">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="4f03c-203">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="4f03c-204">Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report</span><span class="sxs-lookup"><span data-stu-id="4f03c-204">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[<span data-ttu-id="4f03c-205">Come installare il server di pubblicazione in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="4f03c-205">How to Install the Publishing Server on a Remote Computer</span></span>](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[<span data-ttu-id="4f03c-206">Come distribuire il server App-V 5.1 con uno script</span><span class="sxs-lookup"><span data-stu-id="4f03c-206">How to Deploy the App-V 5.1 Server Using a Script</span></span>](how-to-deploy-the-app-v-51-server-using-a-script.md)

 

 





