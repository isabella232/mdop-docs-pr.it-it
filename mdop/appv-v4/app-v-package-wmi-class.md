---
title: Classe WMI del pacchetto App-V
description: Classe WMI del pacchetto App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819796"
---
# Classe WMI del pacchetto App-V


Nel client Application Virtualization (App-V) la classe **Package** è una classe WMI (Windows Management Instrumentation) che rappresenta tutti i pacchetti virtuali nel client. I pacchetti virtuali possono contenere molte applicazioni virtuali.

## Sintassi


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## Proprietà


<a href="" id="name"></a>**Nome**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Nome descrittivo del pacchetto virtuale.

<a href="" id="version"></a>**Versione**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Versione del pacchetto virtuale.

<a href="" id="packageguid"></a>**PackageGUID**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: chiave

Identificatore GUID della configurazione del pacchetto e dei file di origine.

<a href="" id="sftpath"></a>**SftPath**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Percorso del file SFT.

<a href="" id="totalsize"></a>**TotalSize**  
Tipo di dati: **UInt64**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Dimensione totale del pacchetto virtuale, espressa in kilobyte.

<a href="" id="cachedsize"></a>**CachedSize**  
Tipo di dati: **UInt64**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Dimensione totale della cache per il pacchetto virtuale, espressa in kilobyte.

<a href="" id="launchsize"></a>**LaunchSize**  
Tipo di dati: **UInt64**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Dimensione totale del blocco di funzionalità principale del pacchetto virtuale, espressa in kilobyte.

<a href="" id="cachedlaunchsize"></a>**CachedLaunchSize**  
Tipo di dati: **UInt64**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Dimensione totale del blocco di funzionalità principale del pacchetto virtuale memorizzato nella cache, in kilobyte.

<a href="" id="inuse"></a>**InUse**  
Tipo di dati: **Boolean**

Tipo di accesso: sola lettura

Qualificatori: nessuno

**true** se è in corso un'applicazione virtuale nel pacchetto virtuale; in caso contrario, **false**.

<a href="" id="locked"></a>**Bloccato**  
Tipo di dati: **Boolean**

Tipo di accesso: sola lettura

Qualificatori: nessuno

**true** se il pacchetto virtuale è bloccato; in caso contrario, **false**.

<a href="" id="cachedpercentage"></a>**CachedPercentage**  
Tipo di dati: **UInt16**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Percentuale dei file di cache. In base alla formula seguente: CachedSize/TotalSize × 100.

<a href="" id="versionguid"></a>**VersionGUID**  
Tipo di dati: **stringa**

Tipo di accesso: sola lettura

Qualificatori: nessuno

Identificatore GUID della versione del pacchetto.

 

 





