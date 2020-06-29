---
title: Pianificazione di come proteggere i siti Web di MBAM
description: Pianificazione di come proteggere i siti Web di MBAM
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825025"
---
# <span data-ttu-id="1ee01-103">Pianificazione di come proteggere i siti Web di MBAM</span><span class="sxs-lookup"><span data-stu-id="1ee01-103">Planning How to Secure the MBAM Websites</span></span>


<span data-ttu-id="1ee01-104">In questo argomento vengono descritti i metodi seguenti per proteggere il sito Web di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 e il portale self-service di amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="1ee01-104">This topic describes the following methods for securing the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Administration and Monitoring Website and Self-Service Portal:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee01-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="1ee01-105">Method</span></span></th>
<th align="left"><span data-ttu-id="1ee01-106">Obbligatorio o facoltativo?</span><span class="sxs-lookup"><span data-stu-id="1ee01-106">Required or optional?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-107">Usare i certificati per proteggere i siti Web di MBAM</span><span class="sxs-lookup"><span data-stu-id="1ee01-107">Using certificates to secure MBAM websites</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-108">Facoltativo, ma altamente raccomandato</span><span class="sxs-lookup"><span data-stu-id="1ee01-108">Optional, but highly recommended</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-109">Registrazione di nomi di entità servizio (SPN) per l'account del pool di applicazioni</span><span class="sxs-lookup"><span data-stu-id="1ee01-109">Registering Service Principal Names (SPN) for the application pool account</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-110">Obbligatorio</span><span class="sxs-lookup"><span data-stu-id="1ee01-110">Required</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="1ee01-111">Per altre informazioni su come proteggere la distribuzione di MBAM, vedere [considerazioni sulla sicurezza di mbam 2,5](mbam-25-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="1ee01-111">For more information about how to secure your MBAM deployment, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md).</span></span>

## <span data-ttu-id="1ee01-112">Usare i certificati per proteggere i siti Web di MBAM</span><span class="sxs-lookup"><span data-stu-id="1ee01-112">Using certificates to secure MBAM websites</span></span>


<span data-ttu-id="1ee01-113">È consigliabile usare un certificato per proteggere la comunicazione tra:</span><span class="sxs-lookup"><span data-stu-id="1ee01-113">We recommend that you use a certificate to secure the communication between the:</span></span>

-   <span data-ttu-id="1ee01-114">Client MBAM e servizi Web</span><span class="sxs-lookup"><span data-stu-id="1ee01-114">MBAM Client and the web services</span></span>

-   <span data-ttu-id="1ee01-115">Browser e sito Web per l'amministrazione e il monitoraggio e i siti Web portale self-service</span><span class="sxs-lookup"><span data-stu-id="1ee01-115">Browser and the Administration and Monitoring Website and the Self-Service Portal websites</span></span>

<span data-ttu-id="1ee01-116">Per informazioni sulla richiesta e l'installazione di un certificato, vedere [configurazione di certificati server Internet](https://technet.microsoft.com/library/cc731977.aspx).</span><span class="sxs-lookup"><span data-stu-id="1ee01-116">For information about requesting and installing a certificate, see [Configuring Internet Server Certificates](https://technet.microsoft.com/library/cc731977.aspx).</span></span>

**<span data-ttu-id="1ee01-117">Nota</span><span class="sxs-lookup"><span data-stu-id="1ee01-117">Note</span></span>**  
<span data-ttu-id="1ee01-118">È possibile configurare i siti Web e i servizi Web in server diversi solo se si usa Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ee01-118">You can configure the websites and web services on different servers only if you are using Windows PowerShell.</span></span> <span data-ttu-id="1ee01-119">Se si usa la configurazione guidata di MBAM server per configurare i siti Web, è necessario configurare i siti Web e i servizi Web nello stesso server.</span><span class="sxs-lookup"><span data-stu-id="1ee01-119">If you use the MBAM Server Configuration wizard to configure the websites, you must configure the websites and the web services on the same server.</span></span>



<span data-ttu-id="1ee01-120">Per proteggere la comunicazione tra i servizi Web e i database, è consigliabile forzare la crittografia in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1ee01-120">To secure the communication between the web services and the databases, we also recommend that you force encryption in SQL Server.</span></span> <span data-ttu-id="1ee01-121">Per informazioni su come proteggere tutte le connessioni a SQL Server, incluse le comunicazioni tra i servizi Web e SQL Server, vedere [considerazioni sulla sicurezza di MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).</span><span class="sxs-lookup"><span data-stu-id="1ee01-121">For information about securing all connections to SQL Server, including communication between the web services and SQL Server, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-secure-databases).</span></span>

