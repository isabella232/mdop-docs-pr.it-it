---
title: Scheda generale delle proprietà di Application Virtualization
description: Scheda generale delle proprietà di Application Virtualization
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819686"
---
# Proprietà Application Virtualization: Scheda Generale


Usare la scheda **generale** della finestra di dialogo **Proprietà Application Virtualization** per modificare le impostazioni del log e le posizioni dei dati.

Questa scheda contiene gli elementi seguenti.

<a href="" id="log-level"></a>**Livello di log**  
Selezionare il livello nell'elenco a discesa. Il livello predefinito è le **informazioni**.

<a href="" id="reset-log"></a>**Reimposta log**  
Fare clic su questo pulsante per eseguire il backup del file di log corrente e avviare immediatamente un nuovo file di log.

<a href="" id="location"></a>**Posizione**  
Immettere o passare al percorso in cui si vuole salvare il file di log sftlog.txt. I percorsi predefiniti sono i seguenti:

-   Per WindowsXP, Windows Server2003 —*c:\\Documents and e Settings\\All Users\\Application Data\\Microsoft\\Application client di virtualizzazione*

-   Per Windows Vista, Windows 7, Windows Server2008 —*client di virtualizzazione C:\\ProgramData\\Microsoft\\Application*

<a href="" id="system-log-level"></a>**Livello di registro di sistema**  
Selezionare il livello nell'elenco a discesa. Il livello predefinito è **warning**.

**Nota**  L'impostazione **livello registro di sistema** controlla il livello di messaggi inviati al log eventi di sistema. I messaggi registrati sono identici ai messaggi che vengono registrati nel log eventi del client, ma archiviati in una posizione diversa che non ha le limitazioni di spazio del log eventi del client. Poiché il log eventi di sistema non ha limitazioni di spazio, è ideale per le situazioni in cui è necessaria la registrazione dettagliata.

 

<a href="" id="global-data-directory"></a>**Directory dati globale**  
Immettere o passare al percorso della directory del file di log. I percorsi predefiniti sono i seguenti:

-   Per WindowsXP, Windows Server2003 —*c:\\Documents and e Settings\\All Users\\Application Data\\Microsoft\\Application client di virtualizzazione*

-   Per Windows Vista, Windows 7, Windows Server2008 —*client di virtualizzazione C:\\ProgramData\\Microsoft\\Application*

<a href="" id="user-data-directory"></a>**Directory dati utente**  
Immettere o passare al percorso della directory in cui sono archiviati i dati specifici dell'utente. Il valore predefinito è% APPDATA%. Questo percorso deve essere una variabile di ambiente valida nel computer client.

## Argomenti correlati


[Client Management Console: Proprietà Application Virtualization](client-management-console-application-virtualization-properties.md)

 

 





