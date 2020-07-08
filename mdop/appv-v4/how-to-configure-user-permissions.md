---
title: Come configurare le autorizzazioni utente
description: Come configurare le autorizzazioni utente
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817735"
---
# Come configurare le autorizzazioni utente


È possibile abilitare e disabilitare alcune azioni per gli utenti che non hanno diritti amministrativi modificando i valori chiave nella chiave del registro di sistema **delle autorizzazioni** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions). Questa chiave è progettata principalmente per impedire agli utenti di commettere errori anziché fornire una sicurezza speciale, perché gli utenti con diritti amministrativi possono modificare uno di questi valori chiave. Le procedure seguenti sono esempi di come modificare i valori di chiave. Per altre informazioni sulle chiavi e i valori del registro di sistema client Application Virtualization (App-V), vedere <https://go.microsoft.com/fwlink/?LinkId=121528> .

**Per modificare le autorizzazioni utente**

1.  Per consentire agli utenti di scegliere di eseguire il client in modalità offline, impostare il valore della chiave seguente su 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode

2.  Per consentire agli utenti di visualizzare tutte le applicazioni tramite l'interfaccia utente, impostare il valore della chiave seguente su 1. L'impostazione del valore su 0 (zero) consente agli utenti di visualizzare solo le applicazioni disponibili.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications

## Argomenti correlati


[Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[Autorizzazioni di accesso utente in Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





