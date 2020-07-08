---
title: Architettura di alto livello
description: Architettura di alto livello
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826205"
---
# Architettura di alto livello


La soluzione MED-V include gli elementi seguenti:

-   **Macchina virtuale definita dall'amministratore**: incapsula un ambiente desktop completo, tra cui un sistema operativo, le applicazioni e gli strumenti di gestione e sicurezza facoltativi.

-   **Archivio immagini**: archivia tutte le immagini virtuali in un server IIS standard e consente la gestione delle versioni delle immagini virtuali, il recupero delle immagini autenticate dal client e il download efficiente (di una nuova immagine o aggiornamenti) tramite la tecnologia di trasferimento dei ritagli.

-   **Server di gestione**: associa le immagini virtuali del repository di immagini insieme ai criteri di utilizzo dell'amministratore a Active Directory® utenti o gruppi. Il server di gestione aggrega inoltre gli eventi dei client e li archivia in un database esterno (Microsoft SQL Server®) per scopi di monitoraggio e creazione di report.

-   **Console di gestione**: consente agli amministratori di controllare il server di gestione e il repository di immagini.

-   **Client per utenti finali**

    1.  Ciclo di vita dell'immagine virtuale: autenticazione, recupero delle immagini, applicazione dei criteri di utilizzo.

    2.  Gestione sessioni della macchina virtuale: avviare, arrestare, bloccare la macchina virtuale.

    3.  Esperienza desktop singola: le applicazioni installate nella macchina virtuale sono facilmente disponibili tramite il menu Start desktop standard e integrate con altre applicazioni sul desktop dell'utente.

Tutte le comunicazioni tra il client e i server (server di gestione e archivio immagini) vengono effettuate sopra un canale HTTP o HTTPS standard.

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





