---
title: Elenco di controllo aggiornamento di App-V
description: Elenco di controllo aggiornamento di App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819736"
---
# <span data-ttu-id="2f8c6-103">Elenco di controllo aggiornamento di App-V</span><span class="sxs-lookup"><span data-stu-id="2f8c6-103">App-V Upgrade Checklist</span></span>


<span data-ttu-id="2f8c6-104">Prima di provare a eseguire l'aggiornamento a Microsoft Application Virtualization (App-V) 4,5 o versioni successive, è necessario aggiornare tutte le versioni precedenti a App-V 4,1 in App-V 4,1.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-104">Before trying to upgrade to Microsoft Application Virtualization (App-V) 4.5 or later versions, any version earlier than App-V 4.1 must be upgraded to App-V 4.1.</span></span> <span data-ttu-id="2f8c6-105">È consigliabile pianificare prima di tutto l'aggiornamento dei client e quindi aggiornare i componenti del server.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-105">You should plan to upgrade clients first, and then upgrade the server components.</span></span> <span data-ttu-id="2f8c6-106">I client App-V che sono stati aggiornati a App-V 4,5 continuano a funzionare con i server App-V che non sono ancora stati aggiornati.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-106">App-V clients that have been upgraded to App-V 4.5 continue to work with App-V servers that have not yet been upgraded.</span></span> <span data-ttu-id="2f8c6-107">Le versioni precedenti del client non sono supportate nei server che sono stati aggiornati a App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-107">Earlier versions of the client are not supported on servers that have been upgraded to App-V 4.5.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f8c6-108">Passaggio</span><span class="sxs-lookup"><span data-stu-id="2f8c6-108">Step</span></span></th>
<th align="left"><span data-ttu-id="2f8c6-109">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2f8c6-109">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-110">Aggiornare i client App-V.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-110">Upgrade the App-V clients.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)"><span data-ttu-id="2f8c6-111">Come aggiornare Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="2f8c6-111">How to Upgrade the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-112">Aggiornare i server e il database App-V.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-112">Upgrade the App-V servers and database.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="2f8c6-113">Importante</span><span class="sxs-lookup"><span data-stu-id="2f8c6-113">Important</span></span></strong><br/><p><span data-ttu-id="2f8c6-114">Se si dispone di più di un server di accesso alla condivisione del database App-V, è necessario che tutti i server vengano disattivati durante l'aggiornamento del database.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-114">If you have more than one server sharing access to the App-V database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="2f8c6-115">Devi seguire le normali procedure aziendali per l'aggiornamento del database, ma ti consigliamo di testare l'aggiornamento del database usando una copia di backup del database prima in un server di test.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-115">You should follow your regular business practices for the database upgrade, but we recommend that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="2f8c6-116">Devi quindi selezionare uno dei server per il primo aggiornamento, che aggiornerà lo schema del database.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="2f8c6-117">Dopo che il database di produzione è stato aggiornato correttamente, è possibile aggiornare il software App-V sugli altri server.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-117">After the production database has been successfully upgraded, you can upgrade the App-V software on the other servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="2f8c6-118">Come aggiornare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="2f8c6-118">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-119">Aggiornare il servizio Web di gestione App-V.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-119">Upgrade the App-V Management Web Service.</span></span></p>
<p><span data-ttu-id="2f8c6-120">Questo passaggio si applica solo se il servizio Web di gestione si trova in un server distinto, che richiede l'esecuzione del programma di installazione del server nel server separato per l'aggiornamento del servizio Web di gestione.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-120">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Management Web service.</span></span> <span data-ttu-id="2f8c6-121">In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà automaticamente il servizio Web di gestione.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-121">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="2f8c6-122">Come aggiornare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="2f8c6-122">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-123">Aggiornare la console di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-123">Upgrade the App-V Management Console.</span></span></p>
<p><span data-ttu-id="2f8c6-124">Questo passaggio si applica solo se la console di gestione si trova in un computer separato, per cui è necessario eseguire il programma di installazione del server in tale computer separato per aggiornare la console.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-124">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="2f8c6-125">In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-125">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="2f8c6-126">Come aggiornare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="2f8c6-126">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-127">Aggiornare l'App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-127">Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)"><span data-ttu-id="2f8c6-128">Come eseguire l'aggiornamento di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="2f8c6-128">How to Upgrade the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="2f8c6-129">Considerazioni aggiuntive sull'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2f8c6-129">Additional Upgrade Considerations</span></span>


