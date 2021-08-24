---
title: Funzionalità illustrate di una distribuzione di MBAM 2.5
description: Funzionalità illustrate di una distribuzione di MBAM 2.5
author: dansimp
ms.assetid: 7b5eff42-af8c-4bd0-a20a-18cc2e779f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: 139980fb6712b40685a41bab45610da670803afa
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910621"
---
# <a name="illustrated-features-of-an-mbam-25-deployment"></a>Funzionalità illustrate di una distribuzione di MBAM 2.5


In questo argomento vengono descritte le singole funzionalità che costituiscono una distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 per le topologie seguenti:

-   MBAM autonomo

-   System Center Configuration Manager Integrazione

**Importante**  
Queste funzionalità non rappresentano l'architettura consigliata per la distribuzione di MBAM. Utilizzare queste informazioni solo come guida per comprendere le singole funzionalità che costituiscono una distribuzione di MBAM. Per [l'architettura consigliata per MBAM, vedere High-Level Architecture for MBAM 2.5.](high-level-architecture-for-mbam-25.md)



Per un elenco delle versioni supportate del software menzionato in questo argomento, vedere [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).

## <a name="mbam-stand-alone-topology"></a><a href="" id="bkmk-standalone"></a> Topologia autonoma MBAM


Nell'immagine e nella tabella seguenti vengono illustrate le funzionalità di una topologia autonoma di MBAM.

![mbab2\-5.](images/mbam2-5-standalonecomponents.png)

|Tipo di funzionalità|Descrizione|Database|
|-|-|-|
|Database di ripristino|In questo database vengono archiviati i dati di ripristino raccolti dai computer client MBAM.|Questa funzionalità è configurata in un server che esegue Windows Server e in un'istanza SQL Server supportata.|
|Database di conformità e controllo|In questo database vengono archiviati i dati di conformità, utilizzati principalmente per i report SQL Server Reporting Services host.|Questa funzionalità è configurata in un server che esegue Windows Server e in un'istanza SQL Server supportata.|
|Report di conformità e controllo|||
|Reporting Web Service|Questo servizio Web consente la comunicazione tra il sito Web di amministrazione e monitoraggio e l'SQL Server in cui sono archiviati i dati di report.|Questa funzionalità viene installata in un server che esegue Windows Server.|
|Sito Web di report (sito Web di amministrazione e monitoraggio)|È possibile visualizzare i report dal sito Web amministrazione e monitoraggio. I report forniscono i dati sullo stato di conformità e di controllo del ripristino relativi ai computer client dell'organizzazione.|Questa funzionalità è configurata in un server che esegue Windows Server.|
|SQL Server Reporting Services (SSRS)|I report vengono configurati in un'istanza del database SSRS. I report possono essere visualizzati direttamente da SSRS o dal sito Web amministrazione e monitoraggio.|Questa funzionalità è configurata in un server che esegue Windows Server e in un'istanza SQL Server supportata che esegue SSRS.|
|Self-Service Server|||
|Self-Service Web|Questo servizio Web viene utilizzato dal client MBAM e dal sito Web di amministrazione e monitoraggio e Self-Service Portal per comunicare con il database di ripristino.|Questa funzionalità viene installata in un computer che esegue Windows Server.|
|Self-Service (portale self-service)|Questo sito Web consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.|Questa funzionalità è configurata in un computer che esegue Windows Server.|
|Amministrazione e Monitoring Server|||
|Servizio Web di amministrazione e monitoraggio|Il servizio Web di monitoraggio viene utilizzato dal client MBAM e dai siti Web per comunicare con i database.|Questa funzionalità viene installata in un computer che esegue Windows Server.|

**Importante**  
Il servizio Web Self-Service non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, in cui il client MBAM, il sito Web di amministrazione e monitoraggio e il portale di Self-Service comunicano direttamente con il database di ripristino.

**Importante**  
Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 poiché il client MBAM e i siti Web comunicano direttamente con il database di ripristino.


## <a name="system-center-configuration-manager-integration-topology"></a><a href="" id="bkmk-cmintegrated"></a>System Center Configuration Manager Topologia di integrazione

L'immagine e la tabella seguenti illustrano le funzionalità della topologia di System Center Configuration Manager Integration.

![mbam2\-5.](images/mbam2-5-cmcomponents.png)

**Importante**  
Il servizio Web Self-Service non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1, in cui il client MBAM, il sito Web di amministrazione e monitoraggio e il portale di Self-Service comunicano direttamente con il database di ripristino.

**Warning**  
Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 poiché il client MBAM e i siti Web comunicano direttamente con il database di ripristino.


|                        Tipo di funzionalità                        |                                                                                                    Descrizione                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Self-Service Server                     |                                                                                                                                                                                                                   |
|                  Self-Service Web                  |                                                 Questo servizio Web viene utilizzato dal client MBAM e dal portale Self-Service per comunicare al database di ripristino.                                                  |
|                    Self-Service Website                    |                          Questo sito Web consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.                          |
| Administration and Monitoring Server/Recovery Audit Report |                                                                                                                                                                                                                   |
|         Servizio Web di amministrazione e monitoraggio          |                               Questo servizio Web consente la comunicazione tra il sito Web di amministrazione e monitoraggio e i SQL Server database in cui sono archiviati i dati di report.                               |
|           Sito Web di amministrazione e monitoraggio            | Il report Di controllo del ripristino viene visualizzato dal sito Web amministrazione e monitoraggio. Utilizzare la console di Configuration Manager per visualizzare tutti gli altri report o visualizzare i report direttamente da SQL Server Reporting Services. |
|                         Database                          |                                                                                                                                                                                                                   |
|                     Database di ripristino                      |                                                                 In questo database vengono archiviati i dati di ripristino raccolti dai computer client MBAM.                                                                  |
|                       Database di controllo                       |                                                                   In questo database sono archiviate le informazioni di controllo sui tentativi di ripristino e sulle attività.                                                                    |
|               Funzionalità di Configuration Manager               |                                                                                                                                                                                                                   |
|          Console di gestione di Configuration Manager          |                                                                   Questa console è incorporata in Configuration Manager e viene utilizzata per visualizzare i report.                                                                   |
|               Report di Configuration Manager                |                                                             I report mostrano i dati di controllo di conformità e ripristino per i computer client dell'organizzazione.                                                              |
|               SQL Server Reporting Services                |                                                SSRS abilita i report MBAM. I report possono essere visualizzati direttamente da SSRS o dalla console di Configuration Manager.                                                 |

## <a name="related-topics"></a>Argomenti correlati

[Architettura di alto livello per MBAM 2.5](high-level-architecture-for-mbam-25.md)

[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

## <a name="got-a-suggestion-for-mbam"></a>Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, utilizzare il [Forum TechNet di MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




