---
title: Come recuperare un'unità spostata
description: Come recuperare un'unità spostata
author: dansimp
ms.assetid: 0c7199d8-9463-4f44-9af3-b70eceeaff1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e73e0878a3102d56494feb33efa69182029988c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804594"
---
# Come recuperare un'unità spostata


Quando si trasferisce un'unità del sistema operativo crittografata in precedenza con Microsoft BitLocker Administration and Monitoring (MBAM), è necessario risolvere alcuni problemi. Dopo aver allegato un PIN al nuovo computer, l'unità non accetterà il PIN di avvio usato nel computer precedente. Il sistema considera non valido il PIN a causa della modifica del chip TPM (Trusted Platform Module). È necessario ottenere un ID chiave di ripristino per recuperare la password di ripristino per poter usare l'unità spostata. Per eseguire questa operazione, usare la procedura seguente.

**Per recuperare un'unità spostata**

1.  Nel computer che contiene l'unità spostata, iniziare in modalità ambiente ripristino Windows (WinRE) o avviare il computer usando il set di strumenti di diagnostica e ripristino Microsoft.

2.  Dopo aver avviato il computer con WinRE o DaRT, MBAM tratterà l'unità di sistema operativo spostata come unità dati. MBAM visualizzerà quindi l'ID password di ripristino dell'unità e chiederà la password di ripristino.

    **Nota**  In alcuni casi, potresti essere in grado di fare clic su **dimentica il pin** durante il processo di avvio per accedere alla modalità di ripristino. In questo articolo viene visualizzato anche l'ID chiave di ripristino.

     

3.  Nel sito Web Amministrazione MBAM usare l'ID chiave di ripristino per recuperare la password di ripristino e sbloccare l'unità.

4.  Se l'unità spostata è stata configurata per l'uso di un chip TPM nel computer originale, è necessario eseguire ulteriori passaggi dopo l'apertura dell'unità e completare il processo di avvio. In modalità WinRE aprire un prompt dei comandi e usare lo strumento **Manage-bde** per decrittografare l'unità. L'uso di questo strumento è l'unico modo per rimuovere la protezione TPM-Plus-PIN senza il chip TPM originale.

5.  Al termine della rimozione, avviare il sistema in genere. L'agente MBAM procederà per applicare il criterio per crittografare l'unità con il PIN TPM Plus del nuovo computer.

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam.md)

 

 





