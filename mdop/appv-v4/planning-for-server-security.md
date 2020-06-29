---
title: Pianificazione per la sicurezza dei server
description: Pianificazione per la sicurezza dei server
author: dansimp
ms.assetid: c7cd8227-b359-41e7-a8ae-d0d5718a76a2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bea1bd8287a15385200bbfb425ed8e00fbcdb02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815905"
---
# Pianificazione per la sicurezza dei server


Per migliorare la sicurezza di un ambiente, è necessario esaminare l'esposizione a eventuali potenziali minacce nell'ambiente. La sicurezza per un'infrastruttura di App-V richiede l'uso delle caratteristiche di sicurezza App-V specifiche, nonché le procedure e le funzionalità di sicurezza per l'infrastruttura sottostante. La protezione dell'infrastruttura sottostante per servizi come Internet Information Services (IIS), servizi di dominio Active Directory e SQL Server migliorerà la sicurezza complessiva per il sistema App-V.

Le impostazioni predefinite per l'installazione del server garantiscono i livelli di sicurezza più alti. Tuttavia, alcuni componenti si basano sull'infrastruttura sottostante che non è configurata come parte dell'installazione. La procedura successiva all'installazione migliorerà la sicurezza dell'infrastruttura di App-V.

La directory di contenuto contiene tutti i pacchetti che devono essere trasmessi ai client. Queste risorse devono essere il più sicuro possibile per eliminare molti possibili rischi per la sicurezza. L'elenco seguente offre alcune indicazioni aggiuntive:

-   Pubblicazione e/o flusso basato su UNC: le autorizzazioni per questo elemento devono essere le più restrittive nell'ambiente. Usare le autorizzazioni NTFS per implementare gli elenchi di controllo di accesso (ACL) più restrittivi per la directory di contenuto (utenti = lettura, amministratori = lettura e scrittura).

-   IIS usato per la pubblicazione e/o lo streaming: configura IIS per supportare solo l'autenticazione integrata di Windows. Rimuovere l'accesso anonimo al server IIS e limitare l'accesso alla directory con le autorizzazioni NTFS.

-   RTSP/RTSPs per trasmettere pacchetti di applicazioni: configurare i criteri del provider App-V per richiedere l'autenticazione, applicare le autorizzazioni di accesso e abilitare solo i gruppi obbligatori ad avere accesso ai criteri del provider. Configurare le applicazioni con le autorizzazioni appropriate nel database.

Limitare al minimo il numero di utenti con privilegi amministrativi per ridurre le possibili minacce per i dati nell'archivio dati e per evitare di pubblicare applicazioni illecite nell'infrastruttura.

## Protezione della virtualizzazione delle applicazioni


App-V usa diversi metodi di comunicazione tra i vari componenti dell'infrastruttura. Quando si pianifica l'infrastruttura di App-V, la protezione delle comunicazioni tra i server può ridurre i rischi per la sicurezza che potrebbero essere già presenti nella rete esistente.

### Archivio dati

L'Application Virtualization Management Server e il servizio di gestione della virtualizzazione delle applicazioni comunicano con l'archivio dati tramite una connessione SQL tramite la porta TCP 1433. Il server di gestione usa l'archivio dati per recuperare i dati dell'applicazione e della configurazione e scrive le informazioni sull'utilizzo nel database. Il servizio di gestione comunica con l'archivio dati per conto di un amministratore che sta configurando l'infrastruttura App-V. Dato che l'archivio dati contiene informazioni critiche, è importante minimizzare le minacce per questi dati.

Si consiglia di proteggere le comunicazioni tra App-V Management Server, il servizio di gestione e l'archivio dati con IPsec (Internet Protocol Security). In particolare, creare criteri che proteggano il canale di comunicazione tra l'archivio dati (SQL) e il server di gestione e l'archivio dati e il servizio di gestione. È anche possibile distribuire l'isolamento del server e del dominio con IPsec, garantendo che tutti i componenti dell'infrastruttura App-V comunichino solo con i canali sicuri. Per informazioni sull'implementazione di IPsec, vedere la documentazione seguente:

-   Per Windows Server2003, vedere <https://go.microsoft.com/fwlink/?LinkId=133226> ( https://go.microsoft.com/fwlink/?LinkId=133226) .

-   Per Windows Server2008, vedere <https://go.microsoft.com/fwlink/?LinkId=133227> ( https://go.microsoft.com/fwlink/?LinkId=133227) .

### Directory di contenuto

L'installazione di App-V Management Server configura una posizione per la directory di contenuto. Questa directory è la posizione di archiviazione per i pacchetti di applicazioni virtualizzate. Questa posizione può essere locale per il server oppure può essere inserita in una condivisione di rete remota. Implementare quindi IPsec per proteggere la comunicazione con una posizione remota per la directory di contenuto.

È anche possibile usare una directory virtuale in un server IIS per eseguire il flusso di pacchetti ai client. Se la directory virtuale creata per il contenuto si trova in un'origine remota, usare IPsec per proteggere la comunicazione tra il server IIS e la posizione di archiviazione remota.

La directory di contenuto contiene tutti i pacchetti che vengono trasmessi ai client. Queste risorse devono essere il più sicuro possibile per eliminare molti possibili rischi per la sicurezza.

