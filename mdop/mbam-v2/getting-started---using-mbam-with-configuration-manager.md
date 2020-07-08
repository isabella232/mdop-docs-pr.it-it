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
ms.openlocfilehash: 654de38918102a41395efe37dc593ce8f49113e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825166"
---
# Attività iniziali: uso di MBAM con Configuration Manager


Quando si installa Microsoft BitLocker Administration and Monitoring (MBAM), è possibile scegliere una topologia che integri MBAM con Configuration Manager 2007 o SystemCenter2012 ConfigurationManager. Per un elenco delle versioni supportate di Configuration Manager che MBAM supporta, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). Nella topologia integrata le funzionalità di conformità e creazione di report hardware vengono rimosse da MBAM e si accede da Configuration Manager.

**Importante**  Windows to go non è supportato quando si installa la topologia integrata di MBAM con Configuration Manager 2007.

 

## Uso di MBAM con Configuration Manager


L'integrazione di MBAM si basa su un nuovo pacchetto di configurazione che installa i tre elementi seguenti in Configuration Manager 2007 o SystemCenter2012 ConfigurationManager, descritti in dettaglio nelle sezioni seguenti:

Dati di configurazione costituiti da elementi di configurazione e da una previsione di configurazione

Raccolta

Rapporti

### Dati di configurazione

I dati di configurazione installano una previsione di configurazione, denominata "protezione BitLocker", che contiene due elementi di configurazione: "protezione unità sistema operativo BitLocker" e "protezione delle unità dati fisse di BitLocker". La linea di base della configurazione viene distribuita nella raccolta, che viene creata anche quando viene installato MBAM. I due elementi di configurazione costituiscono la base per valutare lo stato di conformità dei computer client. Queste informazioni vengono acquisite, archiviate e valutate in Gestione configurazione. Gli elementi di configurazione si basano sui requisiti di conformità per le unità del sistema operativo (OSDs) e sulle unità dati fisse (FDDs). I dettagli necessari per i computer distribuiti vengono raccolti in modo da poter valutare la conformità per tali tipi di unità. Per impostazione predefinita, la linea di base della configurazione valuta lo stato di conformità ogni 12 ore e invia i dati di conformità a Configuration Manager.

### Raccolta

MBAM crea una raccolta che si chiama MBAM computer supportati. La linea di base della configurazione è destinata ai computer client inclusi in questa raccolta. Si tratta di una raccolta dinamica che, per impostazione predefinita, viene eseguita ogni 12 ore e valuta l'appartenenza. L'appartenenza si basa su tre criteri:

-   Si tratta di una versione supportata del sistema operativo Windows. Attualmente, MBAM supporta solo Windows 7 Enterprise e Windows 7 Ultimate, Windows 8 Enterprise e Windows to go, quando Windows to go è in uso in Windows 8 Enterprise.

-   Si tratta di un computer fisico. Le macchine virtuali non sono supportate.

-   Il TPM (Trusted Platform Module) è disponibile. Per Windows 7 è necessaria una versione compatibile del TPM 1,2 o successiva. Windows 8 e Windows to go non richiedono un TPM.

La raccolta viene valutata in tutti i computer e crea il sottoinsieme di computer compatibili che fornisce la base per la valutazione della conformità e la creazione di report per l'integrazione con MBAM.

### Rapporti

Sono disponibili quattro report che è possibile usare per visualizzare la conformità. e sono:

-   **Dashboard di conformità di BitLocker Enterprise** offre agli amministratori IT tre diverse visualizzazioni di informazioni su un singolo report: distribuzione dello stato di conformità, non conforme, distribuzione degli errori e distribuzione dello stato di conformità per tipo di unità. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.

-   **Dettagli conformità di BitLocker Enterprise** consente agli amministratori IT di visualizzare informazioni sullo stato di conformità della crittografia BitLocker dell'organizzazione e include lo stato di conformità per ogni computer. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.

-   **Conformità del computer BitLocker** : consente agli amministratori IT di visualizzare un singolo computer e determinare il motivo per cui è stato segnalato con uno stato specifico conforme o non conforme. Il report visualizza anche lo stato di crittografia delle unità di sistema operativo (OSD) e delle unità dati fisse (FDDs).

