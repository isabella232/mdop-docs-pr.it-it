---
title: Pianificazione della disponibilità elevata per MBAM 2.5
description: Pianificazione della disponibilità elevata per MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826945"
---
# Pianificazione della disponibilità elevata per MBAM 2.5


Microsoft BitLocker Administration and Monitoring (MBAM) può mantenere elevata la disponibilità con l'uso di una o più delle tecnologie seguenti, descritte nelle sezioni seguenti:

-   [Gruppi di disponibilità di SQL Server AlwaysOn](#bkmk-alwayson)

-   [Clustering di Microsoft SQL Server](#bkmk-sql-clustering)

-   [Bilanciamento del carico di rete IIS](#bkmk-load-balance)

-   [Mirroring del database in SQL Server](#bkmk-db-mirroring)

-   [Backup dei database di MBAM tramite il servizio Copia Shadow del volume (VSS)](#bkmk-vss)

Usare le informazioni nelle sezioni seguenti per comprendere le opzioni per la distribuzione di MBAM in una configurazione a disponibilità elevata.

## <a href="" id="bkmk-alwayson"></a>Supporto per i gruppi di disponibilità di SQL Server AlwaysOn


MBAM consente di configurare e gestire i gruppi di disponibilità per i database in Microsoft SQL Server. Un gruppo di disponibilità per MBAM supporta un ambiente di failover in cui il database di conformità e controllo e il database di ripristino non vengono più Uniti, invece che separatamente.

Un gruppo di disponibilità supporta un set di database primari di lettura/scrittura e uno-quattro set di database secondari corrispondenti. Facoltativamente, i database secondari possono essere resi disponibili per le autorizzazioni di sola lettura, alcune operazioni di backup o per entrambi.

Per informazioni su come configurare i gruppi di disponibilità, vedere [gruppi di disponibilità AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).

## <a href="" id="bkmk-sql-clustering"></a>Clustering di Microsoft SQL Server


È possibile eseguire il database di conformità e controllo di MBAM 2,5 e il database di ripristino nei computer che eseguono cluster di SQL Server.

## <a href="" id="bkmk-load-balance"></a>Bilanciamento del carico di rete IIS


È possibile usare il bilanciamento del carico di rete per configurare un ambiente altamente disponibile per i computer che eseguono il sito Web di amministrazione e monitoraggio (noto anche come Help desk), il portale self-service e i servizi Web distribuiti tramite Internet Information Services (IIS).

### Prerequisiti

Prima di configurare il bilanciamento del carico, verificare di avere soddisfatto i prerequisiti seguenti:

-   Un bilanciamento del carico deve essere disponibile. È possibile usare il bilanciamento del carico da Microsoft o da un'altra società. Per altre informazioni sulla tecnologia di bilanciamento del carico Microsoft, vedere [creare una Web farm con i server IIS](https://go.microsoft.com/fwlink/?LinkId=393326).

-   Almeno due server stanno usando IIS e hanno soddisfatto tutti i prerequisiti di MBAM per supportare le caratteristiche Web, tra cui ASP.NET MVC 4.

-   I database e i report MBAM sono in uso in un server.

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> Modifiche specifiche per MBAM necessarie per abilitare il bilanciamento del carico

Completare le attività seguenti:

1.  Registrare un nome dell'entità servizio (SPN) per il nome host virtuale nell'account di dominio in uso per i pool di applicazioni Web. Ad esempio, se il nome host virtuale è mbamvirtual.contoso.com e l'account di dominio usato per i pool di applicazioni Web è contoso\\mbamapppooluser, il comando seguente registra l'SPN in modo appropriato.

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  Configurare le caratteristiche Web di MBAM seguenti:

    -   In ogni server che ospiterà le caratteristiche Web di MBAM, USA lo stesso account di dominio per le credenziali amministrative del pool di applicazioni.

    -   Specificare un nome host che corrisponda al nome host virtuale (nome DNS) del cluster di bilanciamento del carico. Ad esempio, quando si installa MBAM in un server denominato "NLB1" con un nome host virtuale di **mbamvirtual.contoso.com**, assicurarsi che il nome host specificato nel cmdlet di Windows PowerShell sia **mbamvirtual.contoso.com**.

3.  Se si configurano i siti Web in una Web farm con un dispositivo di bilanciamento del carico, è necessario configurare i siti Web in modo da usare la stessa chiave del computer.

    Per altre informazioni, vedere le sezioni seguenti in [elemento machineKey (schema delle impostazioni di ASP.NET)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):

    -   Spiegazione della chiave del computer

    -   Considerazioni sulla distribuzione di Web farm

    Per istruzioni su come generare automaticamente una chiave, vedere [generare una chiave del computer (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).

Le informazioni sul bilanciamento del carico si applicano anche ai cluster di bilanciamento del carico di rete di IIS (NLB) in Windows Server 2012 o Windows Server2008R2. La funzionalità di bilanciamento del carico di rete di IIS in Windows Server 2012 è in genere uguale a quella di Windows Server2008R2. Tuttavia, alcuni dettagli delle attività sono diversi in Windows Server 2012. Per informazioni sulle nuove modalità di attività, vedere [attività di gestione comuni e spostamento in Windows server 2012 R2 Preview e Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).

## <a href="" id="bkmk-db-mirroring"></a>Mirroring del database in SQL Server


MBAM supporta l'uso di mirroring di SQL Server, in cui il database di conformità e controllo e il database di ripristino vengono speculati utilizzando due istanze di SQL Server per ogni database. Prima di implementare il mirroring, tenere presente che il mirroring viene gradualmente eliminato, a favore dei gruppi di disponibilità, descritti più indietro in questo argomento.

Per implementare il mirroring per MBAM, devi specificare le stringhe di connessione appropriate per la configurazione del database con mirroring usando il cmdlet di Windows PowerShell **Enable-MbamWebApplication** . Per altre informazioni sui cmdlet di Windows PowerShell per MBAM 2,5, vedere [configurazione delle funzionalità del server di mbam 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

### Esempi di implementazione del mirroring di SQL Server tramite Windows PowerShell

Gli esempi seguenti illustrano come implementare il mirroring di SQL Server usando i cmdlet di Windows PowerShell.

**Esempio 1**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**Esempio 2**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### Altre informazioni sul mirroring di SQL Server

I collegamenti seguenti includono ulteriori informazioni sulla configurazione del mirroring di SQL Server:

-   [Procedura: preparare un database mirror per il mirroring (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Stabilire una sessione di mirroring del database con l'autenticazione di Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a>Backup dei database di MBAM tramite il servizio Copia Shadow del volume (VSS)


MBAM offre un writer del servizio Copia Shadow del volume (VSS), denominato Microsoft BitLocker Administration and Management writer. Questo writer VSS semplifica il backup del database di conformità e di controllo e del database di ripristino.

Il writer VSS è registrato in tutti i server in cui si Abilita un'applicazione Web MBAM. MBAM VSS Writer dipende da SQL Server VSS Writer, registrato come parte dell'installazione di Microsoft SQL Server. Qualsiasi tecnologia di backup che usa writer VSS per eseguire il backup può individuare il writer di MBAM VSS.



## Argomenti correlati


[Pianificazione della distribuzione di MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




