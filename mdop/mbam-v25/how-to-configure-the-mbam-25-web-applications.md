---
title: Come configurare le applicazioni Web di MBAM 2.5
description: Come configurare le applicazioni Web di MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824496"
---
# Come configurare le applicazioni Web di MBAM 2.5


Questo argomento spiega come configurare le applicazioni Web di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 per l' [architettura di alto livello consigliata per MBAM 2,5](high-level-architecture-for-mbam-25.md) usando uno dei metodi seguenti:

-   Cmdlet di Windows PowerShell

-   Configurazione guidata server MBAM

Le applicazioni Web includono i siti Web seguenti e i relativi servizi Web:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Website</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sito Web di amministrazione e monitoraggio</p></td>
<td align="left"><p>Sito Web in cui gli utenti specificati possono visualizzare i report e aiutare gli utenti finali a recuperare i propri computer quando dimenticano il PIN o la password</p></td>
</tr>
<tr class="even">
<td align="left"><p>Portale self-service</p></td>
<td align="left"><p>Sito Web a cui gli utenti finali possono accedere per ottenere l'accesso in modo indipendente ai propri computer se dimenticano il PIN o la password</p></td>
</tr>
</tbody>
</table>



**Prima di iniziare la configurazione:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Passaggio</th>
<th align="left">Dove ottenere le istruzioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Esaminare l'architettura consigliata per MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Architettura di alto livello per MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Esaminare le configurazioni supportate per MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Completare i prerequisiti necessari per ogni server.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Verificare di aver configurato SQL ServerReporting Services (SSRS) in modo da usare il Secure Sockets Layer (SSL) prima di configurare il sito Web di amministrazione e monitoraggio. In caso contrario, la caratteristica report utilizzerà HTTP anziché HTTPS.</p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Prerequisiti di MBAM 2,5 server che si applicano solo alla topologia di integrazione di Configuration Manager </a> (se applicabile)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Registrare nomi di entità servizio (SPN) per l'account del pool di applicazioni per i siti Web. È necessario eseguire questa procedura solo se non si hanno diritti di dominio amministrativi in servizi di dominio Active Directory. Se si hanno questi diritti in servizi di dominio Active Directory, MBAM creerà i nomi SPN per l'utente.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)">Pianificazione di come proteggere i siti Web di MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare il software MBAM server su ogni server in cui verrà configurata una caratteristica del server MBAM.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se si prevede di installare i siti Web in un server e i servizi Web in un altro, sarà possibile configurarli solo usando il <strong> cmdlet Enable-MbamWebApplication di </strong> Windows PowerShell. La configurazione guidata di MBAM server non supporta la configurazione di questi elementi in server distinti.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet per configurare le caratteristiche del server MBAM.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Per configurare le applicazioni Web tramite Windows PowerShell**

1.  Prima di avviare la configurazione, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.

2.  Usare il cmdlet **Enable-MbamWebApplication** per configurare le applicazioni Web tramite Windows PowerShell. Per ottenere informazioni su questo cmdlet, digitare **Get-Help Enable-MbamWebApplication**.

**Per configurare le impostazioni per tutte le applicazioni Web tramite la procedura guidata**

1. Nel server in cui si vogliono configurare le applicazioni Web, avviare la configurazione guidata del server MBAM. È possibile selezionare la **configurazione di mbam server** dal menu **Start** per aprire la procedura guidata.

2. Fare clic su **Aggiungi nuove funzionalità**, selezionare **amministrazione e monitoraggio del sito Web** e **portale self-service**, quindi fare clic su **Avanti**. La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per le applicazioni Web.

3. Se il controllo dei prerequisiti è riuscito, fare clic su **Avanti** per continuare. In caso contrario, risolvere i prerequisiti mancanti e quindi fare di **nuovo clic su Controlla prerequisiti**.

4. Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong>Campo</strong></th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Certificato di sicurezza</strong></p></td>
   <td align="left"><p>Selezionare un certificato creato in precedenza per crittografare facoltativamente la comunicazione tra i servizi Web e il server in cui si configurano i siti Web. Se si sceglie <strong> di non usare un certificato </strong> , la comunicazione web potrebbe non essere sicura.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Nome dell'host</strong></p></td>
   <td align="left"><p>Nome del computer host in cui si configurano i siti Web.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Percorso di installazione</strong></p></td>
   <td align="left"><p>Percorso in cui si installano i siti Web.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Port</strong></p></td>
   <td align="left"><p>Numero di porta da usare per la comunicazione tramite sito Web e servizi.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Per abilitare le comunicazioni tramite la porta specificata, è necessario impostare un'eccezione del firewall.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Account di dominio e password del pool di applicazioni Web Service</strong></p></td>
   <td align="left"><p>Account utente di dominio e password per il pool di applicazioni del servizio Web.</p>
   <p>Se si immette un nome utente nel <strong> campo utente o gruppo di dominio di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , è necessario immettere lo stesso valore in questo campo.</p>
   <p>Se si immette un nome di gruppo nel <strong> campo utente o gruppo di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , il valore immesso in questo campo deve essere un membro del gruppo.</p>
   <p>Se non specifichi le credenziali, verranno usate le credenziali specificate per qualsiasi applicazione Web abilitata in precedenza. Tutte le applicazioni Web devono usare le stesse credenziali del pool di applicazioni. Se si specificano credenziali diverse per diverse applicazioni Web, verrà usato il valore specificato più di recente.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Per una maggiore sicurezza, imposta l'account specificato nelle credenziali per avere diritti utente limitati. Imposta inoltre la password dell'account su non scadono mai.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. Verificare che l'account predefinito di IIS \ _IUSRS o l'account del pool di applicazioni sia stato aggiunto al **client** di rappresentanza dopo l'autenticazione e le impostazioni di sicurezza locali del **processo di accesso come batch** .

   Per verificare se è stata aggiunta alle impostazioni di sicurezza locali, aprire l' **Editor criteri di sicurezza locali**, espandere il **nodo Criteri locali** , fare clic sul nodo **assegnazione diritti utente** e quindi fare doppio clic su **rappresenta un client dopo l'autenticazione** e **accedere come criteri processo batch** nel riquadro destro.

**Per configurare le informazioni di connessione per i database tramite la procedura guidata**

1.  Usare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di conformità e controllo.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nome di SQL Server</strong></p></td>
    <td align="left"><p>Nome del server in cui è configurato il database di conformità e controllo.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Istanza di database di SQL Server</strong></p></td>
    <td align="left"><p>Nome dell'istanza di SQL Server in cui è configurato il database di conformità e controllo.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nome database</strong></p></td>
    <td align="left"><p>Nome del database di conformità e controllo.</p></td>
    </tr>
    </tbody>
    </table>



2.  Usare le descrizioni dei campi seguenti per configurare le informazioni di connessione nella procedura guidata per il database di ripristino.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Campo</th>
    <th align="left">Descrizione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nome di SQL Server</strong></p></td>
    <td align="left"><p>Nome del server in cui è configurato il database di ripristino.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Istanza di database di SQL Server</strong></p></td>
    <td align="left"><p>Nome dell'istanza di SQL Server in cui è configurato il database di ripristino.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Nome database</strong></p></td>
    <td align="left"><p>Nome del database di ripristino.</p></td>
    </tr>
    </tbody>
    </table>



**Per configurare le applicazioni Web tramite la procedura guidata**

1. Usare le descrizioni seguenti per immettere i valori dei campi nella procedura guidata per configurare il sito Web di amministrazione e monitoraggio.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Gruppo di domini del ruolo Advanced helpdesk</strong></p></td>
   <td align="left"><p>Gruppo di utenti del dominio i cui membri hanno accesso a tutte le aree del sito Web di amministrazione e monitoraggio eccetto l'area report.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Gruppo di domini del ruolo helpdesk</strong></p></td>
   <td align="left"><p>Gruppo di utenti del dominio i cui membri hanno accesso alle <strong> </strong> aree di gestione TPM e <strong> recupero unità </strong> del sito Web amministrazione e monitoraggio.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Usare l'integrazione di System Center Configuration Manager</strong></p></td>
   <td align="left"><p>Selezionare questa casella di controllo se si sta configurando MBAM con la topologia di integrazione di Configuration Manager. Selezionando questa casella di controllo tutti i report, eccetto il rapporto di controllo del ripristino, verranno visualizzati in Configuration Manager invece che nel sito Web di amministrazione e monitoraggio.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Gruppo di Domain Role Reporting</strong></p></td>
   <td align="left"><p>Gruppo di utenti del dominio i cui membri hanno accesso in sola lettura all'area report del sito Web amministrazione e monitoraggio.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>URL di SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>URL per il server SSRS in cui sono configurati i report MBAM.</p>
   <p>Esempi di URL del report:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tipo di nome host</th>
   <th align="left">Esempio</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Esempio con un nome di dominio completo</p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Esempio con un nome host personalizzato</p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Directory virtuale</strong></p></td>
   <td align="left"><p>Directory virtuale del sito Web di amministrazione e monitoraggio. Questo nome corrisponde alla directory fisica del sito Web del server e viene accodato al nome host del sito Web, ad esempio:</p>
   <p>http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> porta </em> &gt; /helpdesk/</p>
   <p>Se non si specifica una directory virtuale, verrà usato l'helpdesk per il valore <strong> </strong> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Gruppo di dominio del ruolo di migrazione dei dati </strong> (facoltativo)</p></td>
   <td align="left"><p>Gruppo di utenti di dominio i cui membri hanno accesso per usare i cmdlet di informazioni di scrittura-mbam * per scrivere le informazioni di ripristino tramite questo endpoint.</p></td>
   </tr>
   </tbody>
   </table>



