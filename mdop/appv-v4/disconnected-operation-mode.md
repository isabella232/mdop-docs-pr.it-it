---
title: Modalità di operazioni senza connessione
description: Modalità di operazioni senza connessione
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821625"
---
# Modalità di operazioni senza connessione


Le impostazioni della modalità di operazione disconnessa, accessibile facendo clic con il pulsante destro del mouse sul nodo **Application Virtualization** , selezionando **Proprietà**e facendo clic sulla scheda **connettività** , consentono al client Desktop Application Virtualization o al client per Servizi Desktop remoto (in precedenza Servizi terminal) di eseguire applicazioni archiviate nella cache del file System del client quando il client non è in grado di connettersi al server Application Virtualization Management.

Motivi per cui la mancata connessione al server include l'errore del server, l'interruzione della rete o la disconnessione dalla rete. Se si verifica un errore, il client passerà automaticamente all'operazione disconnessa. Dopo la disconnessione, se il client necessita di dati aggiuntivi dal server per continuare a eseguire un'applicazione o se il timeout dell'operazione disconnessa scade, il client tenterà di riconnettersi al server. Se il tentativo di connessione non riesce, l'applicazione verrà chiusa.

Per impostazione predefinita, l'operazione disconnessa è abilitata e il timeout è impostato su 90 giorni. Il valore di timeout viene specificato come numero di giorni per cui si vuole limitare la modalità di operazione disconnessa ed è possibile immettere un valore da 1-999.

## Argomenti correlati


[Come disabilitare o modificare le impostazioni della modalità di operazioni senza connessione](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