-   <span data-ttu-id="2f8c6-130">Tutti i pacchetti di applicazioni virtuali sequenziati nella versione 4,2 non dovranno essere di nuovo sequenziati per l'uso con la versione 4,5.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-130">Any virtual application packages sequenced in version 4.2 will not have to be sequenced again for use with version 4.5.</span></span> <span data-ttu-id="2f8c6-131">Tuttavia, è consigliabile aggiornare i pacchetti virtuali al formato di Microsoft Application Virtualization 4,5 se si desidera applicare elenchi di controllo di accesso (ACL) predefiniti o generare un file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-131">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization 4.5 format if you want to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="2f8c6-132">Si tratta di un processo semplice e richiede solo che il pacchetto di applicazione virtuale esistente venga aperto e salvato con l'App-V 4,5 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-132">This is a simple process and requires only that the existing virtual application package be opened and saved with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="2f8c6-133">Questa operazione può essere automatizzata usando l'interfaccia della riga di comando App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-133">This can be automated by using the App-VSequencer command-line interface.</span></span> <span data-ttu-id="2f8c6-134">Per altre informazioni, vedere [come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span><span class="sxs-lookup"><span data-stu-id="2f8c6-134">For more information, see [How to Create or Upgrade Virtual Applications Using the App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span></span>

-   <span data-ttu-id="2f8c6-135">Una delle caratteristiche del sequencer di 4,5 è la possibilità di creare file di Windows Installer (con estensione msi) come punti di controllo per l'interoperabilità dei pacchetti di applicazioni virtuali con sistemi ESD (Electronic Software Distribution), come Microsoft endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-135">One of the features of the 4.5 Sequencer is the ability to create Windows Installer (.msi) files as control points for virtual application package interoperability with electronic software distribution (ESD) systems, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="2f8c6-136">I file di Windows Installer precedenti creati con lo strumento MSI per la virtualizzazione delle applicazioni installato in un client App-V 4,1 o 4,2 che viene successivamente aggiornato a App-V 4,5 continueranno a funzionare, anche se non possono essere installati nel client App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-136">Previous Windows Installer files created with the MSI tool for Application Virtualization that were installed on a App-V 4.1 or 4.2 client that is subsequently upgraded to App-V 4.5 will continue to work, although they cannot be installed on the App-V 4.5 client.</span></span> <span data-ttu-id="2f8c6-137">Tuttavia, non possono essere rimossi o aggiornati a meno che non vengano aggiornati nel sequencer di App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-137">However, they cannot be removed or upgraded unless they are upgraded in the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="2f8c6-138">Il pacchetto originale App-V precedente a 4,5 deve essere aperto nell'App-V 4,5 Sequencer e quindi salvato come file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-138">The original App-V package earlier than 4.5 has to be opened in the App-V 4.5 Sequencer and then saved as a Windows Installer File.</span></span>

    **<span data-ttu-id="2f8c6-139">Nota</span><span class="sxs-lookup"><span data-stu-id="2f8c6-139">Note</span></span>**  
    <span data-ttu-id="2f8c6-140">Se il client App-V 4,2 è già stato aggiornato a App-V 4,5, è possibile eseguire lo script di una soluzione alternativa per conservare i pacchetti della versione 4,2 nei client della versione 4,5 e consentire loro di gestirli.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-140">If the App-V 4.2 Client has already been upgraded to App-V 4.5, it is possible to script a workaround to preserve the version 4.2 packages on version 4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="2f8c6-141">Questo script deve copiare due file, msvcp71.dll e msvcr71.dll, nella cartella di installazione di App-V e impostare i valori della chiave del registro di sistema seguenti nella chiave del registro di sistema: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="2f8c6-141">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key:\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

    <span data-ttu-id="2f8c6-142">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="2f8c6-142">"ClientVersion"="4.2.1.20"</span></span>

    <span data-ttu-id="2f8c6-143">"GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (una posizione di scrittura globale)</span><span class="sxs-lookup"><span data-stu-id="2f8c6-143">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>



-   <span data-ttu-id="2f8c6-144">I file di Windows Installer generati dall'App-V 4,5 Sequencer visualizzano il messaggio di errore "questo pacchetto richiede Microsoft Application Virtualization Client 4,5 o versione successiva" quando si tenta di eseguirli in un client App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-144">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when trying to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="2f8c6-145">Aprire il vecchio pacchetto con l'App-V 4,5 SP1 Sequencer o l'App-V 4,6 Sequencer e generare un nuovo file MSI per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-145">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi file for the package.</span></span>

-   <span data-ttu-id="2f8c6-146">Tutti i report di versione 4,2 creati e salvati verranno sovrascritti quando il server viene aggiornato alla versione 4,5.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-146">Any version 4.2 reports that were created and saved will be overwritten when the server is upgraded to version 4.5.</span></span> <span data-ttu-id="2f8c6-147">Se è necessario conservare questi report, è necessario salvare una copia di backup del file SftMMC. msc che si trova nella cartella di SoftGrid Management Console nel server e usare tale copia per sostituire il nuovo SftMMC. msc installato durante l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-147">If you have to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

-   <span data-ttu-id="2f8c6-148">Per altre informazioni sull'aggiornamento dalle versioni precedenti, vedere [aggiornamento alle domande frequenti su Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="2f8c6-148">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="2f8c6-149">Supporto del pacchetto client App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="2f8c6-149">App-V 4.6 Client Package Support</span></span>


<span data-ttu-id="2f8c6-150">Puoi distribuire pacchetti creati in versioni precedenti di App-V ai client App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-150">You can deploy packages created in previous versions of App-V to App-V 4.6 clients.</span></span> <span data-ttu-id="2f8c6-151">È tuttavia necessario modificare il file OSD associato in modo che includa le informazioni appropriate per il sistema operativo e l'architettura di chip.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-151">However, you must modify the associated .osd file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="2f8c6-152">I valori seguenti possono essere usati:</span><span class="sxs-lookup"><span data-stu-id="2f8c6-152">The following values can be used:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f8c6-153">Valore OS</span><span class="sxs-lookup"><span data-stu-id="2f8c6-153">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-154">&lt;VALORE OS = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-154">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-155">&lt;VALORE OS = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-155">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-156">&lt;VALORE OS = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-156">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-157">&lt;VALORE OS = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-157">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-158">&lt;VALORE OS = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-158">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-159">&lt;VALORE OS = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-159">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-160">&lt;VALORE OS = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-160">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-161">&lt;VALORE OS = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-161">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-162">&lt;VALORE OS = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-162">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-163">&lt;VALORE OS = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-163">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-164">&lt;VALORE OS = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="2f8c6-164">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2f8c6-165">Per eseguire un pacchetto di 32 bit appena creato, è necessario sequenziare l'applicazione in un computer che esegue un sistema operativo a 32 bit con l'App-V 4,6 Sequencer installato.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-165">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V 4.6 Sequencer installed.</span></span> <span data-ttu-id="2f8c6-166">Dopo aver sequenziato l'applicazione, nella console Sequencer fare clic sulla scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-166">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

**<span data-ttu-id="2f8c6-167">Importante</span><span class="sxs-lookup"><span data-stu-id="2f8c6-167">Important</span></span>**  
<span data-ttu-id="2f8c6-168">Le applicazioni sequenziate in un computer che eseguono un sistema operativo a 64 bit devono essere distribuite nei computer che eseguono un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-168">Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="2f8c6-169">I nuovi pacchetti a 32 bit creati con l'App-V 4,6 Sequencer non vengono eseguiti nei computer che eseguono il client App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-169">New 32-bit packages created by using the App-V 4.6 Sequencer do not run on computers running the App-V 4.5 client.</span></span>



<span data-ttu-id="2f8c6-170">Per eseguire nuovi pacchetti di 64 bit nel client App-V 4,6, è necessario sequenziare l'applicazione in un computer che esegue App-V 4,6 Sequencer e che esegue un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-170">To run new 64-bit packages on the App-V 4.6 Client, you must sequence the application on a computer running the App-V 4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="2f8c6-171">Dopo aver sequenziato l'applicazione, nella console Sequencer fare clic sulla scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-171">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab, and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="2f8c6-172">La tabella seguente elenca le versioni client in cui verranno eseguiti i pacchetti creati con le varie versioni del sequencer.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-172">The following table lists which client versions will run packages created by using the various versions of the sequencer.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="2f8c6-173">Sequenziato tramite l'App-V 4,2 Sequencer</span><span class="sxs-lookup"><span data-stu-id="2f8c6-173">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="2f8c6-174">Sequenziato tramite l'App-V 4,5 Sequencer</span><span class="sxs-lookup"><span data-stu-id="2f8c6-174">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="2f8c6-175">Sequenziato tramite l'app 32 bit-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="2f8c6-175">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="2f8c6-176">Sequenziato tramite l'app 64 bit-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="2f8c6-176">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-177">Client di 4,2</span><span class="sxs-lookup"><span data-stu-id="2f8c6-177">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-178">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-179">No</span><span class="sxs-lookup"><span data-stu-id="2f8c6-179">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-180">No</span><span class="sxs-lookup"><span data-stu-id="2f8c6-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-181">No</span><span class="sxs-lookup"><span data-stu-id="2f8c6-181">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-182">4,5 client ¹</span><span class="sxs-lookup"><span data-stu-id="2f8c6-182">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-183">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-184">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-185">No</span><span class="sxs-lookup"><span data-stu-id="2f8c6-185">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-186">No</span><span class="sxs-lookup"><span data-stu-id="2f8c6-186">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f8c6-187">Client di 4,6 (32 bit)</span><span class="sxs-lookup"><span data-stu-id="2f8c6-187">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-188">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-189">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-190">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-191">No</span><span class="sxs-lookup"><span data-stu-id="2f8c6-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f8c6-192">Client di 4,6 (64 bit)</span><span class="sxs-lookup"><span data-stu-id="2f8c6-192">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-193">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-194">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-194">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-195">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f8c6-196">Sì</span><span class="sxs-lookup"><span data-stu-id="2f8c6-196">Yes</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="2f8c6-197">¹ si applica a tutte le versioni del client App-V 4,5, tra cui App-V 4,5, App-V 4,5 CU1 e App-V 4,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="2f8c6-197">¹Applies to all versions of the App-V 4.5 client, including App-V 4.5, App-V 4.5 CU1, and App-V 4.5 SP1.</span></span>









