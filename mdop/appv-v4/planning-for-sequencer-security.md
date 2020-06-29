---
title: Pianificazione per la sicurezza di Sequencer
description: Pianificazione per la sicurezza di Sequencer
author: dansimp
ms.assetid: 8043cb02-476d-4c28-a850-903a8ac5b2d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf1e85e24d93d373add38b5efe51ceb40faae24e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815915"
---
# Pianificazione per la sicurezza di Sequencer


Incorporare le procedure di implementazione consigliate il prima possibile quando si configura Application Virtualization (App-V) in modo che l'implementazione del sequencer sia funzionale e più sicura. Se il sequencer è già stato configurato, usare le linee guida consigliate seguenti per rivedere le decisioni di progettazione e analizzarle da un punto di vista della sicurezza.

**Importante**  
App-V Sequencer raccoglie e distribuisce tutte le informazioni sull'applicazione registrate nel computer che gestisce il sequencer. Devi verificare che tutti gli utenti che accedono al computer con il sequencer abbiano credenziali amministrative. Gli utenti con le credenziali dell'account utente non devono avere accesso a controllare il contenuto del pacchetto e i file di pacchetto. Se si esegue la sequenziazione in un computer con Servizi Desktop remoto (in precedenza Servizi terminal), verificare che sia un computer dedicato alla sequenziazione e che gli utenti con le credenziali dell'account utente non siano connessi durante la sequenziazione.



## Procedure consigliate per la sicurezza sequenziale


Per l'implementazione e l'uso dell'Application Virtualization (App-V) Sequencer, considerare gli scenari e le procedure consigliate seguenti:

-   **Ricerca di virus nel computer che esegue il sequencer**, è consigliabile analizzare il computer che esegue il sequencer per i virus e quindi disabilitare tutti i software di rilevamento antivirus e malware nel computer che esegue il sequencer durante il processo di sequenziazione. Questo accelererà il processo di sequenziazione e impedirà ai componenti software antivirus e anti-malware di interferire con il processo di sequenziazione. Installare quindi il pacchetto sequenziato in un computer che non esegue il sequencer e dopo aver eseguito l'installazione, analizzare il computer per i virus. Se vengono trovati virus, il produttore del software deve essere contattato per informarli dei file di origine infetti e richiedere un'origine di installazione aggiornata senza virus. Facoltativamente, il sequencer può essere scansionato dopo la fase di installazione e se viene trovato un virus, il produttore del software deve essere contattato come indicato sopra.

    **Nota**  
    Se un virus viene rilevato in un'applicazione, l'applicazione non deve essere distribuita in computer di destinazione.



-   **Acquisizione di elenchi di controllo di accesso (ACL) nei file NTFS**: l'App-V Sequencer acquisisce le autorizzazioni di file system NTFS per i file controllati durante l'installazione del prodotto. Questa funzionalità consente di replicare in modo più accurato il comportamento previsto dell'applicazione, come se fosse installato localmente e non virtualizzato. In alcuni scenari, un'applicazione potrebbe archiviare informazioni che gli utenti non erano destinate ad accedere all'interno dei file dell'applicazione. Ad esempio, un'applicazione può archiviare le informazioni sulle credenziali in un file all'interno dell'applicazione. Se gli ACL non vengono applicati nel pacchetto, un utente può potenzialmente visualizzare e quindi usare queste informazioni all'esterno dell'applicazione.

    **Nota**  
    Non è consigliabile sequenziare le applicazioni che archiviano informazioni specifiche per la sicurezza non crittografate, ad esempio password e così via.



~~~
During the installation phase, you can modify the default permissions of the files if necessary. After completion of the sequencing process, but before saving the package, you can choose whether to enforce security descriptors that were captured during the installation of the application. By default, App-V will enforce the security descriptors specified during the installation of the application. If you turn off security descriptor enforcement, you should test the application to ensure the removal of associated Access Control Lists (ACL) will not cause the application to perform unexpectedly.
~~~

-   **Sequencer non acquisisce gli ACL del registro**di sistema, anche se il sequencer acquisisce gli ACL del file system NTFS durante la fase di installazione della sequenziazione, non acquisisce gli ACL per il registro. Gli utenti avranno accesso completo a tutte le chiavi del registro di sistema per le applicazioni virtuali eccetto per i servizi. Tuttavia, se un utente modifica il registro di sistema di un'applicazione virtuale, la modifica verrà archiviata in uno specifico archivio (**uservol \ _sftfs \ _v1. pkg**) e non influirà su altri utenti.

-   **Application Services**: App-V offre il supporto per i servizi delle applicazioni che fanno parte di un'applicazione virtualizzata. Tuttavia, nell'ambiente virtuale, il contesto di sicurezza che verrà eseguito come è limitato. Gli unici contesti di sicurezza supportati in un ambiente virtuale sono il sistema locale, il servizio locale e il servizio di rete. Durante la sequenziazione, se viene specificato un contesto di sicurezza per un servizio applicazione diverso da tre supportati, il contesto di sicurezza del sistema locale verrà applicato nell'ambiente virtuale. Se il servizio applicazione è configurato per l'uso del servizio locale o del servizio di rete, verrà rispettato nell'ambiente virtuale. La configurazione dell'account del servizio può essere eseguita durante il processo di sequenziazione usando questi tre contesti di sicurezza.

-   **Informazioni di sicurezza permanenti**: durante la sequenziazione delle applicazioni, è possibile installare l'applicazione come utente oppure sviluppare un metodo automatizzato per l'installazione dell'applicazione durante il monitoraggio. Tutto ciò che non viene escluso dal pacchetto verrà acquisito come parte di tale pacchetto in modo che l'applicazione disponga delle risorse necessarie per l'esecuzione in un ambiente virtualizzato. Alcune applicazioni archiviano informazioni di sicurezza riservate (ad esempio password) durante l'installazione; Se PERSISTED non protetto, queste informazioni di sicurezza potrebbero essere accessibili da altri utenti con accesso al pacchetto. Durante l'installazione, se un'installazione di un'applicazione richiede una password o altre informazioni riservate alla sicurezza, verificare che la documentazione non venga mantenuta (rimossa dopo l'installazione) o, se persistente, che sia protetta (crittografata).

-   **Protezione dei pacchetti di applicazioni virtuali**: salvare sempre i pacchetti di applicazioni virtuali in un percorso sicuro della rete per proteggere il pacchetto dall'essere manomesso o danneggiato.

## Argomenti correlati


[Pianificazione per sicurezza e protezione](planning-for-security-and-protection.md)









