---
title: Informazioni su MBAM 2.0 SP1
description: Informazioni su MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823555"
---
# Informazioni su MBAM 2.0 SP1

In questo argomento vengono illustrate le modifiche apportate a Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1). Per una descrizione generale di MBAM, vedere [Introduzione a mbam 2,0](getting-started-with-mbam-20-mbam-2.md).

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a>Novità di MBAM 2,0 SP1

Questa versione di MBAM offre le nuove caratteristiche e funzionalità seguenti.

### Supporto per Windows 8,1, Windows Server 2012 R2 e gestione configurazione di System Center 2012 R2

Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) aggiunge il supporto per Windows 8,1, Windows Server 2012 R2 e System Center 2012 R2 Configuration Manager.

### Supporto per Microsoft SQL Server 2008 R2 SP2

Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) aggiunge il supporto per Microsoft SQL Server 2008 R2 SP2. Se si esegue Microsoft System Center Configuration Manager 2007 R2, è necessario usare Microsoft SQL Server 2008 R2 o versioni successive.

### Rollup feedback dei clienti

MBAM 2,0 SP1 include un rollup di correzioni per risolvere i problemi che sono stati trovati dopo la versione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,0. Come parte di queste modifiche, il campo nome computer viene ora visualizzato nei report di conformità del computer e della conformità di BitLocker per i dettagli dell'organizzazione durante l'esecuzione di MBAM con Microsoft System Center Configuration Manager 2007.

### L'eccezione del firewall deve essere impostata sulle porte per il portale self-service e il sito Web di amministrazione e monitoraggio

Quando si configura il portale self-service e il sito Web di amministrazione e monitoraggio, è necessario impostare un'eccezione del firewall per consentire la comunicazione tramite le porte specificate. In precedenza, l'installazione di MBAM server ha aperto le porte automaticamente in Windows Firewall.

### La posizione dei report di MBAM è cambiata in Configuration Manager

I report di MBAM per la topologia integrata di Configuration Manager sono ora disponibili in sottocartelle all'interno del nodo MBAM. I nomi delle sottocartelle rappresentano la lingua dei report all'interno della sottocartella.

### Possibilità di installare MBAM in un server del sito principale quando si installa MBAM con Configuration Manager

È possibile installare MBAM in un server del sito principale o in un server del sito di amministrazione centrale quando si installa MBAM con la topologia integrata di Configuration Manager. In precedenza, era necessario installare MBAM in un server del sito di amministrazione centrale.

**Importante**  
Il server in cui si installa MBAM deve essere il server di livello superiore della gerarchia.



L'installazione di MBAM funziona in modo diverso per Microsoft System Center Configuration Manager 2007 e Microsoft System Center 2012 Configuration Manager come segue:

-   **Configuration manager 2007** : se si installa mbam in un server del sito principale che fa parte di una gerarchia di Configuration Manager più grande e dispone di un server padre del sito centrale, mbam risolve il server padre del sito centrale ed esegue tutte le azioni di installazione in tale server padre. Le azioni di installazione includono il controllo dei prerequisiti e l'installazione di oggetti e report di Configuration Manager. Ad esempio, se si installa MBAM in un server del sito principale che è un elemento figlio di un server padre del sito centrale, MBAM installa tutti gli oggetti e i report di Configuration Manager nel server padre. Se si installa MBAM nel server padre, MBAM esegue tutte le operazioni di installazione in tale server padre.

-   **System Center 2012 Configuration Manager** : se si installa mbam in un server del sito principale o in un server di amministrazione centrale, mbam esegue tutte le operazioni di installazione nel server del sito.

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> La console di Configuration Manager deve essere installata nel computer in cui si installa il server MBAM

Quando si installa MBAM con la topologia integrata di Configuration Manager, è necessario installare la console di Configuration Manager nello stesso computer in cui verrà installato MBAM. Se si usa l'architettura consigliata, descritta in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), è necessario installare Mbam nel server del sito primario di Configuration Manager.

