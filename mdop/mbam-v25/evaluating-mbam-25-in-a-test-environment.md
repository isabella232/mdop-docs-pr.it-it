---
title: Valutazione di MBAM 2.5 in un ambiente di test
description: Valutazione di MBAM 2.5 in un ambiente di test
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823155"
---
# Valutazione di MBAM 2.5 in un ambiente di test


Questo argomento descrive come configurare un ambiente di test per valutare l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) 2,5 nella topologia di integrazione autonoma o System Center Configuration Manager.

## Valutazione di MBAM 2,5 tramite la topologia autonoma


Per valutare MBAM usando la topologia autonoma, usare le informazioni nelle tabelle seguenti per installare il software MBAM server e quindi configurare le caratteristiche del server MBAM nell'ambiente di test.

**Per valutare MBAM 2,5 usando la topologia autonoma**

1. Prima di installare MBAM, eseguire le operazioni seguenti:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Attività</th>
   <th align="left">Dove ottenere le istruzioni</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verificare di avere installato tutto il software prerequisito.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Verificare l'hardware, la RAM e altre specifiche richieste.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet per configurare MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installare il software MBAM server e quindi configurare le caratteristiche desiderate.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Attività</th>
   <th align="left">Dove ottenere le istruzioni</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installare il software MBAM server su ogni server in cui si vuole configurare una caratteristica del server MBAM.</p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurare il database di conformità e controllo e il database di ripristino.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Come configurare i database di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurare la caratteristica report.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Come configurare i report di MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurare le applicazioni Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Come configurare le applicazioni Web di MBAM 2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. In un computer client eseguire le operazioni seguenti:

   1.  Installare il client MBAM in un computer client.

   2.  Applicare gli oggetti Criteri di gruppo di MBAM al computer.

   3.  Impostare le chiavi del registro di sistema seguenti per imporre al client MBAM di riattivarsi più rapidamente e a intervalli regolari:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Nota**  
       Dato che questi tasti riattivano il client MBAM ogni minuto, ti consigliamo di usare queste impostazioni della chiave del registro di sistema solo in un ambiente di test.



   4.  Riavviare il **servizio client di gestione di BitLocker**.

## Valutazione di MBAM 2,5 tramite la topologia di integrazione di System Center 2012 Configuration Manager


Per valutare MBAM usando la topologia di integrazione di Configuration Manager, usare le informazioni nelle tabelle seguenti per installare il software di MBAM server e quindi configurare le caratteristiche del server MBAM nell'ambiente di test. Dopo l'installazione del client MBAM su un computer client, verranno completate le procedure aggiuntive per forzare il client MBAM a segnalare lo stato del computer a MBAM più rapidamente.

**Per valutare MBAM 2,5 usando la topologia di integrazione di System Center 2012 Configuration Manager**

1. Prima di installare MBAM, rivedere il software prerequisito e la configurazione supportata.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Attività</th>
   <th align="left">Dove ottenere le istruzioni</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verificare di avere installato tutto il software prerequisito.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Verificare l'hardware, la RAM e altre specifiche richieste.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Esaminare i prerequisiti per l'uso di Windows PowerShell se si prevede di usare i cmdlet per configurare MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Creare o modificare i file con estensione MOF.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Modificare il file Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Creare o modificare il file Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installare il software MBAM server e quindi configurare le caratteristiche desiderate.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Attività</th>
   <th align="left">Dove ottenere le istruzioni</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installare il software MBAM server su ogni server in cui si vuole configurare una caratteristica del server MBAM.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>È possibile installare i database in un computer SQL Server remoto tramite Windows PowerShell o un pacchetto di applicazione a livello di dati esportato (DAC). Per altre informazioni sui pacchetti DAC, vedere <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applicazioni a livello di dati </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurare il database di conformità e controllo e il database di ripristino.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Come configurare i database di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurare la caratteristica report.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Come configurare i report di MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurare le applicazioni Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Come configurare le applicazioni Web di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurare System Center Configuration Manager per installare gli oggetti di Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager</a></p></td>
   </tr>
   </tbody>
   </table>



3. In un computer client eseguire le operazioni seguenti:

   1.  Installare il client MBAM e il client Configuration Manager in un computer client.

   2.  Applicare gli oggetti Criteri di gruppo di MBAM al computer.

   3.  Impostare le chiavi del registro di sistema seguenti per imporre al client MBAM di riattivarsi più rapidamente e a intervalli regolari:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Nota**  
       Dato che questi tasti riattivano il client MBAM ogni minuto, ti consigliamo di usare queste impostazioni della chiave del registro di sistema solo in un ambiente di test.



   4.  Riavviare il **servizio client di gestione di BitLocker**.

   5.  Nel pannello di controllo aprire **Gestione configurazione**e quindi fare clic sulla scheda **azioni** .

   6.  Selezionare **ciclo di inventario hardware**e quindi fare clic su **Esegui ora**. Questo passaggio esegue l'inventario hardware usando le nuove classi importate nei file MOF e quindi invia i dati al Server Configuration Manager.

   7.  Selezionare **recupero criteri computer & ciclo di valutazione**e quindi fare clic su **Esegui ora** per applicare gli oggetti Criteri di gruppo rilevanti per il computer client.



4. Nella console di Configuration Manager eseguire le operazioni seguenti:

   1.  Nel riquadro di spostamento fare clic con il pulsante destro del mouse su **computer supportati mbam**, scegliere **Aggiorna appartenenza**e quindi fare clic su **Sì** per forzare il computer client a segnalare immediatamente l'appartenenza.

   2.  Nel riquadro di spostamento fare clic su **mbam computer supportati** per verificare che il computer client venga visualizzato nella raccolta.

