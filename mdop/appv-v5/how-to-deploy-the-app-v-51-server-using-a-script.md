---
title: Come distribuire il server App-V 5.1 con uno script
description: Come distribuire il server App-V 5.1 con uno script
author: dansimp
ms.assetid: 15c33d7b-9b61-4dbc-8674-399bb33e5f7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/20/2020
ms.openlocfilehash: 579ca685f677aaaa4f5ebb6ac8d2969fdcbe2cd2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805494"
---
# <span data-ttu-id="5f770-103">Come distribuire il server App-V 5.1 con uno script</span><span class="sxs-lookup"><span data-stu-id="5f770-103">How to Deploy the App-V 5.1 Server Using a Script</span></span>

<span data-ttu-id="5f770-104">Per completare la configurazione del server **appv\_server\_setup.exe** con successo tramite la riga di comando, è necessario specificare e combinare più parametri.</span><span class="sxs-lookup"><span data-stu-id="5f770-104">In order to complete the **appv\_server\_setup.exe** Server setup successfully using the command line, you must specify and combine multiple parameters.</span></span>

## <span data-ttu-id="5f770-105">Installare il server App-V 5,1 usando uno script</span><span class="sxs-lookup"><span data-stu-id="5f770-105">Install the App-V 5.1 server using a script</span></span>

- <span data-ttu-id="5f770-106">Usare le informazioni seguenti sull'installazione del server App-V 5,1 tramite la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5f770-106">Use the following information about installing the App-V 5.1 server using the command line.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5f770-107">È anche possibile accedere alle informazioni nelle tabelle seguenti tramite la riga di comando digitando il comando seguente: **appv\_server\_setup.exe/?**.</span><span class="sxs-lookup"><span data-stu-id="5f770-107">The information in the following tables can also be accessed using the command line by typing the following command: **appv\_server\_setup.exe /?**.</span></span>

### <span data-ttu-id="5f770-108">Installare il server di gestione e il database di gestione in un computer locale</span><span class="sxs-lookup"><span data-stu-id="5f770-108">Install the Management server and Management database on a local machine</span></span>

<span data-ttu-id="5f770-109">I parametri seguenti sono validi sia per l'istanza predefinita che per quella personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-109">The following parameters are valid with both the default and custom instance of Microsoft SQL Server:</span></span>

- <span data-ttu-id="5f770-110">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-110">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="5f770-111">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-111">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="5f770-112">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-112">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-113">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-113">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-114">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="5f770-114">/DB_PREDEPLOY_MANAGEMENT</span></span>
- <span data-ttu-id="5f770-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-115">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="5f770-116">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-116">/MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="5f770-117">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f770-117">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### <span data-ttu-id="5f770-118">Installare il server di gestione usando un database di gestione esistente in un computer locale</span><span class="sxs-lookup"><span data-stu-id="5f770-118">Install the Management server using an existing Management database on a local machine</span></span>

<span data-ttu-id="5f770-119">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-119">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-120">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-120">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="5f770-121">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-121">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="5f770-122">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-122">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-123">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-123">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-124">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="5f770-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-125">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-126">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-126">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="5f770-127">Per usare un'istanza personalizzata di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-127">To use a custom instance of Microsoft SQL Server, use the following parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-128">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-128">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="5f770-129">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-129">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="5f770-130">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-130">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-131">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-131">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-132">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="5f770-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-133">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-134">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-134">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="5f770-135">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f770-135">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="5f770-136">Installare il server di gestione usando un database di gestione esistente in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="5f770-136">Install the Management server using an existing Management database on a remote machine</span></span>

<span data-ttu-id="5f770-137">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-137">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-138">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-138">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="5f770-139">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-139">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="5f770-140">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-140">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-141">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-141">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-142">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="5f770-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-143">/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-144">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-144">/EXISTING_MANAGEMENT_DB_NAME</span></span>

<span data-ttu-id="5f770-145">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-145">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-146">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-146">/MANAGEMENT_SERVER</span></span>
- <span data-ttu-id="5f770-147">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-147">/MANAGEMENT_ADMINACCOUNT</span></span>
- <span data-ttu-id="5f770-148">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-148">/MANAGEMENT_WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-149">/MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-149">/MANAGEMENT_WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-150">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="5f770-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-151">/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-152">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-152">/EXISTING_MANAGEMENT_DB_NAME</span></span>

**<span data-ttu-id="5f770-153">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-153">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### <span data-ttu-id="5f770-154">Installare il database di gestione e il server di gestione nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="5f770-154">Install the Management database and the Management Server on the same computer</span></span>

