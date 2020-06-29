---
title: Come configurare le azioni script
description: Come configurare le azioni script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804191"
---
# <span data-ttu-id="86695-103">Come configurare le azioni script</span><span class="sxs-lookup"><span data-stu-id="86695-103">How to Set Up Script Actions</span></span>


<span data-ttu-id="86695-104">L'Editor azioni script consente all'amministratore di creare azioni da eseguire durante la configurazione dell'area di lavoro MED-V, nonché di definire l'ordine in cui vengono eseguite.</span><span class="sxs-lookup"><span data-stu-id="86695-104">The script actions editor allows the administrator to create actions to be performed during MED-V workspace setup, as well as to define the order in which they are performed.</span></span>

<span data-ttu-id="86695-105">Di seguito è riportato un elenco di azioni che possono essere aggiunte allo script di configurazione del dominio:</span><span class="sxs-lookup"><span data-stu-id="86695-105">The following is a list of actions that can be added to the domain setup script:</span></span>

-   <span data-ttu-id="86695-106">**Riavvia Windows**: riavvia Windows.</span><span class="sxs-lookup"><span data-stu-id="86695-106">**Restart Windows**—Restart Windows.</span></span>

-   <span data-ttu-id="86695-107">**Join Domain**: se si partecipa a un dominio, includere questa azione e configurare il nome utente, la password, il nome di dominio completo, il nome di dominio NetBIOS e l'unità organizzativa (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="86695-107">**Join Domain**—If joining a domain, include this action and configure the user name, password, fully qualified domain name, NetBIOS domain name, and organization unit (optional).</span></span>

-   <span data-ttu-id="86695-108">**Verificare la connettività**: configurare un server a cui connettersi e verificare che l'area di lavoro MED-V sia in grado di connettersi a una risorsa di rete, ad esempio il server di dominio.</span><span class="sxs-lookup"><span data-stu-id="86695-108">**Check Connectivity**—Configure a server to connect to and verify that the MED-V workspace can connect to a network resource (such as the domain server).</span></span>

-   <span data-ttu-id="86695-109">**Riga di comando**: configurare uno script nell'area di lavoro MED-V e immettere una riga di comando che includa il percorso dello script e gli argomenti dello script.</span><span class="sxs-lookup"><span data-stu-id="86695-109">**Command Line**—Configure a script in the MED-V workspace, and enter a command line that includes the path of the script and the script arguments.</span></span>

-   <span data-ttu-id="86695-110">**Rinomina computer**: rinominare il computer della macchina virtuale in base alle impostazioni definite.</span><span class="sxs-lookup"><span data-stu-id="86695-110">**Rename Computer**—Rename the virtual machine computer based on the defined settings.</span></span>

-   <span data-ttu-id="86695-111">**Disabilitare l'accesso automatico**: disabilitare l'accesso automatico di Windows.</span><span class="sxs-lookup"><span data-stu-id="86695-111">**Disable Auto-Logon**—Disable Windows Auto-Logon.</span></span> <span data-ttu-id="86695-112">Questa azione deve essere aggiunta alla fine degli script che aggiungono il computer al dominio.</span><span class="sxs-lookup"><span data-stu-id="86695-112">This action should be added at the end of scripts that add the computer to the domain.</span></span>

## <a href="" id="how-to-set-up-script-actions-"></a><span data-ttu-id="86695-113">Come configurare le azioni script</span><span class="sxs-lookup"><span data-stu-id="86695-113">How to Set Up Script Actions</span></span>


**<span data-ttu-id="86695-114">Per configurare le azioni di script</span><span class="sxs-lookup"><span data-stu-id="86695-114">To set up script actions</span></span>**

1.  <span data-ttu-id="86695-115">Nella scheda **configurazione VM** fare clic su **Editor script**.</span><span class="sxs-lookup"><span data-stu-id="86695-115">On the **VM Setup** tab, click **Script Editor**.</span></span>

2.  <span data-ttu-id="86695-116">Nella finestra di dialogo **azioni script** fare clic su **Aggiungi**e quindi nel sottomenu fare clic sulle azioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="86695-116">In the **Script Actions** dialog box, click **Add**, and on the submenu, click the desired actions.</span></span>

