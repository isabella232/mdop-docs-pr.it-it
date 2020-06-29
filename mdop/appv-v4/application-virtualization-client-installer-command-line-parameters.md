---
title: Parametri della riga di comando del programma di installazione di Application Virtualization Client
description: Parametri della riga di comando del programma di installazione di Application Virtualization Client
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819716"
---
# Parametri della riga di comando del programma di installazione di Application Virtualization Client


Nella tabella seguente sono elencati tutti i parametri della riga di comando di Microsoft Application Virtualization Client Installer disponibili, i relativi valori e una breve descrizione di ogni parametro. I parametri sono maiuscole/minuscole e devono essere immessi come lettere maiuscole. Tutti i valori dei parametri devono essere racchiusi tra virgolette doppie.

**Nota**  
-   Per App-V versione 4,6, i parametri della riga di comando non possono essere usati durante l'aggiornamento del client.

-   I parametri *SWICACHESIZE* e *MINFREESPACEMB* non possono essere combinati nella riga di comando. Se vengono usati entrambi, il parametro *SWICACHESIZE* verrà ignorato.



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro</th>
<th align="left">Valori</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>ALLOWINDEPENDENTFILESTREAMING</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indica se lo streaming da file verrà abilitato indipendentemente dal modo in cui il client è stato configurato con il <em> </em> parametro APPLICATIONSOURCEROOT. Se impostato su FALSE, il trasporto non consentirà lo streaming da file, anche se l'OSD HREF o il <em> </em> parametro APPLICATIONSOURCEROOT contiene un percorso di file.</p>
<p>Valori possibili:</p>
<ul>
<li><p>TRUE: l'applicazione distribuita manualmente può essere caricata da disco.</p></li>
<li><p>FALSE: tutte le applicazioni devono provenire da server di flusso di origine.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>APPLICATIONSOURCEROOT</em></p></td>
<td align="left"><p><em>URL RTSP:// </em> (per il recapito dinamico del pacchetto)</p>
<p><em>URL file:// </em> o <em> UNC </em> (per il caricamento dal pacchetto di distribuzione di file)</p></td>
<td align="left"><p>Per consentire a un amministratore o a un sistema di distribuzione elettronica del software di assicurarsi che il caricamento dell'applicazione venga eseguito in conformità con lo schema di gestione della topologia, consente l'override della BASE di codice OSD per l'elemento HREF dell'applicazione (la posizione di origine). Se il valore è "", che è il valore predefinito, vengono usate le impostazioni di file OSD esistenti.</p>
<p>Un URL include diverse parti:</p>
<p>&lt;protocollo &gt; :// &lt; server &gt; : &lt; percorso della porta &gt; / &lt; &gt; / &lt; &gt; &lt; #fragment query&gt;</p>
<p>Un percorso UNC include tre parti:</p>
<p>&amp;lt; nomecomputer &gt; &amp; lt; cartella condivisione &gt; &amp; lt; risorsa&gt;</p>
<p>Se il <em> </em> parametro APPLICATIONSOURCEROOT è specificato in un client, il client suddividerà l'URL o il percorso UNC da un file OSD nelle parti costituenti e sostituirà le sezioni OSD con le <em> sezioni ApplicationSourceRoot corrispondenti </em> .</p>
<div class="alert">
<strong>Importante</strong><br/><p>Assicurarsi di usare il formato corretto quando si usa file://con un percorso UNC. Il formato corretto è file:// &amp; lt; server &gt; &amp; lt; share &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>ICONSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> http:// </em> o <em> URL https://</em></p></td>
<td align="left"><p>Consente a un amministratore di specificare una posizione di origine per il recupero delle icone per un pacchetto di applicazione sequenziata durante la pubblicazione. Le radici di origine delle icone supportano i percorsi UNC e gli URL (HTTP o HTTPS). Se il valore è "", che è il valore predefinito, vengono usate le impostazioni di file OSD esistenti.</p>
<p>Un URL include diverse parti:</p>
<p>&lt;protocollo &gt; :// &lt; server &gt; : &lt; percorso della porta &gt; / &lt; &gt; / &lt; &gt; &lt; #fragment query&gt;</p>
<p>Un percorso UNC include tre parti:</p>
<p>&amp;lt; nomecomputer &gt; &amp; lt; cartella condivisione &gt; &amp; lt; risorsa&gt;</p>
<div class="alert">
<strong>Importante</strong><br/><p>Assicurarsi di usare il formato corretto quando si usa un percorso UNC. I formati accettabili sono &amp; lt; server &gt; &amp; lt; lettera di condivisione &gt; o &lt; unità &gt; : &amp; lt; cartella &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>OSDSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> http:// </em> o <em> URL https://</em></p></td>
<td align="left"><p>Consente a un amministratore di specificare una posizione di origine per il recupero dei file OSD per un pacchetto di applicazione durante la pubblicazione. Le radici di origine OSD supportano i percorsi UNC e gli URL (HTTP o HTTPS). Se il valore è "", che è il valore predefinito, vengono usate le impostazioni di file OSD esistenti.</p>
<p>Un URL include diverse parti:</p>
<p>&lt;protocollo &gt; :// &lt; server &gt; : &lt; percorso della porta &gt; / &lt; &gt; / &lt; &gt; &lt; #fragment query&gt;</p>
<p>Un percorso UNC include tre parti:</p>
<p>&amp;lt; nomecomputer &gt; &amp; lt; cartella condivisione &gt; &amp; lt; risorsa&gt;</p>
<div class="alert">
<strong>Importante</strong><br/><p>Assicurarsi di usare il formato corretto quando si usa un percorso UNC. I formati accettabili sono &amp; lt; server &gt; &amp; lt; lettera di condivisione &gt; o &lt; unità &gt; : &amp; lt; cartella &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>AUTOLOADONLOGIN</em></p>
<p><em>AUTOLOADONLAUNCH</em></p>
<p><em>AUTOLOADONREFRESH</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Trigger AutoLoad che definiscono gli eventi che avviano il caricamento automatico delle applicazioni. Autoload USA in modo implicito lo streaming in background per consentire il caricamento completo dell'applicazione nella cache.</p>
<p>Il blocco di funzionalità principale verrà caricato il più rapidamente possibile. I blocchi di funzionalità rimanenti verranno caricati in background per abilitare le operazioni in primo piano, ad esempio l'interazione dell'utente con le applicazioni, per avere priorità e ottenere prestazioni ottimali.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Il <em> </em> parametro AUTOLOADTARGET determina le applicazioni caricate automaticamente. Per impostazione predefinita, i pacchetti che sono stati usati vengono caricati automaticamente, a meno che non <em> </em> sia impostato AUTOLOADTARGET.</p>
</div>
<div>