2. Usare la descrizione seguente per immettere i valori dei campi nella procedura guidata per configurare il portale self-service.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Campo</th>
   <th align="left">Descrizione</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Directory virtuale</strong></p></td>
   <td align="left"><p>Directory virtuale dell'applicazione Web. Questo nome corrisponde alla directory fisica del sito Web del server e viene accodato al nome host del sito Web, ad esempio:</p>
   <p>http (s):// &lt; <em> hostname </em> &gt; : &lt; <em> porta </em> &gt; /selfservice/</p>
   <p>Se non specifichi una directory virtuale, verrà usato il valore <strong> selfservice </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Nome azienda</p></td>
   <td align="left"><p>Specificare il nome di una società per il portale self-service, ad esempio:</p>
   <p>Contoso IT</p>
   <p>Il nome della società viene visualizzato da tutti gli utenti del portale self-service.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Testo dell'URL dell'helpdesk</p></td>
   <td align="left"><p>Specificare un'istruzione di testo che indirizzi gli utenti al sito Web dell'helpdesk dell'organizzazione, ad esempio:</p>
   <p>Contattare l'helpdesk o il reparto IT</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>URL dell'helpdesk</p></td>
   <td align="left"><p>Specificare l'URL del sito Web dell'helpdesk dell'organizzazione, ad esempio:</p>
   <p>http (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>File di testo di avviso</p></td>
   <td align="left"><p>Selezionare un file contenente l'avviso che si vuole visualizzare agli utenti nella pagina di destinazione del portale self-service.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Non visualizzare il testo dell'avviso per gli utenti</p></td>
   <td align="left"><p>Selezionare questa casella di controllo per specificare che il testo dell'avviso non viene visualizzato agli utenti.</p></td>
   </tr>
   </tbody>
   </table>



3. Dopo aver completato le voci, fare clic su **Avanti**.

   La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per le applicazioni Web.

4. Fai clic su **Next** per continuare.

5. Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.

   **Nota**  
   Per creare uno script di Windows PowerShell per le voci effettuate, fare clic su **Esporta script di PowerShell** e salvare lo script.



6. Fare clic su **Aggiungi** per aggiungere le applicazioni Web al server e quindi fare clic su **Chiudi**.

   Per personalizzare il portale self-service con l'aggiunta di testo di avviso personalizzato, il nome della società, i puntatori a altre informazioni e così via, vedere [personalizzazione del portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md).

**Per configurare il portale self-service se i computer client non riescono ad accedere alla rete CDN**

1.  Determinare se è in uso Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1. In caso affermativo, non eseguire alcuna operazione. La configurazione del portale self-service è completa.

    **Nota**  
    Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 installa i file JavaScript in configurazione e non deve quindi essere connesso alla rete di distribuzione del contenuto Microsoft AJAX per configurare il portale self-service. I passaggi seguenti sono necessari solo se si usa una versione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 precedente a SP1.



2.  Determinare se i computer client hanno accesso alla rete CDN (Microsoft AJAX Content Delivery Network).

    La rete CDN offre al portale self-service l'accesso necessario a determinati file JavaScript. Se non si configura il portale self-service quando i computer client non riescono ad accedere alla rete CDN, verranno visualizzati solo il nome della società e l'account in cui l'utente finale ha effettuato l'accesso. Nessun messaggio di errore verrà visualizzato.

3.  Effettua una delle seguenti operazioni:

    -   Se i computer client hanno accesso alla rete CDN, non eseguire alcuna operazione. La configurazione del portale self-service è completa.

    -   Se i computer client non hanno accesso alla rete CDN, completare la procedura descritta in [come configurare il portale self-service quando i computer client non riescono ad accedere a Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).


## Argomenti correlati


[Registri eventi del server](server-event-logs.md)

[Configurazione delle funzionalità server di MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[Personalizzazione del portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md)

[Convalida della configurazione delle funzionalità del server di MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)



## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





