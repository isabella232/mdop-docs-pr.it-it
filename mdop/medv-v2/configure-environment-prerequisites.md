---
title: Configurare i prerequisiti di ambiente
description: Configurare i prerequisiti di ambiente
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826446"
---
# Configurare i prerequisiti di ambiente


Prima di poter distribuire ed eseguire Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, è necessario assicurarsi che l'ambiente soddisfi i prerequisiti minimi seguenti.

**Windows 7**

L'agente host MED-V e il Packager area di lavoro MED-V sono supportati solo in Windows 7 o versioni successive.

**Windows XP SP3**

L'agente guest MED-V è supportato solo in Windows XP SP3.

**.NET Framework 3,5 SP1**

Gli agenti Guest e host MED-V e Packager area di lavoro MED-V richiedono Microsoft .NET Framework 3,5 SP1.

**Importante**  È inoltre necessario installare l'aggiornamento [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) https://go.microsoft.com/fwlink/?LinkId=204950) , che affronta diversi problemi noti di compatibilità delle applicazioni.

 

**Nota**  È necessario installare manualmente .NET Framework 3,5 SP1 e l'aggiornamento di KB959209 nell'immagine di Windows Virtual PC preparata per l'uso con MED-V. Per impostazione predefinita, tuttavia, Microsoft .NET Framework 3,5 SP1 e l'aggiornamento sono inclusi quando si installa Windows 7 nel computer host.

 

**Infrastruttura di Active Directory**

Criteri di gruppo offre la gestione centralizzata e la configurazione di sistemi operativi, applicazioni e impostazioni degli utenti in un ambiente Active Directory.

## Argomenti correlati


[Configurare i prerequisiti di installazione](configure-installation-prerequisites.md)

[Architettura di alto livello](high-level-architecturemedv2.md)

[Configurazioni supportate di MED-V 2.0](med-v-20-supported-configurations.md)

 

 





