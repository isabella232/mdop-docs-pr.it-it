---
title: Come recuperare un'unità in modalità di ripristino
description: Come recuperare un'unità in modalità di ripristino
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825056"
---
# Come recuperare un'unità in modalità di ripristino


Le funzionalità di ripristino delle unità crittografate di Microsoft BitLocker Administration and Monitoring (MBAM) garantiscono l'acquisizione e l'archiviazione dei dati e la disponibilità degli strumenti necessari per accedere a un volume protetto da BitLocker quando BitLocker entra in modalità di ripristino. Un volume protetto da BitLocker entra in modalità di ripristino quando un PIN o una password viene persa o dimenticata oppure quando il chip TPM (Trusted Module Platform) rileva le modifiche apportate al BIOS o ai file di avvio di un computer.

Questa procedura consente di accedere al sistema di dati di ripristino centralizzato delle chiavi, che può fornire una password di ripristino se viene fornito un ID password di ripristino e un Identificativo utente associato.

**Importante**  
L'amministrazione e il monitoraggio di Microsoft BitLocker usano chiavi di ripristino monouso che scadono al momento dell'uso. L'uso singolo di una password di ripristino viene applicato automaticamente alle unità del sistema operativo e alle unità fisse. In unità rimovibili viene applicata quando l'unità viene rimossa e quindi reinserita e sbloccata in un computer in cui sono attivate le impostazioni dei criteri di gruppo per gestire le unità rimovibili.



**Per recuperare un'unità in modalità di ripristino**

1.  Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio.

2.  Nel riquadro di spostamento fare clic su **ripristino unità**. Verrà visualizzata la pagina Web "Recupera accesso a un'unità crittografata".

3.  Immettere il dominio di accesso di Windows e il nome utente dell'utente per visualizzare le informazioni di ripristino e le prime otto cifre dell'ID chiave di ripristino per ricevere un elenco di possibili chiavi di ripristino corrispondenti o dell'intero ID chiave di ripristino per ricevere l'esatta chiave di ripristino.

4.  Selezionare una delle opzioni predefinite dall'elenco **motivo per l'unità di sblocco** e quindi fare clic su **Invia**.

    **Nota**  
    Se si è un utente di MBAM Advanced helpdesk, le voci di dominio utente e ID utente non sono necessarie.



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. Per copiare la password, fare clic su **copia chiave**e quindi incollare la password di ripristino in un messaggio di posta elettronica. In alternativa, fare clic su **Salva** per salvare la password di ripristino in un file.

   Quando l'utente digita la password di ripristino nel sistema o usa il pacchetto di ripristino, l'unità viene sbloccata.

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









