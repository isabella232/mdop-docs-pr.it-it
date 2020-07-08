---
title: Come configurare una cache di sola lettura sul client App-V (VDI)
description: Come configurare una cache di sola lettura sul client App-V (VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817945"
---
# Come configurare una cache di sola lettura sul client App-V (VDI)


In Microsoft Application Virtualization (App-V) 4,6 il client supporta l'uso di una cache di sola lettura condivisa. La cache di sola lettura condivisa consente al client di usare in modo efficiente lo spazio su disco in un sistema VDI (Virtual Desktop Infrastructure), in cui gli utenti eseguono applicazioni in macchine virtuali ospitate in un ambiente server Data Center e condividono l'archiviazione di rete in una rete di area di archiviazione (SAN). Le procedure seguenti includono una panoramica del processo necessario per implementare il client App-V in una delle architetture VDI primarie, note come "VM in pool" o "VM statica". Si presuppone che tu abbia familiarità con la pianificazione, la distribuzione e il funzionamento del sistema App-V e dei relativi componenti, oltre che per l'operazione e la gestione del server VDI. Per altre informazioni su App-V, Vedi [virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)

**Nota**  I dettagli descritti in queste procedure sono intesi solo come esempi. Per completare il processo globale, è possibile usare metodi diversi.

 

## Distribuzione del client App-V in uno scenario VDI


Puoi distribuire il client App-V in uno scenario VDI usando una cache di sola lettura condivisa che è stata popolata con tutte le applicazioni necessarie per tutti gli utenti. Si configura quindi l'immagine di VM Master VDI in modo che tutti i client App-V usino lo stesso file di cache. Agli utenti viene concesso l'accesso a specifiche applicazioni tramite il processo di pubblicazione App-V. Dato che la cache è già precaricata con tutte le applicazioni, nessun flusso si verifica quando un utente avvia un'applicazione. Tuttavia, i pacchetti usati per prepopolare la cache devono essere inseriti in un server App-V che supporta il flusso RTSP (Real Time Streaming Protocol) e che concede le autorizzazioni di accesso ai client App-V. Se pubblichi le applicazioni usando un server di gestione di App-V, puoi usarlo per ottenere questa funzione di flusso.

Il processo di distribuzione è costituito da quattro attività principali:

-   Creazione e popolamento del file della cache condivisa Master

-   Copia del file della cache condivisa nell'archiviazione del server VDI

-   Configurazione del software client App-V nell'immagine master VDI

-   Gestione del ciclo di aggiornamento della distribuzione per il file della cache condivisa dopo la distribuzione iniziale

Queste attività richiedono una pianificazione accurata. Ti consigliamo di preparare e documentare un processo metodico e riproducibile per l'organizzazione da seguire. Questo aspetto è particolarmente importante per la preparazione e la distribuzione iniziali del file della cache condivisa master e per la gestione continua degli aggiornamenti delle applicazioni, ognuno dei quali richiede un aggiornamento alla cache condivisa master. Per completare queste attività primarie, usare le procedure seguenti.

**Nota**  Anche se è possibile pubblicare le applicazioni usando diversi metodi, le procedure seguenti si basano sull'uso di un'app-V Management Server per la pubblicazione.

 

**Per configurare la cache di sola lettura per la distribuzione iniziale in uno scenario di VM VDI o VM statica in pool**

1. Configurazione e configurazione di un server di gestione App-V in una VM nel server VDI per consentire l'autenticazione utente e il supporto della pubblicazione.

2. Popolare la cartella contenuto di questo server di gestione con tutti i pacchetti di applicazioni necessari per tutti gli utenti.

3. Configurare un computer di staging in cui è installato il client App-V. Accedere al computer di staging con un account che abbia accesso a tutte le applicazioni in modo che il set completo di applicazioni venga pubblicato nel computer e quindi eseguire il flusso delle applicazioni in cache in modo che siano completamente caricate.

   **Importante**  
   Il computer di staging deve usare lo stesso tipo di sistema operativo e l'architettura di sistema di quelle usate dalle VM in cui verrà eseguito il client App-V.

     

4. Riavviare il computer di staging in modalità provvisoria per verificare che i driver non siano avviati, in modo da bloccare il file della cache.

   **Nota**  
   In alternativa, è possibile arrestare e disabilitare il servizio di virtualizzazione dell'applicazione e quindi riavviare il computer. Dopo aver copiato il file, ricordarsi di abilitare e riavviare il servizio.

     

5. Copiare il file di cache Sftfs. fsd nella SAN del server VDI in cui tutte le VM possono accedervi, ad esempio in una cartella condivisa. Imposta le autorizzazioni di accesso alle cartelle per la sola lettura per il gruppo Everyone e per il controllo completo per gli amministratori che gestiscono gli aggiornamenti dei file della cache. La posizione del file di cache può essere ottenuta dal registro di sistema AppFS\\FileName.

   **Importante**  
   È necessario inserire il file FSD in una posizione che abbia la capacità di risposta e l'affidabilità equivalenti alle prestazioni di archiviazione associate localmente, ad esempio una SAN.

     

6. Installare il client Desktop App-V nell'immagine VDI Master VM e quindi configurarlo per l'uso della cache di sola lettura aggiungendo i valori della chiave del registro di sistema seguenti alla chiave AppFS nel client. La chiave AppFS si trova in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Chiave</th>
   <th align="left">Tipo</th>
   <th align="left">Value</th>
   <th align="left">Scopo</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>FileName</p></td>
   <td align="left"><p>String</p></td>
   <td align="left"><p>percorso di FSD</p></td>
   <td align="left"><p>Specifica il percorso del file della cache condivisa, ad esempio \VDIServername\Sharefolder\SFTFS. FSD (obbligatorio).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>1</p></td>
   <td align="left"><p>Configura il client per l'uso in modalità di sola lettura. In questo modo, il client non tenterà di eseguire lo streaming degli aggiornamenti nella cache del pacchetto. (obbligatorio).</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>String</p></td>
   <td align="left"><p>percorso del file di log degli errori (ETL)</p></td>
   <td align="left"><p>Voce usata per specificare il percorso del log degli errori. Consigliato. Usare un percorso locale come C:\Logs\Sftfs.etl).</p></td>
   </tr>
   </tbody>
   </table>

     