### Nuovi parametri della riga di comando della configurazione per la topologia integrata di Configuration Manager

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parametro della riga di comando</th>
<th align="left">Descrizione</th>
<th align="left">Esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CM_SSRS_REMOTE_SERVER_NAME</p></td>
<td align="left"><p>Consente di installare i report di Configuration Manager in un server SQL Server Reporting Services (SSRS) remoto che fa parte dello stesso sito di Configuration Manager in cui è installato MBAM. Puoi impostare il valore sul nome di dominio completo del server dei ruoli del punto di SSRS remoto.</p></td>
<td align="left"><p>MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</p></td>
</tr>
<tr class="even">
<td align="left"><p>CM_REPORTS_ONLY</p></td>
<td align="left"><p>Consente di installare solo i report di Configuration Manager, senza altri oggetti di Configuration Manager, ad esempio la linea di base, la raccolta e gli elementi di configurazione.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Devi combinare questo parametro con il parametro CM_REPORTS_COLLECTION_ID.</p>
</div>
<div>

</div>
<p>Valori di parametro validi:</p>
<ul>
<li><p>True</p></li>
<li><p>False</p></li>
</ul>
<p>Puoi combinare questo parametro con il parametro CM_SSRS_REMOTE_SERVER_NAME se vuoi installare i report solo su un server del ruolo del punto di SSRS remoto.</p>
<p>Se non si imposta il parametro o se lo si imposta su false, MBAM setup installa tutti gli oggetti di Configuration Manager, inclusi i report.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CM_REPORTS_COLLECTION_ID</p></td>
<td align="left"><p>ID della raccolta esistente che identifica la raccolta per cui verranno visualizzati i dati di conformità per la creazione di report. Puoi specificare qualsiasi ID raccolta. Non è necessario usare l'ID della raccolta "MBAM supported Computers".</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
</tbody>
</table>



### Possibilità di attivare o disattivare il testo dell'avviso del portale self-service

MBAM 2,0 SP1 consente di disattivare il testo dell'avviso nel portale self-service. In precedenza, il testo dell'avviso viene visualizzato per impostazione predefinita e non è stato possibile disattivarlo.

**Per disattivare il testo dell'avviso**

1.  Nel server in cui è stato installato il portale self-service aprire Internet Information Services (IIS) e individuare i **siti di &gt; amministrazione e monitoraggio &gt; &gt; delle impostazioni delle applicazioni di Microsoft BitLocker selfservice**.

2.  Nella colonna **nome** selezionare **DisplayNotice**e impostare il valore su **false**.

### Possibilità di localizzare l'istruzione HelpdeskText che punta gli utenti a più informazioni sul portale self-service

Puoi configurare una versione localizzata dell'istruzione Self-Service Portal "HelpdeskText", che indica agli utenti finali come ottenere assistenza aggiuntiva quando usano il portale self-service. Se si configura il testo localizzato per l'istruzione, come descritto nelle istruzioni seguenti, MBAM visualizzerà la versione localizzata. Se MBAM non trova la versione localizzata, Visualizza il valore che si trova nel parametro **HelpdeskText** .

**Per visualizzare una versione localizzata dell'istruzione HelpdeskText**

1.  Nel server in cui è stato installato il portale self-service aprire IIS e individuare ** &gt; &gt; &gt; le impostazioni dell'applicazione di amministrazione e monitoraggio di selfservice di Microsoft BitLocker**.

2.  Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .

3.  Nel campo **nome** Digitare **HelpdeskText**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per il testo. Ad esempio, per creare un'istruzione HelpdeskText localizzata in spagnolo, devi assegnare un nome al parametro HelpdeskText \ _es-es. Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Nel campo **valore** Digitare il testo localizzato che si vuole visualizzare per gli utenti finali.

### Possibilità di localizzare il portale self-service HelpdeskURL

È possibile configurare una versione localizzata del portale self-service HelpdeskURL per la visualizzazione agli utenti finali per impostazione predefinita. Se si crea una versione localizzata, come descritto nelle istruzioni seguenti, MBAM trova e visualizza la versione localizzata. Se MBAM non trova una versione localizzata, Visualizza l'URL configurato per il parametro HelpDeskURL.

**Per visualizzare un HelpdeskURL localizzato**

1.  Nel server in cui è stato installato il portale self-service aprire IIS e individuare ** &gt; &gt; &gt; le impostazioni dell'applicazione di amministrazione e monitoraggio di selfservice di Microsoft BitLocker**.