## <span data-ttu-id="1ee01-122">Registrazione di nomi SPN per l'account del pool di applicazioni</span><span class="sxs-lookup"><span data-stu-id="1ee01-122">Registering SPNs for the application pool account</span></span>


<span data-ttu-id="1ee01-123">Per consentire ai server MBAM di autenticare le comunicazioni dal sito Web di amministrazione e monitoraggio e dal portale self-service, è necessario registrare un nome dell'entità servizio (SPN) per il nome host sotto l'account di dominio in uso per il pool di applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="1ee01-123">To enable the MBAM Servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span>

<span data-ttu-id="1ee01-124">Questo argomento contiene istruzioni su come registrare i nomi SPN per i tipi di nome host seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ee01-124">This topic contains instructions on how to register SPNs for the following types of host names:</span></span>

-   <span data-ttu-id="1ee01-125">Nome di dominio completo</span><span class="sxs-lookup"><span data-stu-id="1ee01-125">Fully qualified domain name</span></span>

-   <span data-ttu-id="1ee01-126">Nome NetBIOS</span><span class="sxs-lookup"><span data-stu-id="1ee01-126">NetBIOS name</span></span>

-   <span data-ttu-id="1ee01-127">Nome virtuale</span><span class="sxs-lookup"><span data-stu-id="1ee01-127">Virtual name</span></span>

### <span data-ttu-id="1ee01-128">Prima di creare nomi SPN per un'installazione iniziale di MBAM</span><span class="sxs-lookup"><span data-stu-id="1ee01-128">Before you create SPNs for an initial MBAM installation</span></span>

<span data-ttu-id="1ee01-129">Esaminare le informazioni nella tabella seguente prima di iniziare la creazione di nomi SPN.</span><span class="sxs-lookup"><span data-stu-id="1ee01-129">Review the information in the following table before you start creating SPNs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee01-130">Attività o elemento</span><span class="sxs-lookup"><span data-stu-id="1ee01-130">Task or item</span></span></th>
<th align="left"><span data-ttu-id="1ee01-131">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="1ee01-131">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-132">Creare un account del servizio in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ee01-132">Create a service account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-133">L'account del servizio è un account utente creato in servizi di dominio Active Directory per garantirne la sicurezza per i siti Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ee01-133">The service account is a user account that you create in AD DS to provide security for the MBAM websites.</span></span> <span data-ttu-id="1ee01-134">I siti Web di MBAM vengono eseguiti in un pool di applicazioni, la cui identità è il nome dell'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="1ee01-134">The MBAM websites run under an application pool, whose identity is the name of the service account.</span></span> <span data-ttu-id="1ee01-135">I nomi SPN vengono quindi registrati nell'account del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ee01-135">The SPNs are then registered in the application pool account.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="1ee01-136">Nota</span><span class="sxs-lookup"><span data-stu-id="1ee01-136">Note</span></span></strong><br/><p><span data-ttu-id="1ee01-137">È necessario usare lo stesso account del pool di applicazioni per tutti i server Web.</span><span class="sxs-lookup"><span data-stu-id="1ee01-137">You must use the same application pool account for all web servers.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-138">Verificare che l'account del gruppo IIS-IUSRS o l'account del pool di applicazioni dispongano dei diritti necessari.</span><span class="sxs-lookup"><span data-stu-id="1ee01-138">Verify that either the IIS-IUSRS group account or the application pool account has been granted the necessary rights.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-139">Per eseguire questa operazione, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ee01-139">To check this, follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="1ee01-140">Aprire l' <strong> Editor criteri di sicurezza locali </strong> ed espandere il <strong> nodo Criteri locali </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-140">Open the <strong>Local Security Policy editor</strong> and expand the <strong>Local Policies</strong> node.</span></span></p></li>
<li><p><span data-ttu-id="1ee01-141">Selezionare il <strong> nodo assegnazione diritti utente </strong> e fare doppio clic sul pulsante <strong> rappresenta un client dopo l'autenticazione </strong> e <strong> accedere come impostazioni dei </strong> criteri di gruppo processo batch nel riquadro destro.</span><span class="sxs-lookup"><span data-stu-id="1ee01-141">Select the <strong>User Rights Assignment</strong> node, and double-click the <strong>Impersonate a client after authentication</strong> and <strong>Log on as a batch job</strong> Group Policy settings in the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-142">Se si configurano i siti Web di MBAM usando un account di amministrazione del dominio, MBAM creerà i nomi SPN per l'utente.</span><span class="sxs-lookup"><span data-stu-id="1ee01-142">If you configure the MBAM websites by using a domain administrative account, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-143">Se si configurano i siti Web di MBAM usando un account di amministrazione del dominio, seguire i passaggi descritti in questo argomento per registrare i nomi SPN manualmente per il tipo di nome host in uso.</span><span class="sxs-lookup"><span data-stu-id="1ee01-143">If you configure the MBAM websites by using a domain administrative account, follow the steps in this topic to register SPNs manually for the type of host name that you are using.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1ee01-144">Registrazione di nomi SPN quando si usa un nome host di dominio completo</span><span class="sxs-lookup"><span data-stu-id="1ee01-144">Registering SPNs when you use a fully qualified domain host name</span></span>

