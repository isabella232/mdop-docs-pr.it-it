---
title: Miglioramento della sicurezza durante la sequenza di App-V
description: Miglioramento della sicurezza durante la sequenza di App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816356"
---
# Miglioramento della sicurezza durante la sequenza di App-V


Le applicazioni di creazione di pacchetti per la sequenziazione sono l'attività in corso più grande in un'infrastruttura di App-V. Poiché questa attività è in corso, è consigliabile valutare attentamente la creazione di criteri e procedure da seguire durante la sequenziazione delle applicazioni. In App-V 4.5, durante la sequenziazione, è possibile acquisire gli elenchi di controllo di accesso (ACL) negli asset di file dell'applicazione virtualizzata.

## Ricerca di virus nel sequencer


È consigliabile installare il software di analisi nel computer di sequenziazione e quindi analizzare il computer per ottenere virus e malware. Quando il computer di sequenziazione viene digitalizzato e privo di virus o malware, disattivare il software di analisi, inclusi tutti i software di rilevamento antivirus e malware, nel computer di sequenziazione prima di sequenziare qualsiasi applicazione. Questo accelera il processo di sequenziazione e impedisce che i componenti software di analisi vengano rilevati durante la sequenziazione e inclusi nel pacchetto di applicazione virtuale.

## Acquisizione di ACL nei file (NTFS)


Il sequencer acquisisce le autorizzazioni NTFS (ACL) per i file monitorati durante la fase di installazione sequenziazione. Prima del rilascio di App-V 4.5, gli ACL non sono stati acquisiti come parte del processo di sequenziazione. Questa nuova funzionalità consente l'esecuzione di alcune applicazioni per gli utenti con un basso livello di autorizzazione che in genere richiedono privilegi amministrativi.

Questa funzionalità consente inoltre all'ingegnere sequenziazione di acquisire le impostazioni di sicurezza identificate dal fornitore. Se non si applicano le impostazioni consigliate dal fornitore, l'applicazione può essere aperta a un attacco o un uso improprio da parte degli utenti. Per informazioni sul fatto che sia necessario distribuire o meno un'applicazione con ACL aperti, vedere il gruppo di supporto dell'applicazione o il fornitore del software.

**Importante**  Anche se il sequencer acquisisce gli ACL NTFS durante il monitoraggio della fase di installazione della sequenziazione, non acquisisce gli ACL per il registro di sistema. Gli utenti hanno accesso completo a tutte le chiavi del registro di sistema per le applicazioni virtuali eccetto i servizi. Tuttavia, se un utente modifica il registro di sistema di un'applicazione virtuale, tale modifica viene archiviata in una posizione specifica ( `uservol_sftfs_v1.pkg` ) e non influisce su altri utenti.

 

Durante la fase di installazione, un ingegnere della sequenziazione può modificare le autorizzazioni predefinite dei file, se necessario. Dopo aver completato il processo di sequenziazione, ma prima di salvare il pacchetto, l'ingegnere della sequenziazione può quindi scegliere di applicare i descrittori di sicurezza acquisiti durante la fase di installazione. Si tratta di una procedura consigliata per applicare i descrittori di sicurezza se nessun'altra soluzione consente l'esecuzione corretta dell'applicazione una volta virtualizzata.

 

 





