---
title: Informazioni sulla risoluzione dei problemi per Application Virtualization Server
description: Informazioni sulla risoluzione dei problemi per Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815186"
---
# Informazioni sulla risoluzione dei problemi per Application Virtualization Server


Questo argomento include le informazioni che è possibile usare per risolvere i problemi relativi ai vari tipi di server Application Virtualization (App-V).

## Messaggio di avviso 25017 nel log di installazione dopo l'installazione del server


Dopo l'installazione potrebbe essere visualizzato il messaggio seguente nel log di configurazione del server.

*Avviso 25017. Il programma di installazione non può creare l'oggetto indicatore di Active Directory per il server. L'account usato per l'installazione non ha i diritti sufficienti per scrivere in Active Directory o Active Directory non è disponibile.*

Il programma di installazione di App-V Management o Streaming Server crea una voce del punto di connessione del servizio sotto l'oggetto computer in servizi di dominio Active Directory che corrisponde al computer in cui è installato il server se l'account usato per eseguire il programma di installazione ha i diritti appropriati. La mancata creazione di questa voce non comporterà un errore di installazione e ciò non dovrebbe influire in altro modo sul funzionamento del prodotto. La causa probabile di qualsiasi errore è che l'account utente usato per eseguire l'installazione non dispone di diritti sufficienti per la scrittura in aggiunte. Anche se la registrazione dell'App-V Server in aggiunte è facoltativa, uno dei vantaggi di questa operazione consente agli strumenti di gestione centralizzati di individuare l'App-V Server per scopi di inventario e gestione.

## Argomenti correlati


[Application Virtualization Server](application-virtualization-server.md)

 

 





