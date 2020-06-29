---
title: Sicurezza di App-V Desktop Client
description: Sicurezza di App-V Desktop Client
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822316"
---
# <span data-ttu-id="79a79-103">Sicurezza di App-V Desktop Client</span><span class="sxs-lookup"><span data-stu-id="79a79-103">App-V Desktop Client Security</span></span>


<span data-ttu-id="79a79-104">Il client Desktop App-V offre numerosi miglioramenti della sicurezza non disponibili nelle versioni precedenti del prodotto.</span><span class="sxs-lookup"><span data-stu-id="79a79-104">The App-V Desktop Client provides many security enhancements that were not available in previous versions of the product.</span></span> <span data-ttu-id="79a79-105">Queste modifiche conferiscono livelli di sicurezza più alti per impostazione predefinita e tramite la configurazione delle impostazioni del client.</span><span class="sxs-lookup"><span data-stu-id="79a79-105">These changes provide higher levels of security by default and through configuration of the client settings.</span></span>

<span data-ttu-id="79a79-106">**Nota**  Quando si installa il client Desktop App-V in un computer, il software viene impostato automaticamente sulle impostazioni più sicure.</span><span class="sxs-lookup"><span data-stu-id="79a79-106">**Note** When you install the App-V Desktop Client on a computer, the software defaults to the most secure settings.</span></span> <span data-ttu-id="79a79-107">Tuttavia, durante l'aggiornamento, le impostazioni precedenti del client persistono.</span><span class="sxs-lookup"><span data-stu-id="79a79-107">However, when upgrading, the previous settings of the client persist.</span></span>

 

<span data-ttu-id="79a79-108">Per impostazione predefinita, il client Desktop App-V è configurato solo con le autorizzazioni necessarie per consentire a un utente non amministrativo di eseguire un'applicazione di aggiornamento e flusso di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="79a79-108">By default, the App-V Desktop Client is configured only with the permissions required to allow a non-administrative user to perform a publishing refresh and stream applications.</span></span> <span data-ttu-id="79a79-109">I miglioramenti aggiuntivi per la sicurezza forniti nel client desktop di App-V includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="79a79-109">Additional security enhancements provided in the App-V Desktop Client include the following:</span></span>

-   <span data-ttu-id="79a79-110">Per impostazione predefinita, un aggiornamento della cache OSD è consentito solo dal processo di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="79a79-110">By default, an OSD cache update is allowed only by the publishing refresh process.</span></span>

-   <span data-ttu-id="79a79-111">Il file di log ( `sftlog.txt` ) è accessibile solo dagli account con accesso amministrativo locale al client.</span><span class="sxs-lookup"><span data-stu-id="79a79-111">The log file (`sftlog.txt`) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="79a79-112">Il file di log ha ora una dimensione massima.</span><span class="sxs-lookup"><span data-stu-id="79a79-112">The log file now has a maximum size.</span></span>

-   <span data-ttu-id="79a79-113">I file di log vengono gestiti tramite le impostazioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="79a79-113">The log files are managed through archive settings.</span></span>

-   <span data-ttu-id="79a79-114">Ora viene eseguita la registrazione degli eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="79a79-114">System Event logging is now performed.</span></span>

## <span data-ttu-id="79a79-115">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="79a79-115">Permissions</span></span>


<span data-ttu-id="79a79-116">Dopo aver installato il client desktop, è possibile configurare altre impostazioni di sicurezza tramite MMC o un singolo client usando il registro di sistema o il modello ADM fornito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="79a79-116">After you install the Desktop Client, you can configure other security settings through the MMC, or on an individual client by using the registry or the ADM Template provided by Microsoft.</span></span> <span data-ttu-id="79a79-117">Il client Desktop App-V dispone delle autorizzazioni che è possibile impostare per limitare l'accesso a tutte le funzionalità del client desktop da parte di utenti non amministrativi.</span><span class="sxs-lookup"><span data-stu-id="79a79-117">The App-V Desktop Client has permissions that you can set to restrict non-administrative users from accessing all the features of the Desktop Client.</span></span> <span data-ttu-id="79a79-118">Per un elenco completo delle autorizzazioni, vedere il file della Guida dell'App-V client o l'App-V Operations Guide.</span><span class="sxs-lookup"><span data-stu-id="79a79-118">For a full list of permissions, please see the App-V Client Help file or App-V Operations Guide.</span></span>

