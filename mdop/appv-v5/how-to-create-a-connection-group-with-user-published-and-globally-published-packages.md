---
title: Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente
description: Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805662"
---
# Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente
È possibile creare gruppi di connessioni autorizzati dall'utente che contengono sia i pacchetti pubblicati dall'utente che quelli pubblicati a livello globale, usando uno dei metodi seguenti:

-   [Come usare i cmdlet di PowerShell per creare i gruppi di connessioni autorizzati dall'utente](#bkmk-posh-userentitled-cg)

-   [Come usare app-V Server per creare i gruppi di connessioni autorizzati dall'utente](#bkmk-appvserver-userentitled-cg)

**Informazioni da conoscere prima di iniziare:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Scenari non supportati e potenziali problemi</th>
<th align="left">Risultato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Non è possibile includere pacchetti pubblicati dall'utente in gruppi di connessioni autorizzati a livello globale.</p></td>
<td align="left"><p>Il gruppo di connessioni avrà esito negativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Se si pubblica un pacchetto a livello globale e quindi si crea un gruppo di connessioni pubblicato dall'utente in cui è stato reso non facoltativo il pacchetto, è comunque possibile eseguire <strong> il pacchetto Unpublish-AppvClientPackage &lt; &gt; -Global </strong> per annullare la pubblicazione del pacchetto, anche quando il pacchetto viene usato in un altro gruppo di connessioni.</p></td>
<td align="left"><p>Se un altro gruppo di connessioni usa il pacchetto, il pacchetto non riuscirà in questi gruppi di connessioni.</p>
<p>Per evitare di non pubblicare inavvertitamente un pacchetto non facoltativo usato in un altro gruppo di connessioni, è consigliabile tenere traccia dei gruppi di connessioni in cui è stato usato un pacchetto non facoltativo.</p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**Come usare i cmdlet di PowerShell per creare gruppi di connessioni autorizzati dall'utente**

1.  Aggiungere e pubblicare pacchetti usando i comandi seguenti:

    **Add-AppvClientPackage package1 \ _AppV \ _file \ _Path**

    **Add-AppvClientPackage Package2 \ _AppV \ _file \ _Path**

    **Publish-AppvClientPackage-PackageId package1 \ _ID-VersionId package1 \ _Version ID-globale**

    **Publish-AppvClientPackage-PackageId Package2 \ _ID-VersionIdPackage2 \ _ID**

2.  Creare il file XML del gruppo di connessioni. Per altre informazioni, vedere [informazioni sul file del gruppo di connessioni](about-the-connection-group-file.md).

3.  Aggiungere e pubblicare il gruppo di connessioni usando i comandi seguenti:

    **Connessione Add-AppvClientConnectionGroup \ _Group \ _XML \ _file \ _Path**

    **Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**Come usare app-V Server per creare gruppi di connessioni autorizzati dall'utente**

1.  Aprire la console di gestione di App-V 5,0.

2.  Seguire le istruzioni fornite in [come pubblicare un pacchetto usando la console di gestione](how-to-publish-a-package-by-using-the-management-console-50.md) per pubblicare i pacchetti a livello globale e per l'utente.

3.  Seguire le istruzioni fornite in [come creare un gruppo di connessioni](how-to-create-a-connection-group.md) per creare il gruppo di connessioni e aggiungere i pacchetti pubblicati dall'utente e a livello globale.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Gestione dei gruppi di connessione](managing-connection-groups.md)

[Come usare i pacchetti facoltativi nei gruppi di connessione](how-to-use-optional-packages-in-connection-groups.md)

 

 





