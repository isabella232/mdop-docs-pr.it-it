---
title: Creare modelli percorsi impostazioni UE-V con Generatore UE-V
description: Creare modelli percorsi impostazioni UE-V con Generatore UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826645"
---
# Creare modelli percorsi impostazioni UE-V con Generatore UE-V


Microsoft User Experience Virtualization (UE-V) USA i *modelli di posizione delle impostazioni* per aggirare le impostazioni delle applicazioni tra i computer degli utenti. Alcuni modelli di posizione standard delle impostazioni sono inclusi nella virtualizzazione dell'esperienza utente. È anche possibile creare, modificare o convalidare i modelli di posizione delle impostazioni personalizzate con il generatore UE-V.

Il generatore di UE-V monitora un'applicazione per individuare e acquisire le posizioni in cui vengono archiviate le impostazioni dell'applicazione. L'applicazione che viene monitorata deve essere un'applicazione tradizionale. Il generatore UE-V non può creare un modello di posizione delle impostazioni dai tipi di applicazione seguenti:

-   Applicazioni virtualizzate

-   Applicazione offerta tramite Servizi terminal

-   Applicazioni Java

-   Applicazioni di Windows 8

**Nota**  I modelli UE-V non possono essere creati da applicazioni virtualizzate o da applicazioni di Servizi terminal. Tuttavia, le impostazioni sincronizzate con i modelli possono essere applicate a tali applicazioni. Per creare modelli che supportano le applicazioni VDI (Virtual Desktop Infrastructure) e Servizi terminal, aprire una versione di Windows Installer (con estensione msi) dell'applicazione con il generatore UE-V.

 

**Percorsi esclusi**

Il processo di individuazione esclude le posizioni che in genere archiviano i file software dell'applicazione che non si spostano correttamente tra i computer degli utenti o gli ambienti. Gli elementi seguenti sono esclusi:

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file a cui l'utente connesso non può scrivere valori

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file associati alle funzionalità di base di Windows

-   Tutte le chiavi del registro di sistema situate nell'HKEY \ _LOCAL \ _MACHINE hive

-   File che si trovano nelle directory dei file di programma

-   File che si trovano in utenti \ \ \ [nome utente \] \ \ AppData \ \ LocalLow

-   File di sistema operativo Windows che si trovano in% SystemRoot%

Se le chiavi del registro di sistema e i file archiviati in questi percorsi esclusi sono necessari per il roaming delle impostazioni dell'applicazione, gli amministratori possono aggiungere manualmente le posizioni al modello di posizione delle impostazioni durante il processo di creazione del modello.

## Creare modelli UE-V


Usare il generatore UE-V per creare modelli di posizione delle impostazioni per le applicazioni line-of-business o altre applicazioni. Dopo la creazione del modello per un'applicazione, è possibile distribuire il modello ai computer in modo che gli utenti possano aggirare le impostazioni per tale applicazione.

**Per creare un modello di posizione delle impostazioni di UE-V con il generatore UE-V**

1.  Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.

2.  Fare clic su **Crea modello posizione impostazioni**.

3.  Specifica l'applicazione. Individuare il percorso del file dell'applicazione (con estensione exe) o il collegamento all'applicazione (con estensione lnk) per cui si vuole creare un modello di posizione delle impostazioni. Specificare gli argomenti della riga di comando, se presenti, e la directory di lavoro, se presenti. Fai clic su **Next** per continuare.

    **Nota**  Prima che l'applicazione venga avviata, il sistema Visualizza un prompt per il **controllo dell'account utente**. È necessaria l'autorizzazione per monitorare il registro di sistema e i percorsi dei file usati dall'applicazione per archiviare le impostazioni.

     

4.  Dopo l'avvio dell'applicazione, chiudere l'applicazione. Il generatore UE-V registra le posizioni in cui vengono archiviate le impostazioni dell'applicazione.

5.  Al termine del processo, fare clic su **Avanti** per continuare.

