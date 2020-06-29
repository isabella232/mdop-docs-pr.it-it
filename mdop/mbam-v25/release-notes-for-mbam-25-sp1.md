---
title: Note sulla versione di MBAM 2.5 SP1
description: Note sulla versione di MBAM 2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824986"
---
# <span data-ttu-id="26004-103">Note sulla versione di MBAM 2.5 SP1</span><span class="sxs-lookup"><span data-stu-id="26004-103">Release Notes for MBAM 2.5 SP1</span></span>


<span data-ttu-id="26004-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="26004-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="26004-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="26004-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 SP1.</span></span> <span data-ttu-id="26004-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente MBAM e possono contenere informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="26004-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="26004-107">Se queste note sulla versione si differenziano da altre documentazioni di MBAM 2,5 SP1, tenere presente che la modifica più recente è autorevole.</span><span class="sxs-lookup"><span data-stu-id="26004-107">If these release notes differ from other MBAM 2.5 SP1 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="26004-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="26004-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> <span data-ttu-id="26004-109">Problemi noti di MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="26004-109">MBAM 2.5 SP1 known issues</span></span>


<span data-ttu-id="26004-110">Questa sezione contiene le note sulla versione per MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="26004-110">This section contains release notes for MBAM 2.5 SP1.</span></span>

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a><span data-ttu-id="26004-111">I cmdlet di PowerShell Read-AD \ \* non consentono di inviare commenti e suggerimenti se l'utente non dispone di diritti sufficienti</span><span class="sxs-lookup"><span data-stu-id="26004-111">PowerShell Read-AD\* cmdlets do not provide feedback if user does not have sufficient rights</span></span>

<span data-ttu-id="26004-112">Se un utente che prova a usare i cmdlet di PowerShell Read-AD \ \* per il server MBAM non ha diritti utente per leggere le informazioni di ripristino di Active Directory o per leggere le informazioni sul TPM, i cmdlet non forniranno all'utente alcun errore o avviso.</span><span class="sxs-lookup"><span data-stu-id="26004-112">If a user trying to use the PowerShell Read-AD\* cmdlets for the MBAM Server does not have user rights to read the Active Directory recovery information or to read the TPM information, the cmdlets will not provide the user with any error or warning.</span></span>

<span data-ttu-id="26004-113">**Soluzione alternativa:** Usare i cmdlet di PowerShell Read-AD \ \* solo se si hanno i diritti utente necessari.</span><span class="sxs-lookup"><span data-stu-id="26004-113">**Workaround:** Only use the PowerShell Read-AD\* cmdlets if you have the required user rights.</span></span>

### <span data-ttu-id="26004-114">I cmdlet di migrazione di MBAM Active Directory (AD) non recuperano le informazioni sul ripristino del volume</span><span class="sxs-lookup"><span data-stu-id="26004-114">MBAM Active Directory (AD) Migration cmdlets do not retrieve volume recovery information</span></span>

<span data-ttu-id="26004-115">I cmdlet di migrazione di MBAM Active Directory (AD) non riescono a recuperare le informazioni di ripristino del volume per i computer in unità organizzative (OU) se il carattere barra (/) fa parte del nome dell'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="26004-115">MBAM Active Directory (AD) Migration cmdlets fail to retrieve volume recovery information for computers in organizational units (OUs) if the forward slash character (/) is part of the OU name.</span></span> <span data-ttu-id="26004-116">Le estrazioni degli annunci ripetute avranno esito negativo con un errore di terminazione della pipeline quando viene rilevato questo errore.</span><span class="sxs-lookup"><span data-stu-id="26004-116">Repeated AD pulls will fail with a pipeline terminating error when this error is encountered.</span></span>

<span data-ttu-id="26004-117">**Dettagli tecnici:** Questo errore verrà visualizzato quando si eseguirà il comando:</span><span class="sxs-lookup"><span data-stu-id="26004-117">**Technical Details:** You will see this error when running the command:</span></span>

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

<span data-ttu-id="26004-118">Inoltre, l'analisi dello stack dell'eccezione `Error[0].Exception.StackTrace` avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="26004-118">In addition, the Exception stack trace `Error[0].Exception.StackTrace` will look like this:</span></span>

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

