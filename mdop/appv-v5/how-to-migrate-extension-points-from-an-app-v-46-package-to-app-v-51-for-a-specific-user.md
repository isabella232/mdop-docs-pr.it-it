---
title: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.1 per un utente specifico
description: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.1 per un utente specifico
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805301"
---
# Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.1 per un utente specifico


Usare la procedura seguente per eseguire la migrazione dei pacchetti creati con App-V usando il file di configurazione dell'utente.

**Nota**  Questa procedura presuppone che si esegua l'ultima versione di App-V 4,6.

**Per convertire un pacchetto**

1. Individuare il file di configurazione dell'utente per il pacchetto che si vuole convertire. Per impostare il criterio, eseguire gli aggiornamenti seguenti nella sezione **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; pacchetto**.

   Di seguito è riportato un esempio di file di configurazione utente:

   &lt;? XML version = "1.0"?&gt;

   &lt;UserConfiguration PackageId = &lt; ID pacchetto &gt; DisplayName = &lt; nome del pacchetto&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID pacchetto&gt;

   &lt;/UserConfiguration&gt;

2. Per aggiungere il pacchetto App-V 5,1, digitare quanto segue in una finestra del prompt dei comandi di PowerShell con privilegi elevati:

   PS &gt; **$pkg = Add-AppvClientPackage-** percorso percorso della &lt; posizione del pacchetto&gt;

   PS &gt; **Publish-AppVClientPackage $pkg-percorso DynamicUserConfiguration** &lt; del file di configurazione utente&gt;

3. Aprire l'applicazione usando accordi o i tasti di scelta rapida ora. L'applicazione deve essere aperta usando App-V 5,1.

   Il pacchetto App-V 4,6 e il pacchetto convertito App-V 5,1 vengono pubblicati per l'utente, ma i accordi e i tasti di scelta rapida per le applicazioni sono stati assunti dal pacchetto App-V 5,1.

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

[Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per un utente specifico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





