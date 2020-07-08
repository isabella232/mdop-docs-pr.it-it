---
ms.reviewer: ''
title: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico
description: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805205"
---
# Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico

*Nota:** App-V 4,6 è uscito dal supporto mainstream.

Usare la procedura seguente per ripristinare un pacchetto App-V 5,0 nel formato di file App-V usando il file di configurazione dell'utente.

**Per ripristinare un pacchetto**

1.  Assicurati che il pacchetto App-V 4,6 venga pubblicato dagli utenti, ma i accordi e i tasti di scelta rapida sono stati assunti dal pacchetto App-V 5,0 usando il metodo di migrazione seguente, [come eseguire la migrazione dei punti di estensione da un pacchetto App-v 4,6 a App-v 5,0 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).

    Nella sezione **userConfiguration** del file di configurazione della distribuzione per il pacchetto convertito, per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; pacchetto**

2.  Da un prompt dei comandi con privilegi elevati digitare:

    PS &gt; **Publish-AppVClientPackage $pkg** -percorso DynamicUserConfigurationPath del &lt; file di configurazione utente&gt;

3.  Eseguire un aggiornamento della pubblicazione o attendere il prossimo aggiornamento della pubblicazione pianificata per l'App-V 4,6. Aprire l'applicazione usando accordi o i tasti di scelta rapida. L'applicazione deve ora aprirsi usando App-V 4,6 SP2.

    **Nota**  
    Se non è più necessario il pacchetto App-V 5,0, è possibile annullare la pubblicazione del pacchetto App-V 5,0 e i punti di estensione verranno ripristinati automaticamente in App-V 4,6.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)












