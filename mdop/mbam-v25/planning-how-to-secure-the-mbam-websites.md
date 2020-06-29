---
title: Pianificazione di come proteggere i siti Web di MBAM
description: Pianificazione di come proteggere i siti Web di MBAM
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825025"
---
# Pianificazione di come proteggere i siti Web di MBAM


In questo argomento vengono descritti i metodi seguenti per proteggere il sito Web di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 e il portale self-service di amministrazione e monitoraggio:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Obbligatorio o facoltativo?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usare i certificati per proteggere i siti Web di MBAM</p></td>
<td align="left"><p>Facoltativo, ma altamente raccomandato</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrazione di nomi di entità servizio (SPN) per l'account del pool di applicazioni</p></td>
<td align="left"><p>Obbligatorio</p></td>
</tr>
</tbody>
</table>



Per altre informazioni su come proteggere la distribuzione di MBAM, vedere [considerazioni sulla sicurezza di mbam 2,5](mbam-25-security-considerations.md).

## Usare i certificati per proteggere i siti Web di MBAM


È consigliabile usare un certificato per proteggere la comunicazione tra:

-   Client MBAM e servizi Web

-   Browser e sito Web per l'amministrazione e il monitoraggio e i siti Web portale self-service

Per informazioni sulla richiesta e l'installazione di un certificato, vedere [configurazione di certificati server Internet](https://technet.microsoft.com/library/cc731977.aspx).

**Nota**  
È possibile configurare i siti Web e i servizi Web in server diversi solo se si usa Windows PowerShell. Se si usa la configurazione guidata di MBAM server per configurare i siti Web, è necessario configurare i siti Web e i servizi Web nello stesso server.



Per proteggere la comunicazione tra i servizi Web e i database, è consigliabile forzare la crittografia in SQL Server. Per informazioni su come proteggere tutte le connessioni a SQL Server, incluse le comunicazioni tra i servizi Web e SQL Server, vedere [considerazioni sulla sicurezza di MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).

## Registrazione di nomi SPN per l'account del pool di applicazioni


Per consentire ai server MBAM di autenticare le comunicazioni dal sito Web di amministrazione e monitoraggio e dal portale self-service, è necessario registrare un nome dell'entità servizio (SPN) per il nome host sotto l'account di dominio in uso per il pool di applicazioni Web.

Questo argomento contiene istruzioni su come registrare i nomi SPN per i tipi di nome host seguenti:

-   Nome di dominio completo

-   Nome NetBIOS

-   Nome virtuale

### Prima di creare nomi SPN per un'installazione iniziale di MBAM

Esaminare le informazioni nella tabella seguente prima di iniziare la creazione di nomi SPN.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività o elemento</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Creare un account del servizio in servizi di dominio Active Directory.</p></td>
<td align="left"><p>L'account del servizio è un account utente creato in servizi di dominio Active Directory per garantirne la sicurezza per i siti Web di MBAM. I siti Web di MBAM vengono eseguiti in un pool di applicazioni, la cui identità è il nome dell'account del servizio. I nomi SPN vengono quindi registrati nell'account del pool di applicazioni.</p>
<div class="alert">
<strong>Nota</strong><br/><p>È necessario usare lo stesso account del pool di applicazioni per tutti i server Web.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Verificare che l'account del gruppo IIS-IUSRS o l'account del pool di applicazioni dispongano dei diritti necessari.</p></td>
<td align="left"><p>Per eseguire questa operazione, eseguire le operazioni seguenti:</p>
<ol>
<li><p>Aprire l' <strong> Editor criteri di sicurezza locali </strong> ed espandere il <strong> nodo Criteri locali </strong> .</p></li>
<li><p>Selezionare il <strong> nodo assegnazione diritti utente </strong> e fare doppio clic sul pulsante <strong> rappresenta un client dopo l'autenticazione </strong> e <strong> accedere come impostazioni dei </strong> criteri di gruppo processo batch nel riquadro destro.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p>Se si configurano i siti Web di MBAM usando un account di amministrazione del dominio, MBAM creerà i nomi SPN per l'utente.</p></td>
<td align="left"><p>Se si configurano i siti Web di MBAM usando un account di amministrazione del dominio, seguire i passaggi descritti in questo argomento per registrare i nomi SPN manualmente per il tipo di nome host in uso.</p></td>
</tr>
</tbody>
</table>



### Registrazione di nomi SPN quando si usa un nome host di dominio completo

Se si usa un nome host di dominio completo quando si configura MBAM, è necessario registrare un solo SPN, come illustrato nell'esempio seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cosa è necessario fare</th>
<th align="left">Esempi e altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registrare un SPN per il nome di dominio completo.</p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p>Il nome host completo è <strong> mybitlockerrecovery.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurare la delega vincolata per l'SPN che si sta registrando per l'account del pool di applicazioni.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configurazione della delega vincolata</a></p>
<p>Questo requisito si applica solo a MBAM 2,5; non è necessario in MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### Registrazione di nomi SPN quando si usa un nome host NetBIOS

