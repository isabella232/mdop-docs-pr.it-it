---
title: Considerazioni sulla sicurezza per UE-V 2.x
description: Considerazioni sulla sicurezza per UE-V 2.x
author: dansimp
ms.assetid: 9d5c3cae-9fcb-4dea-bd67-741b3dea63be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8e24e9e37de11053663bb90974fabf2ff369aeca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824665"
---
# Considerazioni sulla sicurezza per UE-V 2.x


Questo argomento contiene una breve panoramica di account e gruppi, file di log e altre considerazioni relative alla sicurezza per Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1. Per altre informazioni, seguire i collegamenti forniti qui.

## Considerazioni sulla sicurezza per la configurazione di UE-V


**Importante**  Quando si crea la condivisione di archiviazione delle impostazioni, limitare l'accesso alla condivisione agli utenti che richiedono l'accesso.

 

Poiché i pacchetti di impostazioni potrebbero contenere informazioni personali, è necessario prestare particolare attenzione per proteggerli nel modo migliore possibile. In generale, eseguire le operazioni seguenti:

-   Limitare la condivisione solo agli utenti che richiedono l'accesso. Creare un gruppo di sicurezza per gli utenti che hanno reindirizzato le cartelle in una determinata condivisione e limitano l'accesso solo agli utenti.

-   Quando si crea la condivisione, nascondere la condivisione inserendo un $ dopo il nome della condivisione. Questa aggiunta nasconde la condivisione da browser casual e la condivisione non è visibile in risorse di rete.

-   Assegna solo agli utenti la quantità minima di autorizzazioni che devono avere. Le tabelle seguenti mostrano le autorizzazioni necessarie.

    1.  Impostare le autorizzazioni SMB a livello di condivisione seguenti per la cartella della posizione di archiviazione dell'impostazione.

        | Account utente | Autorizzazioni consigliate |
        | - | - |
        | Tutti | Nessuna autorizzazione |
        |Gruppo sicurezza di UE-V | Controllo completo |

    2.  Impostare le autorizzazioni di file system NTFS seguenti per la cartella della posizione di archiviazione delle impostazioni.

        | Account utente | Autorizzazioni consigliate | Cartella |
        | - | - | - |
        | Creatore/proprietario | Controllo completo | Solo sottocartelle e file|
        | Amministratori di dominio | Controllo completo | Questa cartella, le sottocartelle e i file |
        | Gruppo di sicurezza degli utenti di UE-V | Cartella di elenco/dati letti, creare cartelle/accodare dati | Solo questa cartella |
        | Tutti | Rimuovere tutte le autorizzazioni | Nessuna autorizzazione |

    3.  Impostare le autorizzazioni SMB a livello di condivisione seguenti per la cartella del catalogo dei modelli di impostazioni.

        | Account utente | Consigliare le autorizzazioni |
        | - | - |
        | Tutti | Nessuna autorizzazione |
        | Computer di dominio | Livelli di autorizzazione di lettura |
        | Administrators | Livelli di autorizzazione di lettura/scrittura |
         
    4.  Impostare le autorizzazioni NTFS seguenti per la cartella del catalogo dei modelli di impostazioni.

        | Account utente | Autorizzazioni consigliate | Applica a |
        | - | - | - |
        | Creatore/proprietario | Controllo completo | Questa cartella, le sottocartelle e i file |
        | Computer di dominio | Contenuto della cartella di elenco e autorizzazioni di lettura | Questa cartella, le sottocartelle e i file|
        | Tutti| Nessuna autorizzazione| Nessuna autorizzazione|
        | Administrators| Controllo completo| Questa cartella, le sottocartelle e i file|

### Usare WindowsServer come di WindowsServer2003 per ospitare le condivisioni di file reindirizzate

I file di pacchetto delle impostazioni utente contengono informazioni personali trasferite tra il computer client e il server in cui sono archiviati i pacchetti di impostazioni. A causa di questo processo, devi assicurarti che i dati siano protetti mentre viaggiano in rete.

I dati delle impostazioni utente sono vulnerabili a queste potenziali minacce: l'intercettazione dei dati durante il passaggio sulla rete, la manomissione dei dati durante il passaggio della rete e lo spoofing del server che ospita i dati.

A partire da Windows Server2003, diverse funzionalità del sistema operativo Windows Server possono aiutare a proteggere i dati degli utenti:

-   **Kerberos** -Kerberos è standard in tutte le versioni di Microsoft Windows2000Server e WindowsServer che iniziano con WindowsServer2003. Kerberos garantisce il più alto livello di sicurezza per le risorse di rete. NTLM autentica il client solo; Kerberos autentica il server e il client. Quando si usa NTLM, il client non sa se il server è valido. Questa differenza è particolarmente importante se il client scambia i file personali con il server, come nel caso dei profili utente mobili. Kerberos offre una sicurezza migliore rispetto a NTLM. Kerberos non è disponibile nei sistemi operativi Microsoft WindowsNTServer 4,0 o versioni precedenti.

