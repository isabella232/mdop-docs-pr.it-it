---
title: Preparazione dell'ambiente per MBAM 1.0
description: Preparazione dell'ambiente per MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823195"
---
# Preparazione dell'ambiente per MBAM 1.0


Prima di iniziare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), verificare di avere soddisfatto i prerequisiti necessari per installare il prodotto. Se si conoscono i prerequisiti in anticipo, è possibile distribuire il prodotto in modo efficiente e abilitarne le caratteristiche, in grado di supportare più efficacemente gli obiettivi aziendali dell'organizzazione.

## Verificare i prerequisiti di distribuzione di MBAM 1,0


Il client MBAM e ognuna delle funzionalità di MBAM server presentano prerequisiti specifici che devono essere soddisfatti prima che possano essere installati correttamente.

Per garantire l'installazione di successo di MBAM client e le caratteristiche del server MBAM, si dovrebbe pianificare per garantire che i computer specificati per MBAM client o MBAM Server funzionalità di installazione sono adeguatamente preparati per la configurazione MBAM.

**Nota**  MBAM setup verifica se tutti i prerequisiti vengono soddisfatti prima dell'avvio dell'installazione. Se non sono soddisfatte, il programma di installazione avrà esito negativo.

 

[Prerequisiti per la distribuzione di MBAM 1.0](mbam-10-deployment-prerequisites.md)

## Pianificare i requisiti di criteri di gruppo di MBAM 1,0


Prima che MBAM possa gestire i client nell'organizzazione, è necessario definire i criteri di gruppo per i requisiti di crittografia dell'ambiente.

**Importante**  MBAM non funziona con i criteri per la crittografia unità BitLocker autonoma. I criteri di gruppo devono essere definiti per MBAM; in caso contrario, la crittografia e l'imposizione di BitLocker avranno esito negativo.

 

[Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0](planning-for-mbam-10-group-policy-requirements.md)

## Pianificare i ruoli di amministratore di MBAM 1,0


I ruoli di amministratore di MBAM sono gestiti da gruppi locali creati tramite MBAM setup quando si installano le operazioni seguenti: server di amministrazione e monitoraggio di BitLocker, la caratteristica conformità e report di controllo e il database di stato di conformità e controllo.

L'appartenenza ai ruoli di MBAM può essere gestita in modo più efficace se si creano gruppi di sicurezza in ActiveDirectoryDomainServices, si aggiungono gli account di amministratore appropriati a tali gruppi e quindi si aggiungono tali gruppi di sicurezza ai gruppi locali di MBAM. Per altre informazioni, Vedi [come gestire i ruoli di amministratore di mbam](how-to-manage-mbam-administrator-roles-mbam-1.md).

[Pianificazione dei ruoli di amministrazione di MBAM 1.0](planning-for-mbam-10-administrator-roles.md)

## Altre risorse per la pianificazione di MBAM


[Pianificazione di MBAM 1.0](planning-for-mbam-10.md)

 

 





