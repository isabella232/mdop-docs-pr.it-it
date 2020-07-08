---
title: Come aggiungere un pacchetto
description: Come aggiungere un pacchetto
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821396"
---
# Come aggiungere un pacchetto


È possibile aggiungere un pacchetto dalla console di gestione di Application Virtualization Server nei modi seguenti:

-   Importa un'applicazione, che crea il pacchetto automaticamente nel processo.

-   Aggiungere un pacchetto manualmente.

È consigliabile importare le applicazioni invece di aggiungerle manualmente. Per altre informazioni sull'importazione di applicazioni, vedere [come importare un'applicazione](how-to-import-an-applicationserver.md).

**Per aggiungere un pacchetto manualmente**

1.  Nella console di gestione di Application Virtualization Server fare clic con il pulsante destro del mouse sul nodo **pacchetti** nel riquadro sinistro e scegliere **nuovo pacchetto**.

2.  Nella finestra di dialogo **nuovo pacchetto** Digitare un nome nel campo **nome pacchetto** .

3.  Cercare o digitare un nome di percorso nel campo **percorso completo per il file del pacchetto** . Questo deve essere un file SFT.

    **Nota**  Se si passa al file SFT, sostituire il percorso locale, ad esempio C:\\Programmi Files\\User\ _Apps \\Virtual\ _App \ _Server \\Content) con il nome host statico o l'indirizzo IP del server. L'uso della variabile *% sft \ _SOFTGRIDSERVER%* richiede la configurazione del computer per client.

    Nelle finestre di dialogo che fanno riferimento a server delle applicazioni virtuali, è necessario usare un percorso di rete, ad esempio il nome host statico o l'indirizzo IP del server, a cui gli utenti possono accedere. Il file OSD (Open Software Descriptor) dell'applicazione può sostituire la variabile segnaposto *% sft \ _SOFTGRIDSERER%* con il nome host statico del server o l'indirizzo IP. Se si lascia la variabile segnaposto, è necessario impostare questa variabile su ogni computer client che accederà al server. Impostare un utente o una variabile di sistema in ogni computer per SFT \ _SOFTGRIDSERVER. Il valore della variabile deve essere il nome host statico o l'indirizzo IP del server. Se si imposta una variabile, si esce dalla sessione client, si disconnette e si torna in Microsoft Windows e quindi si riavvia la sessione in ogni computer in cui è stata eseguita una sessione ed è stata impostata la variabile.

     

4.  Fai clic su **Avanti**.

5.  La finestra di dialogo **Riepilogo** Mostra il percorso del file e chiede di copiare il file nella posizione se non è già stato fatto. Dopo aver verificato le informazioni, fare clic su **fine** .

    **Nota**  Se si gestiscono applicazioni in un server remoto, nella finestra di dialogo successiva digitare solo il percorso del file relativo alla radice del contenuto del server.

     

## Argomenti correlati


[Come importare un'applicazione](how-to-import-an-applicationserver.md)

[Come gestire i pacchetti in Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





