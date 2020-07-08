---
title: Note sulla versione di MBAM 1.0
description: Note sulla versione di MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826026"
---
# Note sulla versione di MBAM 1.0


**Per cercare un problema specifico in queste note sulla versione, premere CTRL + F.**

Leggere queste note sulla versione accuratamente prima di installare Microsoft BitLocker Administration and Monitoring (MBAM).

Queste note sulla versione contengono informazioni necessarie per installare correttamente MBAM. Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di MBAM, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Informazioni sulla documentazione del prodotto


Per informazioni sulla documentazione di MBAM, vedere la Home page di MBAM in Microsoft TechNet.

Per ottenere una copia scaricabile della documentazione di MBAM, vedere nell' <https://go.microsoft.com/fwlink/p/?LinkId=225356> area download Microsoft.

## Inviare commenti e suggerimenti


Siamo interessati al feedback su MBAM. È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .

**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future nella documentazione e nei rilasci del prodotto.

 

Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemi noti di MBAM 1,0


Questa sezione contiene note sulla versione sui problemi noti relativi alla configurazione e all'installazione di MBAM.

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a>Se si seleziona l'opzione "usa un certificato per crittografare la comunicazione di rete" durante l'installazione, le connessioni a database esistenti e le applicazioni dipendenti possono interrompere il funzionamento

È possibile configurare MBAM per la **comunicazione di rete crittografata** dopo aver installato il database di ripristino e hardware o le caratteristiche del database dello stato di conformità. Se si sceglie di configurare MBAM per la comunicazione di rete crittografata, MBAM setup Configura l'istanza del motore di database di SQL Server in modo da usare SSL (Secure Sockets Layer) per la comunicazione tra il database applicabile e il server di amministrazione e monitoraggio e le caratteristiche del server di report di conformità e controllo.

-   Se l'istanza di motore di database di SQL Server non è già configurata per l'uso di SSL, la configurazione di MBAM lo configura per farlo. Questo può impedire alle applicazioni che provano di usare database non MBAM nell'istanza del motore di database di SQL Server di comunicare con i loro database.

-   Se l'istanza di motore di database di SQL Server è già configurata per l'uso di SSL, è configurata per l'uso del certificato selezionato dall'utente durante l'installazione. Se il certificato è diverso da quello già in uso, può impedire l'utilizzo di database di SQL Server nell'istanza del motore di database di SQL Server.

**Soluzione alternativa:** Nessuno

### La configurazione di MBAM non riesce durante l'installazione quando si usa un account di amministratore locale

La configurazione di MBAM non riesce quando si usa un account di amministratore locale. Il file di log contiene le informazioni seguenti:

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

**Soluzione alternativa:** Usare un account di dominio con credenziali amministrative nel computer server durante l'installazione di MBAM.

### La configurazione di MBAM riconfigura l'istanza del motore di database di SQL Server per non usare SSL se selezioni "non crittografare le comunicazioni di rete"

Quando si installa il database di ripristino e hardware o il database dello stato di conformità, è possibile usare la configurazione per configurare MBAM selezionando **comunicazioni di rete crittografate**. Se si decide di non crittografare la comunicazione di rete, la configurazione di MBAM riconfigura l'istanza del motore di database di SQL Server in modo che non usi SSL.

-   Se l'istanza di motore di database di SQL Server è già configurata per l'uso di SSL, la configurazione di MBAM Disabilita SSL nell'istanza del motore di database di SQL Server. Questo modifica la sicurezza delle comunicazioni tra le applicazioni che usano database non correlati ai database di MBAM nell'istanza di motore di database di SQL Server.

**Soluzione alternativa:** Nessuno

### Prerequisiti mancanti per gli script di gestione Internet Information Services (IIS) e gli strumenti Web Server

La configurazione di MBAM dipende dagli script di gestione di IIS e dalle funzionalità del server Web degli strumenti, ma non è un prerequisito imposta. La configurazione del server consente di installare MBAM quando manca questa caratteristica. In questo modo, tuttavia, il servizio di backup MBAM VSS Writer verrà avviato e quindi si arresta, perché non può individuare il provider di Strumentazione gestione Windows (WMI) e Internet Information Services (IIS). Non viene visualizzato alcun messaggio di errore per questa condizione, ad eccezione di quello che si verifica nel log eventi. L'installazione di MBAM senza gli script e gli strumenti di gestione di IIS fa in modo che le operazioni di backup non vengano eseguite per MBAM.

