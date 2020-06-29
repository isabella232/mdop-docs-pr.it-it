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
# Come distribuire il server App-V 5.0 con uno script


Per completare la configurazione del server **appv\_server\_setup.exe** con successo tramite la riga di comando, è necessario specificare e combinare più parametri.

Usare le tabelle seguenti per altre informazioni sull'installazione del server App-V 5,0 tramite la riga di comando.

>[!NOTE]
> È anche possibile accedere alle informazioni nelle tabelle seguenti tramite la riga di comando digitando il comando seguente:
>```
> appv\_server\_setup.exe /?
>```

## Parametri ed esempi comuni

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Per installare il server di gestione e il database di gestione in un computer locale.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "servizio di gestione di Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
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
    <td align="left"><p>Per installare il server di gestione usando un database di gestione esistente in un computer locale.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "servizio di gestione di Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
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
    <td align="left"><p>Per installare il server di gestione usando un database di gestione esistente in un computer remoto.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>/MANAGEMENT_SERVER</p></li>
    <li><p>/MANAGEMENT_ADMINACCOUNT</p></li>
    <li><p>/MANAGEMENT_WEBSITE_NAME</p></li>
    <li><p>/MANAGEMENT_WEBSITE_PORT</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_MANAGEMENT_DB_NAME</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/MANAGEMENT_SERVER</p>
    <p>/MANAGEMENT_ADMINACCOUNT = "Domain\AdminGroup"</p>
    <p>/MANAGEMENT_WEBSITE_NAME = "servizio di gestione di Microsoft AppV"</p>
    <p>/MANAGEMENT_WEBSITE_PORT = "8080"</p>
    <p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME = "SqlServermachine. DomainName"</p>
    <p>/EXISTING_MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXISTING_MANAGEMENT_DB_NAME = "AppVManagement"</p></td>
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
    <td align="left"><p>Per installare il database di gestione e il server di gestione nello stesso computer.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
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
    <td align="left"><p>Per installare il database di gestione in un computer diverso da quello del server di gestione.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_MANAGEMENT</p></li>
    <li><p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/MANAGEMENT_DB_NAME</p></li>
    <li><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_MANAGEMENT</p>
    <p>/MANAGEMENT_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/MANAGEMENT_DB_NAME = "AppVManagement"</p>
    <p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
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
    <td align="left"><p>Per installare il server di pubblicazione.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/PUBLISHING_SERVER</p></li>
    <li><p>/PUBLISHING_MGT_SERVER</p></li>
    <li><p>/PUBLISHING_WEBSITE_NAME</p></li>
    <li><p>/PUBLISHING_WEBSITE_PORT</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/PUBLISHING_SERVER</p>
    <p>/PUBLISHING_MGT_SERVER = " http://ManagementServerName:ManagementPort "</p>
    <p>/PUBLISHING_WEBSITE_NAME = "Microsoft AppV Publishing Service"</p>
    <p>/PUBLISHING_WEBSITE_PORT = "8081"</p></td>
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
    <td align="left"><p>Per installare il server di report e il database di report in un computer locale.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>_SERVER/REPORTING</p></li>
    <li><p>_WEBSITE_NAME/REPORTING</p></li>
    <li><p>_WEBSITE_PORT/REPORTING</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</p></li>
    <li><p>_DB_NAME/REPORTING</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>_SERVER/REPORTING</p></li>
    <li><p>_ADMINACCOUNT/REPORTING</p></li>
    <li><p>_WEBSITE_NAME/REPORTING</p></li>
    <li><p>_WEBSITE_PORT/REPORTING</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>_DB_CUSTOM_SQLINSTANCE/REPORTING</p></li>
    <li><p>_DB_NAME/REPORTING</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <ul>
    <li><p>/appv_server_setup.exe/QUIET</p></li>
    <li><p>/REPORTING_SERVER</p></li>
    <li><p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p></li>
    <li><p>/REPORTING_WEBSITE_PORT = "8082"</p></li>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p></li>
    <li><p>/REPORTING_DB_NAME = "AppVReporting"</p></li>
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
    <td align="left"><p>Per installare il server di report e usare un database di report esistente in un computer locale.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>_SERVER/REPORTING</p></li>
    <li><p>_WEBSITE_NAME/REPORTING</p></li>
    <li><p>_WEBSITE_PORT/REPORTING</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>_SERVER/REPORTING</p></li>
    <li><p>_ADMINACCOUNT/REPORTING</p></li>
    <li><p>_WEBSITE_NAME/REPORTING</p></li>
    <li><p>_WEBSITE_PORT/REPORTING</p></li>
    <li><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
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
    <td align="left"><p>Per installare il server di report usando un database di report esistente in un computer remoto.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>_SERVER/REPORTING</p></li>
    <li><p>_WEBSITE_NAME/REPORTING</p></li>
    <li><p>_WEBSITE_PORT/REPORTING</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_SQLINSTANCE_USE_DEFAULT</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>_SERVER/REPORTING</p></li>
    <li><p>_ADMINACCOUNT/REPORTING</p></li>
    <li><p>_WEBSITE_NAME/REPORTING</p></li>
    <li><p>_WEBSITE_PORT/REPORTING</p></li>
    <li><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></li>
    <li><p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE</p></li>
    <li><p>/EXISTING_REPORTING _DB_NAME</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/REPORTING_SERVER</p>
    <p>/REPORTING_WEBSITE_NAME = "Microsoft AppV Reporting Service"</p>
    <p>/REPORTING_WEBSITE_PORT = "8082"</p>
    <p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME = "SqlServerMachine. DomainName"</p>
    <p>/EXISTING_REPORTING _DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/EXITING_REPORTING_DB_NAME = "AppVReporting"</p></td>
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
    <td align="left"><p>Per installare il database delle relazioni nello stesso computer del server di report.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</p></li>
    <li><p>_DB_NAME/REPORTING</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>_DB_CUSTOM_SQLINSTANCE/REPORTING</p></li>
    <li><p>_DB_NAME/REPORTING</p></li>
    <li><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
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
    <td align="left"><p>Per installare il database delle relazioni in un computer diverso da quello del server dei report.</p></td>
    <td align="left"><p>Per usare l'istanza predefinita di Microsoft SQL Server, usare i parametri seguenti:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>_DB_SQLINSTANCE_USE_DEFAULT/REPORTING</p></li>
    <li><p>_DB_NAME/REPORTING</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Per usare un'istanza personalizzata di Microsoft SQL Server, usare questi parametri:</p>
    <ul>
    <li><p>/DB_PREDEPLOY_REPORTING</p></li>
    <li><p>_DB_CUSTOM_SQLINSTANCE/REPORTING</p></li>
    <li><p>_DB_NAME/REPORTING</p></li>
    <li><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></li>
    <li><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></li>
    </ul>
    <p>Uso di un'istanza personalizzata di esempio di Microsoft SQL Server:</p>
    <p>/appv_server_setup.exe/QUIET</p>
    <p>/DB_PREDEPLOY_REPORTING</p>
    <p>/REPORTING_DB_CUSTOM_SQLINSTANCE = "SqlInstanceName"</p>
    <p>/REPORTING_DB_NAME = "AppVReporting"</p>
    <p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\MachineAccount"</p>
    <p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = "Domain\InstallAdminAccount"</p></td>
    </tr>
    </tbody>
    </table>