3.  <span data-ttu-id="86695-117">Configurare le azioni come descritto nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="86695-117">Configure the actions as described in the following tables.</span></span>

    <span data-ttu-id="86695-118">**Nota** 
     **Rinominare il computer** è configurato nella scheda **Impostazioni VM** . Per altre informazioni, vedere [come configurare le proprietà del modello di nome computer VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="86695-118">**Note**
**Rename Computer** is configured in the **VM Settings** tab. For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. <span data-ttu-id="86695-119">Impostare l'ordine delle azioni selezionando un'azione e facendo clic **su in alto o in** **basso**.</span><span class="sxs-lookup"><span data-stu-id="86695-119">Set the order of the actions by selecting an action and clicking **Up** or **Down**.</span></span>

5. <span data-ttu-id="86695-120">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="86695-120">Click **OK**.</span></span>

**<span data-ttu-id="86695-121">Nota</span><span class="sxs-lookup"><span data-stu-id="86695-121">Note</span></span>**  
<span data-ttu-id="86695-122">Durante l'esecuzione dello script di join Domain, perché lo script funzioni, l'utente che ha eseguito l'accesso alla macchina virtuale dell'area di lavoro MED-V deve avere diritti di amministratore locale.</span><span class="sxs-lookup"><span data-stu-id="86695-122">When running the Join Domain script, for the script to work, the user logged into the MED-V workspace virtual machine must have local administrator rights.</span></span>



**<span data-ttu-id="86695-123">Nota</span><span class="sxs-lookup"><span data-stu-id="86695-123">Note</span></span>**  
<span data-ttu-id="86695-124">Durante l'esecuzione dello script di accesso automatico disabilitato, è consigliabile disabilitare l'account Guest locale usato per l'accesso automatico dopo il completamento della configurazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="86695-124">When running the Disable Auto-Logon script, it is recommended to disable the local guest account used for the auto-logon once the initial setup is complete.</span></span>



### <a href="" id="bkmk-joindomainproperties"></a>

**<span data-ttu-id="86695-125">Unire le proprietà del dominio</span><span class="sxs-lookup"><span data-stu-id="86695-125">Join Domain Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86695-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86695-126">Property</span></span></th>
<th align="left"><span data-ttu-id="86695-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86695-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-128">Credenziali da usare quando si unisce la VM al dominio</span><span class="sxs-lookup"><span data-stu-id="86695-128">Credentials to use when joining the VM to the domain</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-129">Selezionare una delle credenziali seguenti da usare quando si unisce la VM al dominio:</span><span class="sxs-lookup"><span data-stu-id="86695-129">Select one of the following credentials to use when joining the VM to the domain:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="86695-130">Usare le credenziali di MED-V </strong> : le credenziali dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="86695-130">Use MED-V credentials</strong>—The end-user credentials.</span></span></p></li>
<li><p><strong><span data-ttu-id="86695-131">Utilizzare le credenziali seguenti </strong> : le credenziali specificate; immettere un nome utente e una password nei campi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="86695-131">Use the following credentials</strong>—The credentials specified; enter a user name and password in the corresponding fields.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="86695-132">Nota</span><span class="sxs-lookup"><span data-stu-id="86695-132">Note</span></span></strong><br/><p><span data-ttu-id="86695-133">Le credenziali immesse sono visibili a tutti gli utenti dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="86695-133">The credentials you enter are visible to all MED-V workspace users.</span></span> <span data-ttu-id="86695-134">Non è consigliabile specificare le credenziali di amministratore di dominio.</span><span class="sxs-lookup"><span data-stu-id="86695-134">It is not recommended to provide domain administrator credentials.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-135">Dominio per l'aggiunta</span><span class="sxs-lookup"><span data-stu-id="86695-135">Domain to join</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-136">Seleziona una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="86695-136">Select one of the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="86695-137">Usare il nome di dominio usato per avviare l'area </strong> di lavoro: partecipare al dominio immesso dall'utente finale quando si accede al client MED-V.</span><span class="sxs-lookup"><span data-stu-id="86695-137">Use the domain name utilized in starting the Workspace</strong>—Join the domain entered by the end user when logging into the MED-V client.</span></span></p>
<p><span data-ttu-id="86695-138">Per definire il mapping da NetBIOS a nomi di dominio completi, fare clic su <strong> tabella di mapping del dominio globale </strong> .</span><span class="sxs-lookup"><span data-stu-id="86695-138">To define the mapping from NetBIOS to fully qualified domain names, click <strong>Global domain mapping table</strong>.</span></span> <span data-ttu-id="86695-139">Nella tabella di mapping del dominio globale fare clic su <strong> Aggiungi </strong> , immettere un <strong> nome di dominio NetBIOS </strong> e un nome di dominio completo e <strong> </strong> fare clic su <strong> OK </strong> .</span><span class="sxs-lookup"><span data-stu-id="86695-139">In the global domain mapping table, click <strong>Add</strong>, enter a <strong>NetBIOS domain name</strong> and a <strong>Fully qualified domain name</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="86695-140">Usare il nome di dominio seguente </strong> : partecipare al dominio specificato; immettere un nome di dominio e un nome di dominio NetBIOS nei campi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="86695-140">Use the following domain name</strong>—Join the domain specified; enter a domain name and NetBIOS domain name in the corresponding fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-141">Unità organizzativa</span><span class="sxs-lookup"><span data-stu-id="86695-141">Organization Unit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-142">Un'unità organizzativa (OU) può essere specificata per partecipare al computer a una specifica UO.</span><span class="sxs-lookup"><span data-stu-id="86695-142">An organization unit (OU) may be specified to join the computer to a specific OU.</span></span> <span data-ttu-id="86695-143">Il formato deve seguire un nome distinto dell'UO: OU = &lt; unità organizzativa &gt; , &lt; controller &gt; di dominio (ad esempio ou = QATest, DC = il, DC = MED-V, DC = com).</span><span class="sxs-lookup"><span data-stu-id="86695-143">The format must follow an OU distinguished name: OU=&lt;Organization Unit&gt;,&lt;Domain Controller&gt; (for example, OU=QATest, DC=il, DC=MED-V, DC=com).</span></span></p>
<div class="alert">
<strong><span data-ttu-id="86695-144">Warning</span><span class="sxs-lookup"><span data-stu-id="86695-144">Warning</span></span></strong><br/><p><span data-ttu-id="86695-145">È supportata solo un'unità organizzativa a livello singolo, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="86695-145">Only a single level OU is supported as is shown in the example above.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**<span data-ttu-id="86695-146">Controllare le proprietà di connettività</span><span class="sxs-lookup"><span data-stu-id="86695-146">Check Connectivity Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86695-147">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86695-147">Property</span></span></th>
<th align="left"><span data-ttu-id="86695-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86695-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-149">Indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="86695-149">IP Address</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-150">Indirizzo IP del server a cui si sta verificando la connessione.</span><span class="sxs-lookup"><span data-stu-id="86695-150">The IP Address of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-151">Port</span><span class="sxs-lookup"><span data-stu-id="86695-151">Port</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-152">La porta del server a cui si sta verificando la connessione.</span><span class="sxs-lookup"><span data-stu-id="86695-152">The port of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-153">Timeout</span><span class="sxs-lookup"><span data-stu-id="86695-153">Timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-154">Numero di secondi di attesa di una risposta prima del timeout.</span><span class="sxs-lookup"><span data-stu-id="86695-154">The number of seconds to wait for a response before timing out.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**<span data-ttu-id="86695-155">Proprietà della riga di comando</span><span class="sxs-lookup"><span data-stu-id="86695-155">Command-Line Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86695-156">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86695-156">Property</span></span></th>
<th align="left"><span data-ttu-id="86695-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86695-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-158">Path</span><span class="sxs-lookup"><span data-stu-id="86695-158">Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-159">Il percorso della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="86695-159">The path of the command line.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-160">Argomenti</span><span class="sxs-lookup"><span data-stu-id="86695-160">Arguments</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-161">Argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="86695-161">Command-line arguments.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-162">Attendere l'uscita</span><span class="sxs-lookup"><span data-stu-id="86695-162">Wait for exit</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-163">Selezionare la casella di controllo per attendere un ritorno prima di continuare con le azioni di script.</span><span class="sxs-lookup"><span data-stu-id="86695-163">Select the check box to wait for a return before continuing with the script actions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-164">Errore non riuscito</span><span class="sxs-lookup"><span data-stu-id="86695-164">Fail on error</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-165">Selezionare questa casella di controllo se il valore restituito è tutt'altro che quello specificato.</span><span class="sxs-lookup"><span data-stu-id="86695-165">Select this check box if the return is anything but the value specified.</span></span></p>
<p><span data-ttu-id="86695-166">Immettere il valore che indicherà il comando come operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="86695-166">Enter the value that will indicate the command as a success.</span></span></p>
<p><span data-ttu-id="86695-167">Impostazione predefinita: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="86695-167">Default: <strong>0</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-168">Eseguire una sola volta</span><span class="sxs-lookup"><span data-stu-id="86695-168">Perform only once</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-169">Selezionare questa casella di controllo per eseguire la riga di comando una sola volta.</span><span class="sxs-lookup"><span data-stu-id="86695-169">Select this check box to run the command line only once.</span></span> <span data-ttu-id="86695-170">Se lo script non riesce o viene annullato, il comando non verrà eseguito di nuovo.</span><span class="sxs-lookup"><span data-stu-id="86695-170">If the script fails or is canceled, this command will not be performed again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-171">Questa riga di comando causa il riavvio di Windows nell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="86695-171">This command line causes a restart of Windows in the Workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-172">Selezionare questa casella di controllo se la riga di comando causa un riavvio dopo il completamento.</span><span class="sxs-lookup"><span data-stu-id="86695-172">Select this check box if the command line causes a restart after completion.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-173">Consenti interazione</span><span class="sxs-lookup"><span data-stu-id="86695-173">Allow interaction</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-174">Selezionare questa casella di controllo se il comando richiede l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="86695-174">Select this check box if the command will require user interaction.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-175">Messaggio di stato</span><span class="sxs-lookup"><span data-stu-id="86695-175">Progress message</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-176">Messaggio da visualizzare all'utente durante l'esecuzione del comando.</span><span class="sxs-lookup"><span data-stu-id="86695-176">Message to be displayed to the user while the command is running.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-177">Messaggio di errore</span><span class="sxs-lookup"><span data-stu-id="86695-177">Failure message</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-178">Messaggio da visualizzare all'utente se il comando non riesce.</span><span class="sxs-lookup"><span data-stu-id="86695-178">Message to be displayed to the user if the command fails.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="86695-179">Quando si configura l'azione della riga di comando, è possibile usare diverse variabili come definito nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="86695-179">When configuring the command-line action, several variables can be used as defined in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="86695-180">Parametro</span><span class="sxs-lookup"><span data-stu-id="86695-180">Parameter</span></span></th>
<th align="left"><span data-ttu-id="86695-181">Valore</span><span class="sxs-lookup"><span data-stu-id="86695-181">Value</span></span></th>
<th align="left"><span data-ttu-id="86695-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86695-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-183">%MEDVUser%</span><span class="sxs-lookup"><span data-stu-id="86695-183">%MEDVUser%</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-184">Nome utente autenticato.</span><span class="sxs-lookup"><span data-stu-id="86695-184">An authenticated user name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-185">Nome utente autenticato di MED-V.</span><span class="sxs-lookup"><span data-stu-id="86695-185">MED-V authenticated user name.</span></span> <span data-ttu-id="86695-186">Il nome utente e la password possono essere usati nello script di configurazione della VM di join Domain.</span><span class="sxs-lookup"><span data-stu-id="86695-186">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-187">%MEDVPassword%</span><span class="sxs-lookup"><span data-stu-id="86695-187">%MEDVPassword%</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-188">Una password autenticata.</span><span class="sxs-lookup"><span data-stu-id="86695-188">An authenticated password.</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-189">Password autenticata di MED-V.</span><span class="sxs-lookup"><span data-stu-id="86695-189">MED-V authenticated password.</span></span> <span data-ttu-id="86695-190">Il nome utente e la password possono essere usati nello script di configurazione della VM di join Domain.</span><span class="sxs-lookup"><span data-stu-id="86695-190">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="86695-191">%MEDVDomain%</span><span class="sxs-lookup"><span data-stu-id="86695-191">%MEDVDomain%</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-192">Dominio configurato.</span><span class="sxs-lookup"><span data-stu-id="86695-192">Configured domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-193">Il dominio configurato nell'autenticazione MED-V.</span><span class="sxs-lookup"><span data-stu-id="86695-193">The domain configured in the MED-V authentication.</span></span> <span data-ttu-id="86695-194">Può essere usato nello script di configurazione della VM.</span><span class="sxs-lookup"><span data-stu-id="86695-194">It can be used on the VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="86695-195">%DesiredMachineName%</span><span class="sxs-lookup"><span data-stu-id="86695-195">%DesiredMachineName%</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-196">Nome computer.</span><span class="sxs-lookup"><span data-stu-id="86695-196">Computer name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="86695-197">Il nome del computer univoco configurato nell'applicazione di gestione.</span><span class="sxs-lookup"><span data-stu-id="86695-197">The unique computer name configured in the management application.</span></span> <span data-ttu-id="86695-198">Può essere usato nello script di configurazione della VM.</span><span class="sxs-lookup"><span data-stu-id="86695-198">It can be used in the VM setup script.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="86695-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86695-199">Related topics</span></span>


[<span data-ttu-id="86695-200">Come configurare la macchina virtuale per un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="86695-200">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="86695-201">Come configurare le proprietà dei modelli di nome dei computer VM</span><span class="sxs-lookup"><span data-stu-id="86695-201">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





