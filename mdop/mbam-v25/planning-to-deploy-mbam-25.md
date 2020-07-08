---
title: Pianificazione della distribuzione di MBAM 2.5
description: Pianificazione della distribuzione di MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826695"
---
# Pianificazione della distribuzione di MBAM 2.5


Prima di creare il piano di distribuzione per Microsoft BitLocker Administration and Monitoring (MBAM), è consigliabile prendere in considerazione diverse configurazioni e prerequisiti di distribuzione. Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali.

## Esaminare le configurazioni supportate di MBAM 2,5


Dopo aver preparato l'ambiente di elaborazione per il server MBAM e la distribuzione di funzionalità client, assicurati di rivedere le configurazioni supportate per verificare che i computer in cui si sta installando MBAM soddisfino i requisiti minimi per l'hardware e il sistema operativo. Per altre informazioni sui prerequisiti di distribuzione di MBAM, vedi i prerequisiti per la [distribuzione di mbam 2,5](mbam-25-deployment-prerequisites.md).

[Configurazioni supportate di MBAM 2.5](mbam-25-supported-configurations.md)

## Pianificare la distribuzione di MBAM 2,5 Server e client


L'infrastruttura di MBAM Server dipende da un set di funzionalità del server che possono essere configurate in uno o più computer server, in base ai requisiti dell'organizzazione. Queste funzionalità possono essere configurate in una configurazione distribuita in più server.

**Nota**  Un'installazione di MBAM su un singolo server è consigliata solo per gli ambienti Lab.

 

Il client MBAM consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite un sistema di distribuzione del software aziendale o installando il client nei computer client come parte del processo di imaging iniziale.

Con MBAM è possibile crittografare un computer dell'organizzazione prima che l'utente finale riceva il computer o in seguito tramite criteri di gruppo.

[Pianificazione della distribuzione del server di MBAM 2.5](planning-for-mbam-25-server-deployment.md)

[Pianificazione della distribuzione del client di MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Altre risorse per la pianificazione di MBAM


[Pianificazione di MBAM 2.5](planning-for-mbam-25.md)

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





