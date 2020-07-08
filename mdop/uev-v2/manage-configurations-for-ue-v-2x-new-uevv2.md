---
title: Gestire le configurazioni per UE-V 2.x
description: Gestire le configurazioni per UE-V 2.x
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827385"
---
# Gestire le configurazioni per UE-V 2.x


Nel ciclo di vita di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1 è necessario gestire la configurazione dell'agente UE-V e gestire anche le posizioni di archiviazione per le risorse, ad esempio i file di pacchetto delle impostazioni. Potrebbe essere necessario eseguire altre attività, ad esempio configurare il centro impostazioni società per definire il modo in cui gli utenti interagiscono con UE-V. Gli argomenti seguenti includono indicazioni per la gestione delle risorse UE-V.

## Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo


È possibile usare gli oggetti Criteri di gruppo per modificare le impostazioni che definiscono la modalità di sincronizzazione delle impostazioni di UE-V nei computer.

[Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## Configurazione di UE-V 2. x con System Center Configuration Manager 2012


Puoi usare SystemCenter2012 ConfigurationManager per gestire l'agente UE-V usando il pacchetto di configurazione UE-V 2.

[Configurazione di UE-V 2. x con System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## Amministrazione di UE-V 2. x con PowerShell e WMI


UE-V include i cmdlet di Windows PowerShell, che consentono agli amministratori di eseguire varie attività UE-V.

[Amministrazione di UE-V 2. x con Windows PowerShell e WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## Configurazione del centro impostazioni società per UE-V 2. x


Puoi configurare il centro impostazioni società installato usando l'agente UE-V per definire il modo in cui gli utenti interagiscono con UE-V.

[Configurazione del centro impostazioni società per UE-V 2. x](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## Esempi di impostazioni di configurazione per UE-V 2. x


Ecco alcuni esempi di impostazioni di configurazione di UE-V:

-   **Percorso di archiviazione delle impostazioni:** Specifica la posizione della condivisione file in cui sono archiviate le impostazioni UE-V.

-   **Percorso catalogo di modelli di impostazioni:** Specifica il percorso UNC (Universal Naming Convention) che definisce la posizione selezionata per i nuovi modelli di posizione delle impostazioni.

-   **Registrare i modelli Microsoft:** Specifica se i modelli Microsoft predefiniti devono essere registrati durante l'installazione.

-   **Metodo di sincronizzazione:** Specifica se UE-V usa il provider di sincronizzazione o "None". "SyncProvider" supporta i computer disconnessi dalla rete. "None" si applica quando il computer è sempre connesso alla rete. Per altre informazioni sul metodo di sincronizzazione, vedere [metodi di sincronizzazione per UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

-   **Timeout sincronizzazione:** Specifica il numero di millisecondi che il computer attende prima del timeout quando recupera le impostazioni utente dalla posizione di archiviazione delle impostazioni.

-   **Abilitare la sincronizzazione:** Specifica se la sincronizzazione delle impostazioni UE-V è abilitata o disabilitata.

-   **Dimensioni massime del pacchetto:** Specifica una dimensione della soglia dei file del pacchetto di impostazioni in byte in cui l'agente UE-V segnala un avviso.

-   **Non sincronizzare le impostazioni delle app di Windows:** Specifica che UE-V non deve sincronizzare le app di Windows.

-   **Abilitare/disabilitare la notifica First Use:** Specifica se UE-V Visualizza una finestra di dialogo la prima volta che l'agente UE-V viene eseguito nel computer di un utente.

-   **Icona Abilita/Disabilita vassoio:** Specifica se UE-V Visualizza un'icona nell'area di notifica e tutte le notifiche associate. L'icona fornisce un collegamento al centro impostazioni società.

-   **Collegamento ipertestuale contatto personalizzato:** Definisce il percorso, il testo e la descrizione del collegamento ipertestuale **contatto** nel centro impostazioni società.






## Argomenti correlati


[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Distribuire le funzionalità necessarie per UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[Distribuire UE-V 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





