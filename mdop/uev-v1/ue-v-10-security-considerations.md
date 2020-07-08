---
title: Considerazioni sulla sicurezza di UE-V 1.0
description: Considerazioni sulla sicurezza di UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823996"
---
# Considerazioni sulla sicurezza di UE-V 1.0


Questo argomento contiene una breve panoramica di account e gruppi, file di log e altre considerazioni relative alla sicurezza per Microsoft User Experience Virtualization (UE-V). Per altre informazioni, seguire i collegamenti forniti qui.

## Considerazioni sulla sicurezza per la configurazione di UE-V


**Quando si crea la condivisione di archiviazione delle impostazioni, limitare l'accesso alla condivisione agli utenti che hanno bisogno di Access.**

Poiché i pacchetti di impostazioni possono contenere informazioni personali, è necessario prestare particolare attenzione per proteggerli nel modo migliore possibile. In generale, eseguire le operazioni seguenti:

-   Limita la condivisione solo agli utenti che hanno bisogno di Access. Creare un gruppo di sicurezza per gli utenti con cartelle reindirizzate in una particolare condivisione e limitare l'accesso solo agli utenti.

-   Quando si crea la condivisione, nascondere la condivisione inserendo un $ dopo il nome della condivisione. In questo modo si nasconderà la condivisione da browser casual e la condivisione non sarà visibile nelle risorse di rete.

-   Concedere agli utenti solo l'importo minimo delle autorizzazioni necessarie. Le autorizzazioni necessarie sono illustrate nelle tabelle seguenti.

    1.  Impostare le seguenti autorizzazioni SMB (share-level) per la cartella della posizione di archiviazione dell'impostazione:

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left">Account utente</th>
        <th align="left">Autorizzazioni consigliate</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Tutti</p></td>
        <td align="left"><p>Nessuna autorizzazione</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Gruppo sicurezza di UE-V</p></td>
        <td align="left"><p>Controllo completo</p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### Usare i server Windows Server 2003 o versione successiva per ospitare le condivisioni file reindirizzate

I file di pacchetto delle impostazioni utente contengono informazioni personali trasferite tra il computer client e il server in cui sono archiviati i pacchetti di impostazioni. Per questo motivo, devi assicurarti che i dati siano protetti mentre viaggiano in rete.

I dati delle impostazioni utente sono vulnerabili a queste potenziali minacce: l'intercettazione dei dati durante l'attraversamento della rete; manomissione dei dati durante l'attraversamento della rete; e lo spoofing del server che ospita i dati.

Diverse funzionalità di Windows Server 2003 e versioni successive consentono di proteggere i dati degli utenti:

-   **Kerberos** -Kerberos è standard in tutte le versioni di Windows 2000 e windows Server 2003 e versioni successive. Kerberos garantisce il più alto livello di sicurezza per le risorse di rete. NTLM autentica il client solo; Kerberos autentica il server e il client. Quando si usa NTLM, il client non sa se il server è valido. Questo è particolarmente importante se il client scambia i file personali con il server, come nel caso dei profili mobili. Kerberos offre una sicurezza migliore rispetto a NTLM. Kerberos non è disponibile nei sistemi operativi Windows NT versione 4,0 o versioni precedenti.

-   **IPSec** : il protocollo IPSec (IP Security Protocol) offre l'autenticazione a livello di rete, l'integrità dei dati e la crittografia. IPsec garantisce le operazioni seguenti:

    -   I dati in roaming sono al sicuro dalla modifica dei dati durante la route.

    -   I dati in roaming sono sicuri dall'intercettazione, dalla visualizzazione o dalla copia.

    -   I dati in roaming sono sicuri per l'accesso da parte di parti non autenticate.

-   **SMB signing** -il protocollo di autenticazione SMB (Server Message Block) supporta l'autenticazione dei messaggi che impedisce gli attacchi di tipo Active Message e "Man-in-the-Middle". La firma SMB fornisce questa autenticazione inserendo una firma digitale in ogni SMB. La firma digitale viene quindi verificata sia dal client che dal server. Per usare la firma SMB, è prima necessario abilitarla o richiederla sia nel client SMB che nel server SMB. Tieni presente che la firma SMB impone una penalizzazione delle prestazioni. Non utilizza più larghezza di banda della rete, ma usa più cicli di CPU sul lato client e server.

### Usare sempre il file system NTFS per i volumi che tengono i dati degli utenti

