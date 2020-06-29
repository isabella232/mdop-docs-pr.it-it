---
title: Come distribuire il client App-V
description: Come distribuire il client App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805493"
---
# Come distribuire il client App-V


Usare la procedura seguente per installare il client di Microsoft Application Virtualization (App-V) 5,1 e il client di Servizi Desktop remoto. È necessario installare la versione del client che corrisponde al sistema operativo del computer di destinazione.

<a href="" id="bkmk-clt-install-prereqs"></a>**Operazioni da eseguire prima di iniziare**

1. Rivedere e installare i prerequisiti software:

   Installare il software prerequisito che corrisponde alla versione di App-V che si sta installando:

   -   [Informazioni su App-V 5.1](about-app-v-51.md)

   -   [Prerequisiti di App-V 5.1](app-v-51-prerequisites.md)

2. Esaminare gli scenari di coesistenza client e non supportati, in applicazione dell'installazione:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Distribuzione di client App-V coesistenti</p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)">Pianificazione della distribuzione di App-V 5.1 Sequencer e del client</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Scenari di installazione non supportati o limitati</p></td>
   <td align="left"><p>Vedere la sezione client nelle <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurazioni supportate in App-V 5,1</a></p></td>
   </tr>
   </tbody>
   </table>



3. Esaminare le posizioni per informazioni sul Registro di sistema, il log e la risoluzione dei problemi del client:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Informazioni sul Registro di sistema client</p></td>
<td align="left"><ul>
<li><p>Per impostazione predefinita, dopo l'installazione del client App-V 5,1, le informazioni sul client sono archiviate nel registro di sistema nella chiave del registro di sistema seguente:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</strong></p></li>
<li><p>Quando si distribuisce un pacchetto virtualizzato in un computer che sta eseguendo il client App-V, i dati del pacchetto associati vengono archiviati nella posizione seguente:</p>
<p><strong>C: \ ProgramData \ App-V</strong></p>
<p>È tuttavia possibile riconfigurare la posizione con la chiave del registro di sistema seguente:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>File di log client</p></td>
<td align="left"><ul>
<li><p>Per informazioni sul file di log associato al client App-V 5,1, eseguire una ricerca nel log seguente:</p>
<p><strong>Registri eventi/registri applicazioni e servizi/Microsoft/AppV</strong></p></li>
<li><p>In App-V 5,0 SP3 alcuni registri sono stati consolidati e spostati nella posizione seguente:</p>
<p><strong>Registri eventi/registri applicazioni e servizi/Microsoft/AppV/ServiceLog</strong></p>
<p>Per un elenco dei registri spostati, vedere <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> informazioni su App-V 5,0 SP3 </a> .</p></li>
<li><p>I pacchetti attualmente archiviati nei computer che eseguono il client App-V 5,1 vengono salvati nella posizione seguente:</p>
<p><strong>C:\ProgramData\App-V &amp; lt; ID pacchetto &gt; &amp; lt; ID versione&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Informazioni sulla risoluzione dei problemi di installazione client</p></td>
<td align="left"><p>Vedere il log degli errori nella <strong> cartella% Temp% </strong> . Per rivedere i file di log, fare clic sul pulsante <strong> Start </strong> , digitare <strong> % temp% </strong> e quindi cercare il <strong> log appv_ </strong> .</p></td>
</tr>
</tbody>
</table>



**Per installare il client App-V 5,1**

1.  Copiare il file di installazione del client App-V 5,1 nel computer in cui verrà installato. Scegliere tra i tipi di client seguenti:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo di client</th>
    <th align="left">File da usare</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Versione standard del client</p></td>
    <td align="left"><p><strong>appv_client_setup.exe</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Versione Servizi Desktop remoto del client</p></td>
    <td align="left"><p><strong>appv_client_setup_rds.exe</strong></p></td>
    </tr>
    </tbody>
    </table>



2.  Fare doppio clic sul file di installazione e fare clic su **Installa**. Prima che l'installazione venga avviata, il programma di installazione controlla il computer per tutti i [prerequisiti di App-V 5,1](app-v-51-prerequisites.md)mancanti.

3.  Rivedere e accettare le condizioni di licenza software, scegliere se usare Microsoft Update e se partecipare al programma Microsoft Customer Experience Improvement e fare clic su **Installa**.

4.  Nella pagina **installazione completata** fare clic su **Chiudi**.

    L'installazione crea le voci seguenti per il client App-V nei **programmi**:

    -   **.exe**

    -   **.msi**

    -   **Language Pack**

        **Nota**  
        Dopo l'installazione, è possibile disinstallare solo il file exe.



**Per installare il client App-V 5,1 con uno script**

