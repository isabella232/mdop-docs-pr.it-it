---
title: Architettura di alto livello di MBAM 2.5 con topologia autonoma
description: Architettura di alto livello di MBAM 2.5 con topologia autonoma
author: dansimp
ms.assetid: 35f8c5f6-8be3-443d-baf0-56d68b08f3bc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 75e878e24b4675f2f2f574791d0f06ecadd0196d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826556"
---
# Architettura di alto livello di MBAM 2.5 con topologia autonoma


Questo argomento descrive l'architettura consigliata per la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia autonoma di Configuration Manager. In questa topologia MBAM viene distribuito come prodotto autonomo. Puoi in alternativa distribuire MBAM con la topologia di integrazione di Configuration Manager, che si integra con MBAM con Configuration Manager. Per altre informazioni, Vedi [architettura di alto livello di MBAM 2,5 con la topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).

Per un elenco delle versioni supportate del software menzionato in questo argomento, Vedi le [configurazioni supportate di MBAM 2,5](mbam-25-supported-configurations.md).

**Nota**  Ti consigliamo di usare un'architettura a server singolo solo in ambienti di test.

 

## Numero consigliato di server e numero di client supportati


Il numero consigliato di server e il numero di client supportati in un ambiente di produzione sono i seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architettura consigliata in un ambiente di produzione</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Numero di server e altri computer</p></td>
<td align="left"><p>Due server</p>
<p>Una workstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Numero di computer client supportati</p></td>
<td align="left"><p>500.000</p></td>
</tr>
</tbody>
</table>

 

## Consigliabile MBAM architettura di alto livello con la topologia autonoma


Il diagramma e la tabella seguenti descrivono l'architettura a due server di alto livello consigliata per MBAM con la topologia autonoma. Le distribuzioni di MBAM multi-Forest richiedono un trust unidirezionale o bidirezionale. I trust unidirezionali richiedono che il dominio del server si fidi del dominio client.

![mbam2](images/mbam2-5-2servers.png)

Funzionalità del server da configurare nel server di database della descrizione del server

Database di conformità e controllo

Questa funzionalità è configurata in un server con Windows Server e in un'istanza di SQL Server supportata.

Il **database di conformità e controllo** archivia i dati di conformità, che vengono usati principalmente per i report ospitati da SQL Server Reporting Services.

Database di ripristino

Questa funzionalità è configurata in un server con Windows Server e in un'istanza di SQL Server supportata.

Il **database di ripristino** archivia i dati di recupero raccolti dai computer client di mbam.

Rapporti

Questa funzionalità è configurata in un server con Windows Server e in un'istanza di SQL Server supportata.

I **report** includono i dati di controllo del ripristino e dello stato di conformità relativi ai computer client dell'organizzazione. È possibile accedere ai report dal sito Web di amministrazione e monitoraggio o direttamente da SQL Server Reporting Services.

Server di amministrazione e monitoraggio

Sito Web di amministrazione e monitoraggio

Questa caratteristica è configurata in un computer che gestisce Windows Server.

Il **sito Web di amministrazione e monitoraggio** viene usato per:

-   Aiutare gli utenti finali a recuperare l'accesso ai propri computer quando sono bloccati. (L'area del sito Web viene comunemente chiamata Help desk).

-   Visualizzare i report che mostrano lo stato di conformità e l'attività di ripristino per i computer client.

Portale self-service

Questa caratteristica è configurata in un computer che gestisce Windows Server.

Il **portale self-service** è un sito Web che consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.

Monitoraggio dei servizi Web per questo sito Web

Questa caratteristica è configurata in un computer che gestisce Windows Server.

I **servizi Web di monitoraggio** vengono usati dal client mbam e dai siti Web per comunicare con il database.

**Importante**  Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 dato che i siti Web di MBAM comunicano direttamente con il database di ripristino.

 

Workstation di gestione

Modelli di criteri di gruppo di MBAM

-   I modelli dei criteri di gruppo di MBAM sono impostazioni di criteri di gruppo che definiscono le impostazioni di implementazione per MBAM, che consentono di gestire la crittografia unità BitLocker.

-   Prima di eseguire MBAM, è necessario scaricare i modelli di criteri di gruppo da [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation che esegue un sistema operativo Windows Server o Windows supportato.

-   La workstation non deve essere un computer dedicato.

Client MBAM e computer client di Configuration Manager

Software client MBAM

Il client MBAM:

-   USA gli oggetti Criteri di gruppo per applicare la crittografia unità BitLocker nei computer client dell'organizzazione.

-   Raccoglie la chiave di ripristino di BitLocker per tre tipi di unità dati: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

-   Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.



## Argomenti correlati


[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

[Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Funzionalità illustrate di una distribuzione di MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





