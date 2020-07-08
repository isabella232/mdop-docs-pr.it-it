---
title: Distribuzione di MBAM con Configuration Manager
description: Distribuzione di MBAM con Configuration Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823455"
---
# Distribuzione di MBAM con Configuration Manager


Le procedure seguenti descrivono come distribuire Microsoft BitLocker Administration and Monitoring (MBAM) con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager tramite la configurazione consigliata di usingthe, descritta in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). La configurazione consigliata consiste nell'installare le funzionalità di amministrazione e monitoraggio in uno o più server di amministrazione e monitoraggio di Microsoft BitLocker e installare Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager in un server separato.

Prima di avviare l'installazione, verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software per l'installazione di MBAM con Configuration Manager, rivedendo la [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

Se è necessario reinstallare MBAM con la topologia di Configuration Manager, sarà necessario rimuovere prima alcuni oggetti di Configuration Manager. Per altre informazioni, leggere l' [articolo della Knowledge base](https://go.microsoft.com/fwlink/?LinkId=286306) .

I passaggi per installare MBAM con Configuration Manager sono raggruppati nelle categorie seguenti. Completare la procedura per ogni categoria per completare l'installazione.

## Come creare o modificare i file MOF


Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file **Configuration. mof** e modificare o creare il file Sms \ _def. mof, a seconda della versione di Configuration Manager in uso.

[Come creare o modificare i file MOF](how-to-create-or-edit-the-mof-files.md)

## Come installare MBAM con Configuration Manager


Questa sezione illustra come installare le operazioni seguenti: MBAM nel server Configuration Manager; Database di ripristino e controllo nel server di database; e le funzionalità di amministrazione e monitoraggio del server nel server di amministrazione e monitoraggio.

[Come installare MBAM con Configuration Manager](how-to-install-mbam-with-configuration-manager.md)

## Come convalidare l'installazione di funzionalità di MBAM server nel server Configuration Manager


Dopo aver completato l'installazione di amministrazione e monitoraggio di Microsoft BitLocker, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM per il Server Configuration Manager.

[Come convalidare l'installazione di MBAM con Configuration Manager](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## Argomenti correlati


[Uso di MBAM con Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





