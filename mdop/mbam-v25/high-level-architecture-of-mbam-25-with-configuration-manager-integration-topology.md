---
title: Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager
description: Architettura di alto livello di MBAM 2.5 con topologia di integrazione di Configuration Manager
author: dansimp
ms.assetid: 075bafa1-792b-4c24-9d8e-5d3153e2112c
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/23/2018
ms.author: dansimp
ms.openlocfilehash: a0f9349391794100a670e382bb18d0713f4b5b60
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910721"
---
# <a name="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology"></a>Architettura generale di MBAM 2.5 con topologia di integrazione di Configuration Manager

In questo argomento viene descritta l'architettura consigliata per la distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia di integrazione di Configuration Manager. Questa topologia integra MBAM con System Center Configuration Manager. Per distribuire MBAM con la topologia autonoma, vedere [High-Level Architecture of MBAM 2.5 with Stand-alone Topology](high-level-architecture-of-mbam-25-with-stand-alone-topology.md).

Per un elenco delle versioni supportate del software menzionato in questo argomento, vedere [MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md).

**Importante**  
Windows To Go non è supportato per l'installazione della topologia di integrazione di Configuration Manager quando si utilizza Configuration Manager 2007.

 

## <a name="recommended-number-of-servers-and-supported-number-of-clients"></a>Numero consigliato di server e numero supportato di client


Il numero consigliato di server e il numero supportato di client in un ambiente di produzione è il seguente:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Architettura consigliata</th>
<th align="left">Dettagli</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Numero di server e altri computer</p></td>
<td align="left"><p>Tre server</p>
<p>Una workstation</p></td>
</tr>
<tr class="even">
<td align="left"><p>Numero di computer client supportati</p></td>
<td align="left"><p>500,000</p></td>
</tr>
</tbody>
</table>

 

## <a name="differences-between-configuration-manager-integration-and-stand-alone-topologies"></a>Differenze tra l'integrazione di Configuration Manager e le topologie autonome


Le principali differenze tra le topologie sono:

-   Le funzionalità di conformità e creazione di report sono state rimosse da MBAM e sono accessibili da Configuration Manager.

-   I report vengono visualizzati dalla console di gestione di Configuration Manager, ad eccezione del Rapporto di controllo di ripristino, che si continua a visualizzare dal sito Web amministrazione e monitoraggio di MBAM.

## <a name="recommended-mbam-high-level-architecture-with-the-configuration-manager-integration-topology"></a>Architettura di alto livello mbam consigliata con la topologia di integrazione di Configuration Manager


Il diagramma e la tabella seguenti descrivono l'architettura di alto livello consigliata per MBAM con la topologia di integrazione di Configuration Manager. Le distribuzioni a più foreste MBAM richiedono un trust unidirezionale o bidirezionale. I trust unidirezionale richiedono che il dominio del server considera attendibile il dominio client.

![mbam2\-5.](images/mbam2-5-cmserver.png)

### <a name="database-server"></a>Server di database

#### <a name="recovery-database"></a>Database di ripristino

Questa funzionalità è configurata in un computer che esegue Windows Server e supporta SQL Server istanza.

Il **database di ripristino** archivia i dati di ripristino raccolti dai computer client MBAM.

#### <a name="audit-database"></a>Database di controllo

Questa funzionalità è configurata in un computer che esegue Windows Server e supporta SQL Server istanza.

Il **database di controllo** archivia i dati dell'attività di controllo raccolti dai computer client che hanno eseguito l'accesso ai dati di ripristino.

#### <a name="reports"></a>Rapporti

Questa funzionalità è configurata in un computer che esegue Windows Server e supporta SQL Server istanza.

I **report forniscono** dati di controllo di ripristino per i computer client dell'organizzazione. È possibile visualizzare i report dalla console di Configuration Manager o direttamente da SQL Server Reporting Services.

### <a name="configuration-manager-primary-site-server"></a>Server del sito primario di Configuration Manager

System Center Configuration Manager Funzionalità di integrazione

-   Questa funzionalità è configurata nel server del sito primario di Configuration Manager, che è il server di primo livello nell'infrastruttura di Configuration Manager.

-   Il **server di Configuration Manager** raccoglie le informazioni di inventario hardware dai computer client e viene utilizzato per segnalare la conformità di BitLocker dei computer client.

-   Quando si esegue l'installazione guidata di Amministrazione e monitoraggio di Microsoft BitLocker per installare il software server, la raccolta di computer supportati da MBAM, la linea di base di configurazione e i report vengono configurati nel server del sito principale di Configuration Manager.

