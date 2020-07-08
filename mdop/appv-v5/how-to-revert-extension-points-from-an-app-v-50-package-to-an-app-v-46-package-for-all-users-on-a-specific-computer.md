---
title: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
description: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805194"
---
# Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico

*Nota:** App-V 4,6 è uscito dal supporto mainstream. Il seguente presuppone che il client App-V 4,6 SP3 sia già installato.

Usare la procedura seguente per ripristinare i punti di estensione da un pacchetto App-V 5,0 al formato di file App-V 4,6 usando il file di configurazione della distribuzione.

**Per ripristinare un pacchetto**

1.  Assicurati che il pacchetto App-V 4,6 venga pubblicato dagli utenti, ma i accordi e i tasti di scelta rapida sono stati assunti dal pacchetto App-V 5,0 usando il metodo di migrazione seguente, [come eseguire la migrazione dei punti di estensione da un pacchetto App-v 4,6 a un pacchetto di App-v 5,0 convertito per tutti gli utenti di un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).

    Nella sezione **userConfiguration** del file di configurazione della distribuzione per il pacchetto convertito, per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; pacchetto**

2.  Da un prompt dei comandi con privilegi elevati digitare:

    PS &gt; **set-AppvClientPackage $pkg** -percorso DynamicDeploymentConfiguration del &lt; file di configurazione della distribuzione&gt;

    PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**

3.  Eseguire un aggiornamento della pubblicazione o attendere il prossimo aggiornamento della pubblicazione pianificata per il pacchetto App-V 4,6 SP2.

    Aprire l'applicazione usando accordi o i tasti di scelta rapida. L'applicazione deve ora aprirsi usando App-V 4,6.

    **Nota**  
    Se non è più necessario il pacchetto App-V 5,0, è possibile annullare la pubblicazione del pacchetto App-V 5,0 e i punti di estensione verranno ripristinati automaticamente in App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)









