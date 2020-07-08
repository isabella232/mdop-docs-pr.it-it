---
title: Come sequenziare una nuova applicazione con App-V 5.0
description: Come sequenziare una nuova applicazione con App-V 5.0
author: dansimp
ms.assetid: a263fa84-cd6d-4219-a5c2-eb6a553b826c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 13fdda066f79d918da1970e0cab6c1d6e60f6585
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805188"
---
# Come sequenziare una nuova applicazione con App-V 5.0


**Per eseguire una revisione o una procedura prima di iniziare la sequenziazione**

1.  Determinare il tipo di pacchetto di applicazione virtualizzato che si vuole creare:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo di applicazione</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Standard</p></td>
    <td align="left"><p>Crea un pacchetto che contiene un'applicazione o una famiglia di applicazioni. Questa è l'opzione preferita per la maggior parte dei tipi di applicazione.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Componente aggiuntivo o plug-in</p></td>
    <td align="left"><p>Crea un pacchetto che estende la funzionalità di un'applicazione standard, ad esempio un plug-in per Microsoft Excel. È inoltre possibile usare i plug-in per le applicazioni installate nativamente o per un altro pacchetto collegato tramite i gruppi di connessioni.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Middleware</p></td>
    <td align="left"><p>Crea un pacchetto richiesto da un'applicazione standard, ad esempio Java. I pacchetti middleware vengono usati per il collegamento ad altri pacchetti usando i gruppi di connessioni.</p></td>
    </tr>
    </tbody>
    </table>



2.  Copiare tutti i file di installazione necessari nel computer in cui è in corso il sequencer.

3.  Creare un'immagine di backup dell'ambiente virtuale prima di sequenziare un'applicazione e quindi ripristinare l'immagine ogni volta che si termina la sequenziazione di un'applicazione.

4.  Esaminare gli elementi seguenti:

    -   Se un programma di installazione dell'applicazione cambia l'accesso alla sicurezza a un file o a una directory esistente o nuova, le modifiche non vengono acquisite nel pacchetto.

    -   Se i percorsi brevi sono stati disabilitati per il volume di destinazione del pacchetto virtualizzato, è necessario anche sequenziare il pacchetto su un volume creato ed è ancora disabilitato il Short-Path. Non può essere il volume di sistema.

    -   A partire da App-V 5,0 SP3, la directory principale dell'applicazione virtuale (PVAD) è nascosta, ma è possibile riattivarla. Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).

**Per sequenziare una nuova applicazione standard**

1.  Nel computer che esegue il Sequencer fare clic su **tutti i programmi**e quindi su **Microsoft Application Virtualization**e quindi su **Microsoft Application Virtualization Sequencer**.

2.  Nel Sequencer fare clic su **Crea un nuovo pacchetto di applicazione virtuale**. Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.

3.  Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o può causare il pacchetto per contenere dati non necessari. Devi risolvere tutti i potenziali problemi prima di continuare. Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

    **Importante**  
    Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer per verificare che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.



4.  Nella pagina **tipo di applicazione** fare clic sulla casella di controllo **applicazione standard (impostazione predefinita)** e quindi fare clic su **Avanti**.

5.  Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione.

    **Nota**  
    Se il programma di installazione dell'applicazione specificato modifica l'accesso alla sicurezza a un file o una directory, esistente o nuova, le modifiche associate non verranno acquisite nel pacchetto.



~~~
If the application does not have an associated installer file and you plan to run all installation steps manually, select the **Perform a Custom Installation** check box, and then Click **Next**.
~~~

6. Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto. Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto. Il nome del pacchetto viene visualizzato nella console di gestione di App-V 5,0.

   Nella **directory principale dell'applicazione virtuale** viene visualizzato il percorso in cui verrà installata l'applicazione nei computer di destinazione. Per specificare questa posizione, selezionare **Sfoglia**.

   **Nota**  
   A partire da App-V 5,0 SP3, la directory principale dell'applicazione virtuale (PVAD) è nascosta, ma è possibile riattivarla. Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).



