---
title: Come recuperare un'unità in modalità di ripristino
description: Come recuperare un'unità in modalità di ripristino
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823366"
---
# Come recuperare un'unità in modalità di ripristino


Questo argomento spiega come usare il sito Web di amministrazione e monitoraggio (noto anche come Help desk) per ottenere una password di ripristino da assegnare agli utenti finali se l'unità protetta da BitLocker entra in modalità di ripristino. Le unità entrano in modalità di ripristino se gli utenti perdono o dimenticano il PIN o la password o se il chip TPM (Trusted Module Platform) rileva le modifiche apportate al BIOS o ai file di avvio di un computer.

Per ottenere una password di ripristino, usare l'area di **recupero unità** del sito Web amministrazione e monitoraggio. Per accedere all'area del sito Web, è necessario essere assegnati al ruolo degli utenti di MBAM helpdesk o al ruolo degli utenti dell'helpdesk Advanced.

**Nota**  
Quando sono stati creati, è possibile che siano stati assegnati nomi diversi a questi ruoli. Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).



**Importante**  
Le password di ripristino scadono dopo un singolo utilizzo. Nelle unità del sistema operativo e nelle unità dati fisse viene applicata automaticamente la regola di uso singolo. In unità rimovibili viene applicata quando l'unità viene rimossa e quindi reinserita e sbloccata in un computer in cui sono attivate le impostazioni dei criteri di gruppo per gestire le unità rimovibili.



**Per recuperare un'unità in modalità di ripristino**

1.  Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.

2.  Nel riquadro sinistro selezionare unità di **ripristino** per aprire la pagina **Recupera accesso a una unità crittografata** .

3.  Immettere il dominio di log-in Windows dell'utente finale e il nome utente per visualizzare le informazioni di ripristino.

    **Nota**  
    Se ci si trova nel gruppo MBAM Advanced helpdesk Users, il dominio utente e i campi ID utente non sono obbligatori.



4.  Immettere le prime otto cifre dell'ID chiave di ripristino per visualizzare un elenco di possibili chiavi di ripristino corrispondenti oppure immettere l'intero ID chiave di ripristino per ottenere la chiave di ripristino esatta.

5.  Dall'elenco **motivo per l'unità di sblocco** selezionare una delle opzioni predefinite e quindi fare clic su **Invia**.

    MBAM restituisce il seguente:

    -   Messaggio di errore se non viene trovata una password di ripristino corrispondente

    -   Più possibili corrispondenze se l'utente ha più password di ripristino corrispondenti

    -   La password di ripristino e il pacchetto di ripristino per l'utente inviato

        **Nota**  
        Se si sta recuperando un'unità danneggiata, l'opzione pacchetto di ripristino fornisce a BitLocker le informazioni critiche necessarie per recuperare l'unità.



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. Per copiare la password, fare clic su **copia chiave**e quindi incollare la password di ripristino in un messaggio di posta elettronica. In alternativa, fare clic su **Salva** per salvare la password di ripristino in un file.

   Quando l'utente digita la password di ripristino nel sistema o usa il pacchetto di ripristino, l'unità viene sbloccata.



## Argomenti correlati


[Gestione di BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)



## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