<span data-ttu-id="1ee01-145">Se si usa un nome host di dominio completo quando si configura MBAM, è necessario registrare un solo SPN, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="1ee01-145">If you use a fully qualified domain host name when you configure MBAM, you have to register only one SPN, as shown in the following example.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee01-146">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="1ee01-146">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="1ee01-147">Esempi e altre informazioni</span><span class="sxs-lookup"><span data-stu-id="1ee01-147">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-148">Registrare un SPN per il nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="1ee01-148">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="1ee01-149">Il nome host completo è <strong> mybitlockerrecovery.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-149">The fully qualified host name is <strong>mybitlockerrecovery.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-150">Configurare la delega vincolata per l'SPN che si sta registrando per l'account del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ee01-150">Configure constrained delegation for the SPN that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="1ee01-151">Configurazione della delega vincolata</span><span class="sxs-lookup"><span data-stu-id="1ee01-151">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="1ee01-152">Questo requisito si applica solo a MBAM 2,5; non è necessario in MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="1ee01-152">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="1ee01-153">Registrazione di nomi SPN quando si usa un nome host NetBIOS</span><span class="sxs-lookup"><span data-stu-id="1ee01-153">Registering SPNs when you use a NetBIOS host name</span></span>

<span data-ttu-id="1ee01-154">Se si usa un nome host NetBIOS quando si configura MBAM, registrare un SPN per il nome NetBIOS e un altro SPN per il nome di dominio completo, come illustrato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ee01-154">If you use a NetBIOS host name when you configure MBAM, register one SPN for the NetBIOS name, and another SPN for the fully qualified domain name, as shown in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee01-155">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="1ee01-155">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="1ee01-156">Esempi e altre informazioni</span><span class="sxs-lookup"><span data-stu-id="1ee01-156">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-157">Registrare un SPN per il nome host NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="1ee01-157">Register an SPN for the NetBIOS host name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="1ee01-158">Il nome host NetBIOS è <strong> nbname01 </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-158">The NetBIOS host name is <strong>nbname01</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-159">Registrare un SPN per il nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="1ee01-159">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="1ee01-160">Il nome di dominio completo è <strong> nbname01.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-160">The fully qualified domain name is <strong>nbname01.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-161">Configurare la delega vincolata per i nomi SPN che si sta registrando per l'account del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ee01-161">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="1ee01-162">Configurazione della delega vincolata</span><span class="sxs-lookup"><span data-stu-id="1ee01-162">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="1ee01-163">Questo requisito si applica solo a MBAM 2,5; non è necessario in MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="1ee01-163">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a><span data-ttu-id="1ee01-164">Registrazione di nomi SPN quando si usa un nome host virtuale</span><span class="sxs-lookup"><span data-stu-id="1ee01-164">Registering SPNs when you use a virtual host name</span></span>