7. Configurare il client di immagine VM master per usare il server di pubblicazione e per usare l'aggiornamento della pubblicazione all'accesso. Quando gli utenti accedono al sistema VDI e la loro VM viene generata dall'immagine Master VM, viene generato un ciclo di aggiornamento della pubblicazione e vengono pubblicate tutte le applicazioni per cui è autorizzato il proprio account. Queste applicazioni vengono eseguite dalla cache condivisa.

**Per configurare il client per l'aggiornamento del pacchetto in uno scenario di VM in pool**

1.  Completare l'aggiornamento e il test del pacchetto dell'applicazione.

2.  Aggiornare il pacchetto nel server App-V. Quindi, pubblica e trasmetti la nuova versione delle applicazioni al client nel computer di staging in modo che siano completamente caricati nella cache.

3.  Riavviare il computer di staging in modalità provvisoria per verificare che i driver non siano avviati.

    **Nota**  In alternativa, è possibile arrestare e disabilitare il servizio di virtualizzazione dell'applicazione in Services. msc e quindi riavviare il computer. Dopo aver copiato il file, ricordarsi di abilitare e riavviare il servizio.

     

4.  Copiare il file di cache Sftfs. fsd nella SAN del server VDI in cui tutte le VM possono accedervi, ad esempio in una cartella condivisa. È possibile usare un nome file diverso, ad esempio SFTFS \ _V2. FSD per distinguere la nuova versione.

5.  Per configurare il client desktop di App-V nell'immagine VDI Master VM per usare il file della cache condivisa aggiornato, cambiare il valore del nome del file della chiave del registro di sistema AppFS in punto nella posizione di \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Quando gli utenti disconnettersi e quindi accedere di nuovo, viene creata una nuova VM usando l'immagine master aggiornata. Tutte le impostazioni utente verranno mantenute e applicate alla nuova VM. Hanno quindi accesso alle applicazioni aggiornate.

**Per configurare il client per l'aggiornamento del pacchetto in uno scenario VM statico**

1.  Completare l'aggiornamento e il test del pacchetto dell'applicazione.

2.  Aggiornare il pacchetto nel server App-V. Quindi, pubblica e trasmetti la nuova versione delle applicazioni al client nel computer di staging in modo che le applicazioni siano completamente caricate nella cache.

3.  Riavviare il computer di staging in modalità provvisoria per verificare che i driver non siano avviati.

    **Nota**  In alternativa, è possibile arrestare e disabilitare il servizio di virtualizzazione dell'applicazione in Services. msc e quindi riavviare il computer. Dopo aver copiato il file, ricordarsi di abilitare e riavviare il servizio.

     

