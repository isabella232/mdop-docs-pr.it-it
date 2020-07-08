---
title: Risoluzione dei problemi relativi agli aggiornamenti Advanced Group Policy
description: Risoluzione dei problemi relativi agli aggiornamenti Advanced Group Policy
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818246"
---
# Risoluzione dei problemi relativi agli aggiornamenti Advanced Group Policy

In questa sezione vengono elencati i problemi comuni che possono verificarsi quando si aggiorna il server Advanced Group Policy Management in una versione più recente, ad esempio Advanced Group Policy Manager 4,0, in Advanced Group Management 4,3. Per diagnosticare i problemi non elencati in questo articolo, potrebbe essere utile visualizzare la [risoluzione dei problemi di Advanced Group Policy Management](troubleshooting-agpm-agpm40.md) o per un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per usare la registrazione e la traccia. Per altre informazioni, vedere [configurare la registrazione e la traccia](configure-logging-and-tracing-agpm40.md).

## Quali problemi si verificano?

-   [Non è possibile generare un report di differenza GPO HTML (codice di errore 80004003)](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a>Non è possibile generare un report di differenza GPO HTML (codice di errore 80004003)

-   **Causa**: il pacchetto di aggiornamento della Advanced Group Policy è stato installato con un account errato.

-   **Soluzione**: è necessario essere un amministratore della Advanced Group Policy Management per risolvere il problema.
    
    -   Verificare di conoscere il nome utente & la password dell' **account del servizio Advanced Group Policy Management**.

    -   Accedere in modo interattivo al server Advanced Group Policy Management come account del servizio Advanced Group Policy Management.
        
        -   Questa operazione è di importanza cruciale, perché l'installazione non riesce se si usa un account diverso.

    -   Arrestare il servizio Advanced Group Policy Management.
    
    -   Installare l'hotfix necessario.
    
    -   Connettersi a Advanced Group Policy Management usando un client Advanced Group Policy Management per verificare che i report delle differenze funzionino.
    
## Installare il pacchetto hotfix 1 per Microsoft Advanced Group Policy Management 4,0 SP3
    
**Problema risolto in questo hotfix**: Advanced Group Policy Management non può generare report di differenza quando controlla o gestisce nuovi oggetti Criteri di gruppo.

**Come ottenere questo aggiornamento**: installare l'ultima versione di Microsoft Desktop Optimization Pack ([versione di manutenzione di 2017 marzo](https://www.microsoft.com/download/details.aspx?id=54967)). Per altre informazioni, vedere [KB 4014009](https://support.microsoft.com/help/4014009/) .

In particolare, è possibile scegliere di scaricare solo il primo file, `AGPM4.0SP1_Server_X64_KB4014009.exe` dall'elenco presentato dopo aver premuto il pulsante download.
      
Il collegamento per il download al Microsoft Desktop Optimization Pack (versione di manutenzione di marzo 2017) può essere trovato [qui](https://www.microsoft.com/download/details.aspx?id=54967).
      
      
## Collegamento di riferimento
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
