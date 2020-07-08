---
title: Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0
description: Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821195"
---
# Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0


Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate da UE-V. Puoi usare il generatore UE-V per creare modelli di posizione delle impostazioni personalizzati che consentono agli utenti di eseguire il roaming delle impostazioni di applicazioni diverse da quelle incluse nei modelli di UE-V predefiniti. Dopo aver testato il modello personalizzato per verificare che le impostazioni dell'applicazione vengano spostate correttamente in un ambiente di test, è possibile distribuire questi modelli di posizione nei computer dell'organizzazione.

È possibile distribuire i modelli di posizione delle impostazioni personalizzate con un'infrastruttura di distribuzione esistente, ad esempio ESD (Enterprise Software Distribution), con le preferenze dei criteri di gruppo o configurando un catalogo di modelli di impostazioni UE-V. I modelli distribuiti tramite ESD o criteri di gruppo devono essere registrati con WMI o PowerShell di UE-V.

## Catalogo di modelli di impostazioni


Il catalogo dei modelli di impostazioni di virtualizzazione dell'esperienza utente è un percorso di cartella nei computer UE-V o in una condivisione di rete SMB (Server Message Block) in cui sono archiviati tutti i modello di posizione delle impostazioni personalizzate. L'agente UE-V recupera i modelli nuovi o aggiornati da questa posizione. L'agente UE-V controlla la posizione una volta al giorno e aggiorna il comportamento di sincronizzazione in base ai modelli presenti nella cartella. I modelli aggiunti o aggiornati in questa cartella dall'ultima volta che la cartella è stata selezionata vengono registrati dall'agente UE-V. L'agente UE-V Annulla la registrazione dei modelli rimossi dalla cartella. Per impostazione predefinita, i modelli sono registrati e non registrati una volta al giorno alle 3:30 A.M. ora locale dall'utilità di pianificazione. Per altre informazioni sulle attività di UE-V, vedere [modifica della frequenza delle attività pianificate di UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).

È possibile configurare il percorso del catalogo dei modelli di impostazioni usando le opzioni della riga di comando installa, criteri di gruppo, WMI o PowerShell. I modelli archiviati nel percorso del catalogo dei modelli di impostazioni vengono registrati e annullati automaticamente da un'attività pianificata. È possibile personalizzare l'attività pianificata in base alle esigenze.

## Sostituire i modelli Microsoft predefiniti


L'agente UE-V installa un gruppo predefinito di modelli di posizione delle impostazioni per le comuni applicazioni Microsoft e le impostazioni di Windows. Se l'organizzazione richiede versioni personalizzate di questi modelli, l'agente UE-V può essere configurato per l'uso di un catalogo di modelli di impostazioni e quindi sostituire i modelli Microsoft predefiniti.

Durante l'installazione dell'agente UE-V, il parametro della riga di comando `RegisterMSTemplates` può essere usato per disabilitare la registrazione dei modelli Microsoft predefiniti. Per altre informazioni su come impostare i parametri UE-V, vedere [pianificazione dei metodi di configurazione di UE-v](planning-for-ue-v-configuration-methods.md).

Quando si usano criteri di gruppo per configurare il percorso del catalogo dei modelli di impostazioni, è possibile scegliere di sostituire i modelli Microsoft predefiniti. Se si configurano le impostazioni dei criteri per sostituire i modelli Microsoft predefiniti, tutti i modelli Microsoft predefiniti installati dall'agente UE-V verranno eliminati dal computer e verranno usati solo i modelli presenti nel catalogo dei modelli di impostazioni. L'impostazione di configurazione dell'agente UE-V `RegisterMSTemplates` deve essere impostata su true per eseguire l'override del modello Microsoft predefinito.

**Nota**  Se si disattiva l'impostazione di questo criterio dopo che è stata abilitata, l'agente UE-V non ripristinerà i modelli Microsoft predefiniti.

 

Se sono presenti modelli personalizzati nel catalogo di modelli di impostazioni che usano lo stesso ID dei modelli Microsoft predefiniti e l'agente UE-V non è configurato per sostituire i modelli Microsoft predefiniti, i modelli Microsoft nel catalogo verranno ignorati.

È anche possibile sostituire i modelli predefiniti usando le caratteristiche di PowerShell di UE-V. Per sostituire il modello Microsoft predefinito con PowerShell, annullare la registrazione di tutti i modelli Microsoft predefiniti e quindi registrare i modelli personalizzati.

**Nota**  I pacchetti di impostazioni precedenti rimangono nella posizione di archiviazione delle impostazioni anche se vengono distribuiti nuovi modelli di impostazioni per un'applicazione. Questi pacchetti non vengono letti dall'agente, ma non vengono eliminati automaticamente.

 

## Argomenti correlati


[Pianificazione di UE-V 1.0](planning-for-ue-v-10.md)

[Pianificazione delle applicazioni da sincronizzare con UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Pianificazione per i metodi di configurazione di UE-V](planning-for-ue-v-configuration-methods.md)

Pianificazione della distribuzione di modelli personalizzati
 

 