-   **IPSec** : il protocollo IPSec (IP Security Protocol) offre l'autenticazione a livello di rete, l'integrità dei dati e la crittografia. IPsec garantisce le operazioni seguenti:

    -   I dati in roaming sono al sicuro dalla modifica dei dati mentre i dati sono in viaggio.

    -   I dati in roaming sono sicuri dall'intercettazione, dalla visualizzazione o dalla copia.

    -   I dati in roaming sono sicuri dall'accesso da parte di parti non autenticate.

-   **SMB signing** -il protocollo di autenticazione SMB (Server Message Block) supporta l'autenticazione dei messaggi, che impedisce gli attacchi di tipo Active Message e "Man-in-the-Middle". La firma SMB fornisce questa autenticazione inserendo una firma digitale in ogni SMB. La firma digitale viene quindi verificata sia dal client che dal server. Per usare la firma SMB, è prima necessario abilitarla oppure è necessario richiederla sia nel client SMB che nel server SMB. Tieni presente che la firma SMB impone una penalizzazione delle prestazioni. Non utilizza più larghezza di banda della rete, ma usa più cicli di CPU sul lato client e server.

### Usare sempre il file system NTFS per i volumi che contengono i dati utente

Per la configurazione più sicura, configurare i server che ospitano i file delle impostazioni UE-V per usare il file system NTFS. A differenza del file system FAT, NTFS supporta gli elenchi di controllo di accesso discrezionale (DACL) e gli elenchi di controllo di accesso di sistema (SACL). Gli elenchi DACL e SACL controllano chi può eseguire operazioni su un file e quali eventi attivano la registrazione delle azioni eseguite in un file.

### Non affidarsi a EFS per crittografare i file utente quando vengono trasmessi tramite la rete

Quando si usa crittografia file System (EFS) per crittografare i file in un server remoto, i dati crittografati non vengono crittografati durante il transito sulla rete; viene crittografato solo quando è archiviato su disco.

Questo processo di crittografia non si applica quando il sistema include IPsec (Internet Protocol Security) o WebDAV (Web Distributed Authoring and Versioning). IPsec crittografa i dati mentre viene trasportato su una rete TCP/IP. Se il file è crittografato prima che venga copiato o spostato in una cartella WebDAV in un server, rimane crittografato durante la trasmissione e mentre viene archiviato nel server.

### Consentire all'agente UE-V di creare cartelle per ogni utente

Per assicurarsi che UE-V funzioni in modo ottimale, creare solo la condivisione radice sul server e consentire all'agente UE-V di creare le cartelle per ogni utente. UE-V crea queste cartelle utente con la sicurezza appropriata.

Questa configurazione di autorizzazione consente agli utenti di creare cartelle per l'archiviazione delle impostazioni. L'agente UE-V crea e protegge una cartella del pacchetto di impostazioni durante l'esecuzione nel contesto dell'utente. Gli utenti ricevono il controllo completo nella cartella del pacchetto di impostazioni. Altri utenti non ereditano l'accesso alla cartella. Non è necessario creare e proteggere le singole directory utente. L'agente che viene eseguito nel contesto dell'utente lo esegue automaticamente.

**Nota**  La sicurezza aggiuntiva può essere configurata quando viene usato un server Windows per la condivisione di archiviazione delle impostazioni. L'opzione UE-V può essere configurata per verificare che il gruppo Administrators locale o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni. Per abilitare la sicurezza aggiuntiva, usare il comando seguente:

1.  Aggiungere la chiave del registro di sistema REG \ _DWORD RepositoryOwnerCheckEnabled a `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Impostare il valore della chiave del registro di sistema su *1*.

Quando questa impostazione di configurazione è in posizione, l'agente UE-V Verifica che il gruppo Administrators locale o l'utente corrente sia il proprietario della cartella del pacchetto di impostazioni. In caso contrario, l'agente UE-V non concede l'accesso alla cartella.

 

Se è necessario creare cartelle per gli utenti, verificare di avere impostato le autorizzazioni corrette.

Ti consigliamo vivamente di non creare cartelle preliminari. Consente invece all'agente UE-V di creare la cartella per l'utente.

### Verificare le autorizzazioni corrette per archiviare le impostazioni di UE-V 2 in una directory Home o in una directory personalizzata

Se si reindirizza le impostazioni di UE-V nella home directory di un utente o in una directory Active Directory (AD) personalizzata, assicurarsi che le autorizzazioni per la directory siano impostate in modo appropriato per l'organizzazione.






## Argomenti correlati


[Documentazione tecnica su UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





