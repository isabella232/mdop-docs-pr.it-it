---
title: Configurazione dei certificati per supportare App-V Management Server o Streaming Server
description: Configurazione dei certificati per supportare App-V Management Server o Streaming Server
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821896"
---
# Configurazione dei certificati per supportare App-V Management Server o Streaming Server


Dopo aver completato il processo di provisioning dei certificati e aver modificato le autorizzazioni per la chiave privata per supportare l'installazione di App-V, è possibile avviare la configurazione del server di gestione o del server di flusso. Durante l'installazione, se viene eseguito il provisioning di un certificato prima di eseguire il programma di installazione, la procedura guidata Visualizza il certificato nella schermata **modalità di sicurezza della connessione** e, per impostazione predefinita, la casella di controllo **Usa sicurezza avanzata** è selezionata.

**Nota**  Selezionare il certificato configurato per App-V se sono presenti più certificati per il server.

 

**Importante**  Quando si esegue l'aggiornamento dalla versione 4,2 alla versione 4,5, il programma di installazione ha un'opzione per l' **uso della sicurezza avanzata**; Tuttavia, se si seleziona questa opzione, il flusso non verrà disabilitato tramite RTSP. È necessario usare la console di gestione per disabilitare RTSP dopo l'installazione.

 

Selezionare la porta TCP che il servizio userà per le comunicazioni client. La porta predefinita è TCP 322; è tuttavia possibile cambiare la porta in una porta personalizzata per l'ambiente.

I passaggi rimanenti della procedura guidata sono gli stessi di quelli che si stavano distribuendo in un'app-V Management o in un server di streaming senza usare la funzionalità di **sicurezza avanzata** .

## Configurazione di certificati per gli ambienti NLB


Per supportare le grandi aziende, spesso il server di gestione viene inserito in un cluster di bilanciamento del carico di rete (NLB) per supportare il numero elevato di connessioni. In questo articolo sono necessari almeno due server di gestione che sembrano essere un singolo server di gestione. Quando l'ambiente usa un cluster NLB con diversi server di gestione, è necessaria una configurazione avanzata del certificato usato per il cluster NLB.

Il certificato App-V viene inviato a un'autorità di certificazione (CA) configurata in un computer che utilizza Windows Server2003. La rete SAN consente di connettersi a un nome host del cluster NLB di Management Server specifico usando un nome DNS (Domain Name System) che potrebbe essere diverso dai nomi dei computer effettivi, perché possono essere presenti fino a 32 server che includono il cluster NLB.

Questa configurazione è necessaria solo quando si usa un cluster NLB. Quando il client si connette al server, si connetterà usando il nome di dominio completo (FQDN) del cluster NLB e non l'FQDN di un singolo server. Se non si aggiunge la proprietà SAN con il nome di dominio completo dei nodi del server nel cluster, tutte le connessioni client verranno rifiutate, perché il nome comune del certificato non corrisponde a quello del server.

Per informazioni più dettagliate sulla configurazione dei certificati con l'attributo SAN, vedere <https://go.microsoft.com/fwlink/?LinkId=133228> .

## Argomenti correlati


[Configurazione dei certificati per il supporto dello streaming sicuro](configuring-certificates-to-support-secure-streaming.md)

[Come modificare le autorizzazioni della chiave privata supportare Management Server o Streaming Server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





