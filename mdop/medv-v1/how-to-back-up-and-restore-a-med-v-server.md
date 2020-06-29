---
title: Come eseguire il backup e ripristinare un server MED-V
description: Come eseguire il backup e ripristinare un server MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823086"
---
# Come eseguire il backup e ripristinare un server MED-V


I file XML che si trovano nel server possono essere sottoposti a backup e quindi ripristinati in caso di perdita di dati nel server.

**Per eseguire il backup di un server MED-V**

-   Eseguire il backup dei file seguenti, che si trovano in * &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer*:

    **Nota**  Se la configurazione è stata modificata rispetto all'impostazione predefinita, i file potrebbero essere archiviati in una posizione diversa.

     

    -   ClientPolicy.xml

    -   ClientSettings.xml

    -   ConfigurationFiles.xml

    -   OrganizationPolicy.xml

    -   WorkspaceKeys.xml

    **Nota**  È anche possibile eseguire il backup del file ServerSettings.xml. Tuttavia, se è stata modificata una configurazione specifica, ad esempio nel server originale, la directory di VM MED-V si trova in "*C:\\Vms*" e tale directory non esiste nel nuovo server, può causare un errore.

     

**Per ripristinare un server MED-V**

1.  Installare un nuovo server MED-V.

2.  Copiare i file di backup nella directory seguente:

    *&lt;InstallDir &gt; \\Servers\\ConfigurationServer*

3.  Riavviare il servizio MED-V.

 

 





