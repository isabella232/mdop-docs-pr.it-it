---
title: Configurazione di un'immagine di Windows Virtual PC per MED-V
description: Configurazione di un'immagine di Windows Virtual PC per MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826816"
---
# Configurazione di un'immagine di Windows Virtual PC per MED-V


Dopo aver installato tutto ciò che si vuole includere nell'immagine di MED-V, è possibile configurare l'immagine per l'uso in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0. Gli argomenti di questa sezione includono indicazioni per la configurazione dell'immagine MED-V per eseguire la configurazione iniziale prima di creare il pacchetto dell'area di lavoro MED-V.

La configurazione per la prima volta prepara l'area di lavoro MED-V per un utente finale. Il processo crea una macchina virtuale dall'immagine confezionata nell'area di lavoro MED-V e quindi esegue la configurazione minima di Windows nella macchina virtuale. Questo include l'esecuzione di script di configurazione personalizzati e l'applicazione di completamento della configurazione per la prima volta, FtsCompletion.exe.

Seguire questa procedura per configurare l'immagine MED-V per l'esecuzione della configurazione per la prima volta:

1. Come opzione, è possibile compattare il disco rigido virtuale (VHD) per recuperare spazio vuoto e ridurre le dimensioni del disco rigido virtuale prima di continuare a configurare l'immagine di Windows Virtual PC. Per altre informazioni, vedere [compattazione del disco rigido virtuale MED-V](compacting-the-med-v-virtual-hard-disk.md).

2. Personalizzare il processo di configurazione della macchina virtuale.

3. Chiudere l'immagine MED-V usando Sysprep.

   **Personalizzazione del processo di configurazione della macchina virtuale**

4. Come parte della preparazione dell'immagine da usare con MED-V, è possibile configurare varie impostazioni nella macchina virtuale, ad esempio specificando le impostazioni per l'uso di Windows Update. Specificare tutte le impostazioni necessarie per la macchina virtuale prima di creare il pacchetto dell'area di lavoro MED-V.

5. Prima di creare il pacchetto dell'area di lavoro MED-V, è consigliabile disabilitare i punti di ripristino nella macchina virtuale per evitare che il disco differenze cresca in modo non associato. Per altre informazioni, vedere [come disattivare e attivare Ripristino configurazione di sistema in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

   **Nota**  
   È possibile configurare il file Sysprep. inf per disabilitare i punti di ripristino quando viene eseguita la configurazione per la prima volta. Per un esempio di impostazione di questa chiave GuiRunOnce, vedere il file Sysprep. inf di esempio più avanti in questa sezione.



6. Configurare il processo di configurazione per eseguire la configurazione minima anziché l'impostazione predefinita di Windows Welcome. È necessario eseguire lo strumento Sysprep usando l'opzione **-mini** oppure selezionare la casella di controllo **MiniSetup** nell'interfaccia utente grafica. Per altre informazioni, vedere [come sigillare l'immagine con Sysprep](#bkmk-seal).

   **Chiamata del file di completamento della configurazione per la prima volta**

   1.  Un eseguibile denominato FtsCompletion.exe è incluso nell'installazione dell'agente guest MED-V. Per impostazione predefinita, si trova nell'unità di sistema dell'immagine MED-V in **file di programma-virtualizzazione desktop Microsoft Enterprise**.

       **Importante**  
       Come passaggio finale nel processo di configurazione per la prima volta, è necessario eseguire questo programma eseguibile. L'utente per il quale viene chiamato il programma eseguibile deve essere membro del gruppo di amministratori locali dell'ospite.



   2.  Puoi decidere in che modo vuoi chiamare questo programma eseguibile, ad esempio tramite uno script distribuito con l'area di lavoro MED-V. Puoi chiamare questo eseguibile come ultima riga del file Sysprep. inf. Per un esempio di come chiamare questo programma eseguibile nel file Sysprep. inf, vedere il file di esempio più avanti in questa sezione.

Dopo aver completato la personalizzazione dell'immagine MED-V, si è pronti a chiudere l'immagine usando Sysprep.

<a href="" id="bkmk-seal"></a>**Sealing dell'immagine MED-V tramite Sysprep**

1.  Lo strumento di preparazione del sistema (Sysprep) è una tecnologia che è possibile usare per eseguire installazioni basate su immagini in tutta la rete con interventi minimi da parte di un amministratore o di un professionista IT.

2.  In un ambiente MED-V è possibile usare Sysprep per assegnare ID di sicurezza univoci (SID) e altre impostazioni a ogni area di lavoro MED-V la prima volta che vengono avviati.

    **Nota**  
    Per altre informazioni sull'uso di Sysprep, vedere [riferimenti tecnici su Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## Esempio


Ecco un esempio di file Sysprep. inf.

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## Argomenti correlati


[Creare un pacchetto nell'area di lavoro MED-V](create-a-med-v-workspace-package.md)

[Creare un'immagine MED-V](prepare-a-med-v-image.md)









