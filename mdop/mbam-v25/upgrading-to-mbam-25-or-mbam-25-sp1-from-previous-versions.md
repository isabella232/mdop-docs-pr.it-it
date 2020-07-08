---
title: Aggiornamento a MBAM 2.5 o MBAM 2.5 SP1 da versioni precedenti
description: Aggiornamento a MBAM 2.5 o MBAM 2.5 SP1 da versioni precedenti
author: dansimp
ms.assetid: a9edb4b8-5d5e-42ab-8db6-619db2878e50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 07a03ebbbfce45f7f69a85000e18ddf1a58e53ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804462"
---
# Aggiornamento a MBAM 2.5 o MBAM 2.5 SP1 da versioni precedenti


Questo argomento descrive il processo per l'aggiornamento del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) e del client MBAM dalle versioni precedenti di MBAM.

**Nota**  È possibile eseguire l'aggiornamento direttamente a MBAM 2,5 o MBAM 2,5 SP1 da qualsiasi versione precedente di MBAM.

 

## Prima di iniziare l'aggiornamento


Prima di iniziare l'aggiornamento, esaminare le informazioni seguenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Informazioni da conoscere prima di iniziare</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Se si stanno installando i siti Web di MBAM su un server e i servizi Web in un altro server, è necessario usare i cmdlet di Windows PowerShell per configurarli.</p></td>
<td align="left"><p>La configurazione guidata di MBAM server non supporta la configurazione dei siti Web in un server e i servizi Web in un server diverso.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Se si esegue l'aggiornamento a MBAM 2.5 o 2,5 SP1 da MBAM 2.0 o 2,0 SP1 in Windows Server2008 R2:</p>
<p>Il sito Web di amministrazione e monitoraggio e il portale self-service non funzioneranno se si installa il software .NET Framework 4.5 richiesto dopo l'installazione di Internet Information Services (IIS).</p>
<p>Questo problema si verifica perché ASP.NET non può essere registrato correttamente con IIS se .NET Framework è installato dopo che IIS è già stato installato.</p></td>
<td align="left"><p><strong>Per risolvere il problema:</strong></p>
<p>Eseguire <strong> aspnet_regiis-i </strong> dalla posizione seguente:</p>
<p>C:\windows\microsoft.net\Framework\v4.0.30319</p>
<p>Per altre informazioni, vedere: <a href="https://go.microsoft.com/fwlink/?LinkId=393272" data-raw-source="[ASP.NET IIS Registration Tool](https://go.microsoft.com/fwlink/?LinkId=393272)"> strumento di registrazione di IIS ASP.NET </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registrare un nome SPN nell'account del pool di applicazioni se sono vere tutte le operazioni seguenti:</p>
<ul>
<li><p>Si esegue l'aggiornamento da una versione precedente di MBAM.</p></li>
<li><p>Attualmente, non si eseguono i siti Web MBAM in una configurazione con bilanciamento del carico o distribuiti, ma si vuole farlo quando si esegue l'aggiornamento a MBAM 2.5 o 2,5 SP1.</p></li>
</ul></td>
<td align="left"><p>Per istruzioni, vedere <a href="planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-registerspn)"> pianificazione di come proteggere i siti Web di mbam </a> .</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Cosa consigliamo</strong></p></td>
<td align="left"><p>Registrare un nome dell'entità servizio (SPN) per l'account del pool di applicazioni, anche se per l'account del computer potrebbero essere già presenti SPN registrati.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Perché è consigliabile</strong></p></td>
<td align="left"><p>È necessario registrare un nome SPN nell'account del pool di applicazioni per configurare i siti Web in una configurazione con bilanciamento del carico o distribuita.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cosa succede se i nomi SPN sono già configurati in un account del computer?</strong></p></td>
<td align="left"><p>MBAM utilizzerà i nomi SPN già registrati e non è necessario configurare altri nomi SPN, ma non è possibile configurare i siti Web in una configurazione con bilanciamento del carico o distribuita.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## Procedura per aggiornare l'infrastruttura del server MBAM


Usare i passaggi descritti nelle sezioni seguenti per aggiornare MBAM per la topologia autonoma o la topologia di integrazione di System Center Configuration Manager.

**Per aggiornare l'infrastruttura di MBAM server per la topologia autonoma**

1.  Disinstallare versioni precedenti di MBAM da **programmi e funzionalità** e da server Web per assicurarsi che le informazioni non vengano scritte da client mbam per l'infrastruttura mbam. Per istruzioni, Vedi [rimozione delle funzionalità o del software di mbam server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Eseguire il backup dei database.

