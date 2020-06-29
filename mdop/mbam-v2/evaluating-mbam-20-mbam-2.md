---
title: Valutazione di MBAM 2.0
description: Valutazione di MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824736"
---
# Valutazione di MBAM 2.0


Prima di distribuire Microsoft BitLocker Administration and Monitoring (MBAM) in un ambiente di produzione, è consigliabile valutarlo in un ambiente di test. Le informazioni contenute in questo argomento possono essere usate per configurare l'amministrazione e il monitoraggio di Microsoft BitLocker con una topologia autonoma in un ambiente di test a server singolo per scopi di valutazione. Una topologia a server singolo non è consigliata per gli ambienti di produzione.

Per istruzioni sulla distribuzione di MBAM in un ambiente di test, vedere [come installare e configurare mbam in un singolo server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).

## Configurazione dell'ambiente di test


Anche se si sta configurando un'istanza non di produzione di MBAM per la valutazione in un ambiente di test, è comunque necessario verificare che siano stati soddisfatti i prerequisiti e i requisiti hardware e software. Prima di avviare l'installazione, vedere [mbam 2,0 prerequisiti di distribuzione](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 configurazioni supportate](mbam-20-supported-configurations-mbam-2.md)e [preparare l'ambiente per MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).

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
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)">Attività iniziali di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare i prerequisiti per la distribuzione di MBAM 2,0 e preparare l'ambiente di elaborazione.</p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)">Prerequisiti per la distribuzione di MBAM 2.0</a></p></td>
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
<td align="left"><p>Pianificare e creare gruppi di sicurezza di ActiveDirectoryDomainServices necessari e pianificare i requisiti per i membri del gruppo di sicurezza locale di MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Pianificazione dei ruoli di amministrazione di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare la distribuzione della funzionalità MBAM Server Deployment.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)">Pianificazione della distribuzione del server di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Pianificare la distribuzione di MBAM Client Deployment.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Pianificazione della distribuzione del client di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### Eseguire una distribuzione di valutazione MBAM

Dopo aver completato le necessarie installazioni per la pianificazione e il software prerequisito per preparare l'ambiente di calcolo per l'installazione di MBAM, è possibile iniziare la distribuzione di valutazione MBAM.

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
<td align="left"><p>Esaminare le informazioni sulle configurazioni supportate da MBAM per verificare che i computer client e server selezionati siano supportati per l'installazione delle funzionalità di MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Configurazioni supportate di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Eseguire la configurazione di MBAM per distribuire le funzionalità di MBAM server su un singolo server a scopo di valutazione.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)">Come installare e configurare MBAM in un server singolo</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Aggiungere gruppi di sicurezza di ActiveDirectoryDomainServices, creati durante la fase di pianificazione, per i gruppi locali appropriati di MBAM server locale nel nuovo server MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Pianificazione per i ruoli di amministratore di MBAM 2,0 </a> e <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> come gestire i ruoli di amministratore di mbam</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Creare e distribuire gli oggetti necessari per i criteri di gruppo di MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Distribuire il software del client MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Distribuzione del client MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Configurare computer lab per la valutazione di MBAM


Questa sezione contiene informazioni che possono essere usate per velocizzare la segnalazione dello stato di MBAM client. Queste modifiche devono tuttavia essere usate solo per scopi di test.

**Nota**  Le informazioni nella sezione seguente illustrano come modificare il registro di sistema di Windows. L'uso errato dell'editor del registro di sistema può causare seri problemi che potrebbero richiedere la reinstallazione di Windows. Microsoft non può garantire che i problemi causati dall'uso errato dell'editor del registro di sistema possano essere risolti. Usare l'editor del registro di sistema a proprio rischio.

 

### Modificare le impostazioni di frequenza di segnalazione dello stato del client MBAM

Le frequenze di attivazione e segnalazione dello stato di MBAM client hanno un valore minimo di 90 minuti quando vengono impostate tramite criteri di gruppo. Puoi usare il registro di sistema di Windows per modificare queste frequenze in un valore inferiore nei computer client di MBAM per velocizzare i test.

Per modificare le impostazioni di frequenza per la segnalazione dello stato del client MBAM:

1.  Usare un editor del registro di sistema per passare a **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.

2.  Modificare i valori di **ClientWakeupFrequency** e **StatusReportingFrequency** su **1** come valore minimo supportato dal client. Questa modifica fa sì che il client MBAM riferisca ogni minuto.

3.  Riavviare il **servizio client di gestione di BitLocker**.

**Nota**  Per impostare valori così bassi, è necessario impostarli manualmente nel registro di sistema.

 

### Modificare il ritardo di avvio del servizio client MBAM

Oltre alle frequenze di attivazione e segnalazione dello stato di MBAM client, c'è un ritardo casuale fino a 90 minuti quando il servizio agente client MBAM viene avviato nei computer client. Se non si vuole che il ritardo casuale, creare un valore **DWORD** di **NoStartupDelay** in **HKLM\\Software\\Microsoft\\MBAM**, impostarne il valore su **1**e quindi riavviare il **servizio client di gestione di BitLocker**.

## Argomenti correlati


[Attività iniziali di MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





