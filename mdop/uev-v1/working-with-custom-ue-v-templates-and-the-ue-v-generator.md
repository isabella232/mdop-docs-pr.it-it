---
title: Uso di modelli UE-V personalizzati e di Generatore UE-V
description: Uso di modelli UE-V personalizzati e di Generatore UE-V
author: dansimp
ms.assetid: 7bb2583a-b032-4800-9bf9-eb33528e1d0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: db5387254842bfdcf3898089bc12a8e929e3813a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823976"
---
# Uso di modelli UE-V personalizzati e di Generatore UE-V


Per aggirare le applicazioni tra i computer degli utenti, Microsoft User Experience Virtualization (UE-V) USA i *modelli di posizione delle impostazioni*. Alcuni modelli di posizione delle impostazioni sono inclusi nella virtualizzazione dell'esperienza utente. È anche possibile creare, modificare o convalidare i modelli di posizione delle impostazioni personalizzate con il generatore UE-V.

Il generatore di UE-V monitora un'applicazione per individuare e acquisire le posizioni in cui vengono archiviate le impostazioni dell'applicazione. L'applicazione monitorata deve essere un'applicazione tradizionale. Il generatore UE-V non può creare un modello di posizione delle impostazioni per i tipi di applicazione seguenti:

-   Applicazioni virtualizzate

-   Applicazione offerta tramite Servizi terminal

-   Applicazioni Java

-   Applicazioni di Windows 8

## Creare modelli percorsi impostazioni UE-V con Generatore UE-V


Come usare il generatore UE-V per creare modelli di posizione delle impostazioni.

[Creare modelli percorsi impostazioni UE-V con Generatore UE-V](create-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V


Come usare il generatore UE-V per modificare i modelli di posizione delle impostazioni.

[Modificare i modelli percorsi impostazioni UE-V con Generatore UE-V](edit-ue-v-settings-location-templates-with-the-ue-v-generator.md)

## Convalidare i modelli percorsi impostazioni UE-V con Generatore UE-V


Come usare il generatore UE-V per convalidare i modelli di posizione delle impostazioni modificati all'esterno del generatore UE-V.

[Convalidare i modelli percorsi impostazioni UE-V con Generatore UE-V](validate-ue-v-settings-location-templates-with-ue-v-generator.md)

## <a href="" id="bkmk-standardnonstandardsettingslocations"></a>Posizioni delle impostazioni standard e non standard


Il generatore UE-V consente di identificare dove le applicazioni cercano i file di impostazioni e le impostazioni del registro di sistema usate dalle applicazioni per archiviare le informazioni sulle impostazioni. Puoi usare il generatore UE-V per aprire l'applicazione nell'ambito del processo di individuazione per acquisire le impostazioni in posizioni standard. Le posizioni standard includono le seguenti:

-   **Impostazioni del registro** di sistema-posizioni del registro di sistema in **HKEY \ _CURRENT \ _USER**

-   **File di impostazioni applicazione** : file archiviati in \ \ **Users** \ \ \ [nome utente \] \ \ **AppData**  \\  **roaming**

Il generatore UE-V esclude le posizioni che in genere archiviano i file del software dell'applicazione e non si spostano correttamente tra i computer degli utenti o gli ambienti. Il generatore UE-V esclude queste posizioni. I percorsi esclusi sono i seguenti:

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file a cui l'utente connesso non può scrivere valori

-   HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file associati alle funzionalità di base di Windows

-   Tutte le chiavi del registro di sistema che si trovano nell'HKEY \ _LOCAL \ _MACHINE hive (richiede diritti di amministratore e potrebbero richiedere l'impostazione del controllo dell'account utente)

-   File che si trovano nelle directory dei file di programma (richiede i diritti di amministratore e potrebbero richiedere l'impostazione del controllo dell'account utente)

-   File che si trovano in utenti \ \ \ [nome utente \] \ \ AppData \ \ LocalLow

-   I file di sistema operativo Windows che si trovano in% SystemRoot% (richiede diritti di amministratore e potrebbero richiedere l'impostazione del controllo dell'account utente)

Se le chiavi del registro di sistema e i file archiviati in queste posizioni sono necessari per il roaming delle impostazioni dell'applicazione, è possibile aggiungere manualmente i percorsi esclusi al modello di posizione delle impostazioni durante il processo di creazione del modello.

## Altre risorse per questo prodotto


[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

[Amministrazione di UE-V 1.0](administering-ue-v-10.md)

 

 