3.  Disinstallare le versioni precedenti di MBAM da SQL Server usando **programmi e funzionalità**, tra cui SQL Server che ospitano i report di mbam tramite SQL Server Reporting Services. Rimuovere eventuali cartelle o file temporanei di MBAM rimanenti dal server di database e Reporting Services.

    **Nota**  I database non verranno rimossi e tutti i dati di conformità e ripristino vengono mantenuti nel database.

     

4.  Installare e configurare i database MBAM 2.5 o 2,5 SP1, i report e le applicazioni Web, in questo ordine. I database vengono aggiornati in posizione.

5.  Aggiornare gli oggetti Criteri di gruppo usando i modelli di MBAM 2,5 per sfruttare le nuove funzionalità di MBAM, ad esempio la crittografia forzata. Se non si aggiornano gli oggetti Criteri di stato e il client MBAM per MBAM 2,5, le versioni precedenti dei client MBAM continueranno a segnalare i criteri di GPO correnti con funzionalità ridotte. Vedere [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://www.microsoft.com/download/details.aspx?id=41183) per scaricare i modelli ADMX più recenti.

    Dopo l'aggiornamento dell'infrastruttura di MBAM server, i computer client esistenti continuano a segnalare correttamente il server MBAM 2.5 o 2,5 SP1 e i dati di ripristino continuano a essere archiviati.

6.  Installare l'ultimo client di MBAM 2.5 o 2,5 SP1. Dopo la distribuzione, non è necessario riavviare i computer client.

**Per aggiornare l'infrastruttura MBAM per la topologia di integrazione di System Center Configuration Manager**

1.  Disinstallare versioni precedenti di MBAM da **programmi e funzionalità** e da server Web per assicurarsi che le informazioni non vengano scritte da client mbam per l'infrastruttura mbam. Per istruzioni, Vedi [rimozione delle funzionalità o del software di mbam server](removing-mbam-server-features-or-software.md#bkmk-removeserverfeatures).

2.  Eseguire il backup dei database.

3.  Disinstallare le versioni precedenti di MBAM da SQL Server usando **programmi e funzionalità**, tra cui SQL Server che ospitano i report di mbam tramite SQL Server Reporting Services. Rimuovere eventuali cartelle o file temporanei di MBAM rimanenti dal server di database e Reporting Services.

4.  Disinstallare MBAM dal Server Configuration Manager.

    **Nota**  I database e gli oggetti Configuration Manager (Baseline, MBAM supported Computers Collection e Reports) non verranno rimossi e tutti i dati di conformità e ripristino vengono mantenuti nel database.

     

5.  Aggiornare i file con estensione MOF.

6.  Installare e configurare i database MBAM 2.5 o 2,5 SP1, i report, le applicazioni Web e l'integrazione di Configuration Manager in questo ordine. Gli oggetti database e Configuration Manager vengono aggiornati in posizione.

7.  Facoltativamente, aggiornare gli oggetti Criteri di gruppo e modificare le impostazioni se si vogliono implementare nuove funzionalità in MBAM, ad esempio la crittografia imposta. Se non si aggiornano i GPO, MBAM continuerà a segnalare i criteri di GPO correnti. Vedere [come ottenere i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://docs.microsoft.com/microsoft-desktop-optimization-pack/solutions/how-to-download-and-deploy-mdop-group-policy--admx--templates) per scaricare i modelli ADMX più recenti.

    Dopo l'aggiornamento dell'infrastruttura di MBAM server, i computer client esistenti continuano a segnalare correttamente il server MBAM 2.5 o 2,5 SP1 e i dati di ripristino continuano a essere archiviati.

8.  Installare l'ultimo client di MBAM 2.5 o 2,5 SP1. Dopo la distribuzione, non è necessario riavviare i computer client.

## Supporto per l'aggiornamento per il client MBAM


MBAM supporta gli aggiornamenti per il client MBAM 2.5 da qualsiasi versione precedente del client MBAM.

**Modalità di installazione del client MBAM:**

-   Aggiornare i computer che eseguono il client MBAM tutto in una volta o gradualmente dopo aver installato l'infrastruttura del server MBAM 2.5.

-   Installare il client MBAM tramite un sistema elettronico di distribuzione del software o tramite strumenti come servizi di dominio Active Directory o System Center Configuration Manager.



## Argomenti correlati


[Distribuzione di MBAM 2.5](deploying-mbam-25.md)

[Distribuzione del client di MBAM 2.5](deploying-the-mbam-25-client.md)

[Configurazione delle funzionalità server di MBAM 2.5](configuring-the-mbam-25-server-features.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





