---
title: Interoperabilità di App-V con Windows AppLocker
description: Interoperabilità di App-V con Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822315"
---
# Interoperabilità di App-V con Windows AppLocker


La versione 4,5 SP1 di Microsoft Application Virtualization (App-V) client supporta la funzionalità AppLocker di Windows 7. La funzionalità AppLocker consente agli amministratori IT di specificare quali applicazioni sono limitate dall'uso in computer. Questo documento descrive come configurare le regole di AppLocker per l'utilizzo con l'ambiente virtuale App-V e le applicazioni virtualizzate.

**Nota**  Windows AppLocker deve prima essere abilitato prima di configurare le regole di Windows AppLocker per le applicazioni virtuali. Per altre informazioni sull'abilitazione di Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .

 

## Configurazione delle regole di Windows AppLocker per le applicazioni virtuali


Gli amministratori locali possono creare regole di Windows AppLocker che limitano l'uso di file eseguibili di programmi (file exe), file di Windows Installer (file con estensione msi e msp) e script (con estensione PS, bat, cmd e js). L'amministratore esegue questa operazione usando un computer di riferimento in cui è installato il client App-V e che contiene tutte le applicazioni virtuali rilevanti in streaming nella cache del client. L'amministratore usa quindi la sezione Windows AppLocker dello snap-in Microsoft Management Console (MMC) dei criteri di sicurezza locali nel computer di riferimento per creare le regole.

Quando si cerca un percorso di directory o un file specifico per cui si vuole creare una regola, è possibile accedere all'unità App-V usando il percorso della condivisione nascosta. Ad esempio, puoi passare a \\\\localhost\\Q $, dove l'App-V Drive è drive Q. Tuttavia, per creare la regola, devi modificare il percorso per rimuovere il riferimento a \\\\localhost\\Q $ e usare Q:\\. È necessario avviare ogni applicazione nel computer di riferimento per accedere ai file dell'applicazione e sono necessari i diritti amministrativi per passare a \\\\localhost\\Q $.

 

 





