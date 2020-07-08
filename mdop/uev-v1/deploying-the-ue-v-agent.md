---
title: Distribuzione dell'agente di UE-V
description: Distribuzione dell'agente di UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827185"
---
# Distribuzione dell'agente di UE-V


L'agente Microsoft User Experience Virtualization (UE-V) deve essere eseguito in ogni computer che USA UE-V per aggirare le impostazioni dell'applicazione e di Windows. Un singolo file del programma di installazione, AgentSetup.exe, installa l'agente UE-V nei sistemi operativi 32 bit e 64 bit. I parametri della riga di comando dell'agente UE-V sono i seguenti:

**AgentSetup.exe parametri della riga di comando**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Parametro della riga di comando</strong></th>
<th align="left"><strong>Definizione</strong></th>
<th align="left"><strong>Note</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help o/h o/?</p></td>
<td align="left"><p>Visualizza la finestra di dialogo AgentSetup.exe utilizzo.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indica il percorso UNC (Universal Naming Convention) che definisce la posizione in cui sono archiviate le impostazioni.</p></td>
<td align="left"><p>vengono accettate le variabili di ambiente% nomeutente% o% nomecomputer%. Gli script possono richiedere variabili di escape.</p>
<p><strong>Impostazione predefinita </strong> : &lt; None &gt; (Home utente di Active Directory)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indica il percorso UNC (Universal Naming Convention) che definisce la posizione selezionata per i nuovi modelli di posizione delle impostazioni.</p></td>
<td align="left"><p>Obbligatorio solo per i modelli di posizione delle impostazioni personalizzate</p></td>
</tr>
<tr class="even">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Specifica se i modelli Microsoft predefiniti devono essere registrati durante l'installazione.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Impostazione predefinita </strong> : vero</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Specifica il metodo di sincronizzazione da usare.</p></td>
<td align="left"><p>OfflineFiles | Nessuno</p>
<p><strong>Impostazione predefinita </strong> : offlinefiles</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Specifica il numero di millisecondi che il computer attende prima del timeout quando recupera le impostazioni utente dalla posizione di archiviazione delle impostazioni.</p></td>
<td align="left"><p><strong>Impostazione predefinita </strong> : 2000 millisecondi</p>
<p>(attendere fino a 2 secondi)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Specifica se la sincronizzazione UE-V è abilitata o disabilitata.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Impostazione predefinita </strong> : vero</p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Specifica una dimensione del file del pacchetto di impostazioni in byte quando l'agente UE-V segnala che i file superano la soglia.</p></td>
<td align="left"><p>&lt;dimensioni&gt;</p>
<p><strong>Default </strong> : None (nessuna soglia di avviso)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Specifica l'impostazione per la partecipazione al programma Analisi utilizzo software. Se impostato su true, le informazioni sul programma di installazione vengono caricate nel sito Microsoft Customer Experience Improvement Program. Se impostato su false, non vengono caricate informazioni.</p></td>
<td align="left"><p>True | False</p>
<p><strong>Impostazione predefinita </strong> : false</p>
<p><strong>In Windows 7 </strong> : vero</p></td>
</tr>
</tbody>
</table>

 

Durante l'installazione, il parametro della riga di comando SettingsStoragePath specifica la posizione di archiviazione delle impostazioni per i valori delle impostazioni. Una posizione di archiviazione delle impostazioni può essere definita prima della distribuzione dell'agente UE-V. Se non è stata definita la posizione di archiviazione delle impostazioni, quindi UE-V usa la directory Home dell'utente di Active Directory come posizione di archiviazione delle impostazioni. Quando si specifica la configurazione di SettingsStoragePath durante l'installazione e si usa% username% come parte del valore, la stessa esperienza delle impostazioni utente verrà aggirata in tutti i computer o le sessioni in cui un utente accede. Se specifichi le variabili%UserName%\\%ComputerName% come parte del valore SettingsStoragePath, questo consentirà di mantenere l'esperienza delle impostazioni per ogni computer.