<span data-ttu-id="5f770-155">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-155">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-156">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="5f770-156">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="5f770-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-157">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-158">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-158">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="5f770-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-159">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="5f770-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-160">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="5f770-161">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-161">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-162">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="5f770-162">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="5f770-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-163">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-164">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-164">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="5f770-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-165">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="5f770-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-166">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="5f770-167">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f770-167">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="5f770-168">Installare il database di gestione in un computer diverso da quello del server di gestione</span><span class="sxs-lookup"><span data-stu-id="5f770-168">Install the Management database on a different computer than the Management server</span></span>

<span data-ttu-id="5f770-169">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-169">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-170">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="5f770-170">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="5f770-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-171">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-172">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-172">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="5f770-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-173">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="5f770-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-174">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="5f770-175">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-175">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-176">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="5f770-176">/DB_PREDEPLOY_MANAGEMENT</span></span>
- *<span data-ttu-id="5f770-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-177">/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-178">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-178">/MANAGEMENT_DB_NAME</span></span>
- <span data-ttu-id="5f770-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-179">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="5f770-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-180">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="5f770-181">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="5f770-181">Example: Using a custom instance of Microsoft SQL Server</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="5f770-182">Installare il server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="5f770-182">Install the publishing server</span></span>

<span data-ttu-id="5f770-183">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f770-183">To use the default instance of Microsoft SQL Server, use the following parameters:</span></span>

- <span data-ttu-id="5f770-184">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-184">/PUBLISHING_SERVER</span></span>
- <span data-ttu-id="5f770-185">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-185">/PUBLISHING_MGT_SERVER</span></span>
- <span data-ttu-id="5f770-186">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-186">/PUBLISHING_WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-187">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-187">/PUBLISHING_WEBSITE_PORT</span></span>

**<span data-ttu-id="5f770-188">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-188">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### <span data-ttu-id="5f770-189">Installare il server di report e il database di report in un computer locale</span><span class="sxs-lookup"><span data-stu-id="5f770-189">Install the Reporting server and Reporting database on a local machine</span></span>

<span data-ttu-id="5f770-190">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-190">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-191">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-191">/REPORTING _SERVER</span></span>
- <span data-ttu-id="5f770-192">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-192">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-193">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-193">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-194">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-194">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="5f770-195">_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-195">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-196">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-196">/REPORTING _DB_NAME</span></span>

<span data-ttu-id="5f770-197">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-197">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-198">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-198">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="5f770-199">_ADMINACCOUNT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-199">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="5f770-200">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-200">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-201">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-201">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-202">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-202">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="5f770-203">_DB_CUSTOM_SQLINSTANCE/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-203">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-204">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-204">/REPORTING _DB_NAME</span></span>

**<span data-ttu-id="5f770-205">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-205">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="5f770-206">Installare il server di report e usare un database di report esistente in un computer locale</span><span class="sxs-lookup"><span data-stu-id="5f770-206">Install the Reporting server and using an existing Reporting database on a local machine</span></span>

<span data-ttu-id="5f770-207">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-207">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-208">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-208">/REPORTING _SERVER</span></span>
- <span data-ttu-id="5f770-209">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-209">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-210">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-210">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-211">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="5f770-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-212">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-213">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-213">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="5f770-214">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-214">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-215">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-215">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="5f770-216">_ADMINACCOUNT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-216">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="5f770-217">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-217">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-218">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-218">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-219">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span>
- *<span data-ttu-id="5f770-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-220">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-221">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-221">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="5f770-222">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-222">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="5f770-223">Installare il server di report usando un database di report esistente in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="5f770-223">Install the Reporting server using an existing Reporting database on a remote machine</span></span>

<span data-ttu-id="5f770-224">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-224">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-225">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-225">/REPORTING _SERVER</span></span>
- <span data-ttu-id="5f770-226">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-226">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-227">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-227">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-228">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="5f770-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-229">/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-230">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-230">/EXISTING_REPORTING _DB_NAME</span></span>

<span data-ttu-id="5f770-231">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-231">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-232">_SERVER/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-232">/REPORTING _SERVER</span></span>
- *<span data-ttu-id="5f770-233">_ADMINACCOUNT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-233">/REPORTING _ADMINACCOUNT</span></span>*
- <span data-ttu-id="5f770-234">_WEBSITE_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-234">/REPORTING _WEBSITE_NAME</span></span>
- <span data-ttu-id="5f770-235">_WEBSITE_PORT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-235">/REPORTING _WEBSITE_PORT</span></span>
- <span data-ttu-id="5f770-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-236">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span>
- *<span data-ttu-id="5f770-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-237">/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-238">/EXISTING_REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-238">/EXISTING_REPORTING _DB_NAME</span></span>

