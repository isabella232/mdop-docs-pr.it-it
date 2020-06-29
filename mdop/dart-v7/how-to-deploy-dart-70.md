---
title: Come distribuire DaRT 7.0
description: Come distribuire DaRT 7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804684"
---
# <span data-ttu-id="bde21-103">Come distribuire DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="bde21-103">How to Deploy DaRT 7.0</span></span>


<span data-ttu-id="bde21-104">Questo argomento fornisce istruzioni per distribuire Microsoft Diagnostics and Recovery Toolset (DaRT) 7 nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="bde21-104">This topic provides instructions to deploy Microsoft Diagnostics and Recovery Toolset (DaRT)7 in your environment.</span></span> <span data-ttu-id="bde21-105">La prima procedura in questo argomento presuppone che si stiano installando tutte le funzionalità in un computer amministratore.</span><span class="sxs-lookup"><span data-stu-id="bde21-105">The first procedure in this topic assumes that you are installing all functionality on one administrator computer.</span></span> <span data-ttu-id="bde21-106">Quando è necessario distribuire o disinstallare il dardo in più computer usando un sistema di distribuzione elettronica del software, ad esempio, potrebbe essere più semplice usare le opzioni di installazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="bde21-106">When you need to deploy or uninstall DaRT on multiple computers, using an electronic software distribution system for example, it might be easier to use command line installation options.</span></span> <span data-ttu-id="bde21-107">Queste opzioni sono definite nella seconda procedura descritta in questo argomento che fornisce l'utilizzo di esempio per le opzioni della riga di comando disponibili.</span><span class="sxs-lookup"><span data-stu-id="bde21-107">Those options are defined in the second procedure in this topic which provides example usage for the available command line options.</span></span>

<span data-ttu-id="bde21-108">**Importante**  Prima di installare DaRT, assicurati che il computer soddisfi i requisiti minimi di sistema elencati nelle [configurazioni supportate di dart 7,0](dart-70-supported-configurations-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="bde21-108">**Important** Before you install DaRT, ensure that the computer meets the minimum system requirements listed in [DaRT 7.0 Supported Configurations](dart-70-supported-configurations-dart-7.md).</span></span>

 

**<span data-ttu-id="bde21-109">Per installare il dardo in un computer amministratore</span><span class="sxs-lookup"><span data-stu-id="bde21-109">To install DaRT on an administrator computer</span></span>**

1.  <span data-ttu-id="bde21-110">Individuare i file di installazione di DaRT ricevuti come parte del download del software.</span><span class="sxs-lookup"><span data-stu-id="bde21-110">Locate the DaRT installation files that you received as part of your software download.</span></span>

2.  <span data-ttu-id="bde21-111">Fare doppio clic sul file di installazione di DaRT che corrisponde ai requisiti di sistema, ovvero 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="bde21-111">Double-click the DaRT installation file that corresponds to your system requirements, either 32-bit or 64-bit.</span></span> <span data-ttu-id="bde21-112">Il file di installazione di DaRT è denominato **MSDaRT70.msi**.</span><span class="sxs-lookup"><span data-stu-id="bde21-112">The DaRT installation file is named **MSDaRT70.msi**.</span></span>

3.  <span data-ttu-id="bde21-113">Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="bde21-113">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="bde21-114">Selezionare la cartella di destinazione per l'installazione di DaRT, selezionare se il dardo deve essere installato per tutti gli utenti o solo per l'utente corrente e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="bde21-114">Select the destination folder for installing DaRT, select whether DaRT should be installed for all users or just the current user, and then click **Next**.</span></span>

5.  <span data-ttu-id="bde21-115">Selezionare se l'installazione deve essere **tipica**, **personalizzata**o **completa**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="bde21-115">Select whether the installation should be **Typical**, **Custom**, or **Complete**, and then click **Next**.</span></span>

    -   <span data-ttu-id="bde21-116">**Tipico** installa gli strumenti usati più di frequente.</span><span class="sxs-lookup"><span data-stu-id="bde21-116">**Typical** installs the tools that are most frequently used.</span></span> <span data-ttu-id="bde21-117">Questo metodo è consigliato per la maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="bde21-117">This method is recommended for most users.</span></span>

    -   <span data-ttu-id="bde21-118">**Personalizzato** consente di selezionare gli strumenti installati e dove verranno installati.</span><span class="sxs-lookup"><span data-stu-id="bde21-118">**Custom** lets you select the tools that are installed and where they will be installed.</span></span> <span data-ttu-id="bde21-119">Questo è consigliato per gli utenti avanzati, soprattutto se stai installando diversi strumenti DaRT in diversi computer dell'helpdesk.</span><span class="sxs-lookup"><span data-stu-id="bde21-119">This is recommended for advanced users, especially if you are installing different DaRT tools on different helpdesk computers.</span></span>

    -   <span data-ttu-id="bde21-120">**Completa** installa tutti gli strumenti DART e richiede la maggior parte dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="bde21-120">**Complete** installs all DaRT tools and requires the most disk space.</span></span>

    <span data-ttu-id="bde21-121">Dopo aver selezionato il metodo di installazione, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="bde21-121">After you have selected your method of installation, click **Next**.</span></span>

6.  <span data-ttu-id="bde21-122">Per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="bde21-122">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="bde21-123">Dopo aver completato l'installazione, fare clic su **fine** per chiudere la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="bde21-123">After the installation is completed successfully, click **Finish** to exit the wizard.</span></span>

**<span data-ttu-id="bde21-124">Per installare il dardo al prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="bde21-124">To install DaRT at the command prompt</span></span>**

1.  <span data-ttu-id="bde21-125">L'esempio seguente mostra come installare tutte le funzionalità dardo.</span><span class="sxs-lookup"><span data-stu-id="bde21-125">The following example shows how to install all DaRT functionality.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  <span data-ttu-id="bde21-126">L'esempio seguente mostra come installare solo la **creazione guidata immagine di ripristino di freccette**.</span><span class="sxs-lookup"><span data-stu-id="bde21-126">The following example shows how to install only the **DaRT Recovery Image Wizard**.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  <span data-ttu-id="bde21-127">L'esempio seguente mostra come installare solo l'analizzatore crash e il Visualizzatore di connessioni remote DaRT.</span><span class="sxs-lookup"><span data-stu-id="bde21-127">The following example shows how to install only the Crash Analyzer and the DaRT Remote Connection Viewer.</span></span>

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  <span data-ttu-id="bde21-128">L'esempio seguente crea un log di configurazione per Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="bde21-128">The following example creates a setup log for the Windows Installer.</span></span> <span data-ttu-id="bde21-129">Questa operazione è utile per il debug.</span><span class="sxs-lookup"><span data-stu-id="bde21-129">This is valuable for debugging.</span></span>

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

<span data-ttu-id="bde21-130">**Nota**  Puoi aggiungere/qn o/qb alle opzioni del prompt dei comandi per l'installazione di DaRT per eseguire un'installazione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="bde21-130">**Note** You can add /qn or /qb to any of the DaRT installation command prompt options to perform a silent installation.</span></span>

 

## <span data-ttu-id="bde21-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bde21-131">Related topics</span></span>


[<span data-ttu-id="bde21-132">Distribuzione di DaRT 7.0 nei computer di amministrazione</span><span class="sxs-lookup"><span data-stu-id="bde21-132">Deploying DaRT 7.0 to Administrator Computers</span></span>](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





