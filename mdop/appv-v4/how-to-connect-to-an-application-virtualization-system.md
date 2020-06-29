---
title: Come connettersi a un sistema di Application Virtualization
description: Come connettersi a un sistema di Application Virtualization
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817715"
---
# <span data-ttu-id="ee724-103">Come connettersi a un sistema di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ee724-103">How to Connect to an Application Virtualization System</span></span>


<span data-ttu-id="ee724-104">È necessario connettere la console di gestione server Application Virtualization a un sistema di virtualizzazione dell'applicazione prima di poter usare la console di gestione per gestire le applicazioni, le associazioni di tipi di file, i pacchetti, le licenze per le applicazioni, i gruppi di server, i criteri e gli amministratori</span><span class="sxs-lookup"><span data-stu-id="ee724-104">You must connect the Application Virtualization Server Management Console to an Application Virtualization System before you can use the management console to manage applications, file type associations, packages, application licenses, server groups, provider policies and administrators.</span></span> <span data-ttu-id="ee724-105">La procedura seguente illustra i passaggi che è necessario seguire per connettere la console a un sistema di virtualizzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee724-105">The following procedure outlines the steps you must follow to connect the console to an Application Virtualization System.</span></span>

**<span data-ttu-id="ee724-106">Per connettersi a un sistema di virtualizzazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="ee724-106">To connect to an Application Virtualization System</span></span>**

1. <span data-ttu-id="ee724-107">Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro **ambito** e scegliere **Connetti a Application Virtualization System** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="ee724-107">Right-click the Application Virtualization System node in the **Scope** pane, and select **Connect to Application Virtualization System** from the pop-up menu.</span></span>

   **<span data-ttu-id="ee724-108">Nota</span><span class="sxs-lookup"><span data-stu-id="ee724-108">Note</span></span>**  
   <span data-ttu-id="ee724-109">Sono disponibili tre componenti per la gestione di Application Virtualization Server: la console di gestione di Application Virtualization, il servizio Web di gestione e il datastore SQL.</span><span class="sxs-lookup"><span data-stu-id="ee724-109">There are three components to Application Virtualization server management: the Application Virtualization Management Console, the Management Web Service, and the SQL Datastore.</span></span> <span data-ttu-id="ee724-110">Se questi componenti sono distribuiti in computer fisici diversi, è necessario configurare correttamente la sicurezza per i componenti per comunicare in tutto il sistema.</span><span class="sxs-lookup"><span data-stu-id="ee724-110">If these components are distributed across different physical machines, you must configure security properly for the components to communicate across the system.</span></span> <span data-ttu-id="ee724-111">Per altre informazioni, vedere i manuali e gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee724-111">For more information, see the following manuals and articles:</span></span>

   <span data-ttu-id="ee724-112">[Come configurare il server in modo che sia attendibile per la delega](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span><span class="sxs-lookup"><span data-stu-id="ee724-112">[How to Configure the Server to be Trusted for Delegation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span></span>

   <span data-ttu-id="ee724-113">[Guida alla pianificazione e alla distribuzione per il sistema di virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span><span class="sxs-lookup"><span data-stu-id="ee724-113">[Planning and Deployment Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span></span>

   <span data-ttu-id="ee724-114">[Guida alle operazioni per l'Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span><span class="sxs-lookup"><span data-stu-id="ee724-114">[Operations Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span></span>

   <span data-ttu-id="ee724-115">[Articolo 930472](https://go.microsoft.com/fwlink/?LinkId=114647) della Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114647)</span><span class="sxs-lookup"><span data-stu-id="ee724-115">[Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)</span></span>

   <span data-ttu-id="ee724-116">[Articolo 930565](https://go.microsoft.com/fwlink/?LinkId=114648) della Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114648)</span><span class="sxs-lookup"><span data-stu-id="ee724-116">[Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)</span></span>

     

2. <span data-ttu-id="ee724-117">Completare i campi nella finestra di dialogo **Connetti a Application Virtualization System** :</span><span class="sxs-lookup"><span data-stu-id="ee724-117">Complete the fields in the **Connect to Application Virtualization System** dialog box:</span></span>

   1. <span data-ttu-id="ee724-118">**Nome host servizio Web**: immettere il nome del sistema di virtualizzazione delle applicazioni a cui si vuole connettersi o immettere **localhost** per connettersi al server locale.</span><span class="sxs-lookup"><span data-stu-id="ee724-118">**Web Service Host Name**—Enter the name of the Application Virtualization System to which you want to connect, or enter **localhost** to connect to the local server.</span></span>

   2. <span data-ttu-id="ee724-119">**Usa connessione sicura**: selezionare questa casella di controllo se si vuole connettersi al server con una connessione sicura.</span><span class="sxs-lookup"><span data-stu-id="ee724-119">**Use Secure Connection**—Select this check box if you want to connect to the server with a secure connection.</span></span>

   3. <span data-ttu-id="ee724-120">**Porta**: immettere il numero di porta che si vuole usare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="ee724-120">**Port**—Enter the port number you want to use for the connection.</span></span> <span data-ttu-id="ee724-121">**80** è il numero di porta normale predefinito e **443** è il numero di porta sicura.</span><span class="sxs-lookup"><span data-stu-id="ee724-121">**80** is the default regular port number, and **443** is the secure-port number.</span></span>

   4. <span data-ttu-id="ee724-122">**Usare l'account di Windows corrente**: selezionare questo pulsante di opzione per usare le credenziali dell'account di Windows corrente.</span><span class="sxs-lookup"><span data-stu-id="ee724-122">**Use Current Windows Account**—Select this radio button to use the current Windows account credentials.</span></span>

   5. <span data-ttu-id="ee724-123">**Specificare l'account di Windows**: selezionare questo pulsante di opzione quando si vuole connettersi al server come utente diverso.</span><span class="sxs-lookup"><span data-stu-id="ee724-123">**Specify Windows Account**—Select this radio button when you want to connect to the server as a different user.</span></span>

   6. <span data-ttu-id="ee724-124">**Nome**: immettere il nome del nuovo utente usando il formato *dominio omeutente* o <em> username@domain </em> .</span><span class="sxs-lookup"><span data-stu-id="ee724-124">**Name**—Enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

   7. <span data-ttu-id="ee724-125">**Password**: immettere la password corrispondente al nuovo utente.</span><span class="sxs-lookup"><span data-stu-id="ee724-125">**Password**—Enter the password that corresponds to the new user.</span></span>

3. <span data-ttu-id="ee724-126">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee724-126">Click **OK**.</span></span>

## <span data-ttu-id="ee724-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee724-127">Related topics</span></span>


[<span data-ttu-id="ee724-128">Come eseguire attività amministrative in Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="ee724-128">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





