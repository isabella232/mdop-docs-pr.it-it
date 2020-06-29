---
title: Come installare manualmente Application Virtualization Client
description: Come installare manualmente Application Virtualization Client
author: dansimp
ms.assetid: bb67f70b-d525-4317-b254-e4f084c717ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cb41b5e51bd33c377b17c088e97cb54f1a57685
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817085"
---
# Come installare manualmente Application Virtualization Client

Esistono due tipi di componenti client per la virtualizzazione dell'applicazione: il client Desktop Application Virtualization, progettato per l'installazione nei computer desktop, e il client di virtualizzazione dell'applicazione per Servizi Desktop remoto (in precedenza Servizi terminal), che è possibile installare nei server Host sessione Desktop remoto. Anche se i due programmi di installazione client sono diversi, è possibile usare la procedura seguente per installare manualmente il client Desktop Application Virtualization in un singolo computer desktop o nel client di Application Virtualization per Servizi Desktop remoti in un singolo server Host sessione Desktop remoto. In un ambiente di produzione è molto probabile che si installerà il client Desktop Application Virtualization in più computer desktop con un processo di installazione automatizzato con script. Per informazioni su come installare più client usando un processo di installazione con script, vedere [come installare il client tramite la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md).

**Nota**  
1. Se si sta installando il client di Application Virtualization per il software di Servizi Desktop remoto in un server Host sessione RD, consigliare gli utenti che dispongono di una sessione client RDP o ICA aperta con il server Host sessione RD che devono salvare il lavoro e chiudere le sessioni. In una sessione Desktop remoto è possibile installare il client manualmente. Per altre informazioni sull'aggiornamento del client, vedere [come aggiornare l'Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).

2. Se nel computer dell'utente è installata qualsiasi configurazione che dipende dal percorso di installazione del client, tenere presente che il client di Application Virtualization (App-V) 4,5 usa una cartella di installazione diversa rispetto alle versioni precedenti. Per impostazione predefinita, una nuova installazione del client di Application Virtualization (App-V) 4,5 verrà installata nella cartella client Application Virtualization cartella \\Programmi\\microsoft. Se una versione precedente del client è già installata, l'installazione del client App-V eseguirà un aggiornamento nella cartella di installazione esistente.

**Nota**  
Per App-V versione 4,6 e versioni successive, quando è installato App-V client, SFTLDR.DLL viene installato nella directory Windows\\system32. Se l'App-V client è installata in un sistema a 64 bit, SFTLDR\_WOW64.DLL viene installata nella directory Windows\\SysWOW64

**Per installare manualmente Application Virtualization Desktop client**

1. Dopo aver ottenuto il file di archivio del programma di installazione corretto e averlo salvato nel computer, verificare di avere effettuato l'accesso con un account con diritti di amministratore nel computer e fare doppio clic sul file per espandere l'archivio.

2. Scegliere la cartella in cui salvare i file e quindi aprire la cartella dopo che i file sono stati copiati.

3. Esaminare le note sulla versione, se necessario.

4. Individuare il file setup.exe e fare doppio clic su setup.exe per avviare l'installazione.

5. La procedura guidata controlla il sistema per verificare che sia installato tutto il software prerequisito e, se manca una delle opzioni seguenti, la procedura guidata chiederà automaticamente di installarle:

    - Pacchetto ridistribuibile di Microsoft Visual C++ 2005 SP1 (x86)

    - Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)

    - Segnalazione errori applicazione Microsoft

    **Nota**  
    Per App-V versione 4,6 e successive, la procedura guidata installerà anche Microsoft Visual C++ 2008 SP1 Redistributable Package (x86).

    Per altre informazioni sull'installazione di Microsoft Visual C++ 2008 SP1 Redistributable Package (x86), vedere [https://go.microsoft.com/fwlink/?LinkId=150700](https://go.microsoft.com/fwlink/?LinkId=150700) .

    Se richiesto, fare clic su **Installa**. Lo stato di avanzamento dell'installazione viene visualizzato e lo stato viene modificato da **in sospeso** a **installazione**. Lo stato di installazione viene modificato in **riuscito** Man mano che ogni passaggio viene completato correttamente.

