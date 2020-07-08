---
title: Scheda Server di Gestione avanzata Criteri di gruppo
description: Scheda Server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: a6689437-233e-4f33-a0d6-f7d432c96c00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7ffaa3f55d4ae1c2a59287d9dc302aec3dd00aed
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819285"
---
# Scheda Server di Gestione avanzata Criteri di gruppo


La scheda **server Advanced Group Policy Management** nel riquadro **Cambia controllo** consente di selezionare un server Advanced Group Policy Management immettendo un nome di computer completo e una porta e per eliminare le versioni precedenti degli oggetti Criteri di gruppo dall'archivio per risparmiare spazio su disco nel server Advanced Group Policy Management.

## Specifica del server Advanced Group Policy Management


Il server Advanced Group Policy Management selezionato determina quale archivio viene visualizzato nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni di **delega del dominio** . La porta predefinita per Advanced Group Policy Management è la porta 4600.

Se la connessione del server Advanced Group Policy Management è configurata in modo centralizzato usando le impostazioni dei modelli amministrativi, le opzioni disponibili in questa scheda per la configurazione della connessione non sono Per altre informazioni, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm40.md).

## Eliminazione delle versioni precedenti degli oggetti Criteri di stato


Per impostazione predefinita, tutte le versioni di ogni GPO controllato vengono mantenute nell'archivio. Tuttavia, puoi configurare il servizio Advanced Group Policy Management per limitare il numero di versioni conservate per ogni GPO ed eliminare automaticamente la versione meno recente quando tale limite viene superato. Solo le versioni di GPO visualizzate nella scheda **versioni univoche** del conteggio della finestra **cronologia** verso il limite.

**Nota**  Il numero massimo di versioni univoche da archiviare per ogni GPO non include la versione corrente, quindi l'immissione di 0 mantiene solo la versione corrente. Il limite non deve essere superiore alle versioni di 999.

Quando viene eliminata una versione di un GPO, un record di tale versione rimane nella cronologia dell'oggetto Criteri di controllo, ma la versione del GPO viene eliminata dall'archivio. Puoi impedire l'eliminazione di una versione di un GPO contrassegnando la cronologia come non cancellabile.

 

### Riferimenti aggiuntivi

-   [Interfaccia utente: Gestione avanzata Criteri di gruppo](user-interface-advanced-group-policy-management-agpm40.md)

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks-agpm40.md)

-   [Attività del revisore](performing-reviewer-tasks-agpm40.md)

 

 





