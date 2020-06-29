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
# Come distribuire il server App-V 5.1 con uno script

Per completare la configurazione del server **appv\_server\_setup.exe** con successo tramite la riga di comando, è necessario specificare e combinare più parametri.

## Installare il server App-V 5,1 usando uno script

- Usare le informazioni seguenti sull'installazione del server App-V 5,1 tramite la riga di comando.

    > [!NOTE]
    > È anche possibile accedere alle informazioni nelle tabelle seguenti tramite la riga di comando digitando il comando seguente: **appv\_server\_setup.exe/?**.

### Installare il server di gestione e il database di gestione in un computer locale

I parametri seguenti sono validi sia per l'istanza predefinita che per quella personalizzata di Microsoft SQL Server:

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /DB_PREDEPLOY_MANAGEMENT
- /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT
- /MANAGEMENT_DB_NAME

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement"
```

### Installare il server di gestione usando un database di gestione esistente in un computer locale

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Per usare un'istanza personalizzata di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza predefinita in *corsivo*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Installare il server di gestione usando un database di gestione esistente in un computer remoto

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_MANAGEMENT_DB_NAME

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- /MANAGEMENT_SERVER
- /MANAGEMENT_ADMINACCOUNT
- /MANAGEMENT_WEBSITE_NAME
- /MANAGEMENT_WEBSITE_PORT
- /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /EXISTING_MANAGEMENT_DB_NAME

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /MANAGEMENT_SERVER /MANAGEMENT_ADMINACCOUNT="Domain\AdminGroup" /MANAGEMENT_WEBSITE_NAME="Microsoft AppV Management Service" /MANAGEMENT_WEBSITE_PORT="8080" /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME="SqlServermachine.domainName" /EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE ="SqlInstanceName" /EXISTING_MANAGEMENT_DB_NAME ="AppVManagement"
```

### Installare il database di gestione e il server di gestione nello stesso computer

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_SERVER_MACHINE_USE_LOCAL
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_SERVER_MACHINE_USE_LOCAL /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installare il database di gestione in un computer diverso da quello del server di gestione

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- /DB_PREDEPLOY_MANAGEMENT
- */MANAGEMENT_DB_CUSTOM_SQLINSTANCE*
- /MANAGEMENT_DB_NAME
- /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT
- /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_MANAGEMENT /MANAGEMENT_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /MANAGEMENT_DB_NAME="AppVManagement" /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installare il server di pubblicazione

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:

- /PUBLISHING_SERVER
- /PUBLISHING_MGT_SERVER
- /PUBLISHING_WEBSITE_NAME
- /PUBLISHING_WEBSITE_PORT

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /PUBLISHING_SERVER /PUBLISHING_MGT_SERVER="http://ManagementServerName:ManagementPort" /PUBLISHING_WEBSITE_NAME="Microsoft AppV Publishing Service" /PUBLISHING_WEBSITE_PORT="8081"
```

### Installare il server di report e il database di report in un computer locale

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- _SERVER/REPORTING
- _WEBSITE_NAME/REPORTING
- _WEBSITE_PORT/REPORTING
- /DB_PREDEPLOY_REPORTING
- *_DB_SQLINSTANCE_USE_DEFAULT/REPORTING*
- _DB_NAME/REPORTING

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- _SERVER/REPORTING
- *_ADMINACCOUNT/REPORTING*
- _WEBSITE_NAME/REPORTING
- _WEBSITE_PORT/REPORTING
- /DB_PREDEPLOY_REPORTING
- *_DB_CUSTOM_SQLINSTANCE/REPORTING*
- _DB_NAME/REPORTING

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting"
```

