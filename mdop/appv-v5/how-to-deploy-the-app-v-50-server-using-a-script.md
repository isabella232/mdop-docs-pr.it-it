---
title: Come distribuire il server App-V 5.0 con uno script
description: Come distribuire il server App-V 5.0 con uno script
author: dansimp
ms.assetid: b91a35c8-df9e-4065-9187-abafbe565b84
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: aeb16d166fe7b1c4bb418c212024c49f6b151b94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805524"
---
# <span data-ttu-id="0daef-103">Come distribuire il server App-V 5.0 con uno script</span><span class="sxs-lookup"><span data-stu-id="0daef-103">How to Deploy the App-V 5.0 Server Using a Script</span></span>


<span data-ttu-id="0daef-104">Per completare la configurazione del server **appv\_server\_setup.exe** con successo tramite la riga di comando, è necessario specificare e combinare più parametri.</span><span class="sxs-lookup"><span data-stu-id="0daef-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

<span data-ttu-id="0daef-105">Usare le tabelle seguenti per altre informazioni sull'installazione del server App-V 5,0 tramite la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0daef-105">Use the following tables for more information about installing the App-V 5.0 server using the command line.</span></span>

>[!NOTE]
> <span data-ttu-id="0daef-106">È anche possibile accedere alle informazioni nelle tabelle seguenti tramite la riga di comando digitando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="0daef-106">The information in the following tables can also be accessed using the command line by typing the following command:</span></span>
>```
> appv\_server\_setup.exe /?
>```