5. Nel pannello di controllo del computer client riaprire **Configuration Manager** ed eseguire le operazioni seguenti:

   1.  Fare clic sulla scheda **azioni** e quindi rieseguire il **recupero dei criteri del computer & ciclo di valutazione**.

   2.  Fare clic sulla scheda **configurazioni** , selezionare la previsione di BitLocker e quindi fare clic su **valuta**.

6. Nella console di Configuration Manager verificare che il computer client venga visualizzato nel report conformità aziendale: come indicato di seguito:

   1.  Nel riquadro di spostamento selezionare l'area di lavoro **monitoraggio** .

   2.  Nell'albero della console espandere **Panoramica** &gt; **report** &gt; **Reports** &gt; **mbam**.

   3.  Selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro risultati.

## Valutazione di MBAM 2,5 tramite la topologia di integrazione di System Center Configuration Manager 2007


Per valutare MBAM usando la topologia di integrazione di Configuration Manager, seguire la stessa procedura per installare e configurare MBAM nell'ambiente di test durante l'uso in un ambiente di produzione. Dopo l'installazione del client MBAM in un computer client, completare i passaggi aggiuntivi in questo argomento per consentire al client MBAM di iniziare a segnalare lo stato del computer a MBAM più rapidamente.

**Per valutare MBAM usando la topologia di integrazione di Configuration Manager 2007**

1. Prima di installare MBAM, eseguire le operazioni seguenti:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Attività</th>
   <th align="left">Dove ottenere le istruzioni</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Verificare di avere installato tutto il software prerequisito.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Verificare l'hardware, la RAM e altre specifiche richieste.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurazioni supportate di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Creare o modificare i file con estensione MOF.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Modificare il file Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Creare o modificare il file Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installare il software MBAM server e quindi configurare le caratteristiche desiderate.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Attività</th>
   <th align="left">Dove ottenere le istruzioni</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installare il software MBAM server su ogni server in cui si vuole configurare una caratteristica del server MBAM.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>È possibile installare i database in un computer SQL Server remoto tramite Windows PowerShell o un pacchetto di applicazione a livello di dati esportato (DAC). Per altre informazioni sui pacchetti DAC, vedere <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applicazioni a livello di dati </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installazione del software per il server di MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurare il database di conformità e controllo e il database di ripristino.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Come configurare i database di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurare la caratteristica report.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Come configurare i report di MBAM 2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurare le applicazioni Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Come configurare le applicazioni Web di MBAM 2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurare System Center Configuration Manager per installare gli oggetti di Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Come configurare l'integrazione di MBAM 2.5 con System Center Configuration Manager</a></p></td>
   </tr>
   </tbody>
   </table>



3. In un computer client eseguire le operazioni seguenti:

   1.  Installare il client MBAM in un computer client.

   2.  Applicare gli oggetti Criteri di gruppo di MBAM al computer.

   3.  Impostare le chiavi del registro di sistema seguenti per imporre al client MBAM di riattivarsi più rapidamente e a intervalli più rapidi:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Nota**  
       Dato che questi tasti riattivano il client MBAM ogni minuto, ti consigliamo di usare queste impostazioni della chiave del registro di sistema solo in un ambiente di valutazione.



   4.  Riavviare il **servizio client di gestione di BitLocker**.

   5.  Nel pannello di controllo aprire **Gestione configurazione**e quindi fare clic sulla scheda **azioni** .

   6.  Selezionare **recupero criteri computer & ciclo di valutazione**e quindi fare clic su **Esegui ora** per applicare gli oggetti Criteri di gruppo rilevanti per il computer client.

   7.  Selezionare **ciclo di inventario hardware**e quindi fare clic su **Esegui ora**. Questo passaggio esegue l'inventario hardware usando le nuove classi importate nei file MOF e quindi invia i dati al Server Configuration Manager.

4. Nella console di Configuration Manager eseguire le operazioni seguenti:

   1.  Nel riquadro di spostamento fare clic con il pulsante destro del mouse su **computer supportati mbam**, scegliere **Aggiorna appartenenza**e quindi fare clic su **Sì** per forzare il computer client a segnalare immediatamente l'appartenenza.

   2.  Nel riquadro di spostamento fare clic su **mbam computer supportati** per verificare che il computer client venga visualizzato nella raccolta.

5. Nel pannello di controllo del computer client riaprire **Configuration Manager** ed eseguire le operazioni seguenti:

   1.  Fare clic sulla scheda **azioni** e quindi rieseguire il **recupero dei criteri del computer & ciclo di valutazione**.

   2.  Fare clic sulla scheda **configurazioni** , selezionare la previsione di BitLocker e fare clic su **valuta**.

6. Nella console di Configuration Manager verificare che il computer client venga visualizzato nel report conformità aziendale, come indicato di seguito.

   1.  Nel riquadro di spostamento espandere **Gestione computer** &gt; **Reporting** &gt; **Services** &gt; ** &lt; server &gt; mbam**.

   2.  All'interno del nodo **mbam** selezionare la cartella che rappresenta la lingua in cui si vogliono visualizzare i report e quindi selezionare il report nel riquadro risultati.


## Argomenti correlati


[Attività iniziali di MBAM 2.5](getting-started-with-mbam-25.md)


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





