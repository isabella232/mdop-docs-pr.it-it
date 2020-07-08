---
title: Come ripristinare un blocco del TPM
description: Come ripristinare un blocco del TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823325"
---
# Come ripristinare un blocco del TPM


Questo argomento illustra come usare il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per reimpostare un blocco TPM. I blocchi TPM possono verificarsi se un utente finale immette il PIN errato troppo spesso. Numero di volte in cui un utente può immettere un PIN errato prima che i blocchi TPM varino da produttore a produttore.

Nell'area **Manage TPM** del sito Web amministrazione e monitoraggio è possibile accedere al sistema di dati di ripristino della chiave centralizzata, che fornisce un file di password del proprietario del TPM quando si specifica un ID computer e un identificatore utente associato.

Per accedere all'area manage TPM del sito Web di amministrazione e monitoraggio, è necessario essere assegnati al ruolo degli utenti di MBAM helpdesk o al ruolo di utenti avanzati helpdesk di MBAM. Questi ruoli sono gruppi creati dagli amministratori in Active Directory. Puoi usare qualsiasi nome per questi gruppi. Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

Per informazioni su MBAM e la proprietà TPM, vedere [considerazioni sulla sicurezza di mbam 2,5](mbam-25-security-considerations.md#bkmk-tpm).

**Per reimpostare un blocco TPM**

1.  Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.

2.  Nel riquadro sinistro fare clic su **Gestisci TPM** per aprire la pagina **Manage TPM** .

3.  Immettere il nome di dominio completo per il computer e il nome del computer.

4.  Immettere il dominio di log-in Windows dell'utente finale e il nome utente per recuperare il file della password del proprietario del TPM.

    **Nota**  Se ci si trova nel gruppo MBAM Advanced helpdesk Users, il dominio utente e i campi ID utente non sono obbligatori.

     

5.  Dal **motivo per richiedere** l'elenco dei file di password del proprietario del TPM selezionare un motivo per la richiesta e fare clic su **Invia**.

    MBAM restituisce una delle opzioni seguenti:

    -   Messaggio di errore se non viene trovato un file di password del proprietario del TPM corrispondente

    -   File di password del proprietario del TPM per il computer inviato

    Dopo aver recuperato la password del proprietario del TPM, viene visualizzata la password del proprietario.

6.  Per salvare la password in un file con estensione TPM, fare clic sul pulsante **Salva** .

7.  Nell'area **Manage TPM** del **sito Web amministrazione e monitoraggio**selezionare l'opzione **Reimposta il blocco TPM** e specificare il file della password del proprietario del TPM.

    Il blocco TPM viene reimpostato e l'accesso dell'utente finale viene ripristinato.

    **Importante**  Non assegnare il valore hash TPM o il file della password del proprietario del TPM agli utenti finali. Dato che le informazioni sul TPM non cambiano, il file viene creato dagli utenti finali per creare un rischio per la sicurezza.

     



## Argomenti correlati


[Gestione di BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





