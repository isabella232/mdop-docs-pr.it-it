---
title: Come configurare il client per il supporto per le aree di autenticazione MIT Kerberos
description: Come configurare il client per il supporto per le aree di autenticazione MIT Kerberos
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817815"
---
# Come configurare il client per il supporto per le aree di autenticazione MIT Kerberos


In Application Virtualization (App-V) 4,5 SP1 è stato aggiunto il supporto per gli ambiti di autenticazione Kerberos MIT. Questo argomento fornisce informazioni dettagliate su come abilitare tale supporto.

**Per abilitare il supporto per gli ambiti di autenticazione Kerberos MIT**

-   Creare una nuova chiave del registro di sistema denominata **UseMITKerberos** di tipo DWORD, come indicato di seguito, quindi impostarla su un valore pari a 1.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos

 

 





