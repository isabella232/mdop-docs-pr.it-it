---
title: Configurazione di App-V per l'amministrazione sicura
description: Configurazione di App-V per l'amministrazione sicura
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821905"
---
# Configurazione di App-V per l'amministrazione sicura


In un ambiente in cui è importante proteggere le operazioni amministrative, App-V consente la comunicazione sicura tra il servizio di gestione Web App-V e la console di gestione di App-V. Poiché il servizio di gestione è un'applicazione basata sul Web, è necessario proteggere l'applicazione App-V Management Server nel server Web che ospita il servizio di gestione. Come illustrato nella figura seguente, questo processo include l'uso di HTTPS per la comunicazione e la configurazione del server IIS per consentire solo l'autenticazione integrata di Windows.

![configurazione di rete del servizio Web App-v](images/appvmgmtwebservice.gif)

Il servizio di gestione Web App-V viene installato come applicazione basata sul Web in IIS. Per il servizio di gestione Web per supportare connessioni sicure (SSL) tra la console di gestione di App-V e il servizio di gestione Web, sarà necessario configurare il server IIS in cui è installato il servizio di gestione Web e configurare App-V Management Console.

## In questa sezione


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Configurazione dei certificati per supportare il Servizio gestione Web di App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Fornisce informazioni utili sulla configurazione dei certificati per il supporto delle connessioni basate su SSL, per facilitare la comunicazione sicura per il servizio di gestione Web App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Come installare e configurare App-V Management Console per un ambiente più sicuro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Fornisce una procedura dettagliata per la connessione a un servizio di gestione Web App-V tramite una connessione sicura.

 

 