<span data-ttu-id="79a79-119">**Importante**  Valutare attentamente le conseguenze della modifica dei diritti di accesso, in particolare nei sistemi condivisi da più utenti, ad esempio i server terminal.</span><span class="sxs-lookup"><span data-stu-id="79a79-119">**Important** Carefully consider the consequences of changing access rights, especially on systems that are shared by multiple users, such as Terminal Servers.</span></span>

 

<span data-ttu-id="79a79-120">**Nota**  Se gli utenti dell'ambiente hanno privilegi di amministratore locale per i propri computer, le autorizzazioni vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="79a79-120">**Note** If users in the environment have local administrator privileges for their computers, the permissions are ignored.</span></span>

 

### <span data-ttu-id="79a79-121">Modello ADM</span><span class="sxs-lookup"><span data-stu-id="79a79-121">ADM Template</span></span>

<span data-ttu-id="79a79-122">Microsoft Application Virtualization (App-V) introduce un modello ADM che può essere usato per configurare le impostazioni client più comuni tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="79a79-122">Microsoft Application Virtualization (App-V) introduces an ADM Template that you can use to configure the most common client settings through Group Policies.</span></span> <span data-ttu-id="79a79-123">Questo modello consente agli amministratori di implementare e modificare molte delle impostazioni del client tramite un modello di amministrazione centralizzato.</span><span class="sxs-lookup"><span data-stu-id="79a79-123">This template enables administrators to implement and change many of the client settings through a centralized administration model.</span></span> <span data-ttu-id="79a79-124">Alcune delle impostazioni disponibili nel modello ADM sono le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="79a79-124">Some of the settings available in the ADM Template are security settings.</span></span>

<span data-ttu-id="79a79-125">**Importante**  Quando si usa il modello ADM, tenere presente che le impostazioni sono le impostazioni delle preferenze dei criteri di gruppo e i criteri di gruppo non completamente gestiti.</span><span class="sxs-lookup"><span data-stu-id="79a79-125">**Important** When using the ADM Template, remember that the settings are Group Policy preference settings and not fully managed Group Policies.</span></span>

 

<span data-ttu-id="79a79-126">Per una descrizione completa del modello ADM, delle impostazioni specifiche e delle indicazioni per la distribuzione corretta dei client nell'ambiente, vedere il white paper su App-V ADM [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .</span><span class="sxs-lookup"><span data-stu-id="79a79-126">For a full description of the ADM Template, the specific settings, and guidance to successfully deploy clients in your environment, see the App-V ADM Template white paper at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063).</span></span>

## <span data-ttu-id="79a79-127">Rimozione delle associazioni di tipi di file OSD</span><span class="sxs-lookup"><span data-stu-id="79a79-127">Removing OSD File Type Associations</span></span>


<span data-ttu-id="79a79-128">Se l'organizzazione non richiede agli utenti di aprire applicazioni direttamente da un file OSD, è possibile migliorare la sicurezza rimuovendo le associazioni di tipi di file nel client.</span><span class="sxs-lookup"><span data-stu-id="79a79-128">If your organization does not require users to open applications directly from an OSD file, you can enhance security by removing the file type associations on the client.</span></span> <span data-ttu-id="79a79-129">Rimuovere le `HKEY_CURRENT_USERS` chiavi per OSD e `Softgird.osd.file` usare l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="79a79-129">Remove the `HKEY_CURRENT_USERS` keys for OSD and `Softgird.osd.file` by using the registry editor.</span></span> <span data-ttu-id="79a79-130">Puoi inserire questo processo in uno script di accesso o in uno script di post-installazione per automatizzare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="79a79-130">You can put this process into a logon script or into a post-installation script to automate these changes.</span></span>

 

 





