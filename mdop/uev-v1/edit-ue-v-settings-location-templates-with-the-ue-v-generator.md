---
title: Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V
description: Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827115"
---
# Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V


Usare il generatore Microsoft User Experience Virtualization (UE-V) per modificare i modelli di posizione delle impostazioni. Quando le impostazioni modificate vengono aggiunte ai modelli tramite il generatore UE-V, le informazioni sulla versione all'interno del modello vengono aggiornate automaticamente per verificare che i modelli esistenti distribuiti nell'organizzazione vengano aggiornati correttamente.

**Come modificare un modello di posizione delle impostazioni di UE-V con il generatore UE-V**

1.  Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.

2.  Fare clic su **modifica modello posizione impostazioni**.

3.  Nell'elenco dei modelli usati di recente selezionare il modello da modificare. In alternativa, **passare** al file del modello di impostazioni. Fai clic su **Next** per continuare.

4.  Esaminare le **Proprietà**, le posizioni **del registro di sistema** e i percorsi dei **file** per il modello di impostazioni. Modifica in base alle esigenze.

    -   La scheda **Proprietà** consente di visualizzare e modificare le proprietà seguenti:

        -   **Nome applicazione**: il nome dell'applicazione scritto nella descrizione delle proprietà del file di programma.

        -   **Nome programma**: nome del programma ricavato dalle proprietà del file di programma. Questo nome contiene in genere l'estensione exe.

        -   **Versione del prodotto**: il numero di versione del prodotto del file exe dell'applicazione. Questa proprietà, insieme alla **versione del file**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del prodotto.

        -   **Versione file**: il numero di versione del file the.exe dell'applicazione. Questa proprietà, insieme alla **versione del prodotto**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del programma.

        -   **Nome autore modello** (facoltativo): nome dell'autore del modello di impostazioni.

        -   **Autore** di un modello (facoltativo): l'indirizzo di posta elettronica dell'autore del modello di posizione delle impostazioni.

    -   La scheda **Registro di sistema** elenca la **chiave** e l' **ambito** delle posizioni del registro di sistema incluse nel modello di posizione delle impostazioni. Per modificare i percorsi del registro di sistema, è possibile usare il menu a discesa **attività** . Le attività includono l'aggiunta di nuove chiavi, la modifica del nome o dell'ambito delle chiavi esistenti, l'eliminazione di chiavi e l'esplorazione del registro di sistema in cui si trovano le chiavi. Quando si definisce l'ambito per il registro di sistema, è possibile usare l'ambito **tutte le impostazioni** per includere tutte le impostazioni del registro di sistema sotto la chiave specificata. Usare **tutte le impostazioni** e le **sottochiavi** per includere tutte le impostazioni del registro di sistema sotto la chiave, le sottochiavi e le impostazioni della sottochiave specificati.

    -   Nella scheda **file** sono elencati il percorso del file e la maschera di file dei percorsi di file inclusi nel modello di posizione delle impostazioni. Per modificare i percorsi dei file, è possibile usare il menu a discesa **attività** . Le attività per i percorsi dei file includono l'aggiunta di nuovi file o posizioni delle cartelle, la modifica dell'ambito di file o cartelle esistenti, l'eliminazione di file o cartelle e l'apertura della posizione selezionata in Esplora risorse. Per includere tutti i file nella cartella specificata, lascia vuota la maschera di file.

5.  Fare clic su **Salva** per salvare le modifiche apportate al modello posizione impostazioni.

6.  Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni. Uscire dall'applicazione Generator UE-V.

    Dopo aver modificato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello. Distribuire il modello di posizione delle impostazioni modificate in un ambiente lab prima di inserirlo nella produzione aziendale.

**Come modificare manualmente un modello di posizione delle impostazioni**

1.  Creare una copia locale del modello di posizione delle impostazioni (file con estensione XML). I modelli di posizione delle impostazioni di UE-V sono file XML che identificano le posizioni in cui i valori delle impostazioni dell'archivio applicazioni.

2.  Aprire il file del modello di posizione delle impostazioni con un editor XML.

3.  Modificare il file del modello di posizione delle impostazioni. Tutte le modifiche devono essere conformi al file di schema UE-V definito in SettingsLocationTempate. xsd. Per impostazione predefinita, viene individuata una copia del file XSD. `\ProgramData\Microsoft\UEV\Templates`

4.  Salvare il file del modello di posizione delle impostazioni e chiudere l'editor XML.

5.  Convalidare il file del modello della posizione delle impostazioni modificate con il generatore UE-V. Per altre informazioni sulla convalida con il generatore UE-V, vedere [convalidare i modelli di posizione delle impostazioni di UE-v con generatore di UE-v](validate-ue-v-settings-location-templates-with-ue-v-generator.md).

## Argomenti correlati


[Uso di modelli UE-V personalizzati e di Generatore UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

 

 





