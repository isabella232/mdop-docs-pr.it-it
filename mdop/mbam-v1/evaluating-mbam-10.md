---
title: Valutazione di MBAM 1.0
description: Valutazione di MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825255"
---
# Valutazione di MBAM 1.0


Prima di distribuire l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) in un ambiente di produzione, è consigliabile valutarlo in un ambiente lab. È possibile usare le informazioni contenute in questo argomento per configurare MBAM in un unico ambiente di Lab server solo per scopi di valutazione.

Mentre i passaggi di distribuzione effettivi sono molto simili allo scenario descritto in [come installare e configurare mbam in un singolo server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), questo argomento contiene informazioni aggiuntive che consentono di configurare un ambiente di valutazione di MBAM nel minor tempo possibile.

## Configurare l'ambiente lab


Anche quando si configura un'istanza non di produzione di MBAM per la valutazione in un ambiente lab, è comunque necessario verificare che siano stati soddisfatti i prerequisiti per la distribuzione e i requisiti hardware e software. Per altre informazioni, Vedi [mbam 1,0 prerequisiti](mbam-10-deployment-prerequisites.md) per la distribuzione e [MBAM 1,0 configurazioni supportate](mbam-10-supported-configurations.md). Si dovrebbe anche rivedere la [preparazione dell'ambiente per mbam 1,0 prima di](preparing-your-environment-for-mbam-10.md) iniziare la distribuzione di valutazione mbam.

### Pianificare una distribuzione di valutazione di MBAM

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
<td align="left"><p>Esaminare le informazioni introduttive su MBAM per ottenere una conoscenza di base del prodotto prima di iniziare la pianificazione della distribuzione.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)">Attività iniziali di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p>Preparare l'ambiente di elaborazione per l'installazione di MBAM. A questo scopo, devi abilitare la crittografia dati trasparente (Transparent Data Encryption) sulle istanze di SQL Server che ospiteranno i database di MBAM. Per abilitare la funzione Transparent nell'ambiente lab, è possibile creare un file con estensione SQL da eseguire sul database master ospitato nell'istanza di SQL Server che verrà usato da MBAM.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Puoi usare l'esempio seguente per creare un file con estensione SQL per l'ambiente lab in modo da abilitare rapidamente Transparent per l'istanza di SQL Server che ospita i database di MBAM. Questi comandi di SQL Server consentiranno a transparent di usare un certificato SQL Server firmato localmente. Assicurarsi di eseguire il backup del certificato di transcodificazione e della chiave di crittografia associata nel percorso di backup locale di esempio di <em> C:\backup </em> . Il certificato e la chiave di transcodificazione dati sono necessari per recuperare il database o per trasferire il certificato e la chiave in un altro server con crittografia transattiva.</p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)">Prerequisiti per la distribuzione di MBAM 1.0</a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)">Crittografia di database in SQL Server 2008 Enterprise Edition</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare e configurare i requisiti dei criteri di gruppo di MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)">Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare e creare i gruppi di sicurezza di servizi di dominio Active Directory necessari e pianificare i requisiti per i membri del gruppo di sicurezza locale di MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Pianificazione dei ruoli di amministrazione di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare la distribuzione delle funzionalità di MBAM server.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)">Pianificazione della distribuzione del server di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare la distribuzione di MBAM client.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)">Pianificazione della distribuzione del client di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Eseguire una distribuzione di valutazione MBAM

Dopo aver completato le installazioni necessarie per la pianificazione e il software prerequisito per preparare l'ambiente di elaborazione per un'installazione di MBAM, è possibile iniziare la distribuzione di valutazione di MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione della funzionalità MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Configurazioni supportate di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Eseguire la configurazione di MBAM per distribuire le funzionalità di MBAM server su un singolo server a scopo di valutazione.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)">Come installare e configurare MBAM in un server singolo</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Aggiungere i gruppi di sicurezza di Active Directory Domain Services creati durante la fase di pianificazione per i gruppi locali appropriati di MBAM server locale nel nuovo server MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Pianificazione per i ruoli di amministratore di MBAM 1,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> come gestire i ruoli di amministratore di mbam</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Distribuire il software del client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Distribuzione del client MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Configurare computer lab per la valutazione di MBAM


È possibile modificare le impostazioni di frequenza nella segnalazione dello stato di MBAM client usando l'editor del registro di sistema. Queste modifiche devono tuttavia essere usate solo per scopi di test.

**Warning**  
Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema. Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows. Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat). Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti. Cambiare il registro di sistema a proprio rischio.



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a>Modificare le impostazioni di frequenza nella segnalazione di stato del client MBAM

Le frequenze di attivazione e segnalazione dello stato di MBAM client hanno un valore minimo di 90 minuti quando sono impostate per l'uso dei criteri di gruppo. Puoi modificare queste frequenze nei computer client di MBAM modificando il registro di sistema di Windows in valori più bassi, per velocizzare i test. Per modificare le impostazioni di frequenza nella segnalazione dello stato di MBAM client, usare un editor del registro di sistema per passare a **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, modificare i valori di **ClientWakeupFrequency** e **StatusReportingFrequency** su **1** come valore minimo supportato dal client e quindi riavviare il servizio client di gestione di BitLocker. Quando si apporta questa modifica, il client MBAM segnala ogni minuto. Puoi impostare i valori così bassi solo quando lo fai manualmente nel registro di sistema.

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a>Modificare il ritardo di avvio del servizio client MBAM

Oltre alle frequenze di attivazione e segnalazione dello stato di MBAM client, c'è un ritardo casuale fino a 90 minuti quando il servizio agente client MBAM viene avviato nei computer client. Se non si vuole che il ritardo casuale, creare un valore **DWORD** di **NoStartupDelay** in **HKLM\\Software\\Microsoft\\MBAM**, impostarne il valore su **1**e quindi riavviare il servizio client di gestione di BitLocker.

## Argomenti correlati


[Attività iniziali di MBAM 1.0](getting-started-with-mbam-10.md)









