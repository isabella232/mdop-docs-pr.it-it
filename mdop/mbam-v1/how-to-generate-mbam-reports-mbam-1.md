---
title: Come generare report di MBAM
description: Come generare report di MBAM
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824526"
---
# Come generare report di MBAM


Microsoft BitLocker Administration and Monitoring (MBAM) genera diversi report per monitorare l'uso e la conformità della crittografia BitLocker. Questo argomento descrive come aprire il sito Web di amministrazione di MBAM e come generare report di MBAM su conformità aziendali, singoli computer, compatibilità hardware e attività di recupero tasti. Per altre informazioni sui report di MBAM, vedere informazioni sui [report di mbam](understanding-mbam-reports-mbam-1.md).

**Nota**  Per eseguire i report, è necessario essere membri del ruolo **report Users** nei computer in cui sono state installate le funzionalità di amministrazione e monitoraggio del server, il database di conformità e controllo e i report di conformità e controllo.

 

**Per aprire il sito Web di amministrazione di MBAM**

1.  Aprire un Web browser e passare al sito Web di MBAM. L'URL predefinito per il sito Web è *http:// &lt; nomecomputer &gt; * del server di amministrazione e monitoraggio di Microsoft BitLocker.

    **Nota**  Se il sito Web di MBAMadministration è stato installato in una porta diversa dalla porta 80, è necessario specificare il numero di porta nell'URL. Ad esempio, *http:// &lt; nomecomputer &gt; : &lt; Port &gt; *. Se è stato specificato un nome host per il sito Web MBAMadministration durante l'installazione, l'URL *sarebbe &lt; http:// &gt; hostname*.

     

2.  Nel riquadro di spostamento fare clic su **report**. Nel riquadro principale fare clic sulla scheda relativa al tipo di report: **report conformità aziendale**, report **conformità computer**, **report controllo hardware**o **rapporto di controllo del ripristino**.

    **Nota**  I dati del client MBAM storici vengono conservati nel database di conformità. I dati conservati potrebbero essere necessari in caso di perdita o di furto di un computer. Durante l'esecuzione di report aziendali, è consigliabile usare le date di inizio e di fine appropriate per applicare l'ambito alle scadenze dei report da una a due settimane per aumentare l'accuratezza dei dati di report.

     

**Per generare un report di conformità aziendale**

1.  Nel sito Web di MBAMadministration fare clic su **report** nel riquadro di spostamento, quindi fare clic sulla scheda **report conformità aziendale** e selezionare i filtri appropriati per il report. Per il report conformità aziendale, è possibile impostare i filtri seguenti.

    -   **Stato conformità**. Usare questo filtro per specificare i tipi di stato di conformità (ad esempio, conformi o non conforme) da includere nel report.

    -   **Stato errore**. Usare questo filtro per specificare i tipi di stato di errore, ad esempio nessun errore o errore, da includere nel report.

2.  Fare clic su **Visualizza report** per visualizzare il report specificato.

    I risultati del report possono essere salvati in uno dei diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.

    **Nota**  Il report conformità aziendale viene generato da un processo SQL che viene eseguito ogni sei ore. Di conseguenza, la prima volta che si prova a visualizzare il report, è possibile che siano presenti alcuni dati mancanti.

     

3.  Per visualizzare informazioni su un computer nel report conformità computer, selezionare il nome del computer.

4.  Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.

**Per generare il report di conformità del computer**

1.  Nel sito Web di MBAMadministration selezionare il nodo **report** nel riquadro di spostamento e quindi selezionare il **report conformità computer**. Usare il report conformità computer per cercare il nome **utente** o il **nome del computer**.

2.  Fare clic su **Visualizza report** per visualizzare il report computer.

    I risultati possono essere salvati in uno dei diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.

3.  Per visualizzare altre informazioni su un computer nel report conformità computer, selezionare il nome del computer.

4.  Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.

    **Nota**  Un computer client di MBAM è considerato conforme se il computer soddisfa i requisiti delle impostazioni dei criteri di MBAM o il modello hardware del computer è impostato su incompatibile. Di conseguenza, quando si visualizzano informazioni dettagliate sui volumi del disco associati al computer, i computer esenti da crittografia BitLocker a causa della compatibilità hardware possono essere visualizzati come conformi anche se lo stato di crittografia del volume dell'unità viene visualizzato come non conforme.

     

**Per generare il report di controllo compatibilità hardware**

1.  Dal sito Web di MBAMadministration selezionare il nodo del **report** nel riquadro di spostamento e quindi selezionare il **report di controllo hardware**. Selezionare i filtri appropriati per il report di controllo hardware. Il report di controllo hardware offre i seguenti filtri disponibili:

    -   **Utente (dominio\\utente)**. Specifica il nome dell'utente che ha apportato una modifica.

    -   **Modificare il tipo**. Specifica il tipo di modifiche da cercare.

    -   **Data di inizio**. Specifica la parte della data di inizio dell'intervallo di date in cui si vuole creare un report.

    -   **Data di fine**. Specifica la parte relativa alla data di fine dell'intervallo di date in cui si vuole creare un report.

2.  Fare clic su **Visualizza report** per visualizzare il report.

    I risultati possono essere salvati in diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.

**Per generare il report di controllo chiave di ripristino**

1.  Nel sito Web MBAMadministration selezionare il nodo **report** nel riquadro di spostamento e quindi selezionare il rapporto di **controllo del ripristino**. Selezionare i filtri per il report di controllo chiave di ripristino. I filtri disponibili per gli audit delle chiavi di ripristino sono i seguenti:

    -   **Richiedente**. Specifica il nome utente del richiedente. Il richiedente è la persona nell'help desk che ha eseguito l'accesso alla chiave per conto di un utente.

    -   **Richiedente**. Specifica il nome utente del richiedente. Il richiedente è la persona che ha chiamato l'help desk per ottenere una chiave di ripristino.

    -   **Risultato della richiesta** Specifica i tipi di risultati della richiesta, ad esempio: successo o non riuscito. Ad esempio, potresti voler visualizzare i tentativi di accesso tramite chiave non riusciti.

    -   **Tipo di chiave**. Specifica il tipo di chiave, ad esempio: password chiave di ripristino o hash della password del TPM.

    -   **Data di inizio**. Specifica la parte della data di inizio dell'intervallo di date.

    -   **Data di fine**. Specifica la parte relativa alla data di fine dell'intervallo di date.

2.  Fare clic su **Visualizza report** per visualizzare il report.

    I risultati possono essere salvati in diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.

## Argomenti correlati


[Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





