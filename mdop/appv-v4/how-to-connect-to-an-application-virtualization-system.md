---
title: Come connettersi a un sistema di Application Virtualization
description: Come connettersi a un sistema di Application Virtualization
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817715"
---
# Come connettersi a un sistema di Application Virtualization


È necessario connettere la console di gestione server Application Virtualization a un sistema di virtualizzazione dell'applicazione prima di poter usare la console di gestione per gestire le applicazioni, le associazioni di tipi di file, i pacchetti, le licenze per le applicazioni, i gruppi di server, i criteri e gli amministratori La procedura seguente illustra i passaggi che è necessario seguire per connettere la console a un sistema di virtualizzazione dell'applicazione.

**Per connettersi a un sistema di virtualizzazione delle applicazioni**

1. Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro **ambito** e scegliere **Connetti a Application Virtualization System** dal menu a comparsa.

   **Nota**  
   Sono disponibili tre componenti per la gestione di Application Virtualization Server: la console di gestione di Application Virtualization, il servizio Web di gestione e il datastore SQL. Se questi componenti sono distribuiti in computer fisici diversi, è necessario configurare correttamente la sicurezza per i componenti per comunicare in tutto il sistema. Per altre informazioni, vedere i manuali e gli articoli seguenti:

   [Come configurare il server in modo che sia attendibile per la delega](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)

   [Guida alla pianificazione e alla distribuzione per il sistema di virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)

   [Guida alle operazioni per l'Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)

   [Articolo 930472](https://go.microsoft.com/fwlink/?LinkId=114647) della Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114647)

   [Articolo 930565](https://go.microsoft.com/fwlink/?LinkId=114648) della Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114648)

     

2. Completare i campi nella finestra di dialogo **Connetti a Application Virtualization System** :

   1. **Nome host servizio Web**: immettere il nome del sistema di virtualizzazione delle applicazioni a cui si vuole connettersi o immettere **localhost** per connettersi al server locale.

   2. **Usa connessione sicura**: selezionare questa casella di controllo se si vuole connettersi al server con una connessione sicura.

   3. **Porta**: immettere il numero di porta che si vuole usare per la connessione. **80** è il numero di porta normale predefinito e **443** è il numero di porta sicura.

   4. **Usare l'account di Windows corrente**: selezionare questo pulsante di opzione per usare le credenziali dell'account di Windows corrente.

   5. **Specificare l'account di Windows**: selezionare questo pulsante di opzione quando si vuole connettersi al server come utente diverso.

   6. **Nome**: immettere il nome del nuovo utente usando il formato *dominio omeutente* o <em> username@domain </em> .

   7. **Password**: immettere la password corrispondente al nuovo utente.

3. Fai clic su **OK**.

## Argomenti correlati


[Come eseguire attività amministrative in Application Virtualization Server Management Console](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





