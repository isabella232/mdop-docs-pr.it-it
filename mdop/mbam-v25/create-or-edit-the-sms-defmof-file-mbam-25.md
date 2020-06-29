---
title: Creare o modificare il file SMS \ _def. mof
description: Creare o modificare il file SMS \ _def. mof
author: dansimp
ms.assetid: 0bc5e7d8-9747-4da6-a1b3-38d8f27ba121
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 272f597974e96efa0c742fecfe9488a4899fc695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823196"
---
# <span data-ttu-id="65a31-103">Creare o modificare il file SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="65a31-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="65a31-104">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario creare o modificare il file SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="65a31-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="65a31-105">Se si usa il ConfigurationManager di SystemCenter2012, è necessario creare il file.</span><span class="sxs-lookup"><span data-stu-id="65a31-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="65a31-106">Creare il file nel sito di primo livello.</span><span class="sxs-lookup"><span data-stu-id="65a31-106">Create the file on the top-tier site.</span></span> <span data-ttu-id="65a31-107">Le modifiche verranno replicate negli altri siti dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="65a31-107">The changes will be replicated to the other sites in your infrastructure.</span></span>

<span data-ttu-id="65a31-108">In Configuration Manager 2007 il file esiste già, quindi è necessario modificarlo.</span><span class="sxs-lookup"><span data-stu-id="65a31-108">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> **<span data-ttu-id="65a31-109">Non sovrascrivere il file esistente.</span><span class="sxs-lookup"><span data-stu-id="65a31-109">Do not overwrite the existing file.</span></span>**

<span data-ttu-id="65a31-110">Nelle sezioni seguenti completare le istruzioni che corrispondono alla versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="65a31-110">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="65a31-111">Per creare il file SMS \ _def. mof per SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="65a31-111">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="65a31-112">Nel server Configuration Manager individuare il percorso in cui è necessario creare il file SMS \ _def. mof, ad esempio il desktop.</span><span class="sxs-lookup"><span data-stu-id="65a31-112">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="65a31-113">Creare un file di testo denominato **SMS \ _def. mof** e copiare il codice seguente per popolare il file con le classi di mbam _def. mof seguenti:</span><span class="sxs-lookup"><span data-stu-id="65a31-113">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="65a31-114">Importare il file **SMS \ _def. mof** eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="65a31-114">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="65a31-115">Aprire la **console di SystemCenter2012 ConfigurationManager** e selezionare la scheda **Amministrazione** .</span><span class="sxs-lookup"><span data-stu-id="65a31-115">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="65a31-116">Nella scheda **Amministrazione** selezionare **Impostazioni client**.</span><span class="sxs-lookup"><span data-stu-id="65a31-116">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="65a31-117">Fare clic con il pulsante destro del mouse su **Impostazioni client predefinite**e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="65a31-117">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="65a31-118">Nella finestra **impostazioni predefinite** selezionare **inventario hardware**.</span><span class="sxs-lookup"><span data-stu-id="65a31-118">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="65a31-119">Fare clic su **Imposta classi**e quindi su **Importa**.</span><span class="sxs-lookup"><span data-stu-id="65a31-119">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="65a31-120">Nel browser che si apre selezionare il file con **estensione MOF** e quindi fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="65a31-120">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="65a31-121">Verrà visualizzata la finestra **Importa Riepilogo** .</span><span class="sxs-lookup"><span data-stu-id="65a31-121">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="65a31-122">Nella finestra **Importa Riepilogo** verificare che sia selezionata l'opzione per importare sia le classi di inventario hardware che le impostazioni della classe, quindi fare clic su **Importa**.</span><span class="sxs-lookup"><span data-stu-id="65a31-122">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="65a31-123">Nella finestra delle **classi di inventario hardware** e nella finestra **impostazioni predefinite** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="65a31-123">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="65a31-124">Abilitare la classe **Win32 \ _Tpm** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="65a31-124">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="65a31-125">Aprire la **console di SystemCenter2012 ConfigurationManager** e selezionare la scheda **Amministrazione** .</span><span class="sxs-lookup"><span data-stu-id="65a31-125">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="65a31-126">Nella scheda **Amministrazione** selezionare **Impostazioni client**.</span><span class="sxs-lookup"><span data-stu-id="65a31-126">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="65a31-127">Fare clic con il pulsante destro del mouse su **Impostazioni client predefinite**e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="65a31-127">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="65a31-128">Nella finestra **impostazioni predefinite** selezionare **inventario hardware**.</span><span class="sxs-lookup"><span data-stu-id="65a31-128">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="65a31-129">Fare clic su **Imposta classi**.</span><span class="sxs-lookup"><span data-stu-id="65a31-129">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="65a31-130">Nella finestra principale scorrere verso il basso e quindi selezionare la classe **TPM (Win32 \ _Tpm)** .</span><span class="sxs-lookup"><span data-stu-id="65a31-130">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="65a31-131">In **TPM**verificare che sia selezionata la proprietà **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="65a31-131">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="65a31-132">Nella finestra delle **classi di inventario hardware** e nella finestra **impostazioni predefinite** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="65a31-132">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="65a31-133">Per modificare il file SMS \ _def. mof per Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="65a31-133">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="65a31-134">Nel server Configuration Manager passare al percorso del file **SMS \ _def. mof** :</span><span class="sxs-lookup"><span data-stu-id="65a31-134">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="65a31-135">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="65a31-135">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="65a31-136">In un'installazione predefinita, il percorso di installazione è% SystemDrive% cartella Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="65a31-136">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="65a31-137">Copiare il codice seguente e quindi accodarlo al file **SMS \ _def. mof** per aggiungere al file le seguenti classi di mbam necessarie:</span><span class="sxs-lookup"><span data-stu-id="65a31-137">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=32|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=64|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy_64: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="65a31-138">Modificare la classe **Win32 \ _Tpm** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="65a31-138">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="65a31-139">Impostare **SMS \ _REPORT** su **true** negli attributi della classe.</span><span class="sxs-lookup"><span data-stu-id="65a31-139">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="65a31-140">Imposta **SMS \ _REPORT** su **true** nell'attributo della proprietà **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="65a31-140">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

    <span data-ttu-id="65a31-141">**Hai un suggerimento per mbam**?</span><span class="sxs-lookup"><span data-stu-id="65a31-141">**Got a suggestion for MBAM**?</span></span> <span data-ttu-id="65a31-142">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="65a31-142">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> <span data-ttu-id="65a31-143">**Hai un problema con mbam**?</span><span class="sxs-lookup"><span data-stu-id="65a31-143">**Got a MBAM issue**?</span></span> <span data-ttu-id="65a31-144">Usare il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="65a31-144">Use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="65a31-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65a31-145">Related topics</span></span>


[<span data-ttu-id="65a31-146">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="65a31-146">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[<span data-ttu-id="65a31-147">Modificare il file Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="65a31-147">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

[<span data-ttu-id="65a31-148">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="65a31-148">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## <span data-ttu-id="65a31-149">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="65a31-149">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="65a31-150">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="65a31-150">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="65a31-151">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="65a31-151">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