4.  Copiare il file di cache Sftfs. fsd nella SAN del server VDI in cui tutte le VM possono accedervi, ad esempio in una cartella condivisa. È possibile usare un nome file diverso, ad esempio SFTFS \ _V2. FSD per distinguere la nuova versione.

5.  Per configurare il client desktop di App-V nell'immagine VDI Master VM per usare il file della cache condivisa aggiornato, cambiare il valore del nome del file della chiave del registro di sistema AppFS in punto nella posizione di \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Questo garantisce che i nuovi utenti ottengano la nuova versione.

6.  Creare uno script che modifichi il valore FILENAME della chiave AppFS per impostarlo nella posizione della cache aggiornata, ad esempio \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Configurare questo script per l'esecuzione quando l'utente si disconnette o accede in modo che venga eseguito prima che i driver client App-V inizino, ad esempio, usando le impostazioni dei criteri di gruppo. Quando gli utenti disconnettersi e accedere di nuovo, la VM esistente viene aggiornata e utilizzerà la copia aggiornata della cache. Hanno quindi accesso alle applicazioni aggiornate.

## Come usare i collegamenti simbolici durante l'aggiornamento della cache


Invece di modificare il valore FILENAME della chiave AppFS ogni volta che viene distribuito un nuovo file di cache che contiene pacchetti nuovi o aggiornati, è possibile usare un collegamento simbolico nei sistemi operativi seguenti: Windows Vista, Windows 7 e Windows Server 2008. Per altre informazioni sui collegamenti simbolici, vedere [collegamenti simbolici](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) . Al contrario, Windows XP non supporta l'uso di collegamenti simbolici ed è invece necessario usare i punti di giunzione. Per altre informazioni sulle giunzioni, vedere l' [articolo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) della Microsoft Knowledge base ( https://go.microsoft.com/fwlink/?LinkId=182553) e anche lo strumento [Junction v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .

**Per configurare un collegamento simbolico per fare riferimento alla cache**

1.  Durante la fase di distribuzione iniziale, aprire una finestra del prompt dei comandi come amministratore locale nel sistema operativo host VDI server.

2.  Creare un collegamento simbolico usando il comando MKLINK e quindi configurarlo in punti al file Sftfs. FSD.

    **     MKLINK symlinkname \\\\vdihostserver\\sharefolder\\sftfs.FSD**

3.  Nell'immagine VDI Master VM aprire una finestra del prompt dei comandi usando l'opzione **Esegui come amministratore** e concedere le autorizzazioni di collegamento remoto in modo che la VM possa accedere al collegamento simbolico nel sistema operativo host VDI. Per impostazione predefinita, le autorizzazioni di collegamento remoto sono disabilitate.

    **fsutil behavior set SymlinkEvaluation R2R: 1**

    **Nota**  Nel server di archiviazione è necessario abilitare le autorizzazioni appropriate per i collegamenti. A seconda della posizione del collegamento e del file Sftfs. FSD, le autorizzazioni sono **L2L: 1** o **L2R: 1** o **R2L: 1** o **R2R: 1**.

     

4.  Quando configuri il client desktop di App-V nell'immagine VDI Master VM, imposta il valore FILENAME della chiave AppFS uguale al percorso UNC del file FSD che usa il collegamento simbolico. ad esempio, impostarla su \\\\VDIHostserver\\Symlinkname. Quando l'App-V client accede prima alla cache, il collegamento simbolico passa al client un handle per il file della cache. Il client continua a usare tale handle purché il client sia in funzione. Il valore del collegamento simbolico può essere aggiornato in modo sicuro anche se i client esistenti hanno aperto la cache condivisa precedente.

5.  Quando è necessario aggiornare un pacchetto o aggiungere un nuovo pacchetto alla cache, seguire i passaggi da 1 a 5 della procedura di aggiornamento per lo scenario VM statico o in pool. Eliminare quindi il collegamento simbolico e ricrearlo in maniera che punti alla nuova versione del file della cache condivisa. Quando la VM viene riavviata, il client riceve un handle per la copia aggiornata della cache perché la VM usa il percorso che contiene il collegamento simbolico aggiornato. Gli utenti hanno quindi accesso alle applicazioni nuove e aggiornate.

## Argomenti correlati


[Come installare il server di gestione di Application Virtualization](how-to-install-application-virtualization-management-server.md)

[Come installare manualmente Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Come installare il client usando la riga di comando](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