## Definizioni di parametri

### Parametri generali

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/QUIET</p></td>
    <td align="left"><p>Specifica l'installazione silenziosa.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/UNINSTALL</p></td>
    <td align="left"><p>Specifica una disinstallazione.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/LAYOUT</p></td>
    <td align="left"><p>Specifica l'azione del layout. Questo estrae i file di MSI e script in una cartella senza installare effettivamente il prodotto. Nessun valore previsto.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/LAYOUTDIR</p></td>
    <td align="left"><p>Specifica la directory del layout. Accetta una stringa. Ad esempio,/LAYOUTDIR = "C:\Application Virtualization Server"</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/INSTALLDIR</p></td>
    <td align="left"><p>Specifica la directory di installazione. Accetta una stringa. Ad esempio /INSTALLDIR = "c: programmi Files\Application Virtualization\Server"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MUOPTIN</p></td>
    <td align="left"><p>Abilita Microsoft Update. Nessun valore previsto</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/ACCEPTEULA</p></td>
    <td align="left"><p>Accetta il contratto di licenza. Questa operazione è necessaria per un'installazione automatica. Esempio di utilizzo: <strong> /AcceptEula </strong> o <strong> /ACCEPTEULA = 1 </strong> .</p></td>
    </tr>
    </tbody>
    </table>

