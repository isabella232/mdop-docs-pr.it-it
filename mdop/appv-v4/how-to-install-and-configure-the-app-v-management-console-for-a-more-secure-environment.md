---
title: Come installare e configurare App-V Management Console per un ambiente più sicuro
description: Come installare e configurare App-V Management Console per un ambiente più sicuro
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817375"
---
# Come installare e configurare App-V Management Console per un ambiente più sicuro


L'installazione predefinita di App-V Management Console include il supporto per le comunicazioni sicure. Ogni console di gestione è configurata in base alle singole connessioni quando la console viene avviata per la prima volta o quando si connette a un altro servizio di gestione Web App-V. La configurazione predefinita Usa SSL sulla porta TCP 443. È possibile modificare il numero di porta se il numero di porta è stato modificato nel server. Per connettersi a un servizio di gestione Web App-V tramite una connessione sicura, è possibile usare la procedura seguente.

**Come connettersi a un servizio di gestione di App-V tramite una connessione SSL**

1.  Avviare l'Application Virtualization Management Console.

2.  Fare clic su **Configura connessione** nel riquadro azioni della console.

3.  Digitare il **nome host del servizio Web**e verificare che sia selezionata l'opzione **Usa connessione sicura** .

    **Importante**  Il nome specificato nel nome host del servizio Web deve corrispondere al nome comune del certificato oppure la connessione avrà esito negativo.

     

4.  Selezionare le credenziali di accesso appropriate e fare clic su **OK**.

## Argomenti correlati


[Configurazione dei certificati per supportare il Servizio gestione Web di App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





