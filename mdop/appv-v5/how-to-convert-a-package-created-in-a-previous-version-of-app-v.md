---
title: Come convertire un pacchetto creato in una versione precedente di App-V
description: Come convertire un pacchetto creato in una versione precedente di App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805668"
---
# Come convertire un pacchetto creato in una versione precedente di App-V


Puoi usare l'utilità Convertitore pacchetti per aggiornare i pacchetti di applicazioni virtuali creati con le versioni precedenti di App-V.

**Nota**  
Se si esegue un computer con un'architettura a 64 bit, è necessario usare la versione x86 di PowerShell.



Il convertitore di pacchetti può convertire direttamente i pacchetti creati usando l'App-V 4,5 Sequencer o una versione successiva. I pacchetti creati con una versione precedente a App-V 4,5 devono essere aggiornati al formato App-V 4,5 o App-V 4,6 prima della conversione.

Le informazioni seguenti forniscono indicazioni per la conversione di pacchetti di applicazioni virtuali esistenti.

**Importante**  
È necessario configurare il convertitore di pacchetti per salvare sempre il file degli ingredienti del pacchetto in un percorso e una directory sicuri. Un percorso sicuro è accessibile solo da un amministratore. Inoltre, quando si distribuisce il pacchetto, è necessario salvare il pacchetto in una posizione sicura oppure assicurarsi che durante il processo di conversione non sia consentito l'accesso a nessun altro utente.



**Attività iniziali**

1.  Installare App-V Sequencer in un computer nell'ambiente. Per informazioni su come installare il sequencer, vedere [come installare Sequencer](how-to-install-the-sequencer-beta-gb18030.md).

2. Importare il modulo di PowerShell necessario

```powershell
Import-Module AppVPkgConverter
```

3. Sono disponibili i cmdlet seguenti:

   -   Test-AppvLegacyPackage: questo cmdlet è progettato per controllare i pacchetti. Restituirà informazioni su eventuali errori con il pacchetto, ad esempio file mancanti **. SFT** , un'origine non valida, errori di file **OSD** o una versione del pacchetto non valida. Questo cmdlet non analizzerà il file con **estensione SFT** o convaliderà in modo approfondito. Per informazioni sulle opzioni e le funzionalità di base per questo cmdlet, usare PowerShell cmdline digitare `Test-AppvLegacyPackage -?` .

   -   ConvertFrom-AppvLegacyPackage-per convertire un pacchetto esistente, digitare `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` . In questo comando `c:\contentStore` rappresenta la posizione del pacchetto esistente ed `c:\convertedPackages` è la directory di output in cui verrà salvato il file del pacchetto di applicazione virtuale App-V 5,0 risultante. Per impostazione predefinita, se non si specifica un nuovo nome, verrà usato il nome del pacchetto precedente per il nome del file App-V 5,0.

       Inoltre, il convertitore di pacchetti ottimizza le prestazioni dei pacchetti in App-V 5,0 impostando il pacchetto in streaming fault il pacchetto App-V.  Questo è più efficiente del blocco di funzionalità principale e scarica completamente il pacchetto. Il contrassegno **DownloadFullPackageOnFirstLaunch** consente di convertire il pacchetto e di impostare il pacchetto da scaricare completamente per impostazione predefinita.

       **Nota**  
       Prima di specificare la directory di output, è necessario creare la directory di output.



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)