<span data-ttu-id="26004-119">**Soluzione alternativa:** Eseguire una di queste attività per risolvere la situazione:</span><span class="sxs-lookup"><span data-stu-id="26004-119">**Workaround:** Perform one of these tasks to resolve this situation:</span></span>

-   <span data-ttu-id="26004-120">Rinominare l'unità organizzativa per rimuovere il carattere barra di inoltro e quindi eseguire lo script.</span><span class="sxs-lookup"><span data-stu-id="26004-120">Rename the OU to remove the forward slash character and then run the script.</span></span>

-   <span data-ttu-id="26004-121">Per escludere un'unità organizzativa problematica dal processo di backup, trovare un elenco delle unità organizzative i cui nomi non contengono il carattere barra di inoltro.</span><span class="sxs-lookup"><span data-stu-id="26004-121">To exclude any problematic OU from the backup process, find a list of OUs whose names do not contain the forward slash character.</span></span> <span data-ttu-id="26004-122">Eseguire lo script in queste unità organizzative, una OU alla volta.</span><span class="sxs-lookup"><span data-stu-id="26004-122">Run the script on these OUs, one OU at a time.</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="26004-123">MBAM non riesce a crittografare un volume e segnala un errore se si imposta una protezione TPM + PIN in un dispositivo Tablet</span><span class="sxs-lookup"><span data-stu-id="26004-123">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="26004-124">Se gli utenti finali provano a impostare una protezione TPM + PIN in un dispositivo tablet, MBAM non riesce a crittografare e segnala un errore.</span><span class="sxs-lookup"><span data-stu-id="26004-124">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="26004-125">Questo problema si verifica perché i dispositivi tablet non dispongono di una tastiera dell'ambiente di avvio preliminare.</span><span class="sxs-lookup"><span data-stu-id="26004-125">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="26004-126">**Soluzione alternativa:** Abilitare l' **uso dell'autenticazione di BitLocker che richiede l'immissione di Preboot da tastiera nell'impostazione di criteri di gruppo Tablet** .</span><span class="sxs-lookup"><span data-stu-id="26004-126">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="26004-127">Questa impostazione è un'impostazione di criteri di gruppo di BitLocker e non è disponibile nei modelli di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="26004-127">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="26004-128">Il nome dell'entità utente è obbligatorio per tutti gli account del servizio</span><span class="sxs-lookup"><span data-stu-id="26004-128">User principal name is required for all service accounts</span></span>

