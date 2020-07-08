---
title: Architettura di alto livello per UE-V 1.0
description: Architettura di alto livello per UE-V 1.0
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 76703cf4c7297401e6516830bf194cef741d60ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827096"
---
# Architettura di alto livello per UE-V 1.0


Questo argomento descrive gli elementi architettonici di alto livello della soluzione di roaming delle impostazioni di Microsoft User Experience Virtualization (UE-V). Gli elementi seguenti fanno parte di una distribuzione standard di UE-V.

![diagramma di architettura dell'agente UE-v](images/ue-vagentarchitecturaldiagram.gif)

L'agente UE-V monitora le applicazioni e i processi del sistema operativo Man mano che vengono identificati nei modelli di posizione delle impostazioni di UE-V. Quando l'applicazione o il sistema operativo viene avviato, le impostazioni vengono lette dal pacchetto di impostazioni e applicate al computer. Quando l'applicazione viene chiusa o quando il sistema operativo è bloccato o arrestato, le impostazioni vengono salvate in un pacchetto di impostazioni di UE-V nella posizione di archiviazione delle impostazioni.

## Posizione di archiviazione delle impostazioni


La posizione di archiviazione delle impostazioni è una condivisione file a cui l'utente che utilizza l'agente di virtualizzazione accede alle impostazioni di lettura e scrittura. Questa posizione è la home directory di Active Directory o definita durante l'installazione di UE-V. È possibile impostare la posizione durante l'installazione dell'agente UE-V oppure impostarla in un secondo momento con criteri di gruppo, WMI o PowerShell. La posizione può essere in qualsiasi condivisione di file comune a cui gli utenti possono accedere. Se durante l'installazione non viene impostata la posizione di archiviazione dell'impostazione, la home directory in Active Directory verrà usata da UE-V. L'agente UE-V Verifica la posizione e crea una cartella di sistema nascosta dall'utente in cui archiviare e accedere alle impostazioni dell'utente. Per altre informazioni sull'archiviazione delle impostazioni, vedere [preparare l'ambiente per la versione UE-V](preparing-your-environment-for-ue-v.md).

## Agente UE-V


