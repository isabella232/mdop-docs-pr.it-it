---
title: Informazioni sulla scheda File
description: Informazioni sulla scheda File
author: dansimp
ms.assetid: 3c20e720-4b0f-465b-b7c4-3013dae1c815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e71cd0b60f9722da9736fc6987100f5c7bf53ab
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819926"
---
# Informazioni sulla scheda File


Nella scheda **file** viene visualizzato l'elenco completo dei file inclusi in un pacchetto di applicazione sequenziata. Nel riquadro sinistro viene visualizzato, in un formato di visualizzazione file standard, l'elenco completo dei file nel pacchetto creato durante la sequenziazione dell'applicazione. Questi file includono la directory radice del pacchetto (la directory specificata durante la fase di installazione dell'applicazione), la cartella VFS (Virtual File System) e i file di ambiente virtuale. Nel riquadro destro vengono visualizzati il nome file, gli attributi di file e gli attributi Sequencer.

## Nome file e nome breve


<a href="" id="file-name"></a>**Nome file**  
Il nome del file si trova nel riquadro sinistro. I file visualizzati nel riquadro sinistro vengono creati durante la sequenziazione.

<a href="" id="short-name"></a>**Nome breve**  
Questo è il nome di un file selezionato nel riquadro sinistro, scritto nella convenzione di denominazione dei formati di 8,3.

## Attributi file


<a href="" id="file-size"></a>**Dimensioni file**  
Dimensione del file in byte.

<a href="" id="file-version"></a>**Versione del file**  
La versione del file selezionato.

<a href="" id="date-created"></a>**Data creazione**  
Data e ora in cui è stato creato il file selezionato.

<a href="" id="date-modified"></a>**Data di modifica**  
Data e ora dell'Ultima modifica del file selezionato.

<a href="" id="file-id"></a>**File ID**  
GUID del file.

## Attributi sequencer


<a href="" id="user-data"></a>**Dati utente**  
Selezionare questo attributo per specificare che un'applicazione deve conservare le informazioni di un singolo utente.

<a href="" id="application-data"></a>**Dati dell'applicazione**  
Selezionare questo attributo per specificare che un'applicazione deve conservare le informazioni generali di un gruppo di utenti.

<a href="" id="override"></a>**Sostituisci**  
Quando l'opzione è selezionata, il client Desktop Application Virtualization sovrascrive il file corrispondente quando il pacchetto dell'applicazione sequenziata viene aggiornato e trasmesso al client. Se questa casella di controllo non è selezionata, il client determina se sovrascrivere o meno il file selezionato.

## Argomenti correlati


[Come modificare i file inclusi in un pacchetto](how-to-modify-the-files-included-in-a-package.md)

[Console di Sequencer](sequencer-console.md)

 

 





