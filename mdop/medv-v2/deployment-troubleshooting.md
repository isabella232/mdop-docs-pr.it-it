---
title: Risoluzione dei problemi relativi alla distribuzione
description: Risoluzione dei problemi relativi alla distribuzione
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822896"
---
# Risoluzione dei problemi relativi alla distribuzione


Questo argomento include informazioni utili per risolvere i problemi di distribuzione in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Risoluzione dei problemi relativi alla distribuzione di MED-V


Il problema seguente può verificarsi quando si distribuisce MED-V. La soluzione consente di risolvere il problema.

**Si verificano problemi se si installa MED-V solo per l'utente corrente.** MED-V supporta solo l'installazione di Packager area di lavoro MED-V, dell'agente host MED-V e dell'area di lavoro MED-V per tutti gli utenti. L'installazione per l'utente corrente causa solo errori nell'installazione dei componenti e nella configurazione dell'area di lavoro MED-V.

**Soluzione**

Non usare mai l'opzione **ALLUSERS = ""** quando si installano i componenti MED-V.

**MED-V richiede l'uso esclusivo dello stack di virtualizzazione.** Solo uno stack di virtualizzazione può essere eseguito alla volta in un computer. Windows Virtual PC deve usare lo stack virtuale e MED-V dipende da Windows Virtual PC. Di conseguenza, se tenti di distribuire o usare MED-V quando sono in esecuzione altre applicazioni che usano lo stack virtuale, MED-V non può essere eseguito o installato correttamente.

**Soluzione**

Chiudere qualsiasi applicazione in esecuzione che usa lo stack di virtualizzazione prima di installare o eseguire MED-V.

**I tasti di scelta rapida rimangono dopo la disinstallazione.** Per impostazione predefinita, quando si disinstalla MED-V, i tasti di scelta rapida nel menu **Start** dell'utente finale vengono rimossi. Tuttavia, in alcune situazioni, ad esempio per gli utenti finali che usano profili mobili, le scelte rapide da usare per le applicazioni pubblicate in MED-V restano nel menu **Start** dell'utente finale.

**Soluzione**

Per eliminare manualmente i tasti di scelta rapida rimanenti nel menu **Start** , fare clic con il pulsante destro del mouse sui tasti di scelta rapida e quindi scegliere **Rimuovi**.

**Disabilitare l'impostazione di criteri di gruppo dei messaggi di accesso nell'area di lavoro MED-V.** Se il messaggio di accesso a Windows XP è abilitato nell'area di lavoro MED-V, l'utente finale deve eseguire l'accesso ogni volta che vuole aprire un'applicazione virtuale MED-V. In questo modo, viene creata un'esperienza utente scadente.

**Soluzione**

Disabilitare le impostazioni di criteri di gruppo seguenti nella macchina virtuale MED-V:

**Accesso interattivo: testo del messaggio per gli utenti che tentano l'accesso**

**Accesso interattivo: titolo del messaggio per gli utenti che tentano l'accesso**

## Argomenti correlati


[Risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md)

 

 