## <span data-ttu-id="0daef-107">Parametri ed esempi comuni</span><span class="sxs-lookup"><span data-stu-id="0daef-107">Common parameters and Examples</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-108">Per installare il server di gestione e il database di gestione in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-108">To Install the Management server and Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-109">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-109">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-110">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-111">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-112">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-113">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-114">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-116">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-117">Per usare un'istanza personalizzata di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-117">To use a custom instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-118">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-118">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-119">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-119">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-120">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-120">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-121">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-121">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-122">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-122">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-123">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-124">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-124">/MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-125">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-125">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-126">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-126">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-127">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-127">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="0daef-128">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="0daef-128">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="0daef-129">/MANAGEMENT_WEBSITE_NAME = "servizio di gestione di Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="0daef-129">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="0daef-130">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="0daef-130">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="0daef-131">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-131">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="0daef-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-132">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-133">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="0daef-133">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
     
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-134">Per installare il server di gestione usando un database di gestione esistente in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-134">To Install the Management server using an existing Management database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-135">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-135">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-136">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-136">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-137">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-137">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-138">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-138">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-139">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-139">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-140">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-141">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-142">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-142">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-143">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-143">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-144">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-144">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-145">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-145">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-146">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-146">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-147">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-147">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-148">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-149">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-150">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-150">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-151">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-151">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-152">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-152">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-153">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-153">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="0daef-154">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="0daef-154">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="0daef-155">/MANAGEMENT_WEBSITE_NAME = "servizio di gestione di Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="0daef-155">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="0daef-156">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="0daef-156">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="0daef-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-157">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="0daef-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-158">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-159">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="0daef-159">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>  

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-160">Per installare il server di gestione usando un database di gestione esistente in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="0daef-160">To install the Management server using an existing Management database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-161">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-161">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-162">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-162">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-163">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-163">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-164">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-164">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-165">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-165">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-166">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-167">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-168">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-168">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-169">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-169">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-170">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-170">/MANAGEMENT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-171">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-171">/MANAGEMENT_ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-172">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-172">/MANAGEMENT_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-173">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-173">/MANAGEMENT_WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-174">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-175">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-176">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-176">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-177">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-177">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-178">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-178">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-179">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-179">/MANAGEMENT_SERVER</span></span></p>
    <p><span data-ttu-id="0daef-180">/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</span><span class="sxs-lookup"><span data-stu-id="0daef-180">/MANAGEMENT_ADMINACCOUNT=”Domain\AdminGroup”</span></span></p>
    <p><span data-ttu-id="0daef-181">/MANAGEMENT_WEBSITE_NAME = "servizio di gestione di Microsoft AppV"</span><span class="sxs-lookup"><span data-stu-id="0daef-181">/MANAGEMENT_WEBSITE_NAME=”Microsoft AppV Management Service”</span></span></p>
    <p><span data-ttu-id="0daef-182">/MANAGEMENT_WEBSITE_PORT = "8080"</span><span class="sxs-lookup"><span data-stu-id="0daef-182">/MANAGEMENT_WEBSITE_PORT=”8080”</span></span></p>
    <p><span data-ttu-id="0daef-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. DomainName"</span><span class="sxs-lookup"><span data-stu-id="0daef-183">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME=”SqlServermachine.domainName”</span></span></p>
    <p><span data-ttu-id="0daef-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-184">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE =”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-185">/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="0daef-185">/EXISTING_MANAGEMENT_DB_NAME =”AppVManagement”</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-186">Per installare il database di gestione e il server di gestione nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="0daef-186">To Install the Management database and the Management Server on the same computer.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-187">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-187">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-188">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-188">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-189">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-190">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-190">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-191">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-192">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-193">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-193">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-194">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-194">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-195">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-196">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-196">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-197">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-198">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-199">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-199">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-200">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-200">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-201">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-201">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="0daef-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-202">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-203">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="0daef-203">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="0daef-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-204">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="0daef-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="0daef-205">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-206">Per installare il database di gestione in un computer diverso da quello del server di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-206">To install the Management database on a different computer than the Management server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-207">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-207">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-208">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-208">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-209">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-210">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-210">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-211">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-212">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-213">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-213">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-214">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-214">/DB_PREDEPLOY_MANAGEMENT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-215">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-216">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-216">/MANAGEMENT_DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-217">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-218">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-219">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-219">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-220">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-220">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-221">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-221">/DB_PREDEPLOY_MANAGEMENT</span></span></p>
    <p><span data-ttu-id="0daef-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-222">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-223">/MANAGEMENT_DB_NAME = "AppVManagement"</span><span class="sxs-lookup"><span data-stu-id="0daef-223">/MANAGEMENT_DB_NAME=”AppVManagement”</span></span></p>
    <p><span data-ttu-id="0daef-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="0daef-224">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="0daef-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="0daef-225">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-226">Per installare il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0daef-226">To Install the publishing server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-227">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-227">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-228">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-228">/PUBLISHING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-229">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-229">/PUBLISHING_MGT_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-230">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-230">/PUBLISHING_WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-231">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-231">/PUBLISHING_WEBSITE_PORT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-232">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-232">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-233">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-233">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-234">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-234">/PUBLISHING_SERVER</span></span></p>
    <p><span data-ttu-id="0daef-235">/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</span><span class="sxs-lookup"><span data-stu-id="0daef-235">/PUBLISHING_MGT_SERVER=”http://ManagementServerName:ManagementPort”</span></span></p>
    <p><span data-ttu-id="0daef-236">/PUBLISHING_WEBSITE_NAME = "Microsoft AppV Publishing Service"</span><span class="sxs-lookup"><span data-stu-id="0daef-236">/PUBLISHING_WEBSITE_NAME=”Microsoft AppV Publishing Service”</span></span></p>
    <p><span data-ttu-id="0daef-237">/PUBLISHING_WEBSITE_PORT = "8081"</span><span class="sxs-lookup"><span data-stu-id="0daef-237">/PUBLISHING_WEBSITE_PORT=”8081”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-238">Per installare il server di report e il database di report in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-238">To Install the Reporting server and Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-239">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-239">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-240">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-240">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-241">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-241">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-242">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-242">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-243">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-243">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="0daef-244">_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-244">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-245">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-245">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-246">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-246">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-247">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-247">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-248">_ADMINACCOUNT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-248">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-249">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-249">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-250">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-250">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-251">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-251">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="0daef-252">_DB_CUSTOM_SQLINSTANCE/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-252">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-253">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-253">/REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-254">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-254">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-255">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-255">/appv_server_setup.exe /QUIET</span></span></p></li>
    <li><p><span data-ttu-id="0daef-256">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-256">/REPORTING_SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-257">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="0daef-257">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p></li>
    <li><p><span data-ttu-id="0daef-258">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="0daef-258">/REPORTING_WEBSITE_PORT=”8082”</span></span></p></li>
    <li><p><span data-ttu-id="0daef-259">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-259">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="0daef-260">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-260">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p></li>
    <li><p><span data-ttu-id="0daef-261">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="0daef-261">/REPORTING_DB_NAME=”AppVReporting”</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-262">Per installare il server di report e usare un database di report esistente in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-262">To Install the Reporting server and using an existing Reporting database on a local machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-263">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-263">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-264">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-264">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-265">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-265">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-266">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-266">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-267">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-268">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-269">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-269">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-270">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-270">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-271">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-271">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-272">_ADMINACCOUNT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-272">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-273">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-273">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-274">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-274">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-275">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-276">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-277">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-277">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-278">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-278">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-279">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-279">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-280">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-280">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="0daef-281">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="0daef-281">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="0daef-282">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="0daef-282">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="0daef-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-283">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="0daef-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-284">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-285">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="0daef-285">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-286">Per installare il server di report usando un database di report esistente in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="0daef-286">To Install the Reporting server using an existing Reporting database on a remote machine.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-287">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-287">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-288">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-288">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-289">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-289">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-290">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-290">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-291">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-292">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-293">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-293">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-294">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-294">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-295">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-295">/REPORTING _SERVER</span></span></p></li>
    <li><p><span data-ttu-id="0daef-296">_ADMINACCOUNT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-296">/REPORTING _ADMINACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-297">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-297">/REPORTING _WEBSITE_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-298">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-298">/REPORTING _WEBSITE_PORT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-299">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-300">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-301">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-301">/EXISTING_REPORTING _DB_NAME</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-302">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-302">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-303">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-303">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-304">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-304">/REPORTING_SERVER</span></span></p>
    <p><span data-ttu-id="0daef-305">/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</span><span class="sxs-lookup"><span data-stu-id="0daef-305">/REPORTING_WEBSITE_NAME=”Microsoft AppV Reporting Service”</span></span></p>
    <p><span data-ttu-id="0daef-306">/REPORTING_WEBSITE_PORT = "8082"</span><span class="sxs-lookup"><span data-stu-id="0daef-306">/REPORTING_WEBSITE_PORT=”8082”</span></span></p>
    <p><span data-ttu-id="0daef-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. DomainName"</span><span class="sxs-lookup"><span data-stu-id="0daef-307">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME=”SqlServerMachine.DomainName”</span></span></p>
    <p><span data-ttu-id="0daef-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-308">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-309">/EXITING_REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="0daef-309">/EXITING_REPORTING_DB_NAME=”AppVReporting”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-310">Per installare il database delle relazioni nello stesso computer del server di report.</span><span class="sxs-lookup"><span data-stu-id="0daef-310">To install the Reporting database on the same computer as the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-311">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-311">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-312">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-312">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="0daef-313">_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-313">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-314">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-314">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-315">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-316">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-317">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-317">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-318">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-318">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="0daef-319">_DB_CUSTOM_SQLINSTANCE/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-319">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-320">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-320">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-321">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></li>
    <li><p><span data-ttu-id="0daef-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-322">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-323">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-323">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-324">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-324">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-325">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-325">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="0daef-326">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-326">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-327">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="0daef-327">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="0daef-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-328">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p>
    <p><span data-ttu-id="0daef-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="0daef-329">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-330">Per installare il database delle relazioni in un computer diverso da quello del server dei report.</span><span class="sxs-lookup"><span data-stu-id="0daef-330">To install the Reporting database on a different computer than the Reporting server.</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-331">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0daef-331">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-332">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-332">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="0daef-333">_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-333">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-334">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-334">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-335">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-336">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-337">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</span><span class="sxs-lookup"><span data-stu-id="0daef-337">To use a custom instance of Microsoft SQL Server, use these parameters:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="0daef-338">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-338">/DB_PREDEPLOY_REPORTING</span></span></p></li>
    <li><p><span data-ttu-id="0daef-339">_DB_CUSTOM_SQLINSTANCE/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-339">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span></p></li>
    <li><p><span data-ttu-id="0daef-340">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-340">/REPORTING _DB_NAME</span></span></p></li>
    <li><p><span data-ttu-id="0daef-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-341">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></li>
    <li><p><span data-ttu-id="0daef-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-342">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></li>
    </ul>
    <p><span data-ttu-id="0daef-343">Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="0daef-343">Using a custom instance of Microsoft SQL Server example:</span></span></p>
    <p><span data-ttu-id="0daef-344">/appv_server_setup.exe/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-344">/appv_server_setup.exe /QUIET</span></span></p>
    <p><span data-ttu-id="0daef-345">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-345">/DB_PREDEPLOY_REPORTING</span></span></p>
    <p><span data-ttu-id="0daef-346">/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</span><span class="sxs-lookup"><span data-stu-id="0daef-346">/REPORTING_DB_CUSTOM_SQLINSTANCE=”SqlInstanceName”</span></span></p>
    <p><span data-ttu-id="0daef-347">/REPORTING_DB_NAME = "AppVReporting"</span><span class="sxs-lookup"><span data-stu-id="0daef-347">/REPORTING_DB_NAME=”AppVReporting”</span></span></p>
    <p><span data-ttu-id="0daef-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</span><span class="sxs-lookup"><span data-stu-id="0daef-348">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT=”Domain\MachineAccount”</span></span></p>
    <p><span data-ttu-id="0daef-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</span><span class="sxs-lookup"><span data-stu-id="0daef-349">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT=”Domain\InstallAdminAccount”</span></span></p></td>
    </tr>
    </tbody>
    </table>

