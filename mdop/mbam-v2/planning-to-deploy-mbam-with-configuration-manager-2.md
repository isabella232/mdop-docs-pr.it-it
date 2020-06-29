---
title: Pianificazione della distribuzione di MBAM con Configuration Manager
description: Pianificazione della distribuzione di MBAM con Configuration Manager
author: dansimp
ms.assetid: fb768306-48c2-40b4-ac4e-c279db987391
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e8588ce03c86a8a5138d591327e5f95503dce5ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825626"
---
# Pianificazione della distribuzione di MBAM con Configuration Manager


Per distribuire MBAM con la topologia di Configuration Manager, è consigliata un'architettura a tre server, che supporta i client di 200.000. Usare un server separato per eseguire Configuration Manager e installare le funzionalità di amministrazione e monitoraggio di base su due server, come illustrato nell'immagine dell'architettura in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).

**Importante**  
Windows to go non è supportato quando si installa la topologia integrata di MBAM con Configuration Manager 2007.



## Prerequisiti di distribuzione per l'installazione di MBAM con Configuration Manager


Verificare di avere soddisfatto i prerequisiti seguenti prima di installare MBAM con Configuration Manager:

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
<td align="left"><p>Verificare che il Server Configuration Manager sia un sito principale nel sistema di Configuration Manager.</p></td>
<td align="left"><p>N/D</p></td>
</tr>
<tr class="even">
<td align="left"><p>Abilitare l'agente client Inventory hardware nel server Configuration Manager.</p></td>
<td align="left"><p>Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301656" data-raw-source="[How to Configure Hardware Inventory for a Site](https://go.microsoft.com/fwlink/?LinkId=301656)"> come configurare l'inventario hardware per un sito </a> .</p>
<p>Per System Center 2012 Configuration Manager, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301685" data-raw-source="[How to Configure Hardware Inventory in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301685)"> come configurare l'inventario hardware in Gestione configurazione </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Abilitare l'agente di gestione della configurazione (DCM) o le impostazioni di conformità, a seconda della versione di Configuration Manager in uso.</p></td>
<td align="left"><p>Per Configuration Manager 2007, abilitare la visualizzazione delle <a href="https://go.microsoft.com/fwlink/?LinkId=301686" data-raw-source="[Desired Configuration Management Client Agent Properties](https://go.microsoft.com/fwlink/?LinkId=301686)"> proprietà dell'agente client di gestione della configurazione desiderata </a> .</p>
<p>Per Gestione configurazione di System Center 2012, vedere configurazione <a href="https://go.microsoft.com/fwlink/?LinkId=301687" data-raw-source="[Configuring Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301687)"> delle impostazioni di conformità in Gestione configurazione </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Definire un punto di Reporting Services in Configuration Manager. Obbligatorio per SQL Reporting Services.</p></td>
<td align="left"><p>Per Configuration Manager 2007, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301688" data-raw-source="[How to Create a Reporting Services Point for SQL Reporting Services](https://go.microsoft.com/fwlink/?LinkId=301688)"> come creare un punto di Reporting Services per SQL Reporting Services </a> .</p>
<p>Per Gestione configurazione di System Center 2012, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=301689" data-raw-source="[Prerequisites for Reporting in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=301689)"> prerequisiti per la creazione di report in Configuration Manager </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="---------configuration-manager-supported-versions"></a> Versioni supportate di Configuration Manager


MBAM supporta le versioni seguenti di Configuration Manager:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione supportata</th>
<th align="left">Service Pack</th>
<th align="left">Architettura di sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft System Center Configuration Manager 2007 R2</p></td>
<td align="left"><p>SP1 o versione successiva</p></td>
<td align="left"><p>64 bit</p>
<div class="alert">
<strong>Nota</strong><br/><p>Anche se Configuration Manager 2007 è 32 bit, è necessario installarlo e SQL Server in un sistema operativo a 64 bit per far corrispondere il software MBAM a 64 bit.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Gestione configurazione di Microsoft System Center 2012</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
</tr>
</tbody>
</table>



Per un elenco delle configurazioni supportate per il Server Configuration Manager, vedere la pagina Web appropriata per la versione di Configuration Manager in uso. MBAM non ha requisiti di sistema aggiuntivi per il Server Configuration Manager.

## <a href="" id="---------mbam-and-sql-server-system-requirements"></a> Requisiti di sistema MBAM e SQL Server


Le configurazioni e i requisiti di sistema supportati per i server MBAM e SQL Server per la topologia di Configuration Manager corrispondono a quelli per la topologia autonoma. Per i requisiti di sistema autonomi, Vedi le [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md). Per gli uffici MBAM server e SQL Server Processor, RAM e spazio su disco per la topologia di Configuration Manager, vedere le sezioni seguenti.

## MBAM Server Processor, RAM e spazio su disco requisiti per MBAM


Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco per i server MBAM quando si usa la topologia di integrazione di Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Responsabile del trattamento</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o superiore</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spazio disponibile su disco</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>



## Requisiti per processori, RAM e spazio su disco per SQL Server


Nella tabella seguente sono elencati i requisiti per il processore, la RAM e lo spazio su disco del server per il computer SQL Server quando si usa la topologia di integrazione di Configuration Manager.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente hardware</th>
<th align="left">Requisito minimo</th>
<th align="left">Requisito consigliato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Responsabile del trattamento</p></td>
<td align="left"><p>2,33 GHz</p></td>
<td align="left"><p>2,33 GHz o superiore</p></td>
</tr>
<tr class="even">
<td align="left"><p>RAM</p></td>
<td align="left"><p>4 GB</p></td>
<td align="left"><p>8 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Spazio disponibile su disco</p></td>
<td align="left"><p>5 GB</p></td>
<td align="left"><p>5 GB o superiore</p></td>
</tr>
</tbody>
</table>



## Autorizzazioni necessarie per installare il server MBAM


Per installare MBAM con Configuration Manager, è necessario disporre di un utente amministrativo in Configuration Manager che disponga di un ruolo di sicurezza con le autorizzazioni minime elencate nella tabella seguente. La tabella mostra anche i diritti che è necessario avere, oltre ai diritti di amministratore di Basic computer, per installare il server MBAM.

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
<td align="left"><p>Ruoli del server di accesso alle istanze SQL:-dbcreator-processadmin</p></td>
<td align="left"><p>- Database di ripristino-database di controllo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Diritti di istanza di SQL Server Reporting Services:-creare cartelle-pubblicare report</p></td>
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



## Ordine di distribuzione delle funzionalità di MBAM per la topologia di Configuration Manager


Quando si distribuisce MBAM nel server Configuration Manager, è necessario completare le attività di distribuzione nell'ordine seguente:

1.  Modificare il file Configuration. mof nel server Configuration Manager.

2.  Creare o modificare il server di gestione configurazione file SMS \ _def. mof.

3.  Installare MBAM nel server Configuration Manager.

4.  Installare il database di ripristino e il database di controllo nel server di database.

5.  Installare le funzionalità di MBAM nel server di amministrazione e monitoraggio.

## Elenco di controllo pianificazione per l'installazione di MBAM con Configuration Manager


Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da considerare quando si pianifica una distribuzione di amministrazione e monitoraggio di Microsoft BitLocker con Configuration Manager. È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Attività</th>
<th align="left">Riferimenti</th>
<th align="left">Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Esaminare le informazioni introduttive, che illustrano la modalità di funzionamento di Configuration Manager con MBAM e l'architettura di alto livello consigliata.</p></td>
<td align="left"><p><a href="getting-started---using-mbam-with-configuration-manager.md" data-raw-source="[Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md)">Attività iniziali: uso di MBAM con Configuration Manager</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Esaminare le informazioni di pianificazione, che descrivono i prerequisiti di distribuzione, le configurazioni supportate, le autorizzazioni necessarie e l'ordine di distribuzione per ogni caratteristica.</p></td>
<td align="left"><p>Pianificazione della distribuzione di MBAM con Configuration Manager</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare e configurare i requisiti dei criteri di gruppo di MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare e creare gruppi di sicurezza di servizi di dominio Active Directory necessari e pianificare i requisiti per i membri del gruppo di sicurezza locale di MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Pianificazione dei ruoli di amministrazione di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare la distribuzione di MBAM Client Deployment.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Pianificazione della distribuzione del client di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Uso di MBAM con Configuration Manager](using-mbam-with-configuration-manager.md)









