---
title: Informazioni sugli ambienti virtuali
description: Informazioni sugli ambienti virtuali
author: dansimp
ms.assetid: e03a8c72-56c1-4ae9-aa45-0283c50a154c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15f3ae29ae8d5586f83baa98ea6821e09ae5c305
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822395"
---
# Informazioni sugli ambienti virtuali


Le applicazioni virtuali vengono eseguite in ambienti virtuali. Gli ambienti virtuali consentono l'esecuzione di ogni applicazione su un server desktop, portatile o host sessione Desktop remoto (host RDSession) senza l'installazione e l'alterazione del sistema operativo host. Ogni applicazione trasporta le proprie informazioni di configurazione nell'ambiente virtuale. Di conseguenza, molte applicazioni vengono eseguite affiancate ad altre applicazioni nello stesso computer senza conflitti.

Le applicazioni virtuali vengono eseguite localmente, in modo che vengano eseguite con prestazioni, funzionalità e accesso completo ai servizi locali che ci si aspetterebbe da qualsiasi applicazione installata localmente.

Poiché ogni applicazione viene eseguita in un ambiente virtuale, vengono ridotti i problemi seguenti:

-   Conflitti tra applicazioni: in ambienti che non usano la virtualizzazione delle applicazioni, è necessario testare a fondo ogni applicazione per verificare che non interferisca con altre applicazioni installate.

-   Test di regressione: poiché l'applicazione non modifica il sistema operativo sottostante, viene eliminato un lungo test di regressione.

-   Incompatibilità della versione: le diverse versioni della stessa applicazione possono essere eseguite contemporaneamente nello stesso computer.

-   Accesso multiutente: le applicazioni che non vengono eseguite in modalità multiutente e pertanto non possono essere eseguite all'interno di un host RDSession, ora possono farlo e funzionare correttamente per più utenti in un singolo host di RDSession.

-   Problemi di multilocazione: due istanze della stessa applicazione che usano configurazioni diverse possono essere eseguite nello stesso computer nello stesso momento.

-   Server Siloing: viene eliminata la necessità di molte farm server separate.

Gli ambienti virtuali includono un registro di sistema virtuale per ogni applicazione. Le impostazioni del registro di sistema create da un'applicazione non possono essere visualizzate da altre applicazioni o utilità, ad esempio Regedit. Invece di copiare l'intero registro di sistema, il registro di sistema virtuale usa un metodo di *sovrapposizione* . Gli elementi nel registro di sistema client possono essere letti dall'applicazione purché una copia virtuale dell'elemento del registro di sistema non sia inclusa nel registro di sistema virtuale. Tutte le Scritture dell'applicazione nel registro di sistema sono contenute nel registro di sistema virtuale.

Gli ambienti virtuali includono anche un file system virtuale e altri componenti virtuali, inclusi i servizi virtuali e i COM virtuali.

## Argomenti correlati


[Panoramica di Application Virtualization Client Management Console](application-virtualization-client-management-console-overview.md)

 

 





