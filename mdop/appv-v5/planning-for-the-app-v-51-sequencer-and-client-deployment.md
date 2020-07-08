---
title: Pianificazione della distribuzione di App-V 5.1 Sequencer e del client
description: Pianificazione della distribuzione di App-V 5.1 Sequencer e del client
author: dansimp
ms.assetid: d92f8773-fa7d-4926-978a-433978f91202
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 31a0296814b16ba1c776dca522423fc7b6b6ed96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804995"
---
# Pianificazione della distribuzione di App-V 5.1 Sequencer e del client


Prima di poter iniziare a usare Microsoft Application Virtualization (App-V) 5,1, è necessario installare l'App-V 5,1 sequencer, il client App-V 5,1 e, facoltativamente, l'App-V 5,1 Shared Content Store. Le sezioni seguenti includono la pianificazione per queste installazioni.

## Pianificazione della distribuzione di Sequencer per App-V 5,1


App-V 5,1 usa un processo denominato sequenziazione per creare applicazioni virtualizzate e pacchetti di applicazioni. La sequenziazione richiede l'uso di un computer che esegue l'App-V 5,1 Sequencer.

**Nota**  Per informazioni sulle nuove funzionalità di App-V 5,1 sequencer, vedere la sezione **miglioramenti sequencer** di [About app-v 5,1](about-app-v-51.md).

 

Il computer che esegue l'App-V 5,1 Sequencer deve soddisfare i requisiti minimi di sistema. Per un elenco di questi requisiti, vedere [configurazioni supportate in App-V 5,1](app-v-51-supported-configurations.md).

Idealmente, dovresti installare il sequencer in un computer che si trova in una macchina virtuale. Questo consente di ripristinare più facilmente il computer che ha eseguito il sequencer in uno stato "pulito" prima di sequenziare un'altra applicazione. Quando si installa il sequencer tramite una macchina virtuale, è necessario eseguire la procedura seguente:

1.  Installare tutti i prerequisiti del sequencer associato.

2.  Installare il sequencer.

3.  Eseguire una "snapshot" dell'ambiente.

**Importante**  Dovresti avere la revisione del team di sicurezza aziendale e approvare il piano di processo di sequenziazione. Per motivi di sicurezza, è consigliabile mantenere le operazioni sequencer in un Lab separato dall'ambiente di produzione. La disposizione di separazione può essere il più semplice o esaustivo necessario, in base ai requisiti aziendali. I computer di sequenziazione devono essere in grado di connettersi alla rete aziendale per copiare i pacchetti finiti nei server di produzione. Tuttavia, poiché i computer di sequenziazione sono in genere gestiti senza protezione antivirus, non devono essere protetti dalla rete aziendale. Ad esempio, potresti essere in grado di operare dietro un firewall o su un segmento di rete isolata. Potresti anche essere in grado di usare macchine virtuali configurate per condividere una rete virtuale isolata. Seguire i criteri di sicurezza aziendali per risolvere in modo sicuro questi problemi.

 

## Pianificazione per la distribuzione di client App-V 5,1


Per eseguire i pacchetti virtualizzati nei computer di destinazione, è necessario installare il client App-V 5,1 nei computer di destinazione. Il client App-V 5,1 è il componente che esegue un'applicazione virtualizzata in un computer di destinazione. Il client consente agli utenti di interagire con le icone e i tipi di file specifici per avviare le applicazioni virtualizzate. Il client consente inoltre di ottenere contenuto dell'applicazione dal server di gestione e memorizza nella cache il contenuto prima che l'applicazione venga avviata dal client. Esistono due tipi di client diversi: il client per Servizi Desktop remoto, che viene usato nei sistemi server Host sessione Desktop remoto e nel client App-V 5,1, usato per tutti gli altri computer.

Il client App-V 5,1 deve essere configurato usando la riga di comando del programma di installazione oppure usando uno script di PowerShell dopo il completamento dell'installazione.

