---
title: Preparazione dell'ambiente per MBAM 2.0
description: Preparazione dell'ambiente per MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825606"
---
# Preparazione dell'ambiente per MBAM 2.0


Prima di iniziare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), verificare di avere soddisfatto i prerequisiti per installare il prodotto. Quando si sa quali sono i prerequisiti in anticipo, è possibile distribuire il prodotto in modo efficiente e abilitarne le funzionalità per consentire il supporto più efficace degli obiettivi aziendali dell'organizzazione.

Se si distribuisce l'amministrazione e il monitoraggio di Microsoft BitLocker con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

## Verificare i prerequisiti di distribuzione di MBAM 2,0


Il client MBAM e ognuna delle funzionalità di MBAM server presentano prerequisiti specifici che devono essere soddisfatti prima che possano essere installati correttamente.

Per garantire l'installazione di successo di MBAM client e le caratteristiche del server MBAM, assicurarsi che i computer specificati per MBAM client o MBAM Server funzionalità di installazione sono adeguatamente preparati per la configurazione MBAM.

**Nota**  La configurazione di MBAM controlla che tutti i prerequisiti vengano soddisfatti prima dell'avvio dell'installazione. Se non sono soddisfatti tutti i prerequisiti, il programma di installazione avrà esito negativo.

 

[Prerequisiti per la distribuzione di MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

## Pianificare i requisiti di criteri di gruppo di MBAM 2,0


Prima che MBAM possa gestire i client nell'organizzazione, è necessario definire criteri di gruppo per i requisiti di crittografia dell'ambiente.

**Importante**  MBAM non funziona con i criteri per la crittografia unità BitLocker autonoma. Le impostazioni dei criteri di gruppo devono essere definite per MBAM o la crittografia e l'imposizione di BitLocker non avranno esito negativo.

 

[Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## Pianificare i ruoli di amministratore di MBAM 2,0


I ruoli di amministratore di MBAM sono gestiti da gruppi locali creati dalla configurazione di MBAM quando si installa il server di amministrazione e monitoraggio di BitLocker, la caratteristica rapporti di conformità e controllo e il database di stato di conformità e controllo.

L'appartenenza ai ruoli di amministrazione e monitoraggio di Microsoft BitLocker può essere gestita in modo ottimale tramite la creazione di gruppi di sicurezza in ActiveDirectoryDomainServices, l'aggiunta degli account di amministratore appropriati a tali gruppi e quindi l'aggiunta di tali gruppi di sicurezza ai gruppi locali di amministrazione e monitoraggio di BitLocker. Per altre informazioni, Vedi [come gestire i ruoli di amministratore di mbam](how-to-manage-mbam-administrator-roles-mbam-2.md).

## Altre risorse per la pianificazione di MBAM


[Pianificazione di MBAM 2.0](planning-for-mbam-20-mbam-2.md)

[Configurazioni supportate di MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)

 

 





