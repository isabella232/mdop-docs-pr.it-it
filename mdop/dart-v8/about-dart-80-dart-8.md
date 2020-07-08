---
title: Informazioni su DaRT 8.0
description: Informazioni su DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821285"
---
# Informazioni su DaRT 8.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 consente di risolvere i problemi e ripristinare i computer basati su Windows. Sono inclusi i computer che non possono essere avviati. DaRT 8,0 è un potente set di strumenti che estendono l'ambiente di ripristino di Windows (WinRE). Usando DaRT, puoi analizzare un problema per determinare la causa, ad esempio controllando il log eventi o il registro di sistema del computer. DaRT supporta il ripristino di dischi rigidi di base che contengono partizioni, ad esempio partizioni primarie e unità logiche, e supporta il ripristino dei volumi.

**Nota**  Dardo non supporta il ripristino dei dischi dinamici.

 

DaRT offre anche strumenti che ti aiutano a risolvere un problema non appena ne determini la causa. Ad esempio, puoi usare gli strumenti di DaRT per disabilitare un driver di dispositivo difettoso, rimuovere gli hotfix, ripristinare i file eliminati e analizzare il computer per il malware anche quando non puoi o non devi avviare il sistema operativo Windows installato.

Il dardo consente di recuperare rapidamente i computer in cui è in esecuzione una versione a 32 bit o a 64 bit di Windows 8, in genere in meno tempo rispetto alla riimmagine del computer.

La funzionalità in DaRT consente di creare un'immagine di ripristino. L'immagine di ripristino avvia Windows Recovery Environment (Windows RE), da cui è possibile avviare la finestra del **set di strumenti di diagnostica e ripristino** e accedere agli strumenti DaRT.

Usare la **creazione guidata immagine di ripristino di freccette** per creare l'immagine di ripristino DaRT. Per impostazione predefinita, la procedura guidata crea un file di immagine ISO (International Organization for Standardizzation) e un file WIM (Windows Imaging Format) e consente di masterizzare l'immagine in un CD, un DVD o un dispositivo USB. È possibile distribuire l'immagine localmente nei computer dell'utente finale oppure distribuirla da una partizione di rete remota o da una partizione di ripristino nel disco rigido locale.

## <a href="" id="what-s-new-in-dart-8-0"></a>Novità di DaRT 8,0


DaRT 8,0 consente di recuperare rapidamente i computer in cui è in esecuzione una versione a 32 bit o a 64 bit di Windows 8, in genere in meno tempo rispetto alla riimmagine del computer. Le nuove funzionalità di DaRT 8,0 sono le seguenti.

### Creare immagini DaRT usando Windows 8 o Windows Server 2012

DaRT 8,0 consente di creare immagini dardo usando Windows® 8 o Windows Server® 2012. Per le versioni di Windows precedenti a Windows 8 e Windows Server 2012, i clienti dovrebbero continuare a usare le versioni precedenti di DaRT.

### Generare immagini di bit di 32 e 64 da un computer

DaRT 8,0 consente di generare immagini sia a 32 che a 64 bit da un singolo computer in cui è in corso il comando DaRT, indipendentemente dal fatto che il computer sia un computer a 32 bit o a 64 bit. In DaRT7 l'immagine che è stata creata deve essere la stessa, un po' saggia, come il computer in cui è stato eseguito il dardo.

### Creare un'immagine che supporti i computer con un'interfaccia BIOS o UEFI

Il supporto di DaRT 8.0 sia per l'interfaccia UEFI (Unified Extensible Firmware Interface) che per le interfacce BIOS consente di creare una sola immagine che funziona con i computer che hanno un'interfaccia qualsiasi.

### Usare una tabella di partizione GUID (GPT) per il partizionamento

Gli strumenti di DaRT 8,0 supportano ora i dischi GPT di Windows 8, che includono un meccanismo più flessibile per partizionare i dischi rispetto allo schema di partizionamento MBR (master boot record) più vecchio. Gli strumenti di DaRT 8,0 continuano a supportare il partizionamento MBR.

### Installare Windows 8 e Windows Server 2012 nel disco rigido locale

Gli strumenti di DaRT 8,0 possono essere usati solo quando Windows 8 e Windows Server 2012 sono installati nel disco rigido locale. Attualmente non è disponibile alcun supporto per Windows to go.

### <a href="" id="-------------dart-8-0-release-notes"></a> Note sulla versione di DaRT 8,0

Per altre informazioni e per le ultime notizie che non hanno reso disponibile la documentazione, vedere le [Note sulla versione di DaRT 8,0](release-notes-for-dart-80--dart-8.md).

## Come ottenere il dardo 8,0


Questa tecnologia fa parte di Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Argomenti correlati


[Attività iniziali di DaRT 8.0](getting-started-with-dart-80-dart-8.md)

[Note sulla versione per DaRT 8.0](release-notes-for-dart-80--dart-8.md)

 

 