Le impostazioni devono essere definite con attenzione in anticipo per velocizzare la distribuzione del software client App-V 5,1. Questo aspetto è particolarmente importante quando si hanno computer in uffici diversi in cui i client devono essere configurati per l'uso di percorsi di origine diversi.

Devi anche determinare la modalità di distribuzione del software client. Anche se è possibile distribuire manualmente il client in ogni computer, la maggior parte delle organizzazioni preferisce distribuire il client tramite un processo automatizzato. Un'organizzazione più grande può avere un sistema ESD (Operational Electronic Software Distribution), un sistema di distribuzione client ideale. Se non esiste alcun sistema ESD, puoi usare il metodo standard dell'organizzazione per l'installazione del software. I metodi possibili includono criteri di gruppo o varie tecniche di scripting. A seconda delle posizioni di quantità e disparate dei computer client, questo processo di distribuzione può essere complesso. È necessario usare un approccio strutturato per assicurarsi che tutti i computer vengano installati dal client con la configurazione corretta.

Per un elenco dei requisiti minimi del client [, vedere Prerequisiti di App-V 5,1](app-v-51-prerequisites.md).

## <a href="" id="bkmk-client-coexist"></a>Pianificazione della coesistenza client App-V


Puoi distribuire il client App-V 5,1 affiancato al client App-V 4,6. La coesistenza client richiede l'aggiunta o la pubblicazione di applicazioni virtualizzate usando un file di configurazione della distribuzione o un file di configurazione dell'utente, perché esistono alcune impostazioni in questi file di configurazione che devono essere configurati in modo che App-V 5,1 funzioni con i client App-V 4.6. Quando si esegue l'aggiornamento di un pacchetto tramite il client o il server, il pacchetto deve inviare nuovamente il file di configurazione. Questo vale per qualsiasi pacchetto che contiene un file di configurazione corrispondente, quindi non è specifico della coesistenza del client. Tuttavia, se il file di configurazione non viene inviato durante l'aggiornamento del pacchetto, lo stato del pacchetto non funzionerà come previsto negli scenari di coesistenza.

I file di configurazione dinamica di App-V 5,1 personalizzano un pacchetto per un utente specifico. Per poterli usare, devi creare il file di configurazione dinamica degli utenti o il file di configurazione della distribuzione dinamica. Per creare il file, è necessaria un'operazione manuale avanzata.

Quando si usa un file di configurazione utente dinamico, non viene usata nessuna delle informazioni di App-V 5,1 per l'estensione nel file manifesto. Ciò significa che il file di configurazione dell'utente dinamico deve includere tutto per l'estensione specifica di App-V 5,1 nel file manifesto, nonché le modifiche che si desidera apportare, ad esempio eliminazioni e aggiornamenti. Per altre informazioni su come creare un file di configurazione personalizzato, vedere [come creare un file di configurazione personalizzato usando la console di gestione di App-V 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

## <a href="" id="bkmk-plan-for-scs"></a>Pianificazione per l'App-V 5,1 Shared Content Store (SCS)


La modalità di archiviazione condivisa di App-V 5,1 consente al computer che esegue il client App-V 5,1 di eseguire applicazioni virtualizzate e nessuno dei contenuti del pacchetto viene salvato nel computer che esegue il client App-V 5,1. Le applicazioni virtuali vengono trasmesse in streaming ai computer di destinazione solo quando richiesto dal client.

L'elenco seguente mostra alcuni vantaggi dell'uso dell'App-V 5,1 Shared Content Store:

-   I conflitti tra app per app e multiutente sono ridotti e quindi è necessario ridurre i test di regressione

-   Distribuzione accelerata delle applicazioni tramite riduzione del rischio di distribuzione

-   Gestione semplificata dei profili






## <a href="" id="other-resources-for-the-app-v-5-1-deployment-"></a>Altre risorse per la distribuzione di App-V 5,1


[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

## Argomenti correlati


[Come installare Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)

[Come distribuire il client App-V](how-to-deploy-the-app-v-client-51gb18030.md)

[Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

[Come installare il client App-V 5.1 per la modalità SCS (Shared Content Store)](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

 

 





