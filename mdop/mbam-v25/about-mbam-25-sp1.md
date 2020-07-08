---
title: Informazioni su MBAM 2.5 SP1
description: Informazioni su MBAM 2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823785"
---
# Informazioni su MBAM 2.5 SP1


MBAM 2,5 SP1 offre un'interfaccia amministrativa semplificata per la crittografia unità BitLocker. BitLocker offre una protezione avanzata per il furto di dati o l'esposizione ai dati per i computer persi o rubati. BitLocker crittografa tutti i dati archiviati nel sistema operativo Windows e in unità e unità dati configurate.

## Panoramica di MBAM


MBAM 2,5 SP1 ha le caratteristiche seguenti:

-   Consente agli amministratori di automatizzare il processo di crittografia dei volumi nei computer client in tutta l'organizzazione.

-   Consente agli addetti alla sicurezza di determinare rapidamente lo stato di conformità dei singoli computer o anche dell'organizzazione stessa.

-   Fornisce Reporting centralizzato e gestione hardware con Microsoft System Center Configuration Manager.

-   Riduce il carico di lavoro nell'help desk per aiutare gli utenti finali con le richieste di chiavi di ripristino e PIN di BitLocker.

-   Consente agli utenti finali di recuperare i dispositivi crittografati in modo indipendente usando il portale self-service.

-   Consente agli addetti alla sicurezza di controllare facilmente l'accesso per recuperare le informazioni chiave.

-   Consente agli utenti di Windows Enterprise di continuare a lavorare ovunque con la garanzia che i loro dati aziendali siano protetti.

MBAM applica le opzioni dei criteri di crittografia di BitLocker impostate per l'organizzazione, monitora la conformità dei computer client con tali criteri e segnala lo stato di crittografia dei computer dell'organizzazione e dell'individuo. Inoltre, MBAM consente di accedere alle informazioni chiave di ripristino quando gli utenti dimenticano il PIN o la password o quando cambiano i record del BIOS o del boot.

I gruppi seguenti potrebbero essere interessati all'uso di MBAM per gestire BitLocker:

-   Amministratori, professionisti IT per la sicurezza e responsabili della conformità che hanno la responsabilità di garantire che i dati riservati non vengano divulgati senza autorizzazione

-   Amministratori responsabili della sicurezza dei computer in uffici remoti o succursali

-   Amministratori responsabili per i computer client che eseguono Windows

