---
title: Come spostare i siti Web di MBAM 2.5
description: Come spostare i siti Web di MBAM 2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825746"
---
# Come spostare i siti Web di MBAM 2.5


Usare queste procedure per trasferire i siti Web di MBAM seguenti da un computer a un altro, ovvero per trasferire le caratteristiche seguenti dal server a al server B:

-   Sito Web di amministrazione e monitoraggio

-   Portale self-service

**Importante**  Durante la configurazione di entrambi i siti Web, è necessario specificare la stessa stringa di connessione, l'URL report, gli account di gruppo e l'account di dominio del pool di applicazioni del servizio Web come quelli attualmente in uso. Se non si usano gli stessi valori, non è possibile accedere ad alcuni server. Per ottenere i valori correnti, usare il cmdlet **Get-MbamWebApplication** di Windows PowerShell.

 

**Per trasferire il sito Web di amministrazione e monitoraggio in un altro server**

1.  Nel server B installare il software del server MBAM 2,5. Per istruzioni, vedere [installazione del software server MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica di **amministrazione e monitoraggio del sito Web** .

    In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamWebApplication** per configurare il sito Web di amministrazione e monitoraggio.

    Per istruzioni su come configurare il sito Web di amministrazione e monitoraggio, vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

**Per trasferire il portale self-service in un altro server**

1.  Nel server B installare il software del server MBAM 2,5. Per istruzioni, vedere [installazione del software server MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **portale self-service** .

    In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamWebApplication** per configurare il portale self-service.

    Per istruzioni su come configurare il sito Web di amministrazione e monitoraggio, vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

3.  Se i computer client dell'organizzazione non hanno accesso alla rete di distribuzione del contenuto Microsoft, è anche necessario trasferire i file JavaScript. Informazioni [su come configurare il portale self-service quando i computer client non riescono ad accedere alla rete di distribuzione del contenuto Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) .

4.  Personalizzare il portale self-service per l'organizzazione. Usare le istruzioni per [personalizzare il portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md) per esaminare le personalizzazioni correnti e per configurare le impostazioni personalizzate nel portale self-server nel server B.



## Argomenti correlati


[Come configurare le applicazioni Web di MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Spostamento delle funzionalità di MBAM 2.5 a un altro server](moving-mbam-25-features-to-another-server.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





