---
title: Come installare Application Virtualization Streaming Server
description: Come installare Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817326"
---
# Come installare Application Virtualization Streaming Server


L'Application Virtualization Streaming Server pubblica le proprie applicazioni ai client. In un ambiente con bilanciamento del carico, tipico delle distribuzioni di grandi dimensioni, tutti i server di un gruppo di server devono eseguire il flusso delle stesse applicazioni. Se i server di streaming di Application Virtualization sono in streaming di applicazioni diverse, assegnare i server a gruppi di server diversi. In questo caso, potrebbe anche essere necessario aumentare la capacità di un gruppo di server.

Se è stato designato un computer di destinazione nella rete, con un account di accesso con privilegi amministrativi locali, è possibile usare la procedura seguente per installare l'Application Virtualization Streaming Server e assegnarlo al gruppo di server appropriato.

**Nota**  La procedura guidata per l'installazione può creare un record del gruppo di server, se non esiste, e un record dell'appartenenza all'Application Virtualization Streaming Server in questo gruppo.

 

Dopo aver completato il processo di installazione, riavviare il server.

**Per installare un Application Virtualization Streaming Server**

1.  Verificare che nel computer di destinazione non siano installate versioni precedenti di Application Virtualization Streaming Server.

    **Importante**  Verificare che App-V Management Server non sia installato nel computer in cui si trova. I due prodotti non possono essere installati nello stesso computer.

     

2.  Passare al percorso del programma di installazione di Application Virtualization System nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic sul file **Setup.exe** .

3.  Nella pagina di **benvenuto** fare clic su **Avanti**.

4.  Nella pagina **contratto di licenza** per accettare le condizioni di licenza selezionare **Accetto i termini e le condizioni**di licenza e quindi fare clic su **Avanti**.

5.  Nella pagina **informazioni cliente** specificare il **nome utente** e l'organizzazione e quindi fare clic su **Avanti**.

6.  Nella pagina **percorso di installazione** fare clic su **Sfoglia**, specificare il percorso in cui si vuole installare il server di streaming e quindi fare clic su **Avanti**.

7.  Nella pagina **modalità di sicurezza della connessione** selezionare il certificato desiderato nell'elenco a discesa e quindi fare clic su **Avanti**.

    **Nota**  L'impostazione **modalità di connessione sicura** richiede al server di eseguire il provisioning di un certificato server da un'infrastruttura a chiave pubblica. Se nel server non è installato un certificato del server, questa opzione non è disponibile e non può essere selezionata. È necessario concedere all'account del servizio di rete l'accesso in lettura al certificato in uso.

     

8.  Nella pagina di **configurazione della porta TCP** , per usare la porta standard (554), selezionare **Usa porta predefinita (554)**. Per specificare una porta personalizzata, selezionare **Usa porta personalizzata**, specificare il numero di porta nel campo specificato e quindi fare clic su **Avanti**.

    **Nota**  Quando si installa il server in uno scenario non sicuro, è possibile usare la porta predefinita (554) oppure definire una porta personalizzata.

     

9.  Nella pagina **radice contenuto** specificare la posizione nel computer di destinazione in cui verranno salvati i file SFT e quindi fare clic su **Avanti**.

    **Nota**  Se la porta HTTP o RTSP per il server di streaming delle applicazioni virtuali è già allocata, verrà richiesto di selezionare una nuova porta. Specificare la porta desiderata e quindi fare clic su **Avanti**.

     

10. Nella schermata **Impostazioni avanzate** immettere le informazioni seguenti:

    1.  **Connessioni client max**

    2.  **Timeout connessione (sec)**

    3.  **Dimensioni del pool di thread RTSP**

    4.  **Timeout RTSP (sec)**

    5.  **Numero di processi principali**

    6.  **Timeout di base (sec)**

    7.  **Abilitare l'autenticazione utente**

    8.  **Abilitare l'autorizzazione dell'utente**

    9.  **Dimensioni blocco cache (KB)**

    10. **Dimensioni massime della cache (MB)**

    **Nota**  App-V Streaming Server usa le autorizzazioni di file system NTFS per controllare l'accesso alle applicazioni sotto la condivisione di contenuto. USA **Abilita l'autenticazione utente** e **Abilita l'autorizzazione dell'utente** per controllare se il server controlla e applica gli elenchi di controllo di accesso (ACL) o meno.

     

11. Nella pagina **pronto per l'installazione del programma** , per avviare l'installazione, fare clic su **Installa**.

12. Nella schermata di **installazione guidata completata** , per chiudere la procedura guidata, fare clic su **fine**.

    **Importante**  L'installazione può richiedere diversi minuti per terminare. Un messaggio di stato lampeggerà sopra l'area di notifica desktop di Windows, indicando che l'installazione è riuscita.

    Non è necessario riavviare il computer quando viene richiesto. Per ottimizzare le prestazioni del sistema, è comunque consigliabile un riavvio.

     

13. Ripetere i passaggi da 1 a 12 per ogni server delle applicazioni virtuali che è necessario installare.

## Argomenti correlati


[Come installare i server e i componenti del sistema](how-to-install-the-servers-and-system-components.md)

 

 





