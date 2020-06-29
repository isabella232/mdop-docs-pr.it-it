---
title: Configurazione dell'amministrazione di App-V per un ambiente distribuito
description: Configurazione dell'amministrazione di App-V per un ambiente distribuito
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821915"
---
# Configurazione dell'amministrazione di App-V per un ambiente distribuito


Quando si progetta l'infrastruttura per la propria organizzazione, è possibile installare il servizio Web di gestione App-V in un computer diverso dal computer in cui si installa l'App-V Management Server. I motivi comuni per separare questi componenti App-V includono i seguenti:

-   Prestazioni

-   Affidabilità

-   Disponibilità

-   Scalabilità

La separazione del server di gestione e del servizio Web di gestione richiede una configurazione aggiuntiva per l'infrastruttura per funzionare correttamente. Quando si separano queste due caratteristiche ma non si completano le procedure descritte in questo argomento, la console di gestione si connette al servizio Web di gestione, ma non sarà in grado di eseguire correttamente l'autenticazione con l'archivio dati. La console di gestione non viene caricata correttamente e l'amministratore non sarà in grado di completare le attività amministrative.

Questo comportamento si verifica perché il servizio Web di gestione non può usare le credenziali, passate dalla console di gestione, per accedere all'archivio dati. La soluzione consiste nel configurare il server del servizio Web di gestione come "attendibile per la delega".

## Configurazione dei servizi di dominio Active Directory


È anche necessario configurare correttamente i servizi di dominio Active Directory in modo che funzionino in un ambiente distribuito. Questa sezione include le informazioni necessarie per configurare i servizi di dominio Active Directory.

### Quando SQL Service usa l'account di sistema locale

Per configurare l'ambiente in cui il servizio SQL usa l'account di sistema locale, modificare le proprietà dell'account del computer del servizio Web di gestione come attendibile per la delega. Per informazioni dettagliate su come eseguire questa operazione, vedere [come configurare il server come attendibile per la delega](how-to-configure-the-server-to-be-trusted-for-delegation.md)

### Quando il servizio SQL usa un account basato su dominio

Per configurare l'ambiente in cui SQL Server usa account del servizio basati su dominio, è necessario valutare se applicare o meno una varietà di fattori, inclusi i seguenti:

-   Raggruppamento di SQL Server

-   Replica

-   Attività automatizzate

-   Server collegati

Per informazioni sulla configurazione dei servizi di dominio Active Directory quando il servizio SQL usa un account basato su dominio, vedere <https://go.microsoft.com/fwlink/?LinkId=151968> .

 

 





