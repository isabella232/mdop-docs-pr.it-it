---
title: Come ripristinare un blocco del TPM
description: Come ripristinare un blocco del TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804588"
---
# Come ripristinare un blocco del TPM


La caratteristica di ripristino delle unità crittografata di Microsoft BitLocker Administration and Monitoring (MBAM) include sia l'acquisizione che l'archiviazione dei dati e la disponibilità per gli strumenti necessari per la gestione del TPM (Trusted Platform Module). Questo argomento illustra come accedere al sistema di dati di ripristino centralizzato delle chiavi nel sito Web di bit \ _admmon \ _tlanextref amministrazione. Il sistema di dati di ripristino della chiave può fornire un file di password del proprietario del TPM quando viene fornita l'identità del computer e l'identificatore dell'utente associato.

Se un utente immette un PIN errato troppo spesso, può verificarsi un blocco TPM. Numero di volte in cui un utente può immettere un PIN errato prima che il blocco TPM sia basato sulla specifica del produttore del computer.

**Per reimpostare un blocco TPM**

1.  Aprire il sito Web di amministrazione di MBAM.

2.  Nel riquadro di spostamento selezionare **Gestisci TPM**. Verrà aperta la pagina **Manage TPM** .

3.  Immettere il nome di dominio completo (FQDN) per il computer e il nome del computer. Immettere il dominio di accesso di Windows dell'utente e il nome utente dell'utente. Selezionare una delle opzioni predefinite nel **motivo per richiedere** il menu a discesa file di password del proprietario del TPM. Fai clic su **Invia**.

4.  MBAM restituirà una delle opzioni seguenti:

    -   Messaggio di errore se non viene trovato un file di password del proprietario del TPM corrispondente

    -   File di password del proprietario del TPM per il computer inviato

    **Nota**  Se si è un utente di helpdesk avanzato, il dominio utente e i campi ID utente non sono obbligatori.

     

5.  Al momento del recupero viene visualizzata la password del proprietario. Per salvare la password in un file con estensione TPM, fare clic sul pulsante **Salva** .

6.  L'utente eseguirà la console di gestione TPM e selezionerà l'opzione **Reimposta il blocco TPM** e fornirà il file della password del proprietario del TPM per reimpostare il blocco TPM.

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