**<span data-ttu-id="5f770-239">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-239">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### <span data-ttu-id="5f770-240">Installare il database delle relazioni nello stesso computer del server di report</span><span class="sxs-lookup"><span data-stu-id="5f770-240">Install the Reporting database on the same computer as the Reporting server</span></span>

<span data-ttu-id="5f770-241">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-241">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-242">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-242">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="5f770-243">_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-243">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>*
- <span data-ttu-id="5f770-244">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-244">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="5f770-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-245">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="5f770-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-246">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="5f770-247">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-247">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-248">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-248">/DB_PREDEPLOY_REPORTING</span></span>
- *<span data-ttu-id="5f770-249">_DB_CUSTOM_SQLINSTANCE/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-249">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>*
- <span data-ttu-id="5f770-250">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-250">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="5f770-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-251">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span>
- <span data-ttu-id="5f770-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-252">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="5f770-253">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-253">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="5f770-254">Installare il database di report in un computer diverso da quello del server di report</span><span class="sxs-lookup"><span data-stu-id="5f770-254">Install the Reporting database on a different computer than the Reporting server</span></span>

<span data-ttu-id="5f770-255">Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-255">To use the default instance of Microsoft SQL Server, use the following parameters (difference from custom instance in *italic*):</span></span>

- <span data-ttu-id="5f770-256">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-256">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="5f770-257">_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-257">/REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span>
- <span data-ttu-id="5f770-258">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-258">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="5f770-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-259">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="5f770-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-260">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

<span data-ttu-id="5f770-261">Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):</span><span class="sxs-lookup"><span data-stu-id="5f770-261">To use a custom instance of Microsoft SQL Server, use these parameters (difference from default instance in *italic*):</span></span>

- <span data-ttu-id="5f770-262">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-262">/DB_PREDEPLOY_REPORTING</span></span>
- <span data-ttu-id="5f770-263">_DB_CUSTOM_SQLINSTANCE/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-263">/REPORTING _DB_CUSTOM_SQLINSTANCE</span></span>
- <span data-ttu-id="5f770-264">_DB_NAME/REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-264">/REPORTING _DB_NAME</span></span>
- <span data-ttu-id="5f770-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-265">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span>
- <span data-ttu-id="5f770-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-266">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span>

**<span data-ttu-id="5f770-267">Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:</span><span class="sxs-lookup"><span data-stu-id="5f770-267">Example: Using a custom instance of Microsoft SQL Server:</span></span>**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### <span data-ttu-id="5f770-268">Definizioni di parametri</span><span class="sxs-lookup"><span data-stu-id="5f770-268">Parameter Definitions</span></span>

#### <span data-ttu-id="5f770-269">Parametri generali</span><span class="sxs-lookup"><span data-stu-id="5f770-269">General Parameters</span></span>