**Nota**  BitLocker non è spiegato in dettaglio in questa documentazione di MBAM. Per altre informazioni, vedere [Panoramica della crittografia unità BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a>Novità di MBAM 2,5 SP1


Questa sezione descrive le nuove caratteristiche di MBAM 2,5 SP1.

### Lingue appena supportate per il client MBAM 2,5 SP1

Le seguenti lingue aggiuntive sono ora supportate in MBAM 2,5 SP1 solo per il client MBAM, incluso il portale self-service:

Ceco (Repubblica Ceca) CS-CZ

Danese (Danimarca) da-DK

Olandese (Paesi Bassi) nl-NL

Fi-FI Finlandese (Finlandia)

Greco (Grecia) el-GR

Ungherese (Ungheria) hu-HU

Norvegese, Bokmål (Norvegia) nb-NO

Polacco (Polonia) PL-PL

Portoghese (Portogallo) PT-PT

Slovacco (Slovacchia) SK-SK

Sloveno (Slovenia) SL-SI

Svedese (Svezia) SV-SE

Turco (Turchia) tr-TR

Per un elenco di tutte le lingue supportate per client e server in MBAM 2,5 e MBAM 2,5 SP1, Vedi le [configurazioni supportate di mbam 2,5](mbam-25-supported-configurations.md).

### Supporto per Windows 10

MBAM 2,5 SP1 aggiunge il supporto per Windows 10 e Windows Server 2016, oltre allo stesso software supportato nelle versioni precedenti di MBAM.

Windows 10 è supportato in MBAM 2,5 e MBAM 2,5 SP1.

### Supporto per Microsoft SQL Server 2014 SP1

MBAM 2,5 SP1 aggiunge il supporto per Microsoft SQL Server 2014 SP1, oltre allo stesso software supportato nelle versioni precedenti di MBAM.

### MBAM non viene più distribuito con MSI separato

A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM. È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto.

### MBAM può le password di OwnerAuth escrow senza possedere il TPM

In precedenza, se MBAM non fosse il proprietario del TPM, il TPM OwnerAuth non poteva essere escrowed al database MBAM. Per configurare MBAM per il proprio TPM e per archiviare le password, è stato necessario disabilitare il provisioning automatico del TPM e cancellare il TPM nel computer client.

In Windows 8 e versioni successive, MBAM 2,5 SP1 può ora escrow le password di OwnerAuth senza possedere il TPM. Durante l'avvio del servizio, MBAM esegue una query per verificare se il TPM è già di proprietà e, in caso affermativo, richiede le password del sistema operativo. Le password vengono poi escrowed al database MBAM. Inoltre, i criteri di gruppo devono essere impostati per impedire che OwnerAuth venga eliminato localmente.

In Windows 7, MBAM deve possedere il TPM per l'escrow automaticamente le informazioni di OwnerAuth del TPM nel database MBAM. Se MBAM non è il proprietario del TPM e il backup di Active Directory (AD) del TPM è configurato tramite criteri di gruppo, è necessario usare i **cmdlet di importazione di dati di mbam Active Directory (ad)** per copiare il TPM OwnerAuth da un annuncio nel database mbam. Questi sono cinque nuovi cmdlet di PowerShell che prepopolano i database di MBAM con le informazioni sul recupero di volume e sul proprietario del TPM archiviate in Active Directory.

Per altre informazioni, Vedi [considerazioni sulla sicurezza di MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).

### MBAM può sbloccare automaticamente il TPM dopo un blocco

Nei computer che eseguono TPM 1,2 è ora possibile configurare MBAM per sbloccare automaticamente il TPM in caso di blocco. Se la caratteristica di ripristino automatico del blocco TPM è abilitata, MBAM può rilevare che un utente è bloccato e quindi ottenere la password di OwnerAuth dal database MBAM per sbloccare automaticamente il TPM per l'utente.

Questa caratteristica deve essere abilitata sia sul lato server che in criteri di gruppo sul lato client. Per altre informazioni, Vedi [considerazioni sulla sicurezza di MBAM 2,5](mbam-25-security-considerations.md#bkmk-autounlock).

### Supporto per le protezioni per le password numeriche di BitLocker conformi a FIPS

In MBAM 2.5 è stato aggiunto il supporto per le chiavi di ripristino di BitLocker conformi alla Federal Information Processing Standard (FIPS) nei dispositivi che gestiscono il sistema operativo Windows 8,1. Tuttavia, Windows non ha implementato le chiavi di ripristino conformi FIPS in Windows 7. Di conseguenza, i dispositivi Windows 7 e Windows 8 richiedevano ancora una protezione DRA (Data Recovery Agent) per il ripristino.

Il team di Windows ha le chiavi di ripristino conformi allo standard FIPS con un hotfix e MBAM 2,5 SP1 ha aggiunto il supporto anche per loro.

**Nota**  I computer client che eseguono il sistema operativo Windows8 richiedono ancora una protezione DRA perché l'hotfix non è stato sottoportato al sistema operativo. Vedere [pacchetto hotfix 2 per l'amministrazione e il monitoraggio di bitlocker 2,5](https://support.microsoft.com/kb/3015477) per scaricare e installare i computer hotfix per Windows 7 e Windows 8. Per informazioni su DRA, vedere [uso di agenti di recupero dati con BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

 

Per abilitare la conformità FIPS nell'organizzazione, è necessario configurare le impostazioni dei criteri di gruppo FIPS (Federal Information Processing Standard). Per istruzioni sulla configurazione, vedere [impostazioni dei criteri di gruppo di BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

### Personalizzare il messaggio di ripristino di pre-avvio e l'URL con le nuove impostazioni di criteri di gruppo

Una nuova impostazione di criteri di gruppo, **Configura l'URL e il messaggio di ripristino di pre-avvio**, consente di configurare un messaggio di ripristino personalizzato o di specificare un URL che viene quindi visualizzato nella schermata di ripristino di BitLocker di pre-avvio quando l'unità del sistema operativo è bloccata. Questa impostazione è disponibile solo nei computer client che eseguono Windows 10.

Se si abilita questa impostazione per i criteri, è possibile selezionare una di queste opzioni per il messaggio di ripristino di pre-avvio:

-   **Usare il messaggio di ripristino personalizzato**: selezionare questa opzione per includere un messaggio personalizzato nella schermata di ripristino di BitLocker di pre-avvio.

-   **Usare l'URL di ripristino personalizzato**: selezionare questa opzione per sostituire l'URL predefinito visualizzato nella schermata di ripristino di BitLocker di pre-avvio.

-   **Usare l'URL e il messaggio di ripristino predefiniti**: selezionare questa opzione per visualizzare il messaggio e l'URL di ripristino di BitLocker predefiniti nella schermata di ripristino di BitLocker di pre-avvio. Se in precedenza è stato configurato un URL o un messaggio di ripristino personalizzato e si vuole ripristinare il messaggio predefinito, è necessario abilitare questo criterio e selezionare questa opzione.

La nuova impostazione di criteri di gruppo è disponibile nel nodo GPO seguente: criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management)** &gt; **drive del sistema operativo**. Per altre informazioni, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### MBAM ha aggiunto il supporto per la crittografia dello spazio usato

In MBAM 2,5 SP1, se si Abilita la crittografia dello spazio usato tramite criteri di gruppo di BitLocker, il client MBAM lo onora.

Questa impostazione di criteri di gruppo è denominata **Applica tipo di crittografia unità sulle unità del sistema operativo** e si trova nel nodo GPO seguente: **configurazione di computer** &gt; **modelli amministrativi** &gt; **componenti di Windows** &gt; **unità BitLocker Drive** &gt; **System**Encryption. Se si Abilita questo criterio e si seleziona il tipo di crittografia come **solo spazio usato**per la crittografia, mbam consentirà di rispettare i criteri e BitLocker crittografa solo lo spazio su disco usato nel volume.

Per altre informazioni, vedere [pianificazione per i requisiti di criteri di gruppo di MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### Supporto di MBAM client per dischi rigidi crittografati

MBAM supporta BitLocker su dischi rigidi crittografati che soddisfano i requisiti per le specifiche TCG per gli standard Opal e IEEE 1667. Quando BitLocker è abilitato in questi dispositivi, genererà le chiavi ed eseguirà le funzioni di gestione nell'unità crittografata. Per altre informazioni, Vedi disco [rigido crittografato](https://technet.microsoft.com/library/hh831627.aspx) .

### La configurazione della delega non è più necessaria durante la registrazione di nomi SPN

Il requisito per configurare la delega vincolata per i nomi SPN registrati per l'account del pool di applicazioni non è più necessario in MBAM 2,5 SP1. Tuttavia, è ancora un requisito per MBAM 2,5.

### Abilitare BitLocker tramite MBAM come parte di una distribuzione di Windows

In MBAM 2,5 SP1, è possibile usare uno script di PowerShell per configurare le chiavi di ripristino unità BitLocker e di recupero escrow nel server MBAM.

Per altre informazioni, vedere [come abilitare BitLocker tramite mbam come parte di una distribuzione di Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

### Il portale self-service può essere personalizzato usando PowerShell o la procedura guidata di personalizzazione del provider di servizi condivisi

A partire da MBAM 2,5 SP1, il portale self-service può essere configurato usando la procedura guidata per la personalizzazione e l'uso di PowerShell. Vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

### Il Web browser non viene più eseguito involontariamente come amministratore

Un problema in MBAM 2,5 ha causato collegamenti della guida nello strumento di configurazione del server per consentire l'apertura delle finestre del browser con i diritti di amministratore. Questo problema è stato risolto in MBAM 2,5 SP1.

### Non è più necessario scaricare i file JavaScript per configurare il portale self-service quando la rete CDN non è accessibile

In MBAM 2,5 e versioni precedenti, i file jQuery usati per la configurazione del portale self-service dovevano essere scaricati dalla rete CDN in anticipo se i client che accedevano al portale self-service non avevano accesso a Internet. In MBAM 2,5 SP1 tutti i file JavaScript sono inclusi nel prodotto, quindi non è necessario scaricarli.

### I report possono essere aperti in Generatore report 3,0

In MBAM 2,5 SP1 i report sono stati aggiornati allo schema del linguaggio di definizione del report più recente, consentendo agli utenti di aprire e personalizzare i report in Generatore report 3,0 e di salvarli immediatamente senza danneggiare il file di report.

### Nuovi cmdlet di PowerShell

I nuovi cmdlet di PowerShell per MBAM 2,5 SP1 consentono di configurare e gestire diverse funzionalità di MBAM, tra cui database, report e applicazioni Web. Ogni funzionalità include un cmdlet di PowerShell corrispondente che puoi usare per abilitare o disabilitare le funzionalità o per ottenere informazioni sulla funzionalità.

I cmdlet seguenti sono stati implementati per MBAM 2,5 SP1:

-   Write-MbamTpmInformation

-   Write-MbamRecoveryInformation

-   Read-ADTpmInformation

-   Read-ADRecoveryInformation

-   Write-MbamComputerUser

I parametri seguenti sono stati implementati nei cmdlet Enable-MbamWebApplication e test-MbamWebApplication per MBAM 2,5 SP1:

-   DataMigrationAccessGroup

-   TpmAutoUnlock

Per informazioni sui cmdlet, vedere Considerazioni sulla [sicurezza di MBAM 2,5](mbam-25-security-considerations.md) e [Guida per i cmdlet di amministrazione e monitoraggio di Microsoft BitLocker](https://technet.microsoft.com/library/dn720418.aspx).

### L'agente MBAM rileva la modalità presentazione

L'agente MBAM può rilevare quando il computer è in modalità presentazione ed evitare di richiamare l'interfaccia utente di MBAM in quel momento.

### Servizio di agente MBAM ora configurato per l'uso dell'avvio ritardato

Dopo l'installazione, il servizio imposta il servizio MBAM Agent per l'uso dell'avvio ritardato, diminuendo la quantità di tempo necessaria per avviare Windows.

### I volumi di dati fissi bloccati vengono ora segnalati come conformi

La logica di calcolo della conformità per i volumi "bloccati per i dati fissi" è stata cambiata per segnalare i volumi come "conforme", ma con uno stato di protezione e la crittografia dello stato "sconosciuto" e con un dettaglio dello stato di conformità di "volume bloccato". In precedenza, i volumi bloccati venivano segnalati come "non conformi", uno stato di protezione "crittografato", uno stato di crittografia "sconosciuto" e un dettaglio dello stato di conformità di "errore sconosciuto".


## Come ottenere le tecnologie MDOP


MBAM fa parte del Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte del programma Microsoft Software Assurance. Per altre informazioni sul programma Microsoft Software Assurance e su come acquisire il MDOP, vedere [come si ottiene MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## Note sulla versione di MBAM 2,5 SP1


Per altre informazioni e notizie aggiornate che non sono incluse in questa documentazione, vedere note sulla [versione per MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Argomenti correlati


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)

 

 