</div>
<p>Ogni parametro ha effetto sul comportamento del caricamento nel modo seguente:</p>
<ul>
<li><p><em>AUTOLOADONLOGIN </em> -il caricamento viene avviato quando l'utente effettua l'accesso.</p></li>
<li><p><em>AUTOLOADONLAUNCH </em> -il caricamento viene avviato quando l'utente avvia un'applicazione.</p></li>
<li><p><em>AUTOLOADONREFRESH </em> -il caricamento viene avviato quando si verifica un aggiornamento della pubblicazione.</p></li>
</ul>
<p>I tre valori possono essere combinati. Nell'esempio seguente, i trigger di autoload sono abilitati sia all'accesso dell'utente che quando si verifica l'aggiornamento della pubblicazione:</p>
<p><em>AUTOLOADONLOGIN AUTOLOADONREFRESH</em></p>
<div class="alert">
<strong>Nota</strong><br/><p>Se il client è configurato per la prima volta con questi valori, il comando AutoLoad non verrà attivato fino alla successiva disattivazione dell'utente e non viene eseguito il log.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>AUTOLOADTARGET</em></p></td>
<td align="left"><p>NESSUNO</p>
<p>TUTTI</p>
<p>PREVUSED</p></td>
<td align="left"><p>Indica cosa verrà caricato automaticamente quando si verificherà un trigger di caricamento automatico specifico.</p>
<p>Valori possibili:</p>
<ul>
<li><p>Nessuno: nessun caricamento automatico, indipendentemente dai trigger che potrebbero essere impostati.</p></li>
<li><p>TUTTO: se è abilitato un trigger di autoload, tutti i pacchetti vengono caricati automaticamente, indipendentemente dal fatto che siano stati o meno avviati.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione è configurata per i singoli pacchetti usando il <strong> pacchetto SFTMIME Add Package </strong> e configura i comandi del <strong> pacchetto </strong> . Per altre informazioni su questi comandi, vedere <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> riferimento al comando SFTMIME </a> .</p>
</div>
<div>