| <span data-ttu-id="5f770-270">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-270">Parameter</span></span> | <span data-ttu-id="5f770-271">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-271">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-272">/QUIET</span><span class="sxs-lookup"><span data-stu-id="5f770-272">/QUIET</span></span> | <span data-ttu-id="5f770-273">Specifica l'installazione silenziosa.</span><span class="sxs-lookup"><span data-stu-id="5f770-273">Specifies silent install.</span></span> |
| <span data-ttu-id="5f770-274">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="5f770-274">/UNINSTALL</span></span> | <span data-ttu-id="5f770-275">Specifica una disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="5f770-275">Specifies an uninstall.</span></span> |
| <span data-ttu-id="5f770-276">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="5f770-276">/LAYOUT</span></span> | <span data-ttu-id="5f770-277">Specifica l'azione del layout.</span><span class="sxs-lookup"><span data-stu-id="5f770-277">Specifies layout action.</span></span> <span data-ttu-id="5f770-278">Questo estrae i file di MSI e script in una cartella senza installare effettivamente il prodotto.</span><span class="sxs-lookup"><span data-stu-id="5f770-278">This extracts the MSIs and script files to a folder without actually installing the product.</span></span> <span data-ttu-id="5f770-279">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-279">No value is expected.</span></span> |
| <span data-ttu-id="5f770-280">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="5f770-280">/LAYOUTDIR</span></span> | <span data-ttu-id="5f770-281">Specifica la directory del layout.</span><span class="sxs-lookup"><span data-stu-id="5f770-281">Specifies the layout directory.</span></span> <span data-ttu-id="5f770-282">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-282">Takes a string.</span></span> <span data-ttu-id="5f770-283">Esempio di utilizzo: **/LAYOUTDIR = "C:\\Application Virtualization Server"**</span><span class="sxs-lookup"><span data-stu-id="5f770-283">Example usage: **/LAYOUTDIR="C:\\Application Virtualization Server"**</span></span> |
| <span data-ttu-id="5f770-284">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="5f770-284">/INSTALLDIR</span></span> | <span data-ttu-id="5f770-285">Specifica la directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="5f770-285">Specifies the installation directory.</span></span> <span data-ttu-id="5f770-286">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-286">Takes a string.</span></span> <span data-ttu-id="5f770-287">Esempio di utilizzo: **/INSTALLDIR = "C:\\Programmi Files\\Application Virtualization\\Server"**</span><span class="sxs-lookup"><span data-stu-id="5f770-287">Example usage: **/INSTALLDIR="C:\\Program Files\\Application Virtualization\\Server"**</span></span> |
| <span data-ttu-id="5f770-288">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="5f770-288">/MUOPTIN</span></span> | <span data-ttu-id="5f770-289">Abilita Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="5f770-289">Enables Microsoft Update.</span></span> <span data-ttu-id="5f770-290">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-290">No value is expected.</span></span> |
| <span data-ttu-id="5f770-291">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="5f770-291">/ACCEPTEULA</span></span> | <span data-ttu-id="5f770-292">Accetta il contratto di licenza.</span><span class="sxs-lookup"><span data-stu-id="5f770-292">Accepts the license agreement.</span></span> <span data-ttu-id="5f770-293">Questa operazione è necessaria per un'installazione automatica.</span><span class="sxs-lookup"><span data-stu-id="5f770-293">This is required for an unattended installation.</span></span> <span data-ttu-id="5f770-294">Esempio di utilizzo: **/AcceptEula** o **/ACCEPTEULA = 1**</span><span class="sxs-lookup"><span data-stu-id="5f770-294">Example usage: **/ACCEPTEULA** or **/ACCEPTEULA=1**</span></span> |

#### <span data-ttu-id="5f770-295">Parametri di installazione del server di gestione</span><span class="sxs-lookup"><span data-stu-id="5f770-295">Management Server Installation Parameters</span></span>

|<span data-ttu-id="5f770-296">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-296">Parameter</span></span> |<span data-ttu-id="5f770-297">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-297">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-298">/MANAGEMENT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-298">/MANAGEMENT_SERVER</span></span> | <span data-ttu-id="5f770-299">Specifica che verrà installato il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="5f770-299">Specifies that the management server will be installed.</span></span> <span data-ttu-id="5f770-300">Nessun valore previsto</span><span class="sxs-lookup"><span data-stu-id="5f770-300">No value is expected</span></span> |
| <span data-ttu-id="5f770-301">/MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-301">/MANAGEMENT_ADMINACCOUNT</span></span> | <span data-ttu-id="5f770-302">Specifica l'account a cui sarà consentito l'accesso di amministratore al server di gestione.</span><span class="sxs-lookup"><span data-stu-id="5f770-302">Specifies the account that will be allowed Administrator access to the management server.</span></span> <span data-ttu-id="5f770-303">Può trattarsi di un account utente o di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="5f770-303">This can be a user account or a group.</span></span> <span data-ttu-id="5f770-304">Esempio di utilizzo: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**.</span><span class="sxs-lookup"><span data-stu-id="5f770-304">Example usage: **/MANAGEMENT_ADMINACCOUNT="mydomain\\admin"**.</span></span> <span data-ttu-id="5f770-305">Se **/MANAGEMENT_SERVER** non è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-305">If **/MANAGEMENT_SERVER** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="5f770-306">/MANAGEMENT_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-306">/MANAGEMENT_WEBSITE_NAME</span></span> | <span data-ttu-id="5f770-307">Specifica il nome del sito Web che verrà creato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="5f770-307">Specifies name of the website that will be created for the management service.</span></span> <span data-ttu-id="5f770-308">Esempio di utilizzo: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"**</span><span class="sxs-lookup"><span data-stu-id="5f770-308">Example usage: **/MANAGEMENT_WEBSITE_NAME="Microsoft App-V Management Service"**</span></span> |
| <span data-ttu-id="5f770-309">MANAGEMENT_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-309">MANAGEMENT_WEBSITE_PORT</span></span> | <span data-ttu-id="5f770-310">Specifica il numero di porta che verrà usato dal servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="5f770-310">Specifies the port number that will be used by the management service will use.</span></span> <span data-ttu-id="5f770-311">Esempio di utilizzo: **/MANAGEMENT_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="5f770-311">Example usage: **/MANAGEMENT_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="5f770-312">Parametri per il database del server di gestione</span><span class="sxs-lookup"><span data-stu-id="5f770-312">Parameters for the Management Server Database</span></span>

