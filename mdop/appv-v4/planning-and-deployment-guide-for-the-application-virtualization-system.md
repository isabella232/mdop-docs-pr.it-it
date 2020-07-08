---
title: Guida alla pianificazione e alla distribuzione per il sistema di virtualizzazione delle applicazioni
description: Guida alla pianificazione e alla distribuzione per il sistema di virtualizzazione delle applicazioni
author: dansimp
ms.assetid: 6c012e33-9ac6-4cd8-84ff-54f40973833f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10bcac26fddae2f0e5826dbd7335adda06d3987e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815956"
---
# Guida alla pianificazione e alla distribuzione per il sistema di virtualizzazione delle applicazioni


Microsoft Application Virtualization Management offre la possibilità di rendere le applicazioni disponibili per i computer degli utenti finali senza dover installare le applicazioni direttamente in tali computer. Ciò viene reso possibile tramite un processo noto come *sequenziamento dell'applicazione*, che consente l'esecuzione di ogni applicazione nel proprio ambiente virtuale autonomo nel computer client. Le applicazioni sequenziate vengono isolate l'una dall'altra, eliminando i conflitti tra applicazioni, ma possono comunque interagire con il computer client.

Application Virtualization Client è il componente del sistema di virtualizzazione dell'applicazione che consente all'utente finale di interagire con le applicazioni dopo che sono state pubblicate nel computer. Il client gestisce l'ambiente virtuale in cui vengono eseguite le applicazioni virtualizzate in ogni computer. Dopo l'installazione del client in un computer, le applicazioni devono essere messe a disposizione del computer tramite un processo noto come *pubblicazione*, che consente all'utente finale di eseguire le applicazioni virtuali. Il processo di pubblicazione colloca le icone e i tasti di scelta rapida dell'applicazione virtuale nel computer, in genere nel desktop di Windows o nel menu **Start** , e inserisce anche le informazioni di associazione per la definizione del pacchetto e il tipo di file nel computer. La pubblicazione rende inoltre disponibile il contenuto del pacchetto dell'applicazione per il computer dell'utente finale.

Il contenuto del pacchetto dell'applicazione virtuale può essere inserito in uno o più server di virtualizzazione dell'applicazione in modo che possa essere trasmesso ai client su richiesta e memorizzato nella cache localmente. I server di file e i server Web possono essere usati anche come server di streaming oppure il contenuto può essere posizionato direttamente nel computer dell'utente finale, ad esempio se si usa un sistema di distribuzione del software elettronico, come Microsoft endpoint Configuration Manager. In un'implementazione multiserver, il mantenimento del contenuto del pacchetto e la sua conservazione aggiornata in tutti i server di flusso richiedono una soluzione di gestione dei pacchetti completa. A seconda delle dimensioni dell'organizzazione, potrebbe essere necessario disporre di molte applicazioni virtuali accessibili per gli utenti finali dislocati in tutto il mondo. La gestione dei pacchetti per garantire che le applicazioni giuste siano disponibili per tutti gli utenti dove e quando è necessario accedervi è quindi un requisito essenziale.

La guida alla pianificazione e distribuzione di Application Virtualization offre informazioni utili per comprendere meglio e distribuire l'applicazione Microsoft Application Virtualization e i relativi componenti. Vengono inoltre fornite procedure dettagliate per l'implementazione degli scenari di distribuzione principali.

## In questa sezione


<a href="" id="planning-for-application-virtualization-system-deployment"></a>[Pianificazione della distribuzione del sistema Application Virtualization](planning-for-application-virtualization-system-deployment.md)  
Fornisce le indicazioni necessarie per pianificare l'implementazione e la distribuzione del sistema di virtualizzazione dell'applicazione.

<a href="" id="application-virtualization-deployment-and-upgrade-considerations"></a>[Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)  
Fornisce informazioni sui requisiti hardware e software per installare i vari componenti di virtualizzazione delle applicazioni, nonché le informazioni sull'aggiornamento.

<a href="" id="electronic-software-distribution-based-scenario"></a>[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)  
Fornisce informazioni sulla distribuzione della virtualizzazione delle applicazioni tramite un sistema ESD (Electronic Software Distribution).

<a href="" id="application-virtualization-server-based-scenario"></a>[Scenario basato su Application Virtualization Server](application-virtualization-server-based-scenario.md)  
Fornisce informazioni sulla distribuzione della virtualizzazione delle applicazioni con Application Virtualization Management Server.

<a href="" id="stand-alone-delivery-scenario-for-application-virtualization-clients"></a>[Scenario di recapito autonomo per i Application Virtualization Client](stand-alone-delivery-scenario-for-application-virtualization-clients.md)  
Descrive come distribuire la virtualizzazione delle applicazioni in una modalità autonoma, senza l'uso di ESD o risorse basate su server.

<a href="" id="application-virtualization-reference"></a>[Riferimento per Application Virtualization](application-virtualization-reference.md)  
Contiene materiale dettagliato di riferimento tecnico relativo all'installazione e alla gestione dei componenti di sistema.

 

 





