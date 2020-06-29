---
title: Procedure consigliate per il controllo della versione
description: Procedure consigliate per il controllo della versione
author: dansimp
ms.assetid: 4a2a1ac7-67f3-4ba3-ab07-860d33da0efe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d560913c4e0f49a2015f620564a9038677d65144
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819195"
---
# Procedure consigliate per il controllo della versione


Gestione avanzata Criteri di gruppo di Microsoft fornisce il controllo della versione per gli oggetti Criteri di gruppo (GPO) in modo molto simile a Microsoft Visual SourceSafe® fornisce il controllo della versione per il codice sorgente. Gli sviluppatori possono usare Visual SourceSafe per gestire più versioni di ogni file di origine. Gli amministratori dei criteri di gruppo possono usare Advanced Group Policy Management per eseguire la stessa operazione per GPO. Quando si usa Advanced Group Policy Management, gli amministratori dei criteri di gruppo devono tenere presenti le procedure consigliate applicabili a qualsiasi sistema di controllo delle versioni:

-   **Data e ora:** La data e l'ora vengono timbrate per ogni versione di un oggetto Criteri di controllo. Per assicurarsi che la cronologia sia accurata, soprattutto quando si modificano i GPO in più computer, verificare che ogni computer sincronizza il proprio clock con un'origine temporale autorevole.

-   **Archiviare gli oggetti Criteri di controllo al termine della modifica:** È comune che gli editori verifichino gli oggetti Criteri di ricerca e dimentichino di archiviarli di nuovo nell'archivio. Tuttavia, questo può impedire agli altri amministratori dei criteri di gruppo di modificare l'oggetto Criteri di stato. Verificare sempre che i GPO vengano riattivati immediatamente dopo aver completato la modifica.

-   **Salvare le modifiche di frequente:** Quando si modifica un oggetto Criteri di stato, salvare le modifiche di frequente. La maggior parte degli editori estrae un oggetto Criteri di ricerca, apporta molte modifiche e quindi controlla l'oggetto Criteri di ricerca nell'archivio. Controlla invece l'oggetto Criteri di ricerca nell'archivio regolarmente, quindi controllalo di nuovo. Il dettaglio può essere piccolo come il controllo dell'oggetto Criteri di gruppo dopo la modifica di ogni impostazione (scelta non consigliata) o l'archiviazione del GPO dopo aver creato gruppi di modifiche correlate. Il risultato è una cronologia più documentata per ogni oggetto Criteri di gruppo che può essere utile per la risoluzione dei problemi.

-   **Distribuire spesso gli oggetti Criteri** di stato: Non consentire che i GPO nuovi e modificati che non sono stati ancora distribuiti si accumulino in gran numero nell'archivio. Distribuire invece i GPO nuovi e modificati il prima possibile in modo che abbiano un effetto minimo sull'ambiente di produzione. La distribuzione di molti GPO nuovi e modificati in una sola volta può compromettere l'ambiente di produzione.

-   **Documentare lo scopo delle modifiche quando si archivia GPO:** Qualsiasi revisore può confrontare le versioni di un GPO per vedere le modifiche specifiche tra le due. La documentazione di queste modifiche specifiche non aggiunge alcun valore. È invece possibile documentare l'intenzione e lo scopo di una modifica anziché documentare i revisori che possono essere visualizzati visualizzando i report delle differenze. I commenti della versione devono aggiungere valore al report di confronto e aiutare un revisore a comprendere il motivo per cui l'editor ha modificato l'oggetto Criteri di controllo.

-   **Testare i GPO in un ambiente di test:** La distribuzione di GPO nell'ambiente di produzione senza testarle è rischiosa. Testare invece i GPO in un dominio in una foresta di test e quindi esportare i GPO in file e importarli in un dominio in una foresta di produzione. Inoltre, puoi collegare GPO a un'unità organizzativa che contiene computer e utenti di test. Verificare che ogni oggetto Criteri di controllo funzioni correttamente nell'ambiente di test e quindi distribuire i GPO nell'ambiente di produzione.

### Riferimenti aggiuntivi

-   [Gestione avanzata Criteri di gruppo 4.0](advanced-group-policy-management-40.md)

 

 





