---
title: Note sulla versione di App-V 4.6 SP2
description: Note sulla versione di App-V 4.6 SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822345"
---
# Note sulla versione di App-V 4.6 SP2


**Per cercare queste note sulla versione, premere CTRL + F.**

Leggere accuratamente queste note sulla versione prima di installare Microsoft Application Virtualization (App-V) 4.6 SP2.

Queste note sulla versione contengono informazioni necessarie per installare correttamente Application Virtualization 4,6 SP2. Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V 4.6 SP2, la modifica più recente deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Informazioni sulla documentazione del prodotto


Per altre informazioni sulla documentazione per App-V, vedere la pagina [Application Virtualization](https://go.microsoft.com/fwlink/?LinkID=232982) in Microsoft TechNet.

## Commenti e suggerimenti


Siamo interessati a ricevere commenti e suggerimenti su App-V 4.6 SP2. È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .

**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future per la documentazione e i rilasci del prodotto.

 

Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a>Problemi noti di App-V 4.6 SP2


### Il supporto dei nomi di file brevi è disabilitato per le unità fisiche non di sistema quando si sequenzia

Quando si sequenzia in Windows 8 o Windows Server 2012, il supporto per i nomi di file brevi (8,3) è disabilitato per impostazione predefinita per le unità fisiche non di sistema.

L'unità fisica sottostante associata alla directory principale dell'applicazione virtuale (ad esempio, "Q:\\appname") nella stazione di sequenziazione deve fornire il supporto per il nome di file breve (8,3) in modo che l'App-V 4.6 SP2 sequencer generi i nomi di file brevi durante la creazione di pacchetti di applicazioni virtuali. Il supporto del nome file breve (8,3) è disabilitato per impostazione predefinita per le unità fisiche non di sistema in Windows 8 o Windows Server 2012.

**Soluzione alternativa:** Abilitare il supporto per il nome file breve (8,3) sulle unità fisiche non di sistema. Puoi usare il comando seguente per abilitare il supporto dei nomi di file brevi in Windows 8 o Windows Server 2012.

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

Ad esempio, usa il comando seguente se la lettera dell'unità è "Q:":

``` syntax
fsutil 8dot3name set Q: 0
```

**Nota**  Non è necessario modificare questa impostazione nel client App-V perché il file System App-V gestisce correttamente i percorsi brevi in Windows 8 o Windows Server 2012.

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> App-V non esegue l'override del gestore predefinito per il tipo di file o le associazioni di protocollo in Windows 8

Se selezioni un'applicazione predefinita usando **programmi predefiniti** nel pannello di **controllo** di Windows 8, App-V non eseguirà l'override delle associazioni di tipi di file associate per tale applicazione.

**Soluzione alternativa:** Nessuno.

### Outlook 2010 virtualizzato non è offerto come opzione per i collegamenti selezionabili di mailto in Windows 8

L'estensione della shell mailto non offre Outlook 2010 virtualizzato in Windows 8. Ad esempio, se si fa clic su un collegamento mailto: da Outlook 2010 virtualizzato in uso in Windows 8, non viene creata una nuova finestra di posta elettronica. Questa opzione funziona correttamente in Windows 7 e nelle versioni precedenti del sistema operativo Windows.

**Soluzione alternativa:** Nessuno.

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> L'aggiornamento di Application Virtualization 4,6 SP2 non è disponibile in tutte le impostazioni locali che usano Microsoft Update

Quando si usa Microsoft Update, l'aggiornamento per App-V 4.6 SP2 non è disponibile per le impostazioni locali della lingua seguenti:

-   Kazaco

-   Hindi

-   Serbo-cirillico

**Soluzione alternativa:** Se si usa Microsoft Windows Server Update Services (WSUS), usare la versione in lingua inglese dell'aggiornamento o scaricare l'aggiornamento dal catalogo Microsoft Update.

## Informazioni sul copyright delle note sulla versione


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società. Tutti gli altri marchi sono proprietà dei rispettivi proprietari.



## Argomenti correlati


[Informazioni su Microsoft Application Virtualization 4.6 SP2](about-microsoft-application-virtualization-46-sp2.md)

 

 





