---
title: Note sulla versione per DaRT 7.0
description: Note sulla versione per DaRT 7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822765"
---
# Note sulla versione per DaRT 7.0


**Per cercare queste note sulla versione, premere CTRL + F.**

Leggere accuratamente queste note sulla versione prima di installare Microsoft Diagnostics and Recovery Toolset (DaRT) 7.

## Informazioni su Microsoft Diagnostics and Recovery Toolset 7,0


Queste note sulla versione contengono informazioni necessarie per installare correttamente DaRT7 e contengono informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni della piattaforma DaRT, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Informazioni sulla documentazione del prodotto


La documentazione per Microsoft Diagnostics and Recovery Toolset (DaRT) 7 viene distribuita con il prodotto e nel sito Connect.

Per informazioni dettagliate su come usare gli strumenti in DaRT7, vedere il file della Guida disponibile nel menu **strumenti di diagnostica e ripristino** .

## Commenti e suggerimenti


Siamo interessati a ricevere commenti e suggerimenti su DaRT7. È possibile inviare il proprio feedback a dart7feedback@microsoft.com. Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future per questi strumenti per renderle più utili in futuro.

## Protezione da vulnerabilità e virus della sicurezza


Per proteggere le vulnerabilità e i virus della sicurezza, è consigliabile installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare. Per altre informazioni, vedere [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemi noti di DaRT 7,0


### L'analisi SFC non può essere avviata se la spazzatrice di sistema autonoma è aperta

Se lo strumento di sweep del sistema autonomo è in esecuzione, l'analisi SFC non può essere avviata o eseguita a causa di un conflitto di risorse tra i due strumenti.

**Soluzione alternativa:** Chiudere la spazzatrice di sistema autonomo prima di provare ad aprire o eseguire lo strumento di analisi SFC.

### I caratteri Unicode potrebbero non essere visualizzati nei nomi di file

Se si elimina un file con caratteri Unicode nel nome del file e si prova a ripristinare il file usando lo strumento di ripristino file, il file non viene trovato. Questo problema si verifica solo quando si usano caratteri di una lingua diversa dalla lingua del DVD di Windows usato per creare l'immagine di ripristino.

**Soluzione alternativa:** Verificare che la lingua usata da DaRT corrisponda alla lingua usata dal sistema operativo da cui sta provando a ripristinare i file.

### L'installazione della riga di comando DaRT potrebbe non riuscire automaticamente

L'installazione della riga di comando DaRT non riesce automaticamente se eseguita con l'opzione modalità non interattiva, a meno che non venga eseguita usando autorizzazioni di amministratore elevate.

**Soluzione alternativa:** Eseguire l'installazione della riga di comando usando le autorizzazioni di amministratore elevate. L'installazione di DaRT supporta le tipiche opzioni di Windows Installer per l'installazione della riga di comando. Vedere [Opzioni della riga di comando](https://go.microsoft.com/fwlink/?LinkId=160689) per Windows Installer per altre informazioni sulle diverse opzioni disponibili.

### La ricerca di file non può trasferire una cartella in un volume diverso

Lo spostamento delle cartelle tra volumi non è supportato dall'applicazione di ricerca file. Se si prova a trasferire una cartella in un volume diverso nella ricerca file, viene restituito l'errore seguente: "si è verificato un errore durante la scrittura del * &lt; nome &gt; *file. Verificare che l'unità disponga di spazio sufficiente e che il percorso di destinazione sia accessibile. "

**Soluzione alternativa:** Usare Esplora risorse per trasferire una cartella in un volume diverso.

### Alcuni dati potrebbero non essere disponibili nei computer in cui vengono rimappate le lettere di unità

Questo problema può verificarsi in computer con attivazione BitLocker e multiboot. Questo problema si verifica perché alcune informazioni nel registro di sistema offline includono lettere di unità hardcoded e dardo usa lettere diverse per gli stessi volumi. Gli effetti tipici includono non avere accesso a determinati account utente locali nell'editor del registro di sistema. Inoltre, alcuni strumenti potrebbero non essere in grado di ottenere proprietà che si basano sulla risoluzione dei percorsi di file.

**Soluzione alternativa:** Usa l'opzione per riassociare le lettere dell'unità all'avvio di DaRT. In genere le lettere di unità tipiche vengono allineate a quelle previste.

### La disinstallazione dell'hotfix potrebbe non disinstallare alcuni aggiornamenti

Alcuni aggiornamenti e Service Pack non possono essere disinstallati perché contrassegnati come non installabili o perché devono essere disinstallati in Windows 7. In queste istanze, lo strumento di disinstallazione dell'hotfix può indicare che questi aggiornamenti sono stati disinstallati anche se non sono stati.

**Soluzione alternativa:** Disinstallare questi aggiornamenti problematici da Windows 7.

### Cancellazione disco: non è possibile eliminare i dischi con volumi con spanning, volumi a strisce o volumi speculari

La cancellazione disco non supporta l'eliminazione di dischi con spanning, mirroring o striping in uno o più volumi.

**Soluzione alternativa:** Selezionare ed eliminare ogni disco nel volume separatamente.

## Informazioni sul copyright delle note sulla versione


Questo documento viene fornito "così com'è". Le informazioni e le visualizzazioni espresse in questo documento, incluso l'URL e altri riferimenti al sito Web Internet, possono cambiare senza preavviso. Si rischia di usarlo.

Alcuni esempi descritti in questo documento sono forniti solo per le illustrazioni e sono fittizi.Nessuna associazione o connessione reale è destinata o deve essere dedotta.

Il presente documento non implica la concessione di alcun diritto di proprietà intellettuale in relazione ai prodotti Microsoft. Questo documento è riservato e proprietario di Microsoft. Viene divulgato e può essere usato solo in base a un contratto di segretezza.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista sono marchi di fabbrica del gruppo Microsoft di società.

Tutti gli altri marchi sono proprietà dei rispettivi proprietari.

## Argomenti correlati


[Informazioni su DaRT 7.0](about-dart-70-new-ia.md)

 

 





