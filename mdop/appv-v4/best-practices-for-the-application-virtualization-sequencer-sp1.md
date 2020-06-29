---
title: Procedure consigliate per Application Virtualization Sequencer
description: Procedure consigliate per Application Virtualization Sequencer
author: dansimp
ms.assetid: 95e5e216-864f-41a1-90d4-b8d7e1eb42a0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859514fb34185a339c7f2c2734f331e5a99d050
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821996"
---
# Procedure consigliate per Application Virtualization Sequencer


Questo argomento illustra le procedure consigliate per l'uso di Microsoft Application Virtualization (App-V) Sequencer. Esaminare e prendere in considerazione i suggerimenti seguenti per la pianificazione e l'uso del sequencer nell'ambiente.

## Sequenziazione delle procedure consigliate per la configurazione del computer


Quando si configura il computer che ha eseguito App-V Sequencer, è necessario considerare le procedure consigliate seguenti:

-   **Sequenza in un computer con una configurazione simile e che esegua una versione precedente del sistema operativo rispetto ai computer di destinazione.**

    Verificare che il computer in cui è in esecuzione Sequencer esegua una versione precedente del sistema operativo rispetto ai computer di destinazione. Sono incluse le versioni Service Pack e Update. Ad esempio, se i computer di destinazione eseguono WindowsVista e WindowsXP, dovresti sequenziare le applicazioni in un computer che esegue WindowsXP. La possibilità di sequenziare in un sistema operativo ed eseguire l'applicazione virtualizzata in un sistema operativo diverso non è garantita e dipende dalla particolare applicazione e dal sistema operativo. Se si verificano problemi, potrebbe essere necessario eseguire la sequenza nello stesso ambiente del sistema operativo di quello in cui è in uso il client App-V.

-   **Configurare il computer che esegue il sequencer con più partizioni.**

    Devi configurare il computer che esegue il sequencer con almeno due partizioni primarie. La prima partizione (**C:**) deve contenere il sistema operativo e deve essere formattata con il file system NTFS. La seconda partizione (**Q:**) viene usata come percorso di destinazione per l'installazione dell'applicazione virtuale e deve essere formattata anche tramite il file system NTFS.

-   **Configurare la directory Temp con sufficiente spazio disponibile su disco.**

    Il sequencer usa la directory **% tmp%** o **% Temp%** e la directory **Scratch** per archiviare i file temporanei durante la sequenziazione. Queste directory devono essere configurate nel computer in cui è in esecuzione il sequencer con spazio libero su disco equivalente ai requisiti stimati per l'installazione dell'applicazione. È possibile verificare la posizione della directory **Scratch** aprendo la console sequencer e selezionando **strumenti**, **Opzioni**e quindi selezionando la scheda **percorsi** . la configurazione delle directory Temp e della directory **Scratch** in partizioni del disco rigido diverse può migliorare le prestazioni durante la sequenziazione.

-   **Sequenziare le applicazioni usando Microsoft VirtualPC.**

    La maggior parte delle applicazioni verrà sequenziata più di una volta. Per semplificare questa operazione, è consigliabile eseguire la sequenziazione in un computer in cui è in uso un ambiente virtuale. In questo modo potrai sequenziare un'applicazione e ripristinare uno stato pulito, con una riconfigurazione minima, nel computer che sta usando sequencer.

    Se si esegue Microsoft Hyper-V nell'ambiente, l'App-V Sequencer verrà eseguita quando il computer virtuale Hyper-V in cui è in esecuzione è:

    -   in pausa e ripresa.

    -   il relativo stato viene salvato e ripristinato.

    -   viene salvato come snapshot e viene ripristinato.

    -   migrazione a hardware diverso nell'ambito di una migrazione dinamica.

-   **Prima di sequenziare una nuova applicazione, arrestare altre applicazioni in uso.**

    I processi e le attività pianificate che in genere vengono eseguiti nel computer di sequenziazione possono rallentare il processo di sequenziazione e causare la raccolta di dati irrilevanti durante la sequenziazione. Tutte le applicazioni e i programmi non necessari devono essere arrestati prima di iniziare la sequenziazione.

-   **Sequenza in un computer che gestisce servizi Terminal**

    Non è consigliabile configurare la modalità di installazione in un computer che gestisce servizi terminal prima di installare il sequencer.

## Sequenziazione delle procedure consigliate


Durante la sequenziazione di una nuova applicazione, è necessario considerare le procedure consigliate seguenti:

-   

    **Nota**  Se si esegue App-V 4,6 SP1, non è necessario eseguire la sequenza in una directory successiva alla convenzione di denominazione di 8,3.

     

-   **Sequenza a una directory univoca che segue la convenzione di denominazione di 8,3.**

    Devi sequenziare tutte le applicazioni in una directory successiva alla convenzione di denominazione di 8,3. Il nome di directory specificato non può contenere più di otto caratteri, seguiti da un'estensione di file di tre caratteri, ad esempio **Q:\\MYAPP. ABC**.

-   **Sequenza in una cartella di destinazione nella radice dell'unità, non in una sottodirectory.**

    Se la famiglia di applicazioni ha più parti, installare ogni applicazione in una sottodirectory della directory principale. Ad esempio, se un pacchetto contiene un'applicazione insieme a un client, USA **Q:\\AppSuite** come directory principale e Sequenzia l'applicazione principale in **Q:\\AppSuite\\Main**e Sequenzia il client in **Q:\\AppSuite\\Client**.

-   **Configurare e testare l'applicazione durante la fase di installazione.**

    Il completamento dell'installazione di un'applicazione richiede spesso l'esecuzione di più passaggi manuali che non fanno parte del processo di installazione dell'applicazione. Questa procedura può coinvolgere la configurazione di una connessione a un database o la copia di file aggiornati. È consigliabile eseguire queste configurazioni durante la fase di installazione e quindi eseguire l'applicazione per verificare che funzioni.

-   **Eseguire l'applicazione, più volte se necessario, finché il programma non è stabile.**

    È consigliabile eseguire l'applicazione più volte durante l'installazione per verificare che tutte le configurazioni della registrazione e della finestra di dialogo associate siano state completate. Quando si apre l'applicazione più volte durante l'installazione, viene garantito che solo le caratteristiche dell'applicazione rilevanti vengano caricate nel **blocco di funzionalità principale**.

-   **Disabilitare tutte le funzionalità di aggiornamento automatico associate all'applicazione.**

    Alcune applicazioni hanno la possibilità di verificare automaticamente gli aggiornamenti più recenti durante l'installazione. Per facilitare il controllo delle versioni dei pacchetti di applicazioni virtuali, è consigliabile disabilitare questa funzionalità durante la sequenziazione. Se sono presenti aggiornamenti obbligatori, è necessario sequenziare un nuovo pacchetto di applicazione virtuale con gli aggiornamenti associati installati.

## Argomenti correlati


[Pianificazione della distribuzione del sistema Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 





