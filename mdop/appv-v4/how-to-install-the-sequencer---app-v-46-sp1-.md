---
title: Come installare il sequencer (App-V 4,6 SP1)
description: Come installare il sequencer (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817275"
---
# Come installare il sequencer (App-V 4,6 SP1)


Microsoft Application Virtualization (App-V) Sequencer monitora e registra il processo di installazione e configurazione per le applicazioni in modo che l'applicazione possa essere eseguita come applicazione virtuale. È necessario installare l'App-V Sequencer in un computer in cui è installato solo il sistema operativo. In alternativa, puoi installare il sequencer in un computer in uso in un ambiente virtuale, ad esempio un computer virtuale. Questo metodo è utile perché è più semplice mantenere un ambiente di sequenziazione pulito che è possibile riutilizzare con una configurazione aggiuntiva minima.

È necessario avere credenziali amministrative nel computer in uso per sequenziare l'applicazione e il computer non deve eseguire alcuna versione di client App-V. La creazione di un'applicazione virtuale tramite App-V Sequencer richiede più operazioni, quindi è importante installare il sequencer in un computer che soddisfi o superi i [requisiti hardware e software di Application Virtualization Sequencer](application-virtualization-sequencer-hardware-and-software-requirements.md).

**Nota**  
L'uso dell'App-V Sequencer in modalità provvisoria non è supportato.



**Per installare Microsoft Application Virtualization Sequencer**

1.  Copiare i file di installazione di Microsoft Application Virtualization Sequencer nel computer in cui si vuole installarlo.

2.  Per avviare l'installazione guidata di Microsoft Application Virtualization Sequencer, fare doppio clic su **Setup.exe**. Se il **pacchetto ridistribuibile Microsoft Visual C++ SP1 (x86)** non viene rilevato prima dell'installazione, fare clic su **Installa** per installare il prerequisito necessario.

3.  Per continuare l'installazione, nella pagina **iniziale** fare clic su **Avanti**.

4.  Per accettare le condizioni del contratto di licenza nella pagina **contratto** di licenza, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.

5.  Nella pagina **cartella di destinazione** , per accettare la cartella di installazione predefinita, fare clic su **Avanti**. Per specificare una cartella di destinazione diversa, fare clic su **Cambia** e specificare la cartella di installazione che verrà usata per l'installazione. Fai clic su **Avanti**.

6.  Nella pagina **Virtual Drive** , per configurare l'unità di **Q:\\** predefinita per la virtualizzazione dell'applicazione (impostazione predefinita) come unità in cui verranno eseguite tutte le applicazioni sequenziate, fare clic su **Avanti**. Se si vuole specificare una lettera di unità diversa, usare l'elenco e selezionare la lettera dell'unità che si vuole usare selezionando la lettera di unità appropriata e quindi fare clic su **Avanti**.

    **Importante**  
    La lettera dell'unità di virtualizzazione dell'applicazione specificata con questo passaggio è la lettera dell'unità in cui verranno eseguite le applicazioni virtuali nei computer di destinazione. La lettera dell'unità specificata deve essere disponibile e non attualmente in uso nei computer che eseguono il client App-V. Se l'unità specificata è già in uso, l'applicazione virtuale non riesce nel computer di destinazione.



7.  Nella pagina **pronto per l'installazione del programma** , per avviare l'installazione, fare clic su **Installa**.

8.  Nella pagina **completamento guidata InstallShield** , per chiudere l'installazione guidata e aprire App-V Sequencer, fare clic su **fine**. Per chiudere l'installazione guidata senza aprire il sequencer, deselezionare **Avvia il programma**e quindi fare clic su **fine**.

    **Nota**  
    Se l'App-V Sequencer è stato installato in un computer che gestisce un ambiente virtuale, ad esempio una macchina virtuale, ora è necessario eseguire uno snapshot. Dopo aver sequenziato un'applicazione, è possibile tornare a questa immagine, in modo da poter sequenziare l'applicazione successiva.



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## Argomenti correlati


[Configurazione di Application Virtualization Sequencer (App-V 4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









