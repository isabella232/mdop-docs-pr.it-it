---
title: Come recuperare un'unità danneggiata
description: Come recuperare un'unità danneggiata
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822875"
---
# Come recuperare un'unità danneggiata


Per recuperare un'unità danneggiata protetta da BitLocker, un utente dell'help desk di amministrazione e monitoraggio di Microsoft BitLocker dovrà creare un file di pacchetto chiave di ripristino. Questo file di pacchetto può quindi essere copiato nel computer che contiene l'unità danneggiata e quindi usato per recuperare l'unità. Usare la procedura seguente per i passaggi necessari per eseguire questa operazione.

**Importante**  Per evitare una potenziale perdita di dati, è consigliabile leggere la guida "Repair-bde" e capire chiaramente come usare il comando prima di completare le istruzioni seguenti.

 

**Per recuperare un'unità danneggiata**

1.  Per creare il pacchetto chiave di ripristino necessario per recuperare un'unità danneggiata, avviare un Web browser e aprire il sito Web di amministrazione e monitoraggio di MBAM.

2.  Selezionare **ripristino unità** dal riquadro di spostamento sinistro. Immettere il nome di dominio dell'utente, il nome utente, il motivo per sbloccare l'unità e l'ID password di ripristino dell'utente.

    **Nota**  Se si è membri del ruolo Help desk Administrators, non è necessario immettere il nome di dominio o il nome utente dell'utente.

     

3.  Fai clic su **Invia**. Verrà visualizzata la chiave di ripristino.

4.  Fare clic su **Salva**e quindi selezionare **pacchetto chiave di ripristino**. Il pacchetto chiave di ripristino verrà creato nel computer.

5.  Copiare il pacchetto della chiave di ripristino nel computer in cui è presente l'unità danneggiata.

6.  Apri una finestra del prompt dei comandi con privilegi elevati. A tale scopo, fare clic su **Avvia** e digitare `cmd` nella **casella Cerca programmi e file**. Fare clic con il pulsante destro del mouse **cmd.exe** e scegliere **Esegui come amministratore**.

7.  Al prompt dei comandi digitare quanto segue:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Nota**  Sostituire &lt; l'unità fissa &gt; con un'unità disco rigido disponibile che disponga di spazio libero uguale o maggiore rispetto ai dati nell'unità danneggiata. I dati dell'unità danneggiata vengono recuperati e spostati nell'unità disco rigido specificata.

     

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





