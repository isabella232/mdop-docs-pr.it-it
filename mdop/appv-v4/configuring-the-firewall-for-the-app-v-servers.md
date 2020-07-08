---
title: Configurazione del firewall per i server App-V
description: Configurazione del firewall per i server App-V
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821816"
---
# Configurazione del firewall per i server App-V


Dopo aver installato Microsoft Application Virtualization (App-V) Management Server o streaming server e averlo configurato per l'uso del protocollo RTSP o RTSPs, è necessario creare eccezioni del firewall per i programmi App-V.

## Configurazione delle eccezioni del firewall per Application Virtualization Management Server


Creare un'eccezione del firewall per **sghwdsptr.exe** e **sghwsvr.exe**. Questi programmi si trovano nella cartella C:\\Programmi \\Programmi\\microsoft System Center App Virt Management Server\\App Virt Management Server\\bin in un sistema operativo a 32 bit. Se si usa una versione del sistema operativo a 64 bit, la cartella si trova in file C:\\Programmi (x86) \\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.

## Configurazione delle eccezioni del firewall per Application Virtualization Streaming Server


Creare un'eccezione del firewall per **sglwdsptr.exe** e **sglwsvr.exe**. Questi programmi si trovano nella cartella C:\\Programmi \\Programmi\\microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin in un sistema operativo a 32 bit. Se si usa una versione del sistema operativo a 64 bit, la cartella si trova in file C:\\Programmi (x86) \\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.

## Argomenti correlati


[Come configurare i server per la distribuzione basata su server](how-to-configure-servers-for-server-based-deployment.md)

[Come installare e configurare l'applicazione predefinita](how-to-install-and-configure-the-default-application.md)

 

 





