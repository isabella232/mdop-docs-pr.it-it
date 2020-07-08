---
title: Informazioni sulla scheda Proprietà
description: Informazioni sulla scheda Proprietà
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819925"
---
# Informazioni sulla scheda Proprietà


Usare la scheda **Proprietà** per visualizzare informazioni statistiche di base su un pacchetto di applicazione sequenziata. Le informazioni vengono generate automaticamente, se non diversamente specificato. Questa scheda contiene gli elementi seguenti.

## Informazioni sul pacchetto


<a href="" id="package-name"></a>**Nome pacchetto**  
Il singolo nome usato per un pacchetto di applicazione sequenziale che potrebbe contenere una o più applicazioni, ad esempio Microsoft Office può essere usato per assegnare un'etichetta a un pacchetto di applicazione sequenziale che contiene le applicazioni Microsoft Word e Microsoft Excel eseguite nello stesso ambiente virtuale.

<a href="" id="comments"></a>**Commenti**  
Visualizza una breve descrizione del pacchetto software che verrà visualizzato nell'elemento astratto del file OSD (Open Software Descriptor). Questo elemento è facoltativo.

<a href="" id="package-version"></a>**Versione del pacchetto**  
Versione del pacchetto dell'applicazione sequenziata.

<a href="" id="package-guid"></a>**GUID del pacchetto**  
L'identificatore univoco globale (GUID) assegnato automaticamente al pacchetto dell'applicazione sequenziata per distinguerlo dagli altri pacchetti di applicazioni sequenziate che potrebbero essere in uso nel computer in cui è in streaming un pacchetto di applicazione sequenziata.

<a href="" id="package-version-guid"></a>**GUID versione pacchetto**  
GUID della versione del pacchetto dell'applicazione sequenziata.

<a href="" id="root-directory"></a>**Directory radice**  
Directory nel computer di sequenziazione in cui sono installati i file per il pacchetto dell'applicazione sequenziata. Questa directory viene creata anche nel computer in cui verrà trasmesso un pacchetto di applicazione sequenziata. È consigliabile per la compatibilità con le versioni precedenti che si tratta di un nome di directory in formato 8,3 nella radice dell'unità Q, ad esempio Q:\\MyApp.1\\.

<a href="" id="created"></a>**Creato**  
Data e ora in cui è stato creato il pacchetto dell'applicazione sequenziata.

<a href="" id="modified"></a>**Modificato**  
Data e ora dell'Ultima modifica del pacchetto dell'applicazione sequenziata.

<a href="" id="package-size"></a>**Dimensioni del pacchetto**  
Dimensioni del pacchetto in megabyte.

<a href="" id="launch-size"></a>**Dimensioni di avvio**  
Dimensioni in megabyte della parte del file SFT necessaria per avviare l'applicazione.

## Parametri di sequenziazione


<a href="" id="block-size"></a>**Dimensione blocco**  
Specifica le dimensioni dei blocchi di funzionalità primari e secondari in cui il file SFT è diviso per lo streaming in una rete. Tutti i blocchi equivalgono alle dimensioni specificate; l'ultimo blocco potrebbe tuttavia essere più piccolo di quello specificato. Verrà visualizzato uno dei valori seguenti:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

**Nota**  Dopo aver creato il pacchetto iniziale, il valore della dimensione del blocco non è modificabile.

 

## Argomenti correlati


[Come modificare le proprietà del pacchetto](how-to-change-package-properties.md)

[Console di Sequencer](sequencer-console.md)

 

 





