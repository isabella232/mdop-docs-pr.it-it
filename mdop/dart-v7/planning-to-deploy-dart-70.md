---
title: Pianificazione della distribuzione di DaRT 7.0
description: Pianificazione della distribuzione di DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821316"
---
# Pianificazione della distribuzione di DaRT 7.0


Prima di creare il piano di distribuzione, è necessario prendere in considerazione diverse configurazioni e prerequisiti di distribuzione. Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali.

Quando si pianifica l'installazione di Microsoft Diagnostics and Recovery Toolset (DaRT) 7, tenere presente quanto segue:

-   Quando si installa DaRT, è possibile installare tutte le funzionalità in un computer dell'amministratore IT in cui verranno eseguite tutte le attività associate al dardo in esecuzione. In alternativa, è possibile installare solo la funzionalità DaRT che crea l'immagine di ripristino nel computer dell'amministratore IT. Installare quindi la funzionalità usata per eseguire le freccette, ad esempio il **Visualizzatore di connessioni remote Dart** e l' **analizzatore di crash**, in un computer dell'agente helpdesk.

-   Per poter eseguire le freccette in remoto, verificare che il computer dell'agente helpdesk e tutti i computer a cui si sta risolvendo la risoluzione remota si trovino nella stessa rete.

-   Prima di distribuire il dardo in produzione, è possibile creare prima di tutto un ambiente lab per i test. Un laboratorio di test deve includere almeno due computer, uno per fungere da amministratore IT/computer dell'agente helpdesk e uno per fungere da computer per gli utenti finali. In alternativa, è possibile usare tre computer in laboratorio per separare le responsabilità dell'amministratore IT da quelle dell'agente helpdesk.

## Rivedere le configurazioni supportate


Per verificare che i computer selezionati per l'installazione di client o funzionalità soddisfino i requisiti minimi per l'hardware e il sistema operativo, è consigliabile esaminare le informazioni sulle configurazioni di Microsoft Diagnostics and Recovery (DaRT) 7 supportate.

[Configurazioni supportate di DaRT 7.0](dart-70-supported-configurations-dart-7.md)

## Pianificare la creazione dell'immagine di ripristino delle freccette


Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine. Quando si decide, tenere presente che gli utenti finali potrebbero avere accesso occasionalmente ai vari strumenti DaRT. Quando si crea l'immagine di ripristino, verrà specificato anche se si desidera includere altri driver o file. Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.

È necessario tenere presenti i prerequisiti e altri suggerimenti per la pianificazione aggiuntivi per la creazione dell'immagine di ripristino DaRT.

[Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0](planning-to-create-the-dart-70-recovery-image.md)

## Pianificare il salvataggio e la distribuzione dell'immagine di ripristino delle freccette


Diversi metodi possono essere usati per salvare e distribuire l'immagine di ripristino delle freccette. Quando si determina il metodo che si vuole usare, valutare i vantaggi e gli svantaggi di ognuno di essi. Considera inoltre come vuoi usare il dardo nell'azienda.

**Nota**  Potresti voler usare più di un metodo nell'organizzazione. Ad esempio, è possibile avviare il dardo da una partizione remota per la maggior parte delle situazioni e avere un'unità flash USB disponibile nel caso in cui il computer dell'utente finale non possa connettersi alla rete.

 

[Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## Altre risorse per la pianificazione della distribuzione di DaRT


[Pianificazione di DaRT 7.0](planning-for-dart-70-new-ia.md)

 

 





