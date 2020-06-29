---
title: Come usare il portale self-service per riottenere l'accesso a un computer
description: Come usare il portale self-service per riottenere l'accesso a un computer
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826705"
---
# Come usare il portale self-service per riottenere l'accesso a un computer


Il portale self-service è un sito Web che gli amministratori IT configurano come parte della propria distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5. Il sito Web consente agli utenti finali di recuperare in modo indipendente l'accesso ai propri computer se vengono bloccati da Windows. Il portale self-service non richiede assistenza dal personale dell'help desk.

Le istruzioni seguenti vengono scritte dal punto di vista degli utenti finali, ma le informazioni potrebbero essere utili per gli amministratori IT.

**Importante**  Un utente finale deve avere eseguito fisicamente l'accesso al computer (non in remoto) almeno una volta con successo per poter recuperare la chiave usando il portale self-service. In caso contrario, deve usare il portale helpdesk per il ripristino della chiave.

 

Gli utenti finali possono verificare i blocchi se:

-   Dimenticare la password o il PIN

-   Modificare i file di sistema operativo, il BIOS o il Trusted Platform Module (TPM)

**Nota**  Se l'amministratore IT ha configurato un timeout per lo stato sessione di IIS, viene visualizzato un messaggio nel portale self-service 60 secondi prima del timeout.

 

**Per usare il portale self-service per ottenere l'accesso a un computer**

1.  Nel campo **Recovery keyId** immettere un minimo di otto dell'ID della chiave bitlocker di 32 cifre visualizzato nella schermata di ripristino di BitLocker del computer. Se le prime otto cifre corrispondono a più tasti, viene visualizzato un messaggio che richiede l'immissione di tutte le cifre di 32 dell'ID chiave di ripristino.

2.  Nel campo **motivo** selezionare un motivo per la richiesta per il tasto di ripristino.

3.  Fare clic su **Ottieni chiave**. La chiave di ripristino di BitLocker viene visualizzata nel campo **chiave di ripristino di BitLocker** .

4.  Immettere il codice a 48 cifre nella schermata di ripristino di BitLocker nel computer per ottenere l'accesso al computer.



## Argomenti correlati


[Gestione di BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