I file di Windows Installer (MSI) specifici dell'architettura vengono forniti per l'installazione dell'agente UE-V oltre al programma di installazione combinato a 32 bit e a 64 bit. I file di installazione AgentSetupx86.msi o AgentSetupx64.msi sono più piccoli del file AgentSetup.exe e potrebbero semplificare le distribuzioni degli agenti. I parametri della riga di comando per il programma di installazione di AgentSetup.exe sono supportati per l'installazione di Windows Installer (MSI).

**Nota**  Durante l'installazione o la disinstallazione dell'agente UE-V è possibile usare il file AgentSetup.exe o il &lt; &gt; file Arch. msi di AgentSetup, ma non entrambi. Lo stesso file deve essere usato per disinstallare l'agente UE-V quando è stato usato per installare l'agente UE-V.

 

Assicurarsi di usare il formato di variabile corretto quando si installa l'agente UE-V. La tabella seguente contiene esempi di opzioni di distribuzione per l'uso dei file di installazione AgentSetup.exe o Windows Installer (MSI).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Tipo di distribuzione</strong></th>
<th align="left"><strong>Descrizione della distribuzione</strong></th>
<th align="left"><strong>Esempio</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Prompt dei comandi</p></td>
<td align="left"><p>Quando si installa l'agente UE-V da un prompt dei comandi, usare il formato di variabile% ^ nomeutente%. Se sono necessarie le virgolette a causa di spazi nel percorso di archiviazione delle impostazioni, usare un file di script batch per la distribuzione.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script batch</p></td>
<td align="left"><p>Quando si installa l'agente UE-V da un file di script batch, usare il formato di variabile%% nomeutente%%. Se si usa questo metodo di installazione, è necessario sfuggire alla variabile con i caratteri%%. Senza questo carattere, lo script espande la variabile username al momento dell'installazione, invece che in fase di esecuzione, causando l'uso di una singola posizione di archiviazione delle impostazioni per tutti gli utenti con UE-V.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Quando si installa l'agente UE-V da un prompt di PowerShell o da uno script di PowerShell, usare il formato variabile% nomeutente%.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribuzione elettronica del software, ad esempio distribuzione della distribuzione del software di Configuration Manager</p></td>
<td align="left"><p>Quando si installa l'agente UE-V con Configuration Manager, usare il formato di variabile ^% nomeutente ^%.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

**Nota**  L'installazione dell'agente U-EV richiede i diritti di amministratore e il computer richiederà un riavvio prima che l'agente UE-V possa essere eseguito.

 

## Metodi di distribuzione di agenti UE-V da una condivisione di rete


Puoi usare i metodi seguenti per distribuire l'agente UE-V:

-   Soluzione ESD (Electronic Software Distribution) che può installare un file di Windows Installer (con estensione msi).

-   Uno script di installazione che fa riferimento al file di Windows Installer (con estensione msi) archiviato centralmente in una condivisione.

-   Eseguire manualmente il programma di installazione nel computer.

Per distribuire l'agente UE-V da una condivisione di rete, eseguire la procedura seguente:

**Per installare e configurare l'agente UE-V da una condivisione di rete**

1.  Eseguire il file di installazione dell'agente UE-V (AgentSetup.exe) in una condivisione di rete a cui gli utenti hanno l'autorizzazione "Leggi".

2.  Distribuire uno script nei computer degli utenti che installano l'agente UE-V. Lo script deve specificare la posizione di archiviazione delle impostazioni.

**Aggiornare l'agente UE-V**

Gli aggiornamenti per il software dell'agente UE-V verranno forniti tramite Microsoft Update. Durante l'aggiornamento dell'agente UE-V, il gruppo predefinito dei modelli di posizione delle impostazioni per le comuni applicazioni Microsoft e le impostazioni di Windows può essere aggiornato. Gli aggiornamenti dell'agente UE-V possono essere distribuiti usando l'infrastruttura ESD (Enterprise Software Distribution).

## Argomenti correlati


[Distribuzione di UE-V 1.0](deploying-ue-v-10.md)

[Configurazioni supportate per UE-V 1.0](supported-configurations-for-ue-v-10.md)

[Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Installazione di Generatore UE-V](installing-the-ue-v-generator.md)

Distribuire l'agente di virtualizzazione dell'esperienza utente
 

 