Se si usa un nome host NetBIOS quando si configura MBAM, registrare un SPN per il nome NetBIOS e un altro SPN per il nome di dominio completo, come illustrato negli esempi seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cosa è necessario fare</th>
<th align="left">Esempi e altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registrare un SPN per il nome host NetBIOS.</p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p>Il nome host NetBIOS è <strong> nbname01 </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrare un SPN per il nome di dominio completo.</p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p>Il nome di dominio completo è <strong> nbname01.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare la delega vincolata per i nomi SPN che si sta registrando per l'account del pool di applicazioni.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configurazione della delega vincolata</a></p>
<p>Questo requisito si applica solo a MBAM 2,5; non è necessario in MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a>Registrazione di nomi SPN quando si usa un nome host virtuale

Se si configura MBAM con un nome host virtuale che è un nome di dominio completo, registrare un solo SPN per il nome host virtuale. Se il nome host virtuale configurato non è un nome di dominio completo, è necessario creare un secondo SPN che specifichi il nome di dominio completo, come descritto negli esempi seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cosa è necessario fare</th>
<th align="left">Esempi e altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Se il nome host virtuale è un nome di dominio completo, come in questo esempio, registrare un solo SPN.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>Nell'esempio, il nome host virtuale è <strong> mbamvirtual.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrare questo SPN aggiuntivo se il nome host virtuale non è un nome di dominio completo.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p>Nell'esempio, il nome host virtuale è <strong> mbamvirtual </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registrare questo SPN aggiuntivo se il nome host virtuale non è un nome di dominio completo.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>Nell'esempio, il nome host virtuale è <strong> mbamvirtual.contoso.com </strong> e l'account di dominio usato per il pool di applicazioni Web è <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nel server Domain Name Server (DNS) creare un "un record" per il nome host personalizzato e puntarlo a un server Web o a un servizio di bilanciamento del carico.</p></td>
<td align="left"><p>Vedere la sezione "per configurare DNS host A Records" in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> configurare i record host DNS </a> .</p>
<p>Ti consigliamo di usare un record anziché CNAME. Se si usano i CNAME per puntare all'indirizzo del dominio, è necessario registrare anche i nomi SPN per il nome del server Web nell'account del pool di applicazioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configurare la delega vincolata per i nomi SPN che si sta registrando per l'account del pool di applicazioni.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configurazione della delega vincolata</a></p>
<p>Questo requisito si applica solo a MBAM 2,5; non è necessario in MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a>Registrazione di un SPN quando si esegue l'aggiornamento da versioni precedenti di MBAM

Completare i passaggi descritti in questa sezione solo se si vuole:

-   Eseguire l'aggiornamento da una versione precedente di MBAM.

-   Eseguire i siti Web in MBAM 2,5 in una configurazione con bilanciamento del carico o distribuita ed è attualmente in esecuzione in una configurazione che non viene caricata in maniera equilibrata.

Se i nomi SPN sono già stati registrati nell'account del computer anziché in un account del pool di applicazioni, MBAM usa i nomi SPN esistenti e non è possibile configurare i siti Web in una configurazione con bilanciamento del carico o distribuita.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cosa è necessario fare</th>
<th align="left">Esempi e altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Creare un account del pool di applicazioni in servizi di dominio Active Directory.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Rimuovere i Web site e i servizi Web attualmente installati.</p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)">Rimozione di software o funzionalità del server di MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rimuovere i nomi SPN dall'account del computer.</p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrare nomi SPN nell'account del pool di applicazioni.</p></td>
<td align="left"><p>Seguire la procedura per la <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> registrazione di nomi SPN quando si usa un nome host virtuale </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Riconfigurare le applicazioni Web e i servizi Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Come configurare le applicazioni Web di MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Eseguire una delle operazioni seguenti, a seconda del metodo usato per la configurazione:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configurazione guidata server MBAM</strong></p></td>
<td align="left"><p>Immettere l'account del pool di applicazioni nel <strong> campo account di dominio del pool di applicazioni del servizio Web </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> Cmdlet di Windows PowerShell</p></td>
<td align="left"><p>Immettere l'account nel <code>WebServiceApplicationPoolCredential</code> parametro.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>Il nome host immesso deve avere lo stesso nome del nome host virtuale per cui si stanno creando i nomi SPN. Inoltre, nella Web farm i nomi host e le credenziali del pool di applicazioni devono essere identici per ogni server che si sta configurando.</p>
</div>
<div>

</div>
<p>Quando MBAM configura le applicazioni Web, cercherà di registrare i nomi SPN per l'utente, ma può farlo solo se si hanno diritti di amministratore di dominio nel server in cui si sta installando MBAM. Se non si dispone di questi diritti, è possibile completare la configurazione, ma sarà necessario impostare i nomi SPN prima o dopo la configurazione di MBAM.</p></td>
</tr>
</tbody>
</table>

## Impostazioni di filtro richieste obbligatorie

 Per consentire all'applicazione di operare come previsto, è necessario "Consenti estensioni di file non in elenco".  Questa operazione può essere trovata passando alla pagina "amministrazione e monitoraggio di Microsoft BitLocker"-> filtro delle richieste-> modificare le impostazioni delle caratteristiche.


## Argomenti correlati


[Preparazione dell'ambiente per MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Prerequisiti per la distribuzione di MBAM 2.5](mbam-25-deployment-prerequisites.md)





## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