6. Quando viene visualizzato **Microsoft Application Virtualization Desktop client-InstallShield Wizard** , fare clic su **Avanti**.

7. Viene visualizzata la schermata **contratto di licenza** . Leggere il contratto di licenza e, se si è d'accordo, fare clic su **Accetto i termini del contratto di licenza** e quindi fare clic su **Avanti**.

   Facoltativamente, è possibile fare clic sul pulsante per leggere l'informativa sulla privacy. Per accedere all'informativa sulla privacy, è necessario essere connessi a Internet.

8. Nella schermata **Imposta tipo** selezionare il tipo di configurazione. Fare clic su **tipico** per usare i valori di programma predefiniti oppure fare clic su **personalizzato** per configurare le impostazioni del programma durante l'installazione.

9. Se si sceglie **tipico**, la schermata successiva verrà visualizzata **pronta per l'installazione del programma**. Fare clic su **Installa** per avviare l'installazione.

10. Se si sceglie **personalizzato**, viene visualizzata la schermata **cartella di destinazione** .

11. Nella schermata della **cartella di destinazione** , fare clic su **Avanti** per accettare la cartella predefinita o su **Cambia** per visualizzare la schermata **Cambia cartella di destinazione corrente** . Passare a oppure, nel campo **nome cartella** , immettere la cartella di destinazione, fare clic su **OK**e quindi su **Avanti**.

12. Nella schermata **posizione dei dati di virtualizzazione dell'applicazione** fare clic su **Avanti** per accettare i percorsi di dati predefiniti oppure completare le azioni seguenti per modificare il punto in cui vengono archiviati i dati:

    1. Fare clic su **Cambia**e quindi selezionare o, nel campo **percorso dati globale** , immettere la cartella di destinazione per il percorso dati globale e fare clic su **OK**. La directory globale dei dati è la posizione in cui il client Desktop Application Virtualization memorizza nella cache i dati condivisi da tutti gli utenti nel computer, come i file OSD e i dati del file SFT.

    2. Se si vuole cambiare la lettera dell'unità da usare, selezionare la lettera di unità preferita nell'elenco a discesa.

    3. Immettere un nuovo percorso in cui archiviare i dati specifici dell'utente nel campo della **posizione dei dati specifici degli utenti** , se si vuole modificare la posizione dei dati. La directory dati utente è la posizione in cui il client Desktop Application Virtualization archivia informazioni specifiche dell'utente, come le impostazioni personali per le applicazioni virtualizzate.

       **Nota**  
       Questo percorso deve essere diverso per ogni utente, quindi deve includere una variabile di ambiente specifica dell'utente o un'unità mappata o qualcos'altro che si risolverà in un percorso univoco per ogni utente.

    4. Dopo aver completato le modifiche, fare clic su **Avanti**.

13. Nella schermata **Impostazioni dimensione cache** è possibile accettare o modificare le dimensioni predefinite della cache. Fare clic su uno dei pulsanti di opzione seguenti per scegliere come gestire lo spazio della cache:

    1. **Usare le dimensioni massime della cache**. Immettere un valore numerico da 100-1048576 (1 TB) nel campo **dimensione massima (MB)** per specificare le dimensioni massime della cache.

    2. **Usare la soglia di spazio libero su disco**. Immettere un valore numerico per specificare la quantità di spazio disponibile su disco, in MB, che il client di virtualizzazione dell'applicazione deve uscire dal disco. In questo modo la cache si svilupperà finché la quantità di spazio libero su disco raggiunge questo limite. Il valore visualizzato nello **spazio disponibile su disco rimanente** indica la quantità di spazio su disco attualmente inutilizzata.

    **Importante**  
    Per assicurarti che la cache disponga di spazio sufficiente per tutti i pacchetti che potrebbero essere distribuiti, usa l'impostazione **USA soglia di spazio libero su disco** quando configuri il client in modo che la cache possa crescere in base alle esigenze. In alternativa, determinare in anticipo la quantità di spazio su disco necessaria per la cache di App-V e, al momento dell'installazione, impostare le dimensioni della cache di conseguenza. Per altre informazioni sulla funzionalità di gestione dello spazio della cache, nella Guida alle operazioni di Microsoft Application Virtualization (App-V), vedere **come usare la caratteristica Gestione spazio cache**.

    Fai clic su **Next** per continuare.

