---
title: Come configurare il server in modo che sia attendibile per la delega
description: Come configurare il server in modo che sia attendibile per la delega
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817746"
---
# <span data-ttu-id="aa233-103">Come configurare il server in modo che sia attendibile per la delega</span><span class="sxs-lookup"><span data-stu-id="aa233-103">How to Configure the Server to be Trusted for Delegation</span></span>


<span data-ttu-id="aa233-104">Quando si installa il software Microsoft Application Virtualization (App-V) Management Server, è possibile scegliere di installarlo usando un'architettura di sistema distribuita.</span><span class="sxs-lookup"><span data-stu-id="aa233-104">When you install the Microsoft Application Virtualization (App-V) Management Server software, you can choose to install it by using a distributed system architecture.</span></span> <span data-ttu-id="aa233-105">Se si installa la console, il servizio Web di gestione e il database in computer diversi, è necessario configurare il server Internet Information Services (IIS) come attendibile per la delega.</span><span class="sxs-lookup"><span data-stu-id="aa233-105">If you install the console, the Management Web Service, and the database on different computers, you must configure the Internet Information Services (IIS) server to be trusted for delegation.</span></span> <span data-ttu-id="aa233-106">Questa operazione è necessaria perché il servizio Web di gestione tenterà di connettersi all'archivio dati App-V usando le credenziali dell'amministratore di App-V che usa la console.</span><span class="sxs-lookup"><span data-stu-id="aa233-106">This is necessary because the Management Web Service will attempt to connect to the App-V data store by using the credentials of the App-V administrator who is using the console.</span></span> <span data-ttu-id="aa233-107">Il server di database in cui è installato l'archivio dati non accetterà le credenziali dell'amministratore dal server IIS, a meno che il server IIS non sia configurato per essere considerato attendibile per la delega e quindi il servizio Web di gestione non sarà in grado di connettersi all'archivio dati di App-V.</span><span class="sxs-lookup"><span data-stu-id="aa233-107">The database server on which the data store is installed will not accept the administrator’s credentials from the IIS server unless the IIS server is configured to be trusted for delegation, and so the Management Web Service will not be able to connect to the App-V data store.</span></span>

<span data-ttu-id="aa233-108">**Nota**  Se si installa il software App-V Management Server in un singolo server e si inserisce l'archivio dati in un server distinto, è comunque necessario configurare il server in modo che sia attendibile per la delega anche se il servizio Web di gestione e la console di gestione si trovano nello stesso server.</span><span class="sxs-lookup"><span data-stu-id="aa233-108">**Note** If you install the App-V Management Server software on a single server and place the data store on a separate server, there is one situation in which you must still configure the server to be trusted for delegation even though the Management Web Service and Management Console are on the same server.</span></span> <span data-ttu-id="aa233-109">Questa situazione si verifica se è necessario connettersi al servizio Web di gestione nella console usando l'opzione **Usa credenziali alternative** .</span><span class="sxs-lookup"><span data-stu-id="aa233-109">This situation occurs if you need to connect to the Management Web Service in the console by using the **Use Alternate Credentials** option.</span></span>

 