## <span data-ttu-id="0daef-350">Definizioni di parametri</span><span class="sxs-lookup"><span data-stu-id="0daef-350">Parameter Definitions</span></span>

### <span data-ttu-id="0daef-351">Parametri generali</span><span class="sxs-lookup"><span data-stu-id="0daef-351">General Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-352">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-352">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-353">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-353">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-354">/QUIET</span><span class="sxs-lookup"><span data-stu-id="0daef-354">/QUIET</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-355">Specifica l'installazione silenziosa.</span><span class="sxs-lookup"><span data-stu-id="0daef-355">Specifies silent install.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-356">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="0daef-356">/UNINSTALL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-357">Specifica una disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="0daef-357">Specifies an uninstall.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-358">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="0daef-358">/LAYOUT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-359">Specifica l'azione del layout.</span><span class="sxs-lookup"><span data-stu-id="0daef-359">Specifies layout action.</span></span> <span data-ttu-id="0daef-360">Questo estrae i file di MSI e script in una cartella senza installare effettivamente il prodotto.</span><span class="sxs-lookup"><span data-stu-id="0daef-360">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="0daef-361">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="0daef-361">No value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-362">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="0daef-362">/LAYOUTDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-363">Specifica la directory del layout.</span><span class="sxs-lookup"><span data-stu-id="0daef-363">Specifies the layout directory.</span></span> <span data-ttu-id="0daef-364">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-364">Takes a string.</span></span> <span data-ttu-id="0daef-365">Ad esempio,/LAYOUTDIR = "C:\Application Virtualization Server"</span><span class="sxs-lookup"><span data-stu-id="0daef-365">For example, /LAYOUTDIR=”C:\Application Virtualization Server”</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-366">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="0daef-366">/INSTALLDIR</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-367">Specifica la directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="0daef-367">Specifies the installation directory.</span></span> <span data-ttu-id="0daef-368">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-368">Takes a string.</span></span> <span data-ttu-id="0daef-369">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-369">E.g.</span></span> <span data-ttu-id="0daef-370">/INSTALLDIR = "c: programmi Files\Application Virtualization\Server"</span><span class="sxs-lookup"><span data-stu-id="0daef-370">/INSTALLDIR=”C:\Program Files\Application Virtualization\Server”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-371">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="0daef-371">/MUOPTIN</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-372">Abilita Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="0daef-372">Enables Microsoft Update.</span></span> <span data-ttu-id="0daef-373">Nessun valore previsto</span><span class="sxs-lookup"><span data-stu-id="0daef-373">No value is expected</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-374">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="0daef-374">/ACCEPTEULA</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-375">Accetta il contratto di licenza.</span><span class="sxs-lookup"><span data-stu-id="0daef-375">Accepts the license agreement.</span></span> <span data-ttu-id="0daef-376">Questa operazione è necessaria per un'installazione automatica.</span><span class="sxs-lookup"><span data-stu-id="0daef-376">This is required for an unattended installation.</span></span> <span data-ttu-id="0daef-377">Esempio di utilizzo: <strong> /AcceptEula </strong> o <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-377">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="0daef-378">Parametri di installazione del server di gestione</span><span class="sxs-lookup"><span data-stu-id="0daef-378">Management Server Installation Parameters</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-379">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-379">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-380">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-380">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-381">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-381">/MANAGEMENT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-382">Specifica che verrà installato il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-382">Specifies that the management server will be installed.</span></span> <span data-ttu-id="0daef-383">Nessun valore previsto</span><span class="sxs-lookup"><span data-stu-id="0daef-383">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-384">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-384">/MANAGEMENT_ADMINACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-385">Specifica l'account a cui sarà consentito l'accesso di amministratore al server di gestione questo account può essere un singolo account utente o un gruppo.</span><span class="sxs-lookup"><span data-stu-id="0daef-385">Specifies the account that will be allowed to Administrator access to the management server This account can be an individual user account or a group.</span></span> <span data-ttu-id="0daef-386">Esempio di utilizzo: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-386">Example usage: <strong>/MANAGEMENT_ADMINACCOUNT=”mydomain\admin”</strong>.</span></span> <span data-ttu-id="0daef-387">Se <strong> /MANAGEMENT_SERVER </strong> non è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="0daef-387">If <strong>/MANAGEMENT_SERVER</strong> is not specified, this will be ignored.</span></span> <span data-ttu-id="0daef-388">Specifica l'account a cui sarà consentito l'accesso di amministratore al server di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-388">Specifies the account that will be allowed to Administrator access to the management server.</span></span> <span data-ttu-id="0daef-389">Può trattarsi di un account utente o di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="0daef-389">This can be a user account or a group.</span></span> <span data-ttu-id="0daef-390">Ad esempio, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-390">For example, <strong>/MANAGEMENT_ADMINACCOUNT=&quot;mydomain\admin&quot;</strong>.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-391">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-391">/MANAGEMENT_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-392">Specifica il nome del sito Web che verrà creato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-392">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="0daef-393">Ad esempio,/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"</span><span class="sxs-lookup"><span data-stu-id="0daef-393">For example, /MANAGEMENT_WEBSITE_NAME=”Microsoft App-V Management Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-394">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-394">MANAGEMENT_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-395">Specifica il numero di porta che verrà usato dal servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-395">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="0daef-396">Ad esempio,/MANAGEMENT_WEBSITE_PORT = 82.</span><span class="sxs-lookup"><span data-stu-id="0daef-396">For example, /MANAGEMENT_WEBSITE_PORT=82.</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="0daef-397">Parametri per il database del server di gestione</span><span class="sxs-lookup"><span data-stu-id="0daef-397">Parameters for the Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-398">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-398">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-399">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-399">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-400">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="0daef-400">/DB_PREDEPLOY_MANAGEMENT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-401">Specifica che verrà installato il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-401">Specifies that the management database will be installed.</span></span> <span data-ttu-id="0daef-402">Per completare l'installazione, è necessario disporre di autorizzazioni di database sufficienti.</span><span class="sxs-lookup"><span data-stu-id="0daef-402">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="0daef-403">Nessun valore previsto</span><span class="sxs-lookup"><span data-stu-id="0daef-403">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-404">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-405">Indica che deve essere usata l'istanza SQL predefinita.</span><span class="sxs-lookup"><span data-stu-id="0daef-405">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="0daef-406">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="0daef-406">No value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-407">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-408">Specifica il nome dell'istanza SQL personalizzata che deve essere usata per creare un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="0daef-408">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="0daef-409">Esempio di utilizzo: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "SqlServer" </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-409">Example usage: <strong>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”MYSQLSERVER”</strong>.</span></span> <span data-ttu-id="0daef-410">Se/DB_PREDEPLOY_MANAGEMENT non è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="0daef-410">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-411">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-411">/MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-412">Specifica il nome del nuovo database di gestione che deve essere creato.</span><span class="sxs-lookup"><span data-stu-id="0daef-412">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="0daef-413">Esempio di utilizzo: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-413">Example usage: <strong>/MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="0daef-414">Se/DB_PREDEPLOY_MANAGEMENT non è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="0daef-414">If /DB_PREDEPLOY_MANAGEMENT is not specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-415">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-416">Indica se il server di gestione che accederà al database viene installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-416">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="0daef-417">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="0daef-417">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-418">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-419">Specifica l'account del computer remoto in cui verrà installato il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-419">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="0daef-420">Esempio di utilizzo: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\computername"</span><span class="sxs-lookup"><span data-stu-id="0daef-420">Example usage: <strong>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT=”domain\computername”</span></span></strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-421">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-422">Indica l'account di amministratore che verrà usato per installare il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="0daef-422">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="0daef-423">Esempio di utilizzo: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "dominio\alias"</span><span class="sxs-lookup"><span data-stu-id="0daef-423">Example usage: <strong>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT =”domain\alias”</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="0daef-424">Parametri per l'installazione del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="0daef-424">Parameters for Installing Publishing Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-425">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-425">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-426">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-426">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-427">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-427">/PUBLISHING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-428">Specifica che verrà installato il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0daef-428">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="0daef-429">Nessun valore previsto</span><span class="sxs-lookup"><span data-stu-id="0daef-429">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-430">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-430">/PUBLISHING_MGT_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-431">Specifica l'URL del servizio di gestione a cui il server di pubblicazione si connette.</span><span class="sxs-lookup"><span data-stu-id="0daef-431">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="0daef-432">Esempio di utilizzo: <strong> http:// &lt; Management Server Name &gt; : numero di porta del server di &lt; gestione &gt; </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-432">Example usage: <strong>http://&lt;management server name&gt;:&lt;Management server port number&gt;</strong>.</span></span> <span data-ttu-id="0daef-433">Se/PUBLISHING_SERVER non viene usato, questo parametro verrà ignorato</span><span class="sxs-lookup"><span data-stu-id="0daef-433">If /PUBLISHING_SERVER is not used, this parameter will be ignored</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-434">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-434">/PUBLISHING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-435">Specifica il nome del sito Web che verrà creato per il servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0daef-435">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="0daef-436">Ad esempio,/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"</span><span class="sxs-lookup"><span data-stu-id="0daef-436">For example, /PUBLISHING_WEBSITE_NAME=”Microsoft App-V Publishing Service”</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-437">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-437">/PUBLISHING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-438">Specifica il numero di porta usato dal servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="0daef-438">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="0daef-439">Ad esempio,/PUBLISHING_WEBSITE_PORT = 83</span><span class="sxs-lookup"><span data-stu-id="0daef-439">For example, /PUBLISHING_WEBSITE_PORT=83</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="0daef-440">Parametri per Reporting Server</span><span class="sxs-lookup"><span data-stu-id="0daef-440">Parameters for Reporting Server</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-441">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-441">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-442">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-442">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-443">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="0daef-443">/REPORTING_SERVER</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-444">Specifica che verrà installato il server di report.</span><span class="sxs-lookup"><span data-stu-id="0daef-444">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="0daef-445">Nessun valore previsto</span><span class="sxs-lookup"><span data-stu-id="0daef-445">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-446">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-446">/REPORTING_WEBSITE_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-447">Specifica il nome del sito Web che verrà creato per il servizio di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="0daef-447">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="0daef-448">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-448">E.g.</span></span> <span data-ttu-id="0daef-449">/REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-449">/REPORTING_WEBSITE_NAME=&quot;Microsoft App-V ReportingService&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-450">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="0daef-450">/REPORTING_WEBSITE_PORT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-451">Specifica il numero di porta che verrà usato dal servizio Reporting.</span><span class="sxs-lookup"><span data-stu-id="0daef-451">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="0daef-452">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-452">E.g.</span></span> <span data-ttu-id="0daef-453">/REPORTING_WEBSITE_PORT = 82</span><span class="sxs-lookup"><span data-stu-id="0daef-453">/REPORTING_WEBSITE_PORT=82</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

