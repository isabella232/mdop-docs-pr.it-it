---
title: Classe WMI dell'applicazione App-V
description: Classe WMI dell'applicazione App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822325"
---
# Classe WMI dell'applicazione App-V


Nel client Application Virtualization (App-V) la classe **Application** è una classe WMI (Windows Management Instrumentation) che rappresenta tutte le applicazioni virtuali nel client.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format). Il codice include tutte le proprietà ereditate.

## Sintassi


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## Requisiti


## Proprietà


<a href="" id="name"></a>**Nome**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: chiave

Nome visualizzato dell'applicazione virtuale.

<a href="" id="version"></a>**Versione**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: chiave

Versione dell'applicazione virtuale.

<a href="" id="packageguid"></a>**PackageGUID**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: nessuno

GUID del pacchetto a cui è associata l'applicazione virtuale.

<a href="" id="lastlaunchonsystem"></a>**LastLaunchOnSystem**  
Tipo di dati: **DateTime**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Ultima data e ora in cui è stata avviata l'applicazione virtuale.

<a href="" id="globalrunningcount"></a>**GlobalRunningCount**  
Tipo di dati: **UInt32**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Conteggio delle istanze in uso dell'applicazione virtuale avviate direttamente.

<a href="" id="loading"></a>**Caricamento in corso**  
Tipo di dati: **Boolean**

Tipo di accesso: sola lettura

Qualificatori: nessuno

**true** se l'applicazione virtuale viene avviata; in caso contrario, **false**.

<a href="" id="originalosdpath"></a>**OriginalOsdPath**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Percorso del file originale del file OSD registrato con il client App-V.

<a href="" id="cachedosdpath"></a>**CachedOsdPath**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Il percorso del file OSD se il client App-V ha memorizzato la cache del file OSD localmente.

 

 