-   La **console di Configuration Manager** deve essere installata nello stesso computer in cui si installa il software del server MBAM.

### <a name="administration-and-monitoring-server"></a>Server di amministrazione e monitoraggio

#### <a name="administration-and-monitoring-website"></a>Sito Web di amministrazione e monitoraggio

Questa funzionalità è configurata in un computer che esegue Windows Server.

Il **sito Web Amministrazione e monitoraggio** consente di:

-   Aiutare gli utenti finali a recuperare l'accesso ai computer quando sono bloccati. Quest'area del sito Web è comunemente chiamata Help Desk.

-   Visualizzare il rapporto di controllo del ripristino, che mostra l'attività di ripristino per i computer client. Altri report vengono visualizzati dalla console di Configuration Manager.

#### <a name="self-service-portal"></a>Portale self-service

Questa funzionalità è configurata in un computer che esegue Windows Server.

Il **portale self-service** è un sito Web che consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker.

#### <a name="monitoring-web-services-for-this-website"></a>Monitoraggio dei servizi Web per questo sito Web

Questa funzionalità viene installata in un computer che esegue Windows Server.

I **servizi Web di monitoraggio** vengono utilizzati dal client MBAM e dai siti Web per comunicare con il database.

**Importante**<br>Il servizio Web di monitoraggio non è più disponibile in Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1 poiché i siti Web MBAM comunicano direttamente con il database di ripristino. 

 

### <a name="management-workstation"></a>Workstation di gestione

#### <a name="mbam-group-policy-templates"></a>Modelli di Criteri di gruppo MBAM

-   I **modelli di Criteri di gruppo MBAM** sono impostazioni di Criteri di gruppo che definiscono le impostazioni di implementazione per MBAM, che consentono di gestire la crittografia dell'unità BitLocker.