### <span data-ttu-id="0daef-454">Parametri per l'uso di un database del server di report esistente</span><span class="sxs-lookup"><span data-stu-id="0daef-454">Parameters for using an Existing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-455">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-455">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-456">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-456">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-457">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-458">Indica che Microsoft SQL Server è installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-458">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="0daef-459">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="0daef-459">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-460">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-461">Specifica il nome del computer remoto in cui è installato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0daef-461">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="0daef-462">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-462">Takes a string.</span></span> <span data-ttu-id="0daef-463">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-463">E.g.</span></span> <span data-ttu-id="0daef-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-464">/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-465">/EXISTING_ REPORTING <em> DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-465">/EXISTING_ REPORTING <em>DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-466">Indica che deve essere usata l'istanza SQL predefinita.</span><span class="sxs-lookup"><span data-stu-id="0daef-466">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="0daef-467">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="0daef-467">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-468"></em>REPORTING_DB_CUSTOM_SQLINSTANCE/existing</span><span class="sxs-lookup"><span data-stu-id="0daef-468">/EXISTING</em> REPORTING_DB_CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-469">Specifica il nome dell'istanza SQL personalizzata che deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="0daef-469">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="0daef-470">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-470">Takes a string.</span></span> <span data-ttu-id="0daef-471">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-471">E.g.</span></span> <span data-ttu-id="0daef-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; SqlServer&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-472">/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-473">/EXISTING_ REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-473">/EXISTING_ REPORTING _DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-474">Specifica il nome del database di report esistente che deve essere usato.</span><span class="sxs-lookup"><span data-stu-id="0daef-474">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="0daef-475">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-475">Takes a string.</span></span> <span data-ttu-id="0daef-476">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-476">E.g.</span></span> <span data-ttu-id="0daef-477">/EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-477">/EXISTING_REPORTING_DB_NAME=&quot;AppVReporting&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="0daef-478">Parametri per l'installazione del database di Reporting Server</span><span class="sxs-lookup"><span data-stu-id="0daef-478">Parameters for installing Reporting Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-479">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-479">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-480">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-480">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-481">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="0daef-481">/DB_PREDEPLOY_REPORTING</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-482">Specifica che verrà installato il database delle relazioni.</span><span class="sxs-lookup"><span data-stu-id="0daef-482">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="0daef-483">Per questa installazione sono necessarie le autorizzazioni di DBA.</span><span class="sxs-lookup"><span data-stu-id="0daef-483">DBA permissions are required for this installation.</span></span> <span data-ttu-id="0daef-484">Nessun valore previsto</span><span class="sxs-lookup"><span data-stu-id="0daef-484">No value is expected</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-485">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-486">Specifica il nome dell'istanza SQL personalizzata che deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="0daef-486">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="0daef-487">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-487">Takes a string.</span></span> <span data-ttu-id="0daef-488">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-488">E.g.</span></span> <span data-ttu-id="0daef-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; SqlServer&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-489">/REPORTING_DB_ CUSTOM_SQLINSTANCE=&quot;MYSQLSERVER&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-490">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-490">/REPORTING_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-491">Specifica il nome del nuovo database di report che deve essere creato.</span><span class="sxs-lookup"><span data-stu-id="0daef-491">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="0daef-492">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-492">Takes a string.</span></span> <span data-ttu-id="0daef-493">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-493">E.g.</span></span> <span data-ttu-id="0daef-494">/REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-494">/REPORTING_DB_NAME=&quot;AppVMgmtDB&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-495">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-496">Indica che il server di report che accederà al database verrà installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-496">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="0daef-497">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="0daef-497">Switch parameter so no value is expected.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-498">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-499">Specifica l'account del computer remoto in cui verrà installato il server di report.</span><span class="sxs-lookup"><span data-stu-id="0daef-499">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="0daef-500">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-500">Takes a string.</span></span> <span data-ttu-id="0daef-501">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-501">E.g.</span></span> <span data-ttu-id="0daef-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; Domain\computername&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-502">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot;domain\computername&quot;</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="0daef-503">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-504">Indica l'account di amministratore che verrà usato per installare App-V Reporting Server.</span><span class="sxs-lookup"><span data-stu-id="0daef-504">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="0daef-505">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-505">Takes a string.</span></span> <span data-ttu-id="0daef-506">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-506">E.g.</span></span> <span data-ttu-id="0daef-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; dominio\alias&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-507">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot;domain\alias&quot;</span></span></p></td>
    </tr>
    </tbody>
    </table>