| <span data-ttu-id="5f770-313">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-313">Parameter</span></span> | <span data-ttu-id="5f770-314">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-314">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-315">/DB_PREDEPLOY_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="5f770-315">/DB_PREDEPLOY_MANAGEMENT</span></span> | <span data-ttu-id="5f770-316">Specifica che verrà installato il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="5f770-316">Specifies that the management database will be installed.</span></span> <span data-ttu-id="5f770-317">Per completare l'installazione, è necessario disporre di autorizzazioni di database sufficienti.</span><span class="sxs-lookup"><span data-stu-id="5f770-317">You must have sufficient database permissions to complete this installation.</span></span> <span data-ttu-id="5f770-318">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-318">No value is expected.</span></span> |
| <span data-ttu-id="5f770-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-319">/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="5f770-320">Indica che deve essere usata l'istanza SQL predefinita.</span><span class="sxs-lookup"><span data-stu-id="5f770-320">Indicates that the default SQL instance should be used.</span></span> <span data-ttu-id="5f770-321">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-321">No value is expected.</span></span> |
| <span data-ttu-id="5f770-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-322">/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="5f770-323">Specifica il nome dell'istanza SQL personalizzata che deve essere usata per creare un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="5f770-323">Specifies the name of the custom SQL instance that should be used to create a new database.</span></span> <span data-ttu-id="5f770-324">Esempio di utilizzo: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "SqlServer"**.</span><span class="sxs-lookup"><span data-stu-id="5f770-324">Example usage: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**.</span></span> <span data-ttu-id="5f770-325">Se **/DB_PREDEPLOY_MANAGEMENT** non è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-325">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="5f770-326">/MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-326">/MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="5f770-327">Specifica il nome del nuovo database di gestione che deve essere creato.</span><span class="sxs-lookup"><span data-stu-id="5f770-327">Specifies the name of the new management database that should be created.</span></span> <span data-ttu-id="5f770-328">Esempio di utilizzo: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="5f770-328">Example usage: **/MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="5f770-329">Se **/DB_PREDEPLOY_MANAGEMENT** non è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-329">If **/DB_PREDEPLOY_MANAGEMENT** is not specified, this will be ignored.</span></span> |
| <span data-ttu-id="5f770-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-330">/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="5f770-331">Indica se il server di gestione che accederà al database viene installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="5f770-331">Indicates if the management server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="5f770-332">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-332">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="5f770-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-333">/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="5f770-334">Specifica l'account del computer remoto in cui verrà installato il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="5f770-334">Specifies the machine account of the remote machine that the management server will be installed on.</span></span> <span data-ttu-id="5f770-335">Esempio di utilizzo: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"**</span><span class="sxs-lookup"><span data-stu-id="5f770-335">Example usage: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="domain\\computername"**</span></span> |
| <span data-ttu-id="5f770-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-336">/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="5f770-337">Indica l'account di amministratore che verrà usato per installare il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="5f770-337">Indicates the Administrator account that will be used to install the management server.</span></span> <span data-ttu-id="5f770-338">Esempio di utilizzo: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="5f770-338">Example usage: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT ="domain\\alias"**</span></span> |

#### <span data-ttu-id="5f770-339">Parametri per l'installazione del server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="5f770-339">Parameters for Installing Publishing Server</span></span>

