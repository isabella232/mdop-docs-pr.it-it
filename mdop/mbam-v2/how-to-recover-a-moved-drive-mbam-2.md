---
title: Come recuperare un'unità spostata
description: Come recuperare un'unità spostata
author: dansimp
ms.assetid: 697cd78d-962c-411e-901a-2e9220ba6552
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bd0d43f2eea95fe71225a50e7fa68d4fb1c35485
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825065"
---
# Come recuperare un'unità spostata


Quando si trasferisce un'unità del sistema operativo crittografata tramite Microsoft BitLocker Administration and Monitoring (MBAM), l'unità non accetterà il PIN usato in un computer precedente a causa della modifica del chip TPM (Trusted Platform Module). Per usare l'unità spostata, è necessario un modo per ottenere l'ID chiave di ripristino per recuperare la password di ripristino. Usare la procedura seguente per recuperare un'unità spostata.

**Per recuperare un'unità spostata**

1.  Nel computer che contiene l'unità spostata, avviare il computer in modalità ambiente ripristino Windows (WinRE) o avviare il computer usando il set di strumenti di diagnostica e ripristino Microsoft (DaRT).

2.  Dopo aver avviato il computer con WinRE o DaRT, l'amministrazione e il monitoraggio di Microsoft BitLocker considereranno l'unità di sistema operativo spostata come unità dati. MBAM visualizzerà quindi l'ID password di ripristino dell'unità e chiederà la password di ripristino.

    **Nota**  In alcuni casi, è possibile fare clic su **ho dimenticato il pin** durante il processo di avvio e quindi immettere la modalità di ripristino per visualizzare l'ID chiave di ripristino.

     

3.  Usare l'ID chiave di ripristino per recuperare la password di ripristino e sbloccare l'unità dal sito Web di amministrazione e monitoraggio.

4.  Se l'unità spostata è stata configurata per l'uso di un chip TPM nel computer originale, è necessario eseguire ulteriori operazioni dopo lo sblocco dell'unità e il completamento del processo di avvio. In modalità WinRE aprire un prompt dei comandi e usare lo strumento **Manage-bde** per decrittografare l'unità. L'uso di questo strumento è l'unico modo per rimuovere la protezione del PIN TPM Plus senza il chip TPM originale.

5.  Una volta completata la rimozione, avviare il computer in genere. L'agente MBAM implicherà ora il criterio per crittografare l'unità con il PIN TPM Plus del nuovo computer.

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