2.  Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .

3.  Nel campo **nome** Digitare **HelpdeskURL**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per l'URL. Ad esempio, per creare un HelpdeskURL localizzato in spagnolo, devi assegnare un nome al parametro HelpdeskURL \ _es-es. Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Nel campo **valore** Digitare il HelpdeskURL localizzato che si vuole visualizzare per gli utenti finali.

### Possibilità di localizzare il testo dell'avviso del portale self-service

È possibile configurare il testo dell'avviso localizzato per la visualizzazione agli utenti finali per impostazione predefinita nel portale self-service. Il file notice.txt, che Visualizza il testo dell'avviso, si trova nella directory radice seguente:

&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self

Per visualizzare il testo dell'avviso localizzato, è possibile creare un file notice.txt localizzato e salvarlo in una specifica cartella della lingua nella directory seguente:

&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self

MBAM Visualizza il testo dell'avviso in base alle regole seguenti:

-   Se crei un file notice.txt localizzato nella cartella della lingua appropriata, MBAM visualizzerà il testo dell'avviso localizzato.

-   Se MBAM non trova una versione localizzata del file notice.txt, Visualizza il testo nel file notice.txt predefinito.

-   Se MBAM non trova un file di notice.txt predefinito, Visualizza il testo predefinito nel portale self-service.

**Nota**  
Se il browser di un utente finale è impostato su una lingua che non ha una sottocartella o notice.txt di lingua corrispondente, viene visualizzato il testo presente nel file notice.txt nella directory radice seguente:

&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self



**Per creare un file notice.txt localizzato**

1.  Nel server in cui è stato installato il portale self-service creare una &lt; cartella della *lingua* &gt; nella directory seguente, dove &lt; *lingua* &gt; rappresenta il nome della lingua localizzata:

    &lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self

    **Nota**  
    Alcune cartelle di lingua esistono già, quindi potrebbe non essere necessario crearne una. Se è necessario creare una cartella della lingua, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) per un elenco dei nomi validi che è possibile usare per la cartella della &lt; *lingua* &gt; .



2.  Creare un file di notice.txt contenente il testo dell'avviso localizzato.

3.  Salvare il file notice.txt nella cartella della &lt; *lingua* &gt; . Per creare un file di notice.txt localizzato in spagnolo, ad esempio, è necessario salvare il file notice.txt localizzato nella cartella seguente:

    &lt;Directory di installazione *di mbam self-service* &gt; Website\\es-es servizio \\Self

## Aggiornamento a MBAM 2,0 SP1


È possibile eseguire l'aggiornamento a MBAM 2,0 SP1 da qualsiasi versione precedente di MBAM.

### Aggiornamento dell'infrastruttura MBAM

È possibile aggiornare l'infrastruttura del server MBAM per MBAM 2,0 SP1 come segue:

**Sostituzione del server sul posto manuale**: è necessario disinstallare manualmente l'infrastruttura di mbam server esistente e quindi installare l'infrastruttura del server MBAM 2,0 SP1. Non è necessario rimuovere i database per eseguire l'aggiornamento. Devi invece selezionare i database esistenti, che la versione precedente di MBAM ha creato. L'installazione di aggiornamento di MBAM 2,0 SP1 esegue quindi la migrazione dei database esistenti in MBAM 2,0 SP1.

**Aggiornamento client distribuito**: se si usa la topologia di mbam autonoma, è possibile aggiornare gradualmente i client mbam dopo l'installazione dell'infrastruttura del Server MBAM 2,0 SP1.

Dopo aver aggiornato l'infrastruttura di MBAM server, i client MBAM 1,0 o 2,0 verranno segnalati al server MBAM 2,0 SP1 con successo e memorizzerà i dati di ripristino, ma la conformità sarà basata sui criteri disponibili per la versione client di MBAM attualmente installata. Per abilitare la creazione di report con i criteri di MBAM 2,0 SP1, è necessario aggiornare i computer client a MBAM 2,0 SP1. È possibile aggiornare i computer client al client MBAM 2,0 SP1 senza disinstallare il client precedente e il client inizierà ad applicarsi e a segnalare, in base ai criteri di MBAM 2,0 SP1.