<span data-ttu-id="1ee01-165">Se si configura MBAM con un nome host virtuale che è un nome di dominio completo, registrare un solo SPN per il nome host virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ee01-165">If you configure MBAM with a virtual host name that is a fully qualified domain name, register only one SPN for the virtual host name.</span></span> <span data-ttu-id="1ee01-166">Se il nome host virtuale configurato non è un nome di dominio completo, è necessario creare un secondo SPN che specifichi il nome di dominio completo, come descritto negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ee01-166">If the virtual host name that you configure is not a fully qualified domain name, you must create a second SPN that specifies the fully qualified domain name, as described in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee01-167">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="1ee01-167">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="1ee01-168">Esempi e altre informazioni</span><span class="sxs-lookup"><span data-stu-id="1ee01-168">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-169">Se il nome host virtuale è un nome di dominio completo, come in questo esempio, registrare un solo SPN.</span><span class="sxs-lookup"><span data-stu-id="1ee01-169">If your virtual host name is a fully qualified domain name, as in this example, register only one SPN.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="1ee01-170">Nell'esempio, il nome host virtuale è <strong> mbamvirtual.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-170">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-171">Registrare questo SPN aggiuntivo se il nome host virtuale non è un nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="1ee01-171">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="1ee01-172">Nell'esempio, il nome host virtuale è <strong> mbamvirtual </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-172">In the example, the virtual host name is <strong>mbamvirtual</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-173">Registrare questo SPN aggiuntivo se il nome host virtuale non è un nome di dominio completo.</span><span class="sxs-lookup"><span data-stu-id="1ee01-173">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="1ee01-174">Nell'esempio, il nome host virtuale è <strong> mbamvirtual.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-174">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-175">Nel server Domain Name Server (DNS) creare un "un record" per il nome host personalizzato e puntarlo a un server Web o a un servizio di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1ee01-175">On the Domain Name Server (DNS) server, create an “A record” for the custom host name and point it to a web server or a load balancer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-176">Vedere la sezione "per configurare DNS host A Records" in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> configurare i record host DNS </a> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-176">See the “To configure DNS Host A Records” section in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)">Configure DNS Host Records</a>.</span></span></p>
<p><span data-ttu-id="1ee01-177">Ti consigliamo di usare un record anziché CNAME.</span><span class="sxs-lookup"><span data-stu-id="1ee01-177">We recommend that you use A records instead of CNAMES.</span></span> <span data-ttu-id="1ee01-178">Se si usano i CNAME per puntare all'indirizzo del dominio, è necessario registrare anche i nomi SPN per il nome del server Web nell'account del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ee01-178">If you use CNAMES to point to the domain address, you must also register SPNs for the web server name in the application pool account.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-179">Configurare la delega vincolata per i nomi SPN che si sta registrando per l'account del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ee01-179">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="1ee01-180">Configurazione della delega vincolata</span><span class="sxs-lookup"><span data-stu-id="1ee01-180">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="1ee01-181">Questo requisito si applica solo a MBAM 2,5; non è necessario in MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="1ee01-181">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a><span data-ttu-id="1ee01-182">Registrazione di un SPN quando si esegue l'aggiornamento da versioni precedenti di MBAM</span><span class="sxs-lookup"><span data-stu-id="1ee01-182">Registering an SPN when you upgrade from previous versions of MBAM</span></span>

<span data-ttu-id="1ee01-183">Completare i passaggi descritti in questa sezione solo se si vuole:</span><span class="sxs-lookup"><span data-stu-id="1ee01-183">Complete the steps in this section only if you want to:</span></span>

-   <span data-ttu-id="1ee01-184">Eseguire l'aggiornamento da una versione precedente di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ee01-184">Upgrade from a previous version of MBAM.</span></span>

-   <span data-ttu-id="1ee01-185">Eseguire i siti Web in MBAM 2,5 in una configurazione con bilanciamento del carico o distribuita ed è attualmente in esecuzione in una configurazione che non viene caricata in maniera equilibrata.</span><span class="sxs-lookup"><span data-stu-id="1ee01-185">Run the websites in MBAM 2.5 in a load-balanced or distributed configuration, and you are currently running in a configuration that is not load balanced.</span></span>

