---
title: Come configurare il file di registro del client
description: Come configurare il file di registro del client
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817796"
---
# <span data-ttu-id="65b7c-103">Come configurare il file di registro del client</span><span class="sxs-lookup"><span data-stu-id="65b7c-103">How to Configure the Client Log File</span></span>


<span data-ttu-id="65b7c-104">Per configurare il file di log client Application Virtualization (App-V), è possibile usare le procedure seguenti.</span><span class="sxs-lookup"><span data-stu-id="65b7c-104">You can use the following procedures to configure the Application Virtualization (App-V) Client log file.</span></span>

**<span data-ttu-id="65b7c-105">Per modificare il percorso del file di log</span><span class="sxs-lookup"><span data-stu-id="65b7c-105">To change the log file location</span></span>**

-   <span data-ttu-id="65b7c-106">Modificare il valore della chiave del registro di sistema seguente per specificare il nuovo percorso per il file di log.</span><span class="sxs-lookup"><span data-stu-id="65b7c-106">Edit the following registry key value to specify the new path for the log file.</span></span> <span data-ttu-id="65b7c-107">Dopo aver modificato questo valore, devi riavviare il servizio **sftlist** .</span><span class="sxs-lookup"><span data-stu-id="65b7c-107">You must restart the **sftlist** service after changing this value.</span></span> <span data-ttu-id="65b7c-108">Questa posizione può essere modificata anche in modo interattivo dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="65b7c-108">This location can also be changed interactively after installation.</span></span>

    <span data-ttu-id="65b7c-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span><span class="sxs-lookup"><span data-stu-id="65b7c-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span></span>

**<span data-ttu-id="65b7c-110">Per modificare il livello di report del log</span><span class="sxs-lookup"><span data-stu-id="65b7c-110">To change the log reporting level</span></span>**

-   <span data-ttu-id="65b7c-111">Per impostazione predefinita, il tipo di messaggi scritti nel log include tutti gli eventi di livello di gravità 4 (informativo) o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="65b7c-111">By default, the type of messages that are written to the log include all events of severity level 4 (Informational) or higher.</span></span> <span data-ttu-id="65b7c-112">Il livello di gravità viene archiviato nel valore di chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="65b7c-112">The severity level is stored in the following key value.</span></span> <span data-ttu-id="65b7c-113">Impostare questo valore di chiave su 5 per abilitare la registrazione dettagliata.</span><span class="sxs-lookup"><span data-stu-id="65b7c-113">Set this key value to 5 to enable verbose logging.</span></span> <span data-ttu-id="65b7c-114">Usare la registrazione dettagliata solo per brevi periodi durante la risoluzione dei problemi perché genererà un volume molto elevato di messaggi e causerà il riempimento rapido del log.</span><span class="sxs-lookup"><span data-stu-id="65b7c-114">Use verbose logging only for short periods during troubleshooting because it will generate a very large volume of messages and cause the log to fill up quickly.</span></span>

    <span data-ttu-id="65b7c-115">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="65b7c-115">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span></span>

**<span data-ttu-id="65b7c-116">Per modificare le dimensioni del log</span><span class="sxs-lookup"><span data-stu-id="65b7c-116">To change the log size</span></span>**

-   <span data-ttu-id="65b7c-117">In Application Virtualization (App-V) 4,5 la dimensione del log è controllata dal valore della chiave del registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="65b7c-117">In Application Virtualization (App-V) 4.5, the log size is controlled by the following registry key value.</span></span> <span data-ttu-id="65b7c-118">Questo valore viene impostato su 256 MB e definisce le dimensioni massime, in MB, in cui il log può essere incrementato prima di essere reimpostato.</span><span class="sxs-lookup"><span data-stu-id="65b7c-118">This value defaults to 256MB and defines the maximum size, in MB, that the log can grow to before being reset.</span></span>

    <span data-ttu-id="65b7c-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="65b7c-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span></span>

    <span data-ttu-id="65b7c-120">**Attenzione**  Il valore della chiave del registro di sistema deve essere impostato su un valore maggiore di zero per verificare che il file di log venga reimpostato.</span><span class="sxs-lookup"><span data-stu-id="65b7c-120">**Caution** This registry key value must be set to a value greater than zero to ensure the log file does get reset.</span></span>

     

