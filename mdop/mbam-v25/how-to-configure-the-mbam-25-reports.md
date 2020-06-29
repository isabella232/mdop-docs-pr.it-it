---
title: Come configurare i report di MBAM 2.5
description: Come configurare i report di MBAM 2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826616"
---
# Come configurare i report di MBAM 2.5


In questo argomento viene illustrato come configurare la funzionalità di report di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 tramite:

-   Cmdlet di Windows PowerShell

-   Configurazione guidata server MBAM

Le istruzioni si basano sull'architettura consigliata nell' [architettura di alto livello per MBAM 2,5](high-level-architecture-for-mbam-25.md).

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
<td align="left"><p>Completare i prerequisiti necessari per ogni server.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Prerequisiti di MBAM 2,5 server che si applicano solo alla topologia di integrazione di Configuration Manager </a> (se applicabile)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Installare il software MBAM server su ogni server in cui si prevede di configurare una caratteristica del server MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet di Windows PowerShell per configurare le caratteristiche del server MBAM.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Per configurare i report tramite Windows PowerShell**

1.  Prima di avviare la configurazione, vedere [configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) per esaminare i prerequisiti per l'uso di Windows PowerShell.

2.  Usare il cmdlet **Enable-MbamReport** di Windows PowerShell per configurare i report. Per ottenere informazioni su questo cmdlet di Windows PowerShell, digitare **Get-Help Enable-MbamReport**.

**Per configurare i report tramite la procedura guidata**

1. Nel server in cui si vogliono configurare i report avviare la configurazione guidata del **Server mbam** . È possibile selezionare la **configurazione di mbam server** dal menu **Start** per aprire la procedura guidata.

2. Fare clic su **Aggiungi nuove funzionalità**, selezionare **report**e quindi fare clic su **Avanti**. La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per i report.

3. Fai clic su **Next** per continuare.

4. Usando le descrizioni seguenti, immettere i valori dei campi nella procedura guidata:

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
   <td align="left"><p><strong>Istanza di SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>Istanza di SQL Server Reporting Services in cui verranno configurati i report.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Gruppo di Domain Role Reporting</strong></p></td>
   <td align="left"><p>Nome del gruppo Domain Users i cui membri hanno diritti di accesso ai report nel server di amministrazione e monitoraggio.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nome di SQL Server</strong></p></td>
   <td align="left"><p>Nome del server in cui è configurato il database di conformità e controllo.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Istanza di database di SQL Server</strong></p></td>
   <td align="left"><p>Nome dell'istanza di SQL Server, ad esempio MSSQLSERVER, <em> in </em> cui è configurato il database di conformità e controllo.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>È necessario aggiungere un'eccezione nel computer report per abilitare il traffico in ingresso sulla porta del server di report (la porta predefinita è 80).</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Nome database</strong></p></td>
   <td align="left"><p>Nome del database di conformità e controllo. Per impostazione predefinita, il nome del database è <strong> lo stato di conformità di mbam </strong> , anche se è possibile modificare il nome quando si configura il database di conformità e controllo.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Se si esegue l'aggiornamento da una versione precedente di MBAM, è necessario usare lo stesso nome del database del nome usato nella distribuzione precedente.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Account di dominio del database di conformità e audit</strong></p></td>
   <td align="left"><p>Account utente e password di dominio per accedere al database di conformità e controllo.</p>
   <p>Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un utente, è necessario immettere lo stesso valore in questo campo.</p>
   <p>Se il valore immesso nell' <strong> utente o nel campo di gruppo di Access di sola lettura nella </strong> <strong> pagina Configura database </strong> è un gruppo, il valore immesso in questo campo deve essere un membro del gruppo.</p>
   <p>Configurare la password per l'account per non scadere mai. L'account utente dovrebbe essere in grado di accedere a tutti i dati disponibili per il gruppo di utenti di MBAM Reports.</p></td>
   </tr>
   </tbody>
   </table>



5. Dopo aver completato le voci, fare clic su **Avanti**.

   La procedura guidata controlla che siano stati soddisfatti tutti i prerequisiti per la caratteristica report.

6. Fai clic su **Next** per continuare.

7. Nella pagina **Riepilogo** esaminare le caratteristiche che verranno aggiunte.

   **Nota**  
   Per creare uno script di Windows PowerShell delle voci appena effettuate, fare clic su **Esporta script di PowerShell**e quindi salvare lo script.



8. Fare clic su **Aggiungi** per aggiungere i report nel server e quindi fare clic su **Chiudi**.



## Argomenti correlati


[Registri eventi del server](server-event-logs.md)

[Configurazione delle funzionalità server di MBAM 2.5](configuring-the-mbam-25-server-features.md)

[Come configurare le applicazioni Web di MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Convalida della configurazione delle funzionalità del server di MBAM 2.5](validating-the-mbam-25-server-feature-configuration.md)


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






