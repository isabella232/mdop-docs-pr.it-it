---
title: Installazione sicura di App-V Management Server o Streaming Server
description: Installazione sicura di App-V Management Server o Streaming Server
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816326"
---
# Installazione sicura di App-V Management Server o Streaming Server


Gli argomenti di questa sezione includono informazioni per l'installazione di una versione di sicurezza avanzata di App-V Management Server o App-V Streaming Server.

**Nota**  L'installazione o la configurazione di un'app-V Management o di un server di streaming per l'uso della sicurezza avanzata (ad esempio, Transport Layer Security o TLS) richiede che un certificato X. 509 v3 sia stato provisionato nel server App-V.

 

Quando si prepara l'installazione o la configurazione di una gestione sicura o di un server di flusso, tenere presente quanto segue:

-   Il certificato deve essere valido. Se il certificato non è valido, il client termina la connessione.

-   Il certificato deve contenere l'utilizzo corretto della *chiave avanzata* (EKU), ovvero l'autenticazione del server (OID 1.3.6.1.5.5.7.3.1). Se il certificato non contiene questo EKU, il client termina la connessione.

-   Il nome di dominio completo (FQDN) del certificato deve corrispondere al server in cui è installato. Ad esempio, se il client chiama `RTSPS://Myserver.mycompany.com/content/MyApp.sft` e il certificato **emesso per** il campo è impostato su `Server1.mycompany.com` , il client non si connette al server e la sessione termina. L'errore viene segnalato per l'utente.

    **Nota**  Se si usa App-V in un cluster di bilanciamento del carico di rete, è necessario configurare il certificato con i nomi alternativi oggetto (SANs) per supportare RTSPs. Per informazioni sulla configurazione dell'autorità di certificazione (CA) e sulla creazione di certificati con SANs, vedere <https://go.microsoft.com/fwlink/?LinkId=133228> .

     

-   Il client e il server devono considerare attendibile la CA radice: la CA che rilascia il certificato al server App-V deve essere considerata attendibile dal client che si connette al server. In caso contrario, il client termina la connessione.

-   La chiave privata del certificato deve avere le autorizzazioni modificate per consentire all'account di servizio App-V di accedere al certificato. Per impostazione predefinita, App-V usa l'account del servizio di rete e, per impostazione predefinita, l'account del servizio di rete non ha l'autorizzazione per accedere alla chiave privata, impedendo connessioni sicure.

## In questa sezione


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[Configurazione dei certificati per il supporto dello streaming sicuro](configuring-certificates-to-support-secure-streaming.md)  
Fornisce informazioni su come ottenere, configurare e installare i certificati per supportare lo streaming sicuro.

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
Fornisce le procedure che è possibile usare per modificare le chiavi in Windows Server2003 e Windows Server2008.

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[Configurazione dei certificati per supportare App-V Management Server o Streaming Server](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
Fornisce informazioni sulla configurazione dei certificati per i server di gestione o di flusso di App-V, incluse informazioni sulla configurazione dei certificati per gli ambienti di bilanciamento del carico di rete.

 

 





