---
title: Note sulla versione di App-V 4.6
description: Note sulla versione di App-V 4.6
author: dansimp
ms.assetid: a3eba129-edac-48bf-a933-3bf43a9873e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9eee3c309a927a72155dec707d8dd95f43e90fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822366"
---
# Note sulla versione di App-V 4.6


Per cercare queste note sulla versione, premere CTRL + F.

**Importante**  Leggere accuratamente queste note sulla versione prima di installare il sistema di gestione di Microsoft Application Virtualization (App-V). Queste note sulla versione contengono informazioni necessarie per installare correttamente Application Virtualization (App-V) 4.6. Questo documento contiene informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una discrepanza tra queste note sulla versione e altre documentazioni di App-V, la modifica più recente deve essere considerata autorevole.

 

## Protezione da vulnerabilità e virus della sicurezza


Per proteggere le vulnerabilità e i virus della sicurezza, è importante installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare. Per altre informazioni, vedere il [sito Web Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemi noti di Application Virtualization 4.6


Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.6. Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente. Quando possibile, questi problemi verranno risolti in versioni successive.

### Errore di caricamento/installazione in cui viene eseguito un file di Windows Installer generato dall'App-V 4.5 Sequencer

L'esecuzione di un file di Windows Installer generato da App-V 4.5 Sequencer genera un errore di caricamento/installazione durante il tentativo di eseguirlo in un client App-V 4,6. Verrà visualizzato il messaggio seguente: "questo pacchetto richiede Microsoft Application Virtualization Client 4.5 o versioni successive". Usare la soluzione alternativa seguente.

WORKAROUNDOpen il vecchio pacchetto con il sequencer App-V 4,5 SP1 o con l'App-V 4,6 Sequencer e genera un nuovo file MSI per il pacchetto.

**Nota**  In alternativa, al prompt dei comandi, l'App-V Sequencer può generare il nuovo file con estensione MSI usando i parametri */Open* e */MSI* , ad esempio `SFTSequencer /Open:”package.sprj” /MSI` . Per altre informazioni, vedere [come aggiornare un'applicazione virtuale tramite la riga di comando](how-to-upgrade-a-virtual-application-by-using-the-command-line.md).

 

### Informazioni sul copyright delle note sulla versione

Questo documento viene fornito "così com'è". Le informazioni e le opinioni espresse nel presente documento, inclusi gli URL e altri riferimenti a siti Web Internet, sono soggette a modifiche senza preavviso. Si rischia di usarlo.

Alcuni esempi descritti in questo documento sono forniti solo per le illustrazioni e sono fittizi.Nessuna associazione o connessione reale è destinata o deve essere dedotta.

Il presente documento non implica la concessione di alcun diritto di proprietà intellettuale in relazione ai prodotti Microsoft. È possibile copiare e usare questo documento per fini di riferimento interno. È possibile modificare questo documento per gli scopi interni e di riferimento.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server e Windows Vista sono marchi di fabbrica del gruppo Microsoft di società.

Tutti gli altri marchi sono proprietà dei rispettivi proprietari.

 

 





