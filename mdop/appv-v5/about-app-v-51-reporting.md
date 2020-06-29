---
title: Informazioni sulla creazione di report in App-V 5.1
description: Informazioni sulla creazione di report in App-V 5.1
author: dansimp
ms.assetid: 385dca00-7178-4e35-8d86-c58867ebd65c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 827343d538238ca638b57a74ae5d2d74bc6c5968
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814955"
---
# Informazioni sulla creazione di report in App-V 5.1

Microsoft Application Virtualization (App-V) 5,1 include una funzionalità di Reporting predefinita che consente di raccogliere informazioni sui computer che eseguono il client App-V 5,1 e informazioni sull'utilizzo del pacchetto di applicazioni virtuali. Puoi usare queste informazioni per generare report da un database centralizzato.

## <a href="" id="---------app-v-5-1-reporting-overview"></a> Panoramica delle relazioni di App-V 5,1

Nell'elenco seguente viene visualizzato il flusso di lavoro di alto livello end-to-end per la creazione di report in App-V 5,1.

1. Il server di report App-V 5,1 ha i prerequisiti seguenti:

    - Ruolo del server Web Internet Information Service (IIS)

    - Ruolo di autenticazione di Windows (in **IIS/sicurezza**)

    - SQL Server installato ed eseguito con SQL Server Reporting Services (SSRS)

    Per verificare che SQL Server Reporting Services sia in uso, visualizzare `http://localhost/Reports` in un Web browser come amministratore nel server che ospiterà la creazione di report di App-V 5,1. La Home page di SQL Server Reporting Services dovrebbe essere visualizzata.

2. Installare il server di report App-V 5,1 e il database associato. Per altre informazioni sull'installazione di Reporting Server, vedere [come installare il server di report in un computer autonomo e connetterlo al database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md). Configurare l'ora in cui il computer che ha eseguito il client App-V 5,1 deve inviare i dati al server di report.

3. Se non si usa un sistema di distribuzione software elettronico, ad esempio Configuration Manager, per visualizzare i report, è possibile definire i report in SQL Server Reporting Service. Scaricare i report SSRS predefiniti dall' [area download](https://go.microsoft.com/fwlink/?LinkId=397255).

    > [!NOTE]
    > Se si usa l'integrazione di Configuration Manager con App-V 5,1, la maggior parte dei report viene generata da Configuration Manager invece che da App-V 5,1.

