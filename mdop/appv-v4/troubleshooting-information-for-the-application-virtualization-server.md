---
title: Informazioni sulla risoluzione dei problemi per Application Virtualization Server
description: Informazioni sulla risoluzione dei problemi per Application Virtualization Server
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815186"
---
# <span data-ttu-id="97800-103">Informazioni sulla risoluzione dei problemi per Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="97800-103">Troubleshooting Information for the Application Virtualization Server</span></span>


<span data-ttu-id="97800-104">Questo argomento include le informazioni che è possibile usare per risolvere i problemi relativi ai vari tipi di server Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="97800-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Servers.</span></span>

## <span data-ttu-id="97800-105">Messaggio di avviso 25017 nel log di installazione dopo l'installazione del server</span><span class="sxs-lookup"><span data-stu-id="97800-105">Warning Message 25017 in Setup Log After Installing the Server</span></span>


<span data-ttu-id="97800-106">Dopo l'installazione potrebbe essere visualizzato il messaggio seguente nel log di configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="97800-106">You might find the following message in the server setup log after installation.</span></span>

*<span data-ttu-id="97800-107">Avviso 25017.</span><span class="sxs-lookup"><span data-stu-id="97800-107">Warning 25017.</span></span> <span data-ttu-id="97800-108">Il programma di installazione non può creare l'oggetto indicatore di Active Directory per il server.</span><span class="sxs-lookup"><span data-stu-id="97800-108">The installation Program could not create the Active Directory marker object for the server.</span></span> <span data-ttu-id="97800-109">L'account usato per l'installazione non ha i diritti sufficienti per scrivere in Active Directory o Active Directory non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="97800-109">The account used to install did not have the sufficient rights to write to Active Directory or Active Directory was unavailable.</span></span>*

<span data-ttu-id="97800-110">Il programma di installazione di App-V Management o Streaming Server crea una voce del punto di connessione del servizio sotto l'oggetto computer in servizi di dominio Active Directory che corrisponde al computer in cui è installato il server se l'account usato per eseguire il programma di installazione ha i diritti appropriati.</span><span class="sxs-lookup"><span data-stu-id="97800-110">The App-V Management or Streaming Server installer creates a Service Connection Point entry under the Computer object in Active Directory Domain Services (ADDS) that corresponds to the computer on which the server is installed if the account used to run the installer has the appropriate rights.</span></span> <span data-ttu-id="97800-111">La mancata creazione di questa voce non comporterà un errore di installazione e ciò non dovrebbe influire in altro modo sul funzionamento del prodotto.</span><span class="sxs-lookup"><span data-stu-id="97800-111">Failure to create this entry will not cause the install to fail and this should not otherwise affect the functioning of the product.</span></span> <span data-ttu-id="97800-112">La causa probabile di qualsiasi errore è che l'account utente usato per eseguire l'installazione non dispone di diritti sufficienti per la scrittura in aggiunte.</span><span class="sxs-lookup"><span data-stu-id="97800-112">The likely cause of any failure is that the user account used to run the install did not have sufficient rights to write to ADDS.</span></span> <span data-ttu-id="97800-113">Anche se la registrazione dell'App-V Server in aggiunte è facoltativa, uno dei vantaggi di questa operazione consente agli strumenti di gestione centralizzati di individuare l'App-V Server per scopi di inventario e gestione.</span><span class="sxs-lookup"><span data-stu-id="97800-113">Although registering the App-V server in ADDS is optional, one benefit of doing so enables centralized management tools to locate the App-V server for inventory and management purposes.</span></span>

## <span data-ttu-id="97800-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97800-114">Related topics</span></span>


[<span data-ttu-id="97800-115">Application Virtualization Server</span><span class="sxs-lookup"><span data-stu-id="97800-115">Application Virtualization Server</span></span>](application-virtualization-server.md)

 

 