| <span data-ttu-id="5f770-340">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-340">Parameter</span></span> | <span data-ttu-id="5f770-341">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-341">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-342">/PUBLISHING_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-342">/PUBLISHING_SERVER</span></span> | <span data-ttu-id="5f770-343">Specifica che verrà installato il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="5f770-343">Specifies that the Publishing Server will be installed.</span></span> <span data-ttu-id="5f770-344">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-344">No value is expected.</span></span> |
| <span data-ttu-id="5f770-345">/PUBLISHING_MGT_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-345">/PUBLISHING_MGT_SERVER</span></span> | <span data-ttu-id="5f770-346">Specifica l'URL del servizio di gestione a cui il server di pubblicazione si connette.</span><span class="sxs-lookup"><span data-stu-id="5f770-346">Specifies the URL to Management Service the Publishing server will connect to.</span></span> <span data-ttu-id="5f770-347">Esempio di utilizzo: **http:// &lt; Management Server Name &gt; : numero &lt; &gt; di porta del server di gestione**.</span><span class="sxs-lookup"><span data-stu-id="5f770-347">Example usage: **http://&lt;management server name&gt;:&lt;Management server port number&gt;**.</span></span> <span data-ttu-id="5f770-348">Se **/PUBLISHING_SERVER** non viene usato, questo parametro verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-348">If **/PUBLISHING_SERVER** is not used, this parameter will be ignored.</span></span> |
| <span data-ttu-id="5f770-349">/PUBLISHING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-349">/PUBLISHING_WEBSITE_NAME</span></span> | <span data-ttu-id="5f770-350">Specifica il nome del sito Web che verrà creato per il servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="5f770-350">Specifies name of the website that will be created for the publishing service.</span></span> <span data-ttu-id="5f770-351">Esempio di utilizzo: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"**</span><span class="sxs-lookup"><span data-stu-id="5f770-351">Example usage: **/PUBLISHING_WEBSITE_NAME="Microsoft App-V Publishing Service"**</span></span> |
| <span data-ttu-id="5f770-352">/PUBLISHING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-352">/PUBLISHING_WEBSITE_PORT</span></span> | <span data-ttu-id="5f770-353">Specifica il numero di porta usato dal servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="5f770-353">Specifies the port number used by the publishing service.</span></span> <span data-ttu-id="5f770-354">Esempio di utilizzo: **/PUBLISHING_WEBSITE_PORT = 83**</span><span class="sxs-lookup"><span data-stu-id="5f770-354">Example usage: **/PUBLISHING_WEBSITE_PORT=83**</span></span> |

#### <span data-ttu-id="5f770-355">Parametri per Reporting Server</span><span class="sxs-lookup"><span data-stu-id="5f770-355">Parameters for Reporting Server</span></span>

| <span data-ttu-id="5f770-356">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-356">Parameter</span></span> | <span data-ttu-id="5f770-357">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-357">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-358">/REPORTING_SERVER</span><span class="sxs-lookup"><span data-stu-id="5f770-358">/REPORTING_SERVER</span></span> | <span data-ttu-id="5f770-359">Specifica che verrà installato il server di report.</span><span class="sxs-lookup"><span data-stu-id="5f770-359">Specifies that the Reporting Server will be installed.</span></span> <span data-ttu-id="5f770-360">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-360">No value is expected.</span></span> |
| <span data-ttu-id="5f770-361">/REPORTING_WEBSITE_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-361">/REPORTING_WEBSITE_NAME</span></span> | <span data-ttu-id="5f770-362">Specifica il nome del sito Web che verrà creato per il servizio di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="5f770-362">Specifies name of the website that will be created for the Reporting Service.</span></span> <span data-ttu-id="5f770-363">Esempio di utilizzo: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"**</span><span class="sxs-lookup"><span data-stu-id="5f770-363">Example usage: **/REPORTING_WEBSITE_NAME="Microsoft App-V ReportingService"**</span></span> |
| <span data-ttu-id="5f770-364">/REPORTING_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="5f770-364">/REPORTING_WEBSITE_PORT</span></span> | <span data-ttu-id="5f770-365">Specifica il numero di porta che verrà usato dal servizio Reporting.</span><span class="sxs-lookup"><span data-stu-id="5f770-365">Specifies the port number that the Reporting Service will use.</span></span> <span data-ttu-id="5f770-366">Esempio di utilizzo: **/REPORTING_WEBSITE_PORT = 82**</span><span class="sxs-lookup"><span data-stu-id="5f770-366">Example usage: **/REPORTING_WEBSITE_PORT=82**</span></span> |

#### <span data-ttu-id="5f770-367">Parametri per l'uso di un database del server di report esistente</span><span class="sxs-lookup"><span data-stu-id="5f770-367">Parameters for using an Existing Reporting Server Database</span></span>

