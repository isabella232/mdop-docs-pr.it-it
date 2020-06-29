---
title: Come modificare le dimensioni della cache del server
description: Come modificare le dimensioni della cache del server
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818026"
---
# Come modificare le dimensioni della cache del server


È possibile usare la procedura seguente per modificare le dimensioni della cache per qualsiasi server direttamente dalla console di gestione di Application Virtualization Server.

**Nota**  Anche se è possibile modificare le dimensioni della cache, a meno che la configurazione non richieda specificamente la modifica delle dimensioni, è consigliabile abbandonare la dimensione della cache impostata sui valori predefiniti.

 

**Per modificare le dimensioni della cache del server**

1.  Fare clic sul nodo **gruppi di server** nel riquadro sinistro per espandere l'elenco di gruppi di server.

2.  Nel riquadro **risultati** fare doppio clic sul gruppo di server desiderato per visualizzare l'elenco dei server nel gruppo.

3.  Nel riquadro **risultati** fare clic con il pulsante destro del mouse sul server desiderato e scegliere **Proprietà**.

4.  Selezionare la scheda **Avanzate** .

5.  Immettere un valore nel campo **massimo allocazione della memoria** per la cache del server e immettere un valore per il livello di avviso soglia nel campo **allocazione della memoria** di avviso.

6.  Immettere un valore nel campo **dimensione blocco massimo** . Questo numero deve essere maggiore o uguale alla dimensione massima del blocco del pacchetto più grande che verrà trasmesso dal server.

7.  Fai clic su **OK**.

## Argomenti correlati


[Come modificare la porta del server](how-to-change-the-server-port.md)

[Come gestire i server in Server Management Console](how-to-manage-servers-in-the-server-management-console.md)

 

 





