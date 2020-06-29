---
title: Pianificazione per la compatibilità del sistema operativo dell'applicazione
description: Pianificazione per la compatibilità del sistema operativo dell'applicazione
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825466"
---
# Pianificazione per la compatibilità del sistema operativo dell'applicazione


Questo argomento consente di determinare come risolvere i problemi di compatibilità dei sistemi operativi delle applicazioni e illustra come funziona Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 come soluzione per l'organizzazione.

Questo argomento illustra i requisiti aziendali per MED-V e confronta MED-V con la modalità Windows XP e Microsoft Application Virtualization (App-V):

-   [Requisiti aziendali per MED-V](#bkmk-whenmedv)

-   [Vantaggi della modalità MED-V versus Windows XP](#bkmk-medvvsxp)

-   [Vantaggi di MED-V versus App-V](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a>Requisiti aziendali per MED-V


Quando il reparto IT dell'azienda sta determinando se eseguire l'aggiornamento a Windows 7, deve prestare attenzione alle applicazioni line-of-business e alle applicazioni line-of-business basate sul Web per accertarsi che possano essere eseguite nel nuovo sistema operativo. Spesso queste applicazioni e URL sono stati creati per lavorare in modo specifico con una versione precedente di Windows o Internet Explorer e i problemi possono verificarsi quando si prova a usarli nel nuovo sistema operativo. Microsoft offre numerosi metodi diversi per gestire i vari problemi di compatibilità che possono verificarsi durante l'aggiornamento, ad esempio Application Compatibility Toolkit (ACT) e Windows 7 Compatibility Assistant. Ma anche dopo che tutte le applicazioni sono state testate per la compatibilità e sono state determinate correzioni, alcune applicazioni non funzionano ancora correttamente in Windows 7 o sono troppo costose per risolverlo.

Usando MED-V puoi eseguire queste applicazioni legacy tramite un ambiente Windows Virtual PC in cui è in esecuzione Windows XP. Dato che non è più necessario testare e convalidare queste applicazioni nel nuovo sistema operativo prima di eseguire l'aggiornamento, la migrazione a Windows 7 è molto più agevole e veloce.

### Uso dell'elenco di controllo MED-V

Considerare MED-V se si applicano gli scenari seguenti:

-   Si è un'organizzazione di grandi dimensioni (ad esempio gli utenti di 500 e altro), si ha un accordo aziendale con Microsoft e si prevede di eseguire l'aggiornamento a Windows 7.

-   Hai testato le tue applicazioni line-of-business e ne hai trovate alcune che non sono compatibili con Windows 7.

-   Sono stati risolti i problemi di compatibilità per alcune di queste applicazioni di problemi aggiornando l'applicazione o usando uno shim fornito da Microsoft, ad esempio Application Compatibility Toolkit (ACT), ma i problemi di compatibilità rimangono per alcune applicazioni.

-   Hai considerato App-V come opzione per il recapito delle applicazioni incompatibili e hai concluso che anche dopo aver implementato App-V, hai ancora problemi di compatibilità del sistema operativo per le applicazioni che devi affrontare.

-   È stata considerata una soluzione la modalità Windows XP e si è stabilito che non è un'opzione efficiente perché:

    -   Si vuole essere in grado di distribuire immagini virtuali che contengono le applicazioni di problemi a tutti gli utenti finali contemporaneamente, invece che individualmente, e che le immagini virtuali vengano unite automaticamente al dominio.

    -   Hai deciso che è molto più conveniente gestire queste applicazioni legacy (che vengono recapitate virtualmente) e controllare le impostazioni di Windows Virtual PC da una posizione centralizzata invece che dal desktop di ogni utente finale.

    -   Si vuole essere in grado di aggiornare e supportare le macchine virtuali in scala anziché per desktop.

    -   Si vuole avere la possibilità di reindirizzare gli URL che vengono eseguiti meglio in una versione precedente di Internet Explorer per le macchine virtuali e di gestire facilmente il reindirizzamento degli URL in un secondo momento.

-   È stato stabilito che sarebbe stato più conveniente e utile eseguire l'aggiornamento a Windows 7 il più presto possibile e aver deciso di rinviare la risoluzione dei problemi di compatibilità delle applicazioni rimanenti fino a una data successiva, sapendo di avere una soluzione disponibile in MED-V.

## <a href="" id="bkmk-medvvsxp"></a> Vantaggi della modalità MED-V versus Windows XP


Windows Virtual PC per Windows 7 consente di eseguire contemporaneamente versioni diverse di un sistema operativo su un singolo dispositivo ed è incluso in Windows 7 Professional Edition e successive.

La funzionalità modalità Windows XP sfrutta Windows Virtual PC fornendo un'immagine di Windows XP preconfigurata che consente di creare un ambiente Windows XP virtuale. In questo ambiente virtuale è possibile installare manualmente le applicazioni che non sono compatibili con Windows 7 e che vengono eseguite senza problemi dal desktop tramite Windows Virtual PC.

**Usando la modalità Windows XP, è possibile eseguire le operazioni seguenti:**

-   Eseguire applicazioni compatibili con Windows XP all'interno di una macchina virtuale eseguita in Windows Virtual PC.

-   Pubblicare queste applicazioni nel menu del desktop o del programma dell'host.

Quando si vuole consegnare queste macchine virtuali su larga scala come parte di una migrazione aziendale a Windows 7, è necessario essere in grado di distribuire le macchine virtuali in modo rapido, provisionare e personalizzarle in modo efficiente, controllarne le impostazioni e supportarle facilmente.

MED-V si basa sulla modalità Windows XP per garantire la compatibilità delle applicazioni a livello aziendale. Mentre la modalità Windows XP si limita a fornire funzionalità di applicazione virtuale a utenti privati e piccole imprese, MED-V consente distribuzioni su larga scala di immagini di Windows XP preconfigurate in tutta la rete aziendale. Offre una soluzione di gestione aziendale pronta per la configurazione, la distribuzione e la manutenzione di queste aree di lavoro virtuali MED-V. MED-V offre anche a enterpriseadministrators un set di criteri per controllare l'uso delle immagini. Ciò include gli utenti che avranno accesso a quali applicazioni specifiche all'interno di queste immagini.

**Usando MED-V, è possibile eseguire le operazioni seguenti:**

-   Eseguire l'aggiornamento al nuovo sistema operativo senza dover testare e risolvere tutte le applicazioni e gli URL non compatibili.

-   Distribuire immagini virtuali di Windows XP che vengono automaticamente unite al dominio e personalizzate per ogni utente.

-   Eseguire il provisioning delle applicazioni e del reindirizzamento degli URL agli utenti.

-   Controllare le impostazioni di Windows Virtual PC.

-   Gestire e supportare gli endpoint tramite il monitoraggio e la risoluzione dei problemi.

-   Assicurarsi che i computer guest siano corretti, anche se in stato sospesa.

-   Automatizzare la creazione di macchine virtuali per utente e l'inizializzazione di Sysprep.

-   Diagnosticare facilmente i problemi nei computer host e Guest.

-   Gestire senza problemi i computer guest connessi tramite la modalità NAT di Windows Virtual PC.

## <a href="" id="bkmk-medvvsappv"></a>Vantaggi di MED-V versus App-V


MED-V e App-V sono due tecnologie molto diverse che possono collaborare facilmente per risolvere i problemi di compatibilità dei sistemi operativi dell'applicazione. Usando App-V, crei un pacchetto individualizzato per ogni applicazione, ognuno dei quali viene quindi mantenuto separato dagli altri. Ogni applicazione virtuale può quindi essere immediatamente recapitata all'utente finale, che è molto utile per una strategia di distribuzione di Windows 7.

MED-V non gestisce le applicazioni singolarmente. Crea invece un'ulteriore istanza di Windows XP nello stesso desktop in cui è in uso Windows 7. È possibile installare tutte le applicazioni necessarie in questa immagine virtuale e gestire l'immagine così come si farebbe con qualsiasi altro desktop dell'organizzazione.

Inoltre, puoi usare MED-V insieme a App-V in modo che le applicazioni virtuali sequenziate tramite App-V vengano installate, pubblicate e gestite tramite MED-V.

## Argomenti correlati


[Definire e pianificare la distribuzione di MED-V](define-and-plan-your-med-v-deployment.md)

 

 