<span data-ttu-id="26004-129">Il nome dell'entità utente (UPN) deve essere impostato per tutti gli account del servizio in MBAM.</span><span class="sxs-lookup"><span data-stu-id="26004-129">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="26004-130">Se non si riesce a creare un UPN per un account, durante il processo di configurazione viene visualizzato un messaggio di errore che indica che non è stato possibile trovare l'utente o il gruppo in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26004-130">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="26004-131">**Soluzione alternativa:** Aggiungere l'UPN all'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="26004-131">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="26004-132">Il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono dopo l'aggiornamento di IIS a .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="26004-132">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="26004-133">Quando si aggiorna Internet Information Services (IIS) a Microsoft .NET Framework 4,5, il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono.</span><span class="sxs-lookup"><span data-stu-id="26004-133">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="26004-134">**Soluzione alternativa:** Vedere l'articolo [messaggio di errore dopo l'installazione di .NET Framework 4,0: "Impossibile caricare il tipo" System. ServiceModel. Activation. HttpModule "](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="26004-134">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="26004-135">Il sito Web di amministrazione e monitoraggio Visualizza un messaggio di errore "Impossibile trovare il report" quando i report non sono configurati</span><span class="sxs-lookup"><span data-stu-id="26004-135">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="26004-136">Se si configura il sito Web amministrazione e monitoraggio e quindi si prova a visualizzare un report senza configurare prima la caratteristica report, viene visualizzato un messaggio di errore che indica che non è possibile trovare il report.</span><span class="sxs-lookup"><span data-stu-id="26004-136">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="26004-137">**Soluzione alternativa:** Configurare la caratteristica report prima di configurare le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="26004-137">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="26004-138">I report nel sito Web amministrazione e monitoraggio visualizzano un avviso se SSL non è configurato in SSRS</span><span class="sxs-lookup"><span data-stu-id="26004-138">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="26004-139">Se SQL Server Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL della caratteristica report verrà impostato su HTTP anziché su HTTPS quando si configura il server MBAM.</span><span class="sxs-lookup"><span data-stu-id="26004-139">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="26004-140">Se si apre il sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio di errore seguente: "viene visualizzato solo il contenuto protetto".</span><span class="sxs-lookup"><span data-stu-id="26004-140">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="26004-141">**Soluzione alternativa:** Per visualizzare il report, fare clic su **Mostra tutto il contenuto**.</span><span class="sxs-lookup"><span data-stu-id="26004-141">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="26004-142">Per risolvere il problema, passare al computer MBAM in cui è installato SQL Server Reporting Services, eseguire **Gestione configurazione di Reporting Services**e quindi fare clic su **URL servizio Web**.</span><span class="sxs-lookup"><span data-stu-id="26004-142">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="26004-143">Selezionare il certificato SSL appropriato per il server, immettere la porta SSL appropriata (la porta predefinita è 443) e quindi fare clic su **applica**.</span><span class="sxs-lookup"><span data-stu-id="26004-143">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="26004-144">Se si fa clic su "back" nel report Riepilogo conformità di BitLocker, potrebbe essere generato un errore</span><span class="sxs-lookup"><span data-stu-id="26004-144">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="26004-145">Se si esegue il drill-down in un report di riepilogo conformità di BitLocker e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe essere generato un errore.</span><span class="sxs-lookup"><span data-stu-id="26004-145">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="26004-146">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="26004-146">**Workaround:** None.</span></span>

### <span data-ttu-id="26004-147">La forza di crittografia viene visualizzata in modo non corretto nel report conformità computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="26004-147">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="26004-148">Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo forza di crittografia, il report conformità computer BitLocker nella topologia di integrazione di Configuration Manager Visualizza sempre "sconosciuto" per il livello di cifratura, anche quando l'intensità della cifratura usa l'impostazione predefinita della crittografia a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="26004-148">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="26004-149">Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="26004-149">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="26004-150">**Soluzione alternativa:** Imposta sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di crittografia.</span><span class="sxs-lookup"><span data-stu-id="26004-150">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="26004-151">La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="26004-151">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="26004-152">Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="26004-152">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="26004-153">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="26004-153">**Workaround:** None.</span></span> <span data-ttu-id="26004-154">La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.</span><span class="sxs-lookup"><span data-stu-id="26004-154">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="26004-155">La configurazione di sicurezza avanzata può causare la visualizzazione errata di un messaggio di errore</span><span class="sxs-lookup"><span data-stu-id="26004-155">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="26004-156">Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM.</span><span class="sxs-lookup"><span data-stu-id="26004-156">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="26004-157">Per impostazione predefinita, ESC è attivato per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="26004-157">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="26004-158">**Soluzione alternativa:** Se viene visualizzato il messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="26004-158">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="26004-159">È anche possibile visualizzare in alternativa i report di un altro computer in cui ESC non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="26004-159">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="26004-160">Supporto per l'algoritmo di crittografia BitLocker XTS-AES</span><span class="sxs-lookup"><span data-stu-id="26004-160">Support for Bitlocker XTS-AES encryption algorithm</span></span>
<span data-ttu-id="26004-161">BitLocker ha aggiunto il supporto per l'algoritmo di crittografia XTS-AES in Windows 10, versione 1511.</span><span class="sxs-lookup"><span data-stu-id="26004-161">Bitlocker added support for the XTS-AES encryption algorithm in Windows 10, version 1511.</span></span> <span data-ttu-id="26004-162">Con HF02, MBAM ha aggiunto il supporto client per l'opzione BitLocker e in HF04 è stato aggiunto il supporto lato server.</span><span class="sxs-lookup"><span data-stu-id="26004-162">With HF02, MBAM added client support for this Bitlocker option and in HF04, the server-side support was added.</span></span> <span data-ttu-id="26004-163">Tuttavia, esiste un limite noto:</span><span class="sxs-lookup"><span data-stu-id="26004-163">However, there is one known limitation:</span></span>

* <span data-ttu-id="26004-164">I clienti devono usare la stessa forza di crittografia per il sistema operativo e i volumi di dati nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="26004-164">Customers must use the same encryption strength for OS and data volumes on the same machine.</span></span>
<span data-ttu-id="26004-165">Se vengono usati diversi punti di forza per la crittografia, MBAM riporterà la macchina come **non conforme**.</span><span class="sxs-lookup"><span data-stu-id="26004-165">If different encryption strengths are used, MBAM will report the machine as **non-compliant**.</span></span>

### <span data-ttu-id="26004-166">Il portale self-service aggiunge automaticamente "-" alla voce ID chiave</span><span class="sxs-lookup"><span data-stu-id="26004-166">Self-Service Portal automatically adds "-" on Key ID entry</span></span>
<span data-ttu-id="26004-167">A partire da HF02, il portale self-service di MBAM aggiunge automaticamente la voce "-" all'ID chiave.</span><span class="sxs-lookup"><span data-stu-id="26004-167">As of HF02, the MBAM Self-Service Portal automatically adds the '-' on Key ID entry.</span></span>  
<span data-ttu-id="26004-168">**Nota:** Il server deve essere riconfigurato per il fatto che il codice JavaScript abbia effetto.</span><span class="sxs-lookup"><span data-stu-id="26004-168">**Note:** The Server has to be reconfigured for the Javascript to take effect.</span></span>

### <span data-ttu-id="26004-169">I report di MBAM 2,5 SP1 non funzionano/eseguono correttamente il rendering</span><span class="sxs-lookup"><span data-stu-id="26004-169">MBAM 2.5 Sp1 Reports does not work / render properly</span></span>
<span data-ttu-id="26004-170">La pagina report non esegue il rendering correttamente quando SSRS è ospitato in SQL Server 2016 Edition.</span><span class="sxs-lookup"><span data-stu-id="26004-170">Reports Page does not render properly when SSRS is hosted on SQL Server 2016 edition.</span></span> 
<span data-ttu-id="26004-171">Ad esempio, passando all'helpdesk-facendo clic sui report-(la parte evidenziata contiene "x" su di essa), questa operazione viene ulteriormente eseguita con Fiddler, che ha l'aspetto di una volta che si fa clic su report, che chiama la pagina SSRS con il formato di rendering HTML 4,0.</span><span class="sxs-lookup"><span data-stu-id="26004-171">For example – Browsing to Helpdesk – Clicking on Reports – ( Highlighted portion have “x” on it ) Digging this further with Fiddler – it does look like once we click on Reports – it calls the SSRS page with HTML 4.0 rendering format.</span></span>

<span data-ttu-id="26004-172">**Soluzione alternativa:** Guardando il codice sito. master e notato che la modalità X-UA è stata dettata come IE8.</span><span class="sxs-lookup"><span data-stu-id="26004-172">**Workaround:** Looking at the site.master code and noticed the X-UA mode was dictated as IE8.</span></span> <span data-ttu-id="26004-173">Il modo in cui IE8 supera la fine della vita e il cliente usa IE11.</span><span class="sxs-lookup"><span data-stu-id="26004-173">As IE8 is WAY past the end of life, and customer is using IE11.</span></span> <span data-ttu-id="26004-174">Aggiornare l'impostazione al codice seguente.</span><span class="sxs-lookup"><span data-stu-id="26004-174">Update the setting to the below code.</span></span> <span data-ttu-id="26004-175">Questo consente al sito di usare le tecnologie di rendering di IE11</span><span class="sxs-lookup"><span data-stu-id="26004-175">This allows the site to utilize IE11 rendering technologies</span></span>

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

<span data-ttu-id="26004-176">L'impostazione originale è:</span><span class="sxs-lookup"><span data-stu-id="26004-176">Original setting is:</span></span> 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


<span data-ttu-id="26004-177">Questo è il motivo per cui il problema non è stato visto con altri browser come Chrome, Firefox e così via.</span><span class="sxs-lookup"><span data-stu-id="26004-177">This is the reason why the issue was not seen with other browsers like Chrome, Firefox etc.</span></span>



## <span data-ttu-id="26004-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26004-178">Related topics</span></span>


[<span data-ttu-id="26004-179">Informazioni su MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="26004-179">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="26004-180">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="26004-180">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="26004-181">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="26004-181">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="26004-182">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="26004-182">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





