---
title: Come convalidare l'installazione di MBAM con Configuration Manager
description: Come convalidare l'installazione di MBAM con Configuration Manager
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822636"
---
# <span data-ttu-id="1ee77-103">Come convalidare l'installazione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1ee77-103">How to Validate the MBAM Installation with Configuration Manager</span></span>


<span data-ttu-id="1ee77-104">Dopo l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM) con Configuration Manager, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM completando la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="1ee77-104">After installing Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, validate that the installation has successfully set up all the necessary features for MBAM by completing the following steps.</span></span>

**<span data-ttu-id="1ee77-105">Per convalidare l'installazione delle funzionalità di MBAM server con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1ee77-105">To validate the MBAM Server feature installation with Configuration Manager</span></span>**

1.  <span data-ttu-id="1ee77-106">Nel server in cui è distribuito System Center Configuration Manager aprire il **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-106">On the server where System Center Configuration Manager is deployed, open **Control Panel**.</span></span> <span data-ttu-id="1ee77-107">Selezionare il programma usato per disinstallare o modificare un programma.</span><span class="sxs-lookup"><span data-stu-id="1ee77-107">Select the program that is used to uninstall or change a program.</span></span> <span data-ttu-id="1ee77-108">Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco di programmi e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1ee77-108">Verify that **Microsoft BitLocker Administration and Monitoring** appears in the list of programs and features.</span></span>

    <span data-ttu-id="1ee77-109">**Nota**  Per convalidare l'installazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.</span><span class="sxs-lookup"><span data-stu-id="1ee77-109">**Note** To validate the installation, you must use a domain account that has local computer administrative credentials on each server.</span></span>

     

2.  <span data-ttu-id="1ee77-110">Usare la console di Configuration Manager per verificare che venga visualizzata una nuova raccolta, denominata "MBAM supported Computers".</span><span class="sxs-lookup"><span data-stu-id="1ee77-110">Use the Configuration Manager console to confirm that a new collection, called “MBAM Supported Computers,” is displayed.</span></span>

    <span data-ttu-id="1ee77-111">Per visualizzare la raccolta con Configuration Manager 2007: fare clic su **database sito** ( &lt; **codicesito** &gt;  -  &lt; **nomeserver** &gt; , &lt; **siteName** &gt; ), **Gestione computer**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-111">To view the collection with Configuration Manager 2007: Click **Site Database** (&lt;**SiteCode**&gt; - &lt;**ServerName**&gt;, &lt;**SiteName**&gt;), **Computer Management**.</span></span>

    <span data-ttu-id="1ee77-112">Per visualizzare la raccolta con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **asset e conformità** , **Raccolte dispositivi**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-112">To view the collection with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Device Collections**.</span></span>

3.  <span data-ttu-id="1ee77-113">Usare la console di Configuration Manager per verificare che i report seguenti siano elencati nella cartella **mbam** :</span><span class="sxs-lookup"><span data-stu-id="1ee77-113">Use the Configuration Manager console to verify that the following reports are listed in the **MBAM** folder:</span></span>

    -   <span data-ttu-id="1ee77-114">Conformità al computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="1ee77-114">BitLocker Computer Compliance</span></span>

    -   <span data-ttu-id="1ee77-115">Dashboard di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="1ee77-115">BitLocker Enterprise Compliance Dashboard</span></span>

    -   <span data-ttu-id="1ee77-116">Dettagli di conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="1ee77-116">BitLocker Enterprise Compliance Details</span></span>

    -   <span data-ttu-id="1ee77-117">Riepilogo conformità di BitLocker Enterprise</span><span class="sxs-lookup"><span data-stu-id="1ee77-117">BitLocker Enterprise Compliance Summary</span></span>

    <span data-ttu-id="1ee77-118">Per visualizzare i report con Configuration Manager 2007: fare clic su **report**, **Reporting Services**, \ \ \ \ &lt; **nomeserver** &gt; , **cartelle report**</span><span class="sxs-lookup"><span data-stu-id="1ee77-118">To view the reports with Configuration Manager 2007: Click **Reporting**, **Reporting Services**, \\\\&lt;**ServerName**&gt;, **Report Folders**</span></span>

    <span data-ttu-id="1ee77-119">Per visualizzare i report con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **monitoraggio** , **creazione**di report e **report**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-119">To view the reports with SystemCenter2012 ConfigurationManager: Click the **Monitoring** workspace, **Reporting**, **Reports**.</span></span>

4.  <span data-ttu-id="1ee77-120">Usare la console di Configuration Manager per verificare che la configurazione della previsione "protezione BitLocker" sia elencata.</span><span class="sxs-lookup"><span data-stu-id="1ee77-120">Use the Configuration Manager console to confirm that the configuration baseline “BitLocker Protection” is listed.</span></span>

    <span data-ttu-id="1ee77-121">Per visualizzare le previsioni di configurazione con Configuration Manager 2007: fare clic su **Gestione configurazione desiderata**, **previsioni di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-121">To view the configuration baselines with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Baselines**.</span></span>

    <span data-ttu-id="1ee77-122">Per visualizzare le previsioni di configurazione con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **asset e conformità** , **Impostazioni conformità**, **previsioni di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-122">To view the configuration baselines with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Baselines**.</span></span>

5.  <span data-ttu-id="1ee77-123">Usare la console di Configuration Manager per verificare che vengano visualizzati i nuovi elementi di configurazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ee77-123">Use the Configuration Manager console to confirm that the following new configuration items are displayed:</span></span>

    -   <span data-ttu-id="1ee77-124">Protezione delle unità dati fisse di BitLocker</span><span class="sxs-lookup"><span data-stu-id="1ee77-124">BitLocker Fixed Data Drives Protection</span></span>

    -   <span data-ttu-id="1ee77-125">Protezione unità sistema operativo BitLocker</span><span class="sxs-lookup"><span data-stu-id="1ee77-125">BitLocker Operating System Drive Protection</span></span>

    <span data-ttu-id="1ee77-126">Per visualizzare gli elementi di configurazione con Configuration Manager 2007: fare clic su **Gestione configurazione desiderata**, **elementi di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-126">To view the configuration items with Configuration Manager 2007: Click **Desired Configuration Management**, **Configuration Items**.</span></span>

    <span data-ttu-id="1ee77-127">Per visualizzare gli elementi di configurazione con SystemCenter2012 ConfigurationManager: fare clic sull'area di lavoro **asset e conformità** , **Impostazioni conformità**, **elementi di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="1ee77-127">To view the configuration items with SystemCenter2012 ConfigurationManager: Click the **Assets and Compliance** workspace, **Compliance Settings**, **Configuration Items**.</span></span>

## <span data-ttu-id="1ee77-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ee77-128">Related topics</span></span>


[<span data-ttu-id="1ee77-129">Distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="1ee77-129">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





