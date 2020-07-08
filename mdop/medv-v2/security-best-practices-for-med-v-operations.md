---
title: Procedure consigliate per le operazioni MED-V
description: Procedure consigliate per le operazioni MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825396"
---
# Procedure consigliate per le operazioni MED-V


In qualità di amministratore autorizzato, è responsabile proteggere le informazioni degli utenti e mantenere la sicurezza dell'organizzazione durante e dopo la distribuzione delle aree di lavoro MED-V. In particolare, prendere in considerazione i problemi seguenti.

**Personalizzazione di Internet Explorer nell'area di lavoro MED-V**. Le versioni precedenti del sistema operativo Windows e di Internet Explorer non sono sicure come le versioni correnti. Di conseguenza, Internet Explorer nell'area di lavoro MED-V è configurato per impedire l'esplorazione e altre attività che possono rappresentare rischi per la sicurezza. Inoltre, l'impostazione dell'area di sicurezza Internet per Internet Explorer nell'area di lavoro MED-V è impostata sul livello più alto. Per impostazione predefinita, entrambe le configurazioni vengono impostate nel Packager area di lavoro MED-V quando si crea il pacchetto dell'area di lavoro MED-V.

Utilizzando Internet Explorer Administration Kit (IEAK) o modificando le impostazioni predefinite nel Packager area di lavoro MED-V, è possibile personalizzare Internet Explorer nell'area di lavoro MED-V. Tuttavia, rendersi conto che se si personalizza Internet Explorer nell'area di lavoro MED-V in modo da renderla meno sicura, è possibile esporre l'organizzazione a tali rischi per la sicurezza presenti nelle versioni precedenti di Internet Explorer.

Da un punto di vista della sicurezza, le procedure consigliate per la gestione di Internet Explorer nell'area di lavoro MED-V sono le seguenti:

-   Quando si crea il pacchetto dell'area di lavoro MED-V, uscire dal set di impostazioni predefinite in modo che Internet Explorer nell'area di lavoro MED-V sia configurato per impedire l'esplorazione e altre attività che possono rappresentare rischi per la sicurezza.

-   Quando si crea il pacchetto dell'area di lavoro MED-V, uscire dal set di impostazioni predefinite in modo che l'impostazione di sicurezza per l'area di sicurezza Internet rimanga al massimo livello.

-   Configurare il proxy aziendale o il Content Advisor di Internet Explorer per bloccare i domini esterni alla rete Intranet aziendale.

**Configurazione di un'area di lavoro MED-V per tutti gli utenti in un computer condiviso.** Quando si configura un'area di lavoro MED-V in modo che sia possibile accedervi da tutti gli utenti in un computer condiviso, si renderà conto che la macchina virtuale guest viene inserita in una posizione che offre l'accesso in lettura e scrittura a tutti gli utenti del sistema.

**Configurazione di un account proxy per l'aggiunta di domini.** Quando si configura un account proxy per l'aggiunta di macchine virtuali al dominio, è necessario sapere che l'utente finale può ottenere le credenziali dell'account proxy. Occorre pertanto prendere precauzioni necessarie, ad esempio limitare i diritti degli utenti dell'account, per evitare che un utente finale usi le credenziali per causare danni.

**Configurazione Sysprep.** Anche se il file Sysprep. inf viene crittografato per impostazione predefinita, il contenuto può essere decrittografato e letto da qualsiasi utente finale determinato che possa accedere correttamente alla macchina virtuale. In questo articolo vengono generate preoccupazioni per la sicurezza perché il file Sysprep. inf può contenere credenziali oltre a un codice Product Key di Windows.

È possibile ridurre questo rischio impostando un account limitato per l'aggiunta di macchine virtuali al dominio e specificando le credenziali per tale account durante la configurazione di Sysprep. In alternativa, è anche possibile configurare Sysprep e la configurazione per la prima volta per l'esecuzione in modalità **assistita** e richiedere agli utenti finali di specificare le proprie credenziali per l'aggiunta della macchina virtuale al dominio.

Una procedura consigliata per MED-V consiste nel specificare che FtsCompletion.exe venga eseguito con un account che conferisce ai diritti degli utenti finali la connessione al Guest tramite il client di connessione Desktop remoto.

**Autenticazione dell'utente finale.** L'abilitazione della memorizzazione nella cache delle credenziali degli utenti finali offre la migliore esperienza utente di MED-V, ma crea il potenziale per cui qualcuno potrebbe avere accesso alle credenziali dell'utente finale. L'unico modo per ridurre il rischio è specificare nel **Packager area di lavoro MED-V** che le credenziali dell'utente finale non sono archiviate. Per altre informazioni sull'autenticazione degli utenti finali, vedere [autenticazione degli utenti finali di MED-V](authentication-of-med-v-end-users.md).

## Argomenti correlati


[Risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md)

[Microsoft Enterprise Desktop Virtualization 2,0](index.md)

 

 





