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
ms.openlocfilehash: c95fab4b2b4f402df4ff0f82f2f346c9bd226e00
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910481"
---
# <a name="configuring-app-v-for-secure-administration"></a>Configurazione di App-V per l'amministrazione sicura


In un ambiente in cui la protezione delle operazioni amministrative è importante, App-V consente comunicazioni protette tra il servizio di gestione Web app-V e la console di gestione di App-V. Poiché il servizio di gestione è un'applicazione basata sul Web, richiede la protezione dell'applicazione del server di gestione App-V nel server Web che ospita il servizio di gestione. Come illustrato nella figura seguente, questo processo include l'utilizzo di HTTPS per la comunicazione e la configurazione del server IIS in modo da consentire solo l Windows a autenticazione integrata.

![configurazione di rete del servizio Web app-v.](images/appvmgmtwebservice.gif)

Il servizio di gestione Web App-V viene installato come applicazione basata sul Web in IIS. Perché il servizio di gestione Web supporti connessioni protette (SSL) tra la console di gestione di App-V e il servizio di gestione Web, sarà necessario configurare il server IIS in cui è installato il servizio di gestione Web e configurare la console di gestione di App-V.

## <a name="in-this-section"></a>In questa sezione


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Configurazione dei certificati per supportare il Servizio gestione Web di App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Fornisce informazioni utili sulla configurazione dei certificati per supportare le connessioni basate su SSL, per proteggere le comunicazioni per il servizio di gestione Web app-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Come installare e configurare App-V Management Console per un ambiente più sicuro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Viene illustrata una procedura dettagliata per la connessione a un servizio di gestione Web app-V tramite una connessione protetta.

 

 





