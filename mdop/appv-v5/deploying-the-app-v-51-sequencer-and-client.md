---
title: Distribuzione di App-V 5.1 Sequencer e del client
description: Distribuzione di App-V 5.1 Sequencer e del client
author: dansimp
ms.assetid: 74f32794-4c76-436f-a542-f9e95d89063d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3b78059e5005f563bb99d7e6f4b5fe0af2eae8d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805824"
---
# Distribuzione di App-V 5.1 Sequencer e del client


Il sequencer e il client di Microsoft Application Virtualization (App-V) 5,1 consentono agli amministratori di virtualizzare ed eseguire applicazioni virtualizzate.

## Distribuire il client


Il client App-V 5,1 è il componente che esegue un'applicazione virtualizzata in un computer di destinazione. Il client consente agli utenti di interagire con le icone e fare doppio clic su tipi di file, in modo che possano avviare un'applicazione virtualizzata. Il client può anche ottenere il contenuto dell'applicazione virtuale dal server di gestione.

[Come distribuire il client App-V](how-to-deploy-the-app-v-client-51gb18030.md)

[Come disinstallare il client App-V 5.1](how-to-uninstall-the-app-v-51-client.md)

[Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

## Impostazioni di configurazione client


Il client App-V 5,1 archivia la configurazione nel registro di sistema. Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client. È anche possibile configurare molte azioni client modificando le voci del registro di sistema.

[Informazioni sulle impostazioni di configurazione client](about-client-configuration-settings51.md)

## Configurare il client tramite il modello ADMX e i criteri di gruppo


È possibile usare il modello Microsoft ADMX per configurare le impostazioni client per il client App-V 5,1 e il client Servizi Desktop remoto. Il modello ADMX gestisce le configurazioni client comuni usando un'infrastruttura di criteri di gruppo esistente e include le impostazioni per la configurazione client App-V 5,1.

**Importante**  Puoi ottenere il modello ADMX App-V 5,1 dall'area download Microsoft.

 

Dopo aver scaricato e installato il modello ADMX, eseguire la procedura seguente nel computer che verrà usato per gestire i criteri di gruppo. Si tratta in genere del controller di dominio.

1.  Salvare il file con **estensione ADMX** nella directory seguente: **Windows \ \ PolicyDefinitions**

2.  Salvare il file con estensione **ADML** nella directory seguente: **Windows \ \ PolicyDefinitions \ \ &lt; Language directory &gt; **

Dopo aver completato la procedura descritta in precedenza, è possibile gestire le impostazioni di configurazione del client App-V 5,1 con la console **Gestione criteri di gruppo** .

Il client App-V 5,1 archivia anche la configurazione nel registro di sistema. Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client. È anche possibile configurare molte azioni client modificando le voci del registro di sistema.

[Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

## Distribuire il client tramite la modalità di archiviazione contenuto condivisa


La modalità SCS (Shared Content Store) App-V 5,1 consente ai client SCS App-V 5,1 di eseguire applicazioni virtualizzate senza salvare localmente i dati del pacchetto associati. Tutti i dati del pacchetto virtualizzato necessari vengono trasmessi attraverso la rete; Devi quindi usare la modalità SCS solo in ambienti con una connessione veloce. I Servizi Desktop remoto (RDS) e la versione standard del client App-V 5,1 sono supportati con la modalità SCS.

**Importante**  Se il client App-V 5,1 è configurato per l'esecuzione in modalità SCS, la posizione in cui vengono trasmessi i pacchetti App-V 5,1 deve essere disponibile, in caso contrario il pacchetto virtualizzato non riuscirà. Inoltre, non è consigliabile distribuire applicazioni virtualizzate nei computer che eseguono il client App-V 5,1 in modalità SCS su Internet.

 

Inoltre, il SCS non è una posizione fisica che contiene pacchetti virtualizzati. Si tratta di una modalità che consente al client App-V 5,1 di trasmettere i dati del pacchetto virtualizzato necessario in tutta la rete.

La modalità SCS è utile negli scenari seguenti:

-   Distribuzioni di Virtual Desktop Infrastructure (VDI)

-   Distribuzioni Remote Desktop Services (RDS)

Per usare SCS nell'ambiente, è necessario abilitare il client App-V 5,1 per l'esecuzione in modalità SCS. Questa impostazione deve essere specificata durante l'installazione. Per impostazione predefinita, il client non è configurato per l'uso della modalità SCS. È consigliabile installare il client usando la procedura suggerita se si prevede di usare SCS. Tuttavia, puoi configurare un client App-V 5,1 esistente per l'esecuzione in modalità SCS immettendo il comando PowerShell seguente nel computer che esegue il client App-V 5,1:

**set-AppvClientConfiguration-SharedContentStoreMode 1**

Potrebbero verificarsi casi in cui l'amministratore carica alcune applicazioni virtuali nel computer che esegue il client App-V 5,1 in modalità SCS. Questa operazione può essere eseguita con i comandi di PowerShell per aggiungere, pubblicare e montare il pacchetto. Ad esempio, se un pacchetto è precaricato in tutti i computer, l'amministratore può aggiungere, pubblicare e montare il pacchetto usando i comandi di PowerShell. Il pacchetto non eseguirebbe il flusso in tutta la rete perché sarebbe archiviato localmente.

[Come installare il client App-V 5.1 per la modalità SCS (Shared Content Store)](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

## Distribuire il sequencer


Sequencer è uno strumento usato per convertire le applicazioni standard in pacchetti virtuali per la distribuzione in computer che eseguono il client App-V 5,1. Il sequencer aiuta a creare un processo di conversione semplice e prevedibile con modifiche minime ai flussi di lavoro di sequenziazione precedenti. Inoltre, il Sequencer consente agli utenti di configurare più facilmente le applicazioni per abilitare le connessioni delle applicazioni virtualizzate.

Per un elenco delle modifiche apportate all'App-V 5,1 sequencer, vedere [informazioni su App-v 5,1](about-app-v-51.md).

[Come installare Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)

## <a href="" id="---------app-v-5-1-client-and-sequencer-logs"></a> Client e log sequenziatore di App-V 5,1


Puoi usare le informazioni del log sequencer di App-V 5,1 per risolvere i problemi relativi all'installazione e agli eventi operativi del sequencer durante l'uso di App-V 5,1. Le informazioni del log correlate al sequencer possono essere esaminate con il **Visualizzatore eventi**. Nella riga seguente viene visualizzato il percorso specifico per gli eventi correlati al sequencer:

**Visualizzatore eventi \ \ applicazioni e registri Servizi \ \ Microsoft \ \ App V**. Gli eventi correlati al sequencer sono presospesi con **appv \ _Sequencer**. Gli eventi correlati al client sono presospesi con **appv \ _Client**.

## Altre risorse per la distribuzione di Sequencer e client


[Distribuzione di App-V 5.1](deploying-app-v-51.md)

[Pianificazione di App-V 5.1](planning-for-app-v-51.md)






 

 





