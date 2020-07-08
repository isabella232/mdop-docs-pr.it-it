---
title: Pianificazione della distribuzione di MBAM 1.0
description: Pianificazione della distribuzione di MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823186"
---
# Pianificazione della distribuzione di MBAM 1.0


Prima di creare il piano di distribuzione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 1,0, è necessario considerare un certo numero di configurazioni e prerequisiti di distribuzione diversi. Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali.

## Esaminare le configurazioni supportate di MBAM 1,0


Dopo aver preparato l'ambiente di elaborazione per l'installazione di MBAM client e server, assicurati di rivedere le informazioni sulle configurazioni supportate per MBAM per verificare che i computer in cui si installano MBAM soddisfino i requisiti minimi per l'hardware e il sistema operativo. Per altre informazioni sui prerequisiti di distribuzione di MBAM, vedi i prerequisiti per la [distribuzione di mbam 1,0](mbam-10-deployment-prerequisites.md).

[Configurazioni supportate di MBAM 1.0](mbam-10-supported-configurations.md)

## Pianificare la distribuzione di MBAM 1,0 Server e client


L'infrastruttura di MBAM Server dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione. Queste funzionalità possono essere installate in un singolo server o distribuite in più server.

Il client MBAM consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite strumenti come servizi di dominio Active Directory oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.

Con MBAM è possibile crittografare un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito usando criteri di gruppo. Puoi usare uno o entrambi i metodi dell'organizzazione. Se si sceglie di usare entrambi i metodi, è possibile migliorare la conformità, la creazione di report e il supporto per il recupero della chiave.

[Pianificazione della distribuzione del server di MBAM 1.0](planning-for-mbam-10-server-deployment.md)

[Pianificazione della distribuzione del client di MBAM 1.0](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Altre risorse per la pianificazione di MBAM


-   [Pianificazione di MBAM 1.0](planning-for-mbam-10.md)

 

 





