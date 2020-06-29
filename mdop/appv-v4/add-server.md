---
title: ADD SERVER
description: ADD SERVER
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819886"
---
# <span data-ttu-id="d6e97-103">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="d6e97-103">ADD SERVER</span></span>


<span data-ttu-id="d6e97-104">Aggiunge un server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="d6e97-104">Adds a publishing server.</span></span>

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d6e97-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="d6e97-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d6e97-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6e97-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6e97-107">SERVER: &lt; nome server&gt;</span><span class="sxs-lookup"><span data-stu-id="d6e97-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-108">Nome visualizzato per il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="d6e97-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6e97-109">&lt;Hostname/host&gt;</span><span class="sxs-lookup"><span data-stu-id="d6e97-109">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-110">Il nome host o l'indirizzo IP per il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="d6e97-110">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6e97-111">/TYPE {HTTP | RTSP</span><span class="sxs-lookup"><span data-stu-id="d6e97-111">/TYPE {HTTP|RTSP}</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-112">Indica se il server di pubblicazione è un server Web ( &quot; http &quot; ) o un Application Virtualization Server ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="d6e97-112">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6e97-113">&lt;Porta/Port&gt;</span><span class="sxs-lookup"><span data-stu-id="d6e97-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-114">Porta in cui è in ascolto il server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="d6e97-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="d6e97-115">Il valore predefinito è 80 per i normali server HTTP, 443 per i server HTTP con sicurezza avanzata, 554 per i normali server di virtualizzazione delle applicazioni e 322 per i server che usano la sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="d6e97-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6e97-116">&lt;Percorso/path&gt;</span><span class="sxs-lookup"><span data-stu-id="d6e97-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-117">Parte del percorso dell'URL usato in una richiesta di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="d6e97-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="d6e97-118">Se il parametro TYPE è impostato su RTSP, il percorso è facoltativo e il valore predefinito è &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="d6e97-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6e97-119">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="d6e97-119">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-120">Se impostato su attivato, le informazioni di pubblicazione verranno aggiornate quando l'utente effettua l'accesso.</span><span class="sxs-lookup"><span data-stu-id="d6e97-120">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="d6e97-121">Impostazioni predefinite su attivato.</span><span class="sxs-lookup"><span data-stu-id="d6e97-121">Defaults to ON.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6e97-122">/SECURE</span><span class="sxs-lookup"><span data-stu-id="d6e97-122">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-123">Se presente, indica che nel server di pubblicazione deve essere stabilita una connessione con sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="d6e97-123">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6e97-124">/LOG</span><span class="sxs-lookup"><span data-stu-id="d6e97-124">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-125">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="d6e97-125">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6e97-126">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="d6e97-126">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-127">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="d6e97-127">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d6e97-128">/GUI</span><span class="sxs-lookup"><span data-stu-id="d6e97-128">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-129">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="d6e97-129">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d6e97-130">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="d6e97-130">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d6e97-131">/LOGU</span><span class="sxs-lookup"><span data-stu-id="d6e97-131">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="d6e97-132">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d6e97-132">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d6e97-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6e97-133">Related topics</span></span>


[<span data-ttu-id="d6e97-134">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="d6e97-134">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





