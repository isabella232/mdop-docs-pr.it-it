---
title: Come usare il portale self-service per riottenere l'accesso a un computer
description: Come usare il portale self-service per riottenere l'accesso a un computer
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826076"
---
# Come usare il portale self-service per riottenere l'accesso a un computer


Se gli utenti finali vengono bloccati da Windows da BitLocker perché hanno dimenticato la password o il PIN oppure perché hanno modificato i file del sistema operativo o hanno modificato il BIOS o il Trusted Platform Module (TPM), possono usare il portale self-service per ottenere l'accesso a Windows senza dover chiedere assistenza al proprio help desk.

**Nota**  Se l'amministratore IT ha configurato un timeout per lo stato sessione di IIS, viene visualizzato un messaggio di 60 secondi prima del timeout.

 

**Nota**  Queste istruzioni sono scritte per e dal punto di vista degli utenti finali.

 

**Per usare il portale self-service per ottenere l'accesso a un computer**

1.  Nel campo **Recovery keyId** immettere un minimo di otto dell'ID della chiave bitlocker di 32 cifre visualizzato nella schermata di ripristino di BitLocker del computer.

    **Nota**  Se le prime otto cifre corrispondono a più tasti, viene visualizzato un messaggio che richiede l'immissione di tutte le cifre di 32 dell'ID chiave di ripristino.

     

2.  Nel campo **motivo** selezionare un motivo per la richiesta per il tasto di ripristino.

3.  Fare clic su **Ottieni chiave**. La chiave di ripristino di BitLocker viene visualizzata nel campo "chiave di ripristino di BitLocker".

4.  Immettere il codice a 48 cifre nella schermata di ripristino di BitLocker nel computer per ottenere l'accesso al computer.

## Argomenti correlati


[Gestione di BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





