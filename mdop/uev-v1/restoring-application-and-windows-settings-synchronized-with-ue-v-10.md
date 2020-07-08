---
title: Ripristino dell'applicazione e delle impostazioni di Windows sincronizzate con UE-V 1.0
description: Ripristino dell'applicazione e delle impostazioni di Windows sincronizzate con UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804180"
---
# Ripristino dell'applicazione e delle impostazioni di Windows sincronizzate con UE-V 1.0


Le funzionalità WMI e PowerShell di Microsoft User Experience Virtualization (UE-V) consentono di ripristinare i pacchetti di impostazioni. I comandi WMI e PowerShell consentono di ripristinare le impostazioni dell'applicazione e di Windows nei valori delle impostazioni presenti nel computer la prima volta che l'applicazione è stata avviata dopo l'installazione dell'agente UE-V. Questa azione di ripristino viene eseguita in base alle impostazioni per applicazione o Windows. Le impostazioni vengono ripristinate la volta successiva che l'applicazione viene eseguita o quando l'utente accede al sistema operativo.

**Per ripristinare le impostazioni dell'applicazione e le impostazioni di Windows con PowerShell**

1.  Aprire la finestra di Windows PowerShell. Per importare il modulo Microsoft UE-V PowerShell, immettere il comando seguente:

    ``` syntax
    Import-module UEV
    ```

2.  Immettere il cmdlet di PowerShell seguente per ripristinare le impostazioni dell'applicazione e le impostazioni di Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cmdlet di PowerShell</strong></th>
    <th align="left"><strong>Descrizione</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Ripristinare-UevUserSetting</p></td>
    <td align="left"><p>Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows</p></td>
    </tr>
    </tbody>
    </table>

     

**Per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows con WMI**

1.  Aprire una finestra di PowerShell.

2.  Immettere il comando WMI seguente per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Comando WMI</strong></th>
    <th align="left"><strong>Descrizione</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-namespace root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-argument &lt; template_ID&gt;</p></td>
    <td align="left"><p>Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows</p></td>
    </tr>
    </tbody>
    </table>

     

## Argomenti correlati


[Amministrazione di UE-V 1.0](administering-ue-v-10.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

 

 