Per altre informazioni sull'aggiornamento dei server MBAM, vedere [aggiornamento dalle versioni precedenti di mbam](upgrading-from-previous-versions-of-mbam.md).

### Aggiornamento del client MBAM per MBAM 2,0 SP1

Per aggiornare i computer degli utenti finali al client MBAM 2,0 SP1, eseguire **MbamClientSetup.exe** in ogni computer client. Il programma di installazione aggiorna automaticamente il client al client MBAM 2,0 SP1. Dopo l'installazione, i computer client non devono essere riavviati e il client MBAM 2,0 SP1 inizia ad applicarsi e a segnalare i criteri di MBAM 2,0 SP1.

Se si usa MBAM con Configuration Manager, è necessario aggiornare i computer client MBAM per MBAM 2,0 SP1.

Per altre informazioni sull'aggiornamento dei computer client MBAM, vedere [aggiornamento dalle versioni precedenti di mbam](upgrading-from-previous-versions-of-mbam.md).

## Installazione o aggiornamento di MBAM 2,0 SP1 con Configuration Manager


Questa sezione descrive i requisiti durante l'installazione di MBAM 2,0 SP1 come nuova installazione o come aggiornamento a un'installazione precedente di MBAM 2,0 SP1.

### File necessari per l'installazione di MBAM 2,0 SP1 se si usa MBAM con Configuration Manager

Se si sta installando MBAM per la prima volta e si usa MBAM 2,0 SP1 con System Center Configuration Manager, è necessario creare o modificare i file MOF per consentire a MBAM di funzionare correttamente con Configuration Manager.

-   **file MOF di Configuration**

    -   Se si usa Configuration Manager 2007, è necessario modificare il file Configuration. mof completando il passaggio 3 dall'elemento **aggiornare il file Configuration. mof se si esegue l'aggiornamento a mbam 2,0 SP1 e si usa mbam con Configuration Manager 2007**, che segue questo elemento.

    -   Se si usa System Center 2012 Configuration Manager, modificare il file Configuration. mof seguendo le istruzioni in [modificare il file Configuration. mof](edit-the-configurationmof-file.md).

-   **SMS \ _def file MOF** : seguire le istruzioni in [creare o modificare il file SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).

### Aggiornare il file Configuration. mof se si esegue l'aggiornamento a MBAM 2,0 SP1 e si usa MBAM con Configuration Manager 2007

Se si esegue l'aggiornamento a MBAM 2,0 SP1 e si usa MBAM con Configuration Manager 2007, è necessario aggiornare il file Configuration. mof per verificare che MBAM 2,0 SP1 funzioni correttamente.

**Per aggiornare il file Configuration. mof:**

1.  Nel server Configuration Manager passare al percorso del file Configuration. mof:

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    In un'installazione predefinita, il percorso di installazione è%systemdrive%\\Program Files (x86) \\Microsoft Configuration Manager.

2.  Esaminare il blocco di codice aggiunto al file Configuration. MOF ed eliminarlo. Il blocco di codice sarà simile a quello mostrato nel passaggio seguente.

3.  Copiare il blocco di codice seguente e quindi accodarlo al file Configuration. mof per aggiungere al file le classi di MBAM necessarie seguenti:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### Traduzione di MBAM 2,0 SP1

MBAM 2,0 SP1 è ora disponibile nelle lingue seguenti:

-   Inglese (Stati Uniti) en-US
-   Francese (Francia) fr-FR
-   Italiano (Italia) it-IT
-   Tedesco (Germania) de-DE
-   Spagnolo, ordinamento internazionale (Spagna) es-ES
-   Coreano (Corea) ko-KR
-   Giapponese (Giappone) ja-JP
-   Portoghese (Brasile) PT-BR
-   Russo (Russia) ru-RU
-   Zh-TW tradizionale cinese
-   Zh-CN semplificato in cinese

## Come ottenere le tecnologie MDOP

MBAM 2,0 SP1 fa parte di Microsoft Desktop Optimization Pack (MDOP). MDOP fa parte di Microsoft Software Assurance. Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Argomenti correlati

[Note sulla versione di MBAM 2.0 SP1](release-notes-for-mbam-20-sp1.md)









