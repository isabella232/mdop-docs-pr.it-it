---
title: Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
description: Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805193"
---
# Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico


Usare la procedura seguente per ripristinare i punti di estensione da un pacchetto App-V 5,1 al formato di file App-V 4,6 usando il file di configurazione della distribuzione.

**Per ripristinare un pacchetto**

1.  Assicurati che il pacchetto App-V 4,6 venga pubblicato dagli utenti, ma i accordi e i tasti di scelta rapida sono stati assunti dal pacchetto App-V 5,1 usando il metodo di migrazione seguente, [come eseguire la migrazione dei punti di estensione da un pacchetto App-v 4,6 a un pacchetto di App-v 5,1 convertito per tutti gli utenti di un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).

    Nella sezione **userConfiguration** del file di configurazione della distribuzione per il pacchetto convertito, per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; pacchetto**

2.  Da un prompt dei comandi con privilegi elevati digitare:

    PS &gt; **set-AppvClientPackage $pkg** -percorso DynamicDeploymentConfiguration del &lt; file di configurazione della distribuzione&gt;

    PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**

3.  Eseguire un aggiornamento della pubblicazione o attendere il prossimo aggiornamento della pubblicazione pianificata per il pacchetto App-V 4,6.

    Aprire l'applicazione usando accordi o i tasti di scelta rapida. L'applicazione deve ora aprirsi usando App-V 4,6.

    **Nota**  
    Se non è più necessario il pacchetto App-V 5,1, è possibile annullare la pubblicazione del pacchetto App-V 5,1 e i punti di estensione verranno ripristinati automaticamente in App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)









