---
title: Come gestire le esenzioni della crittografia BitLocker del computer
description: Come gestire le esenzioni della crittografia BitLocker del computer
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825676"
---
# Come gestire le esenzioni della crittografia BitLocker del computer


Microsoft BitLocker Administration and Monitoring (MBAM) può essere usato per esentare determinati computer dalla protezione di BitLocker. Ad esempio, un'organizzazione può decidere di controllare l'esenzione da BitLocker in base al computer.

Per esonerare un computer dalla crittografia BitLocker, è necessario aggiungere il computer a un gruppo di sicurezza in ActiveDirectoryDomainServices per aggirare le regole di protezione di BitLocker basate su computer.

**Nota**  Se il computer è già protetto da BitLocker, i criteri di esenzione dal computer non hanno effetto.

 

**Per esonerare un computer dalla crittografia BitLocker**

1.  Aggiungere l'account del computer che si vuole esentare da un gruppo di sicurezza in ActiveDirectoryDomainServices. In questo modo è possibile ignorare le regole di protezione di BitLocker basate su computer.

2.  Creare un oggetto Criteri di gruppo usando il modello di criteri di gruppo di MBAM, quindi associare l'oggetto Criteri di gruppo al gruppo Active Directory creato nel passaggio precedente. Per altre informazioni sulla creazione degli oggetti Criteri di gruppo necessari, vedere [distribuzione di oggetti Criteri di gruppo di MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

3.  Quando viene avviato un computer esentato, il client MBAM controlla l'impostazione dei criteri di esenzione del computer e sospende la protezione in base al fatto che il computer faccia parte del gruppo di sicurezza per l'esenzione da BitLocker.

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 1.0](administering-mbam-10-features.md)

 

 





