---
title: Come gestire i gruppi di connessione in un computer autonomo con PowerShell
description: Come gestire i gruppi di connessione in un computer autonomo con PowerShell
author: dansimp
ms.assetid: e1589eff-d306-40fb-a0ae-727190dafe26
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ab120f7089619fa01885d5182313dc33fc47f827
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805314"
---
# Come gestire i gruppi di connessione in un computer autonomo con PowerShell


Un gruppo di connessioni App-V consente di eseguire tutte le applicazioni virtuali come set di pacchetti definiti in un unico ambiente virtuale. Ad esempio, puoi virtualizzare un'applicazione e i relativi plug-in usando pacchetti distinti, ma eseguirli insieme in un singolo gruppo di connessioni.

Un file XML del gruppo di connessioni definisce il gruppo di connessioni eseguito nel computer in cui è stato installato il client App-V. Per informazioni sul file XML del gruppo di connessioni e su come configurarlo, vedere [informazioni sul file del gruppo di connessioni](about-the-connection-group-file51.md).

In questo argomento vengono illustrate le procedure seguenti:

-   [Per aggiungere e pubblicare i pacchetti App-V nel gruppo connessione](#bkmk-add-pub-pkgs-in-cg)

-   [Per aggiungere e abilitare il gruppo di connessioni nel client App-V](#bkmk-add-enable-cg-on-clt)

-   [Per abilitare o disabilitare un gruppo di connessioni per un utente specifico](#bkmk-enable-cg-for-user-poshtopic)

-   [Per consentire solo agli amministratori di abilitare i gruppi di connessioni](#bkmk-admin-only-posh-topic-cg)

<a href="" id="bkmk-add-pub-pkgs-in-cg"></a>*Per aggiungere e pubblicare i pacchetti App-V nel gruppo connessione**

1.  Per aggiungere e pubblicare i pacchetti App-V 5,1 nel computer che gestisce il client App-V, digitare il comando seguente:

    Add-AppvClientPackage – path c:\\tmpstore\\quartfin.AppV | Publish-AppvClientPackage

2.  Ripetere il **passaggio 1** di questa procedura per ogni pacchetto nel gruppo di connessioni.

<a href="" id="bkmk-add-enable-cg-on-clt"></a>**Per aggiungere e abilitare il gruppo di connessioni nel client App-V**

1.  Aggiungere il gruppo di connessioni digitando il comando seguente:

    Add-AppvClientConnectionGroup – Path c:\\tmpstore\\financ.xml

2.  Abilitare il gruppo di connessioni digitando il comando seguente:

    Enable-AppvClientConnectionGroup-Name "applicazioni finanziarie"

    Quando nel computer di destinazione vengono eseguite tutte le applicazioni virtuali che si trovano nei pacchetti di membri, verranno eseguite all'interno dell'ambiente virtuale del gruppo di connessioni e saranno disponibili per tutte le applicazioni virtuali degli altri pacchetti del gruppo di connessioni.

<a href="" id="bkmk-enable-cg-for-user-poshtopic"></a>**Per abilitare o disabilitare un gruppo di connessioni per un utente specifico**

1.  Esaminare la descrizione e i requisiti dei parametri:

    -   Il parametro consente a un amministratore di abilitare o disabilitare un gruppo di connessioni per un utente specifico.

    -   Per usare questo parametro è necessario usare il pacchetto hotfix 5 o versioni successive di App-V 5,0 SP2.

    -   Puoi eseguire questo cmdlet dalla sessione utente o amministratore.

    -   Per usare il parametro è necessario avere effettuato l'accesso con le credenziali amministrative.

    -   L'utente finale deve essere connesso.

    -   Devi specificare l'identificatore di sicurezza (SID) dell'utente finale.

2.  USA i cmdlet seguenti e Aggiungi il parametro facoltativo **-UserSID** , dove **-UserSID** rappresenta l'identificatore di sicurezza dell'utente finale (SID):

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Esempi</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Enable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Enable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Disable-AppVClientConnectionGroup</p></td>
    <td align="left"><p>Disable-AppVClientConnectionGroup "ConnectionGroupA"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</p></td>
    </tr>
    </tbody>
    </table>

<a href="" id="bkmk-admin-only-posh-topic-cg"></a>**Per consentire solo agli amministratori di abilitare i gruppi di connessioni**

1.  Esaminare la descrizione e il requisito per l'uso di questo cmdlet:

    -   Usa questo cmdlet e il parametro per configurare il client App-V per consentire solo agli amministratori (non agli utenti finali) di abilitare o disabilitare i gruppi di connessioni.

    -   Per usare questo cmdlet, è necessario utilizzare almeno App-V 5,0 SP3.

2.  Eseguire il cmdlet e il parametro seguenti:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cmdlet</th>
    <th align="left">Parametro e valori</th>
    <th align="left">Esempio</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Set-AppvClientConfiguration</p></td>
    <td align="left"><p>–RequirePublishAsAdmin</p>
    <ul>
    <li><p>0-falso</p></li>
    <li><p>1-vero</p></li>
    </ul></td>
    <td align="left"><p>Set-AppvClientConfiguration-RequirePublishAsAdmin1</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

[Amministrazione di App-V 5.1 con PowerShell](administering-app-v-51-by-using-powershell.md)