| <span data-ttu-id="5f770-368">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-368">Parameter</span></span> | <span data-ttu-id="5f770-369">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-369">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-370">/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="5f770-371">Indica che Microsoft SQL Server è installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="5f770-371">Indicates that the Microsoft SQL Server is installed on the local server.</span></span> <span data-ttu-id="5f770-372">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-372">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="5f770-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-373">/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="5f770-374">Specifica il nome del computer remoto in cui è installato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5f770-374">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="5f770-375">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-375">Takes a string.</span></span> <span data-ttu-id="5f770-376">Esempio di utilizzo: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="5f770-376">Example usage: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="5f770-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-377">/EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="5f770-378">Indica che deve essere usata l'istanza SQL predefinita.</span><span class="sxs-lookup"><span data-stu-id="5f770-378">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="5f770-379">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-379">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="5f770-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-380">/EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="5f770-381">Specifica il nome dell'istanza SQL personalizzata che deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="5f770-381">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="5f770-382">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-382">Takes a string.</span></span> <span data-ttu-id="5f770-383">Esempio di utilizzo: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "SqlServer"**</span><span class="sxs-lookup"><span data-stu-id="5f770-383">Example usage: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="5f770-384">/EXISTING_ REPORTING _DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-384">/EXISTING_ REPORTING _DB_NAME</span></span> | <span data-ttu-id="5f770-385">Specifica il nome del database di report esistente che deve essere usato.</span><span class="sxs-lookup"><span data-stu-id="5f770-385">Specifies the name of the existing Reporting database that should be used.</span></span> <span data-ttu-id="5f770-386">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-386">Takes a string.</span></span> <span data-ttu-id="5f770-387">Esempio di utilizzo: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"**</span><span class="sxs-lookup"><span data-stu-id="5f770-387">Example usage: **/EXISTING_REPORTING_DB_NAME="AppVReporting"**</span></span> |

#### <span data-ttu-id="5f770-388">Parametri per l'installazione del database di Reporting Server</span><span class="sxs-lookup"><span data-stu-id="5f770-388">Parameters for installing Reporting Server Database</span></span>

| <span data-ttu-id="5f770-389">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-389">Parameter</span></span> | <span data-ttu-id="5f770-390">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-390">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-391">/DB_PREDEPLOY_REPORTING</span><span class="sxs-lookup"><span data-stu-id="5f770-391">/DB_PREDEPLOY_REPORTING</span></span> | <span data-ttu-id="5f770-392">Specifica che verrà installato il database delle relazioni.</span><span class="sxs-lookup"><span data-stu-id="5f770-392">Specifies that the Reporting Database will be installed.</span></span> <span data-ttu-id="5f770-393">Per questa installazione sono necessarie le autorizzazioni di DBA.</span><span class="sxs-lookup"><span data-stu-id="5f770-393">DBA permissions are required for this installation.</span></span> <span data-ttu-id="5f770-394">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-394">No value is expected.</span></span> |
| <span data-ttu-id="5f770-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-395">/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="5f770-396">Specifica il nome dell'istanza SQL personalizzata che deve essere usata.</span><span class="sxs-lookup"><span data-stu-id="5f770-396">Specifies the name of the custom SQL instance that should be used.</span></span> <span data-ttu-id="5f770-397">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-397">Takes a string.</span></span> <span data-ttu-id="5f770-398">Esempio di utilizzo: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "SqlServer"**</span><span class="sxs-lookup"><span data-stu-id="5f770-398">Example usage: **/REPORTING_DB_ CUSTOM_SQLINSTANCE="MYSQLSERVER"**</span></span> |
| <span data-ttu-id="5f770-399">/REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-399">/REPORTING_DB_NAME</span></span> | <span data-ttu-id="5f770-400">Specifica il nome del nuovo database di report che deve essere creato.</span><span class="sxs-lookup"><span data-stu-id="5f770-400">Specifies the name of the new Reporting database that should be created.</span></span> <span data-ttu-id="5f770-401">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-401">Takes a string.</span></span> <span data-ttu-id="5f770-402">Esempio di utilizzo: **/REPORTING_DB_NAME = "AppVMgmtDB"**</span><span class="sxs-lookup"><span data-stu-id="5f770-402">Example usage: **/REPORTING_DB_NAME="AppVMgmtDB"**</span></span> |
| <span data-ttu-id="5f770-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-403">/REPORTING_SERVER_MACHINE_USE_LOCAL</span></span> | <span data-ttu-id="5f770-404">Indica che il server di report che accederà al database verrà installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="5f770-404">Indicates that the Reporting server that will be accessing the database is installed on the local server.</span></span> <span data-ttu-id="5f770-405">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-405">Switch parameter so no value is expected.</span></span> |
| <span data-ttu-id="5f770-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-406">/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span> | <span data-ttu-id="5f770-407">Specifica l'account del computer remoto in cui verrà installato il server di report.</span><span class="sxs-lookup"><span data-stu-id="5f770-407">Specifies the machine account of the remote machine that the Reporting server will be installed on.</span></span> <span data-ttu-id="5f770-408">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-408">Takes a string.</span></span> <span data-ttu-id="5f770-409">Esempio di utilizzo: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\computername"**</span><span class="sxs-lookup"><span data-stu-id="5f770-409">Example usage: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="domain\computername"**</span></span> |
| <span data-ttu-id="5f770-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="5f770-410">/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span> | <span data-ttu-id="5f770-411">Indica l'account di amministratore che verrà usato per installare App-V Reporting Server.</span><span class="sxs-lookup"><span data-stu-id="5f770-411">Indicates the Administrator account that will be used to install the App-V Reporting Server.</span></span> <span data-ttu-id="5f770-412">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-412">Takes a string.</span></span> <span data-ttu-id="5f770-413">Esempio di utilizzo: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"**</span><span class="sxs-lookup"><span data-stu-id="5f770-413">Example usage: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="domain\\alias"**</span></span> |

