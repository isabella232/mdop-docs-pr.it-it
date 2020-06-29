---
title: CONFIGURE SERVER
description: CONFIGURE SERVER
author: dansimp
ms.assetid: c916eddd-74f2-46e4-953d-120b23284e37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7757f281ec57645d20367056ba0013ef476a91a1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821975"
---
# <span data-ttu-id="22870-103">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="22870-103">CONFIGURE SERVER</span></span>


<span data-ttu-id="22870-104">Consente a un utente di modificare la configurazione di un server; le impostazioni non specificate non verranno modificate.</span><span class="sxs-lookup"><span data-stu-id="22870-104">Enables a user to change the setup of a server; any settings not specified will not be modified.</span></span>

`SFTMIME CONFIGURE SERVER:server-name [/NAME display-name] [/HOST hostname]                 [/PORT port] [/PATH path] [/TYPE {HTTP|RTSP}]                 [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22870-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="22870-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="22870-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22870-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22870-107">SERVER: &lt; nome server&gt;</span><span class="sxs-lookup"><span data-stu-id="22870-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-108">Nome visualizzato per il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="22870-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22870-109">/NAME &lt; -nome visualizzato&gt;</span><span class="sxs-lookup"><span data-stu-id="22870-109">/NAME &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-110">Nuovo nome visualizzato per il server.</span><span class="sxs-lookup"><span data-stu-id="22870-110">New display name for the server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22870-111">&lt;Hostname/host&gt;</span><span class="sxs-lookup"><span data-stu-id="22870-111">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-112">Il nome host o l'indirizzo IP per il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="22870-112">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22870-113">&lt;Porta/Port&gt;</span><span class="sxs-lookup"><span data-stu-id="22870-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-114">Porta in cui è in ascolto il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="22870-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="22870-115">Il valore predefinito è 80 per i normali server HTTP, 443 per i server HTTP con sicurezza avanzata, 554 per i normali server di virtualizzazione delle applicazioni e 322 per i server che usano la sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="22870-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22870-116">&lt;Percorso/path&gt;</span><span class="sxs-lookup"><span data-stu-id="22870-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-117">Parte del percorso dell'URL usato in una richiesta di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="22870-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="22870-118">Se il parametro TYPE è impostato su RTSP, il percorso è facoltativo e il valore predefinito è &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="22870-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22870-119">/TYPE</span><span class="sxs-lookup"><span data-stu-id="22870-119">/TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-120">Indica se il server di pubblicazione è un server Web ( &quot; http &quot; ) o un Application Virtualization Server ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="22870-120">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22870-121">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="22870-121">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-122">Se impostato su attivato, le informazioni di pubblicazione verranno aggiornate quando l'utente effettua l'accesso.</span><span class="sxs-lookup"><span data-stu-id="22870-122">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="22870-123">Impostazioni predefinite su attivato.</span><span class="sxs-lookup"><span data-stu-id="22870-123">Defaults to ON.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22870-124">/SECURE</span><span class="sxs-lookup"><span data-stu-id="22870-124">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-125">Se presente, indica che nel server di pubblicazione deve essere stabilita una connessione con sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="22870-125">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22870-126">/LOG</span><span class="sxs-lookup"><span data-stu-id="22870-126">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-127">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="22870-127">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22870-128">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="22870-128">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-129">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="22870-129">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22870-130">/GUI</span><span class="sxs-lookup"><span data-stu-id="22870-130">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-131">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="22870-131">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="22870-132">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="22870-132">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22870-133">/LOGU</span><span class="sxs-lookup"><span data-stu-id="22870-133">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="22870-134">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="22870-134">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="22870-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22870-135">Related topics</span></span>


[<span data-ttu-id="22870-136">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="22870-136">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





