---
title: Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V
description: Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817935"
---
# Come configurare il supporto per il mirroring di Microsoft SQL Server per App-V


È possibile usare la procedura seguente per configurare l'ambiente Microsoft Application Virtualization (App-V) in modo da usare il mirroring del database di Microsoft SQL Server. La configurazione del mirroring del database può essere utile per scenari di failover e ripristino di emergenza. App-V 4,5 SP2 supporta tutte le modalità di mirroring del database attualmente disponibili per Microsoft SQL Server 2005 e SQL Server 2008.

**Nota**  
Questa procedura viene scritta per gli amministratori che hanno familiarità con l'impostazione e la configurazione dei database di SQL Server e del mirroring del database con Microsoft SQL Server e quindi copre solo le impostazioni di configurazione specifiche univoche per App-V.



**Per configurare l'ambiente App-V in modo da usare il mirroring del database di Microsoft SQL Server**

1.  Configurare il mirroring del database di SQL Server del database App-V seguendo le normali procedure aziendali per il mirroring del database. Usare i collegamenti seguenti per informazioni generali sull'implementazione del mirroring del database di Microsoft SQL Server:

    -   **Microsoft SQL 2005**—[configurazione del mirroring del database](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)

    -   **Microsoft SQL 2008**—[configurazione del mirroring del database](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)

    Inoltre, è possibile trovare informazioni sulle procedure consigliate nelle procedure consigliate per il [mirroring del database e le considerazioni sulle prestazioni](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .

2.  Dopo aver configurato il mirroring, verificare che il database App-V indichi uno stato **(Principal, synchronized)** e che il database con mirroring visualizzi lo stato **(mirror, synchronized/Restoring)**. Risolvere i problemi di mirroring prima di procedere con il passaggio successivo. Per altre informazioni sul monitoraggio dello stato, vedere [monitoraggio dello stato del mirroring](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .

3.  Nel computer SQL Server che ospita lo specchio del database di App-v creare l'account di accesso di SQL Server per il servizio di rete dell'app-v Management Server usando il nome del dominio di account ** &lt; &gt; \\ &lt; ManagementServerHostName &gt; $ **.

4.  Installare Microsoft SQL Server Native client in App-V Management Server e nel computer in cui è in uso l'App-V Management Web Service se installato in un altro computer. Se si prevede di connettere altri server di gestione di App-V al database SQL con mirroring per il bilanciamento del carico, è necessario installare anche Microsoft SQL Server Native client in tali computer. È possibile scaricare Microsoft SQL Server Native Client dalla pagina [Microsoft SQL server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) nell'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=187479) .

5.  Selezionare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** e verificare che contenga solo il nome host di SQL Server. Se include un nome di istanza, ad esempio *serverhostname\\instancename*, il nome dell'istanza deve essere rimosso.

    **Importante**  
    App-V Management Server usa la libreria di rete TCP/IP per comunicare con il server SQL quando è abilitato il mirroring del database e quindi non è possibile usare i nomi di istanza. I numeri di porta devono essere specificati nelle chiavi del registro di sistema.



6.  Selezionare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** e verificare che contenga il numero di porta usato per SQL nel computer SQL Server. Se si usa un'istanza denominata, il valore della chiave deve essere impostato sulla porta utilizzata per l'istanza denominata.

7.  Creare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** come REG \ _SZ e quindi impostare il valore sul nome host di SQL Server che ospita il mirror.

8.  Creare la chiave del registro di sistema **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** come DWORD e quindi impostare il valore sul numero di porta usato per SQL nel computer in cui è in uso SQL Server per ospitare il mirror. Se si usa un'istanza denominata per il mirror, il valore della chiave deve essere impostato sul numero di porta usato per l'istanza denominata.

9.  Nel computer che sta usando il servizio Web di gestione App-V configurare il file di testo UDL (Universal Data Link). Nella directory in cui è installato App-V fare doppio clic su **SftMgmt. UDL** e specificare i valori seguenti:

    -   Nella scheda **provider** selezionare il provider OLE DB **SQL Server Native Client 10,0**.

    -   Fare clic su **Avanti** per selezionare la scheda **connessione** . Nella casella **nome server** immettere il nome del server di SQL Server. Selezionare quindi **Usa sicurezza integrata di Windows NT**. Infine, fare clic sull'elenco **selezionare il database**e quindi selezionare il nome del database App-V.

    -   Fare clic sulla scheda **tutte** e quindi selezionare il partner per il **failover**delle voci. Fare clic su **Modifica valore**e quindi immettere il nome del server di SQL Server di failover. Fai clic su **OK**.

    **Importante**  
    Il sistema App-V usa l'autenticazione Kerberos. Di conseguenza, quando si configura il mirroring SQL in cui l'autenticazione Kerberos è abilitata in SQL Server e il servizio SQL Server viene eseguito in un account utente di dominio, è necessario configurare manualmente un nome SPN. Per altre informazioni, vedere "quando il servizio SQL usa un account basato su dominio" nell'articolo [configurazione dell'amministrazione di App-V per un ambiente distribuito](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .



10. Per verificare che il mirroring del database sia in corso correttamente, verificare il failover e verificare che l'App-V Management Server continui a funzionare correttamente.

    **Importante**  
    Procedere con attenzione e seguire le procedure aziendali standard per verificare che le operazioni di sistema non vengano interrotte in caso di errore.



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## Argomenti correlati


[Come eseguire attività amministrative in Application Virtualization Server Management Console](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