#### <span data-ttu-id="5f770-414">Parametri per l'uso di un database del server di gestione esistente</span><span class="sxs-lookup"><span data-stu-id="5f770-414">Parameters for using an existing Management Server Database</span></span>

| <span data-ttu-id="5f770-415">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f770-415">Parameter</span></span> | <span data-ttu-id="5f770-416">Informazioni</span><span class="sxs-lookup"><span data-stu-id="5f770-416">Information</span></span> |
|--|--|
| <span data-ttu-id="5f770-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5f770-417">/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</span></span> | <span data-ttu-id="5f770-418">Indica che il server SQL è installato nel server locale.</span><span class="sxs-lookup"><span data-stu-id="5f770-418">Indicates that the SQL Server is installed on the local server.</span></span> <span data-ttu-id="5f770-419">Parametro switch in modo che nessun valore sia previsto. Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-419">Switch parameter so no value is expected.If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="5f770-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-420">/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</span></span> | <span data-ttu-id="5f770-421">Specifica il nome del computer remoto in cui è installato SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5f770-421">Specifies the name of the remote computer that SQL Server is installed on.</span></span> <span data-ttu-id="5f770-422">Accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="5f770-422">Takes a string.</span></span> <span data-ttu-id="5f770-423">Esempio di utilizzo: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"**</span><span class="sxs-lookup"><span data-stu-id="5f770-423">Example usage: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME="mycomputer1"**</span></span> |
| <span data-ttu-id="5f770-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="5f770-424">/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</span></span> | <span data-ttu-id="5f770-425">Indica che deve essere usata l'istanza SQL predefinita.</span><span class="sxs-lookup"><span data-stu-id="5f770-425">Indicates that the default SQL instance is to be used.</span></span> <span data-ttu-id="5f770-426">Parametro switch in modo che nessun valore sia previsto.</span><span class="sxs-lookup"><span data-stu-id="5f770-426">Switch parameter so no value is expected.</span></span> <span data-ttu-id="5f770-427">Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-427">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="5f770-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="5f770-428">/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</span></span> | <span data-ttu-id="5f770-429">Specifica il nome dell'istanza di SQL personalizzata che verrà usata.</span><span class="sxs-lookup"><span data-stu-id="5f770-429">Specifies the name of the custom SQL instance that will be used.</span></span> <span data-ttu-id="5f770-430">Esempio di utilizzo **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**.</span><span class="sxs-lookup"><span data-stu-id="5f770-430">Example usage **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE="AppVManagement"**.</span></span> <span data-ttu-id="5f770-431">Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-431">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |
| <span data-ttu-id="5f770-432">/EXISTING_MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="5f770-432">/EXISTING_MANAGEMENT_DB_NAME</span></span> | <span data-ttu-id="5f770-433">Specifica il nome del database di gestione esistente che deve essere usato.</span><span class="sxs-lookup"><span data-stu-id="5f770-433">Specifies the name of the existing management database that should be used.</span></span> <span data-ttu-id="5f770-434">Esempio di utilizzo: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**.</span><span class="sxs-lookup"><span data-stu-id="5f770-434">Example usage: **/EXISTING_MANAGEMENT_DB_NAME="AppVMgmtDB"**.</span></span> <span data-ttu-id="5f770-435">Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5f770-435">If **/DB_PREDEPLOY_MANAGEMENT** is specified, this will be ignored.</span></span> |

<span data-ttu-id="5f770-436">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="5f770-436">Got an App-V issue?</span></span> <span data-ttu-id="5f770-437">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="5f770-437">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="5f770-438">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f770-438">Related topics</span></span>

[<span data-ttu-id="5f770-439">Distribuzione del server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="5f770-439">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)
