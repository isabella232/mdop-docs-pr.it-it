---
title: Note sulla versione di MBAM 2.5
description: Note sulla versione di MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824985"
---
# <span data-ttu-id="d5f8d-103">Note sulla versione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5f8d-103">Release Notes for MBAM 2.5</span></span>


<span data-ttu-id="d5f8d-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="d5f8d-105">Leggere queste note sulla versione accuratamente prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM) 2.5.</span></span> <span data-ttu-id="d5f8d-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente MBAM e possono contenere informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-106">These release notes contain information that is required to successfully install MBAM and can contain information that is not available in the product documentation.</span></span> <span data-ttu-id="d5f8d-107">Se queste note sulla versione differiscono da altre documentazioni di MBAM 2,5, tenere presente che la modifica più recente è autorevole.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-107">If these release notes differ from other MBAM 2.5 documentation, consider the latest change to be authoritative.</span></span> <span data-ttu-id="d5f8d-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-5-known-issues"></a> <span data-ttu-id="d5f8d-109">Problemi noti di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="d5f8d-109">MBAM 2.5 known issues</span></span>


<span data-ttu-id="d5f8d-110">Questa sezione contiene le note sulla versione per MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-110">This section contains release notes for MBAM 2.5.</span></span>

### <span data-ttu-id="d5f8d-111">Web browser eseguito involontariamente come amministratore</span><span class="sxs-lookup"><span data-stu-id="d5f8d-111">Web browser unintentionally run as administrator</span></span>

<span data-ttu-id="d5f8d-112">I collegamenti della guida nello strumento di configurazione di MBAM server possono causare l'apertura delle finestre del browser con i diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-112">Help links in the MBAM Server Configuration tool can cause browser windows to open with administrator rights.</span></span>

<span data-ttu-id="d5f8d-113">**Soluzione alternativa:** Abilitare la configurazione di sicurezza avanzata di Internet Explorer (IESC) o chiudere il Web browser prima di spostarsi in altri siti.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-113">**Workaround:** Enable Internet Explorer Enhanced Security Configuration (IESC) or close your web browser before navigating to other sites.</span></span>

<span data-ttu-id="d5f8d-114">**Nota**  Questo problema è stato risolto in MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-114">**Note** This is fixed in MBAM 2.5 SP1.</span></span>

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> <span data-ttu-id="d5f8d-115">I report di MBAM sono conformi ai client crittografati con le chiavi di crittografia e il diffusore AES a 256 bit</span><span class="sxs-lookup"><span data-stu-id="d5f8d-115">MBAM reports as noncompliant a client encrypted with AES 256-bit encryption keys and Diffuser</span></span>

<span data-ttu-id="d5f8d-116">Se un computer ha installato il client MBAM 2,5 e viene crittografato usando l'AES 256 bit con la forza di cifratura del diffusore, il client MBAM viene segnalato come non conforme nei report di conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-116">If a computer has the MBAM 2.5 client installed and is encrypted by using the AES 256-bit with Diffuser cipher strength, the MBAM client is reported as noncompliant in the MBAM compliance reports.</span></span>

<span data-ttu-id="d5f8d-117">**Soluzione alternativa:** Installare l'hotfix su [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span><span class="sxs-lookup"><span data-stu-id="d5f8d-117">**Workaround:** Install the hotfix at [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).</span></span>

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> <span data-ttu-id="d5f8d-118">MBAM non riesce a crittografare un volume e segnala un errore se si imposta una protezione TPM + PIN in un dispositivo Tablet</span><span class="sxs-lookup"><span data-stu-id="d5f8d-118">MBAM fails to encrypt a volume and reports an error if you set a TPM + PIN protector on a tablet device</span></span>

