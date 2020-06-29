---
title: Impostare un modello predefinito
description: Impostare un modello predefinito
author: dansimp
ms.assetid: e0acf980-437f-4357-b237-298aaebe490d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 870c1d4c13049992509f6aa831966736e6ba25ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820226"
---
# Impostare un modello predefinito


In qualità di Editor puoi specificare quale dei modelli disponibili sarà il modello predefinito consigliato per tutti gli amministratori di criteri di gruppo per la creazione di nuovi oggetti Criteri di gruppo.

**Nota**  Un modello è una versione statica non modificabile di un oggetto Criteri di ricerca da usare come punto di partenza per la creazione di nuovi GPO modificabili.

 

Per completare questa procedura è necessario un account utente con l'editor o il ruolo amministratore Advanced Group Policy Management (controllo completo) o le autorizzazioni necessarie in Gestione criteri di gruppo avanzati. Esaminare i dettagli in "considerazioni aggiuntive" in questo argomento.

**Per impostare il modello predefinito da usare per la creazione di nuovi GPO**

1.  Nell'albero della **console di gestione di criteri di gruppo** fare clic su **Cambia controllo** nella foresta e nel dominio in cui si vuole gestire gli oggetti GPO.

2.  Nella scheda **contenuto** del riquadro dei dettagli fare clic sulla scheda **modelli** per visualizzare i modelli disponibili.

3.  Fare clic con il pulsante destro del mouse sul modello che si desidera impostare come predefinito e quindi scegliere **Imposta come predefinito**.

4.  Fare clic su **Sì** per confermare.

5.  Quando la finestra di **stato** indica che lo stato di avanzamento complessivo è stato completato, fare clic su **Chiudi**. Il modello predefinito ha un'icona blu e lo stato è identificato come **modello (impostazione predefinita)** nella scheda **modelli** .

### Considerazioni aggiuntive

-   Per impostazione predefinita, per eseguire questa procedura è necessario essere un editor o un amministratore di Advanced Group Policy Management (controllo completo). In particolare, devi avere il **contenuto dell'elenco** e creare le autorizzazioni di **modello** per il dominio.

-   Dopo aver impostato un modello come predefinito, tale modello sarà quello selezionato inizialmente nella finestra di dialogo **nuovo GPO controllato** quando gli amministratori dei criteri di gruppo creano nuovi GPO. Tuttavia, avranno la possibilità di selezionare un altro modello di GPO, incluso il ** &lt; GPO &gt; vuoto**, che non include alcuna impostazione.

-   La ridenominazione o l'eliminazione di un modello non ha effetti sugli oggetti Criteri di creazione creati da tale modello.

-   Poiché non può essere modificato, un modello non ha una cronologia.

### Riferimenti aggiuntivi

-   [Creazione di un modello e impostazione di un modello predefinito](creating-a-template-and-setting-a-default-template.md)

-   [Richiedere la creazione di un nuovo oggetto Criteri di gruppo controllato](request-the-creation-of-a-new-controlled-gpo.md)

 

 





