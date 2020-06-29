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
ms.openlocfilehash: c3b205d4f0b4b18cf8bdbf51982b5a59e5e1b9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804197"
---
# Funzionalità illustrate di una distribuzione di MBAM 2.5


Questo argomento descrive le singole caratteristiche che costituiscono una distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 per le topologie seguenti:

-   MBAM autonomo

-   Integrazione di System Center Configuration Manager

**Importante**  
Queste caratteristiche non rappresentano l'architettura consigliata per la distribuzione di MBAM. Usare queste informazioni solo come guida per comprendere le singole funzionalità che costituiscono una distribuzione di MBAM. Vedi [architettura di alto livello per mbam 2,5](high-level-architecture-for-mbam-25.md) per l'architettura consigliata per mbam.



Per un elenco delle versioni supportate del software menzionato in questo argomento, Vedi le [configurazioni supportate di MBAM 2,5](mbam-25-supported-configurations.md).

## <a href="" id="bkmk-standalone"></a> Topologia autonoma di MBAM


L'immagine e la tabella seguenti spiegano le funzionalità di una topologia autonoma di MBAM.

![mbab2\-5](images/mbam2-5-standalonecomponents.png)

|Tipo di funzionalità|Descrizione|Database|
|-|-|-|
|Database di ripristino|Questo database archivia i dati di recupero raccolti dai computer client di MBAM.|Questa caratteristica è configurata in un server che supporta Windows Server e un'istanza di SQL Server supportata.|
|Database di conformità e controllo|Questo database archivia i dati di conformità, che vengono usati principalmente per i report ospitati da SQL Server Reporting Services.|Questa caratteristica è configurata in un server che supporta Windows Server e un'istanza di SQL Server supportata.|
|Report di conformità e controllo|||
|Servizio Web Reporting|Questo servizio Web consente la comunicazione tra il sito Web di amministrazione e monitoraggio e l'istanza di SQL Server in cui vengono archiviati i dati di report.|Questa funzionalità è installata in un server che utilizza Windows Server.|
|Sito Web di report (sito Web di amministrazione e monitoraggio)|È possibile visualizzare i report dal sito Web amministrazione e monitoraggio. I report includono i dati di controllo del ripristino e dello stato di conformità relativi ai computer client dell'organizzazione.|Questa funzionalità è configurata in un server che utilizza Windows Server.|
|SQL Server Reporting Services (SSRS)|I report vengono configurati in un'istanza del database SSRS. I report possono essere visualizzati direttamente da SSRS o dal sito Web di amministrazione e monitoraggio.|Questa caratteristica è configurata in un server che gestisce Windows Server e un'istanza di SQL Server supportata in cui è in uso SSRS.|
|Server self-service|||
|Servizio Web Self-Service|Questo servizio Web viene usato dal client MBAM e dal sito Web di amministrazione e monitoraggio e dal portale self-service per comunicare con il database di ripristino.|Questa funzionalità è installata in un computer che gestisce Windows Server.|
|Sito Web Self-Service (portale self-service)|Questo sito Web consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.|Questa caratteristica è configurata in un computer che gestisce Windows Server.|
|Server di amministrazione e monitoraggio|||
|Servizio Web di amministrazione e monitoraggio|Il servizio Web di monitoraggio viene usato dal client MBAM e dai siti Web per comunicare con i database.|Questa funzionalità è installata in un computer che gestisce Windows Server.|

**Importante**  
Il servizio Web Self-Service non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, in cui il client MBAM, il sito Web di amministrazione e monitoraggio e il portale self-service comunicano direttamente con il database di ripristino.

**Importante**  
Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 poiché il client MBAM e i siti Web comunicano direttamente con il database di ripristino.


## <a href="" id="bkmk-cmintegrated"></a>Topologia di integrazione di System Center Configuration Manager

L'immagine e la tabella seguenti illustrano le caratteristiche della topologia di integrazione di System Center Configuration Manager.

![mbam2\-5](images/mbam2-5-cmcomponents.png)

**Importante**  
Il servizio Web Self-Service non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1, in cui il client MBAM, il sito Web di amministrazione e monitoraggio e il portale self-service comunicano direttamente con il database di ripristino.

**Warning**  
Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 poiché il client MBAM e i siti Web comunicano direttamente con il database di ripristino.


|                        Tipo di funzionalità                        |                                                                                                    Descrizione                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Server self-service                     |                                                                                                                                                                                                                   |
|                  Servizio Web Self-Service                  |                                                 Questo servizio Web viene usato dal client MBAM e dal portale self-service per comunicare con il database di ripristino.                                                  |
|                    Sito Web Self-Service                    |                          Questo sito Web consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.                          |
| Report di controllo di amministrazione e monitoraggio server/ripristino |                                                                                                                                                                                                                   |
|         Servizio Web di amministrazione e monitoraggio          |                               Questo servizio Web consente la comunicazione tra il sito Web di amministrazione e monitoraggio e i database di SQL Server in cui vengono archiviati i dati di report.                               |
|           Sito Web di amministrazione e monitoraggio            | Il report di controllo del recupero viene visualizzato dal sito Web di amministrazione e monitoraggio. Usare la console di Configuration Manager per visualizzare tutti gli altri report oppure visualizzare i report direttamente da SQL Server Reporting Services. |
|                         Database                          |                                                                                                                                                                                                                   |
|                     Database di ripristino                      |                                                                 Questo database archivia i dati di recupero raccolti dai computer client di MBAM.                                                                  |
|                       Database di controllo                       |                                                                   Questo database archivia le informazioni di controllo sui tentativi di ripristino e sulle attività.                                                                    |
|               Caratteristiche di Configuration Manager               |                                                                                                                                                                                                                   |
|          Configuration Manager Management Console          |                                                                   Questa console è integrata in Configuration Manager e viene usata per visualizzare i report.                                                                   |
|               Report di Configuration Manager                |                                                             I report mostrano i dati di controllo della conformità e del ripristino per i computer client nell'organizzazione.                                                              |
|               SQL Server Reporting Services                |                                                SSRS consente i report di MBAM. I report possono essere visualizzati direttamente da SSRS o dalla console di Configuration Manager.                                                 |

## Argomenti correlati

[Architettura di alto livello per MBAM 2.5](high-level-architecture-for-mbam-25.md)

[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