~~~
**Important**  
The primary application virtual directory should match the installation location for the application that is being sequenced. For example, if you install Notepad to **C:\\Program Files\\Notepad**; you should configure **C:\\Program Files\\Notepad** as your primary virtual directory. Alternatively, you can choose to set **C:\\Notepad** as the primary virtual application directory, as long as during installation time, you configure the installer to install to **C:\\Notepad**. Editing the Application Virtualization path is an advanced configuration task. For most applications, the default path is recommended for the following reasons:

-   Application Compatibility. Some virtualized applications will not function correctly, or will fail to open if the directories are not configured with identical virtual directory paths.

-   Performance. Since no file system redirection is required, the runtime performance can improve.



**Tip**  
It is recommended that prior to Sequencing an application, you open the associated installer to determine the default installation directory, and then configure that location as the **Primary Virtual Application Directory**.



Click **Next**.
~~~

7. Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, è possibile procedere con l'installazione dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione.

   **Importante**  
   È consigliabile installare le applicazioni sempre in un percorso sicuro e assicurarsi che nessun altro utente abbia effettuato l'accesso al computer che esegue il sequencer durante il monitoraggio.



~~~
Use the application's installation process to perform the installation. If additional installation files must be run as part of the installation, click **Run** to locate and run the additional installation files. When you are finished with the installation, select **I am finished installing**. Click **Next**.
~~~

8. Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazioni virtualizzate.

9. Nella pagina **Configura software** eseguire facoltativamente i programmi contenuti nel pacchetto. Questo passaggio consente di completare tutte le attività necessarie per la licenza o la configurazione prima di distribuire ed eseguire il pacchetto nei computer di destinazione. Per eseguire contemporaneamente tutti i programmi, selezionare almeno un programma e quindi fare clic su **Esegui tutto**. Per eseguire programmi specifici, selezionare il programma o i programmi e quindi fare clic su **Esegui selezionato**. Completare le attività di configurazione necessarie e quindi chiudere le applicazioni. Potrebbe essere necessario attendere diversi minuti per l'esecuzione di tutti i programmi.

   **Nota**  
   Per eseguire le attività di primo utilizzo per qualsiasi applicazione che non è disponibile nell'elenco, aprire l'applicazione. Le informazioni associate verranno acquisite durante questo passaggio.



~~~
Click **Next**.
~~~

10. Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtualizzato appena sequenziato. In **altre informazioni**, fare doppio clic su un evento per ottenere informazioni più dettagliate. Per continuare, fare clic su **Avanti**.

11. Viene visualizzata la pagina **Personalizza** . Se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 14 di questa procedura. Per eseguire una delle personalizzazioni seguenti, selezionare **Personalizza**.

    -   Preparare il pacchetto virtuale per lo streaming. Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione.

    -   Specifica i sistemi operativi che possono eseguire questo pacchetto.

    Fai clic su **Avanti**.

12. Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni e quindi fare clic su **Avanti**.

   **Nota**  
   Se non si aprono applicazioni durante questo passaggio, il metodo di flusso predefinito è il recapito dello streaming su richiesta. Questo significa che le applicazioni verranno scaricate bit per bit finché non sarà possibile aprirle e quindi, a seconda del modo in cui il caricamento in background è configurato, verrà caricato il resto dell'applicazione.



13. Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto. Per consentire l'esecuzione di questo pacchetto in tutti i sistemi operativi supportati nell'ambiente, selezionare **Consenti questo pacchetto per l'esecuzione in qualsiasi sistema operativo**. Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare **Consenti questo pacchetto per l'esecuzione solo nei sistemi operativi seguenti** e selezionare i sistemi operativi che possono eseguire questo pacchetto. Fai clic su **Avanti**.

   **Importante**  
   Verificare che i sistemi operativi specificati in questo articolo siano supportati dall'applicazione che si sta sequenziando.



