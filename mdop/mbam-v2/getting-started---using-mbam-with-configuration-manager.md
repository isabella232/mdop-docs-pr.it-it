---
title: 'Attività iniziali: uso di MBAM con Configuration Manager'
description: 'Attività iniziali: uso di MBAM con Configuration Manager'
author: dansimp
ms.assetid: b0a1d3cc-0b01-4b69-a2cd-fd09fb3beda4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f23a0eba923608fb6e25e44ee2843f3cde4c2dc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910811"
---
# <a name="getting-started---using-mbam-with-configuration-manager"></a>Attività iniziali: uso di MBAM con Configuration Manager


Quando si installa Microsoft BitLocker Administration and Monitoring (MBAM), è possibile scegliere una topologia che integra MBAM con Configuration Manager 2007 o System Center 2012 Configuration Manager. Per un elenco delle versioni supportate di Configuration Manager supportate da MBAM, vedere [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). Nella topologia integrata, le funzionalità di conformità e creazione di report hardware vengono rimosse da MBAM e sono accessibili da Configuration Manager.

**Importante**  
Windows To Go non è supportato quando si installa la topologia integrata di MBAM con Configuration Manager 2007.

 

## <a name="using-mbam-with-configuration-manager"></a>Uso di MBAM con Configuration Manager


L'integrazione di MBAM si basa su un nuovo Configuration Pack che installa i tre elementi seguenti in Configuration Manager 2007 o System Center 2012 Configuration Manager, descritti in dettaglio nelle sezioni seguenti:

Dati di configurazione costituiti da elementi di configurazione e una linea di base di configurazione

Raccolta

Rapporti

### <a name="configuration-data"></a>Dati di configurazione

I dati di configurazione installano una linea di base di configurazione, denominata "Protezione BitLocker", che contiene due elementi di configurazione: "Protezione unità disco del sistema operativo BitLocker" e "Protezione unità dati fisse BitLocker". La linea di base di configurazione viene distribuita nella raccolta, che viene creata anche quando viene installato MBAM. I due elementi di configurazione forniscono la base per valutare lo stato di conformità dei computer client. Queste informazioni vengono acquisite, archiviate e valutate in Configuration Manager. Gli elementi di configurazione si basano sui requisiti di conformità per le unità del sistema operativo (OSD) e le unità dati fisse (FDD). I dettagli necessari per i computer distribuiti vengono raccolti in modo da poter valutare la conformità per tali tipi di unità. Per impostazione predefinita, la linea di base di configurazione valuta lo stato di conformità ogni 12 ore e invia i dati di conformità a Configuration Manager.

### <a name="collection"></a>Raccolta

MBAM crea una raccolta denominata MbAM Supported Computers. La linea di base della configurazione è destinata ai computer client presenti in questa raccolta. Si tratta di una raccolta dinamica che, per impostazione predefinita, viene eseguita ogni 12 ore e valuta l'appartenenza. L'appartenenza si basa su tre criteri:

-   Si tratta di una versione supportata del Windows sistema operativo. Attualmente, MBAM supporta solo Windows 7 Enterprise e Windows 7 Ultimate, Windows 8 Enterprise e Windows To Go, quando Windows To Go è in esecuzione su Windows 8 Enterprise.

-   Si tratta di un computer fisico. Le macchine virtuali non sono supportate.

-   Trusted Platform Module (TPM) è disponibile. È necessaria una versione compatibile di TPM 1.2 o versione successiva per Windows 7. Windows 8 e Windows To Go non richiedono un TPM.

La raccolta viene valutata in base a tutti i computer e crea il sottoinsieme di computer compatibili che costituisce la base per la valutazione della conformità e la creazione di report per l'integrazione mbam.

### <a name="reports"></a>Rapporti

Sono disponibili quattro report che è possibile utilizzare per visualizzare la conformità. e sono:

-   **BitLocker Enterprise Dashboard** di conformità: offre agli amministratori IT tre diverse visualizzazioni delle informazioni in un singolo report: Distribuzione dello stato di conformità, Non conforme - Distribuzione errori e Distribuzione dello stato di conformità per tipo di unità. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.

