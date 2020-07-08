---
title: Progettare i repository delle immagini MED-V
description: Progettare i repository delle immagini MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823615"
---
# Progettare i repository delle immagini MED-V


Dopo che le immagini MED-V vengono create e imballate, possono essere archiviate in un file server in qualsiasi posizione. I file possono essere inviati tramite HTTP o HTTPS da uno o più server IIS. Il repository di immagini può essere condiviso da più istanze di MED-V.

Per progettare i repository di immagini, è prima di tutto necessario decidere in che modo verranno distribuite le immagini in ogni client e quindi se tale client richiede un repository di immagini locale. Ogni repository viene quindi progettato e posizionato, insieme al server IIS che lo accompagna.

## Determinare il modo in cui verranno distribuite le immagini


Per ogni area di lavoro MED-V, decidere in che modo pianificare la distribuzione di immagini MED-V nel client. Questo è importante per determinare il numero di repository necessari per archiviare le immagini imballate, in cui verranno posizionati questi repository e quindi per progettare questi repository.

Le immagini imballate possono essere distribuite nei modi seguenti:

-   Scaricati tramite rete da un server di distribuzione delle immagini, che include un file server e un server IIS.

-   Su supporti rimovibili, ad esempio un'unità USB o un DVD.

-   Preallestito in una directory dello Store di immagini nel computer client usando un centro di distribuzione del software aziendale.

Decidi quale metodo o i metodi verranno usati per distribuire le immagini MED-V in ognuno dei client e se la posizione richiederà un repository di immagini.

## Determinare il numero di repository di immagini


Dopo aver determinato il numero minimo di repository necessari, aggiungere altro se si applicano i criteri seguenti:

-   Motivi di organizzazione o di regolamentazione per separare le immagini MED-V: alcune immagini MED-V potrebbero non essere in grado di coesistere nello stesso repository. Ad esempio, i dati personali riservati possono richiedere spazio di archiviazione su un server disponibile solo per un set limitato di dipendenti che hanno bisogno di accedere ai dati.

-   Client in reti isolate: se le immagini verranno distribuite tramite la rete, determinare se le reti sono isolate e richiedono un repository separato. Ad esempio, le organizzazioni spesso isolano le reti Lab dalle reti di produzione.

-   Client in reti remote: se le immagini verranno distribuite tramite la rete, alcuni computer client potrebbero essere separati dal repository da collegamenti di rete con una larghezza di banda insufficiente per offrire un'esperienza adeguata quando un client carica un'area di lavoro MED-V. Se necessario, progetta altre istanze di MED-V per rispondere a questa esigenza.

Aggiungere questi repository alla struttura. Scegliere un nome per ogni repository e il motivo per cui è stato progettato. Decidere quali immagini di MED-V verranno archiviate nei repository e quali client MED-V caricherà aree di lavoro MED-V con immagini del repository.

## Progettare e posizionare i repository di immagini


Quando una nuova immagine è disponibile per i client, i client iniziano a scaricare l'immagine, possibilmente contemporaneamente. In questo modo, viene creata una richiesta elevata nel repository e deve essere presa in considerazione durante la progettazione del repository di immagini.

Per ogni repository, determinare la quantità di dati che verranno archiviati. Sommare le dimensioni delle immagini che verranno archiviate nel repository. Questo è il valore dello spazio su disco necessario nel file server.

Aggiungere quindi il numero di client che possono scaricare le immagini MED-V dal repository. Questo è il numero massimo di download simultanei che possono verificarsi quando viene caricata una nuova immagine MED-V nel repository. Il file server deve essere progettato con un sottosistema di dischi in grado di soddisfare le richieste di i/o che verranno create.

Il repository di immagini può risiedere nello stesso sistema del server MED-V e del server che ha eseguito SQL Server oppure in una condivisione file remota. Puoi anche eseguirlo in una VM di Windows Server2008 Hyper-V. Controllare il percorso di rete dei client che il repository di immagini sarà in grado di gestire e posizionare il repository in un percorso di rete in cui disponga di larghezza di banda sufficiente per soddisfare le aspettative dei livelli di servizio di tali client.

### Tolleranza di errore

Se il repository di immagini non è disponibile, i client non saranno in grado di scaricare immagini MED-V nuove o aggiornate. Per progettare le opzioni di tolleranza d'errore per il file server e i dischi a tolleranza d'errore, vedere la guida alla [pianificazione e alla progettazione dell'infrastruttura Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .

## Progettare e posizionare i server IIS


Questa sezione è pertinente solo se i client scaricheranno i file di immagine tramite la rete tramite HTTP o HTTPS.

Il server IIS può coesistere nello stesso sistema del server MED-V e del server che ha eseguito SQL Server. Può anche essere eseguito in una VM di Windows Server2008 Hyper-V. L'infrastruttura del server IIS deve avere un throughput sufficiente per consegnare le immagini ai client all'interno delle aspettative del livello di servizio dell'organizzazione. Deve essere progettata con un sottosistema di dischi in grado di soddisfare le richieste IO.

Per ogni repository di immagini, sommare il numero di client che possono scaricare immagini MED-V tramite IIS. Questo è il numero massimo di download simultanei che possono verificarsi quando un'immagine viene caricata nel repository. Usare la somma effettiva e le aspettative del livello di servizio determinate in [definire l'ambito del progetto](define-the-project-scope.md) per pianificare la progettazione dell'infrastruttura del server IIS e determinare la quantità di larghezza di banda appropriata da allocare per il repository.

Per progettare l'infrastruttura IIS, vedere la guida alla [pianificazione e progettazione dell'infrastruttura Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

### Tolleranza di errore

Se l'infrastruttura del server IIS non è disponibile, i client non saranno in grado di scaricare immagini nuove o aggiornate. Per configurare la tolleranza di errore, il server IIS basato su Windows Server2008 può essere inserito in un cluster di failover. Per progettare la tolleranza d'errore per l'infrastruttura del server IIS, vedere la guida alla [pianificazione e alla progettazione dell'infrastruttura Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

## Argomenti correlati


[Distribuzione di un'area di lavoro MED-V con un sistema di distribuzione del software aziendale](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[Distribuzione di un'area di lavoro MED-V con un pacchetto di distribuzione](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