<span data-ttu-id="aa233-110">Il tipo di delega che puoi usare dipende dal livello di funzionalità del dominio configurato nell'infrastruttura di servizi di dominio Active Directory (aggiunge).</span><span class="sxs-lookup"><span data-stu-id="aa233-110">The type of delegation that you can use depends on the Domain Functional Level that you have configured in your Active Directory Domain Services (ADDS) infrastructure.</span></span> <span data-ttu-id="aa233-111">La tabella seguente elenca i tipi di delega che possono essere configurati per ogni livello di funzionalità del dominio per App-V.</span><span class="sxs-lookup"><span data-stu-id="aa233-111">The following table lists the types of delegation that can be configured for each Domain Functional Level for App-V.</span></span> <span data-ttu-id="aa233-112">Istruzioni dettagliate seguire la tabella.</span><span class="sxs-lookup"><span data-stu-id="aa233-112">Detailed instructions follow the table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="aa233-113">Livello di funzionalità del dominio</span><span class="sxs-lookup"><span data-stu-id="aa233-113">Domain Functional Level</span></span></th>
<th align="left"><span data-ttu-id="aa233-114">Livelli di delega disponibili</span><span class="sxs-lookup"><span data-stu-id="aa233-114">Delegation Levels Available</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="aa233-115">Windows 2000 Native</span><span class="sxs-lookup"><span data-stu-id="aa233-115">Windows 2000 native</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="aa233-116">Nessuna delega (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa233-116">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="aa233-117">Delega senza vincoli</span><span class="sxs-lookup"><span data-stu-id="aa233-117">Unconstrained delegation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="aa233-118">Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa233-118">Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="aa233-119">Nessuna delega (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa233-119">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="aa233-120">Delega senza vincoli ¹</span><span class="sxs-lookup"><span data-stu-id="aa233-120">Unconstrained delegation¹</span></span></p></li>
<li><p><span data-ttu-id="aa233-121">Delega vincolata (usare solo protocolli Kerberos)</span><span class="sxs-lookup"><span data-stu-id="aa233-121">Constrained delegation (Use Kerberos Only Protocols)</span></span></p></li>
<li><p><span data-ttu-id="aa233-122">Delega vincolata (usare qualsiasi protocollo di autenticazione) ¹</span><span class="sxs-lookup"><span data-stu-id="aa233-122">Constrained delegation (Use any authentication protocol) ¹</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="aa233-123">¹ non consigliato.</span><span class="sxs-lookup"><span data-stu-id="aa233-123">¹ Not recommended.</span></span>

## <span data-ttu-id="aa233-124">Per configurare la delega senza vincoli quando il livello di funzionalità del dominio è Windows 2000 Native</span><span class="sxs-lookup"><span data-stu-id="aa233-124">To configure unconstrained delegation when the Domain Functional Level is Windows 2000 native</span></span>


<span data-ttu-id="aa233-125">Nel Domain controller per il dominio del server Web completare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="aa233-125">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="aa233-126">Fare clic su **Start**, **strumenti di amministrazione**e quindi su **utenti e computer di Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="aa233-126">Click **Start**, **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="aa233-127">Espandere Domain e quindi espandere la cartella computer.</span><span class="sxs-lookup"><span data-stu-id="aa233-127">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="aa233-128">Nel riquadro destro fare clic con il pulsante destro del mouse sul nome del computer per il server Web e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="aa233-128">In the right pane, right-click the computer name for the Web server, and then click **Properties**.</span></span>

4.  <span data-ttu-id="aa233-129">Nella scheda **generale** verificare che la casella **di controllo attendibile computer per delega** sia selezionata.</span><span class="sxs-lookup"><span data-stu-id="aa233-129">On the **General** tab, ensure that the **Trust computer for delegation** check box is selected.</span></span>

5.  <span data-ttu-id="aa233-130">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa233-130">Click **OK**.</span></span>

## <span data-ttu-id="aa233-131">Per configurare la delega senza vincoli quando il livello di funzionalità del dominio è Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa233-131">To configure unconstrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="aa233-132">Nel Domain controller per il dominio del server Web completare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="aa233-132">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="aa233-133">Fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e quindi fare clic su **utenti e computer di Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="aa233-133">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="aa233-134">Espandere Domain ed espandere la cartella computer.</span><span class="sxs-lookup"><span data-stu-id="aa233-134">Expand domain, and expand the Computers folder.</span></span>

3.  <span data-ttu-id="aa233-135">Nel riquadro destro fare clic con il pulsante destro del mouse sul nome del computer per il server Web, scegliere **Proprietà**e quindi fare clic sulla scheda **delega** .</span><span class="sxs-lookup"><span data-stu-id="aa233-135">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="aa233-136">Fare clic per selezionare **Considera attendibile il computer per la delega a qualsiasi servizio (solo Kerberos)**.</span><span class="sxs-lookup"><span data-stu-id="aa233-136">Click to select **Trust this computer for delegation to any service (Kerberos only)**.</span></span>

5.  <span data-ttu-id="aa233-137">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa233-137">Click **OK**.</span></span>

## <span data-ttu-id="aa233-138">Per configurare la delega vincolata quando il livello di funzionalità del dominio è Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa233-138">To configure constrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="aa233-139">Nel Domain controller per il dominio del server Web completare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="aa233-139">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="aa233-140">Fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**e quindi fare clic su **utenti e computer di Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="aa233-140">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="aa233-141">Espandere Domain e quindi espandere la cartella computer.</span><span class="sxs-lookup"><span data-stu-id="aa233-141">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="aa233-142">Nel riquadro destro fare clic con il pulsante destro del mouse sul nome del computer per il server Web, scegliere **Proprietà**e quindi fare clic sulla scheda **delega** .</span><span class="sxs-lookup"><span data-stu-id="aa233-142">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="aa233-143">Fare clic per selezionare **Considera attendibile il computer solo per la delega per i servizi specificati**.</span><span class="sxs-lookup"><span data-stu-id="aa233-143">Click to select **Trust this computer for delegation to specified services only**.</span></span>

5.  <span data-ttu-id="aa233-144">Verificare che l'opzione **Usa solo Kerberos** sia selezionata e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa233-144">Ensure that **Use Kerberos only** is selected, and then click **OK**.</span></span>

6.  <span data-ttu-id="aa233-145">Fare clic sul pulsante **Aggiungi** .</span><span class="sxs-lookup"><span data-stu-id="aa233-145">Click the **Add** button.</span></span> <span data-ttu-id="aa233-146">Nella finestra di dialogo **Aggiungi servizi** fare clic su **utenti o computer**e quindi selezionare o digitare il nome di Microsoft SQL Server in cui è installato l'App-V Data Store e ricevere le credenziali degli utenti da IIS.</span><span class="sxs-lookup"><span data-stu-id="aa233-146">In the **Add Services** dialog box, click **Users or Computers**, and then browse to or type the name of the Microsoft SQL server that has the App-V data store and is to receive the users credentials from IIS.</span></span> <span data-ttu-id="aa233-147">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa233-147">Click **OK**.</span></span>

7.  <span data-ttu-id="aa233-148">Nell'elenco **Servizi disponibili** selezionare il servizio MSSQLSvc che elenca il numero di porta in cui Microsoft SQL Server accetta connessioni per il database App-V (la porta predefinita è 1433).</span><span class="sxs-lookup"><span data-stu-id="aa233-148">In the **Available Services** list, select the MSSQLSvc service that lists port number on which the Microsoft SQL Server is accepting connections for the App-V database (the default port is 1433).</span></span> <span data-ttu-id="aa233-149">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa233-149">Click **OK**.</span></span>

### <span data-ttu-id="aa233-150">Passaggi aggiuntivi per configurare IIS 7 per la delega vincolata</span><span class="sxs-lookup"><span data-stu-id="aa233-150">Additional steps to configure IIS 7 for constrained delegation</span></span>

<span data-ttu-id="aa233-151">Se si esegue il servizio Web di gestione in un server IIS 7, è necessario completare la procedura seguente per impostare la variabile *useAppPoolCredentials* di IIS 7 su true.</span><span class="sxs-lookup"><span data-stu-id="aa233-151">If you are running the Management Web Service on an IIS 7 server, you must complete the following steps to set the IIS 7 *useAppPoolCredentials* variable to True.</span></span>

1.  <span data-ttu-id="aa233-152">Aprire una finestra del prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="aa233-152">Open an elevated Command Prompt window.</span></span> <span data-ttu-id="aa233-153">Per aprire una finestra del prompt dei comandi con privilegi elevati, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Accessori**, fare clic con il pulsante destro del mouse su prompt dei **comandi**e quindi scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="aa233-153">To open an elevated Command Prompt window, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="aa233-154">Passare a%windir%\\system32\\inetsrv.</span><span class="sxs-lookup"><span data-stu-id="aa233-154">Navigate to %windir%\\system32\\inetsrv.</span></span>

3.  <span data-ttu-id="aa233-155">Digitare **appcmd.exe set config-section: System. webServer/security/authentication/windowsAuthentication-useAppPoolCredentials: true**e quindi premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="aa233-155">Type **appcmd.exe set config -section:system.webServer/security/authentication/windowsAuthentication -useAppPoolCredentials:true**, and then press ENTER.</span></span>

 

 





