---
title: Come distribuire i database App-V con script SQL
description: Come distribuire i database App-V con script SQL
author: dansimp
ms.assetid: 1183b1bc-d4d7-4914-a049-06e82bf2d96d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4695d105c1aa6732efb6b8ed05169cf29e7f972b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805476"
---
# <span data-ttu-id="a650e-103">Come distribuire i database App-V con script SQL</span><span class="sxs-lookup"><span data-stu-id="a650e-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>

<span data-ttu-id="a650e-104">Seguire le istruzioni seguenti per usare gli script SQL, invece di Windows Installer, per:</span><span class="sxs-lookup"><span data-stu-id="a650e-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

- <span data-ttu-id="a650e-105">Installare i database di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="a650e-105">Install the App-V 5.1 databases</span></span>
- <span data-ttu-id="a650e-106">Aggiornare i database di App-V in una versione successiva</span><span class="sxs-lookup"><span data-stu-id="a650e-106">Upgrade the App-V databases to a later version</span></span>

> [!NOTE]
> <span data-ttu-id="a650e-107">Se è già stato distribuito il database App-V 5,0 SP3, gli script SQL non sono necessari per eseguire l'aggiornamento a App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="a650e-107">If you have already deployed the App-V 5.0 SP3 database, the SQL scripts are not required to upgrade to App-V 5.1.</span></span>

## <span data-ttu-id="a650e-108">Come installare i database di App-V usando gli script SQL</span><span class="sxs-lookup"><span data-stu-id="a650e-108">How to install the App-V databases by using SQL scripts</span></span>

1. <span data-ttu-id="a650e-109">Prima di installare gli script di database, rivedere e conservare una copia delle condizioni di licenza di App-V.</span><span class="sxs-lookup"><span data-stu-id="a650e-109">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="a650e-110">Eseguendo gli script del database si accettano le condizioni di licenza.</span><span class="sxs-lookup"><span data-stu-id="a650e-110">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="a650e-111">Se non è possibile accettarli, non usare questo software.</span><span class="sxs-lookup"><span data-stu-id="a650e-111">If you do not accept them, you should not use this software.</span></span>
1. <span data-ttu-id="a650e-112">Copiare il **appv\_server\_setup.exe** dal supporto per la versione di App-V in un percorso temporaneo.</span><span class="sxs-lookup"><span data-stu-id="a650e-112">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>
1. <span data-ttu-id="a650e-113">Da un prompt dei comandi eseguire **appv\_server\_setup.exe** e specificare una posizione temporanea per l'estrazione degli script di database.</span><span class="sxs-lookup"><span data-stu-id="a650e-113">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

    <span data-ttu-id="a650e-114">Esempio: appv\_server\_setup.exe/layout c:\\ &lt; _percorso temporaneo_&gt;</span><span class="sxs-lookup"><span data-stu-id="a650e-114">Example: appv\_server\_setup.exe /layout c:\\&lt;_temporary location path_&gt;</span></span>

1. <span data-ttu-id="a650e-115">Passare al percorso temporaneo creato, aprire la cartella **DatabaseScripts** estratta e rivedere il file Readme.txt appropriato per le istruzioni:</span><span class="sxs-lookup"><span data-stu-id="a650e-115">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

    | <span data-ttu-id="a650e-116">Database</span><span class="sxs-lookup"><span data-stu-id="a650e-116">Database</span></span> | <span data-ttu-id="a650e-117">Posizione del file Readme.txt da usare</span><span class="sxs-lookup"><span data-stu-id="a650e-117">Location of Readme.txt file to use</span></span> |
    |--|--|
    | <span data-ttu-id="a650e-118">Database di gestione</span><span class="sxs-lookup"><span data-stu-id="a650e-118">Management database</span></span> | <span data-ttu-id="a650e-119">Sottocartella ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="a650e-119">ManagementDatabase subfolder</span></span> |
    | <span data-ttu-id="a650e-120">Database di report</span><span class="sxs-lookup"><span data-stu-id="a650e-120">Reporting database</span></span> | <span data-ttu-id="a650e-121">Sottocartella ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="a650e-121">ReportingDatabase subfolder</span></span> |

