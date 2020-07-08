---
title: Come convalidare l'installazione di MBAM con Configuration Manager
description: Come convalidare l'installazione di MBAM con Configuration Manager
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822636"
---
# Come convalidare l'installazione di MBAM con Configuration Manager


Dopo l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM) con Configuration Manager, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM completando la procedura seguente.

**Per convalidare l'installazione delle funzionalità di MBAM server con Configuration Manager**

1.  Nel server in cui è distribuito System Center Configuration Manager aprire il **Pannello di controllo**. Selezionare il programma usato per disinstallare o modificare un programma. Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco di programmi e funzionalità.

    **Nota**  Per convalidare l'installazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.

     

2.  Usare la console di Configuration Manager per verificare che venga visualizzata una nuova raccolta, denominata "MBAM supported Computers".

    Per visualizzare la raccolta con Configuration Manager 2007: fare clic su **database sito** ( &lt; **codicesito** &gt;  -  &lt; **nomeserver** &gt; , &lt; **siteName** &gt; ), **Gestione computer**.

    Per visualizzare la raccolta con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **asset e conformità** , **Raccolte dispositivi**.

3.  Usare la console di Configuration Manager per verificare che i report seguenti siano elencati nella cartella **mbam** :

    -   Conformità al computer BitLocker

    -   Dashboard di conformità di BitLocker Enterprise

    -   Dettagli di conformità di BitLocker Enterprise

    -   Riepilogo conformità di BitLocker Enterprise

    Per visualizzare i report con Configuration Manager 2007: fare clic su **report**, **Reporting Services**, \ \ \ \ &lt; **nomeserver** &gt; , **cartelle report**

    Per visualizzare i report con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **monitoraggio** , **creazione**di report e **report**.

4.  Usare la console di Configuration Manager per verificare che la configurazione della previsione "protezione BitLocker" sia elencata.

    Per visualizzare le previsioni di configurazione con Configuration Manager 2007: fare clic su **Gestione configurazione desiderata**, **previsioni di configurazione**.

    Per visualizzare le previsioni di configurazione con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **asset e conformità** , **Impostazioni conformità**, **previsioni di configurazione**.

5.  Usare la console di Configuration Manager per verificare che vengano visualizzati i nuovi elementi di configurazione seguenti:

    -   Protezione delle unità dati fisse di BitLocker

    -   Protezione unità sistema operativo BitLocker

    Per visualizzare gli elementi di configurazione con Configuration Manager 2007: fare clic su **Gestione configurazione desiderata**, **elementi di configurazione**.

    Per visualizzare gli elementi di configurazione con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **asset e conformità** , **Impostazioni conformità**, **elementi di configurazione**.

## Argomenti correlati


[Distribuzione di MBAM con Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





