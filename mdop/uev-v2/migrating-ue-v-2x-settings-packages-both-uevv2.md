---
title: Migrazione dei pacchetti di impostazioni UE-V 2. x
description: Migrazione dei pacchetti di impostazioni UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825516"
---
# Migrazione dei pacchetti di impostazioni UE-V 2. x


Nel ciclo di vita di una distribuzione di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, potrebbe essere necessario rilocare i pacchetti delle impostazioni utente quando si esegue la migrazione a un nuovo server o quando si eseguono i backup. Potrebbe essere necessario eseguire la migrazione dei pacchetti di impostazioni negli scenari seguenti:

-   Aggiornamento dell'hardware del server esistente a un server più moderno.

-   Migrazione di una condivisione della posizione di archiviazione delle impostazioni da un server di prova a un server di produzione.

La semplice copia di file e cartelle non consente di mantenere le impostazioni e le autorizzazioni di sicurezza. La procedura seguente descrive come copiare correttamente il pacchetto di impostazioni insieme alle autorizzazioni di file system NTFS per una nuova condivisione.

**Per conservare i pacchetti di impostazioni di UE-V 2 quando si esegue la migrazione a un nuovo server**

1.  In una nuova posizione in un server diverso creare una nuova cartella, ad esempio impostazioni.

2.  Disabilitare la condivisione per la condivisione della cartella precedente nel server precedente.

3.  Per copiare i pacchetti di impostazioni esistenti nel nuovo server con Robocopy

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Nota**  Per monitorare lo stato di avanzamento della copia, aprire MySettings.txt con un visualizzatore log, ad esempio Trace32.

     

4.  Concedere le autorizzazioni a livello di condivisione alla nuova condivisione. Abbandonare le autorizzazioni di file system NTFS Man mano che erano impostate da Robocopy.

    Nei computer che eseguono l'agente UE-V aggiornare l'impostazione di configurazione **SettingsStoragePath** al percorso UNC (Universal Naming Convention) della nuova condivisione.

    **Hai un suggerimento per l'UE-V**? Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization). **È stato ottenuto un problema UE-V**? Utilizzare il [forum TechNet di UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Argomenti correlati


[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





