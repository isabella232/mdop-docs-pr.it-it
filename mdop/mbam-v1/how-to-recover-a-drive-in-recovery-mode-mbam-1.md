---
title: Come recuperare un'unità in modalità di ripristino
description: Come recuperare un'unità in modalità di ripristino
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804612"
---
# Come recuperare un'unità in modalità di ripristino


Microsoft BitLocker Administration and Monitoring (MBAM) include funzionalità crittografate per il ripristino delle unità. Queste funzionalità garantiscono l'acquisizione e l'archiviazione dei dati e la disponibilità di strumenti necessari per accedere a un volume protetto da BitLocker quando BitLocker inserisce tale volume in modalità di ripristino. Un volume protetto da BitLocker entra in modalità di ripristino quando un PIN o una password viene persa o dimenticata oppure quando il chip TPM (Trusted Module Platform) rileva una modifica del BIOS o dei file di avvio del computer.

Questa procedura consente di accedere al sistema di dati di ripristino della chiave centralizzata in grado di fornire una password di ripristino quando viene fornito un ID password di ripristino e un Identificativo utente associato.

**Importante**  MBAM genera chiavi di ripristino monouso. In questa limitazione, una chiave di ripristino può essere usata una sola volta e quindi non è più valida. L'uso singolo di una password di ripristino viene applicato automaticamente alle unità del sistema operativo e alle unità fisse. In unità rimovibili, il singolo uso viene applicato quando l'unità viene rimossa e quindi reinserita e sbloccata in un computer in cui sono attivate le impostazioni dei criteri di gruppo per gestire le unità rimovibili.

 

**Per recuperare un'unità in modalità di ripristino**

1.  Aprire il sito Web di MBAM.

2.  Nel riquadro di spostamento fare clic su **ripristino unità**. Viene visualizzata la pagina Web **Recupera accesso a un'unità crittografata** .

3.  Immettere il dominio di accesso di Windows e il nome utente dell'utente e le prime otto cifre dell'ID chiave di ripristino per ricevere un elenco di possibili chiavi di ripristino corrispondenti. In alternativa, immettere l'intero ID chiave di ripristino per ricevere l'esatta chiave di ripristino. Selezionare una delle opzioni predefinite nell'elenco a discesa **motivo per l'unità di sblocco** e quindi fare clic su **Invia**.

    **Nota**  Se si è un utente di MBAM Advanced helpdesk, le voci di dominio utente e ID utente non sono necessarie.

     

4.  MBAM restituisce il seguente:

    1.  Messaggio di errore se non viene trovata una password di ripristino corrispondente

    2.  Più possibili corrispondenze se l'utente ha più password di ripristino corrispondenti

    3.  La password di ripristino e il pacchetto di ripristino per l'utente inviato

        **Nota**  Se si sta recuperando un'unità danneggiata, l'opzione pacchetto di ripristino fornisce a BitLocker le informazioni critiche necessarie per tentare il ripristino.

         

5.  Dopo aver recuperato la password di ripristino e il pacchetto di ripristino, viene visualizzata la password di ripristino. Per copiare la password, fare clic su **copia chiave**e quindi incollare la password di ripristino in un messaggio di posta elettronica o in un altro file di testo per lo spazio di archiviazione temporaneo. In alternativa, per salvare la password di ripristino in un file, fare clic su **Salva**.

6.  Quando l'utente digita la password di ripristino nel sistema o usa il pacchetto di ripristino, l'unità viene sbloccata.

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