### <span data-ttu-id="0daef-508">Parametri per l'uso di un database del server di gestione esistente</span><span class="sxs-lookup"><span data-stu-id="0daef-508">Parameters for using an existing Management Server Database</span></span>

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="0daef-509">Parametro</span><span class="sxs-lookup"><span data-stu-id="0daef-509">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="0daef-510">Informazioni</span><span class="sxs-lookup"><span data-stu-id="0daef-510">Information</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="0daef-511">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-512">Indica che il server SQL è installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="0daef-512">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="0daef-513">Parametro switch in modo che nessun valore sia previsto. Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="0daef-513">Switch parameter so no value is expected.If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-514">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-515">Specifica il nome del computer remoto in cui è installato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0daef-515">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="0daef-516">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="0daef-516">Takes a string.</span></span> <span data-ttu-id="0daef-517">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="0daef-517">E.g.</span></span> <span data-ttu-id="0daef-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</span><span class="sxs-lookup"><span data-stu-id="0daef-518">/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME=&quot;mycomputer1&quot;</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="0daef-519">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-520">Indica che deve essere usata l'istanza SQL predefinita.</span><span class="sxs-lookup"><span data-stu-id="0daef-520">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="0daef-521">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="0daef-521">Switch parameter so no value is expected.</span></span> <span data-ttu-id="0daef-522">Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="0daef-522">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="0daef-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="0daef-523">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-524">Specifica il nome dell'istanza di SQL personalizzata che verrà usata.</span><span class="sxs-lookup"><span data-stu-id="0daef-524">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="0daef-525">Esempio di utilizzo <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-525">Example usage <strong>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE=”AppVManagement”</strong>.</span></span> <span data-ttu-id="0daef-526">Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="0daef-526">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="0daef-527">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="0daef-527">/EXISTING_MANAGEMENT_DB_NAME</span></span></p></td>
    <td align="left"><p><span data-ttu-id="0daef-528">Specifica il nome del database di gestione esistente che deve essere usato.</span><span class="sxs-lookup"><span data-stu-id="0daef-528">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="0daef-529">Esempio di utilizzo: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> .</span><span class="sxs-lookup"><span data-stu-id="0daef-529">Example usage: <strong>/EXISTING_MANAGEMENT_DB_NAME=”AppVMgmtDB”</strong>.</span></span> <span data-ttu-id="0daef-530">Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="0daef-530">If /DB_PREDEPLOY_MANAGEMENT is specified, this will be ignored.</span></span></p>
    <p></p>
    <p><strong><span data-ttu-id="0daef-531">Hai un suggerimento per App-V </strong> ?</span><span class="sxs-lookup"><span data-stu-id="0daef-531">Got a suggestion for App-V</strong>?</span></span> <span data-ttu-id="0daef-532">Aggiungere o votare i suggerimenti <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> qui </a> .</span><span class="sxs-lookup"><span data-stu-id="0daef-532">Add or vote on suggestions <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)">here</a>.</span></span> <strong><span data-ttu-id="0daef-533">È stata emessa un'app-V </strong> e?</span><span class="sxs-lookup"><span data-stu-id="0daef-533">Got an App-V issu</strong>e?</span></span> <span data-ttu-id="0daef-534">Usare l' <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> App-V Forum TechNet </a> .</span><span class="sxs-lookup"><span data-stu-id="0daef-534">Use the <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)">App-V TechNet Forum</a>.</span></span></p></td>
</tr>
</tbody>
</table>
  

## <span data-ttu-id="0daef-535">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0daef-535">Related topics</span></span>

[<span data-ttu-id="0daef-536">Distribuzione del server App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="0daef-536">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

 

 





