---
title: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
description: Come ripristinare i computer remoti con l'immagine di ripristino di DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822795"
---
# Come ripristinare i computer remoti con l'immagine di ripristino di DaRT


La funzionalità di connessione remota in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 consente a un amministratore IT di eseguire gli strumenti DaRT in remoto in un computer dell'utente finale. Dopo che alcune informazioni sono state fornite dall'utente finale (o da un helpdesk professionale che lavora nel computer dell'utente finale), l'amministratore IT o l'agente dell'helpdesk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.

**Importante**  
I due computer che stabiliscono una connessione remota devono far parte della stessa rete.



**Per recuperare un computer remoto tramite dardo**

1.  Avviare un computer dell'utente finale usando l'immagine di ripristino DaRT.

    Si utilizzerà in genere uno dei metodi seguenti per avviare il dardo per recuperare un computer remoto, a seconda di come si distribuisce l'immagine di ripristino delle freccette. Per altre informazioni sulla distribuzione dell'immagine di ripristino delle freccette, vedere [distribuzione dell'immagine di ripristino di dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).

    -   Avviare il dardo da una partizione di ripristino nel computer del problema.

    -   Avviare il dardo da una partizione remota nella rete.

    Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

    Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.

    **Nota**  
    La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.



2.  Man mano che il computer si avvia nell'immagine di ripristino DaRT, viene visualizzata la finestra di dialogo **netstart** . Viene chiesto se si desidera inizializzare i servizi di rete. Se si fa clic su **Sì**, si presuppone che in rete sia presente un server DHCP e si tenti di ottenere un indirizzo IP dal server. Se la rete usa indirizzi IP statici anziché DHCP, è possibile usare lo strumento di **configurazione TCP/IP** in DART per specificare un indirizzo IP statico.

    Per ignorare il processo di inizializzazione della rete, fare clic su **No**.

3.  Dopo la finestra di dialogo di inizializzazione della rete, viene chiesto se si vuole rimappare le lettere dell'unità. Quando si esegue Windows online, il volume di sistema viene in genere mappato all'unità C. Tuttavia, quando si esegue Windows offline in WinRE, il volume di sistema originale potrebbe essere mappato a un'altra unità e ciò può causare confusione. Se decidi di rimappare il mapping, dardo cerca di eseguire il mapping delle lettere dell'unità offline in base alle lettere dell'unità online. Il rimapping viene eseguito solo se un sistema operativo offline viene selezionato in un secondo momento nel processo di avvio.

4.  Dopo la finestra di dialogo rimappatura viene visualizzata la finestra di dialogo **Opzioni di ripristino del sistema** e viene chiesto di selezionare un layout di tastiera. Visualizza quindi la directory radice di sistema, il tipo di sistema operativo installato e le dimensioni della partizione. Se il sistema operativo in uso non è visualizzato e si sospetta che la mancanza di driver sia una causa possibile dell'errore, fare clic su **carica driver** per caricare i driver sospetti. Verrà richiesto di inserire il supporto di installazione per il dispositivo e di selezionare il driver. Selezionare l'installazione che si vuole ripristinare o diagnosticare e quindi fare clic su **Avanti**.

    **Nota**  
    Se l'ambiente di ripristino di Windows (WinRE) rileva o sospetta che Windows 7 non sia stato avviato correttamente l'ultima volta che è stato provato, il **ripristino dell'avvio** potrebbe iniziare a essere eseguito automaticamente. Per informazioni su questa situazione, ad esempio su come risolverlo, vedere [risoluzione dei problemi relativi a DaRT 7,0](troubleshooting-dart-70-new-ia.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. Nella finestra **Opzioni ripristino sistema** selezionare strumenti di **diagnostica e ripristino di Microsoft** per aprire la finestra del **set di strumenti di diagnostica e ripristino** .

6. Nella finestra del **set di strumenti di diagnostica e ripristino** fare clic su **connessione remota** per aprire la finestra di **connessione remota Dart** . Se viene richiesto di fornire l'accesso remoto all'help desk, fare clic su **OK**.

   Viene visualizzata la finestra di connessione remota dardo e viene visualizzato un numero di biglietto, un indirizzo IP e le informazioni sulla porta.

7. Nel computer dell'agente helpdesk aprire il **Visualizzatore connessioni remote di Dart**.

   Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Microsoft DaRT 7**e quindi fare clic su **Visualizzatore connessione remota dardo**.

8. Nella finestra di **connessione remota Dart** immettere il ticket, l'indirizzo IP e le informazioni sulla porta necessari.

   **Nota**  
   Queste informazioni vengono create nel computer dell'utente finale e devono essere fornite dall'utente finale. Potrebbe essere possibile scegliere tra più indirizzi IP, a seconda del numero di utenti disponibili nel computer dell'utente finale.



9. Fai clic su **Connetti**.

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

**Per eseguire il Visualizzatore di connessione remota al prompt dei comandi**

1.  È possibile eseguire il **Visualizzatore di connessioni remote di Dart** al prompt dei comandi specificando il comando **DartRemoteViewer.exe** e usando i parametri seguenti:

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


[Ripristino dei computer con DaRT 7.0](recovering-computers-using-dart-70-dart-7.md)