### Parametri di installazione del server di gestione

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER</p></td>
    <td align="left"><p>Specifica che verrà installato il server di gestione. Nessun valore previsto</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_ADMINACCOUNT</p></td>
    <td align="left"><p>Specifica l'account a cui sarà consentito l'accesso di amministratore al server di gestione questo account può essere un singolo account utente o un gruppo. Esempio di utilizzo: <strong> /MANAGEMENT_ADMINACCOUNT = "mydomain\admin" </strong> . Se <strong> /MANAGEMENT_SERVER </strong> non è specificato, verrà ignorato. Specifica l'account a cui sarà consentito l'accesso di amministratore al server di gestione. Può trattarsi di un account utente o di un gruppo. Ad esempio, <strong> /MANAGEMENT_ADMINACCOUNT = &quot; mydomain\admin &quot; </strong> .</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_WEBSITE_NAME</p></td>
    <td align="left"><p>Specifica il nome del sito Web che verrà creato per il servizio di gestione. Ad esempio,/MANAGEMENT_WEBSITE_NAME = "Microsoft App-V Management Service"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MANAGEMENT_WEBSITE_PORT</p></td>
    <td align="left"><p>Specifica il numero di porta che verrà usato dal servizio di gestione. Ad esempio,/MANAGEMENT_WEBSITE_PORT = 82.</p></td>
    </tr>
    </tbody>
    </table>

### Parametri per il database del server di gestione

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_MANAGEMENT</p></td>
    <td align="left"><p>Specifica che verrà installato il database di gestione. Per completare l'installazione, è necessario disporre di autorizzazioni di database sufficienti. Nessun valore previsto</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Indica che deve essere usata l'istanza SQL predefinita. Nessun valore previsto.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Specifica il nome dell'istanza SQL personalizzata che deve essere usata per creare un nuovo database. Esempio di utilizzo: <strong> /MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "SqlServer" </strong> . Se/DB_PREDEPLOY_MANAGEMENT non è specificato, verrà ignorato.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Specifica il nome del nuovo database di gestione che deve essere creato. Esempio di utilizzo: <strong> /MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Se/DB_PREDEPLOY_MANAGEMENT non è specificato, verrà ignorato.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Indica se il server di gestione che accederà al database viene installato nel server locale. Parametro switch in modo che nessun valore sia previsto.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Specifica l'account del computer remoto in cui verrà installato il server di gestione. Esempio di utilizzo: <strong> /MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT = "Domain\computername"</strong></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Indica l'account di amministratore che verrà usato per installare il server di gestione. Esempio di utilizzo: <strong> /MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT = "dominio\alias"</strong></p></td>
    </tr>
    </tbody>
    </table>

### Parametri per l'installazione del server di pubblicazione

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_SERVER</p></td>
    <td align="left"><p>Specifica che verrà installato il server di pubblicazione. Nessun valore previsto</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_MGT_SERVER</p></td>
    <td align="left"><p>Specifica l'URL del servizio di gestione a cui il server di pubblicazione si connette. Esempio di utilizzo: <strong> http:// &lt; Management Server Name &gt; : numero di porta del server di &lt; gestione &gt; </strong> . Se/PUBLISHING_SERVER non viene usato, questo parametro verrà ignorato</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/PUBLISHING_WEBSITE_NAME</p></td>
    <td align="left"><p>Specifica il nome del sito Web che verrà creato per il servizio di pubblicazione. Ad esempio,/PUBLISHING_WEBSITE_NAME = "Microsoft App-V Publishing Service"</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/PUBLISHING_WEBSITE_PORT</p></td>
    <td align="left"><p>Specifica il numero di porta usato dal servizio di pubblicazione. Ad esempio,/PUBLISHING_WEBSITE_PORT = 83</p></td>
    </tr>
    </tbody>
    </table>

### Parametri per Reporting Server

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/REPORTING_SERVER</p></td>
    <td align="left"><p>Specifica che verrà installato il server di report. Nessun valore previsto</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_WEBSITE_NAME</p></td>
    <td align="left"><p>Specifica il nome del sito Web che verrà creato per il servizio di creazione di report. Ad esempio /REPORTING_WEBSITE_NAME = &quot; Microsoft App-V ReportingService&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_WEBSITE_PORT</p></td>
    <td align="left"><p>Specifica il numero di porta che verrà usato dal servizio Reporting. Ad esempio /REPORTING_WEBSITE_PORT = 82</p></td>
    </tr>
    </tbody>
    </table>

     

