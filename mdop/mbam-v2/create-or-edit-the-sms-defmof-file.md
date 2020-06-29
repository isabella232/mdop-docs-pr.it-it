---
title: Creare o modificare il file SMS \ _def. mof
description: Creare o modificare il file SMS \ _def. mof
author: dansimp
ms.assetid: d1747e43-484e-4031-a63b-6342fe588aa2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/04/2017
ms.openlocfilehash: 15f1d1a1c19cb9b19b7d83534e035d5410720ce9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823515"
---
# <span data-ttu-id="ce25e-103">Creare o modificare il file SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="ce25e-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="ce25e-104">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario creare o modificare il file SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="ce25e-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="ce25e-105">Se si usa il ConfigurationManager di SystemCenter2012, è necessario creare il file.</span><span class="sxs-lookup"><span data-stu-id="ce25e-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

<span data-ttu-id="ce25e-106">In Configuration Manager 2007 il file esiste già, quindi è necessario modificarlo.</span><span class="sxs-lookup"><span data-stu-id="ce25e-106">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> <span data-ttu-id="ce25e-107">Non **sovrascrivere il file esistente**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-107">**Do not overwrite the existing file**.</span></span>

<span data-ttu-id="ce25e-108">Nelle sezioni seguenti completare le istruzioni che corrispondono alla versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="ce25e-108">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="ce25e-109">Per creare il file SMS \ _def. mof per SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="ce25e-109">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="ce25e-110">Nel server Configuration Manager individuare il percorso in cui è necessario creare il file SMS \ _def. mof, ad esempio il desktop.</span><span class="sxs-lookup"><span data-stu-id="ce25e-110">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="ce25e-111">Creare un file di testo denominato **SMS \ _def. mof** e copiare il codice seguente per popolare il file con le classi di mbam _def. mof seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce25e-111">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

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

        //MBAM agent fields
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

3.  <span data-ttu-id="ce25e-112">Importare il file **SMS \ _def. mof** eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ce25e-112">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="ce25e-113">Aprire la **console di SystemCenter2012 ConfigurationManager** e selezionare la scheda **Amministrazione** .</span><span class="sxs-lookup"><span data-stu-id="ce25e-113">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="ce25e-114">Nella scheda **Amministrazione** selezionare **Impostazioni client**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-114">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="ce25e-115">Fare clic con il pulsante destro del mouse su **Impostazioni client predefinite**e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-115">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="ce25e-116">Nella finestra **impostazioni predefinite** selezionare **inventario hardware**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-116">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="ce25e-117">Fare clic su **Imposta classi**e quindi su **Importa**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-117">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="ce25e-118">Nel browser che si apre selezionare il file con **estensione MOF** e quindi fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-118">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="ce25e-119">Verrà visualizzata la finestra **Importa Riepilogo** .</span><span class="sxs-lookup"><span data-stu-id="ce25e-119">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="ce25e-120">Nella finestra **Importa Riepilogo** verificare che sia selezionata l'opzione per importare sia le classi di inventario hardware che le impostazioni della classe, quindi fare clic su **Importa**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-120">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="ce25e-121">Nella finestra delle **classi di inventario hardware** e nella finestra **impostazioni predefinite** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-121">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="ce25e-122">Abilitare la classe **Win32 \ _Tpm** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ce25e-122">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="ce25e-123">Aprire la **console di SystemCenter2012 ConfigurationManager** e selezionare la scheda **Amministrazione** .</span><span class="sxs-lookup"><span data-stu-id="ce25e-123">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="ce25e-124">Nella scheda **Amministrazione** selezionare **Impostazioni client**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-124">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="ce25e-125">Fare clic con il pulsante destro del mouse su **Impostazioni client predefinite**e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-125">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="ce25e-126">Nella finestra **impostazioni predefinite** selezionare **inventario hardware**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-126">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="ce25e-127">Fare clic su **Imposta classi**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-127">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="ce25e-128">Nella finestra principale scorrere verso il basso e quindi selezionare la classe **TPM (Win32 \ _Tpm)** .</span><span class="sxs-lookup"><span data-stu-id="ce25e-128">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="ce25e-129">In **TPM**verificare che sia selezionata la proprietà **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="ce25e-129">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="ce25e-130">Nella finestra delle **classi di inventario hardware** e nella finestra **impostazioni predefinite** fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce25e-130">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="ce25e-131">Per modificare il file SMS \ _def. mof per Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="ce25e-131">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="ce25e-132">Nel server Configuration Manager passare al percorso del file **SMS \ _def. mof** :</span><span class="sxs-lookup"><span data-stu-id="ce25e-132">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="ce25e-133">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="ce25e-133">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="ce25e-134">In un'installazione predefinita, il percorso di installazione è% SystemDrive% cartella Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ce25e-134">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="ce25e-135">Copiare il codice seguente e quindi accodarlo al file **SMS \ _def. mof** per aggiungere al file le seguenti classi di mbam necessarie:</span><span class="sxs-lookup"><span data-stu-id="ce25e-135">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

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

3.  <span data-ttu-id="ce25e-136">Modificare la classe **Win32 \ _Tpm** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ce25e-136">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="ce25e-137">Impostare **SMS \ _REPORT** su **true** negli attributi della classe.</span><span class="sxs-lookup"><span data-stu-id="ce25e-137">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="ce25e-138">Imposta **SMS \ _REPORT** su **true** nell'attributo della proprietà **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="ce25e-138">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

## <span data-ttu-id="ce25e-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce25e-139">Related topics</span></span>


[<span data-ttu-id="ce25e-140">Come creare o modificare i file MOF</span><span class="sxs-lookup"><span data-stu-id="ce25e-140">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

[<span data-ttu-id="ce25e-141">Distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ce25e-141">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





