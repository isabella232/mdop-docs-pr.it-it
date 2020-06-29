---
title: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico
description: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805313"
---
# Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico

**Nota:** App-V 4,6 è uscito dal supporto mainstream.

Usare la procedura seguente per eseguire la migrazione di punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5,0 usando il file di configurazione della distribuzione.

**Nota**  La procedura seguente non richiede un server di gestione di App-V 5,0.

 

**Per eseguire la migrazione di punti di estensione da un pacchetto da un pacchetto App-V 4.6 a un pacchetto convertito App-V 5,0 usando il file di configurazione della distribuzione**

1. Individuare la directory che contiene il file di configurazione della distribuzione per il pacchetto che si vuole eseguire la migrazione. Per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **userConfiguration** :

   **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID pacchetto&gt;**

   Di seguito è riportato un esempio di contenuto di un file di configurazione della distribuzione:

   &lt;? XML version = "1.0"?&gt;

   &lt;DeploymentConfiguration

   xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageID = &lt; ID pacchetto &gt; DisplayName = &lt; nome visualizzato&gt;

   &lt;MachineConfiguration/&gt;

   &lt;UserConfiguration&gt;

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID pacchetto&gt;

   &lt;/UserConfiguration&gt;

   &lt;/DeploymentConfiguration&gt;

2. Per aggiungere il pacchetto App-V 5,0, in un tipo di prompt dei comandi di PowerShell con privilegi elevati:

   PS &gt; **$pkg = Add-AppvClientPackage** **-** path path &lt; to package location &gt;  - **DynamicDeploymentConfiguration** &lt; percorso del file di configurazione della distribuzione&gt;

   PS &gt; **Publish-AppVClientPackage $pkg**

3. Per testare la migrazione, Apri l'applicazione virtuale usando le accordi o i tasti di scelta rapida associati. L'applicazione si apre con App-V 5,0. Sia il pacchetto App-V 4,6 che il pacchetto convertito App-V 5,0 vengono pubblicati per l'utente, ma i accordi e i tasti di scelta rapida per le applicazioni sono stati assunti dal pacchetto App-V 5,0.

   **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





