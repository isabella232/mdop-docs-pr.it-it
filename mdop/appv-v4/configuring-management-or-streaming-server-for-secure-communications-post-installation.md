---
title: Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione
description: Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821876"
---
# Configurazione di Management Server o Streaming Server per comunicazioni sicure dopo l'installazione


Se non è stato effettuato il provisioning del certificato corretto prima dell'installazione di App-V Management Server o App-V Streaming Server, l'App-V può essere configurata per una maggiore sicurezza dopo l'installazione iniziale. Puoi configurare App-V Management Server tramite App-V Management Console. Tuttavia, l'App-V Streaming Server viene gestito tramite il registro di sistema. In entrambi i casi, il certificato deve includere l' *utilizzo appropriato delle chiavi estese* (EKU) per l'autenticazione del server e il servizio di rete deve avere accesso in lettura alla chiave privata.

## In questa sezione


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[Come configurare la sicurezza di Management Server dopo l'installazione](how-to-configure-management-server-security-post-installation.md)  
Fornisce una procedura che può essere eseguita dopo l'installazione, usando la console di gestione di App-V, per aggiungere il certificato e configurare App-V Management Server per una maggiore sicurezza.

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[Come configurare la sicurezza di Streaming Server dopo l'installazione](how-to-configure-streaming-server-security-post-installation.md)  
Fornisce una procedura che può essere eseguita dopo l'installazione, per aggiungere il certificato e configurare App-V Streaming Server per una maggiore sicurezza.

<a href="" id="troubleshooting-certificate-permission-issues"></a>[Risoluzione dei problemi di autorizzazione dei certificati](troubleshooting-certificate-permission-issues.md)  
Fornisce indicazioni per la risoluzione dei problemi quando la chiave privata non è stata configurata con l'ACL appropriato per il servizio di rete.

 

 