<span data-ttu-id="d5f8d-119">Se gli utenti finali provano a impostare una protezione TPM + PIN in un dispositivo tablet, MBAM non riesce a crittografare e segnala un errore.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-119">If end users try to set a TPM + PIN protector on a tablet device, MBAM fails to encrypt, and it reports an error.</span></span> <span data-ttu-id="d5f8d-120">Questo problema si verifica perché i dispositivi tablet non dispongono di una tastiera dell'ambiente di avvio preliminare.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-120">This issue occurs because tablet devices do not have a pre-boot environment keyboard.</span></span>

<span data-ttu-id="d5f8d-121">**Soluzione alternativa:** Abilitare l' **uso dell'autenticazione di BitLocker che richiede l'immissione di Preboot da tastiera nell'impostazione di criteri di gruppo Tablet** .</span><span class="sxs-lookup"><span data-stu-id="d5f8d-121">**Workaround:** Enable the **Enable use of BitLocker authentication requiring preboot keyboard input on tablets** Group Policy setting.</span></span> <span data-ttu-id="d5f8d-122">Questa impostazione è un'impostazione di criteri di gruppo di BitLocker e non è disponibile nei modelli di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-122">This setting is a BitLocker Group Policy setting and is not available in the MBAM Group Policy Templates.</span></span>

### <span data-ttu-id="d5f8d-123">Il nome dell'entità utente è obbligatorio per tutti gli account del servizio</span><span class="sxs-lookup"><span data-stu-id="d5f8d-123">User principal name is required for all service accounts</span></span>

<span data-ttu-id="d5f8d-124">Il nome dell'entità utente (UPN) deve essere impostato per tutti gli account del servizio in MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-124">A user principal name (UPN) must be set for all service accounts in MBAM.</span></span> <span data-ttu-id="d5f8d-125">Se non si riesce a creare un UPN per un account, durante il processo di configurazione viene visualizzato un messaggio di errore che indica che non è stato possibile trovare l'utente o il gruppo in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-125">If you fail to create a UPN for an account, an error message appears during the configuration process to indicate that the user or group could not be found in Active Directory.</span></span>

<span data-ttu-id="d5f8d-126">**Soluzione alternativa:** Aggiungere l'UPN all'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-126">**Workaround:** Add the UPN to the service account.</span></span>

### <span data-ttu-id="d5f8d-127">Il portale self-service richiede una configurazione aggiuntiva se i computer client non possono accedere alla rete di distribuzione del contenuto Microsoft AJAX</span><span class="sxs-lookup"><span data-stu-id="d5f8d-127">Self-Service Portal requires additional configuration if client computers cannot access Microsoft Ajax Content Delivery Network</span></span>

<span data-ttu-id="d5f8d-128">Se i computer client non hanno accesso alla rete CDN (Microsoft AJAX Content Delivery Network), che fornisce al portale self-service l'accesso necessario per determinati file JavaScript, è necessario configurare il portale self-service in modo che faccia riferimento ai file JavaScript da un'origine accessibile.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-128">If your client computers do not have access to the Microsoft Ajax Content Delivery Network (CDN), which gives the Self-Service Portal the access that it requires to certain JavaScript files, you must configure the Self-Service Portal to reference the JavaScript files from an accessible source.</span></span> <span data-ttu-id="d5f8d-129">Se non si configura il portale self-service quando i computer client non riescono ad accedere alla rete CDN, viene visualizzato solo il nome della società e l'account in cui è stato effettuato l'accesso.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-129">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which you logged on is displayed.</span></span> <span data-ttu-id="d5f8d-130">Non viene visualizzato alcun messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-130">No error message appears.</span></span>

<span data-ttu-id="d5f8d-131">**Soluzione alternativa:** Installare MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-131">**Workaround:** Install MBAM 2.5 SP1.</span></span> <span data-ttu-id="d5f8d-132">o configura il portale self-service seguendo queste istruzioni: [come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione del contenuto Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span><span class="sxs-lookup"><span data-stu-id="d5f8d-132">or configure the Self-Service Portal by following these instructions: [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).</span></span>