Per la configurazione più sicura, configurare i server che ospitano i file delle impostazioni UE-V per usare il file system NTFS. Diversamente da FAT, NTFS supporta gli elenchi di controllo di accesso discrezionale (DACL) e gli elenchi di controllo di accesso di sistema (SACL). Gli elenchi DACL e SACL controllano chi può eseguire operazioni su un file e quali eventi attiverà la registrazione delle azioni eseguite in un file.

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a>Non affidarsi a EFS per crittografare i file degli utenti quando vengono trasmessi tramite la rete

Quando si usa crittografia file System (EFS) per crittografare i file in un server remoto, i dati crittografati non vengono crittografati durante il transito sulla rete; Viene crittografato solo quando è archiviato su disco.

Le eccezioni a questo problema si verificano quando il sistema include IPsec (Internet Protocol Security) o WebDAV (Web Distributed Authoring and Versioning). IPsec crittografa i dati mentre viene trasportato su una rete TCP/IP. Se il file viene crittografato prima di essere copiato o spostato in una cartella WebDAV in un server, resterà crittografato durante la trasmissione e mentre viene archiviato nel server.

### Crittografare la cache dei file offline

Per impostazione predefinita, la cache dei file offline è protetta dalle partizioni NTFS tramite ACL, ma la crittografia della cache migliora ulteriormente la sicurezza in un computer locale. Per impostazione predefinita, la cache nel computer locale non è crittografata, quindi qualsiasi file crittografato memorizzato nella cache dalla rete non verrà crittografato nel computer locale. Questo potrebbe rappresentare un rischio per la sicurezza in alcuni ambienti.

Quando la crittografia è abilitata, tutti i file della cache dei file offline vengono crittografati. Questo include la crittografia dei file esistenti e i file che verranno aggiunti in un secondo momento. La copia memorizzata nella cache nel computer locale è interessata, ma la copia di rete associata non è.

La cache può essere crittografata in uno dei due modi seguenti:

1.  Tramite criteri di gruppo. -Abilitare l'impostazione **Crittografa la cache dei file offline** , disponibile nel computer Configuration\\Administrative Templates\\Network\\Offline file, nell'Editor criteri di gruppo.

2.  Manualmente. -Selezionare strumenti e quindi Opzioni cartella nel menu di comando di Esplora risorse. Selezionare la scheda file offline e quindi selezionare la casella **di controllo Crittografa i file offline per i dati protetti** .

### Consentire all'agente UE-V di creare cartelle per ogni utente

Per assicurarsi che UE-V funzioni in modo ottimale, creare solo la condivisione radice sul server e consentire all'agente UE-V di creare le cartelle per ogni utente. UE-V creerà queste cartelle utente con la sicurezza appropriata.

Questa configurazione delle autorizzazioni consente agli utenti di creare cartelle per l'archiviazione delle impostazioni. L'agente UE-V crea e protegge una cartella settingspackage durante l'esecuzione nel contesto dell'utente. L'utente riceve il controllo completo nella propria cartella settingspackage. Altri utenti non ereditano l'accesso alla cartella. Non è necessario creare e proteggere le singole directory utente. Questa operazione verrà eseguita automaticamente dall'agente che viene eseguito nel contesto dell'utente.

**Nota**  
La sicurezza aggiuntiva può essere configurata quando viene usato un server Windows per la condivisione di archiviazione delle impostazioni. L'opzione UE-V può essere configurata per verificare che il gruppo di amministratori locali o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni. Per abilitare la sicurezza aggiuntiva, usare il comando seguente:

1.  Aggiungere una chiave del registro di sistema REG \ _DWORD denominata "RepositoryOwnerCheckEnabled" `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Impostare il valore della chiave del registro di sistema su 1.

Quando questa impostazione di configurazione è in posizione, l'agente UE-V Verifica che il gruppo o l'utente corrente dell'amministratore locale sia il proprietario della cartella settingspackage. In caso contrario, l'agente UE-V non consentirà l'accesso alla cartella.



Se è necessario creare cartelle per gli utenti e verificare di avere impostato le autorizzazioni corrette.

Ti consigliamo vivamente di non creare cartelle precreative e, invece, puoi consentire all'agente UE-V di creare la cartella per l'utente.

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a>Verificare che le autorizzazioni corrette vengano impostate durante l'archiviazione delle impostazioni di UE-V nella home directory di un utente

Se si reindirizza le impostazioni di UE-V nella home directory di un utente, assicurarsi che le autorizzazioni nella directory Home dell'utente siano impostate in modo appropriato per l'organizzazione.

## Argomenti correlati


[Sicurezza e privacy per UE-V 1.0](security-and-privacy-for-ue-v-10.md)









