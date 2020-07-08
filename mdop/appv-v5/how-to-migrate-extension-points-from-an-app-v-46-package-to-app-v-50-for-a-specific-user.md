---
title: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico
description: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805307"
---
# Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico

*Nota:** App-V 4,6 è uscito dal supporto mainstream.

Usare la procedura seguente per eseguire la migrazione dei pacchetti creati con App-V usando il file di configurazione dell'utente.

**Per convertire un pacchetto**

1. Individuare il file di configurazione dell'utente per il pacchetto che si vuole convertire. Per impostare il criterio, eseguire gli aggiornamenti seguenti nella sezione **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; pacchetto**.

   Di seguito è riportato un esempio di file di configurazione utente:

   &lt;? XML version = "1.0"?&gt;

   &lt;UserConfiguration PackageId = &lt; ID pacchetto &gt; DisplayName = &lt; nome del pacchetto&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID pacchetto&gt;

   &lt;/UserConfiguration&gt;

2. Per aggiungere il pacchetto App-V 5,0, digitare quanto segue in un prompt dei comandi di PowerShell con privilegi elevati:

   PS &gt; **$pkg = Add-AppvClientPackage-** percorso percorso della &lt; posizione del pacchetto&gt;

   PS &gt; **Publish-AppVClientPackage $pkg-percorso DynamicUserConfiguration** &lt; del file di configurazione utente&gt;

3. Aprire l'applicazione usando accordi o i tasti di scelta rapida ora. L'applicazione deve essere aperta usando App-V 5,0.

   Il pacchetto App-V SP2 e il pacchetto convertito App-V 5,0 vengono pubblicati per l'utente, ma i accordi e i tasti di scelta rapida per le applicazioni sono stati assunti dal pacchetto App-V 5,0.

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





