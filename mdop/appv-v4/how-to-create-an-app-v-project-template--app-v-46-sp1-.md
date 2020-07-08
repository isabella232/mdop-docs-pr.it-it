---
title: Come creare un modello di progetto di App-V (App-V 4.6 SP1)
description: Come creare un modello di progetto di App-V (App-V 4.6 SP1)
author: dansimp
ms.assetid: 7e87fba2-b72a-4bc9-92b8-220e25aae99a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e264d5c41b663bc9c450dc642e2b26297ee7ea1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817646"
---
# Come creare un modello di progetto di App-V (App-V 4.6 SP1)


Puoi usare un modello di progetto App-V per salvare le impostazioni comunemente applicate associate a un pacchetto di applicazione virtuale esistente. Queste impostazioni possono quindi essere applicate quando crei nuovi pacchetti di applicazioni virtuali nell'ambiente che possono semplificare il processo di creazione di pacchetti di applicazioni virtuali.

**Nota**  Puoi applicare un modello di progetto App-V solo quando crei un nuovo pacchetto di applicazione virtuale. L'applicazione di modelli di progetto a pacchetti di applicazioni virtuali esistenti non è supportata.

 

Per altre informazioni sull'applicazione di un modello di progetto App-V, vedere [come applicare un modello di progetto App-v (app-v 4,6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md).

I modelli di progetto di App-V si differenziano dagli acceleratori delle applicazioni App-v perché i tasti di scelta rapida dell'applicazione App-V sono specifici dell'applicazione e i modelli di progetto App-V possono essere applicati a più applicazioni. Non è inoltre possibile usare un modello di progetto quando si usa un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale.

Le impostazioni generali seguenti vengono salvate con un modello di progetto App-V:

-   **Opzioni di monitoraggio avanzate**. Consente l'esecuzione di Microsoft Update durante il monitoraggio, rebase **. dll**.

-   **Impostazioni di distribuzione del pacchetto**. Contiene **protocollo**, **nome host**, **porta**, **percorso**, **sistemi operativi**, **applica descrittori di sicurezza**, **Crea MSI**, **Comprimi pacchetto**.

-   **Opzioni generali**. Consente di generare il pacchetto di **Microsoft Windows Installer (MSI)** , **consentire la virtualizzazione degli eventi**, **consentire la virtualizzazione dei servizi**, **aggiungere la versione del pacchetto al nome del file**.

-   **Elementi di esclusione**. Contiene l'elenco dei criteri di esclusione.

**Per creare un modello di progetto**

1.  Per avviare l'app-v sequencer, nel computer che sta usando l'app-v Sequencer fare clic su **Avvia**tutti i programmi Microsoft Application Virtualization  /  **All Programs**  /  **Microsoft Application Virtualization**  /  **sequencer**.

2.  Se il pacchetto di applicazione virtuale è attualmente aperto in App-V Sequencer, passare al passaggio 3 di questa procedura. Per aprire il pacchetto di applicazione virtuale esistente che contiene le impostazioni che si vuole salvare con il modello di progetto App-V, fare clic su **file**  /  **aperto** e quindi su **modifica** **pacchetto**. Nella pagina **Seleziona pacchetto** fare clic su **Sfoglia** e individuare il pacchetto di applicazione virtuale che si vuole aprire. Fai clic su **Modifica**.

3.  Nella console App-V Sequencer fare clic su **file**  /  **Salva come modello**. Dopo aver esaminato le impostazioni che verranno salvate con il nuovo modello, fare clic su **OK**. Specifica un nome che verrà associato al nuovo modello di progetto App-V. Fare clic su **Save**.

    Il nuovo modello di progetto App-V viene salvato nella directory specificata nel passaggio 3 di questa procedura.

## Argomenti correlati


[Attività per Application Virtualization Sequencer (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[Come applicare un modello di progetto di App-V (App-V 4.6 SP1)](how-to-apply-an-app-v-project-template--app-v-46-sp1-.md)

 

 





