---
title: Testare un oggetto Criteri di gruppo in un'unità organizzativa separata
description: Testare un oggetto Criteri di gruppo in un'unità organizzativa separata
author: dansimp
ms.assetid: 9a9e6d22-74e6-41d8-ac2f-12a1b76ad5a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 509721fdd775c8669399549f6dcc29cb9ebaea2f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818256"
---
# Testare un oggetto Criteri di gruppo in un'unità organizzativa separata


Se si usa un'unità organizzativa testing (OU) per testare gli oggetti Criteri di gruppo all'interno dello stesso dominio prima della distribuzione nell'ambiente di produzione, è necessario disporre delle autorizzazioni necessarie per accedere all'unità organizzativa di test. L'uso di un'unità organizzativa di test è facoltativo.

**Per usare un'unità organizzativa di test**

1.  Anche se l'oggetto Criteri di **gruppo**è stato estratto per la modifica, fare clic su **oggetti Criteri di gruppo** nell'insieme di strutture e nel dominio in cui si gestiscono i GPO.

2.  Fare clic sulla copia estratta dell'oggetto Criteri di controllo da testare. Il nome verrà preceduto da **\ [Advanced Group Policy Management \]**. Se non è elencato, fare clic su **azione**e quindi su **Aggiorna**. Ordinare i nomi in ordine alfabetico e **\ [Advanced Group Policy Management \]** i GPO verranno in genere visualizzati nella parte superiore dell'elenco.

3.  Trascinare il GPO nell'unità organizzativa di test.

4.  Fare clic su **OK** nella finestra di dialogo che chiede se creare un collegamento al GPO nell'UO di test.

### Considerazioni aggiuntive

-   Al termine del test, il controllo nel GPO Elimina automaticamente il collegamento alla copia Estratto del GPO.

### Riferimenti aggiuntivi

-   [Uso di un ambiente di test](using-a-test-environment.md)

 

 





