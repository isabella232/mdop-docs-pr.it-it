---
title: Distribuzione del client MBAM 1.0
description: Distribuzione del client MBAM 1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822905"
---
# Distribuzione del client MBAM 1.0


Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione distribuendo il client tramite strumenti come servizi di dominio Active Directory oppure crittografando direttamente i computer client nell'ambito del processo di imaging iniziale.

A seconda di quando si distribuisce il client MBAM, è possibile abilitare la crittografia BitLocker in un computer dell'organizzazione prima o dopo che l'utente finale riceva il computer. Per controllare questa tempistica, puoi configurare criteri di gruppo e distribuire il software del client MBAM usando un sistema di distribuzione del software aziendale.

Puoi usare uno o entrambi questi metodi nell'organizzazione. Se si usano entrambi i metodi, è possibile migliorare la conformità, la creazione di report e il supporto per il recupero della chiave.

## Distribuire il client MBAM in computer desktop o portatili


Dopo aver configurato Criteri di gruppo, è possibile distribuire i file di installazione di Windows Installer del client MBAM in computer di destinazione. A questo scopo, puoi usare un prodotto del sistema di distribuzione del software aziendale, ad esempio Microsoft System Center 2012 Configuration Manager o Active Directory Domain Services. I due file di installazione di Windows Installer disponibili per MBAM client sono MBAMClient-64bit.msi e MBAMClient-32bit.msi. Questi file sono forniti con il software MBAM. Per altre informazioni su come distribuire gli oggetti dei criteri di gruppo di MBAM, vedere [distribuzione di oggetti Criteri di gruppo di mbam 1,0](deploying-mbam-10-group-policy-objects.md).

[Come distribuire il client MBAM a computer desktop o portatili](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## Distribuire il client MBAM come parte di una distribuzione di Windows


In alcune organizzazioni i nuovi computer vengono ricevuti e configurati centralmente. Questa situazione consente agli amministratori di installare il client MBAM per gestire la crittografia BitLocker in ogni computer prima che tutti i dati degli utenti vengano scritti nel computer. Questo approccio consente di verificare che i computer siano crittografati correttamente perché l'amministratore esegue l'azione senza affidarsi alle azioni dell'utente finale. Un presupposto chiave per questo scenario è che i criteri dell'organizzazione installano un'immagine Windows aziendale prima che il computer venga recapitato all'utente.

[Come distribuire il client MBAM come parte di una distribuzione di Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## Altre risorse per la distribuzione del client MBAM


[Distribuzione di MBAM 1.0](deploying-mbam-10.md)

[Pianificazione della distribuzione del client di MBAM 1.0](planning-for-mbam-10-client-deployment.md)

 

 





