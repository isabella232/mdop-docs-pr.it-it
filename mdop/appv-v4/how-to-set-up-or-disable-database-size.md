---
title: Come configurare o disabilitare le dimensioni dei database
description: Come configurare o disabilitare le dimensioni dei database
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816565"
---
# Come configurare o disabilitare le dimensioni dei database


È possibile usare le procedure seguenti nella console di gestione di Application Virtualization Server per specificare le dimensioni (in MB) dell'utilizzo del sistema di virtualizzazione delle applicazioni che si desidera archiviare nel database.

Quando la dimensione dei dati archiviati raggiunge il 95% (la filigrana alta) del limite specificato, il sistema eliminerà il 10% dei dati di utilizzo, lasciando il 85% dei dati. I dati di utilizzo del pacchetto e dell'applicazione verranno eliminati. Quando il database diventa abbastanza grande e si avvicina alla filigrana elevata, viene inviato un messaggio di avviso al log di SQL Server per comunicare che è stato raggiunto il limite. Questo avviso è necessario perché l'azione di pulitura può influire sull'output dei report. Consente inoltre di decidere se è necessario aumentare le dimensioni massime del database, ridurre il numero di mesi di dati di utilizzo da mantenere oppure abbassare il livello di registrazione.

**Nota**  Sono disponibili le opzioni **Nessun limite di dimensioni** e **Mantieni tutto l'utilizzo** per disabilitare la creazione di report di utilizzo e la pulizia del database. La selezione di questi elementi consente di pulire anche il log delle transazioni del database. Tutte le transazioni di Microsoft SQL Server salvate verranno rimosse dal log del database.

 

**Per impostare le dimensioni del database**

1.  Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro sinistro e scegliere **Opzioni di sistema**.

2.  Selezionare la scheda **database** .

3.  Selezionare il pulsante di opzione **dimensione massima del database (MB)** o **Nessun limite di dimensione** .

4.  Se si sceglie di specificare le dimensioni di un database, è consigliabile immettere un numero compreso tra 512 e 4096 MB. La dimensione predefinita è 1024 MB e se è necessario aumentare le dimensioni del database, il valore massimo che è possibile immettere è 2.147.483.647. Se si seleziona **Nessun limite di dimensione**, il database si svilupperà fino a raggiungere il limite di dimensioni del disco.

5.  Fare clic su **applica** o **OK**.

**Per disabilitare i limiti delle dimensioni del database**

1.  Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro **ambito** e scegliere **Opzioni di sistema**.

2.  Selezionare la scheda **database** .

3.  Selezionare il **limite nessuna dimensione** e **Mantieni tutti i** pulsanti di opzione utilizzo.

4.  Fare clic su **applica** o **OK**.

## Argomenti correlati


[Come personalizzare un sistema di Application Virtualization in Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Come configurare o disabilitare la creazione di report di utilizzo](how-to-set-up-or-disable-usage-reporting.md)

 

 





