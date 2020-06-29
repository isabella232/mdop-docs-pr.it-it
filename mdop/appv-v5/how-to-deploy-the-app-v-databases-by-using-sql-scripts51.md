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
# Come distribuire i database App-V con script SQL

Seguire le istruzioni seguenti per usare gli script SQL, invece di Windows Installer, per:

- Installare i database di App-V 5,1
- Aggiornare i database di App-V in una versione successiva

> [!NOTE]
> Se è già stato distribuito il database App-V 5,0 SP3, gli script SQL non sono necessari per eseguire l'aggiornamento a App-V 5,1.

## Come installare i database di App-V usando gli script SQL

1. Prima di installare gli script di database, rivedere e conservare una copia delle condizioni di licenza di App-V. Eseguendo gli script del database si accettano le condizioni di licenza. Se non è possibile accettarli, non usare questo software.
1. Copiare il **appv\_server\_setup.exe** dal supporto per la versione di App-V in un percorso temporaneo.
1. Da un prompt dei comandi eseguire **appv\_server\_setup.exe** e specificare una posizione temporanea per l'estrazione degli script di database.

    Esempio: appv\_server\_setup.exe/layout c:\\ &lt; _percorso temporaneo_&gt;

1. Passare al percorso temporaneo creato, aprire la cartella **DatabaseScripts** estratta e rivedere il file Readme.txt appropriato per le istruzioni:

    | Database | Posizione del file Readme.txt da usare |
    |--|--|
    | Database di gestione | Sottocartella ManagementDatabase |
    | Database di report | Sottocartella ReportingDatabase |

> [!CAUTION]
> Il file readme.txt nella sottocartella ManagementDatabase non è aggiornato. Le informazioni contenute nei file Leggimi aggiornati sono le più aggiornate e devono sostituire le informazioni di Readme fornite nelle cartelle di **DatabaseScripts** .

> [!IMPORTANT]
> Lo script InsertVersionInfo. SQL non è necessario per le versioni del database di gestione di App-V più avanti rispetto all'App-V 5,0 SP3.

Lo script Permissions. SQL deve essere aggiornato in base al **passaggio 2** nell' [articolo 3031340 della KB](https://support.microsoft.com/kb/3031340). Il **passaggio 1** non è necessario per le versioni di App-v successive all'app-v 5,0 SP3.

## Contenuto del file Leggimi del database di gestione aggiornato

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

## Contenuto del file Leggimi del database di report aggiornato

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

**Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati

[Distribuzione del server App-V 5.1](deploying-the-app-v-51-server.md)

[Come distribuire il server App-V 5.1](how-to-deploy-the-app-v-51-server.md)
