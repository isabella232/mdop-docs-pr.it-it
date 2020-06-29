---
title: Pubblicazione delle applicazioni virtuali con distribuzione elettronica del software
description: Pubblicazione delle applicazioni virtuali con distribuzione elettronica del software
author: dansimp
ms.assetid: 295fbc1d-ed1c-43b4-aeee-0df384d4e630
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0354fc1226aa78d947dd764a0ab6157b563a321
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815745"
---
# Pubblicazione delle applicazioni virtuali con distribuzione elettronica del software


Un sistema ESD (Electronic Software Distribution) è progettato per trasferire in modo efficiente il software a molti computer diversi tramite connessioni di rete lente o veloci. Con la virtualizzazione delle applicazioni, usando un sistema ESD, puoi usare uno dei metodi seguenti per distribuire i pacchetti di applicazioni virtuali:

-   Configurare il sistema ESD per distribuire i pacchetti direttamente a ogni computer client usando la versione di Windows Installer del pacchetto generato da Application Virtualization Sequencer. Il file di Windows Installer contiene le icone, le informazioni sulla definizione dei pacchetti e il contenuto e quando si usa Windows Installer pubblica le icone sul desktop di Windows e sul menu Start e carica il contenuto del pacchetto nella cache del client di Application Virtualization. L'utente può iniziare subito a usare le applicazioni senza ulteriori requisiti di configurazione. L'aggiornamento di un pacchetto a una versione più recente viene eseguito tramite Windows Installer per disinstallare il file package.msi e quindi per installare la nuova versione.

-   Posizionare il contenuto del pacchetto in un punto di distribuzione del software o Application Virtualization Streaming Server che è facilmente accessibile ai computer client tramite una connessione di rete con una buona larghezza di banda, ad esempio una LAN. Ad esempio, è possibile usare i computer del punto di distribuzione del sistema ESD esistente in ogni filiale. Usando i parametri della riga di comando per definire l'origine di flusso da cui i client eseguiranno il flusso del pacchetto di applicazione virtuale, il sistema ESD distribuirebbe la versione di Windows Installer del pacchetto a ogni client. Il sistema ESD può anche essere usato per copiare il file SFT che contiene il contenuto del pacchetto nella condivisione file in tutti i server di flusso. L'aggiornamento di un pacchetto a una versione più recente viene eseguito tramite Windows Installer per disinstallare il file package.msi e quindi installare la nuova versione.

-   In alternativa all'uso del file self-contained di Windows Installer in una delle modalità precedenti per la distribuzione dei pacchetti, è possibile controllare la distribuzione in modo molto più dettagliato usando la lingua della riga di comando di Application Virtualization SFTMIME. In questo articolo vengono forniti molti comandi per controllare tutti gli aspetti della gestione dei pacchetti. Mentre SFTMIME è potente, è anche complessa, quindi gli amministratori dovrebbero pianificare la creazione di tutti i comandi come script e testarli a fondo in un ambiente di test prima dell'uso della produzione. Per altre informazioni sui comandi di SFTMIME disponibili, vedi la pagina di riferimento dei comandi di [SFTMIME](sftmime--command-reference.md).

## Argomenti correlati


[Scenario basato sulla distribuzione elettronica del software](electronic-software-distribution-based-scenario.md)

[Pianificazione della distribuzione del sistema Application Virtualization](planning-for-application-virtualization-system-deployment.md)

[Pianificazione della soluzione di streaming in un'implementazione della distribuzione elettronica del software](planning-your-streaming-solution-in-an-electronic-software-distribution-implementation.md)

[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)

 

 