14. Viene visualizzata la pagina **Crea pacchetto** . Per modificare il pacchetto senza salvarlo, selezionare **continua per modificare il pacchetto senza salvarlo con l'editor di pacchetti**. Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

   Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto ora** (impostazione predefinita). Aggiungere **Commenti** facoltativi da associare al pacchetto. I commenti sono utili per identificare la versione del programma e altre informazioni sul pacchetto.

   **Importante**  
   Il sistema non supporta i caratteri non stampabili nei **Commenti** e nelle **descrizioni**.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

15. Viene visualizzata la pagina **completamento** . Esaminare le informazioni nel riquadro del **report pacchetto applicazione virtuale** in base alle esigenze, quindi fare clic su **Chiudi**. Queste informazioni sono disponibili anche nel file **Report.xml** che si trova nella directory in cui è stato creato il pacchetto.

   Il pacchetto è ora disponibile nel sequencer.

   **Importante**  
   Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.



**Per sequenziare un'applicazione per il componente aggiuntivo o il plug-in**

1.  

    **Nota**  
    Prima di eseguire la procedura seguente, installare l'applicazione padre localmente nel computer in cui è in esecuzione Sequencer. Oppure, se l'applicazione padre è virtualizzata, è possibile eseguire la procedura descritta nel flusso di lavoro del componente aggiuntivo o del plug-in per decomprimere l'applicazione padre nel computer.

    Ad esempio, se si esegue la sequenziazione di un plug-in per Microsoft Excel, installare Microsoft Excel localmente nel computer in cui è in corso il sequencer. Installare inoltre l'applicazione padre nella stessa directory in cui è installata l'applicazione nei computer di destinazione. Se il plug-in o il componente aggiuntivo verrà usato con un pacchetto di applicazione virtuale esistente, installare l'applicazione nella stessa unità di applicazione virtuale usata quando è stato creato il pacchetto dell'applicazione virtuale padre.



~~~
On the computer that runs the sequencer, click **All Programs**, and then Click **Microsoft Application Virtualization**, and then click **Microsoft Application Virtualization Sequencer**.
~~~

2. *<strong><em>Nel Sequencer fare clic su * </em> creare un nuovo pacchetto di applicazione virtuale </strong> . Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.

3. Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o potrebbero causare il pacchetto per contenere dati non necessari. Devi risolvere tutti i potenziali problemi prima di continuare. Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

   **Importante**  
   Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer per verificare che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.



4. Nella pagina **tipo di applicazione** selezionare **componente aggiuntivo o plug-in**e quindi fare clic su **Avanti**.

5. Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per il componente aggiuntivo o il plug-in. Se il componente aggiuntivo o il plug-in non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

6. Nella pagina **Install Primary** verificare che l'applicazione principale sia installata nel computer in cui è in esecuzione Sequencer. In alternativa, è possibile espandere un pacchetto esistente salvato localmente nel computer in cui viene eseguito il sequencer. A tale scopo, fare clic su **Espandi pacchetto**e quindi selezionare il pacchetto. Dopo aver espanso o installato il programma padre, selezionare **ho installato il programma padre principale**.

   Fai clic su **Avanti**.

7. Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto. Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto. Il nome del pacchetto verrà visualizzato nella console di gestione di App-V 5,0. Nella **directory principale dell'applicazione virtuale** viene visualizzato il percorso in cui verrà installata l'applicazione. Per specificare questa posizione, digitare il percorso oppure fare clic su **Sfoglia**.

   **Nota**  
   A partire da App-V 5,0 SP3, la directory principale dell'applicazione virtuale (PVAD) è nascosta, ma è possibile riattivarla. Vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-pvad-hidden).



~~~
Click **Next**.
~~~

8. Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione sono pronti, è possibile procedere con l'installazione del plug-in o dell'applicazione del componente aggiuntivo in modo che il Sequencer possa monitorare il processo di installazione. Usa il processo di installazione dell'applicazione per eseguire l'installazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui** e individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare **ho terminato l'installazione**e quindi fare clic su **Avanti**.

9. Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato. Per una spiegazione più dettagliata sulle informazioni visualizzate in **altre informazioni**, fare doppio clic sull'evento. Dopo aver esaminato le informazioni, fare clic su **Avanti**.

10. Viene visualizzata la pagina **Personalizza** . Se è stata completata l'installazione e la configurazione dell'applicazione virtuale, selezionare **Interrompi ora** e passare al passaggio 12 della procedura. Per eseguire una delle personalizzazioni seguenti, selezionare **Personalizza**.

    -   Ottimizzare la modalità di esecuzione del pacchetto in una rete lenta o inaffidabile.

    -   Specifica i sistemi operativi che possono eseguire questo pacchetto.

    Fai clic su **Avanti**.

11. Nella pagina **flusso** eseguire ogni programma in modo che possa essere ottimizzato ed eseguito in maniera più efficiente nei computer di destinazione. Lo streaming migliora l'esperienza quando il pacchetto dell'applicazione virtuale viene eseguito nei computer di destinazione in reti a latenza elevata. Per eseguire tutte le applicazioni, possono essere necessarie diversi minuti. Dopo l'esecuzione di tutte le applicazioni, chiudere tutte le applicazioni. È anche possibile configurare il pacchetto da richiedere per il download completo prima dell'apertura selezionando la casella di controllo **forza applicazioni da scaricare** . Fai clic su **Avanti**.

   **Nota**  
   Se necessario, è possibile interrompere il caricamento di un'applicazione durante questo passaggio. Nella finestra di dialogo **avvio applicazione** fare clic su **Interrompi** e selezionare una delle caselle di controllo: **arrestare tutte le applicazioni** o **arrestare solo l'applicazione**.



12. Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto. Per consentire l'esecuzione di questo pacchetto in tutti i sistemi operativi supportati nell'ambiente, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** . Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e quindi selezionare i sistemi operativi che possono eseguire il pacchetto. Fai clic su **Avanti**.

13. Viene visualizzata la pagina **Crea pacchetto** . Per modificare il pacchetto senza salvarlo, selezionare **la casella di controllo continua a modificare il pacchetto senza salvare l'uso dell'editor di pacchetti** . Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

   Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto**. Facoltativamente, aggiungere una **Descrizione** che verrà associata al pacchetto. Le descrizioni sono utili per identificare la versione e altre informazioni sul pacchetto.

   **Importante**  
   Il sistema non supporta i caratteri non stampabili nei commenti e nelle descrizioni.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

**Per sequenziare un'applicazione middleware**

1. Nel computer che esegue il Sequencer fare clic su **tutti i programmi**e quindi su **Microsoft Application Virtualization**e quindi su **Microsoft Application Virtualization Sequencer**.

2. *<strong><em>Nel Sequencer fare clic su * </em> creare un nuovo pacchetto di applicazione virtuale </strong> . Selezionare **Crea pacchetto (impostazione predefinita)** e quindi fare clic su **Avanti**.

3. Nella pagina **preparazione computer** esaminare i problemi che potrebbero causare l'esito negativo della creazione del pacchetto o può causare il pacchetto per contenere dati non necessari. Devi risolvere tutti i potenziali problemi prima di continuare. Dopo aver eseguito le correzioni, fare clic su **Aggiorna** per visualizzare le informazioni aggiornate. Dopo aver risolto tutti i potenziali problemi, fare clic su **Avanti**.

   **Importante**  
   Se è necessario disabilitare il software antivirus, è consigliabile analizzare prima di tutto il computer in cui viene eseguito il sequencer di App-V 5,0, in modo da assicurarti che non sia possibile aggiungere file indesiderati o malevoli al pacchetto.



4. Nella pagina **tipo di applicazione** selezionare **middleware**e quindi fare clic su **Avanti**.

