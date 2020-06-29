---
title: Informazioni su Application Virtualization Sequencer
description: Informazioni su Application Virtualization Sequencer
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819996"
---
# Informazioni su Application Virtualization Sequencer


Microsoft Application Virtualization (App-V) Sequencer monitora e registra tutti i processi di installazione e configurazione per un'applicazione e crea i file seguenti: **ico**, **OSD**, **SFT**e **SPRJ**. Questi file contengono tutte le informazioni necessarie su un'applicazione in modo che l'applicazione possa essere eseguita in un ambiente virtuale nei computer di destinazione. Puoi usare Microsoft Application Virtualization (App-V) Sequencer per creare applicazioni virtuali. Dopo aver sequenziato un'applicazione, è possibile eseguirne il flusso per i computer di destinazione oppure i computer di destinazione possono eseguire l'applicazione virtuale scaricando il contenuto del pacchetto di applicazione virtuale ed eseguendo l'applicazione localmente.

**Importante**  Per eseguire un pacchetto di applicazione virtuale, il computer di destinazione deve eseguire la versione appropriata del client App-V.

 

I pacchetti di applicazioni virtuali vengono eseguiti nei computer di destinazione senza interagire con il sistema operativo sottostante nel computer di destinazione, perché ogni applicazione viene eseguita in un ambiente virtuale ed è isolata da altre applicazioni installate o in esecuzione nel computer di destinazione. Questo isolamento può ridurre i conflitti tra le applicazioni e può contribuire a diminuire la quantità necessaria di test pre-distribuzione dell'applicazione.

## Terminologia Sequencer


<a href="" id="application-virtualization-drive"></a>Unità di virtualizzazione delle applicazioni  
L'unità di virtualizzazione dell'applicazione è l'unità predefinita (Q:\) nel computer di destinazione in cui vengono eseguite le applicazioni sequenziate.

<a href="" id="ico-file"></a>File ICO  
Il file dell'icona sul desktop client che viene usato per avviare un'applicazione sequenziata.

<a href="" id="installation-directory"></a>Directory di installazione  
Directory utilizzata dal sequencer per inserire i file di installazione durante l'installazione.

<a href="" id="open-software-descriptor--osd--file"></a>File OSD (Open Software Descriptor)  
Un file basato su XML che indica al client App-V come recuperare l'applicazione sequenziata dall'App-V Streaming Server e come eseguire l'applicazione sequenziata nell'ambiente virtuale.

<a href="" id="package-root-directory"></a>Directory radice del pacchetto  
Directory nel computer di sequenziazione in cui sono installati i file per il pacchetto dell'applicazione sequenziata. Questa directory esiste anche virtualmente nel computer in cui verrà trasmessa un'applicazione sequenziata.

<a href="" id="sequenced-application"></a>Applicazione sequenziata  
Un'applicazione monitorata dal sequencer, suddivisa in blocchi di funzionalità primari e secondari, in streaming in un computer di destinazione in cui è in esecuzione l'App-V Client t e viene eseguito un ambiente virtuale.

<a href="" id="sequenced-application-package"></a>Pacchetto di applicazione sequenziata  
I file che includono un'applicazione virtuale e consentono l'esecuzione di un'applicazione virtuale. Questi file vengono creati dopo la sequenziazione e includono in particolare i file **OSD**, **SFT**, **SPRJ**e **ico** .

<a href="" id="sequencing"></a>Sequenziamento  
Processo di creazione di un pacchetto dell'applicazione tramite App-V Sequencer. In questo processo viene monitorata un'applicazione, vengono configurati i tasti di scelta rapida e viene creato un pacchetto di applicazione sequenziata.

<a href="" id="sequencing-computer"></a>Sequenziazione del computer  
Il computer usato per sequenziare un'applicazione.

<a href="" id="virtual-application"></a>Applicazione virtuale  
Un'applicazione imballata dal sequencer per l'esecuzione in un ambiente virtuale indipendente. L'ambiente virtuale contiene le informazioni necessarie per eseguire l'applicazione nel client senza installare l'applicazione localmente.

<a href="" id="primary-feature-block"></a>Blocco di funzionalità principale  
Il contenuto minimo in un pacchetto di applicazione virtuale necessario per l'esecuzione di un'applicazione in un computer di destinazione. Il contenuto del blocco di funzionalità principale viene identificato durante la fase di applicazione della sequenziazione e in genere è costituito dal contenuto per le caratteristiche dell'applicazione più usate.

## <a href="" id="sequencing-applications-"></a>Sequenziazione delle applicazioni


Esistono due metodi per creare e modificare pacchetti di applicazioni virtuali nell'ambiente. Il primo metodo consiste nell'usare la **sequenziazione** guidata. La **sequenziazione** guidata consente di creare nuovi o modificare i pacchetti di applicazioni virtuali esistenti. Per altre informazioni sull'uso della procedura guidata per la **sequenziazione** , vedere [come sequenziare una nuova applicazione](how-to-sequence-a-new-application.md). Il secondo metodo consiste nell'usare la riga di comando. La riga di comando consente di creare nuovi o modificare pacchetti di applicazioni virtuali esistenti tramite il prompt dei comandi. Per altre informazioni sull'uso della riga di comando, vedere [come gestire le applicazioni virtuali tramite la riga di comando](how-to-manage-virtual-applications-using-the-command-line.md).

La **sequenziazione** guidata offre le funzioni seguenti per la creazione di pacchetti di applicazioni virtuali:

1.  **Configurazione del pacchetto**: la **sequenziazione** guidata richiede le informazioni di configurazione del pacchetto necessarie per completare il file OSD (Open Software Descriptor), che è un file obbligatorio per l'avvio di un pacchetto di applicazione sequenziata.

2.  **Installazione dell'applicazione**: la **sequenziazione** guidata raccoglie informazioni sulle configurazioni di installazione e avvio di un'applicazione. Monitora e registra le informazioni di installazione e avvio associate all'applicazione per creare i file necessari per un pacchetto di applicazione virtuale.

3.  **Avvio di un'applicazione**: la **sequenziazione** guidata raccoglie informazioni per la compilazione e l'ordinamento dei blocchi di codice necessari per eseguire l'avvio iniziale del pacchetto di applicazione sequenziata nel computer di destinazione. La compilazione del blocco di codice viene definita blocco di funzionalità principale.

## Considerazioni sulla sicurezza di Application Virtualization Sequencer


App-V Sequencer esegue tutti i servizi rilevati in fase di sequenziazione usando l'account di sistema locale e non applica i descrittori di sicurezza sulle richieste di controllo del servizio. Se il servizio è stato installato con un account utente diverso o se i descrittori di sicurezza hanno lo scopo di concedere autorizzazioni di servizio specifiche per gruppi di utenti diversi, valutare attentamente se il servizio deve essere virtualizzato. In alcuni casi, è necessario installare il servizio localmente per verificare che la sicurezza del servizio prevista venga mantenuta.

**Importante**  È consigliabile salvare sempre i pacchetti di applicazioni virtuali in una posizione sicura.

 

## Argomenti correlati


[Panoramica di Application Virtualization Sequencer](application-virtualization-sequencer-overview.md)

 

 