### <span data-ttu-id="d5f8d-133">Il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono dopo l'aggiornamento di IIS a .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="d5f8d-133">Self-Service Portal and the Administration and Monitoring Website do not open after you upgrade IIS to .NET Framework 4.5</span></span>

<span data-ttu-id="d5f8d-134">Quando si aggiorna Internet Information Services (IIS) a Microsoft .NET Framework 4,5, il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-134">When you upgrade Internet Information Services (IIS) to the Microsoft .NET Framework 4.5, the Self-Service Portal and the Administration and Monitoring Website do not open.</span></span>

<span data-ttu-id="d5f8d-135">**Soluzione alternativa:** Vedere l'articolo [messaggio di errore dopo l'installazione di .NET Framework 4,0: "Impossibile caricare il tipo" System. ServiceModel. Activation. HttpModule "](https://go.microsoft.com/fwlink/?LinkId=393568).</span><span class="sxs-lookup"><span data-stu-id="d5f8d-135">**Workaround:** See the article [Error message after you install the .NET Framework 4.0: "Could not load type 'System.ServiceModel.Activation.HttpModule'](https://go.microsoft.com/fwlink/?LinkId=393568).</span></span>

### <span data-ttu-id="d5f8d-136">Il sito Web di amministrazione e monitoraggio Visualizza un messaggio di errore "Impossibile trovare il report" quando i report non sono configurati</span><span class="sxs-lookup"><span data-stu-id="d5f8d-136">Administration and Monitoring Website displays a "Report cannot be found" error message when Reports are not configured</span></span>

<span data-ttu-id="d5f8d-137">Se si configura il sito Web amministrazione e monitoraggio e quindi si prova a visualizzare un report senza configurare prima la caratteristica report, viene visualizzato un messaggio di errore che indica che non è possibile trovare il report.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-137">If you configure the Administration and Monitoring Website and then try to view a report without configuring the Reports feature first, an error message indicates that the report cannot be found.</span></span>

<span data-ttu-id="d5f8d-138">**Soluzione alternativa:** Configurare la caratteristica report prima di configurare le applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-138">**Workaround:** Configure the Reports feature before you configure the web applications.</span></span>

### <span data-ttu-id="d5f8d-139">I report nel sito Web amministrazione e monitoraggio visualizzano un avviso se SSL non è configurato in SSRS</span><span class="sxs-lookup"><span data-stu-id="d5f8d-139">Reports in the Administration and Monitoring Website display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="d5f8d-140">Se SQL Server Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL della caratteristica report verrà impostato su HTTP anziché su HTTPS quando si configura il server MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-140">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the Reports feature will be set to HTTP instead of to HTTPS when you configure the MBAM Server.</span></span> <span data-ttu-id="d5f8d-141">Se si apre il sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio di errore seguente: "viene visualizzato solo il contenuto protetto".</span><span class="sxs-lookup"><span data-stu-id="d5f8d-141">If you then open the Administration and Monitoring Website and select a report, the following error message appears: "Only Secure Content is Displayed."</span></span>

<span data-ttu-id="d5f8d-142">**Soluzione alternativa:** Per visualizzare il report, fare clic su **Mostra tutto il contenuto**.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-142">**Workaround:** To show the report, click **Show All Content**.</span></span> <span data-ttu-id="d5f8d-143">Per risolvere il problema, passare al computer MBAM in cui è installato SQL Server Reporting Services, eseguire **Gestione configurazione di Reporting Services**e quindi fare clic su **URL servizio Web**.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-143">To correct this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="d5f8d-144">Selezionare il certificato SSL appropriato per il server, immettere la porta SSL appropriata (la porta predefinita è 443) e quindi fare clic su **applica**.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-144">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="d5f8d-145">Se si fa clic su "back" nel report Riepilogo conformità di BitLocker, potrebbe essere generato un errore</span><span class="sxs-lookup"><span data-stu-id="d5f8d-145">Clicking "Back" in the BitLocker Compliance Summary report might throw an error</span></span>

<span data-ttu-id="d5f8d-146">Se si esegue il drill-down in un report di riepilogo conformità di BitLocker e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe essere generato un errore.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-146">If you drill down into a BitLocker Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="d5f8d-147">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-147">**Workaround:** None.</span></span>

### <span data-ttu-id="d5f8d-148">Solo spazio usato la crittografia non funziona correttamente</span><span class="sxs-lookup"><span data-stu-id="d5f8d-148">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="d5f8d-149">Se si crittografa un computer per la prima volta dopo l'installazione del client MBAM e si è configurata un'impostazione di criteri di gruppo per implementare la crittografia solo spazio usato, MBAM crittografa erroneamente l'intero disco invece di crittografare solo lo spazio usato del disco.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-149">If you encrypt a computer for the first time after you install the MBAM Client, and you have configured a Group Policy setting to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="d5f8d-150">Se un computer è già crittografato con lo spazio usato solo quando si installa il client MBAM e si è configurata la stessa impostazione di criteri di gruppo, MBAM segnala che l'unità è crittografata correttamente e non tenta di ricrittografare l'unità.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-150">If a computer is already encrypted with Used Space Only when you install the MBAM Client, and you have configured the same Group Policy setting, MBAM reports that the drive is encrypted correctly, and does not try to re-encrypt the drive.</span></span>

<span data-ttu-id="d5f8d-151">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-151">**Workaround:** None.</span></span>

### <span data-ttu-id="d5f8d-152">La forza di crittografia viene visualizzata in modo non corretto nel report conformità computer BitLocker</span><span class="sxs-lookup"><span data-stu-id="d5f8d-152">Cipher strength displays incorrectly on the BitLocker Computer Compliance report</span></span>

<span data-ttu-id="d5f8d-153">Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo forza di crittografia, il report conformità computer BitLocker nella topologia di integrazione di Configuration Manager Visualizza sempre "sconosciuto" per il livello di cifratura, anche quando l'intensità della cifratura usa l'impostazione predefinita della crittografia a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-153">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the BitLocker Computer Compliance report in the Configuration Manager Integration topology always displays "unknown" for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="d5f8d-154">Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-154">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="d5f8d-155">**Soluzione alternativa:** Imposta sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di crittografia.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-155">**Workaround:** Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="d5f8d-156">La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="d5f8d-156">Compliance Status Distribution by Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="d5f8d-157">Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-157">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="d5f8d-158">**Soluzione alternativa:** Nessuno.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-158">**Workaround:** None.</span></span> <span data-ttu-id="d5f8d-159">La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-159">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="d5f8d-160">La configurazione di sicurezza avanzata può causare la visualizzazione errata di un messaggio di errore</span><span class="sxs-lookup"><span data-stu-id="d5f8d-160">Enhanced Security Configuration might cause reports to display an error message incorrectly</span></span>

<span data-ttu-id="d5f8d-161">Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-161">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an "Access Denied" error message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="d5f8d-162">Per impostazione predefinita, ESC è attivato per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-162">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="d5f8d-163">**Soluzione alternativa:** Se viene visualizzato il messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-163">**Workaround:** If the "Access Denied" error message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="d5f8d-164">È anche possibile visualizzare in alternativa i report di un altro computer in cui ESC non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-164">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a><span data-ttu-id="d5f8d-165">Aggiornamenti rapidi e articoli della Knowledge base per MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="d5f8d-165">Hotfixes and Knowledge Base articles for MBAM 2.5</span></span>


<span data-ttu-id="d5f8d-166">Questa tabella elenca gli articoli relativi a hotfix e KB per MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="d5f8d-166">This table lists the hotfixes and KB articles for MBAM 2.5.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="d5f8d-167">Articolo KB</span><span class="sxs-lookup"><span data-stu-id="d5f8d-167">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="d5f8d-168">Title</span><span class="sxs-lookup"><span data-stu-id="d5f8d-168">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="d5f8d-169">Link</span><span class="sxs-lookup"><span data-stu-id="d5f8d-169">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5f8d-170">2975636</span><span class="sxs-lookup"><span data-stu-id="d5f8d-170">2975636</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5f8d-171">Pacchetto hotfix 1 per l'amministrazione e il monitoraggio di Microsoft BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="d5f8d-171">Hotfix Package 1 for Microsoft BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)"><span data-ttu-id="d5f8d-172">support.microsoft.com/kb/2975636/EN-US</span><span class="sxs-lookup"><span data-stu-id="d5f8d-172">support.microsoft.com/kb/2975636/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5f8d-173">3015477</span><span class="sxs-lookup"><span data-stu-id="d5f8d-173">3015477</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5f8d-174">Pacchetto hotfix 2 per l'amministrazione e il monitoraggio di BitLocker 2,5</span><span class="sxs-lookup"><span data-stu-id="d5f8d-174">Hotfix Package 2 for BitLocker Administration and Monitoring 2.5</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)"><span data-ttu-id="d5f8d-175">support.microsoft.com/kb/3015477</span><span class="sxs-lookup"><span data-stu-id="d5f8d-175">support.microsoft.com/kb/3015477</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5f8d-176">3011022</span><span class="sxs-lookup"><span data-stu-id="d5f8d-176">3011022</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5f8d-177">I report di installazione o Gestione configurazione di MBAM 2,5 non riescono se il nome dell'istanza SSRS contiene un carattere di sottolineatura</span><span class="sxs-lookup"><span data-stu-id="d5f8d-177">MBAM 2.5 installation or Configuration Manager reporting fails if the name of SSRS instance contains an underscore</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)"><span data-ttu-id="d5f8d-178">support.microsoft.com/kb/3011022/EN-US</span><span class="sxs-lookup"><span data-stu-id="d5f8d-178">support.microsoft.com/kb/3011022/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5f8d-179">2756402</span><span class="sxs-lookup"><span data-stu-id="d5f8d-179">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5f8d-180">Il client MBAM fallirebbe con l'ID evento 4 e il codice di errore 0x8004100E nella descrizione dell'evento</span><span class="sxs-lookup"><span data-stu-id="d5f8d-180">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="d5f8d-181">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="d5f8d-181">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5f8d-182">2639518</span><span class="sxs-lookup"><span data-stu-id="d5f8d-182">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5f8d-183">Errore durante l'apertura di report di conformità Enterprise o computer in MBAM</span><span class="sxs-lookup"><span data-stu-id="d5f8d-183">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="d5f8d-184">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="d5f8d-184">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d5f8d-185">2870842</span><span class="sxs-lookup"><span data-stu-id="d5f8d-185">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5f8d-186">La configurazione di MBAM 2,0 non riesce durante lo scenario di integrazione di Configuration Manager con SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5f8d-186">MBAM 2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="d5f8d-187">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="d5f8d-187">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d5f8d-188">2975472</span><span class="sxs-lookup"><span data-stu-id="d5f8d-188">2975472</span></span></p></td>
<td align="left"><p><span data-ttu-id="d5f8d-189">Deadlock SQL quando molti client MBAM si connettono al database di ripristino MBAM</span><span class="sxs-lookup"><span data-stu-id="d5f8d-189">SQL deadlocks when many MBAM clients connect to the MBAM recovery database</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)"><span data-ttu-id="d5f8d-190">support.microsoft.com/kb/2975472/EN-US</span><span class="sxs-lookup"><span data-stu-id="d5f8d-190">support.microsoft.com/kb/2975472/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="d5f8d-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5f8d-191">Related topics</span></span>


[<span data-ttu-id="d5f8d-192">Informazioni su MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="d5f8d-192">About MBAM 2.5</span></span>](about-mbam-25.md)

 

## <span data-ttu-id="d5f8d-193">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="d5f8d-193">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="d5f8d-194">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="d5f8d-194">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="d5f8d-195">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="d5f8d-195">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





