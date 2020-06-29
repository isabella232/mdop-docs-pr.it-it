---
title: Monitoraggio dei contatori delle prestazioni per le richieste di servizi Web
description: Monitoraggio dei contatori delle prestazioni per le richieste di servizi Web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823876"
---
# Monitoraggio dei contatori delle prestazioni per le richieste di servizi Web


Microsoft BitLocker Administration and Monitoring (MBAM) offre contatori delle prestazioni che registrano le prestazioni delle richieste inviate ai seguenti servizi Web:

-   **StatusReportingService. svc** -servizio che riceve le richieste per lo stato di conformità

-   **CoreService. svc** -servizio che riceve le richieste per i tentativi di recupero delle chiavi

## Contatori delle prestazioni forniti da MBAM


MBAM offre i contatori delle prestazioni seguenti per ognuno dei metodi pubblici implementati dai relativi servizi Web StatusReportingService e CoreService:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di contatore delle prestazioni</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Numero totale di richieste</p></td>
<td align="left"><p>Fornisce un conteggio incrementale che inizia da zero quando il server viene avviato o riavviato.</p>
<p>Offre una visualizzazione complessiva delle attività di sistema. Può essere monitorata da strumenti automatizzati per garantire l'integrità del server e per verificare che il contatore venga incrementato continuamente in un determinato periodo di tempo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Richieste al secondo</p></td>
<td align="left"><p>Indica la velocità effettiva corrente del server MBAM in quanto supporta la base client di MBAM.</p>
<p>Consente agli amministratori del sito di:</p>
<ul>
<li><p>Calcolare il numero medio di richieste al secondo, in base al numero di client MBAM e alla frequenza di segnalazione.</p></li>
<li><p>Verificare che il numero di richieste al secondo sia ampiamente correlato al numero medio calcolato di richieste al secondo. Una varianza significativa può indicare che il client MBAM non è installato in una percentuale della base client o che un oggetto Criteri di gruppo di MBAM non è stato distribuito correttamente.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Richiedi durata</p></td>
<td align="left"><p>Registra la durata delle richieste in millisecondi.</p>
<p>Anche se questo contatore viene aggiornato con la durata di ogni richiesta, Windows Performance Monitor lo campiona solo periodicamente (in genere ogni secondo), quindi potresti vedere una certa variabilità nel valore. Per questo motivo, è consigliabile usare il valore medio visualizzato da performance monitor.</p></td>
</tr>
</tbody>
</table>

 

## Risultati e suggerimenti per i contatori delle prestazioni


Man mano che si aggiungono nuovi client MBAM a un server MBAM con capacità di riserva, si prevede di visualizzare un aumento del numero di richieste al secondo. Questo aumento sarà proporzionale al numero di nuovi computer client. La durata della richiesta media rimarrà relativamente statica. Man mano che il server raggiunge la sua capacità massima, le richieste al secondo iniziano a livellarsi e la durata della richiesta media inizia a essere più lunga.

In caso di dubbi sul fatto che i server MBAM possano supportare la propria base client, valutare la possibilità di distribuire MBAM in fasi tra diverse raccolte di computer client. Durante la distribuzione di MBAM in ogni raccolta di computer client, è consigliabile eseguire snapshot dei contatori delle prestazioni per vedere l'impatto relativo della distribuzione in ogni nuova raccolta di client. Se il numero di richieste al secondo inizia a livellare e la durata media della richiesta aumenta, è consigliabile migliorare l'infrastruttura di MBAM server eseguendo una delle operazioni seguenti:

-   Spostamento del database MBAM su un cluster Microsoft SQL Server o SQL Server dedicato

-   MBAM di bilanciamento del carico in più server Web Internet Information Services (IIS)

-   Distribuzione di MBAM su hardware server più potente

## Visualizzazione di contatori delle prestazioni


Lo strumento consigliato per la visualizzazione dei contatori delle prestazioni di MBAM è Windows Performance Monitor, che include Windows. Se si usa Windows PowerShell, non è necessario abilitare i contatori prima della loro visualizzazione, perché vengono automaticamente registrati dal cmdlet **Enable-WebApplication** di Windows PowerShell.

Per istruzioni dettagliate su come visualizzare i contatori delle prestazioni, vedere [come visualizzare i contatori delle prestazioni di mbam](https://go.microsoft.com/fwlink/?LinkId=393457).



## Argomenti correlati


[Manutenzione di MBAM 2.5](maintaining-mbam-25.md)

 

 


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).


