---
title: Pianificazione della distribuzione di MBAM 2.0
description: Pianificazione della distribuzione di MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825635"
---
# Pianificazione della distribuzione di MBAM 2.0


Prima di creare il piano di distribuzione per Microsoft BitLocker Administration and Monitoring (MBAM), è consigliabile prendere in considerazione diverse configurazioni e prerequisiti di distribuzione. Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali. Se si sta installando MBAM con la topologia di Configuration Manager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) per altre informazioni sulla pianificazione.

## Esaminare le configurazioni supportate di MBAM 2,0


Dopo aver preparato l'ambiente di calcolo per l'installazione di MBAM server e client, assicurati di rivedere le configurazioni supportate per verificare che i computer in cui si sta installando MBAM soddisfino i requisiti minimi per l'hardware e il sistema operativo. Per altre informazioni sui prerequisiti di distribuzione di MBAM, vedi i prerequisiti per la [distribuzione di mbam 2,0](mbam-20-deployment-prerequisites-mbam-2.md).

[Configurazioni supportate di MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)

## Pianificare la distribuzione di MBAM 2,0 Server e client


L'infrastruttura di MBAM Server dipende da un set di funzionalità del server che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione. Queste funzionalità possono essere installate in una configurazione distribuita in più server.

**Nota**  Un'installazione di MBAM su un singolo server è consigliata solo per gli ambienti Lab.

 

Il client MBAM consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione del software aziendale o installando l'agente client nei computer client come parte del processo di imaging iniziale.

Con MBAM è possibile crittografare un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito tramite criteri di gruppo.

[Pianificazione della distribuzione del server di MBAM 2.0](planning-for-mbam-20-server-deployment-mbam-2.md)

[Pianificazione della distribuzione del client di MBAM 2.0](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Altre risorse per la pianificazione di MBAM


[Pianificazione di MBAM 2.0](planning-for-mbam-20-mbam-2.md)

 

 





