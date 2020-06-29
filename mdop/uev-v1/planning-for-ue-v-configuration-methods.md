---
title: Pianificazione per i metodi di configurazione di UE-V
description: Pianificazione per i metodi di configurazione di UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827095"
---
# Pianificazione per i metodi di configurazione di UE-V


Le configurazioni Microsoft User Experience Virtualization (UE-V) determinano la sincronizzazione delle impostazioni in tutta l'organizzazione. Questo argomento descrive come vengono create le configurazioni UE-V per facilitare la formulazione di un piano di configurazione che soddisfi meglio i requisiti aziendali.

## Metodi di configurazione per UE-V


Puoi configurare la versione UE-V prima, durante o dopo l'installazione dell'agente, a seconda del metodo di configurazione che usi.

**Criteri di gruppo:** l'infrastruttura di criteri di gruppo esistente può essere usata per configurare la versione UE-v prima o dopo la distribuzione di agenti UE-v. Il modello ADMX UE-V consente la gestione centralizzata delle opzioni di configurazione dell'agente UE-V comuni e include le impostazioni per la configurazione della sincronizzazione UE-V. Gli ambienti di rete che usano criteri di gruppo possono preconfigurare UE-V in previsione della distribuzione dell'agente.

[Configurazione di UE-V con oggetti Criteri di gruppo](configuring-ue-v-with-group-policy-objects.md)

[Installazione di modelli ADMX di Criteri di gruppo di UE-V](installing-the-ue-v-group-policy-admx-templates.md)

**Installazione in una riga di comando o in batch script:** i parametri usati con la distribuzione dell'agente UE-v consentono la configurazione di molte impostazioni UE-v. I sistemi di distribuzione elettronica del software, ad esempio System Center Configuration Manager, usano questi parametri per configurare i client durante la distribuzione e l'installazione del software dell'agente UE-V. Per un elenco dei parametri di installazione e degli script di installazione di esempio, vedere [distribuzione dell'agente UE-V](deploying-the-ue-v-agent.md).

**PowerShell e WMI:** i comandi con script che usano PowerShell o WMI possono essere usati per modificare le configurazioni dopo l'installazione dell'agente UE-V. Per un elenco di comandi di PowerShell e WMI, vedere [gestione dell'agente e dei pacchetti UE-V 1,0 con PowerShell e WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

**Modificare le impostazioni del registro di sistema:** Le impostazioni di UE-V sono archiviate nel registro di sistema e possono essere modificate usando qualsiasi strumento che può modificare le impostazioni del registro di sistema, ad esempio RegEdit.

**Nota**  La modifica del registro di sistema può causare la perdita di dati o il computer diventa inattivo. Ti consigliamo di usare altri metodi di configurazione.

 

### Impostazioni di configurazione di UE-V

Di seguito sono riportati alcuni esempi di impostazioni di configurazione di UE-V:

-   **Impostazione del percorso di archiviazione:** specifica la posizione della condivisione file in cui sono archiviate le impostazioni UE-V.

-   **Percorso catalogo di modelli di impostazioni:** specifica il percorso UNC (Universal Naming Convention) che definisce la posizione selezionata per i nuovi modelli di posizione delle impostazioni.

-   **Registrare i modelli Microsoft:** specifica se i modelli Microsoft predefiniti devono essere registrati durante l'installazione.

-   **Metodo di sincronizzazione:** specifica se la caratteristica file offline di Windows viene usata per il supporto offline.

-   **Timeout sincronizzazione:** specifica il numero di millisecondi che il computer attende prima del timeout durante il recupero delle impostazioni utente dalla posizione di archiviazione delle impostazioni.

-   **Enable sincronizzazione:** specifica se la sincronizzazione delle impostazioni UE-V è abilitata o disabilitata.

-   **Dimensioni massime del pacchetto:** specifica una dimensione della soglia dei file del pacchetto di impostazioni in byte in cui l'agente UE-V segnala un avviso.

## Argomenti correlati


[Pianificazione di UE-V 1.0](planning-for-ue-v-10.md)

[Pianificazione per la configurazione di UE-V](planning-for-ue-v-configuration.md)

 

 