14. Nelle sezioni seguenti della schermata di **configurazione dei criteri del pacchetto di runtime** è possibile modificare i parametri che influiscono sul funzionamento del client di virtualizzazione dell'applicazione durante il periodo di esecuzione:

    1. **Radice dell'origine dell'applicazione**. Specifica la posizione dei file SFT. Se usato, esegue l'override del protocollo, del server e delle parti della porta dell'URL di CODEBASE HREF nel file OSD.

    2. **Autorizzazione dell'applicazione**. Quando si **richiede l'autorizzazione dell'utente anche quando la cache** è selezionata, gli utenti devono connettersi a un server e convalidare le proprie credenziali almeno una volta prima di consentire l'avvio di ogni applicazione virtuale.

    3. **Consenti lo streaming da file**. Indica se il flusso da file verrà abilitato, indipendentemente dal modo in cui viene usato il campo **radice dell'origine dell'applicazione** . Se non è selezionato, lo streaming da file è disabilitato. Questa operazione deve essere selezionata se la **radice dell'origine dell'applicazione** contiene un percorso UNC nel formato \\\\server\\share.

    4. **Caricare automaticamente l'applicazione**. Controlla quando e come viene eseguito il caricamento in background automatico delle applicazioni.

       **Nota**  
       Quando si installa il client App-V da usare con una cache di sola lettura, ad esempio con un'implementazione del server VDI, impostare le **applicazioni da caricare** automaticamente in modo da evitare il caricamento automatico delle **applicazioni** per impedire al client di provare ad aggiornare le applicazioni nella cache di sola lettura.

    Fai clic su **Next** per continuare.

15. Nella schermata del **server di pubblicazione** selezionare la casella di controllo **configura un server di pubblicazione ora** se si vuole definire un server di pubblicazione oppure fare clic su **Avanti** se si vuole completare la procedura in un secondo momento. Per definire un server di pubblicazione, specificare le informazioni seguenti:

    1. **Nome visualizzato**: immettere il nome che si vuole visualizzare per il server.

    2. **Tipo**: selezionare il tipo di server nell'elenco a discesa dei tipi di server.

    3. **Host name** and **Port**: immettere il nome host e la porta nei campi corrispondenti. Quando si seleziona un tipo di server nell'elenco a discesa, il campo della porta verrà automaticamente compilato con i numeri di porta standard. Per cambiare un numero di porta, fare clic sul tipo di server nell'elenco e modificare il numero di porta in base alle proprie esigenze.

    4. **Path**: se è stato selezionato un server **http standard** o un **Server http di sicurezza avanzato**, è necessario immettere il percorso completo del file XML contenente i dati di pubblicazione in questo campo. Se si seleziona **Application Virtualization Server** o **Enhanced Security Application Virtualization Server**, questo campo non è attivo.

    5. **Contattare automaticamente il server per aggiornare le impostazioni quando un utente**effettua l'accesso, selezionare questa casella di controllo se si vuole che il server venga interrogato automaticamente quando gli utenti accedono al proprio account nel client di virtualizzazione dell'applicazione.

    6. Al termine della procedura di configurazione, fare clic su **Avanti**.

16. Nella schermata **pronto per l'installazione** fare clic su **Installa**. Viene visualizzata una schermata che mostra lo stato di avanzamento dell'installazione.

17. Nella schermata di **installazione guidata completata** fare clic su **fine**.

    **Nota**  
    Se l'installazione non riesce per qualsiasi motivo, potrebbe essere necessario riavviare il computer prima di provare di nuovo l'installazione.

## Argomenti correlati

[Come installare il client usando la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md)

[Panoramica dello scenario di recapito autonomo](stand-alone-delivery-scenario-overview.md)
