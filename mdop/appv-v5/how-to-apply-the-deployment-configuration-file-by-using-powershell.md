---
title: Come applicare il file di configurazione della distribuzione con PowerShell
description: Come applicare il file di configurazione della distribuzione con PowerShell
author: dansimp
ms.assetid: 5df5d5bc-6c72-4087-8b93-d6d4b502a1f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6764f07dfe8cff1fb30c354937a405202468428
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805733"
---
# Come applicare il file di configurazione della distribuzione con PowerShell


Il file di configurazione della distribuzione dinamica viene applicato quando un pacchetto viene aggiunto o impostato su un computer che gestisce il client App-V 5,0 prima che il pacchetto sia stato pubblicato. Il file configura le impostazioni predefinite per il pacchetto per tutti gli utenti nel computer che gestisce il client App-V 5,0. Questa sezione descrive i passaggi usati per usare un file di configurazione della distribuzione. La procedura si basa sull'esempio seguente e presuppone che il pacchetto e i file di configurazione seguenti siano presenti in un computer:

**c:\\Packages\\Contoso\\MyApp.appv**

**c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

**Per applicare il file di configurazione della distribuzione tramite PowerShell**

-   Per specificare un nuovo set predefinito di configurazioni per tutti gli utenti che eseguiranno il pacchetto in un computer specifico, usando una console di PowerShell, digitare quanto segue:

    **Add-AppVClientPackage – path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

    **Nota**  
    Questo comando acquisisce l'oggetto risultante in $pkg. Se il pacchetto è già presente nel computer, è possibile usare il cmdlet **set-AppVclientPackage** per applicare il documento di configurazione della distribuzione:

    **Set-AppVClientPackage-Name MyApp-path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)









