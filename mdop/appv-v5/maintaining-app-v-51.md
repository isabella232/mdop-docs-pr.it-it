---
title: Manutenzione di App-V 5.1
description: Manutenzione di App-V 5.1
author: dansimp
ms.assetid: 5abd17d3-e8af-4261-b914-741ae116b0e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 431ad65507a5699358159c73eaf9f3cf0dee33b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805109"
---
# Manutenzione di App-V 5.1


Dopo aver completato tutte le pianificazioni necessarie e quindi la distribuzione di App-V 5,1, è possibile usare le informazioni seguenti per gestire l'infrastruttura di App-V 5,1.

## <a href="" id="move-the-app-v-5-1-server-"></a>Trasferire il server App-V 5,1


Il server App-V 5,1 si connette al database App-V 5,1. È quindi possibile installare il componente di gestione in qualsiasi computer della rete e quindi connetterlo al database App-V 5,1.

[Come spostare il server App-V in un altro computer](how-to-move-the-app-v-server-to-another-computer51.md)

## <a href="" id="determine-if-an-app-v-5-1-application-is-running-virtualized-"></a>Determinare se un'applicazione App-V 5,1 è in uso virtualizzata


I fornitori di software indipendenti che desiderano determinare se un'applicazione è in uso virtualizzato con App-V 5,1 o superiore, dovrebbero aprire un oggetto denominato denominato **AppVVirtual- &lt; PID &gt; ** nello spazio dei nomi predefinito. Ad esempio, l'API di Windows **GetCurrentProcessId ()** può essere usata per ottenere l'ID del processo corrente, ad esempio 4052, e quindi se un oggetto evento denominato denominato **AppVVirtual-4052** può essere aperto correttamente usando **OpenEvent ()** nello spazio dei nomi predefinito per l'accesso in lettura, l'applicazione è virtuale. Se la chiamata a **OpenEvent ()** non riesce, l'applicazione non è virtuale.

Inoltre, gli ISV che vogliono virtualizzare in modo esplicito o meno le chiamate su API specifiche con App-V 5,1 e versioni successive, possono usare le funzioni **VirtualizeCurrentThread ()** e **CurrentThreadIsVirtualized ()** implementate nel modulo AppEntSubsystems32.dll. Questi consentono di accennare a un componente downstream che la chiamata deve o non deve essere virtualizzata.






## Altre risorse per la gestione dell'App-V 5,1


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





