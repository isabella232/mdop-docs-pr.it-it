---
title: Pianificazione della disponibilità elevata con App-V 5.1
description: Pianificazione della disponibilità elevata con App-V 5.1
author: dansimp
ms.assetid: 1f190a0e-10ee-4fbe-a602-7e807e943033
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c8e0e684051859a4caa2c4ef983c040295bc6d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805008"
---
# Pianificazione della disponibilità elevata con App-V 5.1


Le configurazioni di sistema di Microsoft Application Virtualization (App-V) 5,1 possono sfruttare le opzioni che mantengono un livello elevato di servizio disponibile.

Usare le informazioni nelle sezioni seguenti per comprendere le opzioni per la distribuzione di App-V 5,1 in una configurazione altamente disponibile.

-   [Supporto per il clustering di Microsoft SQL Server](#bkmk-sqlcluster)

-   [Supporto per il bilanciamento del carico di rete IIS](#bkmk-iisloadbal)

-   [Supporto per i file server in cluster durante l'uso della modalità SCS](#bkmk-clusterscsmode)

-   [Supporto per il mirroring di Microsoft SQL Server](#bkmk-sqlmirroring)

-   [Supporto per Microsoft SQL Server sempre attivo](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a>Supporto per il clustering di Microsoft SQL Server


È possibile eseguire il database di gestione e la creazione di report di App-V nei computer che eseguono cluster Microsoft SQL Server. È tuttavia necessario installare i database usando gli script.

Per istruzioni, Vedi [come distribuire i database di App-V usando gli script SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).

## <a href="" id="bkmk-iisloadbal"></a>Supporto per il bilanciamento del carico di rete IIS


Puoi usare Internet Information Services (IIS) Network Load Balancing per configurare un ambiente altamente disponibile per i computer che eseguono App-V 5. x Management, Publishing e Reporting Services distribuiti tramite IIS.

Per altre informazioni sulla configurazione di IIS e del bilanciamento del carico di rete per i computer che eseguono sistemi operativi Windows Server, vedere la seguente procedura:

-   Fornisce informazioni sulla configurazione di Internet Information Services (IIS) 7,0.

    [Ottenere elevata disponibilità e scalabilità-ARR e NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)

-   Configurazione di Microsoft Windows Server

    [Bilanciamento del carico di rete](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .

    Queste informazioni si applicano anche ai cluster di bilanciamento del carico di rete di IIS (NLB) in Windows Server2008, Windows Server2008R2 o Windows Server2012.

    **Nota**  La funzionalità di bilanciamento del carico di rete di IIS in Windows Server2012 è in genere uguale a quella di Windows Server2008R2. Tuttavia, alcuni dettagli dell'attività vengono modificati in Windows Server2012. Per informazioni sulle nuove modalità di attività, vedere [attività di gestione comuni e spostamento in Windows server 2012 R2 Preview e Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .

     

## <a href="" id="bkmk-clusterscsmode"></a>Supporto per i file server in cluster durante l'uso della modalità SCS


È supportata la versione in uso di App-V 5,1 in modalità SCS (Share Content Store) con file server raggruppati.

Per abilitare questa configurazione, è possibile usare la procedura seguente:

-   Configura App-V 5,1 per l'esecuzione in modalità SCS client. Per altre informazioni sulla configurazione della modalità SCS App-V 5,1, vedere [come installare il client App-v 5,1 per la modalità di archiviazione di contenuto condiviso](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).

-   Configurare il cluster di file server configurato sia nella modalità di scalabilità orizzontale di Microsoft Server2012 che in quella pre **2012** con una San virtuale.

Per convalidare la configurazione, è possibile usare la procedura seguente:

1.  Aggiungere un pacchetto nel server di pubblicazione. Per altre informazioni sull'aggiunta di un pacchetto, vedere [come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).

2.  Eseguire un aggiornamento della pubblicazione nel computer che esegue il client App-V 5,1 e aprire un'applicazione.

3.  Cambiare i nodi del cluster durante l'aggiornamento e il Mid-streaming per verificare che il failover funzioni correttamente.

Per altre informazioni sulla configurazione dei cluster di failover di Windows Server, vedere quanto segue:

-   [Elenco di controllo: creare un file server in cluster](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .

-   [Usare volumi condivisi del cluster in un cluster di failover di Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .

## <a href="" id="bkmk-sqlmirroring"></a>Supporto per il mirroring di Microsoft SQL Server


Usando il mirroring di Microsoft SQL Server, in cui il database del server di gestione di App-V 5,1 viene speculato utilizzando due istanze di SQL Server, per i database di App-V 5,1 Management Server è supportato.

Per altre informazioni sulla configurazione del mirroring di Microsoft SQL Server, vedere quanto segue:

-   [Procedura: preparare un database mirror per il mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Stabilire una sessione di mirroring del database usando l'autenticazione di Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)

Per convalidare la configurazione, è possibile usare la procedura seguente:

1.  Avviare una sessione di mirroring di Microsoft SQL Server.

2.  Selezionare **failover** per designare una nuova istanza master di Microsoft SQL Server.

3.  Verificare che il server di gestione di App-V 5,1 continui a funzionare come previsto dopo il failover.

La stringa di connessione nel server di gestione può essere modificata per includere **failover partner &lt; = &gt; Server2**. Ciò sarà utile solo quando il principale mirror non ha superato il controllo secondario e il computer che esegue il client App-V 5,1 sta eseguendo una nuova connessione (ad esempio dopo il riavvio).

Eseguire la procedura seguente per modificare la stringa di connessione in modo da includere il **failover partner = &lt; Server2 &gt; **:

**Importante**  Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema. Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows. Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat). Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti. Cambiare il registro di sistema a proprio rischio.

 

1.  Accedere al server di gestione e aprire **Regedit**.

2.  Passare a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **appv**  \\  **Server**  \\  **ManagementService**.

3.  Modificare il valore di **gestione \ _SQL \ _CONNECTION \ _STRING** con il **partner failover &lt; = &gt; Server2**.

4.  Riavviare il servizio di gestione tramite la console IIS.

    **Nota**  Il mirroring del database è nell'elenco delle caratteristiche deprecate del motore di database per Microsoft SQL Server2012 a causa della funzionalità **AlwaysOn** disponibile in Microsoft sql Server 2012.

     

Per altre informazioni, fare clic su uno dei collegamenti seguenti:

-   [Procedura: preparare un database mirror per il mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .

-   [Procedura: configurare una sessione di mirroring del database (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .

-   [Stabilire una sessione di mirroring del database usando l'autenticazione di Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .

-   [Caratteristiche del motore di database obsolete in SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .

## <a href="" id="bkmk-sqlalwayson"></a>Supporto per Microsoft SQL Server sempre nella configurazione


Il database del server di gestione di App-V 5,1 supporta le distribuzioni nei computer che eseguono Microsoft SQL Server con la configurazione **Always on** .






## Argomenti correlati


[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

 

 





