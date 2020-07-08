---
title: Novità in MED-V 2.0
description: Novità in MED-V 2.0
author: dansimp
ms.assetid: 53b10bff-2b6f-463b-bdc2-5edc56526792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 78dba25fec7ae2bb41da00902b59dcd15030f2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823705"
---
# Novità in MED-V 2.0


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 ha sviluppato il supporto per la compatibilità delle applicazioni per Windows 7 e le funzionalità rimosse non necessarie per questo scenario. Ad esempio, sono state rimosse caratteristiche come la crittografia dell'area di lavoro MED-V, il server MED-V centralizzato e il trasferimento di trim dell'area di lavoro MED-V.

## Modifiche della funzionalità standard


In questa sezione vengono illustrate le aree principali in cui è cambiata la funzionalità MED-V 2,0.

### Creazione di aree di lavoro MED-V

Il disco rigido virtuale usato per l'area di lavoro MED-V è ora creato in Windows Virtual PC. I metodi usati per creare l'area di lavoro MED-V includono installare Windows XP SP3, aggiornare il sistema operativo e prepararlo per essere gestito tramite l'infrastruttura di gestione del software.

Le funzionalità di gestione offline e di trasferimento trim sono state rimosse, oltre alle funzionalità di crittografia e compressione dell'area di lavoro MED-V proprietarie. Quando si crea un'area di lavoro MED-V, un amministratore deve preparare e configurare le applicazioni e gli strumenti di gestione appropriati nell'immagine invece di usare lo strumento di preparazione della macchina virtuale fornito in MED-V 1,0.

L'uso di Sysprep nell'immagine MED-V è ora obbligatorio e convalidato durante la creazione dell'area di lavoro MED-V. Packager area di lavoro MED-V offre un'interfaccia utente grafica (GUI) che guida l'amministratore attraverso il processo di creazione di pacchetti. La console di MED-V 1,0 è stata rimossa insieme alla funzionalità di gestione delle immagini, alla gestione dei profili di area di lavoro MED-V e all'esigenza di organizzare e crittografare le aree di lavoro MED-V.

### Distribuzione di area di lavoro MED-V

Per distribuire un'area di lavoro MED-V, un amministratore è ora in grado di sfruttare gli strumenti di distribuzione del software elettronici. Il metodo client-pull disponibile in MED-V 1,0 è stato rimosso e l'area di lavoro MED-V viene ora recapitata tramite metodi esterni a MED-V. Gli amministratori possono gestire le aree di lavoro MED-V come farebbero con qualsiasi altro pacchetto di applicazioni e possono pianificare distribuzioni e installazioni di MED-V usando gli strumenti e i processi esistenti. Le installazioni di MED-V possono essere distribuite in modo invisibile all'utente e possono essere gestite facilmente in un'infrastruttura di distribuzione del software esistente.

### Gestione area di lavoro MED-V

L'area di lavoro MED-V in MED-V 2,0 si basa su un disco rigido virtuale di Windows Virtual PC. MED-V ha esteso le funzionalità fornite da Windows Virtual PC migliorandone l'esperienza senza richiedere la crittografia o strumenti speciali per accedere all'area di lavoro MED-V.

Dopo la distribuzione di MED-V in una workstation, l'area di lavoro MED-V può essere aperta in modalità schermo intero tramite Windows Virtual PC. Questa nuova funzionalità ha rimosso il requisito per i criteri che impostano una preferenza per le modalità seamless o a schermo intero e ha anche rimosso la necessità di forzare la visualizzazione a schermo intero per la diagnostica e la risoluzione dei problemi.

Le applicazioni di pubblicazione nell'area di lavoro MED-V non vengono più eseguite con i profili e immettendo manualmente il percorso delle applicazioni. Si verifica invece automaticamente quando le applicazioni sono installate nel guest. Viene rimosso il repository di immagini centrale che include versioni delle immagini recapitate tramite il trasferimento trim. Invece, MED-V consente agli amministratori di gestire l'area di lavoro MED-V come farebbero con un computer fisico, lasciando che le applicazioni e gli aggiornamenti vengano distribuiti senza la complessità di un'infrastruttura MED-V dedicata.

## Modifiche nelle caratteristiche di MED-V


Diverse aree principali di MED-V 2,0 riflettono miglioramenti o aggiunte alle caratteristiche seguenti.

### Creazione di aree di lavoro MED-V

