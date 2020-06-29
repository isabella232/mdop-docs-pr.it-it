---
title: Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo
description: Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805266"
---
# Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo


Usare il modello ADMX di Microsoft Application Virtualization (App-V) 5,1 per configurare le impostazioni del client App-V 5,1 tramite il modello ADMX e i criteri di gruppo.

**Per modificare la configurazione client di App-V 5,1 con criteri di gruppo**

1.  Per modificare la configurazione del client App-V 5,1, individuare i file di **ADMXTemplate** disponibili in App-v 5,1.

    **Nota**  Usare il collegamento seguente per scaricare i **modelli di ADMX**App-V 5,1: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  Nel computer in cui vengono gestiti i criteri di gruppo, in genere il controller di dominio, copiare il file con estensione **ADMX** modello nella directory seguente: ** &lt; unità di installazione &gt; \ \ Windows \ \ PolicyDefinitions**.

    Nello stesso computer copiare quindi il file con estensione **ADML** nella directory seguente: ** &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US**.

3.  Dopo aver copiato i file, aprire la console di gestione di criteri di gruppo per modificare i criteri associati ai client App-v 5,1 individuare i criteri di **configurazione dei computer**  /  **Policies**  /  **modelli amministrativi**  /  **System**  /  **App-v**.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Distribuzione di App-V 5.1](deploying-app-v-51.md)

[Informazioni sulle impostazioni di configurazione client](about-client-configuration-settings51.md)

 

 





