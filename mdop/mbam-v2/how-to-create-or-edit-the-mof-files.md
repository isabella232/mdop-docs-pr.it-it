---
title: Come creare o modificare i file MOF
description: Come creare o modificare i file MOF
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825325"
---
# Come creare o modificare i file MOF


Prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) con Configuration Manager, è necessario modificare il file Configuration. mof. È inoltre necessario modificare o creare il file SMS \ _def. mof, a seconda della versione di Configuration Manager in uso.

## Modificare il file Configuration.mof


Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file Configuration. mof per Microsoft System Center Configuration Manager 2007 e SystemCenter2012 ConfigurationManager.

[Modificare il file Configuration.mof](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Creare o modificare il file SMS \ _def. mof


Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker nei report di MBAM Configuration Manager, è necessario creare o modificare il file SMS \ _def. mof. In Configuration Manager 2007 il file esiste già, quindi è necessario modificare, ma non sovrascrivere, il file esistente. Se si usa il ConfigurationManager di SystemCenter2012, è necessario creare il file.

[Creare o modificare il file SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md)

## Argomenti correlati


[Distribuzione di MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





