---
title: Manutenzione di MBAM 1.0
description: Manutenzione di MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825775"
---
# Manutenzione di MBAM 1.0


Dopo aver completato tutte le pianificazioni necessarie e quindi distribuito Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurare MBAM per l'esecuzione in modo altamente disponibile durante l'uso per gestire le operazioni di crittografia di BitLocker aziendali. Le informazioni in questa sezione descrive le opzioni di disponibilità elevata per MBAM, nonché come trasferire le funzionalità del server MBAM, se necessario.

## MBAM Management Pack


Il Management Pack di MicrosoftSystemCenterOperationsManager per MBAM è disponibile per il download dall'area download Microsoft.

Questo Management Pack monitora le interazioni critiche nell'infrastruttura lato server, ad esempio le connessioni tra i servizi Web e i database e le chiamate operative tra i siti Web e il servizio Web di supporto. Carica inoltre le richieste tra client desktop e i rispettivi endpoint di servizio Web di ricezione.

[Amministrazione e monitoraggio di Microsoft BitLocker Management Pack](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## Garantire la disponibilità elevata per MBAM 1,0


MBAM è progettato per essere a tolleranza d'errore. Se un server diventa non disponibile, gli utenti non devono essere colpiti negativamente. Le informazioni in questa sezione possono essere usate per configurare un'installazione di MBAM a elevata disponibilità.

[Disponibilità elevata per MBAM 1.0](high-availability-for-mbam-10.md)

## Trasferire le caratteristiche di MBAM 1,0 a un altro server


Quando è necessario trasferire una caratteristica di un server MBAM da un computer server a un altro, esiste un ordine specifico e i passaggi necessari per evitare perdite di produttività o dati. Questa sezione descrive i passaggi da eseguire per trasferire una o più funzionalità di MBAM server in un altro computer.

[Come spostare le funzionalità di MBAM 1.0 in un altro computer](how-to-move-mbam-10-features-to-another-computer.md)

## Altre risorse per la manutenzione di MBAM


[Operazioni relative a MBAM 1.0](operations-for-mbam-10.md)

 

 