4. Dopo aver importato il modulo di PowerShell App-V 5,1 usando `Import-Module AppvClient` come amministratore, abilitare il client App-v 5,1. Questo cmdlet di PowerShell di esempio Abilita la creazione di report App-V 5,1:

    ```powershell
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    Per inviare immediatamente i dati del report di App-V 5,1, eseguire `Send-AppvClientReport` il client App-v 5,1.

    Per altre informazioni sull'installazione del client App-V 5,1 con i report abilitati, vedere [informazioni sulle impostazioni di configurazione del client](about-client-configuration-settings51.md). Per amministrare la creazione di report di App-V 5,1 con Windows PowerShell, vedere [come abilitare la creazione di report nel client App-v 5,1 usando PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).

5. Dopo che il server di Reporting riceve i dati dal client App-V 5,1, invia i dati al database di report. Quando il database riceve ed elabora i dati client, viene inviata una risposta corretta al server di report e quindi viene inviata una notifica al client App-V 5,1.

6. Quando il client App-V 5,1 riceve la notifica di successo, svuota la cache di dati per risparmiare spazio.

    > [!NOTE]
    > Per impostazione predefinita, la cache viene deselezionata dopo che il server ha confermato la ricezione dei dati. È possibile configurare manualmente il client per salvare la cache di dati.

Se il dispositivo client App-V 5,1 non riceve una notifica di successo dal server, mantiene i dati nella cache e cerca di rinviare i dati all'intervallo configurato successivo. I client continuano a raccogliere dati e a aggiungerli alla cache.

### <a href="" id="-------------app-v-5-1-reporting-server-frequently-asked-questions"></a> Domande frequenti su App-V 5,1 Reporting Server

La tabella seguente mostra le risposte alle domande più frequenti sulla creazione di report di App-V 5,1

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Domanda</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Qual è la frequenza con cui vengono inviate le informazioni di segnalazione al database delle relazioni?</p></td>
<td align="left"><p>La frequenza dipende dal modo in cui l'attività di creazione di report è configurata nel computer in cui è in uso il client App-V 5,1. È necessario configurare la frequenza/intervallo per l'invio dei dati di report. La creazione di report di App-V 5,1 non è abilitata per impostazione predefinita.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Quali informazioni sono archiviate nel database del server di Reporting?</p></td>
<td align="left"><p>Nell'elenco seguente vengono visualizzati gli elementi archiviati nel database delle relazioni:</p>
<ul>
<li><p>Il sistema operativo in esecuzione nel computer che gestisce il client App-V 5,1: nome host, versione, Service Pack, tipo-client/server, architettura del processore.</p></li>
<li><p>Informazioni client App-V 5,1: versione.</p></li>
<li><p>Elenco di pacchetti pubblicati: GUID, versione GUID, nome.</p></li>
<li><p>Informazioni sull'uso delle applicazioni: nome, versione, server di streaming, utente (dominio\alias), GUID della versione del pacchetto, stato di avvio e ora, ora di arresto.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Qual è il volume medio di informazioni inviate al server di report?</p></td>
<td align="left"><p>Dipende. Nell'elenco seguente vengono visualizzati i tre set di dati inviati al server di report:</p>
<ol>
<li><p>Sistema operativo e informazioni client di App-V 5,1. ~ 150 byte, ogni volta che vengono inviati questi dati.</p></li>
<li><p>Elenco di pacchetti pubblicati. ~ 7 KB per 30 pacchetti. Viene inviato solo quando l'elenco di pacchetti viene aggiornato con un aggiornamento della pubblicazione, che viene eseguito raramente. Se non è presente alcuna modifica, queste informazioni non vengono inviate.</p></li>
<li><p>Informazioni sull'utilizzo delle applicazioni virtuali-circa 0,25 KB per ogni evento. L'apertura e la chiusura contano come un evento se si verificano entrambi prima di inviare le informazioni. Durante l'invio con un'attività pianificata, solo i dati dopo l'ultimo caricamento riuscito vengono inviati al server. Se l'invio manuale viene eseguito tramite il cmdlet di PowerShell, esiste un argomento facoltativo che controlla se i dati devono essere inviati nuovamente la prossima volta, ovvero che l'argomento è <strong> DeleteOnSuccess </strong> .</p>
<p></p>
<p>Ad esempio, se venti applicazioni vengono aperte e chiuse e le informazioni di segnalazione vengono inviate giornalmente, il traffico giornaliero tipico dovrebbe essere di circa 0,15 KB + 20 x 0,25 KB o su 5KB/utente</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>I report possono essere pianificati?</p></td>
<td align="left"><p>Sì. Oltre a inviare manualmente i report usando i cmdlet di PowerShell ( <strong> Send-AppvClientReport </strong> ), l'attività può essere programmata in modo che avvenga automaticamente. Esistono due modi per pianificare la creazione di report:</p>
<ol>
<li><p>Usare i cmdlet di PowerShell- <strong> set-AppvClientConfiguration </strong> . Ad esempio:</p>
<p>Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</a></p>
<p></p>
<p>Per un elenco completo delle impostazioni di configurazione del client, vedere <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)"> informazioni sulle impostazioni di configurazione del client </a> e cercare le voci seguenti: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , <strong> ReportingInterval </strong> .</p>
<p></p></li>
<li><p>Tramite criteri di gruppo. Se distribuiti con il controller di dominio, le impostazioni sono le stesse elencate in precedenza.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Le impostazioni dei criteri di gruppo eseguono l'override delle impostazioni locali configurate tramite PowerShell</p>
</div>
<div>
</div></li>
</ol></td>
</tr>
</tbody>
</table>

## <a href="" id="---------app-v-5-1-client-reporting"></a> Report client App-V 5,1

Per usare la creazione di report di App-V 5,1, è necessario installare e configurare il client App-V 5,1. Dopo l'installazione del client, usare il cmdlet **set-AppVClientConfiguration** di PowerShell o il **modello ADMX** per configurare la creazione di report. I cmdlet delle funzionalità di creazione di report sono disponibili tramite il collegamento seguente e sono preimpostati per la **creazione di report**. Per un elenco completo delle impostazioni di configurazione del client, vedere [informazioni sulle impostazioni di configurazione del client](about-client-configuration-settings51.md). La sezione seguente contiene esempi di configurazione della creazione di report client App-V 5,1 tramite PowerShell.

### Configurazione della creazione di report client App-V tramite PowerShell

Gli esempi seguenti illustrano come i parametri di PowerShell possono configurare le funzionalità di creazione di report del client App-V 5,1.

> [!NOTE]
> L'attività di configurazione seguente può essere configurata anche usando le impostazioni dei criteri di gruppo nel modello ADMX di App-V 5,1. Per altre informazioni sull'uso del modello ADMX, vedere [come modificare la configurazione del client App-V 5,1 usando il modello ADMX e i criteri di gruppo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).

**Per abilitare la creazione di report e avviare la raccolta dei dati nel computer che gestisce il client App-V 5,1**:

```powershell
Set-AppVClientConfiguration –ReportingEnabled 1
```

**Per configurare il client per l'invio automatico di dati a un server di report specifico**:

```powershell
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30 -ReportingInterval 1 -ReportingRandomDelay 30
```

Questo esempio configura il client per inviare automaticamente i dati dei report all'URL del server di report **http://MyReportingServer:MyPort/** . I dati dei report verranno inoltre inviati giornalmente tra 8:00 e 8:30 PM, a seconda del ritardo casuale generato per la sessione.

**Per limitare le dimensioni della cache dei dati nel client**:

```powershell
Set-AppvClientConfiguration –ReportingDataCacheLimit 100
```

Configura le dimensioni massime della cache dei report nel computer in cui è in uso il client App-V 5,1 per 100 MB. Se il limite della cache viene raggiunto prima che i dati vengano inviati al server, il log viene riposizionato e i dati verranno sovrascritti, se necessario.

**Per configurare le dimensioni del blocco dati trasmesse attraverso la rete tra il client e il server**:

```powershell
Set-AppvClientConfiguration –ReportingDataBlockSize 10240
```

Specifica il blocco di dati massimo inviato dal client a 10240 MB.

### Tipi di dati raccolti

La tabella seguente mostra i tipi di informazioni che è possibile raccogliere usando la creazione di report di App-V 5,1.

|Informazioni sul client  |Informazioni sul pacchetto  |Utilizzo dell'applicazione  |
|---------|---------|---------|
|Nome host |Nome pacchetto|Orari di inizio e fine|
|Versione client di App-V 5,1 |Versione del pacchetto|Stato esecuzione|
|Architettura del processore |Origine pacchetto|Stato arresto|
|Versione del sistema operativo|Percentuale di cache|Nome applicazione|
|Livello di Service Pack| |Versione dell'applicazione|
|Tipo di sistema operativo| |Nome utente|
| | |Gruppo di connessioni|

Il client raccoglie e salva questi dati in un formato **XML** . La cache di dati è nascosta per impostazione predefinita e richiede i diritti di amministratore per aprire il file XML.

### Invio di dati al server

Puoi configurare il computer che sta usando il client App-V 5,1 per inviare automaticamente i dati al server di report specificato. Per specificare il server, usare il cmdlet **set-AppvClientConfiguration** con le impostazioni seguenti:

- ReportingEnabled
- ReportingServerURL
- ReportingStartTime
- ReportingInterval
- ReportingRandomDelay

Dopo aver configurato le impostazioni precedenti, è necessario creare un'attività pianificata. L'attività pianificata contatterà il server specificato dall'impostazione **ReportingServerURL** e avvierà il trasferimento. Se si vogliono inviare manualmente dati al di fuori dell'orario programmato, usare il cmdlet di PowerShell seguente:

```powershell
Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess
```

Se il server di report è stato configurato in precedenza, il parametro **– URL** può essere omesso. In alternativa, se i dati devono essere inviati a una posizione alternativa, specificare un URL diverso per eseguire l'override del **ReportingServerURL** configurato per la raccolta dati.

Il parametro **-DeleteOnSuccess** indica che se il trasferimento ha esito positivo, la cache di dati viene deselezionata. Se non viene specificato, la cache non verrà deselezionata.

### Raccolta dati manuale

Puoi anche usare il cmdlet **Send-AppVClientReport** per raccogliere manualmente i dati. Questa soluzione è utile con o senza un server di report esistente. Nell'elenco seguente vengono visualizzate informazioni sulla raccolta di dati con o senza un server di report.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Con un server di report</th>
<th align="left">Senza un server di report</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Se si dispone di un server di report App-V 5,1 esistente, creare un'attività pianificata personalizzata o uno script. Specifica che il client invia i dati nella posizione specificata con la frequenza desiderata.</p></td>
<td align="left"><p>Se non si dispone di un server di report App-V 5,1 esistente, usare il <strong> parametro – URL </strong> per inviare i dati a una condivisione specificata. Ad esempio:</p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p>L'esempio precedente invierà i dati di report <strong> nella &lt; posizione di \MyShare\MyData/Strong &gt; indicata dal <strong> parametro-URL </strong> . Dopo che i dati sono stati inviati, la cache viene deselezionata.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se viene specificata una posizione diversa da quella del server di Reporting, i dati vengono inviati tramite il <strong> </strong> formato XML senza ulteriori elaborazioni.</p>
</div>
<div>
</div></td>
</tr>
</tbody>
</table>

### Creazione di report

Per recuperare le informazioni sul report e creare report tramite App-V 5,1 è necessario usare uno dei metodi seguenti:

- **Microsoft SQL Server Reporting Services (SSRS)** -Microsoft SQL Server Reporting Services è disponibile con Microsoft SQL Server. SSRS non viene installato quando si installa il server di report App-V 5,1. Deve essere distribuito separatamente per generare i report associati.

    Per altre informazioni sull'uso di [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596), usare il collegamento seguente.

- **Scripting** : è possibile generare report tramite scripting direttamente sul database di report di App-V 5,1. Ad esempio:

    **Stored procedure:**

    **spProcessClientReport** è programmato per l'esecuzione a mezzanotte o 12:00 AM.

    Per eseguire la stored procedure pianificata di Microsoft SQL Server, è necessario che Microsoft SQL Server Agent sia in esecuzione. Devi verificare che Microsoft SQL Server Agent sia impostato su **autostart**. Per altre informazioni, vedere [autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).

    La stored procedure viene creata anche quando si usano gli script di database App-V 5,1.

Devi anche assicurarti che le **connessioni simultanee massime** del servizio di Reporting Server Web siano impostate su un valore che il server potrà gestire senza influire sulla disponibilità. Il numero consigliato di **connessioni simultanee massime** per il **servizio Web Reporting** è **10.000**.

## Argomenti correlati

[Distribuzione del server App-V 5.1](deploying-the-app-v-51-server.md)

[Come installare il server di report in un computer autonomo e connetterlo al database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)
