---
title: Note sulla versione di App-V 4.6 SP3
description: Note sulla versione di App-V 4.6 SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819795"
---
# <span data-ttu-id="d9937-103">Note sulla versione di App-V 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="d9937-103">App-V 4.6 SP3 Release Notes</span></span>


<span data-ttu-id="d9937-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="d9937-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="d9937-105">Leggere accuratamente queste note sulla versione prima di installare il sistema di gestione di Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="d9937-105">Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="d9937-106">Queste note sulla versione contengono informazioni che consentono di installare correttamente Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="d9937-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP3.</span></span> <span data-ttu-id="d9937-107">Questo documento contiene informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d9937-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="d9937-108">Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V, la modifica più recente deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="d9937-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="d9937-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="d9937-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="d9937-110">Protezione da vulnerabilità e virus della sicurezza</span><span class="sxs-lookup"><span data-stu-id="d9937-110">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="d9937-111">Per proteggere le vulnerabilità e i virus della sicurezza, è importante installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare.</span><span class="sxs-lookup"><span data-stu-id="d9937-111">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="d9937-112">Per altre informazioni, vedere il [sito Web Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="d9937-112">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="d9937-113">Problemi noti di Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="d9937-113">Known Issues with Application Virtualization4.6 SP3</span></span>


<span data-ttu-id="d9937-114">Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.6 SP3.</span><span class="sxs-lookup"><span data-stu-id="d9937-114">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6SP3.</span></span> <span data-ttu-id="d9937-115">Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="d9937-115">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="d9937-116">Quando è possibile, questi problemi verranno risolti in versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d9937-116">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="d9937-117">Non è possibile aprire collegamenti ipertestuali tramite Internet Explorer11 in Microsoft Windows 8,1 nell'ambiente virtuale</span><span class="sxs-lookup"><span data-stu-id="d9937-117">Unable to open hyperlinks using Internet Explorer11 on Microsoft Windows 8.1 within the Virtual Environment</span></span>

<span data-ttu-id="d9937-118">Il tentativo di aprire collegamenti ipertestuali dall'interno di un ambiente virtuale non riesce in Windows 8,1 con Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="d9937-118">Attempting to open hyperlinks from within a virtual environment will fail on Windows 8.1 using Internet Explorer 11.</span></span> <span data-ttu-id="d9937-119">Questo perché Internet Explorer 11 ora viene fornito con la modalità di protezione avanzata abilitata per impostazione predefinita e questo fa sì che App-V non sia in grado di accedere alle chiavi del registro di sistema, ai file e agli oggetti della porta di comunicazione necessari.</span><span class="sxs-lookup"><span data-stu-id="d9937-119">This is because Internet Explorer 11 now ships with the Enhanced Protection Mode (EPM) enabled by default and this causes App-V to be unable to access required registry keys, files and communication port objects.</span></span>

<span data-ttu-id="d9937-120">SOLUZIONE alternativa: disabilitare EPM in Internet Explorer11 prima di aprire un pacchetto di App-V.</span><span class="sxs-lookup"><span data-stu-id="d9937-120">WORKAROUND: Disable EPM in Internet Explorer11 before opening an App-V package.</span></span> <span data-ttu-id="d9937-121">In questo modo potrai aprire Internet Explorer dall'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9937-121">This will allow you to open Internet Explorer from within the virtual environment.</span></span>

## <span data-ttu-id="d9937-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9937-122">Related topics</span></span>


[<span data-ttu-id="d9937-123">Informazioni su Microsoft Application Virtualization 4.6 SP3</span><span class="sxs-lookup"><span data-stu-id="d9937-123">About Microsoft Application Virtualization 4.6 SP3</span></span>](about-microsoft-application-virtualization-46-sp3.md)

 

 





