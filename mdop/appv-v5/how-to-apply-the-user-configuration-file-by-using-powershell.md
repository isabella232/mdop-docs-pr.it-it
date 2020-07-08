---
title: Come applicare il file di configurazione utente con PowerShell
description: Come applicare il file di configurazione utente con PowerShell
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805727"
---
# Come applicare il file di configurazione utente con PowerShell


Il file di configurazione dell'utente dinamico viene applicato quando un pacchetto viene pubblicato in un utente specifico e determina il modo in cui verrà eseguito il pacchetto.

Usare la procedura seguente per specificare un file di configurazione specifico dell'utente. La procedura seguente si basa sull'esempio:

**c:\\Packages\\Contoso\\MyApp.appv**

**Per applicare un file di configurazione utente**

1.  Per aggiungere il pacchetto al computer usando la console di PowerShell, digitare il comando seguente:

    **Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.

2.  Usare il comando seguente per pubblicare il pacchetto nell'utente e specificare il file di configurazione dell'utente dinamico aggiornato:

    **Publish-AppVClientPackage $pkg-DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml**

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





