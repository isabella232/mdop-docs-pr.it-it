---
title: Informazioni sul file del gruppo di connessione
description: Informazioni sul file del gruppo di connessione
author: dansimp
ms.assetid: 1f4df515-f5f6-4b58-91a8-c71598cb3ea4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ef9dc9c4465ed8f261b73518348c05ceb78d15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806094"
---
# <span data-ttu-id="f862a-103">Informazioni sul file del gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="f862a-103">About the Connection Group File</span></span>


**<span data-ttu-id="f862a-104">In questo argomento:</span><span class="sxs-lookup"><span data-stu-id="f862a-104">In this topic:</span></span>**

-   [<span data-ttu-id="f862a-105">Scopo e posizione del file del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-105">Connection group file purpose and location</span></span>](#bkmk-cg-purpose-loc)

-   [<span data-ttu-id="f862a-106">Struttura del file XML del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-106">Structure of the connection group XML file</span></span>](#bkmk-define-cg-5-0sp3)

-   [<span data-ttu-id="f862a-107">Configurazione della priorità dei pacchetti in un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-107">Configuring the priority of packages in a connection group</span></span>](#bkmk-config-pkg-priority-incg)

-   [<span data-ttu-id="f862a-108">Configurazioni di connessione dell'applicazione virtuale supportate</span><span class="sxs-lookup"><span data-stu-id="f862a-108">Supported virtual application connection configurations</span></span>](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a><span data-ttu-id="f862a-109">Scopo e posizione del file del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-109">Connection group file purpose and location</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-110">Scopo del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-110">Connection group purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-111">Un gruppo di connessioni è una funzionalità App-V che consente di raggruppare i pacchetti per creare un ambiente virtuale in cui le applicazioni in questi pacchetti possono interagire tra loro.</span><span class="sxs-lookup"><span data-stu-id="f862a-111">A connection group is an App-V feature that enables you to group packages together to create a virtual environment in which the applications in those packages can interact with each other.</span></span></p>
<p><span data-ttu-id="f862a-112">Esempio: si vogliono usare i plug-in con Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f862a-112">Example: You want to use plug-ins with Microsoft Office.</span></span> <span data-ttu-id="f862a-113">È possibile creare un pacchetto che contiene i plug-in e creare un altro pacchetto che contiene Office e quindi aggiungere entrambi i pacchetti a un gruppo di connessioni per consentire a Office di usare questi plug-in.</span><span class="sxs-lookup"><span data-stu-id="f862a-113">You can create a package that contains the plug-ins, and create another package that contains Office, and then add both packages to a connection group to enable Office to use those plug-ins.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f862a-114">Funzionamento del file del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-114">How the connection group file works</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-115">Quando si applica un file del gruppo di connessioni App-V 5,1, i pacchetti enumerati nel file verranno combinati in fase di esecuzione in un unico ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="f862a-115">When you apply an App-V 5.1 connection group file, the packages that are enumerated in the file will be combined at runtime into a single virtual environment.</span></span> <span data-ttu-id="f862a-116">Usare il file del gruppo di connessioni 5,1 di Microsoft Application Virtualization (App-V) per configurare i gruppi di connessioni App-V 5,1 esistenti.</span><span class="sxs-lookup"><span data-stu-id="f862a-116">Use the Microsoft Application Virtualization (App-V) 5.1 connection group file to configure existing App-V 5.1 connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-117">Percorso file di esempio</span><span class="sxs-lookup"><span data-stu-id="f862a-117">Example file path</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span><span class="sxs-lookup"><span data-stu-id="f862a-118">%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups{6CCC7575-162E-4152-9407-ED411DA138F4}{4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a><span data-ttu-id="f862a-119">Struttura del file XML del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-119">Structure of the connection group XML file</span></span>


**<span data-ttu-id="f862a-120">In questa sezione:</span><span class="sxs-lookup"><span data-stu-id="f862a-120">In this section:</span></span>**

-   [<span data-ttu-id="f862a-121">Parametri che definiscono il gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-121">Parameters that define the connection group</span></span>](#bkmk-params-define-cg)

-   [<span data-ttu-id="f862a-122">Parametri che definiscono i pacchetti nel gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-122">Parameters that define the packages in the connection group</span></span>](#bkmk-params-define-pkgs-incg)

-   [<span data-ttu-id="f862a-123">File XML del gruppo di connessioni di esempio App-V</span><span class="sxs-lookup"><span data-stu-id="f862a-123">App-V example connection group XML file</span></span>](#bkmk-50sp3-exp-cg-xml)

-   [<span data-ttu-id="f862a-124">App-V 5,0 tramite l'App-V 5,0 SP2 esempio di file XML del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-124">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a><span data-ttu-id="f862a-125">Parametri che definiscono il gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-125">Parameters that define the connection group</span></span>

<span data-ttu-id="f862a-126">La tabella seguente descrive i parametri nel file XML che definiscono il gruppo di connessioni stesso, non i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f862a-126">The following table describes the parameters in the XML file that define the connection group itself, not the packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f862a-127">Campo</span><span class="sxs-lookup"><span data-stu-id="f862a-127">Field</span></span></th>
<th align="left"><span data-ttu-id="f862a-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f862a-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-129">Nome schema</span><span class="sxs-lookup"><span data-stu-id="f862a-129">Schema name</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-130">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="f862a-130">Name of the schema.</span></span></p>
<p><strong><span data-ttu-id="f862a-131">Applicabile a partire da App-V 5,0 SP3 </strong> : se si vogliono usare le nuove funzionalità "pacchetti facoltativi" e "Usa qualsiasi versione" descritte in questa tabella, è necessario specificare lo schema seguente nel file XML:</span><span class="sxs-lookup"><span data-stu-id="f862a-131">Applicable starting in App-V 5.0 SP3</strong>: If you want to use the new “optional packages” and “use any version” features that are described in this table, you must specify the following schema in the XML file:</span></span></p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f862a-132">AppConnectionGroupId</span><span class="sxs-lookup"><span data-stu-id="f862a-132">AppConnectionGroupId</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-133">Identificatore GUID univoco per il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-133">Unique GUID identifier for this connection group.</span></span> <span data-ttu-id="f862a-134">Lo stato del gruppo di connessioni è associato a questo identificatore.</span><span class="sxs-lookup"><span data-stu-id="f862a-134">The connection group state is associated with this identifier.</span></span> <span data-ttu-id="f862a-135">Specificare questo identificatore solo quando si crea il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-135">Specify this identifier only when you create the connection group.</span></span></p>
<p><span data-ttu-id="f862a-136">È possibile creare un nuovo GUID digitando: <strong>[Guid]::NewGuid()</strong> .</span><span class="sxs-lookup"><span data-stu-id="f862a-136">You can create a new GUID by typing: <strong>[Guid]::NewGuid()</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-137">VersionId</span><span class="sxs-lookup"><span data-stu-id="f862a-137">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-138">Identificatore GUID versione per questa versione del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-138">Version GUID identifier for this version of the connection group.</span></span></p>
<p><span data-ttu-id="f862a-139">Quando si aggiorna un gruppo di connessioni, ad esempio aggiungendo o aggiornando un nuovo pacchetto, è necessario aggiornare il GUID della versione per riflettere la nuova versione.</span><span class="sxs-lookup"><span data-stu-id="f862a-139">When you update a connection group (for example, by adding or updating a new package), you must update the version GUID to reflect the new version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f862a-140">DisplayName</span><span class="sxs-lookup"><span data-stu-id="f862a-140">DisplayName</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-141">Visualizzare il nome del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-141">Display name of the connection group.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-142">Priority</span><span class="sxs-lookup"><span data-stu-id="f862a-142">Priority</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-143">Campo Priority facoltativo per il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-143">Optional priority field for the connection group.</span></span></p>
<p><strong><span data-ttu-id="f862a-144">"0" </strong> - indica la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="f862a-144">“0”</strong> - indicates the highest priority.</span></span></p>
<p><span data-ttu-id="f862a-145">Se è necessaria una priorità, ma non è stata configurata, il pacchetto non riuscirà perché non è possibile determinare il gruppo di connessioni corretto da usare.</span><span class="sxs-lookup"><span data-stu-id="f862a-145">If a priority is required, but has not been configured, the package will fail because the correct connection group to use cannot be determined.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a><span data-ttu-id="f862a-146">Parametri che definiscono i pacchetti nel gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-146">Parameters that define the packages in the connection group</span></span>

<span data-ttu-id="f862a-147">Nella &lt; sezione pacchetti &gt; del file XML del gruppo di connessioni è possibile elencare i pacchetti di membri nel gruppo di connessioni specificando l'identificatore univoco del pacchetto e l'identificatore di versione di ogni pacchetto, come descritto nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f862a-147">In the &lt;Packages&gt; section of the connection group XML file, you list the member packages in the connection group by specifying each package’s unique package identifier and version identifier, as described in the following table.</span></span> <span data-ttu-id="f862a-148">Il primo pacchetto nell'elenco ha la precedenza più alta.</span><span class="sxs-lookup"><span data-stu-id="f862a-148">The first package in the list has the highest precedence.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f862a-149">Campo</span><span class="sxs-lookup"><span data-stu-id="f862a-149">Field</span></span></th>
<th align="left"><span data-ttu-id="f862a-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f862a-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-151">PackageId</span><span class="sxs-lookup"><span data-stu-id="f862a-151">PackageId</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-152">Identificatore GUID univoco per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f862a-152">Unique GUID identifier for this package.</span></span> <span data-ttu-id="f862a-153">Questo GUID non cambia quando vengono pubblicate versioni più recenti del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f862a-153">This GUID doesn’t change when newer versions of the package are published.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f862a-154">VersionId</span><span class="sxs-lookup"><span data-stu-id="f862a-154">VersionId</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-155">Identificatore GUID univoco per la versione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f862a-155">Unique GUID identifier for the version of the package.</span></span></p>
<p><strong><span data-ttu-id="f862a-156">Applicabile a partire da App-V 5,0 SP3 </strong> : se specifichi <strong> "\*" </strong> per la versione del pacchetto, il GUID della versione più recente del pacchetto disponibile viene inserito in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="f862a-156">Applicable starting in App-V 5.0 SP3</strong>: If you specify <strong>“\*”</strong> for the package version, the GUID of the latest available package version is dynamically inserted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-157">IsOptional</span><span class="sxs-lookup"><span data-stu-id="f862a-157">IsOptional</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="f862a-158">Applicabile a partire da App-V 5,0 SP3 </strong> : parametro che consente di rendere facoltativo un pacchetto all'interno del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-158">Applicable starting in App-V 5.0 SP3</strong>: Parameter that enables you to make a package optional within the connection group.</span></span> <span data-ttu-id="f862a-159">Le voci valide sono:</span><span class="sxs-lookup"><span data-stu-id="f862a-159">Valid entries are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="f862a-160">"true" </strong> : il pacchetto è facoltativo nel gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-160">“true”</strong> – package is optional in the connection group</span></span></p></li>
<li><p><strong><span data-ttu-id="f862a-161">"false" </strong> : il pacchetto è obbligatorio nel gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-161">“false”</strong> – package is required in the connection group</span></span></p></li>
</ul>
<p><span data-ttu-id="f862a-162">Informazioni <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)"> su come usare i pacchetti facoltativi nei gruppi di connessioni </a> .</span><span class="sxs-lookup"><span data-stu-id="f862a-162">See <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)">How to Use Optional Packages in Connection Groups</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a><span data-ttu-id="f862a-163">File XML del gruppo di connessioni di esempio App-V</span><span class="sxs-lookup"><span data-stu-id="f862a-163">App-V example connection group XML file</span></span>

<span data-ttu-id="f862a-164">Il file XML del gruppo di connessioni di esempio seguente mostra esempi di campi nelle tabelle precedenti ed evidenzia gli elementi nuovi che iniziano con App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="f862a-164">The following example connection group XML file shows examples of the fields in the previous tables and highlights the items that are new starting in App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup 
  xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"  
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"  
  DisplayName="Sample Connection Group">
  <appv:Packages>    
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="*"
      IsOptional="true"    
    />
    <appv:Package
      PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
      VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      IsOptional="false"    
    />  
  </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a><span data-ttu-id="f862a-165">App-V 5,0 tramite l'App-V 5,0 SP2 esempio di file XML del gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-165">App-V 5.0 through App-V 5.0 SP2 example connection group XML file</span></span>

<span data-ttu-id="f862a-166">Il file XML del gruppo di connessioni di esempio seguente si applica a App-V 5,0 tramite App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="f862a-166">The following example connection group XML file applies to App-V 5.0 through App-V 5.0 SP2.</span></span> <span data-ttu-id="f862a-167">Mostra alcuni esempi dei campi della tabella precedente, ma esclude le modifiche descritte in precedenza per App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="f862a-167">It shows examples of the fields in the previous table, but it excludes the changes described above for App-V 5.0 SP3.</span></span>

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup
  xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"
  DisplayName="Sample Connection Group">
  <appv:Packages>
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
    />
    <appv:Package
     PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
     VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
   />
 </appv:Packages>
<appv:AppConnectionGroup>
```

## <a href="" id="bkmk-config-pkg-priority-incg"></a><span data-ttu-id="f862a-168">Configurazione della priorità dei pacchetti in un gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="f862a-168">Configuring the priority of packages in a connection group</span></span>


<span data-ttu-id="f862a-169">La precedenza del pacchetto viene configurata con l'ordine di elenco dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f862a-169">Package precedence is configured using the package list order.</span></span> <span data-ttu-id="f862a-170">Il primo pacchetto nel documento ha la precedenza più alta.</span><span class="sxs-lookup"><span data-stu-id="f862a-170">The first package in the document has the highest precedence.</span></span> <span data-ttu-id="f862a-171">I pacchetti successivi nell'elenco hanno priorità decrescente.</span><span class="sxs-lookup"><span data-stu-id="f862a-171">Subsequent packages in the list have descending priority.</span></span>

<span data-ttu-id="f862a-172">La precedenza del pacchetto è la risoluzione per eventuali collisioni di risorse inevitabili durante l'inizializzazione dell'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="f862a-172">Package precedence is the resolution for otherwise inevitable resource collisions during virtual environment initialization.</span></span> <span data-ttu-id="f862a-173">Se ad esempio due pacchetti che si aprono nello stesso ambiente virtuale definiscono lo stesso valore DWORD del registro di sistema, il pacchetto con la precedenza più alta determina il valore impostato.</span><span class="sxs-lookup"><span data-stu-id="f862a-173">For example, if two packages that are opening in the same virtual environment define the same registry DWORD value, the package with the highest precedence determines the value that is set.</span></span>

<span data-ttu-id="f862a-174">È possibile usare il file del gruppo di connessioni per configurare ogni gruppo di connessioni usando i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f862a-174">You can use the connection group file to configure each connection group by using the following methods:</span></span>

-   <span data-ttu-id="f862a-175">Specificare le priorità di runtime per i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-175">Specify runtime priorities for connection groups.</span></span> <span data-ttu-id="f862a-176">Per modificare la priorità usando la console di gestione di App-V, fare clic sul gruppo connessione e quindi su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="f862a-176">To edit priority by using the App-V Management Console, click the connection group and then click **Edit**.</span></span>

    <span data-ttu-id="f862a-177">**Nota**  La priorità è obbligatoria solo se il pacchetto è associato a più di un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-177">**Note** Priority is required only if the package is associated with more than one connection group.</span></span>

     

-   <span data-ttu-id="f862a-178">Specificare la precedenza del pacchetto nel gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-178">Specify package precedence within the connection group.</span></span>

<span data-ttu-id="f862a-179">Il campo priorità è obbligatorio quando un'applicazione virtuale in uso viene avviata da una richiesta di applicazione nativa, ad esempio Esplora risorse di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f862a-179">The priority field is required when a running virtual application initiates from a native application request, for example, Microsoft Windows Explorer.</span></span> <span data-ttu-id="f862a-180">Il client App-V usa la priorità per determinare l'ambiente virtuale del gruppo di connessioni in cui deve essere eseguita l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f862a-180">The App-V client uses the priority to determine which connection group virtual environment the application should run in.</span></span> <span data-ttu-id="f862a-181">Questa situazione si verifica se un'applicazione virtuale fa parte di più gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-181">This situation occurs if a virtual application is part of multiple connection groups.</span></span>

<span data-ttu-id="f862a-182">Se un'applicazione virtuale viene aperta con un'altra applicazione virtuale, verrà usato l'ambiente virtuale dell'applicazione virtuale originale.</span><span class="sxs-lookup"><span data-stu-id="f862a-182">If a virtual application is opened using another virtual application the virtual environment of the original virtual application will be used.</span></span> <span data-ttu-id="f862a-183">Il campo priorità non viene usato in questo caso.</span><span class="sxs-lookup"><span data-stu-id="f862a-183">The priority field is not used in this case.</span></span>

**<span data-ttu-id="f862a-184">Esempio:</span><span class="sxs-lookup"><span data-stu-id="f862a-184">Example:</span></span>**

<span data-ttu-id="f862a-185">L'applicazione virtuale Microsoft Outlook è in uso nell'ambiente virtuale **XYZ**.</span><span class="sxs-lookup"><span data-stu-id="f862a-185">The virtual application Microsoft Outlook is running in virtual environment **XYZ**.</span></span> <span data-ttu-id="f862a-186">Quando si apre un documento di Microsoft Word allegato, viene aperta una versione virtualizzata di Microsoft Word nell'ambiente virtuale **XYZ**, indipendentemente dai gruppi di connessioni associati o dalle priorità di runtime virtualizzati di Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="f862a-186">When you open an attached Microsoft Word document, a virtualized version Microsoft Word opens in the virtual environment **XYZ**, regardless of the virtualized Microsoft Word’s associated connection groups or runtime priorities.</span></span>

## <a href="" id="bkmk-va-conn-configs"></a><span data-ttu-id="f862a-187">Configurazioni di connessione dell'applicazione virtuale supportate</span><span class="sxs-lookup"><span data-stu-id="f862a-187">Supported virtual application connection configurations</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f862a-188">Configurazione</span><span class="sxs-lookup"><span data-stu-id="f862a-188">Configuration</span></span></th>
<th align="left"><span data-ttu-id="f862a-189">Scenario di esempio</span><span class="sxs-lookup"><span data-stu-id="f862a-189">Example scenario</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-190">Un.</span><span class="sxs-lookup"><span data-stu-id="f862a-190">An.</span></span> <span data-ttu-id="f862a-191">file exe e plug-in (dll)</span><span class="sxs-lookup"><span data-stu-id="f862a-191">exe file and plug-in (.dll)</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f862a-192">Si vuole distribuire Microsoft Office a tutti gli utenti, ma distribuire un plug-in di Microsoft Excel solo a un sottoinsieme di utenti.</span><span class="sxs-lookup"><span data-stu-id="f862a-192">You want to distribute Microsoft Office to all users, but distribute a Microsoft Excel plug-in to only a subset of users.</span></span></p></li>
<li><p><span data-ttu-id="f862a-193">Abilitare il gruppo di connessioni per gli utenti appropriati.</span><span class="sxs-lookup"><span data-stu-id="f862a-193">Enable the connection group for the appropriate users.</span></span></p></li>
<li><p><span data-ttu-id="f862a-194">Aggiornare ogni pacchetto singolarmente, come richiesto.</span><span class="sxs-lookup"><span data-stu-id="f862a-194">Update each package individually as required.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f862a-195">Un.</span><span class="sxs-lookup"><span data-stu-id="f862a-195">An.</span></span> <span data-ttu-id="f862a-196">file exe e un'applicazione middleware</span><span class="sxs-lookup"><span data-stu-id="f862a-196">exe file and a middleware application</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f862a-197">L'applicazione richiede un'applicazione middleware o diverse applicazioni che dipendono dalla stessa versione di runtime di middleware.</span><span class="sxs-lookup"><span data-stu-id="f862a-197">You have an application requires a middleware application, or several applications that all depend on the same middleware runtime version.</span></span></p></li>
<li><p><span data-ttu-id="f862a-198">Tutti i computer che richiedono una o più applicazioni ricevono i gruppi di connessioni con l'applicazione e il runtime dell'applicazione middleware.</span><span class="sxs-lookup"><span data-stu-id="f862a-198">All computers that require one or more of the applications receive the connection groups with the application and middleware application runtime.</span></span></p></li>
<li><p><span data-ttu-id="f862a-199">Puoi facoltativamente combinare più applicazioni middleware in un singolo gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-199">You can optionally combine multiple middleware applications into a single connection group.</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f862a-200">Esempio</span><span class="sxs-lookup"><span data-stu-id="f862a-200">Example</span></span></th>
<th align="left"><span data-ttu-id="f862a-201">Descrizione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f862a-201">Example description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-202">Gruppo connessione applicazione virtuale per la divisione finanziaria</span><span class="sxs-lookup"><span data-stu-id="f862a-202">Virtual application connection group for the financial division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f862a-203">Applicazione middleware 1</span><span class="sxs-lookup"><span data-stu-id="f862a-203">Middleware application 1</span></span></p></li>
<li><p><span data-ttu-id="f862a-204">Applicazione middleware 2</span><span class="sxs-lookup"><span data-stu-id="f862a-204">Middleware application 2</span></span></p></li>
<li><p><span data-ttu-id="f862a-205">Applicazione middleware 3</span><span class="sxs-lookup"><span data-stu-id="f862a-205">Middleware application 3</span></span></p></li>
<li><p><span data-ttu-id="f862a-206">Middleware Application runtime</span><span class="sxs-lookup"><span data-stu-id="f862a-206">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f862a-207">Gruppo connessione applicazione virtuale per la divisione HR</span><span class="sxs-lookup"><span data-stu-id="f862a-207">Virtual application connection group for HR division</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="f862a-208">Applicazione middleware 5</span><span class="sxs-lookup"><span data-stu-id="f862a-208">Middleware application 5</span></span></p></li>
<li><p><span data-ttu-id="f862a-209">Applicazione middleware 6</span><span class="sxs-lookup"><span data-stu-id="f862a-209">Middleware application 6</span></span></p></li>
<li><p><span data-ttu-id="f862a-210">Middleware Application runtime</span><span class="sxs-lookup"><span data-stu-id="f862a-210">Middleware application runtime</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f862a-211">Un.</span><span class="sxs-lookup"><span data-stu-id="f862a-211">An.</span></span> <span data-ttu-id="f862a-212">file exe e file exe</span><span class="sxs-lookup"><span data-stu-id="f862a-212">exe file and an .exe file</span></span></p></td>
<td align="left"><p><span data-ttu-id="f862a-213">Si ha un'applicazione che si basa su un'altra applicazione e si vuole evitare che i pacchetti vengano separati per l'efficienza operativa, le restrizioni delle licenze o le sequenze temporali di implementazione.</span><span class="sxs-lookup"><span data-stu-id="f862a-213">You have an application that relies on another application, and you want to keep the packages separate for operational efficiencies, licensing restrictions, or rollout timelines.</span></span></p>
<p><strong><span data-ttu-id="f862a-214">Esempio:</span><span class="sxs-lookup"><span data-stu-id="f862a-214">Example:</span></span></strong></p>
<p><span data-ttu-id="f862a-215">Se si distribuisce Microsoft Lync 2010, è possibile usare tre pacchetti:</span><span class="sxs-lookup"><span data-stu-id="f862a-215">If you are deploying Microsoft Lync 2010, you can use three packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="f862a-216">Microsoft Office2010</span><span class="sxs-lookup"><span data-stu-id="f862a-216">Microsoft Office2010</span></span></p></li>
<li><p><span data-ttu-id="f862a-217">Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="f862a-217">Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="f862a-218">Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="f862a-218">Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="f862a-219">È possibile gestire la distribuzione usando i gruppi di connessioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f862a-219">You can manage the deployment using the following connection groups:</span></span></p>
<ul>
<li><p><span data-ttu-id="f862a-220">Microsoft Office2010 e Microsoft Communicator2007</span><span class="sxs-lookup"><span data-stu-id="f862a-220">Microsoft Office2010 and Microsoft Communicator2007</span></span></p></li>
<li><p><span data-ttu-id="f862a-221">Microsoft Office2010 e Microsoft Lync2010</span><span class="sxs-lookup"><span data-stu-id="f862a-221">Microsoft Office2010 and Microsoft Lync2010</span></span></p></li>
</ul>
<p><span data-ttu-id="f862a-222">Al termine della distribuzione, è possibile creare un singolo nuovo pacchetto Microsoft Office2010 + Microsoft Lync2010 oppure conservarlo e mantenerlo come pacchetti separati e distribuirlo usando un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="f862a-222">When the deployment has completed, you can either create a single new Microsoft Office2010 + Microsoft Lync2010 package, or keep and maintain them as separate packages and deploy them by using a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="f862a-223">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f862a-223">Related topics</span></span>


[<span data-ttu-id="f862a-224">Gestione dei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="f862a-224">Managing Connection Groups</span></span>](managing-connection-groups51.md)

 

 





