---
title: Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager
description: Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804323"
---
# Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager


Se si sta installando Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando la funzionalità di integrazione di System Center Configuration Manager, è necessario completare i prerequisiti descritti in questo argomento, oltre a quelli nei [prerequisiti di MBAM 2,5 Server per le topologie di integrazione di gestione autonoma e configurazione](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md). È inoltre necessario creare o modificare i file MOF necessari per la topologia di integrazione di Configuration Manager.

## Prerequisiti per la funzionalità di integrazione di Configuration Manager


Se si sta configurando MBAM con la topologia di integrazione di System Center Configuration Manager, è necessario completare i prerequisiti aggiuntivi necessari per Configuration Manager.

[Prerequisiti per la funzionalità di integrazione di Configuration Manager](prerequisites-for-the-configuration-manager-integration-feature.md)

## Modificare il file Configuration. mof


Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file Configuration. mof per SystemCenter2012 ConfigurationManager e Microsoft System Center Configuration Manager 2007.

[Modificare il file Configuration.mof](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Creare o modificare il file SMS \ _def. mof


Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker nei report di MBAM Configuration Manager, è necessario creare o modificare il file SMS \ _def. mof. Se si usa il ConfigurationManager di SystemCenter2012, è necessario creare il file. In Configuration Manager 2007 il file esiste già, quindi è necessario modificare, ma non sovrascrivere, il file esistente.

[Creare o modificare il file SMS \ _def. mof](create-or-edit-the-sms-defmof-file-mbam-25.md)


## Argomenti correlati


[Preparazione dell'ambiente per MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Configurazioni supportate di MBAM 2.5](mbam-25-supported-configurations.md)

[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




