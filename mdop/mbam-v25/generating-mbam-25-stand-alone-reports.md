---
title: Generazione di report autonomi di MBAM 2.5
description: Generazione di report autonomi di MBAM 2.5
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823125"
---
# Generazione di report autonomi di MBAM 2.5


Quando si configura l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) con la topologia autonoma, è possibile generare report per monitorare l'utilizzo e la conformità della crittografia unità BitLocker. Questo argomento contiene le procedure seguenti:

-   [Per aprire il sito Web di amministrazione e monitoraggio](#bkmk-openadmin)

-   [Per generare un report di conformità aziendale](#bkmk-enterprise)

-   [Per generare un report di conformità del computer](#bkmk-computercomp)

-   [Per generare un report di controllo chiave di ripristino](#bkmk-recoverykey)

Per le descrizioni dei report autonomi, vedere informazioni sui report autonomi di [MBAM 2,5](understanding-mbam-25-stand-alone-reports.md).

**Nota**  Per eseguire i report, è necessario essere un membro del gruppo di **utenti del report mbam** , che si configura in servizi di dominio Active Directory. Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).

 

<a href="" id="bkmk-openadmin"></a>**Per aprire il sito Web di amministrazione e monitoraggio**

1.  Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio. L'URL predefinito per il sito Web di amministrazione e monitoraggio è:

    *http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; porta &gt; /helpdesk*

2.  Nel riquadro sinistro fare clic su **report**. Nella barra dei menu superiore selezionare il report che si vuole eseguire.

    I dati del client MBAM vengono conservati nel database di conformità e controllo per riferimenti cronologici in caso di perdita o di furto di un computer. Durante l'esecuzione di report aziendali, è consigliabile usare le date di inizio e di fine appropriate per l'ambito dei tempi per i report da una a due settimane per aumentare la precisione dei dati di report.

    Dopo aver generato un report, è possibile salvare i risultati in formati diversi, ad esempio HTML, Microsoft Word e Microsoft Excel.

    **Nota**  Configurare SQL Server Reporting Services (SSRS) in modo da usare SSL (Secure Sockets Layer) prima di configurare il sito Web di amministrazione e monitoraggio. Se, per qualsiasi motivo, SSRS non è configurato per l'uso di SSL, l'URL per i report verrà impostato su HTTP anziché su HTTPS quando si configura il sito Web di amministrazione e monitoraggio. Se si passa al sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto". Per visualizzare il report, fare clic su **Mostra tutto il contenuto**.

     

<a href="" id="bkmk-enterprise"></a>**Per generare un report di conformità aziendale**

1.  Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** dal riquadro di spostamento sinistro, selezionare **report conformità aziendale**e selezionare i filtri da usare. I filtri disponibili per il report conformità aziendale sono i seguenti:

    -   **Stato conformità**. Usare questo filtro per specificare i tipi di stato di conformità del report, ad esempio conforme o non conformi.

    -   **Stato errore**. Usare questo filtro per specificare i tipi di stato di errore del report, ad esempio nessun errore o errore.

2.  Fare clic su **Visualizza report** per visualizzare il report selezionato.

3.  Selezionare un nome di computer per visualizzare le informazioni sul computer nel report conformità computer.

4.  Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.

<a href="" id="bkmk-computercomp"></a>**Per generare un report di conformità del computer**

1.  Nel sito Web amministrazione e monitoraggio selezionare il nodo del **report** nel riquadro di spostamento sinistro e quindi selezionare **report conformità computer**. Usare il report conformità computer per cercare il nome **utente** o il **nome del computer**.

2.  Fare clic su **Visualizza report** per visualizzare il report conformità computer.

3.  Selezionare un nome di computer per visualizzare altre informazioni sul computer nel report conformità computer.

4.  Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.

    **Nota**  Un computer client di MBAM è considerato conforme se il computer corrisponde o supera i requisiti delle impostazioni dei criteri di gruppo di MBAM.

<a href="" id="bkmk-recoverykey"></a>**Per generare un report di controllo chiave di ripristino**

1.  Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** nel riquadro di spostamento sinistro e quindi selezionare rapporto di **controllo ripristino**. Selezionare i filtri per il report di controllo chiave di ripristino. I filtri disponibili per gli audit delle chiavi di ripristino sono i seguenti:

    -   **Utente helpdesk**. Questo filtro consente agli utenti di specificare il nome utente del richiedente. Il richiedente è la persona nell'help desk che ha eseguito l'accesso alla chiave per conto di un utente finale.

    -   **Utente finale**. Questo filtro consente agli utenti di specificare il nome utente del richiedente. Il richiedente è l'utente finale che ha chiamato l'help desk per ottenere una chiave di ripristino.

    -   **Richiedi risultato**. Questo filtro consente agli utenti di specificare i tipi di risultati della richiesta, ad esempio successo o non riuscito, su cui si vuole basare il report. Ad esempio, gli utenti potrebbero voler visualizzare i tentativi di accesso tramite chiave non riusciti.

    -   **Tipo di chiave**. Questo filtro consente agli utenti di specificare il tipo di chiave, ad esempio la password del tasto di ripristino o l'hash della password del TPM, su cui si vuole basare il report.

    -   **Data di inizio**. Questo filtro viene usato per definire la parte della data di inizio dell'intervallo di date a cui l'utente vuole segnalare.

    -   **Data di fine**. Questo filtro viene usato per definire la parte relativa alla data di fine dell'intervallo di date a cui gli utenti vogliono segnalare.

2.  Fare clic su **Visualizza report** per visualizzare il report.



## Argomenti correlati


[Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Informazioni sui report autonomi di MBAM 2.5](understanding-mbam-25-stand-alone-reports.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