> [!CAUTION]
> <span data-ttu-id="a650e-122">Il file readme.txt nella sottocartella ManagementDatabase non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a650e-122">The readme.txt file in the ManagementDatabase subfolder is out of date.</span></span> <span data-ttu-id="a650e-123">Le informazioni contenute nei file Leggimi aggiornati sono le più aggiornate e devono sostituire le informazioni di Readme fornite nelle cartelle di **DatabaseScripts** .</span><span class="sxs-lookup"><span data-stu-id="a650e-123">The information in the updated readme files below is the most current and should supersede the readme information provided in the **DatabaseScripts** folders.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a650e-124">Lo script InsertVersionInfo. SQL non è necessario per le versioni del database di gestione di App-V più avanti rispetto all'App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="a650e-124">The InsertVersionInfo.sql script is not required for versions of the App-V management database later than App-V 5.0 SP3.</span></span>

<span data-ttu-id="a650e-125">Lo script Permissions. SQL deve essere aggiornato in base al **passaggio 2** nell' [articolo 3031340 della KB](https://support.microsoft.com/kb/3031340).</span><span class="sxs-lookup"><span data-stu-id="a650e-125">The Permissions.sql script should be updated according to **Step 2** in [KB article 3031340](https://support.microsoft.com/kb/3031340).</span></span> <span data-ttu-id="a650e-126">Il **passaggio 1** non è necessario per le versioni di App-v successive all'app-v 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="a650e-126">**Step 1** is not required for versions of App-V later than App-V 5.0 SP3.</span></span>

## <span data-ttu-id="a650e-127">Contenuto del file Leggimi del database di gestione aggiornato</span><span class="sxs-lookup"><span data-stu-id="a650e-127">Updated management database README file content</span></span>

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************


Steps to install "AppVManagement" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
    Permissions.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the
    necessary SQL Server client software is installed and available from
    the specified location.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVManagement".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
##     in the file will not work.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. Run the following scripts against the "AppVManagement" database using the
    same account as above in order.

    CreateTables.sql
    CreateStoredProcs.sql
    UpdateTables.sql
##     Permissions.sql

```

## <span data-ttu-id="a650e-128">Contenuto del file Leggimi del database di report aggiornato</span><span class="sxs-lookup"><span data-stu-id="a650e-128">Updated reporting database README file content</span></span>

```plaintext
******************************************************************
Before you install and use the Application Virtualization Database Scripts you must:
1.Review the Microsoft Application Virtualization Server 5.0 license terms.
2.Print and retain a copy of the license terms for your records.
By running the Microsoft Application Virtualization Database Scripts you agree to such license terms.  If you do not accept them, do not use the software.
******************************************************************

Steps to install "AppVReporting" schema in SQL SERVER.


## PREREQUISITES:

 1. Review the installation package.  The following files MUST exist:

    SQL files
    ---------
    Database.sql
    UpgradeDatabase.sql
    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
    ScheduleReportingJob.sql

 2. Ensure the target SQL Server instance and SQL Server Agent service are running.

 3. If you are not running the scripts directly on the server, ensure the 
    necessary SQL Server client software is installed and executable from
    the location you have chosen.  Specifically, the "osql" command must
##     be supported for these scripts to run.



## PREPARATION:

 1. Review the database.sql file and modify as necessary.  Although the
    defaults are likely sufficient, it is suggested that the following
    settings be reviewed:

    DATABASE - ensure name is satisfactory - default is "AppVReporting".

 2. Review the Permissions.sql file and provide all the necessary account information
    for setting up read and write access on the database. Note: Default settings
    in the file will not work.

 3. Review the ScheduleReportingJob.sql file and make sure that the stored proc schedule
    time is acceptable. The default stored proc schedule time is at 12.01 AM (line 84). 
    If this time is not suitable, you can change this to a more suitable time. The time is
##     in the format HHMMSS.



## INSTALLATION:

 1. Run the database.sql against the "master" database.  Your user
    credential must have the ability to create databases.
    This script will create the database.

 2. If upgrading the database, run UpgradeDatabase.sql This will upgrade database schema.

 2. Run the following scripts against the "AppVReporting" database using the
    same account as above in order.

    CreateTables.sql
    CreateReportingStoredProcs.sql
    CreateStoredProcs.sql
    CreateViews.sql
    InsertVersionInfo.sql
    Permissions.sql
##     ScheduleReportingJob.sql

```

**<span data-ttu-id="a650e-129">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="a650e-129">Got an App-V issue?</span></span>** <span data-ttu-id="a650e-130">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="a650e-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="a650e-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a650e-131">Related topics</span></span>

[<span data-ttu-id="a650e-132">Distribuzione del server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a650e-132">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="a650e-133">Come distribuire il server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="a650e-133">How to Deploy the App-V 5.1 Server</span></span>](how-to-deploy-the-app-v-51-server.md)
