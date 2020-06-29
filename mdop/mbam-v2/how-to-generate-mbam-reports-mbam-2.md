---
title: Come generare report di MBAM
description: Come generare report di MBAM
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824095"
---
# Come generare report di MBAM


Quando si installa Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia autonoma, è possibile generare report diversi per monitorare l'uso e la conformità della crittografia BitLocker. Le procedure descritte in questo argomento illustrano come aprire il sito Web di amministrazione e monitoraggio e i passaggi necessari per generare i report di amministrazione e monitoraggio di Microsoft BitLocker in conformità aziendale, singoli computer e attività di ripristino delle chiavi. Per informazioni dettagliate utili per comprendere i report di MBAM, vedere informazioni sui [report di mbam](understanding-mbam-reports-mbam-2.md).

**Nota**  Per eseguire i report, è necessario essere membri del **ruolo report Users** nei computer in cui sono installate le funzionalità di amministrazione e monitoraggio del server, la conformità e il database di controllo e i report di conformità e controllo.

 

**Per aprire il sito Web di amministrazione e monitoraggio**

1.  Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio. L'URL predefinito per il sito Web di amministrazione e monitoraggio è *http:// &lt; nomecomputer &gt; *.

    **Nota**  Se colponel e il sito Web di monitoraggio è stato installato in una porta diversa da 80, è necessario specificare la porta nell'URL, ad esempio *http:// &lt; nomecomputer &gt; : &lt; porta &gt; *. Se è stato specificato un nome host per colponel e il sito Web di monitoraggio durante l'installazione, l'URL è *http:// &lt; hostname &gt; *.

     

2.  Nel riquadro sinistro fare clic su **report** e quindi selezionare il report che si vuole eseguire dalla barra dei menu superiore.

    I dati del client MBAM storici vengono conservati nel database di conformità per riferimenti cronologici nel caso in cui un computer venga smarrito o rubato. Durante l'esecuzione di report aziendali, è consigliabile usare le date di inizio e di fine appropriate per l'ambito dei tempi per i report da una a due settimane per aumentare la precisione dei dati di report.

    **Nota**  Se SSRS non è stato configurato per l'uso di Secure Socket Layer, l'URL per i report verrà impostato su HTTP anziché su HTTPS quando si installa il server MBAM. Se si passa al portale help desk e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto". Per visualizzare il report, fare clic su **Mostra tutto il contenuto**.

     

**Per generare un report di conformità aziendale**

1.  Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** dal riquadro di spostamento sinistro, selezionare **report conformità aziendale**e selezionare i filtri da usare. I filtri disponibili per il report conformità aziendale sono i seguenti:

    -   **Stato conformità**. Usare questo filtro per specificare i tipi di stato di conformità (ad esempio, conforme o non conformi) del report.

    -   **Stato errore**. Usare questo filtro per specificare i tipi di stato di errore (ad esempio, nessun errore o errore) del report.

2.  Fare clic su **Visualizza report** per visualizzare il report selezionato.

    I risultati possono essere salvati in diversi formati, ad esempio HTML, Microsoft Word e Microsoft Excel.

    **Nota**  Il report conformità aziendale viene generato da un processo SQL che viene eseguito ogni sei ore. Di conseguenza, la prima volta che si Visualizza il report, è possibile che siano presenti alcuni dati mancanti. È possibile generare manualmente i dati del report aggiornati tramite SQL Management Studio. Nella finestra **Esplora oggetti** espandere **SQL Server Agent**, espandere **processi**, fare clic con il pulsante destro del mouse sul processo **CreateCache** e scegliere **Avvia processo al passaggio.**

     

3.  Selezionare un nome di computer per visualizzare le informazioni sul computer nel report conformità computer.

4.  Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.

**Per generare il report di conformità del computer**

1.  Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** nel riquadro di spostamento sinistro e quindi selezionare il **report conformità computer**. Usare il report conformità computer per cercare il nome **utente** o il **nome del computer**.

2.  Fare clic su **Visualizza report** per visualizzare il report computer.

    I risultati possono essere salvati in diversi formati, ad esempio HTML, Microsoft Word e Microsoft Excel.

3.  Selezionare un nome di computer per visualizzare altre informazioni sul computer nel report conformità computer.

4.  Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.

    **Nota**  Un computer client di MBAM è considerato conforme se il computer soddisfa i requisiti delle impostazioni dei criteri di MBAM.

     

**Per generare il report di controllo chiave di ripristino**

1.  Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** nel riquadro di spostamento sinistro e quindi selezionare il rapporto di **controllo del ripristino**. Selezionare i filtri per il report di controllo chiave di ripristino. I filtri disponibili per gli audit delle chiavi di ripristino sono i seguenti:

    -   **Richiedente**. Questo filtro consente agli utenti di specificare il nome utente del richiedente. Il richiedente è la persona nell'help desk che ha eseguito l'accesso alla chiave per conto di un utente.

    -   **Richiedente**. Questo filtro consente agli utenti di specificare il nome utente del richiedente. Il richiedente è la persona che ha chiamato l'help desk per ottenere una chiave di ripristino.

    -   **Richiedi risultato**. Questo filtro consente agli utenti di specificare i tipi di risultati della richiesta, ad esempio successo o non riuscito, su cui si vuole basare il report. Ad esempio, gli utenti potrebbero voler visualizzare i tentativi di accesso tramite chiave non riusciti.

    -   **Tipo di chiave**. Questo filtro consente agli utenti di specificare il tipo di chiave, ad esempio la password del tasto di ripristino o l'hash della password del TPM, su cui si vuole basare il report.

    -   **Data di inizio**. Questo filtro viene usato per definire la parte della data di inizio dell'intervallo di date a cui l'utente vuole segnalare.

    -   **Data di fine**. Questo filtro viene usato per definire la parte relativa alla data di fine dell'intervallo di date a cui gli utenti vogliono segnalare.

2.  Fare clic su **Visualizza report** per visualizzare il report.

    I risultati possono essere salvati in diversi formati, ad esempio HTML, Microsoft Word e Microsoft Excel.

## Argomenti correlati


[Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