5. Nella pagina **Seleziona programma** di installazione fare clic su **Sfoglia** e specificare il file di installazione per l'applicazione. Se l'applicazione non ha un file di programma di installazione associato e si prevede di eseguire manualmente tutte le operazioni di installazione, selezionare la casella **di controllo seleziona questa opzione per eseguire un'installazione personalizzata** e quindi fare clic su **Avanti**.

6. Nella pagina **nome pacchetto** Digitare un nome che verrà associato al pacchetto. Usa un nome che consenta di identificare lo scopo e la versione dell'applicazione che verrà aggiunta al pacchetto. Il nome del pacchetto viene visualizzato nella console di gestione di App-V 5,0. Nella **directory principale dell'applicazione virtuale** viene visualizzato il percorso in cui verrà installata l'applicazione. Per specificare questa posizione, digitare il percorso o fare clic su **Sfoglia**.

   Fai clic su **Avanti**.

7. Nella pagina di **installazione** , quando il sequencer e il programma di installazione dell'applicazione middleware sono pronti, è possibile procedere con l'installazione dell'applicazione in modo che il Sequencer possa monitorare il processo di installazione. Usa il processo di installazione dell'applicazione per eseguire l'installazione. Se è necessario eseguire altri file di installazione come parte dell'installazione, fare clic su **Esegui**per individuare ed eseguire i file di installazione aggiuntivi. Dopo aver completato l'installazione, selezionare la casella di controllo **ho terminato l'installazione** e quindi fare clic su **Avanti**.

8. Nella pagina di **installazione** attendere che il Sequencer configuri il pacchetto di applicazione virtuale.

9. Nella pagina del **report di installazione** è possibile esaminare le informazioni sul pacchetto di applicazione virtuale appena sequenziato. In **altre informazioni**, fare doppio clic su un evento per ottenere informazioni più dettagliate. Per continuare, fare clic su **Avanti**.

10. Nella pagina del **sistema operativo di destinazione** specificare i sistemi operativi che possono eseguire il pacchetto. Per abilitare tutti i sistemi operativi supportati nell'ambiente per l'esecuzione del pacchetto, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto in qualsiasi sistema operativo** . Per configurare il pacchetto in modo che venga eseguito solo su sistemi operativi specifici, selezionare la casella **di controllo Consenti l'esecuzione del pacchetto solo nei sistemi operativi seguenti** e selezionare i sistemi operativi che possono eseguire il pacchetto. Fai clic su **Avanti**.

11. Nella pagina **Crea pacchetto** viene visualizzato. Per modificare il pacchetto senza salvarlo, selezionare **continua per modificare il pacchetto senza salvarlo con l'editor di pacchetti**. Questa opzione apre il pacchetto nella console sequencer in modo che sia possibile modificare il pacchetto prima che venga salvato. Fai clic su **Avanti**.

    Per salvare immediatamente il pacchetto, selezionare **Salva il pacchetto**. Facoltativamente, aggiungere una **Descrizione** da associare al pacchetto. Le descrizioni sono utili per identificare la versione del programma e altre informazioni sul pacchetto.

    **Importante**  
    Il sistema non supporta i caratteri non stampabili nei commenti e nelle descrizioni.



~~~
The default **Save Location** is also displayed on this page. To change the default location, click **Browse** and specify the new location. Click **Create**.
~~~

12. Viene visualizzata la pagina **completamento** . Esaminare le informazioni nel riquadro del **report pacchetto applicazione virtuale** in base alle esigenze, quindi fare clic su **Chiudi**. Queste informazioni sono disponibili anche nel file **Report.xml** che si trova nella directory specificata nel passaggio 11 di questa procedura.

   Il pacchetto è ora disponibile nel sequencer. Per modificare le proprietà del pacchetto, fare clic su **modifica \ [nome pacchetto \]**.

   **Importante**  
   Dopo aver creato correttamente un pacchetto di applicazione virtuale, non è possibile eseguire il pacchetto dell'applicazione virtuale nel computer che esegue Sequencer.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)