Le aree di lavoro MED-V devono essere create usando Virtual PC Windows. È necessario eseguire la migrazione delle immagini Virtual PC 2007 esistenti. Lo strumento di preparazione della macchina virtuale non è incluso in MED-V 2,0 e gli amministratori devono configurare, aggiornare e ottimizzare le proprie immagini in base al file della Guida di MED-V 2,0. L'esecuzione di Sysprep nell'immagine MED-V è un passaggio obbligatorio e deve essere eseguita prima della creazione di pacchetti.

### Pacchetto area di lavoro MED-V

Windows PowerShell è la base del Packager area di lavoro MED-V. Questa funzionalità sostituisce alcune abilità e funzionalità precedenti della console che gestiscono le funzioni centralizzate di MED-V. Il Packager area di lavoro MED-V consente semplicemente di creare un pacchetto del disco rigido virtuale con le impostazioni e l'immagine appropriate in modo che possano essere facilmente distribuite dagli amministratori. Le funzionalità avanzate vengono fornite tramite Windows PowerShell.

### Distribuzione dell'area di lavoro MED-V

L'infrastruttura server dedicata non è più necessaria per MED-V 2,0 e il metodo pull client per la distribuzione delle aree di lavoro MED-V è stato rimosso. Le aree di lavoro MED-V vengono ora distribuite con l'infrastruttura di distribuzione del software elettronica e possono essere archiviate in condivisioni comuni usate per altri pacchetti di installazione.

### Configurazione per la prima volta

Il processo di configurazione per la prima volta è ora integrato con la convenzione di imaging standard di Sysprep. Il processo di configurazione per la prima volta dell'area di lavoro MED-V consente di applicare in modo dinamico le impostazioni specificate nel Packager area di lavoro MED-V all'immagine Man mano che inizia la configurazione minima. Lo strumento di scripting nella console è stato rimosso e il processo di configurazione per la prima volta ora si basa sulle opzioni configurate nel Packager area di lavoro MED-V dall'amministratore.

### Pubblicazione di applicazioni

Gli amministratori possono installare le applicazioni nell'immagine MED-V prima della creazione del pacchetto, dopo la distribuzione dell'area di lavoro MED-V o tramite una combinazione di entrambi. MED-V non esamina più i criteri dell'area di lavoro MED-V per pubblicare le applicazioni, ma fa riferimento a ciò che viene effettivamente installato nel guest. Mentre le applicazioni sono installate nel guest, vengono rilevate e pubblicate automaticamente nel menu **Start** dell'host e sono pronte per essere avviate dall'utente finale.

### Reindirizzamento URL

MED-V 2,0 offre un reindirizzamento degli indirizzi Web host-to-Guest in base ai criteri configurati e gestiti dall'amministratore. Dopo che un URL viene reindirizzato al browser Guest, l'esperienza predefinita consiste nel tentativo di limitare l'utente al sito reindirizzato. Questo riduce a icona le attività di esplorazione che un utente può eseguire che non sono intese dall'amministratore. Il reindirizzamento del browser Guest-to-host è stato rimosso.

### Risoluzione dei problemi

MED-V ora sfrutta i vantaggi dei processi basati su host standard per la risoluzione dei problemi. Dato che l'area di lavoro MED-V non è più crittografata, può essere aperta in modalità a schermo intero all'interno della console Virtual PC di Windows, dove può essere visualizzata e lavorata come workstation standard. Inoltre, i registri non vengono più crittografati localmente e registrati centralmente. MED-V ora fa uso estensivo dei registri eventi locali e il livello di registrazione dell'output, da informazioni a livelli di debug, può essere facilmente configurato. Infine, viene fornito un Toolkit per la risoluzione dei problemi, che consente agli amministratori e al personale dell'helpdesk di avere una visualizzazione grafica e aggregata di tutte le opzioni di risoluzione dei problemi e può selezionare senza sforzo le attività più adatte alle proprie esigenze.

MED-V non viene più eseguito come servizio di sistema. Viene invece eseguito come processi di proprietà dell'utente e viene eseguito solo quando un utente ha eseguito l'accesso.La funzionalità fornita in precedenza dal servizio di proprietà del sistema ora è disponibile nei processi lato utente.

## Argomenti correlati


[Distribuzione di MED-V](deployment-of-med-v.md)

[Operazioni per MED-V](operations-for-med-v.md)

 

 