### Parametri per l'uso di un database del server di report esistente

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_REPORTING_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Indica che Microsoft SQL Server è installato nel server locale. Parametro switch in modo che nessun valore sia previsto.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_REPORTING_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Specifica il nome del computer remoto in cui è installato SQL Server. Accetta una stringa. Ad esempio /EXISTING_REPORTING_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ REPORTING <em> DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Indica che deve essere usata l'istanza SQL predefinita. Parametro switch in modo che nessun valore sia previsto.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p></em>REPORTING_DB_CUSTOM_SQLINSTANCE/existing</p></td>
    <td align="left"><p>Specifica il nome dell'istanza SQL personalizzata che deve essere usata. Accetta una stringa. Ad esempio /EXISTING_REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; SqlServer&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ REPORTING _DB_NAME</p></td>
    <td align="left"><p>Specifica il nome del database di report esistente che deve essere usato. Accetta una stringa. Ad esempio /EXISTING_REPORTING_DB_NAME = &quot; AppVReporting&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parametri per l'installazione del database di Reporting Server

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/DB_PREDEPLOY_REPORTING</p></td>
    <td align="left"><p>Specifica che verrà installato il database delle relazioni. Per questa installazione sono necessarie le autorizzazioni di DBA. Nessun valore previsto</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Specifica il nome dell'istanza SQL personalizzata che deve essere usata. Accetta una stringa. Ad esempio /REPORTING_DB_ CUSTOM_SQLINSTANCE = &quot; SqlServer&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_DB_NAME</p></td>
    <td align="left"><p>Specifica il nome del nuovo database di report che deve essere creato. Accetta una stringa. Ad esempio /REPORTING_DB_NAME = &quot; AppVMgmtDB&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_MACHINE_USE_LOCAL</p></td>
    <td align="left"><p>Indica che il server di report che accederà al database verrà installato nel server locale. Parametro switch in modo che nessun valore sia previsto.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</p></td>
    <td align="left"><p>Specifica l'account del computer remoto in cui verrà installato il server di report. Accetta una stringa. Ad esempio /REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT = &quot; Domain\computername&quot;</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</p></td>
    <td align="left"><p>Indica l'account di amministratore che verrà usato per installare App-V Reporting Server. Accetta una stringa. Ad esempio /REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT = &quot; dominio\alias&quot;</p></td>
    </tr>
    </tbody>
    </table>

### Parametri per l'uso di un database del server di gestione esistente

<table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Informazioni</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_SQL_SERVER_USE_LOCAL</p></td>
    <td align="left"><p>Indica che il server SQL è installato nel server locale. Parametro switch in modo che nessun valore sia previsto. Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_REMOTE_SQL_SERVER_NAME</p></td>
    <td align="left"><p>Specifica il nome del computer remoto in cui è installato SQL Server. Accetta una stringa. Ad esempio /EXISTING_MANAGEMENT_DB_ REMOTE_SQL_SERVER_NAME = &quot; mycomputer1&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_ MANAGEMENT_DB_SQLINSTANCE_USE_DEFAULT</p></td>
    <td align="left"><p>Indica che deve essere usata l'istanza SQL predefinita. Parametro switch in modo che nessun valore sia previsto. Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE</p></td>
    <td align="left"><p>Specifica il nome dell'istanza di SQL personalizzata che verrà usata. Esempio di utilizzo <strong> /EXISTING_MANAGEMENT_DB_ CUSTOM_SQLINSTANCE = "AppVManagement" </strong> . Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>/EXISTING_MANAGEMENT_DB_NAME</p></td>
    <td align="left"><p>Specifica il nome del database di gestione esistente che deve essere usato. Esempio di utilizzo: <strong> /EXISTING_MANAGEMENT_DB_NAME = "AppVMgmtDB" </strong> . Se/DB_PREDEPLOY_MANAGEMENT è specificato, verrà ignorato.</p>
    <p></p>
    <p><strong>Hai un suggerimento per App-V </strong> ? Aggiungere o votare i suggerimenti <a href="http://appv.uservoice.com/forums/280448-microsoft-application-virtualization" data-raw-source="[here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization)"> qui </a> . <strong>È stata emessa un'app-V </strong> e? Usare l' <a href="https://social.technet.microsoft.com/Forums/home?forum=mdopappv" data-raw-source="[App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)"> App-V Forum TechNet </a> .</p></td>
</tr>
</tbody>
</table>
  

## Argomenti correlati

[Distribuzione del server App-V 5.0](deploying-the-app-v-50-server.md)

 

 