L'agente UE-V viene installato in ogni computer con impostazioni sincronizzate dalla virtualizzazione dell'esperienza utente. L'agente monitora le applicazioni registrate e il sistema operativo per tutte le modifiche apportate alle impostazioni e sincronizza le impostazioni tra i computer. Le impostazioni vengono applicate dalla posizione di archiviazione delle impostazioni all'applicazione quando l'applicazione viene avviata. Le impostazioni vengono quindi salvate di nuovo nel percorso di archiviazione delle impostazioni quando l'applicazione viene chiusa. Le impostazioni del sistema operativo vengono applicate quando l'utente effettua l'accesso, quando il computer viene sbloccato o quando l'utente si connette in remoto al computer usando RDP (Remote Desktop Protocol). L'agente Salva le impostazioni quando l'utente si disconnette, quando il computer è bloccato o quando una connessione remota è disconnessa. Per altre informazioni sull'agente UE-V, vedere [preparare l'ambiente per la versione UE-v](preparing-your-environment-for-ue-v.md).

## <a href="" id="bkmk-settingslocationtemplate"></a>Modelli di posizione delle impostazioni


Il modello posizione impostazioni è un file XML che definisce le posizioni delle impostazioni da monitorare tramite la virtualizzazione dell'esperienza utente. Solo i percorsi delle impostazioni definiti in questi modelli di impostazioni vengono acquisiti o applicati nei computer che eseguono l'agente UE-V. Il modello posizione impostazioni non contiene valori delle impostazioni, ma solo i percorsi in cui sono archiviati i valori nel computer.

UE-V include un set di modelli di posizione delle impostazioni che specificano le posizioni delle impostazioni per alcune applicazioni Microsoft e le impostazioni di Windows. Un amministratore può creare modelli di posizione delle impostazioni personalizzate usando il generatore UE-V.

[Pianificazione delle applicazioni da sincronizzare con UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Uso di modelli UE-V personalizzati e di Generatore UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## Pacchetti di impostazioni


Le impostazioni dell'applicazione e le impostazioni di Windows sono archiviate in pacchetti di impostazioni, creati dall'agente UE-V. Un pacchetto di impostazioni è una raccolta delle impostazioni rappresentate nei modelli di posizione delle impostazioni. Questi pacchetti di impostazioni vengono creati, archiviati localmente e quindi copiati nel percorso di archiviazione delle impostazioni. "WINS ultima scrittura" determina le impostazioni che vengono mantenute quando un singolo utente Sincronizza più computer in una posizione di archiviazione. L'agente che viene eseguito in un computer legge e scrive nella posizione delle impostazioni indipendentemente dagli agenti eseguiti in altri computer. Le impostazioni e i valori scritti più di recente vengono applicati quando l'agente successivo legge il percorso di archiviazione delle impostazioni.

![processo generatore di UE-v](images/ue-vgeneratorprocess.gif)

## Catalogo di modelli di impostazioni


Il catalogo dei modelli di impostazioni è un percorso di cartella nei computer UE-V o in una condivisione di rete SMB (Server Message Block) in cui sono archiviati tutti i modelli di posizione delle impostazioni personalizzate. L'agente UE-V recupera i modelli nuovi o aggiornati da questa posizione. L'agente UE-V controlla questa posizione una volta al giorno e aggiorna il comportamento di sincronizzazione in base ai modelli in questa cartella. I modelli aggiunti o aggiornati in questa cartella dall'ultimo controllo vengono registrati dall'agente UE-V. L'agente UE-V Annulla la registrazione dei modelli rimossi dalla cartella. I modelli sono registrati e non registrati una volta al giorno dall'utilità di pianificazione. Se si utilizzeranno solo i modelli di posizione predefiniti delle impostazioni inclusi in UE-V, il catalogo di un modello di impostazioni non è necessario. Per altre informazioni sui cataloghi di distribuzione delle impostazioni, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Generatore di virtualizzazione Experience utente


Il generatore di virtualizzazione dell'esperienza utente consente di creare modelli di posizione delle impostazioni personalizzati che memorizzano le posizioni delle impostazioni delle applicazioni usate nell'organizzazione e che si desidera includere nella soluzione per le impostazioni mobili. Il generatore UE-V cercherà di individuare le posizioni dei valori del registro di sistema e i file di impostazioni per le applicazioni e quindi registrerà tali posizioni in un file XML del modello di posizione delle impostazioni. È quindi possibile distribuire i modelli di posizione delle impostazioni nei computer degli utenti. Il generatore UE-V consente inoltre a un amministratore di modificare un modello esistente o di convalidare un modello creato con un altro editor XML.

Il generatore di UE-V monitora un'applicazione per individuare e registrare la posizione in cui archivia le impostazioni. A questo scopo, monitora il punto in cui l'applicazione legge o scrive in HKEY \ _CURRENT \ _USER registro di sistema o nelle cartelle file in **utenti** \ \ \ [nome utente \] \ \ **AppData**  \\  **roaming and Users** \ \ \ [nome utente \] \ \ **AppData**  \\  **local**.

Il processo di individuazione esclude le chiavi del registro di sistema e i file a cui l'utente connesso non riesce a scrivere valori. Nessuna di queste operazioni verrà inclusa nel file XML. Il processo di individuazione esclude anche le chiavi del registro di sistema e i file associati alle funzionalità di base di Windows.

Per altre informazioni sul generatore UE-V, vedere [installazione del generatore UE-v](installing-the-ue-v-generator.md).

## Argomenti correlati


[Microsoft User Experience Virtualization (UE-V) 1.0](index.md)

[Attività iniziali di User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Informazioni su User Experience Virtualization 1.0](about-user-experience-virtualization-10.md)

[Uso di modelli UE-V personalizzati e di Generatore UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





