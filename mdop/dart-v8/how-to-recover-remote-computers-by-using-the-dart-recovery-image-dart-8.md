---
title: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
description: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: 363ccd48-6820-4b5b-a43a-323c0b208a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b3e3155dbea8da18338b8a167d22f73b1c8e4bb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824396"
---
# Come ripristinare i computer remoti con l'immagine di ripristino di DaRT


Usare la caratteristica connessione remota in Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 per eseguire gli strumenti DaRT in remoto in un computer per utenti finali. Dopo che l'utente finale fornisce all'amministratore o all'addetto al supporto tecnico informazioni specifiche, l'amministratore IT o il lavoratore dell'help desk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.

Se gli strumenti DaRT sono stati disabilitati quando è stata creata l'immagine di ripristino, è comunque possibile accedere a tutti gli strumenti. Tutti gli strumenti, ad eccezione della connessione remota, non sono disponibili per gli utenti finali.

**Per recuperare un computer remoto usando l'immagine di ripristino di DaRT**

1.  Avviare un computer dell'utente finale usando l'immagine di ripristino DaRT.

    Si utilizzerà in genere uno dei metodi seguenti per avviare il dardo per recuperare un computer remoto, a seconda di come si distribuisce l'immagine di ripristino delle freccette. Per altre informazioni sulla distribuzione dell'immagine di ripristino delle freccette, vedere [distribuzione di dart 8,0](deploying-dart-80-dart-8.md).

    -   Avviare il dardo da una partizione di ripristino nel computer del problema.

    -   Avviare il dardo da una partizione remota nella rete.

    Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

    Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.

    **Nota**  
    La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. Quando viene chiesto se si vuole inizializzare i servizi di rete, selezionare una delle opzioni seguenti:

   **Sì** -si presuppone che sia presente un server DHCP nella rete e si tenti di ottenere un indirizzo IP dal server. Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.

   **No** -ignorare il processo di inizializzazione della rete.

3. Indicare se si vuole riassociare le lettere dell'unità. Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione. Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online. Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.

4. Nella finestra di dialogo **Opzioni ripristino** configurazione di sistema selezionare un layout di tastiera.

5. Controllare la directory radice di sistema visualizzata, il tipo di sistema operativo installato e le dimensioni della partizione. Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti e quindi inserire il supporto di installazione per il dispositivo e selezionare il driver.

6. Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.

   **Nota**  
   Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 8 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente. Per informazioni su come risolvere il problema, vedere [risoluzione dei problemi relativi a DaRT 8,0](troubleshooting-dart-80-dart-8.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Nella finestra **Opzioni ripristino sistema** fare clic su **strumenti di diagnostica e ripristino di Microsoft** per aprire il **set di strumenti di diagnostica e ripristino**.

8. Nella finestra del **set di strumenti di diagnostica e ripristino** fare clic su **connessione remota** per aprire la finestra di **connessione remota Dart** . Se viene richiesto di fornire l'accesso remoto all'help desk, fare clic su **OK**.

   Viene visualizzata la finestra di connessione remota dardo e viene visualizzato un numero di biglietto, un indirizzo IP e le informazioni sulla porta.

9. Nel computer dell'help desk aprire il **Visualizzatore di connessione remota Dart**.

10. Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Microsoft DaRT 8,0**e quindi fare clic su **Visualizzatore connessione remota dardo**.

11. Nella finestra di **connessione remota Dart** immettere il ticket, l'indirizzo IP e le informazioni sulla porta necessari.

   **Nota**  
   Queste informazioni vengono create nel computer dell'utente finale e devono essere fornite dall'utente finale. Potrebbe essere possibile scegliere tra più indirizzi IP, a seconda del numero di utenti disponibili nel computer dell'utente finale.



12. Fai clic su **Connetti**.

L'amministratore IT assume ora il controllo del computer dell'utente finale e può eseguire gli strumenti DaRT in remoto.

**Nota**  
Viene fornito un file denominato inv32.xml che contiene le informazioni di connessione remota, ad esempio il numero di porta e l'indirizzo IP. Per impostazione predefinita, il file si trova in genere in%windir%\\system32.



**Per personalizzare il processo di connessione remota**

1. È possibile personalizzare il processo di connessione remota modificando il file winpeshl.ini. Per altre informazioni su come modificare il file di winpeshl.ini, vedere [Winpeshl.ini file](https://go.microsoft.com/fwlink/?LinkId=219413).

   Specificare i comandi e i parametri seguenti per personalizzare il modo in cui viene stabilita una connessione remota con un computer dell'utente finale:

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Comando</th>
   <th align="left">Parametro</th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>RemoteRecovery.exe</strong></p></td>
   <td align="left"><p>-nomessage</p></td>
   <td align="left"><p>Specifica che la richiesta di conferma non viene visualizzata. <strong>La connessione remota </strong> continua proprio come se l'utente finale avesse risposto &quot; Sì &quot; alla richiesta di conferma.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>WaitForConnection.exe</strong></p></td>
   <td align="left"><p>nessuno</p></td>
   <td align="left"><p>Impedisce che uno script personalizzato continui fino a quando <strong> </strong> non è in esecuzione una connessione remota o non viene stabilita una connessione valida con il computer dell'utente finale.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Questo comando non serve alcuna funzione se specificato in modo indipendente. Deve essere specificato in uno script per funzionare correttamente.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Di seguito è riportato un esempio di file di winpeshl.ini personalizzato per aprire lo strumento di **connessione remota** non appena viene eseguito un tentativo di avvio in dardo:

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

Quando si avvia dardo, crea il file inv32.xml in \\Windows\\System32\\ sul disco RAM. Questo file contiene informazioni sulla connessione: indirizzo IP, porta e numero di biglietto. È possibile copiare il file in una condivisione di rete per attivare un flusso di lavoro Help desk. Ad esempio, un programma personalizzato può controllare la condivisione di rete per i file di connessione e quindi creare un ticket di supporto o inviare notifiche tramite posta elettronica.

**Per eseguire il Visualizzatore di connessione remota al prompt dei comandi**

1.  Per eseguire il **Visualizzatore di connessioni remote di Dart** al prompt dei comandi, specificare il comando **DartRemoteViewer.exe** e usare i parametri seguenti:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parametro</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>-Ticket = &lt; <em> numero ticket</em>&gt;</p></td>
    <td align="left"><p>Dove &lt; <em> numero ticket </em> &gt; è il numero del biglietto, inclusi i trattini generati da una connessione remota.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>-IPAddress = &lt; <em> IPAddress</em>&gt;</p></td>
    <td align="left"><p>Dove &lt; <em> IPAddress </em> &gt; è l'indirizzo IP generato dalla connessione remota.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>-porta = &lt; <em> porta</em>&gt;</p></td>
    <td align="left"><p>Dove &lt; <em> porta </em> &gt; è la porta che corrisponde all'indirizzo IP specificato.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. Se si specificano tutti e tre i parametri e i dati sono validi, viene eseguita immediatamente una connessione all'avvio del programma. Se un parametro qualsiasi non è valido, il programma viene avviato come se non fossero stati specificati parametri.

## Argomenti correlati


[Operazioni relative a DaRT 8.0](operations-for-dart-80-dart-8.md)

[Ripristino dei computer con DaRT 8.0](recovering-computers-using-dart-80-dart-8.md)









