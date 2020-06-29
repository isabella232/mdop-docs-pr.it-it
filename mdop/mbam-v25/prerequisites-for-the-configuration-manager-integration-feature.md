---
title: Prerequisiti per la funzionalità di integrazione di Configuration Manager
description: Prerequisiti per la funzionalità di integrazione di Configuration Manager
author: dansimp
ms.assetid: b318cbd3-b009-44b8-991b-f7364c1cae88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af7abd50f6218810dd6718f091512b48fee32652
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825015"
---
# Prerequisiti per la funzionalità di integrazione di Configuration Manager


Se si distribuisce MBAM con la topologia di integrazione di System Center Configuration Manager, è consigliabile un'architettura a tre server, come descritto in [architettura di alto livello di mbam 2,5 con la topologia di integrazione di Configuration Manager](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md). Questa architettura può supportare i computer client di 500.000.

**Importante**  
Windows to go non è supportato per l'installazione della topologia di integrazione di Configuration Manager quando si usa Configuration Manager 2007.



## Prerequisiti generali per la funzionalità di integrazione di Configuration Manager


Quando si installa MBAM con Configuration Manager, sono necessari i prerequisiti aggiuntivi seguenti, oltre ai prerequisiti per la topologia autonoma.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prerequisiti</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Il Server Configuration Manager è un sito principale nel sistema di gestione configurazione.</p></td>
<td align="left"><p>N/D</p></td>
</tr>
<tr class="even">
<td align="left"><p>L'agente client Inventory hardware si trova nel server Configuration Manager.</p></td>
<td align="left"><p>Per System Center 2012 Configuration Manager, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> come configurare l'inventario hardware in Gestione configurazione </a> .</p>
<p>Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> come configurare l'inventario hardware per un sito </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Una delle opzioni seguenti è abilitata, a seconda della versione di Configuration Manager in uso:</p>
<ul>
<li><p>Impostazioni di conformità-(System Center 2012 Configuration Manager)</p></li>
<li><p>Agente client di gestione della configurazione (DCM) desiderato-(Configuration Manager 2007)</p></li>
</ul></td>
<td align="left"><p>Per Gestione configurazione di System Center 2012, vedere configurazione <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> delle impostazioni di conformità in Gestione configurazione </a> .</p>
<p>Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> proprietà dell'agente client di gestione della configurazione desiderata </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Un punto di Reporting Services è definito in Configuration Manager. Obbligatorio per SQL Server Reporting Services (SSRS).</p></td>
<td align="left"><p>Per Gestione configurazione di System Center 2012, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> prerequisiti per la creazione di report in Configuration Manager </a> .</p>
<p>Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> come creare un punto di Reporting Services per SQL Reporting Services </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuration Manager 2007 richiede Microsoft .NET Framework 2,0</p></td>
<td align="left"><p>L'agente client di gestione della configurazione (DCM) desiderato in Configuration Manager 2007 richiede .NET Framework 2,0 per segnalare la conformità.</p>
<div class="alert">
<strong>Nota</strong><br/><p>L'installazione di .NET Framework 3,5 viene installata automaticamente in .NET Framework 2,0.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Autorizzazioni necessarie per installare MBAM con Configuration Manager


Per installare MBAM con Configuration Manager, è necessario disporre di un utente amministrativo in Configuration Manager che disponga di un ruolo di sicurezza con le autorizzazioni minime elencate nella tabella seguente. La tabella mostra anche i diritti che è necessario avere, oltre ai diritti di amministratore di Basic computer, per installare il server MBAM.

**Le autorizzazioni nella tabella seguente sono valide per entrambe le versioni di Configuration Manager.**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Autorizzazioni</th>
<th align="left">Funzionalità del server MBAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ruoli del server di accesso istanza di SQL Server:-dbcreator-processadmin</p></td>
<td align="left"><p>- Database di ripristino-database di controllo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Diritti istanza SSRS:-creare cartelle-pubblicare report</p></td>
<td align="left"><p>- Integrazione di System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**System Center 2012 Configuration Manager**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Autorizzazioni</th>
<th align="left">Funzionalità del Server Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Diritti del sito di Configuration Manager:-Read</p></td>
<td align="left"><p>Integrazione di System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Diritti di raccolta di Configuration Manager:-Crea-Elimina-leggi-modifica-Distribuisci elementi di configurazione</p></td>
<td align="left"><p>Integrazione di System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Diritti degli elementi di configurazione di Configuration Manager:-Crea-Elimina-leggi</p></td>
<td align="left"><p>Integrazione di System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



**Configuration Manager 2007**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Autorizzazioni</th>
<th align="left">Funzionalità del Server Configuration Manager</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Diritti del sito di Configuration Manager:-Read</p></td>
<td align="left"><p>Integrazione di System Center Configuration Manager</p></td>
</tr>
<tr class="even">
<td align="left"><p>Diritti di raccolta di Configuration Manager:-Crea-Elimina-leggi-ReadResource</p></td>
<td align="left"><p>Integrazione di System Center Configuration Manager</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Diritti degli elementi di configurazione di Configuration Manager:-Crea-Elimina-leggi-Distribuisci</p></td>
<td align="left"><p>Integrazione di System Center Configuration Manager</p></td>
</tr>
</tbody>
</table>



## Modifiche obbligatorie per i file MOF


Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file Configuration. mof e il file SMS \ _def. mof per System Center 2012 Configuration Manager e Microsoft System Center Configuration Manager 2007. Per istruzioni, Vedi [i prerequisiti del server MBAM 2,5 che si applicano solo alla topologia di integrazione di Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md).



## Argomenti correlati


[Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

[Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)



## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





