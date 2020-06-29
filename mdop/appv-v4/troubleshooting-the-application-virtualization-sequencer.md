---
title: Risoluzione dei problemi di Application Virtualization Sequencer
description: Risoluzione dei problemi di Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815185"
---
# Risoluzione dei problemi di Application Virtualization Sequencer


Questo argomento include informazioni che è possibile usare per risolvere i problemi generali di Application Virtualization (App-V) Sequencer.

## La creazione di un file SFTD tramite App-V Sequencer aumenta il numero di versione in modo imprevisto


Il numero di versione associato a un file SFTD aumenta in modo imprevisto.

**Soluzione**

Usare la riga di comando per generare un nuovo file SFT. Per creare il file SFT usando la riga di comando, immettere quanto segue al prompt dei comandi:

**mkdiffpkg.exe &lt; base SFT nome file &gt; &lt; diff SFT nome file&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>Il nome file nel file OSD non è corretto dopo l'aggiornamento del pacchetto


Dopo l'aggiornamento di un pacchetto esistente, il nome del file non è corretto.

**Soluzione**

Quando si apre un pacchetto per l'aggiornamento, è necessario specificare l'unità root Q:\\ come percorso di output per il pacchetto. Non specificare un nome file associato con la posizione di output.

## L'installazione predefinita di Microsoft Word2003 genera un errore quando viene trasmesso a un client


Quando si esegue lo streaming di Microsoft Word2003 in un client, viene restituito un errore, ma Microsoft Word continua a essere eseguito.

**Soluzione**

Risequenziare il pacchetto dell'applicazione virtuale e selezionare **installazione completa**.

## L'aggiornamento del pacchetto non funziona quando si crea un pacchetto dipendente


Quando si crea un pacchetto dipendente con l'aggiornamento del pacchetto e si aggiungono nuove voci del registro di sistema, la funzione viene visualizzata correttamente, ma le voci del registro di sistema aggiornate non sono disponibili.

**Soluzione**

Le impostazioni del registro di sistema vengono sempre archiviate con la versione originale del pacchetto, quindi gli aggiornamenti al pacchetto non saranno disponibili, a meno che non si ripari il pacchetto originale.

## Errore durante il tentativo di sequenziazione. NET 2.0


Quando si sequenzia un pacchetto che richiede. NET 2.0 viene visualizzato un messaggio di errore.

**Soluzione**

Sequenziazione di pacchetti che richiedono. NET 2.0 non è supportato.

## Argomenti correlati


[Application Virtualization Sequencer](application-virtualization-sequencer.md)

 

 