<span data-ttu-id="1ee01-186">Se i nomi SPN sono già stati registrati nell'account del computer anziché in un account del pool di applicazioni, MBAM usa i nomi SPN esistenti e non è possibile configurare i siti Web in una configurazione con bilanciamento del carico o distribuita.</span><span class="sxs-lookup"><span data-stu-id="1ee01-186">If you already registered SPNs on the machine account rather than in an application pool account, MBAM uses the existing SPNs, and you cannot configure the websites in a load-balanced or distributed configuration.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee01-187">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="1ee01-187">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="1ee01-188">Esempi e altre informazioni</span><span class="sxs-lookup"><span data-stu-id="1ee01-188">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-189">Creare un account del pool di applicazioni in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ee01-189">Create an application pool account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-190">Rimuovere i Web site e i servizi Web attualmente installati.</span><span class="sxs-lookup"><span data-stu-id="1ee01-190">Remove the currently installed websites and web services.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="1ee01-191">Rimozione di software o funzionalità del server di MBAM</span><span class="sxs-lookup"><span data-stu-id="1ee01-191">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-192">Rimuovere i nomi SPN dall'account del computer.</span><span class="sxs-lookup"><span data-stu-id="1ee01-192">Remove SPNs from the machine account.</span></span></p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-193">Registrare nomi SPN nell'account del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ee01-193">Register SPNs in the application pool account.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-194">Seguire la procedura per la <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> registrazione di nomi SPN quando si usa un nome host virtuale </a> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-194">Follow the steps for <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">Registering SPNs when you use a virtual host name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ee01-195">Riconfigurare le applicazioni Web e i servizi Web.</span><span class="sxs-lookup"><span data-stu-id="1ee01-195">Reconfigure the web applications and web services.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="1ee01-196">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1ee01-196">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ee01-197">Eseguire una delle operazioni seguenti, a seconda del metodo usato per la configurazione:</span><span class="sxs-lookup"><span data-stu-id="1ee01-197">Do one of the following, depending on the method you use for the configuration:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ee01-198">Metodo</span><span class="sxs-lookup"><span data-stu-id="1ee01-198">Method</span></span></th>
<th align="left"><span data-ttu-id="1ee01-199">Dettagli</span><span class="sxs-lookup"><span data-stu-id="1ee01-199">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="1ee01-200">Configurazione guidata server MBAM</span><span class="sxs-lookup"><span data-stu-id="1ee01-200">MBAM Server Configuration wizard</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="1ee01-201">Immettere l'account del pool di applicazioni nel <strong> campo account di dominio del pool di applicazioni del servizio Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="1ee01-201">Enter the application pool account in the <strong>Web service application pool domain account</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> <span data-ttu-id="1ee01-202">Cmdlet di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ee01-202">Windows PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ee01-203">Immettere l'account nel <code>WebServiceApplicationPoolCredential</code> parametro.</span><span class="sxs-lookup"><span data-stu-id="1ee01-203">Enter the account in the <code>WebServiceApplicationPoolCredential</code> parameter.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="1ee01-204">Importante</span><span class="sxs-lookup"><span data-stu-id="1ee01-204">Important</span></span></strong><br/><p><span data-ttu-id="1ee01-205">Il nome host immesso deve avere lo stesso nome del nome host virtuale per cui si stanno creando i nomi SPN.</span><span class="sxs-lookup"><span data-stu-id="1ee01-205">The host name that you enter must be the same name as the virtual host name for which you are creating the SPNs.</span></span> <span data-ttu-id="1ee01-206">Inoltre, nella Web farm i nomi host e le credenziali del pool di applicazioni devono essere identici per ogni server che si sta configurando.</span><span class="sxs-lookup"><span data-stu-id="1ee01-206">Also, in your web farm, the host names and the application pool credentials must be the same on every server that you are configuring.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="1ee01-207">Quando MBAM configura le applicazioni Web, cercherà di registrare i nomi SPN per l'utente, ma può farlo solo se si hanno diritti di amministratore di dominio nel server in cui si sta installando MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ee01-207">When MBAM configures the web applications, it will try to register the SPNs for you, but it can do so only if you have Domain Admin rights on the server on which you are installing MBAM.</span></span> <span data-ttu-id="1ee01-208">Se non si dispone di questi diritti, è possibile completare la configurazione, ma sarà necessario impostare i nomi SPN prima o dopo la configurazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ee01-208">If you do not have these rights, you can complete the configuration, but you will have to set the SPNs before or after you configure MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="1ee01-209">Impostazioni di filtro richieste obbligatorie</span><span class="sxs-lookup"><span data-stu-id="1ee01-209">Required Request Filtering Settings</span></span>

 <span data-ttu-id="1ee01-210">Per consentire all'applicazione di operare come previsto, è necessario "Consenti estensioni di file non in elenco".</span><span class="sxs-lookup"><span data-stu-id="1ee01-210">'Allow unlisted file name extensions' is required for the application to operate as expected.</span></span>  <span data-ttu-id="1ee01-211">Questa operazione può essere trovata passando alla pagina "amministrazione e monitoraggio di Microsoft BitLocker"-> filtro delle richieste-> modificare le impostazioni delle caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="1ee01-211">This can be found by navigating to the 'Microsoft BitLocker Administration and Monitoring' -> Request Filtering -> Edit Feature Settings.</span></span>


## <span data-ttu-id="1ee01-212">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ee01-212">Related topics</span></span>


[<span data-ttu-id="1ee01-213">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1ee01-213">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="1ee01-214">Prerequisiti per la distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="1ee01-214">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)





## <span data-ttu-id="1ee01-215">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="1ee01-215">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="1ee01-216">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="1ee01-216">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="1ee01-217">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="1ee01-217">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



