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
ms.openlocfilehash: b54a9a207f9b74ad3d028cf4ab1f9842d59b0b3a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910451"
---
# <a name="high-level-architecture-for-ue-v-10"></a>Architettura di alto livello per UE-V 1.0


In questo argomento vengono descritti gli elementi architettonici di alto livello della soluzione Microsoft User Experience Virtualization (UE-V) di roaming. Gli elementi seguenti fanno parte di una distribuzione UE-V standard.

![Diagramma dell'architettura dell'agente ue-v.](images/ue-vagentarchitecturaldiagram.gif)

L UE-V agent monitora le applicazioni e i processi del sistema operativo così come vengono identificati nei modelli di percorso delle UE-V impostazioni. All'avvio dell'applicazione o del sistema operativo, le impostazioni vengono lette dal pacchetto di impostazioni e applicate al computer. Quando l'applicazione viene chiusa o quando il sistema operativo viene bloccato o arrestato, le impostazioni vengono salvate in un pacchetto UE-V impostazioni nel percorso di archiviazione delle impostazioni.

## <a name="settings-storage-location"></a>Impostazioni di archiviazione


Il percorso di archiviazione delle impostazioni è una condivisione file a cui l'agente User Experience Virtualization accede per accedere alle impostazioni di lettura e scrittura. Questo percorso è la home directory di Active Directory o definito durante l UE-V installazione. È possibile impostare il percorso durante l'installazione dell'agente UE-V oppure è possibile impostarlo in un secondo momento con Criteri di gruppo, WMI o PowerShell. Il percorso può essere in qualsiasi condivisione file comune a cui gli utenti possono accedere. Se durante l'installazione non viene impostato alcun percorso di archiviazione UE-V verrà utilizzata la home directory in Active Directory. L'UE-V verifica il percorso e crea una cartella di sistema nascosta all'utente in cui archiviare e accedere alle impostazioni utente. Per ulteriori informazioni sull'archiviazione delle impostazioni, vedere [Preparing Your Environment for UE-V](preparing-your-environment-for-ue-v.md).

## <a name="ue-v-agent"></a>UE-V Agente


L UE-V agent viene installato in ogni computer con impostazioni sincronizzate da User Experience Virtualization. L'agente monitora le applicazioni registrate e il sistema operativo per tutte le modifiche apportate alle impostazioni e sincronizza tali impostazioni tra computer. Impostazioni vengono applicati dal percorso di archiviazione delle impostazioni all'applicazione all'avvio dell'applicazione. Le impostazioni vengono quindi salvate di nuovo nel percorso di archiviazione delle impostazioni alla chiusura dell'applicazione. Le impostazioni del sistema operativo vengono applicate quando l'utente esegue l'accesso, quando il computer viene sbloccato o quando l'utente si connette in remoto al computer utilizzando RDP (Remote Desktop Protocol). L'agente salva le impostazioni quando l'utente si disconnette, quando il computer è bloccato o quando una connessione remota viene disconnessa. Per ulteriori informazioni sull'agente UE-V, vedere [Preparing Your Environment for UE-V](preparing-your-environment-for-ue-v.md).

## <a name="settings-location-templates"></a><a href="" id="bkmk-settingslocationtemplate"></a>Impostazioni di percorso


Il modello di percorso delle impostazioni è un file XML che definisce i percorsi delle impostazioni da monitorare da User Experience Virtualization. Solo i percorsi delle impostazioni definiti in questi modelli di impostazioni vengono acquisiti o applicati nei computer che eseguono UE-V Agent. Il modello di percorso delle impostazioni non contiene valori di impostazioni, ma solo le posizioni in cui i valori sono archiviati nel computer.

UE-V include un set di modelli di percorso delle impostazioni che specificano i percorsi delle impostazioni per alcune applicazioni Microsoft e Windows impostazioni. Un amministratore può creare modelli di percorso delle impostazioni personalizzate utilizzando il generatore UE-V personalizzato.