**<span data-ttu-id="65b7c-121">Per modificare il numero di copie di backup</span><span class="sxs-lookup"><span data-stu-id="65b7c-121">To change the number of backup copies</span></span>**

-   <span data-ttu-id="65b7c-122">Quando il file di log raggiunge la dimensione massima, viene forzata una reimpostazione quando si verifica la successiva scrittura nel log.</span><span class="sxs-lookup"><span data-stu-id="65b7c-122">When the log file reaches the maximum size, a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="65b7c-123">Un reset causa la creazione di un nuovo file di log e il vecchio file viene rinominato come backup.</span><span class="sxs-lookup"><span data-stu-id="65b7c-123">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span> <span data-ttu-id="65b7c-124">L'impostazione seguente del registro di sistema controlla il numero di copie di backup del file di log che vengono mantenute quando il file viene reimpostato.</span><span class="sxs-lookup"><span data-stu-id="65b7c-124">The following registry setting controls the number of backup copies of the log file that are kept when the file is reset.</span></span> <span data-ttu-id="65b7c-125">Il valore predefinito è 4.</span><span class="sxs-lookup"><span data-stu-id="65b7c-125">The default value is 4.</span></span>

    <span data-ttu-id="65b7c-126">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="65b7c-126">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span></span>

    <span data-ttu-id="65b7c-127">Il formato dei nomi di file di log di backup è: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** e si basa sul tempo di reimpostazione, in UTC (Universal Coordinated Time).</span><span class="sxs-lookup"><span data-stu-id="65b7c-127">The format of the backup log file names is: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** and is based on the reset time, in Universal Coordinated Time (UTC).</span></span> <span data-ttu-id="65b7c-128">La tabella seguente elenca i simboli usati per creare i nomi di file e le relative descrizioni.</span><span class="sxs-lookup"><span data-stu-id="65b7c-128">The following table lists the symbols used in creating the file names and their descriptions.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="65b7c-129">Simbolo</span><span class="sxs-lookup"><span data-stu-id="65b7c-129">Symbol</span></span></th>
    <th align="left"><span data-ttu-id="65b7c-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65b7c-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="65b7c-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="65b7c-131">YYYY</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65b7c-132">anno a quattro cifre</span><span class="sxs-lookup"><span data-stu-id="65b7c-132">4-digit year</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="65b7c-133">MM</span><span class="sxs-lookup"><span data-stu-id="65b7c-133">MM</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65b7c-134">mese a due cifre (01-12)</span><span class="sxs-lookup"><span data-stu-id="65b7c-134">2-digit month (01–12)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="65b7c-135">DD</span><span class="sxs-lookup"><span data-stu-id="65b7c-135">DD</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65b7c-136">giorno 2 cifre del mese (01 – 31)</span><span class="sxs-lookup"><span data-stu-id="65b7c-136">2-digit day of the month (01–31)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="65b7c-137">HH</span><span class="sxs-lookup"><span data-stu-id="65b7c-137">hh</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65b7c-138">ora (00-23)</span><span class="sxs-lookup"><span data-stu-id="65b7c-138">hour (00–23)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="65b7c-139">mm</span><span class="sxs-lookup"><span data-stu-id="65b7c-139">mm</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65b7c-140">minuti (00-59)</span><span class="sxs-lookup"><span data-stu-id="65b7c-140">minutes (00–59)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="65b7c-141">ss</span><span class="sxs-lookup"><span data-stu-id="65b7c-141">ss</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65b7c-142">secondi (00-59)</span><span class="sxs-lookup"><span data-stu-id="65b7c-142">seconds (00–59)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="65b7c-143">UUU</span><span class="sxs-lookup"><span data-stu-id="65b7c-143">uuu</span></span></p></td>
    <td align="left"><p><span data-ttu-id="65b7c-144">millisecondi (000-999)</span><span class="sxs-lookup"><span data-stu-id="65b7c-144">milliseconds (000–999)</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="65b7c-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65b7c-145">Related topics</span></span>


[<span data-ttu-id="65b7c-146">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="65b7c-146">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