-   **BitLocker Enterprise conformità:** consente agli amministratori IT di visualizzare informazioni sullo stato di conformità della crittografia BitLocker dell'organizzazione e include lo stato di conformità per ogni computer. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.

-   **Conformità computer BitLocker:** consente agli amministratori IT di visualizzare un singolo computer e di determinare il motivo per cui è stato segnalato con un determinato stato di conformità o non conforme. Nel report viene inoltre visualizzato lo stato di crittografia delle unità del sistema operativo (OSD) e delle unità dati fisse (FDD).

-   **BitLocker Enterprise riepilogo della conformità:** consente agli amministratori IT di visualizzare lo stato di conformità dell'azienda con i criteri MBAM. Lo stato di ogni computer viene valutato e il report mostra un riepilogo della conformità di tutti i computer dell'organizzazione rispetto ai criteri. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.

## <a name="high-level-architecture-of-mbam-with-configuration-manager"></a>High-Level architettura di MBAM con Configuration Manager


L'immagine seguente mostra l'architettura MBAM con la topologia di Configuration Manager. Questa configurazione supporta fino a 200.000 client MBAM in un ambiente di produzione.

![Architettura mbam con Configuration Manager.](images/mbam2-cmserver.gif)

Di seguito viene fornita una descrizione dei server, dei database e delle funzionalità di questa architettura. Le funzionalità del server e i database nell'immagine dell'architettura sono elencati nel computer o nel server in cui è consigliabile installarli.

-   **Server database:** il **database di** **** ripristino, il **database**di controllo e i report di controllo sono installati in un server Windows e sono supportati SQL Server istanza. Il database di ripristino archivia i dati di ripristino raccolti dai computer client MBAM. Il database di controllo archivia i dati dell'attività di controllo raccolti dai computer client che hanno eseguito l'accesso ai dati di ripristino. I report di controllo forniscono dati sullo stato di conformità dei computer client dell'organizzazione.

-   Server del sito primario di **Configuration Manager:** il server di Configuration Manager contiene l'installazione del server MBAM con la topologia di integrazione di System Center Configuration Manager, che deve essere installata in un server di sito primario di Configuration Manager. Il server di Configuration Manager raccoglie le informazioni di inventario hardware dai computer client e viene utilizzato per segnalare la conformità di BitLocker dei computer client. Quando si esegue l'installazione del server di installazione di MBAM, una raccolta e i dati di configurazione vengono installati nel server del sito primario di Configuration Manager.

-   **Amministrazione e Monitoring Server-** Administration **and Monitoring Server** è installato in un server Windows ed è costituito dal sito Web Amministrazione e monitoraggio e dai servizi Web di monitoraggio. Il sito Web Amministrazione e monitoraggio viene utilizzato per controllare l'attività e accedere ai dati di ripristino (ad esempio, chiavi di ripristino di BitLocker). Il **portale self-service** viene installato anche in Administration and Monitoring Server. Il portale consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker. I report di controllo vengono installati anche in Administration and Monitoring Server.

-   **Workstation di gestione:** il **modello di criteri** è costituito da oggetti Criteri di gruppo che definiscono le impostazioni di implementazione mbam per la crittografia dell'unità BitLocker. È possibile installare il modello di criteri in qualsiasi server o workstation, ma in genere viene installato in una workstation di gestione supportata Windows server o computer client. La workstation non deve essere un computer dedicato.

-   **Computer client MBAM** **e Configuration Manager**

    -   Il **client MBAM** esegue le attività seguenti:

        -   Usa oggetti Criteri di gruppo per applicare la crittografia BitLocker dei computer client nell'organizzazione.

        -   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità dati rimovibili (USB).

        -   Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.

    -   **Client di Configuration Manager:** il client di Configuration Manager consente a Configuration Manager di raccogliere dati sulla compatibilità hardware sui computer client e consente a Configuration Manager di segnalare le informazioni di conformità.

## <a name="related-topics"></a>Argomenti correlati


[Uso di MBAM con Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