[Pianificazione delle applicazioni da sincronizzare con UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Uso di modelli UE-V personalizzati e di Generatore UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## <a name="settings-packages"></a>Impostazioni pacchetti


Le impostazioni delle applicazioni Windows vengono archiviate in pacchetti di impostazioni creati dall'UE-V Agent. Un pacchetto di impostazioni è una raccolta di impostazioni rappresentate nei modelli di percorso delle impostazioni. Questi pacchetti di impostazioni vengono creati, archiviati localmente e quindi copiati nel percorso di archiviazione delle impostazioni. "Last write wins" determina quali impostazioni vengono mantenute quando un singolo utente sincronizza più computer in un percorso di archiviazione. L'agente eseguito in un computer legge e scrive nel percorso delle impostazioni indipendentemente dagli agenti eseguiti in altri computer. Le impostazioni e i valori scritti più di recente vengono applicati quando l'agente successivo legge dal percorso di archiviazione delle impostazioni.

![processo generatore ue-v.](images/ue-vgeneratorprocess.gif)

## <a name="settings-template-catalog"></a>Impostazioni modelli


Il catalogo dei modelli di impostazioni è un percorso di cartella UE-V computer o una condivisione di rete SMB (Server Message Block) in cui sono archiviati tutti i modelli di percorso delle impostazioni personalizzate. L UE-V agente recupera modelli nuovi o aggiornati da questa posizione. L UE-V controlla questa posizione una volta al giorno e ne aggiorna il comportamento di sincronizzazione in base ai modelli in questa cartella. I modelli aggiunti o aggiornati in questa cartella dopo l'ultimo controllo vengono registrati dall UE-V agent. L UE-V agente annulla la registrazione dei modelli rimossi da questa cartella. I modelli vengono registrati e annullati una volta al giorno dall'utilità di pianificazione. Se si utilizzeranno solo i modelli di percorso delle impostazioni predefinite inclusi in UE-V, un catalogo di modelli di impostazioni non è necessario. Per ulteriori informazioni sulle impostazioni dei cataloghi di distribuzione, vedere [Planning for Custom Template Deployment for UE-V 1.0.](planning-for-custom-template-deployment-for-ue-v-10.md)

## <a name="user-experience-virtualization-generator"></a>Generatore di virtualizzazione dell'esperienza utente


Il generatore di virtualizzazione dell'esperienza utente consente di creare modelli di percorso delle impostazioni personalizzate in cui verranno archiviati i percorsi delle impostazioni delle applicazioni utilizzate nell'organizzazione e che si desidera includere nella soluzione delle impostazioni di roaming. Il generatore UE-V cercherà di individuare i percorsi dei valori del Registro di sistema e i file di impostazioni per le applicazioni e quindi registrerà tali percorsi in un file XML del modello di percorso delle impostazioni. È quindi possibile distribuire questi modelli di percorso delle impostazioni ai computer degli utenti. Il generatore UE-V consente inoltre a un amministratore di modificare un modello esistente o convalidare un modello creato con un altro editor XML.

Il UE-V esegue il monitoraggio di un'applicazione per individuare e registrare la posizione in cui vengono archiviate le relative impostazioni. A tale scopo, monitora la posizione in cui l'applicazione legge o scrive nel Registro di sistema HKEY\_CURRENT\_USER o nelle cartelle dei file in **Utenti** \\ \[Nome utente\] \\ **AppData**  \\  **Roaming e Utenti** \\ \[Nome utente\] \\ **AppData**  \\  **Local**.

Il processo di individuazione esclude le chiavi del Registro di sistema e i file in cui l'utente connesso non può scrivere valori. Nessuno di questi elementi verrà incluso nel file XML. Il processo di individuazione esclude inoltre le chiavi del Registro di sistema e i file associati alla funzionalità di base del Windows sistema operativo.

Per ulteriori informazioni sul generatore UE-V, vedere [Installing the UE-V Generator](installing-the-ue-v-generator.md).

## <a name="related-topics"></a>Argomenti correlati


[Microsoft User Experience Virtualization (UE-V) 1.0](index.md)

[Attività iniziali di User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[Informazioni su User Experience Virtualization 1.0](about-user-experience-virtualization-10.md)

[Uso di modelli UE-V personalizzati e di Generatore UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