### Installare il server di report e usare un database di report esistente in un computer locale

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- _SERVER/REPORTING
- _WEBSITE_NAME/REPORTING
- _WEBSITE_PORT/REPORTING
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- _SERVER/REPORTING
- *_ADMINACCOUNT/REPORTING*
- _WEBSITE_NAME/REPORTING
- _WEBSITE_PORT/REPORTING
- /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Installare il server di report usando un database di report esistente in un computer remoto

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- _SERVER/REPORTING
- _WEBSITE_NAME/REPORTING
- _WEBSITE_PORT/REPORTING
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT*
- /EXISTING_REPORTING _DB_NAME

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- _SERVER/REPORTING
- *_ADMINACCOUNT/REPORTING*
- _WEBSITE_NAME/REPORTING
- _WEBSITE_PORT/REPORTING
- /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME
- */EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE*
- /EXISTING_REPORTING _DB_NAME

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /REPORTING_SERVER /REPORTING_WEBSITE_NAME="Microsoft AppV Reporting Service" /REPORTING_WEBSITE_PORT="8082" /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME="SqlServerMachine.DomainName" /EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /EXITING_REPORTING_DB_NAME="AppVReporting"
```

### Installare il database delle relazioni nello stesso computer del server di report

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- /DB_PREDEPLOY_REPORTING
- *_DB_SQLINSTANCE_USE_DEFAULT/REPORTING*
- _DB_NAME/REPORTING
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- /DB_PREDEPLOY_REPORTING
- *_DB_CUSTOM_SQLINSTANCE/REPORTING*
- _DB_NAME/REPORTING
- /REPORTING_SERVER_MACHINE_USE_LOCAL
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:**

```dos
appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_SERVER_MACHINE_USE_LOCAL /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Installare il database di report in un computer diverso da quello del server di report

Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti (differenza dall'istanza personalizzata in *corsivo*):

- /DB_PREDEPLOY_REPORTING
- _DB_SQLINSTANCE_USE_DEFAULT/REPORTING
- _DB_NAME/REPORTING
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri (differenza dall'istanza predefinita in *corsivo*):

- /DB_PREDEPLOY_REPORTING
- _DB_CUSTOM_SQLINSTANCE/REPORTING
- _DB_NAME/REPORTING
- /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT
- /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT

**Esempio: utilizzo di un'istanza personalizzata di Microsoft SQL Server:**

```dos
 appv_server_setup.exe /QUIET /DB_PREDEPLOY_REPORTING /REPORTING_DB_CUSTOM_SQLINSTANCE="SqlInstanceName" /REPORTING_DB_NAME="AppVReporting" /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT="Domain\MachineAccount" /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT="Domain\InstallAdminAccount"
```

### Definizioni di parametri

#### Parametri generali

| Parametro | Informazioni |
|--|--|
| /QUIET | Specifica l'installazione silenziosa. |
| /UNINSTALL | Specifica una disinstallazione. |
| /LAYOUT | Specifica l'azione del layout. Questo estrae i file di MSI e script in una cartella senza installare effettivamente il prodotto. Nessun valore previsto. |
| /LAYOUTDIR | Specifica la directory del layout. Accetta una stringa. Esempio di utilizzo: **/LAYOUTDIR = "C:\\Application Virtualization Server"** |
| /INSTALLDIR | Specifica la directory di installazione. Accetta una stringa. Esempio di utilizzo: **/INSTALLDIR = "C:\\Programmi Files\\Application Virtualization\\Server"** |
| /MUOPTIN | Abilita Microsoft Update. Nessun valore previsto. |
| /ACCEPTEULA | Accetta il contratto di licenza. Questa operazione è necessaria per un'installazione automatica. Esempio di utilizzo: **/AcceptEula** o **/ACCEPTEULA = 1** |

#### Parametri di installazione del server di gestione

|Parametro |Informazioni |
|--|--|
| /MANAGEMENT_SERVER | Specifica che verrà installato il server di gestione. Nessun valore previsto |
| /MANAGEMENT_ADMINACCOUNT | Specifica l'account a cui sarà consentito l'accesso di amministratore al server di gestione. Può trattarsi di un account utente o di un gruppo. Esempio di utilizzo: **/MANAGEMENT_ADMINACCOUNT = "mydomain\\admin"**. Se **/MANAGEMENT_SERVER** non è specificato, verrà ignorato. |
| /MANAGEMENT_WEBSITE_NAME | Specifica il nome del sito Web che verrà creato per il servizio di gestione. Esempio di utilizzo: **/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"** |
| MANAGEMENT_WEBSITE_PORT | Specifica il numero di porta che verrà usato dal servizio di gestione. Esempio di utilizzo: **/MANAGEMENT_WEBSITE_PORT = 82** |

#### Parametri per il database del server di gestione

| Parametro | Informazioni |
|--|--|
| /DB_PREDEPLOY_MANAGEMENT | Specifica che verrà installato il database di gestione. Per completare l'installazione, è necessario disporre di autorizzazioni di database sufficienti. Nessun valore previsto. |
| /MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indica che deve essere usata l'istanza SQL predefinita. Nessun valore previsto. |
| /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Specifica il nome dell'istanza SQL personalizzata che deve essere usata per creare un nuovo database. Esempio di utilizzo: **/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "SqlServer"**. Se **/DB_PREDEPLOY_MANAGEMENT** non è specificato, verrà ignorato. |
| /MANAGEMENT_DB_NAME | Specifica il nome del nuovo database di gestione che deve essere creato. Esempio di utilizzo: **/MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Se **/DB_PREDEPLOY_MANAGEMENT** non è specificato, verrà ignorato. |
| /MANAGEMENT_SERVER_MACHINE_USE_LOCAL | Indica se il server di gestione che accederà al database viene installato nel server locale. Parametro switch in modo che nessun valore sia previsto. |
| /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT | Specifica l'account del computer remoto in cui verrà installato il server di gestione. Esempio di utilizzo: **/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "domain\\computername"** |
| /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT | Indica l'account di amministratore che verrà usato per installare il server di gestione. Esempio di utilizzo: **/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parametri per l'installazione del server di pubblicazione

| Parametro | Informazioni |
|--|--|
| /PUBLISHING_SERVER | Specifica che verrà installato il server di pubblicazione. Nessun valore previsto. |
| /PUBLISHING_MGT_SERVER | Specifica l'URL del servizio di gestione a cui il server di pubblicazione si connette. Esempio di utilizzo: **http:// &lt; Management Server Name &gt; : numero &lt; &gt; di porta del server di gestione**. Se **/PUBLISHING_SERVER** non viene usato, questo parametro verrà ignorato. |
| /PUBLISHING_WEBSITE_NAME | Specifica il nome del sito Web che verrà creato per il servizio di pubblicazione. Esempio di utilizzo: **/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"** |
| /PUBLISHING_WEBSITE_PORT | Specifica il numero di porta usato dal servizio di pubblicazione. Esempio di utilizzo: **/PUBLISHING_WEBSITE_PORT = 83** |

#### Parametri per Reporting Server

| Parametro | Informazioni |
|--|--|
| /REPORTING_SERVER | Specifica che verrà installato il server di report. Nessun valore previsto. |
| /REPORTING_WEBSITE_NAME | Specifica il nome del sito Web che verrà creato per il servizio di creazione di report. Esempio di utilizzo: **/REPORTING_WEBSITE_NAME = "Microsoft App-V ReportingService"** |
| /REPORTING_WEBSITE_PORT | Specifica il numero di porta che verrà usato dal servizio Reporting. Esempio di utilizzo: **/REPORTING_WEBSITE_PORT = 82** |

#### Parametri per l'uso di un database del server di report esistente

| Parametro | Informazioni |
|--|--|
| /EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL | Indica che Microsoft SQL Server è installato nel server locale. Parametro switch in modo che nessun valore sia previsto. |
| /EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME | Specifica il nome del computer remoto in cui è installato SQL Server. Accetta una stringa. Esempio di utilizzo: **/EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ REPORTING _DB_SQLINSTANCE_USE_DEFAULT | Indica che deve essere usata l'istanza SQL predefinita. Parametro switch in modo che nessun valore sia previsto. |
| /EXISTING_ REPORTING_DB_CUSTOM_SQLINSTANCE | Specifica il nome dell'istanza SQL personalizzata che deve essere usata. Accetta una stringa. Esempio di utilizzo: **/EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = "SqlServer"** |
| /EXISTING_ REPORTING _DB_NAME | Specifica il nome del database di report esistente che deve essere usato. Accetta una stringa. Esempio di utilizzo: **/EXISTING_REPORTING_DB_NAME = "AppVReporting"** |

#### Parametri per l'installazione del database di Reporting Server

| Parametro | Informazioni |
|--|--|
| /DB_PREDEPLOY_REPORTING | Specifica che verrà installato il database delle relazioni. Per questa installazione sono necessarie le autorizzazioni di DBA. Nessun valore previsto. |
| /REPORTING_DB_SQLINSTANCE_USE_DEFAULT | Specifica il nome dell'istanza SQL personalizzata che deve essere usata. Accetta una stringa. Esempio di utilizzo: **/REPORTING_DB_ CUSTOM_SQLINSTANCE = "SqlServer"** |
| /REPORTING_DB_NAME | Specifica il nome del nuovo database di report che deve essere creato. Accetta una stringa. Esempio di utilizzo: **/REPORTING_DB_NAME = "AppVMgmtDB"** |
| /REPORTING_SERVER_MACHINE_USE_LOCAL | Indica che il server di report che accederà al database verrà installato nel server locale. Parametro switch in modo che nessun valore sia previsto. |
| /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT | Specifica l'account del computer remoto in cui verrà installato il server di report. Accetta una stringa. Esempio di utilizzo: **/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\computername"** |
| /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT | Indica l'account di amministratore che verrà usato per installare App-V Reporting Server. Accetta una stringa. Esempio di utilizzo: **/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "domain\\alias"** |

#### Parametri per l'uso di un database del server di gestione esistente

| Parametro | Informazioni |
|--|--|
| /EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL | Indica che il server SQL è installato nel server locale. Parametro switch in modo che nessun valore sia previsto. Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato. |
| /EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME | Specifica il nome del computer remoto in cui è installato SQL Server. Accetta una stringa. Esempio di utilizzo: **/EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = "mycomputer1"** |
| /EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT | Indica che deve essere usata l'istanza SQL predefinita. Parametro switch in modo che nessun valore sia previsto. Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato. |
| /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE | Specifica il nome dell'istanza di SQL personalizzata che verrà usata. Esempio di utilizzo **/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement"**. Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato. |
| /EXISTING_MANAGEMENT_DB_NAME | Specifica il nome del database di gestione esistente che deve essere usato. Esempio di utilizzo: **/EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB"**. Se **/DB_PREDEPLOY_MANAGEMENT** è specificato, verrà ignorato. |

Hai un problema con l'App-V? Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati

[Distribuzione del server App-V 5.1](deploying-the-app-v-51-server.md)
