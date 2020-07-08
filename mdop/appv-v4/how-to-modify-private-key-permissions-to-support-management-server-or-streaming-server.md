---
title: Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server
description: Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817026"
---
# Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server


Per supportare un'installazione di App-V più sicura, è possibile usare le procedure seguenti per modificare le chiavi private in Windows Server2003 o Windows Server2008. Per modificare le autorizzazioni della chiave privata, è possibile usare lo strumento Windows Server2003 Resource Kit `WinHttpCertCfg.exe` .

Per Windows Server2003, la procedura richiede che un certificato che soddisfi i prerequisiti elencati in questo documento sia installato nel computer o nei computer in cui si vuole installare App-V Management o streaming server. Altre informazioni sull'uso dello `WinHttpCertCfg.exe` strumento sono disponibili all'indirizzo <https://go.microsoft.com/fwlink/?LinkId=151981> .

In Windows Server2008, il processo di modifica degli ACL della chiave privata è molto più semplice. L'interfaccia utente del certificato può essere usata per gestire le autorizzazioni di chiave privata.

**Nota**  Il contesto di sicurezza predefinito è servizio di rete; Tuttavia, è possibile usare un account di dominio.

 

**Per gestire le chiavi private in Windows Server2003**

1.  Nel computer che diventerà App-V Management o streaming server digitare il comando seguente in un prompt dei comandi per elencare le autorizzazioni correnti assegnate a un certificato specifico:

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  Se necessario, modificare le autorizzazioni del certificato per consentire l'accesso in lettura al contesto di sicurezza che verrà usato per la gestione o il servizio di flusso:

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  Verificare che il contesto di sicurezza sia stato aggiunto correttamente elencando le autorizzazioni per il certificato:

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**Per gestire le chiavi private in Windows Server2008**

1.  Creare una Microsoft Management Console (MMC) con lo snap-in *certificati* destinato all'archivio certificati del *computer locale* .

2.  Espandere la console MMC e selezionare **Gestisci chiavi private**.

3.  Nella scheda **sicurezza** aggiungere l'account del **servizio di rete** con l'accesso in **lettura** .

## Argomenti correlati


[Configurazione dei certificati per supportare App-V Management Server o Streaming Server](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[Configurazione dei certificati per il supporto dello streaming sicuro](configuring-certificates-to-support-secure-streaming.md)

 

 