-   **Riepilogo conformità di BitLocker Enterprise** -consente agli amministratori IT di visualizzare lo stato della conformità dell'organizzazione con i criteri di mbam. Lo stato di ogni computer viene valutato e il report Mostra un riepilogo della conformità di tutti i computer dell'organizzazione rispetto al criterio. Le opzioni di drill-down nel report consentono agli amministratori IT di fare clic sui dati e visualizzare un elenco di computer che corrispondono allo stato selezionato.

## Architettura di alto livello di MBAM con Configuration Manager


L'immagine seguente mostra l'architettura MBAM con la topologia di Configuration Manager. Questa configurazione supporta fino a 200.000 client MBAM in un ambiente di produzione.

![architettura mbam con Configuration Manager](images/mbam2-cmserver.gif)

Segue una descrizione dei server, dei database e delle caratteristiche di questa architettura. Le caratteristiche e i database del server nell'immagine dell'architettura sono elencati sotto il computer o il server in cui è consigliabile installarli.

-   **Server di database** : il **database di ripristino**, il database di **controllo**e i report di **controllo** vengono installati in un server Windows e nell'istanza di SqlServer supportata. Il database di ripristino Archivia i dati di recupero raccolti dai computer client di MBAM. Il database di controllo archivia i dati delle attività di controllo raccolti da computer client che hanno eseguito l'accesso ai dati di ripristino. I report di controllo contengono dati sullo stato di conformità dei computer client nell'organizzazione.

-   **Server del sito primario di Configuration Manager** : il Server Configuration Manager contiene l'installazione di mbam server con la topologia di integrazione di System Center Configuration Manager, che deve essere installata in un server del sito primario di Configuration Manager. Il Server Configuration Manager raccoglie le informazioni sull'inventario hardware dai computer client e viene usato per segnalare la conformità di BitLocker dei computer client. Quando si esegue l'installazione di MBAM Setup Server, nel server del sito primario di Configuration Manager viene installata una raccolta e i dati di configurazione.

-   **Server** di amministrazione e monitoraggio: il **server di amministrazione e monitoraggio** viene installato in un server Windows ed è costituito dal sito Web di amministrazione e monitoraggio e dai servizi Web di monitoraggio. Il sito Web di amministrazione e monitoraggio viene usato per controllare le attività e per accedere ai dati di ripristino, ad esempio le chiavi di ripristino di BitLocker. Il **portale self-service** è installato anche nel server di amministrazione e monitoraggio. Il portale consente agli utenti finali nei computer client di accedere in modo indipendente a un sito Web per ottenere una chiave di ripristino se perdono o dimenticano la password di BitLocker. I report di controllo vengono installati anche nel server di amministrazione e monitoraggio.

-   **Management workstation** : il **modello di criteri** è costituito da oggetti Criteri di gruppo che definiscono le impostazioni di implementazione di mbam per crittografia unità BitLocker. È possibile installare il modello di criteri in qualsiasi server o workstation, ma è comunemente installato in una workstation di gestione che è un computer Windows Server o client supportato. La workstation non deve essere un computer dedicato.

-   Client **mbam** e computer **client di Configuration Manager**

    -   Il **client mbam** esegue le attività seguenti:

        -   USA gli oggetti Criteri di gruppo per applicare la crittografia BitLocker dei computer client nell'organizzazione.

        -   Raccoglie la chiave di ripristino per i tre tipi di unità dati di BitLocker: unità del sistema operativo, unità dati fisse e unità USB (removibile Data).

        -   Raccoglie informazioni di ripristino e informazioni sul computer sui computer client.

    -   **Client Configuration Manager** : il client Configuration Manager consente a Gestione configurazione di raccogliere i dati di compatibilità hardware relativi ai computer client e consente a Gestione configurazione di segnalare le informazioni sulla conformità.

## Argomenti correlati


[Uso di MBAM con Configuration Manager](using-mbam-with-configuration-manager.md)

 

 





