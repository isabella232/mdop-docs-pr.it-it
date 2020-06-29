---
title: Risoluzione dei problemi di Application Virtualization Sequencer
description: Risoluzione dei problemi di Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815245"
---
# Risoluzione dei problemi di Application Virtualization Sequencer


Questo argomento include informazioni che è possibile usare per risolvere i problemi generali di Application Virtualization (App-V) Sequencer.

## La creazione di un file SFTD tramite App-V Sequencer aumenta il numero di versione in modo imprevisto


Usare la riga di comando per generare un nuovo file SFT. Per creare il file SFT usando la riga di comando, immettere quanto segue al prompt dei comandi:

**mkdiffpkg.exe &lt; base SFT nome file &gt; &lt; diff SFT nome file&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>Il nome file nel file OSD non è corretto dopo l'aggiornamento del pacchetto


Quando si apre un pacchetto per l'aggiornamento, è necessario specificare l'unità root Q:\\ come percorso di output per il pacchetto. Non specificare un nome file associato con la posizione di output.

## L'installazione predefinita di Microsoft Word2003 genera un errore quando viene trasmesso a un client


Quando si esegue lo streaming di Microsoft Word2003 in un client, viene restituito un errore, ma Microsoft Word continua a essere eseguito.

**Soluzione**

Risequenziare il pacchetto dell'applicazione virtuale e selezionare **installazione completa**.

## L'aggiornamento attivo non funziona quando si crea un pacchetto dipendente


Quando si crea un pacchetto dipendente con l'aggiornamento attivo e si aggiungono nuove voci del registro di sistema, il funzionamento viene eseguito correttamente, ma le voci del registro di sistema aggiornate non sono disponibili.

**Soluzione**

Le impostazioni del registro di sistema vengono sempre archiviate con la versione originale del pacchetto, quindi gli aggiornamenti al pacchetto non saranno disponibili, a meno che non si ripari il pacchetto originale.

## Le informazioni dettagliate non sono visibili per i documenti di Microsoft office2007 tramite la pagina delle proprietà


Quando si prova a visualizzare informazioni dettagliate associate a un documento di Microsoft office2007 tramite la pagina delle proprietà, le informazioni dettagliate non sono visibili.

**Soluzione**

App-V non supporta le estensioni di Shell necessarie per queste pagine delle proprietà.

## Alcune chiavi del registro di sistema non vengono acquisite quando si sequenziano le applicazioni a 16 bit


In App-V 4,5 l'aggancio del registro di sistema è stato spostato dalla modalità kernel alla modalità utente. Se si vuole sequenziare un'applicazione a 16 bit o un'applicazione che usa un programma di installazione a 16 bit, è necessario prima di tutto configurare il computer sequencer in modo che il processo venga eseguito in una copia di Windows NT Virtual DOS Machine (NTVDM).

**Soluzione**

Prima di sequenziare l'applicazione, imposta il valore della chiave del registro di sistema REGSZ globale seguente su "Yes" nel computer di sequenziazione:

HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM

È necessario riavviare il computer prima che questa operazione abbia effetto.

## Argomenti correlati


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





