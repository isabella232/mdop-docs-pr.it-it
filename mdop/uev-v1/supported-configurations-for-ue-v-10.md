---
title: Configurazioni supportate per UE-V 1.0
description: Configurazioni supportate per UE-V 1.0
author: dansimp
ms.assetid: d90ab83e-741f-48eb-b1d8-a64cb9259f7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a84514317de8a4cfd9df9c94a9a130933b00874a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825555"
---
# Configurazioni supportate per UE-V 1.0


Microsoft User Experience Virtualization (UE-V) supporta le configurazioni descritte di seguito.

**Nota**  Microsoft fornisce il supporto per il Service Pack corrente e, in alcuni casi, il Service Pack precedente. Per trovare le sequenze temporali del supporto per il prodotto, vedere i [Service Pack supportati](https://go.microsoft.com/fwlink/p/?LinkId=31975)per il ciclo di vita. Per altre informazioni sui criteri del ciclo di vita del supporto Microsoft, vedere [domande frequenti sui criteri](https://go.microsoft.com/fwlink/p/?LinkId=31976)di supporto del supporto tecnico Microsoft.

 

## Configurazioni supportate per l'agente UE-V e il generatore di UE-V


La tabella seguente elenca i sistemi operativi che supportano il generatore di virtualizzazione dell'esperienza utente e l'agente di virtualizzazione dell'esperienza utente.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Sistema operativo</strong></th>
<th align="left"><strong>Edizione</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Architettura di sistema</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Ultimate, Enterprise o Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (Generatore)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, centro dati o server Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (Generatore)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Edizioni aziendali o professionali</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>32 o 64 bit</p></td>
<td align="left"><p>.NET Framework 4 o .NET Framework 3,5 SP1 (agente)</p>
<p>.NET Framework 4 (Generatore)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Nessuno</p></td>
<td align="left"><p>64 bit</p></td>
<td align="left"><p>.NET Framework 4 o .NET Framework 3,5 SP1 (agente)</p>
<p>.NET Framework 4 (Generatore)</p></td>
</tr>
</tbody>
</table>

 

Non sono previsti particolari requisiti di RAM specifici di UE-V.

L'installazione dell'agente UE-V richiede diritti amministrativi e richiederà il riavvio del computer prima che l'agente UE-V possa essere eseguito.

**Importante**  La caratteristica Sincronizza le impostazioni in Windows 8 deve essere disabilitata per consentire a UE-V di funzionare correttamente. La sincronizzazione delle impostazioni con Windows 8 e UE-V comporterà un comportamento di sincronizzazione imprevedibile.

 

### <a href="" id="requirements-for-the-offline-files-feature-"></a>Requisiti per la caratteristica file offline

L'agente UE-V può sincronizzare le impostazioni utente per i computer che non sono sempre connessi alla rete aziendale, ad esempio un computer portatile o computer che si trovano in uffici remoti, nonché i computer sempre connessi alla rete aziendale, ad esempio i server Windows che ospitano le sessioni di Virtual Desktop Interface (VDI).

La configurazione predefinita UE-V usa la funzionalità file offline di Windows per sincronizzare le impostazioni. I file offline garantiscono che le impostazioni dell'utente siano disponibili anche quando il computer esce dalla rete aziendale. Tutte le modifiche apportate alle impostazioni vengono sincronizzate automaticamente con la posizione di archiviazione delle impostazioni quando viene ristabilita la connessione alla rete aziendale. I file offline assicurano inoltre che le impostazioni dell'utente siano disponibili per i computer che si trovano in un ufficio remoto con una connessione lenta o limitata.

Per sincronizzare le impostazioni per i computer che lasciano occasionalmente la rete aziendale, la caratteristica file offline deve essere abilitata e avviata prima dell'inizio della distribuzione dell'agente UE-V. La funzionalità file offline è abilitata per impostazione predefinita in Windows7. La caratteristica è disabilitata per impostazione predefinita in Windows Server2008R2, Windows Server 2012 e Windows 8. Se la caratteristica file offline non è abilitata, la sincronizzazione delle impostazioni di UE-V non riuscirà.

-   **Windows 7**

    La funzionalità file offline è abilitata per impostazione predefinita in Windows 7. Se necessario, i file offline possono essere abilitati usando il comando seguente a un prompt dei comandi con privilegi elevati:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows 8**

    La funzionalità file offline è disabilitata per impostazione predefinita nella versione di Windows 8. I file offline possono essere abilitati in Windows 8 usando il comando seguente a un prompt dei comandi con privilegi elevati:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows Server 2008 R2 e Windows Server 2012**

    La caratteristica file offline non è installata per impostazione predefinita in Windows Server 2008 R2 o Windows Server 2012. Per abilitare la caratteristica file offline, è necessario che sia installato il pacchetto esperienza desktop. Si tratta di un componente server facoltativo che include la caratteristica file offline. Dopo l'installazione, avviare la caratteristica file offline con i comandi seguenti in un prompt dei comandi con privilegi elevati:

    ``` syntax
    sc config csc start= system
    ```

    ``` syntax
    sc config cscservice start= auto
    ```

Il computer deve essere riavviato prima che le impostazioni inizino a essere sincronizzate.

### Sincronizzazione per i computer con connessioni sempre disponibili

Quando si usa UE-V in computer sempre connessi alla rete aziendale, ad esempio un computer Windows Server che ospita sessioni VDI, i file offline devono essere disabilitati.

Quando l'agente UE-V è configurato per la sincronizzazione delle impostazioni senza usare i file offline, il server di archiviazione delle impostazioni viene considerato come una condivisione di rete standard. Le impostazioni vengono sincronizzate quando la rete è disponibile. In questa configurazione l'agente UE-V può essere configurato per ricevere una notifica se l'importazione delle impostazioni dell'applicazione è ritardata.

Se non viene usata la caratteristica file offline, è necessario disabilitare il comportamento predefinito di UE-V prima o durante la distribuzione dell'agente UE-V. Per disabilitare i file offline per l'UE-V, eseguire una delle operazioni seguenti:

-   Prima di distribuire l'agente UE-V, contrassegnare la casella di controllo "non usare i file offline" nell'impostazione di criteri di gruppo UE-V.

-   Durante l'installazione di UE-V, imposta il parametro AgentSetup.exe `SyncMethod = None` al prompt dei comandi o in un file batch. Per altre informazioni su come distribuire l'agente, vedere [distribuzione dell'agente UE-V](deploying-the-ue-v-agent.md).

Se si disattiva l'impostazione file offline per UE-V e non si specifica il parametro **SyncMethod** al momento dell'installazione, l'installazione dell'agente UE-v non riuscirà. È anche possibile disabilitare i file offline con PowerShell o WMI. Per altre informazioni sui comandi WMI e PowerShell, vedere [gestione dell'agente e dei pacchetti UE-V 1,0 con PowerShell e WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

Il computer deve essere riavviato prima che le impostazioni inizino a essere sincronizzate.

### Prerequisiti per la caratteristica di PowerShell UE-V

La caratteristica di PowerShell UE-V dell'agente richiede che .NET Framework versione 3,5 SP1 sia abilitato e PowerShell versione 2,0 o successiva.

### Prerequisiti per il supporto del generatore di UE-V

Installare il generatore UE-V nel computer usato per creare modelli di posizione delle impostazioni personalizzate. Questo computer dovrebbe avere le applicazioni installate le cui impostazioni andranno in roaming. È necessario essere un membro del gruppo Administrators nel computer in cui è in esecuzione il software Generator UE-V. Inoltre, il generatore UE-V deve essere installato in un computer che usa un file system NTFS. Il software Generator UE-V richiede .NET Framework versione 4. Per altre informazioni, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Argomenti correlati


[Pianificazione di UE-V 1.0](planning-for-ue-v-10.md)

[Preparazione dell'ambiente per UE-V](preparing-your-environment-for-ue-v.md)

[Distribuzione di UE-V 1.0](deploying-ue-v-10.md)

Configurazioni supportate per la virtualizzazione [dell'esperienza utente distribuzione della posizione di archiviazione delle impostazioni per UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Installazione di Generatore UE-V](installing-the-ue-v-generator.md)

[Distribuzione dell'agente di UE-V](deploying-the-ue-v-agent.md)

 

 