1. Installare tutti i prerequisiti software necessari nei computer di destinazione. Vedere [cosa fare prima di iniziare](#bkmk-clt-install-prereqs). Se si installa il client usando un file con estensione msi, l'installazione non riuscirà se mancano i prerequisiti.

2. Per usare uno script per installare il client App-V 5,1, usare i parametri seguenti con **appv\_client\_setup.exe**.

   **Nota**  
   Il client Windows Installer (con estensione msi) supporta lo stesso set di opzioni, fatta eccezione per il parametro **/log** .

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>/INSTALLDIR</p></td>
   <td align="left"><p>Specifica la directory di installazione. Esempio di utilizzo: <strong> /INSTALLDIR = C:\Program Files\AppV client</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/CEIPOPTIN</p></td>
   <td align="left"><p>Consente la partecipazione al programma Analisi utilizzo software. Esempio di utilizzo: <strong> /CEIPOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/MUOPTIN</p></td>
   <td align="left"><p>Abilita Microsoft Update. Esempio di utilizzo: <strong> /MUOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/PACKAGEINSTALLATIONROOT</p></td>
   <td align="left"><p>Specifica la directory in cui installare tutte le nuove applicazioni e gli aggiornamenti. Esempio di utilizzo: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\app-V packages&#39;</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/PACKAGESOURCEROOT</p></td>
   <td align="left"><p>Sostituisce la posizione di origine per il download del contenuto del pacchetto. Esempio di utilizzo: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/AUTOLOAD</p></td>
   <td align="left"><p>Specifica il modo in cui i nuovi pacchetti verranno caricati da App-V 5,1 in un computer specifico. Le opzioni seguenti sono abilitate: [1]; caricare automaticamente tutti i pacchetti [2]; o caricare automaticamente nessun pacchetto [0]. <strong> Esempio di utilizzo:/AUTOLOAD = [0 | 1 | 2]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/SHAREDCONTENTSTOREMODE</p></td>
   <td align="left"><p>Specifica che il contenuto del pacchetto in streaming non verrà salvato nel disco rigido locale. Esempio di utilizzo: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/MIGRATIONMODE</p></td>
   <td align="left"><p>Consente al client App-V 5,1 di modificare i tasti di scelta rapida e i accordi associati ai pacchetti creati con una versione precedente. Esempio di utilizzo: <strong> /MIGRATIONMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ENABLEPACKAGESCRIPTS</p></td>
   <td align="left"><p>Abilita gli script definiti nel file manifesto del pacchetto o nei file di configurazione che devono essere eseguiti. Esempio di utilizzo: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/ROAMINGREGISTRYEXCLUSIONS</p></td>
   <td align="left"><p>Specifica i percorsi del registro di sistema che non andranno in roaming con un profilo utente. Esempio di utilizzo: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ROAMINGFILEEXCLUSIONS</p></td>
   <td align="left"><p>Specifica i percorsi di file relativi a% USERPROFILE% che non sono in roaming con un profilo utente&#39;s. Esempio di utilizzo: <strong> /ROAMINGFILEEXCLUSIONS &#39;desktop; immagini personali&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERNAME</p></td>
   <td align="left"><p>Visualizza il nome del server di pubblicazione. Esempio di utilizzo: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERURL</p></td>
   <td align="left"><p>Visualizza l'URL del server di pubblicazione. Esempio di utilizzo: <strong> /S2PUBLISHINGSERVERURL = \pubserver</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHENABLED-</p></td>
   <td align="left"><p>Abilita un aggiornamento globale della pubblicazione. Esempio di utilizzo: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHONLOGON</p></td>
   <td align="left"><p>Avvia un aggiornamento della pubblicazione globale quando un utente esegue l'accesso. Esempio di utilizzo: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVAL-</p></td>
   <td align="left"><p>Specifica l'intervallo di aggiornamento della pubblicazione, dove <strong> 0 </strong> indica che non viene aggiornato periodicamente. Esempio di utilizzo: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Specifica l'unità di intervallo (ore [0], giorni [1]). Esempio di utilizzo: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHENABLED</p></td>
   <td align="left"><p>Consente di aggiornare la pubblicazione degli utenti. Esempio di utilizzo: <strong> /S2USERREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHONLOGON</p></td>
   <td align="left"><p>Avvia un aggiornamento della pubblicazione degli utenti quando un utente esegue l'accesso. Esempio di utilizzo: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVAL-</p></td>
   <td align="left"><p>Specifica l'intervallo di aggiornamento della pubblicazione, dove <strong> 0 </strong> indica che non viene aggiornato periodicamente. Esempio di utilizzo: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Specifica l'unità di intervallo (ore [0], giorni [1]). Esempio di utilizzo: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/Log</p></td>
   <td align="left"><p>Specifica un percorso in cui vengono salvate le informazioni sul log. La posizione predefinita è% Temp%. Esempio di utilizzo: <strong> /log C:\logs\log.log</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/nocancel/q</p></td>
   <td align="left"><p>Specifica un'installazione automatica.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/REPAIR</p></td>
   <td align="left"><p>Ripristina un'installazione precedente del client.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/NORESTART</p></td>
   <td align="left"><p>Impedisce il riavvio del computer dopo l'installazione del client.</p>
   <p>Il parametro impedisce il riavvio del computer per gli utenti finali dopo l'installazione di ogni aggiornamento e consente di programmare la reinstallazione in base alle proprie esigenze. Ad esempio, è possibile installare App-V 5,1 e quindi installare il pacchetto di hotfix Y senza riavviare il sistema dopo l'installazione del Service Pack. Dopo l'installazione, è necessario riavviare prima di iniziare a usare app-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/UNINSTALL</p></td>
   <td align="left"><p>Disinstalla il client.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ACCEPTEULA</p></td>
   <td align="left"><p>Accetta il contratto di licenza. Questa operazione è necessaria per un'installazione automatica. Esempio di utilizzo: <strong> /AcceptEula </strong> o <strong> /ACCEPTEULA = 1 </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/LAYOUT</p></td>
   <td align="left"><p>Specifica l'azione di layout associata. Estrae anche Windows Installer (. msi) e i file di script in una cartella senza installare App-V 5,1. Nessun valore previsto.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/LAYOUTDIR</p></td>
   <td align="left"><p>Specifica la directory del layout. Richiede un valore stringa. Esempio di utilizzo: <strong> /LAYOUTDIR = "client di virtualizzazione C:\Application" </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/?,/h,/Help</p></td>
   <td align="left"><p>Richiede informazioni sui parametri di installazione precedenti.</p></td>
   </tr>
   </tbody>
   </table>



**Per installare il client App-V 5,1 usando il file di Windows Installer (con estensione msi)**

1.  Installare i prerequisiti necessari nei computer di destinazione. Vedere [cosa fare prima di iniziare](#bkmk-clt-install-prereqs). Se i prerequisiti non sono soddisfatti, l'installazione avrà esito negativo.

2.  Assicurarsi che i computer di destinazione non abbiano un riavvio in sospeso prima di installare il client con i file di Windows Installer (MSI) di App-V 5,1. I file di Windows Installer non contrassegnano un riavvio in sospeso.

3.  Distribuire uno dei file di Windows Installer seguenti nel computer di destinazione. Il file specificato deve corrispondere alla configurazione del computer di destinazione.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo di distribuzione</th>
    <th align="left">Distribuire il file</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Il computer sta usando un sistema operativo Microsoft Windows a 32 bit</p></td>
    <td align="left"><p>appv_client_MSI_x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Il computer sta usando un sistema operativo Microsoft Windows a 64 bit</p></td>
    <td align="left"><p>appv_client_MSI_x64.msi</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Si sta distribuendo il client Servizi Desktop remoto App-V 5,1</p></td>
    <td align="left"><p>appv_client_rds_MSI_x64.msi</p></td>
    </tr>
    </tbody>
    </table>



4.  Usando le informazioni nella tabella seguente, selezionare il Language Pack **. msi** appropriato da installare, in base alla lingua desiderata per il computer di destinazione. Il **xxxx** nella tabella fa riferimento alle impostazioni locali di destinazione del Language Pack.

    **Informazioni da conoscere prima di iniziare:**

    -   I Language Pack sono comuni sia al client standard App-V 5,1 che alla versione Servizi Desktop remoto del client App-V 5,1.

    -   Se si installa il client App-V 5,1 usando il **. exe**, il programma di installazione distribuirà solo il Language Pack che corrisponde al sistema operativo in uso nel computer di destinazione.

    -   Per distribuire altri Language Pack in un computer di destinazione, usare la procedura **per installare il client App-V 5,1 usando il file di Windows Installer (con estensione msi)**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo di distribuzione</th>
    <th align="left">Distribuire il file</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Il computer sta usando un sistema operativo Microsoft Windows a 32 bit</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Il computer sta usando un sistema operativo Microsoft Windows a 64 bit</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x64.msi</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Distribuzione di App-V 5.1](deploying-app-v-51.md)

[Informazioni sulle impostazioni di configurazione client](about-client-configuration-settings51.md)

[Come disinstallare il client App-V 5.1](how-to-uninstall-the-app-v-51-client.md)