**Soluzione alternativa:** Prima di avviare la configurazione di MBAM, assicurati che la funzionalità di gestione degli script e degli strumenti del server Web sia installata in IIS.

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a>La configurazione di MBAM smette di rispondere durante la fase "installazione delle caratteristiche selezionate" quando la configurazione è configurata per l'uso di un certificato

La configurazione di MBAM smette di rispondere durante la fase di installazione delle **caratteristiche selezionate** . Questo problema si verifica durante l'installazione del database di ripristino e hardware o del database dello stato di conformità, dopo aver selezionato l'opzione **Usa un certificato per crittografare la comunicazione di rete** . Inoltre, la configurazione di MBAM smette di rispondere se l'istanza di motore di database di SQL Server non riesce ad accedere al certificato specificato durante l'installazione.

**Soluzione alternativa:** Aggiornare le autorizzazioni per il certificato, in modo che il servizio Windows per l'istanza applicabile di motore di database di SQL Server possa accedere al certificato. È anche possibile modificare l'account in cui viene eseguita l'istanza del motore di database di SQL Server, in modo che il motore di database usi il certificato. Per determinare le autorizzazioni per il certificato, digitare il comando seguente al prompt dei comandi: **certutil-v-Store My**

### La configurazione di MBAM viene sospesa durante l'installazione di SQL Server Reporting Services

Durante l'installazione di MBAM, quando si seleziona un'istanza di SQL Server Reporting Services (SSRS) e l'istanza di SSRS non è disponibile o è configurata in modo non corretto, la configurazione di MBAM potrebbe essere sospesa fino a un minuto mentre tenta di comunicare con l'istanza di SSRS.

**Soluzione alternativa:** Attendere almeno un minuto per la configurazione di MBAM per riprendere mentre il programma di installazione tenta di contattare l'istanza di SSRS.

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a>Il server di amministrazione e monitoraggio non viene eseguito dopo la configurazione

Dopo la configurazione di MBAM installa correttamente la funzionalità di amministrazione e monitoraggio del server, MBAM Visualizza i messaggi di errore quando si tenta di accedere al sito Web dell'amministratore di MBAM. Questo problema si verifica per uno dei motivi seguenti:

-   Uno o più prerequisiti per l'amministrazione e il server di monitoraggio sono stati rimossi dopo l'installazione di MBAM.

-   Uno o più prerequisiti sono stati installati nel server e in seguito sono stati rimossi prima di eseguire la configurazione di MBAM.

**Soluzione alternativa:** Esaminare la documentazione di MBAM e verificare che siano installati tutti i prerequisiti di MBAM.

### Se si fa clic su collegamenti alla documentazione durante la configurazione, viene visualizzato un errore dell'applicazione dopo l'installazione

Quando si fa clic su un collegamento alla documentazione durante l'installazione e quindi si chiude il programma di installazione facendo clic su **Annulla** o **fine** dopo il completamento della configurazione, viene visualizzato un messaggio di errore dell'applicazione.. Il problema è causato da un errore di violazione di Access nell'utilità di pianificazione di Windows.

**Soluzione alternativa:** Nessuno. Puoi ignorare questo errore.

### Errore di installazione di MBAM non rimuove i nuovi database

Se la configurazione di MBAM non riesce, la configurazione potrebbe non rimuovere i database appena creati. Ciò può causare errori durante le installazioni successive.

**Soluzione alternativa:** Scegliere un nome diverso per l'istanza del database durante l'installazione successiva.

### La configurazione di MBAM non riconosce i certificati cluster di bilanciamento del carico di rete validi

Durante l'installazione di MBAM Administration e Monitoring Server, con l'opzione di crittografia della rete selezionata, il certificato del cluster non viene riconosciuto come certificato valido. Viene riconosciuta come valida quando il certificato per la comunicazione con il database è installato, ma viene rifiutato per la comunicazione tramite il cluster di bilanciamento del carico.

**Soluzione alternativa:** Verificare che l'elenco di revoche di certificati associato al certificato sia accessibile oppure utilizzare un certificato che non richiede la convalida tramite il CRL.

## Informazioni sul copyright delle note sulla versione


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società. Tutti gli altri marchi sono proprietà dei rispettivi proprietari.



## Argomenti correlati


[Informazioni su MBAM 1.0](about-mbam-10.md)

 

 