-   Prima di eseguire MBAM, è necessario scaricare i modelli di Criteri di gruppo da Come ottenere modelli di Criteri di gruppo [MDOP (admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) e copiarli in un server o una workstation che esegue un sistema operativo Windows Server o Windows supportato.

    **NOTA**<br>La workstation non deve essere un computer dedicato.

     

### <a name="mbam-client-and-configuration-manager-client-computer"></a>Computer client MBAM e Configuration Manager

#### <a name="mbam-client-software"></a>Software client MBAM

Il **client MBAM**:

-   Usa oggetti Criteri di gruppo per applicare la crittografia dell'unità BitLocker nei computer client dell'organizzazione.

-   Raccoglie la chiave di ripristino di BitLocker per tre tipi di unità dati: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

-   Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.

#### <a name="configuration-manager-client"></a>Client di Gestione configurazione

Il **client di Configuration Manager consente** a Configuration Manager di raccogliere dati sulla compatibilità hardware sui computer client e di segnalare le informazioni di conformità.

 

## <a name="differences-in-mbam-deployment-for-supported-configuration-manager-versions"></a>Differenze nella distribuzione di MBAM per le versioni supportate di Configuration Manager


Quando si distribuisce MBAM con la topologia di integrazione di Configuration Manager, è possibile installare MBAM in un server di sito primario. Tuttavia, l'installazione di MBAM funziona in modo diverso per System Center 2012 Configuration Manager e Configuration Manager 2007.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione di Configuration Manager</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p>
<p>System Center 2012 Configuration Manager</p></td>
<td align="left"><p>Se si installa MBAM in un server di sito primario o in un server di amministrazione centrale, MBAM esegue tutte le azioni di installazione su tale server del sito.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuration Manager 2007 R2</p>
<p>Configuration Manager 2007</p></td>
<td align="left"><p>Se si installa MBAM in un server di sito primario che fa parte di una gerarchia di Configuration Manager più ampia con un server padre del sito centrale, MBAM identifica il server padre del sito centrale ed esegue tutte le azioni di installazione su tale server padre. L'installazione include il controllo dei prerequisiti e l'installazione degli oggetti e dei report di Configuration Manager.</p>
<p>Ad esempio, se si installa MBAM in un server di sito primario figlio di un server padre del sito centrale, MBAM installa tutti gli oggetti e i report di Configuration Manager nel server padre. Se si installa MBAM nel server padre, MBAM esegue tutte le azioni di installazione su tale server padre.</p></td>
</tr>
</tbody>
</table>

 

## <a name="how-mbam-works-with-configuration-manager"></a>Funzionamento di MBAM con Configuration Manager


L'integrazione di MBAM con Configuration Manager si basa su un pacchetto di configurazione che installa gli elementi descritti nella tabella seguente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elementi installati in Configuration Manager</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Dati di configurazione</p></td>
<td align="left"><p>I dati di configurazione installano una linea di base di configurazione, denominata "Protezione BitLocker", che contiene due elementi di configurazione:</p>
<ul>
<li><p>Protezione unità del sistema operativo BitLocker</p></li>
<li><p>Protezione unità dati fisse bitlocker</p></li>
</ul>
<p>La linea di base della configurazione viene distribuita nell'insieme MbAM Supported Computers, che viene creato anche quando viene installato MBAM.</p>
<p>I due elementi di configurazione forniscono la base per valutare lo stato di conformità dei computer client. Queste informazioni vengono acquisite, archiviate e valutate in Configuration Manager.</p>
<p>Gli elementi di configurazione si basano sui requisiti di conformità per le unità del sistema operativo e le unità dati fisse. I dettagli necessari per i computer distribuiti vengono raccolti in modo da poter valutare la conformità per tali tipi di unità.</p>
<p>Per impostazione predefinita, la linea di base di configurazione valuta lo stato di conformità ogni 12 ore e invia i dati di conformità a Configuration Manager.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Insieme MbAM Supported Computers</p></td>
<td align="left"><p>MBAM crea una raccolta denominata MbAM Supported Computers. La linea di base della configurazione è destinata ai computer client presenti in questa raccolta.</p>
<p>Si tratta di una raccolta dinamica. Per impostazione predefinita, viene eseguito ogni 12 ore e valuta l'appartenenza in base a tre criteri:</p>
<ul>
<li><p>Il computer è una versione supportata del Windows sistema operativo.</p></li>
<li><p>Il computer è un computer fisico. Le macchine virtuali non sono supportate.</p></li>
<li><p>Il computer dispone di un TPM (Trusted Platform Module) disponibile. È necessaria una versione compatibile di TPM 1.2 o versione successiva per Windows 7. Windows 10, Windows 8.1, Windows 8 e Windows To Go non richiedono un TPM.</p></li>
</ul>
<p>La raccolta viene valutata in base a tutti i computer e viene creato un sottoinsieme di computer compatibili, che fornisce la base per la valutazione della conformità e la creazione di report per l'integrazione mbam.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Rapporti</p></td>
<td align="left"><p>Quando si configura MBAM con la topologia di integrazione di Configuration Manager, si visualizzano tutti i report in Configuration Manager, ad eccezione del Rapporto di controllo di ripristino, quest'ultimo dei quali continua a essere visualizzato nel sito Web amministrazione e monitoraggio di MBAM. I report disponibili in Configuration Manager sono:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Rapporto</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>BitLocker Enterprise Dashboard di conformità</p></td>
<td align="left"><p>Offre agli amministratori IT tre visualizzazioni delle informazioni in un singolo report: Distribuzione dello stato di conformità, Non conforme - Distribuzione errori e Distribuzione dello stato di conformità per tipo di unità. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Enterprise Dettagli conformità</p></td>
<td align="left"><p>Consente agli amministratori IT di visualizzare informazioni sullo stato di conformità della crittografia BitLocker dell'organizzazione e include lo stato di conformità per ogni computer. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conformità computer BitLocker</p></td>
<td align="left"><p>Consente agli amministratori IT di visualizzare un singolo computer e di determinare il motivo per cui è stato segnalato con lo stato conforme o non conforme. Nel report viene inoltre visualizzato lo stato di crittografia delle unità del sistema operativo e delle unità dati fisse.</p></td>
</tr>
<tr class="even">
<td align="left"><p>BitLocker Enterprise Riepilogo conformità</p></td>
<td align="left"><p>Consente agli amministratori IT di visualizzare lo stato di conformità dei criteri MBAM nell'organizzazione. Lo stato di ogni computer viene valutato e il report mostra un riepilogo della conformità di tutti i computer dell'organizzazione rispetto ai criteri. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 


## <a name="related-topics"></a>Argomenti correlati


[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

[Architettura di alto livello di MBAM 2.5 con topologia autonoma](high-level-architecture-of-mbam-25-with-stand-alone-topology.md)

[Funzionalità illustrate di una distribuzione di MBAM 2.5](illustrated-features-of-an-mbam-25-deployment.md)

 

 
## <a name="got-a-suggestion-for-mbam"></a>Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, utilizzare il [Forum TechNet di MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




