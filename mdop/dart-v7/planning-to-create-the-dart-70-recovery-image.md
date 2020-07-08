---
title: Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0
description: Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821335"
---
# Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0


Usare le informazioni in questa sezione quando si prevede di creare l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 7.

## Pianificazione della creazione dell'immagine di ripristino di DaRT 7


Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine. Quando si decide, tenere presente che gli utenti finali potrebbero avere accesso occasionalmente ai vari strumenti DaRT. Per altre informazioni sugli strumenti DaRT, Vedi [Panoramica degli strumenti di dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md). Per altre informazioni su come semplificare la creazione di un'immagine di ripristino sicura, vedere [considerazioni sulla sicurezza per DaRT 7,0](security-considerations-for-dart-70-dart-7.md).

Quando si crea l'immagine di ripristino delle freccette, si specifica anche se si desidera includere altri driver o file. Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.

## Prerequisiti


Gli elementi seguenti sono obbligatori o consigliati per creare l'immagine di ripristino DaRT:

-   File di origine di Windows 7

    Devi specificare il percorso di un DVD di Windows 7 o di file di origine di Windows 7. I file di origine di Windows 7 sono necessari per creare l'immagine di ripristino DaRT.

-   Strumenti di debug di Windows per la tua piattaforma

    Gli strumenti di debug di Windows sono necessari quando si esegue **analizzatore crash** per determinare la causa di un arresto anomalo del computer. Ti consigliamo di specificare il percorso degli strumenti di debug di Windows al momento della creazione dell'immagine di ripristino DaRT. Se necessario, è possibile scaricare gli strumenti di debug di Windows qui: [scaricare e installare gli strumenti di debug per Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

-   Facoltativo: definizioni di **Sweep System autonome**

    Quando si esegue questo strumento, sono necessarie le definizioni più recenti per la **spazzatrice di sistema autonoma** . Anche se è possibile scaricare le definizioni quando si esegue una **spazzatrice di sistema autonoma**, è consigliabile scaricare le definizioni più recenti al momento della creazione dell'immagine di ripristino delle freccette. In questo modo, è comunque possibile eseguire lo strumento con le definizioni più recenti anche se il computer problema non ha connettività di rete.

-   Facoltativo: file di simboli Windows da usare con **Crash Analyzer**

    In genere, le informazioni di debug sono archiviate in un file di simboli separato dall'eseguibile. È necessario avere accesso alle informazioni sul simbolo quando si effettua il debug di un'applicazione che ha smesso di rispondere, ad esempio se è stata arrestata. Per altre informazioni, vedere [diagnostica degli errori di sistema con Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).

## Argomenti correlati


[Pianificazione della distribuzione di DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





