---
title: Pianificazione di gruppi e account di MBAM 2.5
description: Pianificazione di gruppi e account di MBAM 2.5
author: dansimp
ms.assetid: 73bb9fe5-5900-4b6f-b271-ade62991fca1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 3431c3602685a4f96cb4c1333700107ba9c38b96
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825805"
---
# Pianificazione di gruppi e account di MBAM 2.5


Questo argomento elenca i ruoli e gli account che è necessario creare in servizi di dominio Active Directory per specificare i diritti di sicurezza e di accesso per i database di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker, i report e le applicazioni Web. Per ogni ruolo e account, viene fornito il campo corrispondente nella configurazione guidata di MBAM server. Per un elenco di cmdlet e parametri di Windows PowerShell che corrispondono a questi account, vedere [configurazione delle funzionalità del server di MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md#bkmk-reqd-posh-accts).

**Nota**  
MBAM non supporta l'uso di account di servizio gestiti.



## Account di database


Creare gli account seguenti per il database di conformità e controllo e il database di ripristino.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome dell'account e scopo</th>
<th align="left">Tipo di account</th>
<th align="left">Campo configurazione guidata server di MBAM che corrisponde a questo account</th>
<th align="left">Descrizione del campo della configurazione guidata di MBAM server che corrisponde a questo account</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utente o gruppo di lettura/scrittura di database di conformità e controllo e database di ripristino per i report</p></td>
<td align="left"><p>Utente o gruppo</p></td>
<td align="left"><p>Utente o gruppo di dominio di accesso in lettura/scrittura</p></td>
<td align="left"><p>Utente o gruppo di dominio che ha accesso in lettura/scrittura al database di conformità e controllo e al database di ripristino per consentire alle applicazioni Web di accedere ai dati e ai report in questi database.</p>
<p>Se si immette un nome utente in questo campo, deve essere lo stesso valore del <strong> campo account del pool di applicazioni del servizio Web nella </strong> <strong> pagina Configura applicazioni Web </strong> .</p>
<p>Se si immette un nome di gruppo in questo campo, il valore nel <strong> campo account di dominio del pool di applicazioni del servizio Web nella </strong> <strong> pagina Configura applicazioni Web </strong> deve essere un membro del gruppo immesso in questo campo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Utente o gruppo di sola lettura per i report per il database di conformità e controllo</p></td>
<td align="left"><p>Utente o gruppo</p></td>
<td align="left"><p>Utente o gruppo di dominio di Access di sola lettura</p></td>
<td align="left"><p>Nome dell'utente o del gruppo che avrà accesso di sola lettura al database di conformità e controllo per consentire ai report di accedere ai dati di conformità e controllo in questo database.</p>
<p>Se si immette un nome utente in questo campo, deve essere lo stesso utente di quello specificato nel <strong> campo conformità e controllo del dominio del database nella </strong> <strong> pagina Configura report </strong> .</p>
<p>Se si immette un nome di gruppo in questo campo, il valore specificato nel <strong> campo account di dominio del database di conformità e controllo nella </strong> <strong> pagina Configura report </strong> deve essere un membro del gruppo specificato in questo campo.</p></td>
</tr>
</tbody>
</table>



## Account per la creazione di report


Creare gli account seguenti per la caratteristica report.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome account/scopo</th>
<th align="left">Tipo di account</th>
<th align="left">Campo configurazione guidata server di MBAM che corrisponde a questo account</th>
<th align="left">Descrizione del campo della configurazione guidata di MBAM server che corrisponde a questo account</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Report di gruppo di Access per il dominio di sola lettura</p></td>
<td align="left"><p>Gruppo</p></td>
<td align="left"><p>Gruppo di Domain Role Reporting</p></td>
<td align="left"><p>Specifica il gruppo di utenti del dominio che ha accesso in sola lettura ai report nel sito Web amministrazione e monitoraggio. Il gruppo specificato deve essere lo stesso gruppo specificata per il parametro di gruppo di Access di sola lettura di report quando le app Web sono abilitate.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Account utente del dominio del database di conformità e audit</p></td>
<td align="left"><p>Utente</p></td>
<td align="left"><p>Account di dominio del database di conformità e audit</p></td>
<td align="left"><p>Account utente e password di dominio che l'istanza di SQL Server Reporting Services locale usa per accedere al database di conformità e controllo. Questo account richiede <strong> l'accesso come </strong> diritti batch al server SQL Server Reporting Services.</p>
<p>Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un nome utente, è necessario immettere lo stesso valore in questo campo.</p>
<p>Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un nome di gruppo, il valore immesso in questo campo deve essere un membro del gruppo.</p>
<p>Configurare la password per l'account per non scadere mai. L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-helpdesk-roles"></a>Account di amministrazione e monitoraggio del sito Web (Help desk)


Creare gli account seguenti per il sito Web di amministrazione e monitoraggio.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome account/scopo</th>
<th align="left">Tipo di account</th>
<th align="left">Campo configurazione guidata server di MBAM che corrisponde a questo account</th>
<th align="left">Descrizione del campo della configurazione guidata di MBAM server che corrisponde a questo account</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Account di dominio del pool di applicazioni Web Service</p></td>
<td align="left"><p>Utente</p></td>
<td align="left"><p>Account di dominio del pool di applicazioni Web Service</p></td>
<td align="left"><p>Account utente di dominio che deve essere usato dal pool di applicazioni per le applicazioni Web.</p>
<p>Se si immette un nome utente nel <strong> campo utente o gruppo di dominio di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , è necessario immettere lo stesso valore in questo campo.</p>
<p>Se si immette un nome di gruppo nel <strong> campo utente o gruppo di Access di lettura/scrittura nella </strong> <strong> pagina Configura database </strong> , il valore immesso in questo campo deve essere un membro del gruppo.</p>
<p>Se non specifichi le credenziali, verranno usate le credenziali specificate per qualsiasi applicazione Web abilitata in precedenza. Tutte le applicazioni Web devono usare le stesse credenziali del pool di applicazioni. Se si specificano credenziali diverse per diverse applicazioni Web, verrà usato il valore specificato più di recente.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Per una maggiore sicurezza, imposta l'account specificato nelle credenziali per avere diritti utente limitati.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>MBAM Advanced helpdesk utenti di Access Group</p></td>
<td align="left"><p>Gruppo</p></td>
<td align="left"><p>MBAM Advanced helpdesk utenti</p></td>
<td align="left"><p>Gruppo di utenti di dominio i cui membri hanno accesso a tutte le aree di ripristino del sito Web di amministrazione e monitoraggio. Gli utenti che hanno questo ruolo devono immettere solo la chiave di ripristino e non il dominio e il nome utente dell'utente finale quando aiutano gli utenti finali a recuperare le proprie unità. Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti dell'helpdesk avanzato MBAM eseguono l'override delle autorizzazioni di MBAM Group helpdesk.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gruppo di Access per gli utenti di MBAM helpdesk</p></td>
<td align="left"><p>Gruppo</p></td>
<td align="left"><p>Utenti di MBAM helpdesk</p></td>
<td align="left"><p>Gruppo di utenti di dominio i cui membri hanno accesso alle aree Manage TPM e unità di ripristino del sito Web di amministrazione e monitoraggio di MBAM. Gli utenti che hanno questo ruolo devono compilare tutti i campi, incluso il dominio dell'utente finale e il nome dell'account, quando usano entrambe le opzioni.</p>
<p>Se un utente è un membro sia del gruppo di utenti di MBAM helpdesk che di MBAM Advanced helpdesk Users Group, le autorizzazioni di gruppo degli utenti dell'helpdesk avanzato MBAM eseguono l'override delle autorizzazioni di MBAM Group helpdesk.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gruppo di Access report MBAM utenti</p></td>
<td align="left"><p>Gruppo</p></td>
<td align="left"><p>Utenti di report MBAM</p></td>
<td align="left"><p>Gruppo di utenti di dominio i cui membri hanno accesso in sola lettura ai report nell'area report del sito Web amministrazione e monitoraggio.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gruppo utenti di migrazione dei dati di MBAM</p></td>
<td align="left"><p>Gruppo</p></td>
<td align="left"><p>Utenti di migrazione dei dati di MBAM</p></td>
<td align="left"><p>Gruppo di utenti di dominio facoltativo i cui membri hanno le autorizzazioni per scrivere i dati in MBAM usando il servizio di ripristino e hardware di MBAM in uso nel server MBAM. Questo account viene in genere usato con i cmdlet Write-mbam * per scrivere i dati di ripristino e TPM da Active Directory nel database MBAM.</p>
<p>Per altre informazioni, Vedi <a href="mbam-25-security-considerations.md" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md)"> considerazioni sulla sicurezza di MBAM 2,5 </a> .</p></td>
</tr>
</tbody>
</table>




## Argomenti correlati


[Preparazione dell'ambiente per MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Prerequisiti per la distribuzione di MBAM 2.5](mbam-25-deployment-prerequisites.md)



## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





