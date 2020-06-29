---
title: Configurazione delle impostazioni avanzate con Windows PowerShell
description: Configurazione delle impostazioni avanzate con Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827395"
---
# Configurazione delle impostazioni avanzate con Windows PowerShell


Il pacchetto dell'area di lavoro MED-V creato include un file di script di Windows PowerShell (con estensione ps1) che è possibile modificare prima di testare e distribuire il pacchetto dell'area di lavoro MED-V. Questa sezione fornisce informazioni e indicazioni utili per gestire le impostazioni di configurazione di MED-V tramite Windows PowerShell prima di distribuire le aree di lavoro MED-V.

## Usare i cmdlet di Windows PowerShell in MED-V


I cmdlet di Windows PowerShell seguenti sono disponibili in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:

**New-MedvConfiguration**

**Export-MedvConfiguration**

**New-MedvWorkspace**

**Export-MedvWorkspace**

Per accedere ai cmdlet di Windows PowerShell per MED-V, aprire Windows PowerShell e digitare il comando seguente per importare i moduli MED-V.

``` syntax
Import-Module microsoft.medv
```

Dopo aver importato i moduli, è possibile accedere alla Guida in linea per i cmdlet usando i comandi della Guida di Windows PowerShell standard, **Man** o **Get-Help**. Ad esempio, per accedere a una descrizione del cmdlet **New-MedvConfiguration** , incluso un elenco completo dei parametri disponibili, digitare il comando seguente.

``` syntax
get-help New-MedvConfiguration
```

È anche possibile visualizzare la guida per parametri specifici. Ad esempio, per visualizzare la guida per il parametro VmMemory, digitare quanto segue:

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

Per visualizzare un elenco di tutte le impostazioni di configurazione di MED-V e i relativi valori predefiniti, digitare il comando seguente.

``` syntax
New-MedvConfiguration -ForceDefaults
```

Per visualizzare un elenco di tutte le impostazioni di configurazione di MED-V e i relativi valori correnti, digitare il comando seguente.

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## Creazione di un'area di lavoro MED-V con impostazioni personalizzate


Dopo aver creato un pacchetto di area di lavoro MED-V usando il Packager area di lavoro MED-V, viene generato uno script di Windows PowerShell nella cartella specificata per il salvataggio dei file di Packager. Il contenuto di questo script Mostra alcune delle impostazioni di configurazione di MED-V disponibili che è possibile modificare.

Seguendo questa procedura, è possibile personalizzare lo script e quindi eseguirlo in Windows PowerShell per creare un'area di lavoro MED-V con le nuove impostazioni.

**Importante**  Eseguire Windows PowerShell con le credenziali amministrative e verificare che i criteri di esecuzione di Windows PowerShell consentano l'esecuzione di script.

1.  Modificare lo script di Windows PowerShell generato dal Packager area di lavoro MED-V oppure creare un nuovo script con le impostazioni di configurazione desiderate.

2.  Eseguire Windows PowerShell con le credenziali amministrative e al prompt dei comandi digitare il comando seguente.

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    Questo comando esegue lo script di Windows PowerShell e esegue il cmdlet **New-MedvWorkspace** per generare un nuovo pacchetto dell'area di lavoro MED-V. I nuovi file di Packager vengono salvati nella cartella specificata in origine per l'archiviazione dei file di Packager dell'area di lavoro MED-V. Per altre informazioni su questo cmdlet, vedere la Guida di Windows PowerShell.

 

## Esportazione di una configurazione MED-V in un file del registro di sistema


È possibile aggiornare le impostazioni di configurazione di MED-V dopo l'installazione dell'area di lavoro MED-V. Utilizzare il cmdlet **New-MedvConfiguration** per specificare i parametri che si desidera modificare. Ad esempio, per creare un file del registro di sistema che modifichi l'impostazione della memoria della macchina virtuale, digitare i comandi seguenti.

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

Per applicare le nuove impostazioni di configurazione, è possibile importare il file del registro di sistema risultante dal computer host a un'area di lavoro MED-V.

## Argomenti correlati


[Gestione delle impostazioni di configurazione dell'area di lavoro MED-V](managing-med-v-workspace-configuration-settings.md)

[Testare e distribuire il pacchetto nell'area di lavoro MED-V](test-and-deploy-the-med-v-workspace-package.md)

 

 





