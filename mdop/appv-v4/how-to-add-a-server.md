---
title: Come aggiungere un server
description: Come aggiungere un server
author: dansimp
ms.assetid: 1f31678a-8edf-4d35-a812-e4a2abfd979b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d08b79bcbf34910ce357f39635431d11e3e99bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821386"
---
# Come aggiungere un server


Per gestire in modo più efficiente i server di gestione della virtualizzazione delle applicazioni, organizzarli in gruppi di server. Dopo aver creato un gruppo di server nella console di gestione di Application Virtualization Server, è possibile usare la procedura seguente per aggiungere un server al gruppo.

**Nota**  Tutti i server di un gruppo di server devono essere connessi allo stesso archivio dati.

 

**Per aggiungere un server a un gruppo**

1.  Fare clic sul nodo **gruppi di server** nel riquadro sinistro per espandere l'elenco di gruppi di server.

2.  Fare clic con il pulsante destro del mouse sul gruppo di server desiderato e scegliere **nuovo Application Virtualization Management Server**.

3.  Nella **procedura guidata nuovo gruppo di server**immettere il **nome visualizzato** e il **nome host DNS**.

4.  Abbandonare i valori predefiniti nel campo **massimo allocazione della memoria** per la cache del server e il campo dell' **allocazione della memoria** di avviso per specificare il livello di avviso soglia.

5.  Fai clic su **Avanti**.

6.  Nella finestra di dialogo **modalità di sicurezza della connessione** selezionare la casella **Usa sicurezza avanzata** per scegliere la modalità di sicurezza avanzata, se necessario. Se necessario, completare la **creazione guidata** certificati o visualizzare i certificati esistenti.

7.  Fai clic su **Avanti**.

8.  Nella finestra di dialogo dell' **impostazione della porta App Virt** selezionare la porta **predefinita** o il pulsante di opzione **porta utente personalizzato** e immettere il numero di porta personalizzato.

9.  Fai clic su **Fine**.

## Argomenti correlati


[Come creare un gruppo di server](how-to-create-a-server-group.md)

[Come rimuovere un server](how-to-remove-a-server.md)

 

 





