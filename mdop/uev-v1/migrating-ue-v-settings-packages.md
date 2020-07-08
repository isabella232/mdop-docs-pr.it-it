---
title: Migrazione dei pacchetti di impostazioni UE-V
description: Migrazione dei pacchetti di impostazioni UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823206"
---
# Migrazione dei pacchetti di impostazioni UE-V


Nel ciclo di vita di una distribuzione di Microsoft User Experience Virtualization (UE-V), potrebbe essere necessario rilocare i pacchetti delle impostazioni utente quando si esegue la migrazione a un nuovo server o per scopi di backup. La migrazione dei pacchetti di impostazioni potrebbe essere necessaria negli scenari seguenti:

-   Aggiornamento dell'hardware del server esistente a un server più moderno.

-   Migrazione di una condivisione della posizione di archiviazione delle impostazioni da un Lab a un server di produzione.

La semplice copia di file e cartelle non consentirà di mantenere le impostazioni e le autorizzazioni di sicurezza. La procedura descritta di seguito consente di copiare correttamente i file del pacchetto di impostazioni con le autorizzazioni NTFS per una nuova condivisione.

**Come conservare i pacchetti di impostazioni UE-V quando si esegue la migrazione a un nuovo server**

1.  In una nuova posizione in un server diverso creare una nuova cartella; ad esempio, impostazioni.

2.  Disabilitare la condivisione per la condivisione della cartella precedente nel server precedente.

3.  Trasferire i pacchetti di impostazioni esistenti nel nuovo server con Robocopy dalla riga di comando. Ad esempio:

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Nota**  Per monitorare lo stato di avanzamento della copia, aprire MySettings.txt con un lettore di file di log, ad esempio Trace32.

     

4.  Concedere le autorizzazioni a livello di condivisione alla nuova condivisione. Abbandonare le autorizzazioni NTFS Man mano che erano impostate da Robocopy.

    Nei computer che eseguono l'agente UE-V aggiornare l'impostazione di configurazione SettingsStoragePath al percorso UNC della nuova condivisione.

## Argomenti correlati


[Amministrazione di UE-V 1.0](administering-ue-v-10.md)

[Operazioni per UE-V 1.0](operations-for-ue-v-10.md)

 

 





