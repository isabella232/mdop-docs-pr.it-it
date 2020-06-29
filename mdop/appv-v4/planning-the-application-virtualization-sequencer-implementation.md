---
title: Pianificazione dell'implementazione di Application Virtualization Sequencer
description: Pianificazione dell'implementazione di Application Virtualization Sequencer
author: dansimp
ms.assetid: 052f32fe-ad13-4921-a8ce-4a657eb2b2bf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac62991e290dcd2da1c42f025a19365bda239fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815895"
---
# Pianificazione dell'implementazione di Application Virtualization Sequencer


La sequenziazione, il processo usato dalla virtualizzazione dell'applicazione per creare applicazioni virtuali e pacchetti di applicazioni, richiede l'uso di un computer con il software Application Virtualization Sequencer installato.

Durante il processo di sequenziazione, il sequencer viene posizionato in modalità di monitoraggio e l'applicazione da sequenziare viene installata nel computer di sequenziazione. Viene quindi avviata l'applicazione sequenziata e le relative funzioni più importanti e usate vengono esercitate in modo che il processo di monitoraggio possa configurare il blocco di funzionalità principale, che contiene il contenuto minimo in un pacchetto dell'applicazione necessario per l'esecuzione di un'applicazione. Una volta completate queste procedure, la modalità di monitoraggio viene interrotta e l'applicazione sequenziata viene salvata e testata per verificare il corretto funzionamento.

Quando si decide quali applicazioni scegliere per la sequenziazione, tenere presente che alcune applicazioni non possono essere sequenziate. Questi includono alcune parti del sistema operativo Windows, come Internet Explorer, i driver di dispositivo e le applicazioni che avviano i servizi al momento del boot.

Per informazioni dettagliate sull'installazione del sequencer, vedere [come installare Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).

**Importante**  L'intero piano di processo di sequenziazione deve essere esaminato e approvato dal team di sicurezza aziendale. Le operazioni di Sequencer in genere vengono mantenute separate dall'ambiente di produzione in un Lab. Questa operazione può essere semplice o completa, se necessario, in base ai requisiti aziendali. I computer di sequenziazione avranno bisogno di connettività alla rete aziendale per copiare i pacchetti finiti nei server di produzione. Tuttavia, dato che in genere sono gestite senza protezione antivirus, non devono essere protette dalla rete aziendale, ad esempio potresti essere in grado di operare dietro un firewall o su un segmento di rete isolata. L'uso di macchine virtuali configurate per condividere una rete virtuale isolata può anche essere un approccio accettabile. Seguire i criteri di sicurezza aziendali per risolvere in modo sicuro questa situazione.

 

I passaggi principali per pianificare il processo di sequenziazione includono i seguenti:

-   Considerare il numero di applicazioni che si prevede di elaborare ogni mese, le dimensioni di tali applicazioni e aggiungere un'indennità per la sequenziazione degli aggiornamenti futuri. I pacchetti possono contenere fino a 4 GB di dimensioni, compressi o non compressi.

-   Preparare e documentare un processo metodico e ripetibile per l'organizzazione da seguire durante la sequenziazione di ogni applicazione. Questo dovrebbe includere l'uso di un elenco di controllo per ogni esecuzione, oltre a un processo di controlli della versione. L'uso di un log di rilevamento per ogni applicazione sequenziata è anche molto utile quando si esaminano possibili problemi tecnici con un pacchetto.

-   Per la sequenziazione delle applicazioni, usare computer ad alte prestazioni ottimizzati per l'elaborazione della velocità effettiva, con almeno 4 GB di RAM e una CPU veloce (3 GHz o più veloce). Anche i dischi rigidi veloci e l'uso di volumi di disco separati possono migliorare le prestazioni. Le macchine virtuali sono ideali per la sequenziazione perché possono essere facilmente reimpostate oppure è possibile usare un computer fisico con un'immagine pulita in una partizione locale per consentire una rapida ricreazione delle immagini dopo il completamento di ogni operazione di sequenziazione del pacchetto.

    **Importante**  L'uso dell'App-V Sequencer in modalità provvisoria non è supportato.

     

-   Verificare di aver compreso l'ambiente operativo dell'applicazione sequenziata, inclusi gli elementi di integrazione come Microsoft Office o l'ambiente runtime Java, perché in questo modo viene spesso determinato se è necessario installare qualsiasi elemento nel computer di sequenziazione prima di sequenziare l'applicazione.

-   Verificare che ogni nuova operazione di sequenziazione inizi sempre con un'immagine di base pulita. Verificare che il computer di sequenziazione sia stato reimpostato ripristinando l'immagine salvata in un computer fisico o riavviando una macchina virtuale dopo aver scartato tutte le modifiche. L'immagine di base dovrebbe avere gli aggiornamenti più recenti applicati da Windows Update prima del salvataggio.

-   Disattivare qualsiasi operazione nel computer di sequenziazione che può interferire con il processo di monitoraggio dell'installazione, ad esempio scanner antivirus e Windows Update, perché è essenziale disporre di una piattaforma stabile durante il processo di sequenziazione. Poiché questo passaggio comporta rischi significativi per la sicurezza, assicurarsi che vengano prese le opportune precauzioni per proteggere il computer e la rete, nonché il pacchetto di applicazione sequenziata. È consigliabile eseguire un'analisi antivirus dei pacchetti di applicazioni prima di sequenziarli.

-   Includere una procedura dettagliata per testare ogni applicazione dopo la sequenziazione. Il test dell'applicazione sequenziata determina se funziona correttamente ed è una parte essenziale del processo prima di distribuire l'applicazione virtualizzata agli utenti finali. Come passaggio finale per il testing prima della distribuzione su larga scala per gli utenti finali, è consigliabile pianificare anche una distribuzione pilota in un gruppo di test.

-   Quando si provano le applicazioni sequenziate, scegliere apparecchiature informatiche dello stesso tipo ed eseguire gli stessi sistemi operativi in uso nell'ambiente di produzione aziendale. Purché siano configurati correttamente, è possibile usare macchine virtuali o macchine fisiche.

## Argomenti correlati


[Requisiti hardware e software per Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Come installare Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md)

[Come eseguire l'aggiornamento di Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)

[Panoramica di sicurezza e protezione](security-and-protection-overview.md)

 

 





