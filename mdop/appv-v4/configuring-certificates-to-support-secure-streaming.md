---
title: Configurazione dei certificati per il supporto dello streaming sicuro
description: Configurazione dei certificati per il supporto dello streaming sicuro
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821895"
---
# Configurazione dei certificati per il supporto dello streaming sicuro


Per impostazione predefinita, il servizio App-V viene eseguito con l'account del servizio di rete. È tuttavia possibile creare un account del servizio in servizi di dominio Active Directory e sostituire l'account del servizio di rete con l'account di dominio Active Directory.

Il contesto di sicurezza in cui viene eseguito il servizio è importante per la configurazione di comunicazioni sicure avanzate. Questo contesto di sicurezza deve avere le autorizzazioni di lettura per la chiave privata del certificato. Quando viene generata una *richiesta di firma del certificato* PKCS \ #10 (CSR) per il server App-V, viene chiamato il provider del *servizio crittografico* di Windows e viene generata una chiave privata. La chiave privata è protetta con le autorizzazioni concesse solo agli account di sistema e amministratore.

È necessario modificare gli elenchi di controllo di accesso (ACL) sulla chiave privata per consentire all'App-V Management o al server di streaming di accedere alla chiave privata necessaria per la corretta comunicazione protetta TLS.

## Recupero e installazione di un certificato


Gli scenari per ottenere e installare un certificato per App-V sono i seguenti:

-   Infrastruttura a chiave pubblica interna (PKI).

-   Autorità di certificazione (CA) che rilascia certificati di terze parti.

    **Nota**  Se è necessario ottenere un certificato da una CA di terze parti, seguire la documentazione disponibile nel sito Web della CA.

     

Se è stata distribuita un'infrastruttura PKI, consultare gli amministratori della PKI per acquisire un certificato conforme ai requisiti descritti in questo argomento. Se un'infrastruttura PKI non è disponibile, usare un'autorità di certificazione di terze parti per ottenere un certificato valido.

Per informazioni dettagliate su come ottenere e installare un certificato, vedere <https://go.microsoft.com/fwlink/?LinkId=151969> .

## Argomenti correlati


Configurazione dei certificati per il supporto dello streaming sicuro [come modificare le autorizzazioni di chiave privata per supportare server di gestione o streaming server](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