6.  Esaminare e selezionare le caselle di controllo accanto alle posizioni appropriate per le impostazioni del registro di sistema e alle posizioni dei file di impostazioni per spostarsi nell'applicazione. L'elenco include le due categorie seguenti per i percorsi delle impostazioni:

    -   **Standard**: impostazioni dell'applicazione archiviate nel registro di sistema in HKEY \ _CURRENT \ _USER i tasti o nelle cartelle file in \ \ **Users** \ \ \ [nome utente \] \ \ **AppData**  \\  **roaming**. Il generatore UE-V include queste impostazioni per impostazione predefinita.

    -   Non **standard**: impostazioni dell'applicazione archiviate all'esterno dei percorsi specificati nelle procedure consigliate per l'archiviazione dei dati delle impostazioni (facoltativo). Questi includono file e cartelle in **utenti** \ \ \ [nome utente \] \ \ **AppData**  \\  **local**. Esaminare queste posizioni per determinare se includerle nel modello di posizione delle impostazioni. Selezionare le caselle di controllo percorsi per includerle.

    Fai clic su **Next** per continuare.

7.  Rivedere e modificare le **Proprietà**, le posizioni **del registro di sistema** e i percorsi dei **file** per il modello di posizione delle impostazioni.

    -   Modificare le proprietà seguenti nella scheda **Proprietà** :

        -   **Nome applicazione**: il nome dell'applicazione scritto nella descrizione delle proprietà dei file di programma.

        -   **Nome programma**: nome del programma ricavato dalle proprietà del file di programma. Questo nome contiene in genere l'estensione exe.

        -   **Versione del prodotto**: il numero di versione del prodotto del file exe dell'applicazione. Questa proprietà, insieme alla versione del file, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del prodotto.

        -   **Versione file**: il numero di versione del file the.exe dell'applicazione. Questa proprietà, insieme alla versione del prodotto, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni. Questa proprietà accetta un numero di versione principale. Se questa proprietà è vuota, il modello di posizione delle impostazioni verrà applicato a tutte le versioni del programma.

        -   **Nome autore modello** (facoltativo): nome dell'autore del modello di posizione delle impostazioni.

        -   **Autore** di un modello (facoltativo): l'indirizzo di posta elettronica dell'autore del modello di posizione delle impostazioni.

    -   La scheda **Registro di sistema** elenca la **chiave** e l' **ambito** delle posizioni del registro di sistema incluse nel modello di posizione delle impostazioni. Modificare i percorsi del registro di sistema tramite il menu a discesa **attività** . Le attività includono l'aggiunta di nuove chiavi, la modifica del nome o dell'ambito delle chiavi esistenti, l'eliminazione di chiavi e l'esplorazione del registro di sistema in cui si trovano i tasti. Usare l'ambito **tutte le impostazioni** per includere tutte le impostazioni del registro di sistema sotto la chiave specificata. Usare **tutte le impostazioni e le sottochiavi** per includere tutte le impostazioni del registro di sistema sotto la chiave, le sottochiavi e le impostazioni della sottochiave specificati.

    -   Nella scheda **file** sono elencati il percorso del file e la maschera di file dei percorsi di file inclusi nel modello di posizione delle impostazioni. Modificare i percorsi dei file usando il menu a discesa **attività** . Le attività per i percorsi dei file includono l'aggiunta di nuovi file o posizioni delle cartelle, la modifica dell'ambito di file o cartelle esistenti, l'eliminazione di file o cartelle e l'apertura della posizione selezionata in Esplora risorse. Lascia vuota la maschera di file per includere tutti i file nella cartella specificata.

8.  Fare clic su **Crea** e salvare il modello posizione impostazioni nel computer.

9.  Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni. Uscire dall'applicazione Generator UE-V.

    Dopo aver creato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello. Distribuire il modello in un ambiente lab prima di inserirlo nella produzione aziendale.

## Argomenti correlati


[Uso di modelli UE-V personalizzati e di Generatore UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

 

 





