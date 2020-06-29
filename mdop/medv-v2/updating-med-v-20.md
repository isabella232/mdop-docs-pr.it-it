---
title: Aggiornamento di MED-V 2.0
description: Aggiornamento di MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823735"
---
# Aggiornamento di MED-V 2.0


Proteggere il sistema applicando gli aggiornamenti di sicurezza appropriati per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Aggiornamento di MED-V


Puoi aggiornare MED-V in modo interattivo, dall'utente finale o in silenzio usando un sistema di distribuzione elettronica del software. L'installazione dell'agente host MED-V aggiorna l'agente host MED-V e quindi aggiorna l'area di lavoro MED-V, se necessario. L'agente host MED-V e l'agente guest continuano a essere sincronizzati. Se le applicazioni sono in esecuzione dall'area di lavoro MED-V mentre viene aggiornato l'agente host MED-V, è necessario riavviare il computer host per completare l'aggiornamento. Se non sono in uso applicazioni, MED-V viene riavviato automaticamente e l'aggiornamento viene completato senza riavviare il computer host.

Se si aggiorna MED-V usando un sistema di distribuzione elettronica del software, è possibile controllare il comportamento di riavvio. Per eseguire questa operazione, eliminare il riavvio digitando **Riavvia = "ReallySuppress"** al prompt dei comandi durante l'installazione di MED-V\_HostAgent\_Setup.exe. Configura quindi il sistema di distribuzione elettronica del software per acquisire il codice restituito di 3010 (che segnala che è necessario riavviare il computer) ed eseguire il comportamento set restart.

## Argomenti correlati


[Documentazione tecnica su MED-V](technical-reference-for-med-v.md)

 

 





