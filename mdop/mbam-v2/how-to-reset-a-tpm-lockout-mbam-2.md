---
title: Come ripristinare un blocco del TPM
description: Come ripristinare un blocco del TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825055"
---
# Come ripristinare un blocco del TPM


La caratteristica di ripristino delle unità crittografata di Microsoft BitLocker Administration and Monitoring (MBAM) include sia l'acquisizione che l'archiviazione dei dati e la disponibilità per gli strumenti necessari per gestire il TPM (Trusted Platform Module). Questo argomento illustra come accedere al sistema di dati di ripristino della chiave centralizzata nel sito Web di amministrazione e monitoraggio, che può fornire un file di password del proprietario del TPM quando viene fornito un ID computer e un Identificativo utente associato.

Se un utente immette il PIN errato troppe volte, può verificarsi un blocco TPM. Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino da produttore a produttore.

È possibile reimpostare un blocco TPM solo se MBAM è proprietario del TPM.

**Per reimpostare un blocco TPM**

1.  Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio.

2.  Nel riquadro di spostamento sinistro selezionare **Gestisci TPM** per aprire la pagina **Manage TPM** .

3.  Immettere il nome di dominio completo per il computer e il nome del computer e immettere il dominio di accesso di Windows dell'utente e il nome utente dell'utente per recuperare il file della password del proprietario del TPM.

4.  Dal **motivo per richiedere** l'elenco dei file di password del proprietario del TPM selezionare un motivo per la richiesta e fare clic su **Invia**.

    MBAM restituisce una delle opzioni seguenti:

    -   Messaggio di errore, se non viene trovato un file di password del proprietario del TPM corrispondente

    -   File di password del proprietario del TPM per il computer inviato

    **Nota**  
    Se si è un utente di helpdesk avanzato, il dominio utente e i campi ID utente non sono obbligatori.



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. Per salvare la password in un file con estensione TPM, fare clic sul pulsante **Salva** .

   L'utente eseguirà la console di gestione TPM, selezionerà l'opzione **Reimposta il blocco TPM** e fornirà il file della password del proprietario del TPM per reimpostare il blocco TPM.

   **Importante**  
   Gli amministratori del supporto tecnico non devono assegnare al file di password del valore hash TPM o del proprietario del TPM agli utenti finali. Le informazioni sul TPM non cambiano, quindi potrebbero rappresentare un rischio per la sicurezza se il file viene assegnato agli utenti finali.



## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