### Protocolli di sicurezza

Puoi usare RTSPs o HTTPS per migliorare le comunicazioni sicure. RTSPs è il protocollo usato dai server App-V e HTTPS è il protocollo usato dai server IIS. Questi protocolli vengono usati per la pubblicazione di applicazioni dal server al client Desktop Application Virtualization. Dopo aver determinato il protocollo desiderato, aggiungere un server di pubblicazione che usa tale protocollo.

### <a href="" id="configuring-app-v-servers-for-rtsps-"></a>Configurazione dei server App-V per RTSPs

L'installazione o la configurazione di un'app-V Management Server o di un server di flusso per l'uso della sicurezza avanzata (ad esempio, TLS) richiede che un certificato X. 509 v3 venga provisionato nel server App-V. Quando si prepara l'installazione o la configurazione della sicurezza per un server, è necessario soddisfare alcuni requisiti specifici. I requisiti tecnici per la distribuzione e la configurazione dei certificati per un'app-V Management Server o un server di flusso più sicuro sono i seguenti:

-   Il certificato deve essere valido. In caso contrario, il client interrompe la connessione.

-   Il certificato deve contenere l'autenticazione di utilizzo della chiave avanzata (EKU) corretto (OID 1.3.6.1.5.5.7.3.1). In caso contrario, il client interrompe la connessione.

-   Il nome di dominio completo (FQDN) del certificato deve corrispondere al server in cui è installato. Ad esempio, se il client chiama `RTSPS://Myserver.mycompany.com/content/MyApp.sft` , ma il certificato **rilasciato al** campo contiene `Myserver1.mycompany.com` , il client non si connette al server e la sessione viene terminata, anche se `Myserver.mycompany.com` e `Myserver1.mycompany.com` risolve lo stesso indirizzo IP.

    **Nota**  Se usi App-V in un cluster di bilanciamento del carico di rete, il certificato deve essere configurato con *i nomi alternativi oggetto* (sans) per supportare RTSPS. Per informazioni sulla configurazione dell'autorità di certificazione (CA) e sulla creazione di certificati con SANs, vedere <https://go.microsoft.com/fwlink/?LinkId=133228> ( https://go.microsoft.com/fwlink/?LinkId=133228) .

     

-   La CA che rilascia il certificato al server App-V deve essere considerata attendibile dal client che si connette al server. In caso contrario, il client interrompe la connessione.

-   È necessario modificare le autorizzazioni per la *chiave privata del certificato* per consentire l'accesso tramite il servizio app Server-V. Per impostazione predefinita, i servizi App-V Management Server e streaming server vengono eseguiti con l'account del servizio di rete. Quando viene generato un PKCS \ #10 nel server, viene creata una chiave privata. Solo il sistema locale e i gruppi di amministratori hanno accesso a questa chiave. Questi ACL predefiniti impediscono all'App-V Server di accettare connessioni sicure.

    **Nota**  Per informazioni sulla configurazione di un'infrastruttura a chiave pubblica (PKI), vedere <https://go.microsoft.com/fwlink/?LinkId=133229> ( https://go.microsoft.com/fwlink/?LinkId=133229) .

     

### Configurazione di server IIS con HTTPS

App-V potrebbe usare i server IIS in alcune configurazioni di infrastruttura. Per altre informazioni sulla configurazione dei server IIS, vedere <https://go.microsoft.com/fwlink/?LinkId=133230> ( https://go.microsoft.com/fwlink/?LinkId=133230) .

**Nota**  Se si usa IIS per pubblicare i file ICO e OSD, configurare un tipo MIME per OSD = TXT; in caso contrario, IIS rifiuterà di servire i file ICO e OSD ai client.

 

### Sicurezza a livello di applicazione

Puoi configurare i server per lo streaming di applicazioni specifiche nel desktop di un utente. Tuttavia, l'autorizzazione di accesso viene effettivamente concessa a livello di pacchetto, non a livello di applicazione. Anche se un'applicazione specifica potrebbe non essere pubblicata nel desktop dell'utente, se l'utente ha l'autorizzazione per aggiungere applicazioni o è un amministratore nel computer client, l'utente può creare e usare un collegamento sul client per eseguire tutte le applicazioni in un pacchetto.

## Configurazione dell'amministrazione di App-V per un ambiente distribuito


Quando si progetta l'infrastruttura per la propria organizzazione, è possibile installare il servizio Web di gestione App-V in un computer diverso dal computer in cui si installa l'App-V Management Server. I motivi comuni per separare questi componenti App-V includono i seguenti:

-   Prestazioni

-   Affidabilità

-   Disponibilità

-   Scalabilità

Affinché l'infrastruttura funzioni correttamente, la separazione tra App-V Management Console, server di gestione e servizio Web di gestione richiede una configurazione aggiuntiva. Per informazioni dettagliate su come configurare il server, vedere [come configurare il server in modo che sia attendibile per la delega](how-to-configure-the-server-to-be-trusted-for-delegation.md).

## Argomenti correlati


[Pianificazione per sicurezza e protezione](planning-for-security-and-protection.md)

 

 





