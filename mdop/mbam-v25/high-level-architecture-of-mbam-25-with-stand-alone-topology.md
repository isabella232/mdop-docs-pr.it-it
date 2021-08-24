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
ms.openlocfilehash: 9ec9b1e4391fde3083564f34b5f89d1c5bd174f7
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910671"
---
# <a name="high-level-architecture-of-mbam-25-with-stand-alone-topology"></a>Architettura di alto livello di MBAM 2.5 con topologia autonoma


In questo argomento viene descritta l'architettura consigliata per la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia autonoma di Configuration Manager. In questa topologia MBAM viene distribuito come prodotto autonomo. In alternativa, è possibile distribuire MBAM con la topologia di integrazione di Configuration Manager, che integra MBAM con Configuration Manager. Per ulteriori informazioni, vedere [High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md).

Per un elenco delle versioni supportate del software menzionato in questo argomento, vedere [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).

**Nota**  
È consigliabile utilizzare un'architettura a server singolo solo in ambienti di test.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Numero consigliato di server e numero supportato di client


Il numero consigliato di server e il numero supportato di client in un ambiente di produzione è il seguente:

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
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="recommended-mbam-high-level-architecture-with-the-stand-alone-topology"></a>Architettura di alto livello MBAM consigliata con la topologia autonoma


Il diagramma e la tabella seguenti descrivono l'architettura a due server di alto livello consigliata per MBAM con la topologia autonoma. Le distribuzioni a più foreste MBAM richiedono un trust unidirezionale o bidirezionale. I trust unidirezionale richiedono che il dominio del server considera attendibile il dominio client.

![mbam2.](images/mbam2-5-2servers.png)

Server Features to configure on this server Description Database server

Database di conformità e controllo

Questa funzionalità è configurata in un server che esegue Windows Server e supporta SQL Server istanza.

Il **database di conformità e controllo** archivia i dati di conformità, che vengono utilizzati principalmente per i report SQL Server Reporting Services host.

Database di ripristino

Questa funzionalità è configurata in un server che esegue Windows Server e supporta SQL Server istanza.

Il **database di ripristino** archivia i dati di ripristino raccolti dai computer client MBAM.

Rapporti

Questa funzionalità è configurata in un server che esegue Windows Server e supporta SQL Server istanza.

I **report forniscono** i dati sullo stato di conformità e di controllo del ripristino relativi ai computer client dell'organizzazione. È possibile accedere ai report dal sito Web amministrazione e monitoraggio o direttamente da SQL Server Reporting Services.

Amministrazione e Monitoring Server

Sito Web di amministrazione e monitoraggio

Questa funzionalità è configurata in un computer che esegue Windows Server.

Il **sito Web amministrazione e monitoraggio** viene utilizzato per:

-   Aiutare gli utenti finali a recuperare l'accesso ai computer quando sono bloccati. Quest'area del sito Web è comunemente chiamata Help Desk.

-   Visualizzare i report che mostrano lo stato di conformità e l'attività di ripristino per i computer client.

Self-Service Portal

Questa funzionalità è configurata in un computer che esegue Windows Server.

Il **portale self-service** è un sito Web che consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.

Monitoraggio dei servizi Web per questo sito Web

Questa funzionalità è configurata in un computer che esegue Windows Server.

I **servizi Web di monitoraggio** vengono utilizzati dal client MBAM e dai siti Web per comunicare con il database.

**Importante**  
Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 poiché i siti Web MBAM comunicano direttamente con il database di ripristino.

 

Workstation di gestione

Modelli di Criteri di gruppo MBAM

-   I modelli di Criteri di gruppo MBAM sono impostazioni di Criteri di gruppo che definiscono le impostazioni di implementazione per MBAM, che consentono di gestire Crittografia unità BitLocker.

-   Prima di eseguire MBAM, è necessario scaricare i modelli di Criteri di gruppo da Come ottenere modelli di Criteri di gruppo [MDOP (admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation che esegue un sistema operativo Windows Server o Windows supportato.

-   La workstation non deve essere un computer dedicato.

Client MBAM e computer client di Configuration Manager

Software client MBAM

Il client MBAM:

-   Usa oggetti Criteri di gruppo per applicare Crittografia unità BitLocker ai computer client dell'organizzazione.

-   Raccoglie la chiave di ripristino bitlocker per tre tipi di unità dati: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

-   Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.



## <a name="related-topics"></a>Argomenti correlati


[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

[Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)

[Funzionalità illustrate di una distribuzione di MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

## <a name="got-a-suggestion-for-mbam"></a>Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, utilizzare il [Forum TechNet di MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





