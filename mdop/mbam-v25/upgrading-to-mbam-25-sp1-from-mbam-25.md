---
title: Aggiornamento a MBAM 2.5 SP1 da MBAM 2.5
description: Aggiornamento a MBAM 2.5 SP1 da MBAM 2.5
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 330ded822dd9da96a1c33eabcb31d744044dc28e
ms.sourcegitcommit: ae34c5cb5e7979b472b257a4691142e493d5d6fe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091621"
---
# Aggiornamento a MBAM 2.5 SP1 da MBAM 2.5
Questo argomento descrive il processo per l'aggiornamento di Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 e il client MBAM da 2,5 a MBAM 2,5 SP1.

### Prima di iniziare
#### Scaricare la versione di manutenzione di maggio 2019
[Pacchetto di ottimizzazione desktop](https://www.microsoft.com/download/details.aspx?id=58345)

#### Scaricare la versione di manutenzione di luglio 2018
[Pacchetto di ottimizzazione desktop](https://www.microsoft.com/download/details.aspx?id=57157)


#### Verificare la documentazione dell'installazione
Verificare di avere una documentazione corrente dell'ambiente MBAM, inclusi tutti i nomi dei server, i nomi di database, gli account del servizio e le relative password.

### Passaggi di aggiornamento
#### Procedura per aggiornare il database MBAM (SQL Server)
1. Uso di MBAM Configurator; rimuovere il ruolo report da SQL Server o ovunque sia ospitato il database SSRS. A seconda dell'ambiente, può essere lo stesso server o uno separato.
  > [!NOTE]
  > Non verrà visualizzata un'opzione per rimuovere i database; Questo è previsto.  
2. Installare 2,5 SP1 (che si trova in MDOP-Microsoft Desktop Optimization Pack 2015 dal sito Centro servizi Volume Licensing:  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. Non configurarlo in questo momento 
4. Uso di MBAM Configurator; aggiungere di nuovo il ruolo report
5. Uso di MBAM Configurator; aggiungere di nuovo il ruolo di database SQL in SQL Server
6. Alla fine, sarai avvisato che la DBs esiste già e non è stata creata, ma questo è previsto
7. Questo processo aggiorna i database esistenti alla versione corrente in fase di installazione.              

#### Procedura per aggiornare il server MBAM (in uso MBAM e IIS)
1. Uso di MBAM Configurator; rimuovere i portali amministratore e self service dal server IIS
2. Installare MBAM 2,5 SP1
3. Non configurarlo in questo momento  
4. Uso di MBAM Configurator; aggiungere di nuovo i portali amministratore e self service al server IIS 
5. Aprire un prompt dei comandi con privilegi elevati, digitare **iisreset**e premere INVIO.
 
#### Procedura per aggiornare i client e gli endpoint di MBAM
1. Disinstallare l'agente 2,5 dagli endpoint client
2. Installare l'agente di 2,5 SP1 negli endpoint client
3. Spingere l'aggiornamento del client rollup di maggio 2019 ai client che utilizzano l'agente 2,5 SP1 
4. Non è necessario disinstallare il client esistente prima di installare il rollup di 2019 di maggio.  
