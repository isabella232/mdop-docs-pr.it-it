---
title: Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V
description: Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826925"
---
# Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V


Anche se un'applicazione viene installata in un'area di lavoro MED-V, potrebbe essere necessario pubblicare l'applicazione anche prima che diventi disponibile per l'utente finale. Per impostazione predefinita, la maggior parte delle applicazioni viene pubblicata nel momento in cui sono installate e i tasti di scelta rapida vengono creati e abilitati.

In alcuni casi, è possibile installare le applicazioni nell'area di lavoro MED-V senza renderle disponibili per l'utente finale, ad esempio software per la ricerca di virus. Allo stesso modo, ci sono occasioni in cui vuoi pubblicare un'applicazione installata nell'area di lavoro MED-V che in precedenza non era disponibile per l'utente finale. Ad esempio, potrebbe essere necessario pubblicare un'applicazione installata se l'installazione non crea automaticamente un collegamento nel menu **Start** .

**Importante**  Se pubblichi un'applicazione che non supporta percorsi UNC, ti consigliamo di eseguire il mapping dell'applicazione a un'unità.

 

È possibile pubblicare o annullare la pubblicazione di applicazioni in un'area di lavoro MED-V distribuita eseguendo una delle attività seguenti:

**Per pubblicare o annullare la pubblicazione di un'applicazione installata**

1.  Per pubblicare un'applicazione in un'area di lavoro MED-V distribuita, copiare un collegamento per l'applicazione nella cartella seguente della macchina virtuale:

    Menu di C:\\Documents and e Settings\\All Users\\Start

    Se necessario, usare criteri di gruppo o un sistema ESD per distribuire uno script che copia il collegamento per l'applicazione nella cartella tutti i menu di Users\\Start.

2.  Per annullare la pubblicazione di un'applicazione in un'area di lavoro MED-V distribuita, eliminare il collegamento per l'applicazione dalla cartella seguente nella macchina virtuale:

    Menu di C:\\Documents and e Settings\\All Users\\Start

    Se necessario, usare criteri di gruppo o un sistema ESD per distribuire uno script che elimina il collegamento per tale applicazione dalla cartella tutti i menu di Users\\Start.

    **Nota**  Spesso, quando si disinstalla l'applicazione, il collegamento viene eliminato automaticamente dal menu **Start** del computer host. Tuttavia, in alcuni casi, ad esempio per un'area di lavoro MED-V configurata per tutti gli utenti di un computer condiviso, potrebbe essere necessario eliminare manualmente il collegamento nel menu **Start** dopo la disinstallazione dell'applicazione. L'utente finale può eseguire questa operazione facendo clic con il pulsante destro del mouse sul collegamento e scegliendo **Elimina**.

     

Per verificare che l'applicazione sia stata pubblicata o non pubblicata, verifica nell'area di lavoro MED-V se il collegamento corrispondente è disponibile o meno.

**Nota**  Le applicazioni incluse in Windows XP SP3 e si trovano nella cartella del menu Start della macchina virtuale non vengono pubblicate automaticamente nell'host. Sono controllate dalle impostazioni del registro di sistema che bloccano la pubblicazione automatica. Per altre informazioni, Vedi [elenco esclusioni applicazioni di Windows Virtual PC](windows-virtual-pc-application-exclude-list.md).

 

**Per pubblicare gli elementi del pannello di controllo**

1.  Creare un collegamento nella macchina virtuale in cui la destinazione è il nome dell'elemento, ad esempio C:\\WINDOWS\\system32\\appwiz.cpl.

    Il collegamento deve essere creato in o spostato nella cartella "%ALLUSERSPROFILE%\\Start Menu\\" o in una delle relative sottocartelle.

    L'elemento verrà pubblicato nel computer host nella posizione corrispondente nella cartella del menu di avvio dell'host.

2.  Avviare il collegamento per l'elemento nell'host.

**Attenzione**  Quando si crea il collegamento, non specificare% SystemRoot% \\control.exe. Questa applicazione non verrà pubblicata perché è contenuta nelle impostazioni del registro di sistema che bloccano la pubblicazione automatica.

 

**Come MED-V gestisce la pubblicazione automatica delle applicazioni**

1.  Durante la pubblicazione dell'applicazione, MED-V copia i tasti di scelta rapida dalla macchina virtuale Guest al computer host provando a corrispondere alla gerarchia delle cartelle esistente nel guest. In questo modo, MED-V copia i tasti di scelta rapida dal Guest all'host eseguendo la procedura seguente:

    1.  MED-V cerca di individuare una cartella in Start Menu\\Programs nel computer host denominata uguale alla cartella nel guest in cui si trova il collegamento.

    2.  Se non è presente alcuna cartella corrispondente, MED-V cerca quindi di individuare una cartella nella cartella del menu Start dell'host denominata uguale alla cartella dell'ospite in cui si trova il collegamento.

    3.  Se non è presente alcuna cartella corrispondente, MED-V copia il collegamento alla cartella predefinita dell'host, la cartella Start Menu\\Programs.

2.  Esempio di processo di pubblicazione delle applicazioni:

    1.  Se un collegamento a un'applicazione viene pubblicato nella cartella Start Menu\\Programs\\AppShortcuts nel guest, MED-V Cerca nel computer host una cartella Start Menu\\Programs\\ AppShortcuts e, se trovata, copia il collegamento a tale cartella.

    2.  Se la cartella non viene trovata, MED-V Cerca nel computer host una cartella Start Menu\\AppShortcuts e, se trovata, copia il collegamento a tale cartella.

    3.  Se la cartella non viene trovata, MED-V copia il collegamento alla cartella Start Menu\\Programs.

**Nota**  Una cartella deve esistere già nella cartella del menu Start del computer host per MED-V per copiare il collegamento. MED-V non crea la cartella se non esiste già.

 

## Argomenti correlati


[Installazione e rimozione di un'applicazione nell'area di lavoro MED-V](installing-and-removing-an-application-on-the-med-v-workspace.md)

[Gestione degli aggiornamenti software per le aree di lavoro MED-V](managing-software-updates-for-med-v-workspaces.md)

[Elenco esclusioni dell'applicazione Windows Virtual PC](windows-virtual-pc-application-exclude-list.md)

 

 





