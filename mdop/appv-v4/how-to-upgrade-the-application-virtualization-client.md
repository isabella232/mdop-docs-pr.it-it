---
title: Come aggiornare Application Virtualization Client
description: Come aggiornare Application Virtualization Client
author: dansimp
ms.assetid: 2a75d8b5-da88-456c-85bb-f5bd3d470f7f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b9748fbdba7c8d2777a06c93295e4582be784dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816455"
---
# Come aggiornare Application Virtualization Client


Puoi usare le procedure seguenti per aggiornare il client Desktop Application Virtualization (App-V) o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal). È possibile aggiornare il client installando una nuova versione nella versione precedente installata in precedenza. Quando si aggiornano i client, il software di installazione mantiene automaticamente e esegue la migrazione delle impostazioni dell'utente per le applicazioni virtuali. Per eseguire il programma di installazione sono necessari diritti amministrativi.

**Nota**  Durante l'aggiornamento a Application Virtualization (App-V) 4.5 o versioni successive, le autorizzazioni per la chiave del registro di sistema HKCU vengono modificate. Per questo motivo, gli utenti perderebbero le configurazioni utente impostate in precedenza, ad esempio le impostazioni della modalità disconnessa configurate dall'utente. Se l'utente non è stato limitato attivamente dalla configurazione del comportamento dell'interfaccia utente del client tramite un blocco delle autorizzazioni, l'utente può reimpostare queste preferenze dopo un aggiornamento della pubblicazione.

 

**Importante**  Quando si esegue l'aggiornamento alla versione 4.6 o a una versione successiva del client App-V, è necessario usare il programma di installazione corretto per il sistema operativo del computer, 32 bit o 64 bit. L'installazione non riesce e verrà visualizzato un messaggio di errore se si usa il programma di installazione errato.

 

**Per aggiornare il client Desktop Application Virtualization**

1.  Chiudere tutte le applicazioni virtuali, fare clic con il pulsante destro del mouse sull'icona client desktop dell'App-V visualizzata nell'area di notifica desktop di Windows e scegliere **Exit** per arrestare il client esistente.

2.  Dopo aver ottenuto il file di archivio del programma di installazione corretto e averlo salvato nel computer, fare doppio clic su di esso per espandere l'archivio.

3.  Individuare il file setup.exe e fare doppio clic su setup.exe per avviare l'installazione.

4.  La procedura guidata controlla che il sistema assicuri che sia installato tutto il software prerequisito e chiederà di installare una delle opzioni seguenti, se mancanti:

    -   Microsoft VisualC + + 2005SP1 Redistributable Package (x86)

    -   Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

    -   Segnalazione errori applicazione Microsoft

    **Nota**  Per la versione 4.6 e successive, la procedura guidata installerà anche il seguente requisito software:

    -   Microsoft VisualC + + 2008SP1 Redistributable Package (x86)

     

5.  Fai clic su **Installa**. Lo stato di avanzamento dell'installazione viene visualizzato e lo stato viene modificato da **in sospeso** a **installazione**. Lo stato di installazione viene modificato in **riuscito** Man mano che ogni passaggio viene completato correttamente.

6.  Quando viene visualizzata la finestra di dialogo **client di Application Virtualization Desktop** e viene visualizzato un messaggio che indica che è stata trovata una versione precedente del client nel computer, fare clic su **Avanti** per eseguire l'aggiornamento alla nuova versione.

7.  Quando viene visualizzata la schermata del **contratto di licenza** , leggere il contratto di licenza e, se si è d'accordo, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.

8.  Quando la procedura guidata InstallShield Visualizza la schermata **pronto per l'aggiornamento della** finestra di dialogo programma, fare clic su **Aggiorna** per iniziare l'aggiornamento. La schermata successiva indica che il client è in fase di installazione.

    **Avviso**  Se il programma client non è stato arrestato nel passaggio 1, è possibile che venga visualizzato un messaggio **di avviso in uso** . In questo caso, fai clic con il pulsante destro del mouse sull'icona del client App-V visualizzata nell'area di notifica desktop e seleziona **Esci** per arrestare il client esistente. Quindi fare clic su **Riprova** per continuare.

     

9.  Quando l'installazione viene completata correttamente, verrà richiesto di riavviare il computer. È necessario riavviare il computer per completare l'installazione.

    **Attenzione**  Se l'aggiornamento non riesce per qualsiasi motivo, sarà necessario riavviare il computer prima di riprovare l'aggiornamento.

     

**Per aggiornare l'Application Virtualization Client tramite la riga di comando**

1.  Se si esegue l'aggiornamento del client App-V tramite il programma setup.msi, verificare che sia stato installato il software necessario per i prerequisiti.

    **Importante**  
    -   Per la versione 4.6 e successive del client App-V, il programma setup.msi controlla il sistema e non riesce con un messaggio di errore che indica che l'installazione non può continuare se il software prerequisito non è installato.

    -   Per App-V versione 4.6, i parametri della riga di comando non possono essere usati durante l'aggiornamento e verranno ignorati.

     

2.  L'esempio della riga di comando seguente usa il file setup.msi per aggiornare il client App-V. Sarà necessario usare il programma di installazione client corretto a seconda che si stia aggiornando il client Desktop App-V o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal).

    **msiexec.exe/i "setup.msi"**

    **Importante**  Le virgolette sono obbligatorie solo quando il valore contiene uno spazio. Per coerenza, tutte le istanze nell'esempio precedente vengono visualizzate come virgolette.

     

**Per aggiornare l'Application Virtualization Client per Servizi Desktop remoto**

1.  Seguire i criteri standard dell'organizzazione per l'installazione o l'aggiornamento delle applicazioni nel server Host sessione Desktop remoto (host RDSession). Se il sistema fa parte di una farm, rimuovere l'host RDSession dalla server farm.

2.  Per aggiornare il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal), è necessario usare la riga di comando perché non è possibile aggiornare il client manualmente nell'host RDSession.

    **Nota**  In App-V versione 4,6 e versioni successive, oltre a usare la riga di comando per aggiornare il client, è anche possibile usare una sessione Desktop remoto. Per avviare la sessione Desktop remoto non è necessario alcun parametro speciale.

     

3.  Dopo il completamento dell'aggiornamento del client per Servizi Desktop remoto, riavviare e accedere all'host RDSession.

4.  Dopo aver riavviato il sistema, aggiungere il server alla server farm.

    **Attenzione**  Se l'aggiornamento non riesce per qualsiasi motivo, sarà necessario riavviare il computer prima di riprovare l'aggiornamento.

     

## Argomenti correlati


[Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





