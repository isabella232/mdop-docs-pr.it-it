---
title: Come recuperare un'unità danneggiata
description: Come recuperare un'unità danneggiata
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804606"
---
# Come recuperare un'unità danneggiata


Per recuperare un'unità danneggiata protetta da BitLocker, un utente dell'help desk di amministrazione e monitoraggio di Microsoft BitLocker deve creare un file di pacchetto chiave di ripristino. Questo file di pacchetto può essere copiato nel computer che contiene l'unità danneggiata e quindi usato per recuperare l'unità. Per eseguire questa operazione, usare la procedura seguente.

**Per recuperare un'unità danneggiata**

1.  Aprire il sito Web di amministrazione di MBAM.

2.  Selezionare **ripristino unità** dal riquadro di spostamento. Immettere il nome di dominio e il nome utente dell'utente, il motivo per cui è stato sbloccato l'unità e l'ID password di ripristino dell'utente.

    **Nota**  Se si è membri del ruolo Help desk Administrators, non è necessario immettere il nome di dominio o il nome utente dell'utente.

     

3.  Fai clic su **Invia**. Verrà visualizzata la chiave di ripristino.

4.  Fare clic su **Salva**e quindi selezionare **pacchetto chiave di ripristino**. Il pacchetto chiave di ripristino verrà creato nel computer.

5.  Copiare il pacchetto della chiave di ripristino nel computer in cui è presente l'unità danneggiata.

6.  Apri una finestra del prompt dei comandi con privilegi elevati. A tale scopo, fare clic su **Avvia** e digitare `cmd` nella casella **Cerca programmi e file** . Nell'elenco dei risultati della ricerca fare clic con il pulsante destro del mouse **cmd.exe** e scegliere **Esegui come amministratore**.

7.  Al prompt dei comandi digitare quanto segue:

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    **Nota**  Per l' &lt; unità fissa &gt; nel comando, specificare un dispositivo di archiviazione disponibile che disponga di spazio libero uguale o maggiore rispetto ai dati nell'unità danneggiata. I dati dell'unità danneggiata vengono recuperati e spostati nell'unità fissa specificata.

     

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