</div></li>
<li><p>PREVUSED-Se è abilitato un trigger di autoload, carica solo i pacchetti in cui almeno un'applicazione nel pacchetto è stata usata in precedenza, ovvero avviata o prememorizzata nella cache.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Quando si installa il client App-V per usare una cache di sola lettura (ad esempio, come implementazione di un server VDI), è necessario impostare il <em> </em> parametro AUTOLOADTARGET su None per impedire al client di provare ad aggiornare le applicazioni nella cache di sola lettura.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>DOTIMEOUTMINUTES</em></p></td>
<td align="left"><p>29600 (impostazione predefinita)</p>
<p>1-1439998560 minuti (intervallo)</p></td>
<td align="left"><p>Indica il numero di minuti in cui un'applicazione può essere usata nell'operazione disconnessa.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>INSTALLDIR</em></p></td>
<td align="left"><p>&lt;percorso&gt;</p></td>
<td align="left"><p>Specifica la directory di installazione del client App-V.</p>
<p>Esempio: INSTALLDIR = &quot; C:\Programmi\Microsoft Application Virtualization Client&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>OPTIN</em></p></td>
<td align="left"><p>TRUE</p>
<p>“”</p></td>
<td align="left"><p>I componenti di Microsoft Application Virtualization Client saranno aggiornabili tramite Microsoft Update quando gli aggiornamenti vengono resi disponibili per il pubblico in generale. Microsoft Update Agent installato nei sistemi operativi Windows richiede a un utente di accettare esplicitamente di usare il servizio. Questo opt-in è necessario una sola volta per tutte le applicazioni nel dispositivo. Se hai già optato per Microsoft Update, i componenti Microsoft Application Virtualization nel dispositivo approfitteranno automaticamente del servizio.</p>
<p>Per l'installazione della riga di comando, l'uso di Microsoft Update è per impostazione predefinita opt-out (a meno che un'applicazione precedente non abbia già consentito l'inserimento del dispositivo) a causa del requisito di optare manualmente in Microsoft Update. Di conseguenza, l'opt-in deve essere esplicito per le installazioni della riga di comando. Impostando il parametro della riga <em> di comando optin </em> su true, viene impostato l'opt-in Microsoft Update.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>REQUIREAUTHORIZATIONIFCACHED</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Indica se l'autorizzazione è sempre necessaria, indipendentemente dal fatto che un'applicazione sia già nella cache.</p>
<p>Valori possibili:</p>
<ul>
<li><p>TRUE: l'applicazione deve sempre essere autorizzata all'avvio. Per le applicazioni in streaming RTSP, il token di autorizzazione utente viene inviato al server per l'autorizzazione. Per le applicazioni basate su file, gli ACL dei file determinano se un utente può accedere all'applicazione.</p></li>
<li><p>FALSE: provare sempre a connettersi al server. Se non è possibile stabilire una connessione al server, il client consente comunque all'utente di avviare un'applicazione precedentemente caricata nella cache.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWICACHESIZE</em></p></td>
<td align="left"><p>Dimensioni della cache in MB</p></td>
<td align="left"><p>Specifica le dimensioni in megabyte della cache client. La dimensione predefinita è 4096 MB e la dimensione massima è 1.048.576 MB (1 TB). Il sistema verifica lo spazio disponibile al momento dell'installazione, ma lo spazio non è riservato.</p>
<p>Esempio: <strong> SWICACHESIZE = &quot; 1024&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRDISPLAY</em></p></td>
<td align="left"><p>Nome visualizzato</p></td>
<td align="left"><p>Specifica il nome visualizzato del server di pubblicazione; obbligatorio quando <em> </em> viene usato SWIPUBSVRHOST.</p>
<p>Esempio: <strong> SWIPUBSVRDISPLAY = &quot; ambiente di produzione&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRTYPE</em></p></td>
<td align="left"><p>[HTTP | RTSP</p></td>
<td align="left"><p>Specifica il tipo di server di pubblicazione. Il tipo di server predefinito è Application Virtualization Server. L' <strong> opzione/Secure non fa distinzione tra maiuscole e </strong> minuscole.</p>
<ul>
<li><p>HTTP-server HTTP standard</p></li>
<li><p>HTTP <strong> /Secure </strong> — Server http di sicurezza avanzato</p></li>
<li><p>RTSP — Application Virtualization Server</p></li>
<li><p>RTSP <strong> /Secure </strong> — Enhanced Security Application Virtualization Server</p></li>
</ul>
<p>Esempio: <strong> SWIPUBSVRTYPE = &quot; http/secure&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRHOST</em></p></td>
<td align="left"><p>Indirizzo IP | nome host</p></td>
<td align="left"><p>Specifica l'indirizzo IP del server di virtualizzazione dell'applicazione o un nome host del server che viene risolto nell'indirizzo IP del server&#39;s; obbligatorio quando <em> </em> viene usato SWIPUBSVRDISPLAY.</p>
<p>Esempio: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRPORT</em></p></td>
<td align="left"><p>Numero di porta</p></td>
<td align="left"><p>Specifica la porta logica usata da questo server di virtualizzazione dell'applicazione per ascoltare le richieste dal client (impostazione predefinita = 554).</p>
<ul>
<li><p>Server HTTP standard: impostazione predefinita = 80.</p></li>
<li><p>Server HTTP di sicurezza avanzato-impostazione predefinita = 443.</p></li>
<li><p>Application Virtualization Server-default = 554.</p></li>
<li><p>Enhanced Security Application Virtualization Server-default = 322.</p></li>
</ul>
<p>Esempio: <strong> SWIPUBSVRPORT = &quot; 443&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRPATH</em></p></td>
<td align="left"><p>Nome percorso</p></td>
<td align="left"><p>Specifica la posizione nel server di pubblicazione del file che definisce le associazioni di tipi di file (impostazione predefinita =/); obbligatorio quando il <em> </em> valore del parametro SWIPUBSVRTYPE è http.</p>
<p>Esempio: <strong> SWIPUBSVRPATH = &quot; /APPVIRT/appsntypes.xml&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRREFRESH</em></p></td>
<td align="left"><p>[Attivato | DISATTIVARE</p></td>
<td align="left"><p>Specifica se il client esegue automaticamente una query nel server di pubblicazione per le associazioni di tipi di file e le applicazioni quando un utente accede al client (impostazione predefinita = attivata).</p>
<p>Esempio: <strong> SWIPUBSVRREFRESH = &quot; off&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIGLOBALDATA</em></p></td>
<td align="left"><p>Directory dati globale</p></td>
<td align="left"><p>Specifica la directory in cui verranno archiviati i dati non specifici per gli utenti particolari (impostazione predefinita = C:\Documents and Settings\All Users\Documents).</p>
<p>Esempio: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIUSERDATA</em></p></td>
<td align="left"><p>Directory dati utente</p></td>
<td align="left"><p>Specifica la directory in cui verranno archiviati i dati specifici di determinati utenti (default =% APPDATA%).</p>
<p>Esempio: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization Client&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIFSDRIVE</em></p></td>
<td align="left"><p>Lettera di unità preferita</p></td>
<td align="left"><p>Corrisponde alla lettera dell'unità selezionata per l'unità virtuale.</p>
<p>Esempio: <strong> SWIFSDRIVE = &quot; S&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SYSTEMEVENTLOGLEVEL</em></p></td>
<td align="left"><p>0 – 4</p></td>
<td align="left"><p>Indica il livello di registrazione in cui i messaggi di log vengono scritti nel log eventi di NT. Il valore indica una soglia di ciò che viene registrato, ovvero tutto ciò che è uguale o minore di quel valore viene registrato. Ad esempio, un valore di 0x3 (Warning) indica che vengono registrati gli avvisi (0x3), gli errori (0x2) e gli errori critici (0x1).</p>
<p>Valori possibili:</p>
<ul>
<li><p>0 = = None</p></li>
<li><p>1 = = critico</p></li>
<li><p>2 = = errore</p></li>
<li><p>3 = = avviso</p></li>
<li><p>4 = = informazioni</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>MINFREESPACEMB</em></p></td>
<td align="left"><p>In MB</p></td>
<td align="left"><p>Specifica la quantità di spazio libero (in megabyte) che deve essere disponibile nell'host prima che le dimensioni della cache possano aumentare. L'esempio seguente consente di configurare il client per garantire almeno 5 GB di spazio disponibile sul disco prima di consentire l'aumento delle dimensioni della cache. Il valore predefinito è 5000 MB di spazio disponibile su disco in fase di installazione.</p>
<p>Esempio: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 GB)</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>KEEPCURRENTSETTINGS</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Viene usato quando si applicano le impostazioni del registro di sistema prima della distribuzione di un client, ad esempio tramite criteri di gruppo. Quando si distribuisce un client, impostare questo parametro su un valore pari a 1 in modo che non sovrascriva le impostazioni del registro di sistema.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Se impostato su un valore pari a 1, i parametri della riga di comando del programma di installazione client seguenti vengono ignorati:</p>
<p><strong>SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> , <strong> OSDSourceRoot </strong> , <strong> SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, </strong> SWIFSDRIVE, <strong> AUTOLOADTARGET, </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> AUTOLOADTRIGGERS </strong> e <strong> SWIUSERDATA </strong> .</p>
<p>Per altre informazioni sull'impostazione di questi valori dopo l'installazione, vedere "come configurare le impostazioni del registro di sistema client App-V usando la riga di comando" nella Guida operativa di Application Virtualization (App-V) <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Come installare manualmente Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Come aggiornare Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[Informazioni di riferimento sui comandi di SFTMIME](sftmime--command-reference.md)









