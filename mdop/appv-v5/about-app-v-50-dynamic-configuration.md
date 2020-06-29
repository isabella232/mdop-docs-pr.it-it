---
title: Informazioni sulla configurazione dinamica di App-V 5.0
description: Informazioni sulla configurazione dinamica di App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815035"
---
# <span data-ttu-id="85200-103">Informazioni sulla configurazione dinamica di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="85200-103">About App-V 5.0 Dynamic Configuration</span></span>


<span data-ttu-id="85200-104">Puoi usare la configurazione dinamica per personalizzare un pacchetto di App-V 5,0 per un utente.</span><span class="sxs-lookup"><span data-stu-id="85200-104">You can use the dynamic configuration to customize an App-V 5.0 package for a user.</span></span> <span data-ttu-id="85200-105">Usare le informazioni seguenti per creare o modificare un file di configurazione dinamica esistente.</span><span class="sxs-lookup"><span data-stu-id="85200-105">Use the following information to create or edit an existing dynamic configuration file.</span></span>

<span data-ttu-id="85200-106">Quando si modifica il file di configurazione dinamica, viene personalizzato il modo in cui verrà eseguito un pacchetto di App-V 5,0 per un utente o un gruppo.</span><span class="sxs-lookup"><span data-stu-id="85200-106">When you edit the dynamic configuration file it customizes how an App-V 5.0 package will run for a user or group.</span></span> <span data-ttu-id="85200-107">Questo consente di fornire un metodo più comodo per la personalizzazione del pacchetto rimuovendo la necessità di risequenziare i pacchetti usando le impostazioni desiderate e offre un modo per rendere indipendente il contenuto del pacchetto e le impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="85200-107">This helps to provide a more convenient method for package customization by removing the need to re-sequence packages using the desired settings, and provides a way to keep package content and custom settings independent.</span></span>

## <span data-ttu-id="85200-108">Avanzate: configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="85200-108">Advanced: Dynamic Configuration</span></span>


<span data-ttu-id="85200-109">I pacchetti di applicazioni virtuali contengono un manifesto che fornisce tutte le informazioni di base per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-109">Virtual application packages contain a manifest that provides all the core information for the package.</span></span> <span data-ttu-id="85200-110">Queste informazioni includono i valori predefiniti per le impostazioni del pacchetto e determinano le impostazioni nella maschera più elementare (senza ulteriori personalizzazioni).</span><span class="sxs-lookup"><span data-stu-id="85200-110">This information includes the defaults for the package settings and determines settings in the most basic form (with no additional customization).</span></span> <span data-ttu-id="85200-111">Per modificare queste impostazioni predefinite per un utente o un gruppo specifico, è possibile creare e modificare i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="85200-111">If you want to adjust these defaults for a particular user or group, you can create and edit the following files:</span></span>

-   <span data-ttu-id="85200-112">File di configurazione utente</span><span class="sxs-lookup"><span data-stu-id="85200-112">User Configuration file</span></span>

-   <span data-ttu-id="85200-113">File di configurazione della distribuzione</span><span class="sxs-lookup"><span data-stu-id="85200-113">Deployment configuration file</span></span>

<span data-ttu-id="85200-114">I file XML precedenti specificano le impostazioni del pacchetto e consentono di personalizzare i pacchetti senza influire direttamente sui pacchetti.</span><span class="sxs-lookup"><span data-stu-id="85200-114">The previous .xml files specify package settings and allow for packages to be customized without directly affecting the packages.</span></span> <span data-ttu-id="85200-115">Quando viene creato un pacchetto, sequencer genera automaticamente file XML di distribuzione e configurazione utente usando i dati del manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-115">When a package is created, the sequencer automatically generates default deployment and user configuration .xml files using the package manifest data.</span></span> <span data-ttu-id="85200-116">Di conseguenza, questi file di configurazione generati automaticamente riflettono semplicemente le impostazioni predefinite che il pacchetto innately come le cose sono state configurate durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="85200-116">Therefore, these automatically generated configuration files simply reflect the default settings that the package innately as from how things were configured during sequencing.</span></span> <span data-ttu-id="85200-117">Se si applicano questi file di configurazione a un pacchetto nella maschera generata dal sequencer, i pacchetti avranno le stesse impostazioni predefinite fornite dal manifesto.</span><span class="sxs-lookup"><span data-stu-id="85200-117">If you apply these configuration files to a package in the form generated by the sequencer, the packages will have the same default settings that came from their manifest.</span></span> <span data-ttu-id="85200-118">In questo articolo viene fornito un modello specifico del pacchetto per iniziare se è necessario modificare una delle impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="85200-118">This provides you with a package-specific template to get started if any of the defaults must be changed.</span></span>

<span data-ttu-id="85200-119">**Nota**  Le informazioni seguenti possono essere usate solo per modificare i file di configurazione generati da Sequencer per personalizzare i pacchetti in base a requisiti specifici per gli utenti o i gruppi.</span><span class="sxs-lookup"><span data-stu-id="85200-119">**Note** The following information can only be used to modify sequencer generated configuration files to customize packages to meet specific user or group requirements.</span></span>

 

### <span data-ttu-id="85200-120">Contenuto del file di configurazione dinamica</span><span class="sxs-lookup"><span data-stu-id="85200-120">Dynamic Configuration file contents</span></span>

<span data-ttu-id="85200-121">Tutte le aggiunte, le eliminazioni e gli aggiornamenti nei file di configurazione devono essere eseguiti in relazione ai valori predefiniti specificati dalle informazioni del manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-121">All of the additions, deletions, and updates in the configuration files need to be made in relation to the default values specified by the package's manifest information.</span></span> <span data-ttu-id="85200-122">Esaminare la tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="85200-122">Review the following table:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85200-123">File Configuration. XML dell'utente</span><span class="sxs-lookup"><span data-stu-id="85200-123">User Configuration .xml file</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85200-124">File Configuration. XML di distribuzione</span><span class="sxs-lookup"><span data-stu-id="85200-124">Deployment Configuration .xml file</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85200-125">Manifesto del pacchetto</span><span class="sxs-lookup"><span data-stu-id="85200-125">Package Manifest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="85200-126">La tabella precedente rappresenta il modo in cui verranno letti i file.</span><span class="sxs-lookup"><span data-stu-id="85200-126">The previous table represents how the files will be read.</span></span> <span data-ttu-id="85200-127">La prima voce rappresenta quello che verrà letto per ultimo, quindi il suo contenuto avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="85200-127">The first entry represents what will be read last, therefore, its content takes precedence.</span></span> <span data-ttu-id="85200-128">Di conseguenza, tutti i pacchetti contengono intrinsecamente e includono le impostazioni predefinite del manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-128">Therefore, all packages inherently contain and provide default settings from the package manifest.</span></span> <span data-ttu-id="85200-129">Se viene applicato un file Configuration. XML di distribuzione con impostazioni personalizzate, verranno ignorati i valori predefiniti del manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-129">If a deployment configuration .xml file with customized settings is applied, it will override the package manifest defaults.</span></span> <span data-ttu-id="85200-130">Se prima di tutto viene applicato un file Configuration. XML con impostazioni personalizzate, l'utente eseguirà l'override sia della configurazione della distribuzione che dei valori predefiniti del manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-130">If a user configuration .xml file with customized settings is applied prior to that, it will override both the deployment configuration and the package manifest defaults.</span></span>

<span data-ttu-id="85200-131">Nell'elenco seguente vengono visualizzate altre informazioni sui due tipi di file:</span><span class="sxs-lookup"><span data-stu-id="85200-131">The following list displays more information about the two file types:</span></span>

-   <span data-ttu-id="85200-132">**File di configurazione utente (userconfig)** : consente di specificare o modificare le impostazioni personalizzate per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-132">**User Configuration File (UserConfig)** – Allows you to specify or modify custom settings for a package.</span></span> <span data-ttu-id="85200-133">Queste impostazioni verranno applicate a un utente specifico quando il pacchetto viene distribuito in un computer che gestisce il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="85200-133">These settings will be applied for a specific user when the package is deployed to a computer running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="85200-134">**File di configurazione della distribuzione (deploymentconfig)** : consente di specificare o modificare le impostazioni predefinite per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-134">**Deployment Configuration File (DeploymentConfig)** – Allows you to specify or modify the default settings for a package.</span></span> <span data-ttu-id="85200-135">Queste impostazioni verranno applicate a tutti gli utenti quando un pacchetto viene distribuito in un computer che gestisce il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="85200-135">These settings will be applied for all users when a package is deployed to a computer running the App-V 5.0 client.</span></span>

<span data-ttu-id="85200-136">Per personalizzare le impostazioni di un pacchetto per un set specifico di utenti in un computer o per apportare modifiche che verranno applicate alle posizioni degli utenti locali, ad esempio HKCU, deve essere usato il file UserConfig.</span><span class="sxs-lookup"><span data-stu-id="85200-136">To customize the settings for a package for a specific set of users on a computer or to make changes that will be applied to local user locations such as HKCU, the UserConfig file should be used.</span></span> <span data-ttu-id="85200-137">Per modificare le impostazioni predefinite di un pacchetto per tutti gli utenti di un computer o per apportare modifiche che verranno applicate a posizioni globali come HKEY \ _LOCAL \ _MACHINE e la cartella tutti gli utenti, è necessario usare il file DeploymentConfig.</span><span class="sxs-lookup"><span data-stu-id="85200-137">To modify the default settings of a package for all users on a machine or to make changes that will be applied to global locations such as HKEY\_LOCAL\_MACHINE and the all users folder, the DeploymentConfig file should be used.</span></span>

<span data-ttu-id="85200-138">Il file UserConfig fornisce le impostazioni di configurazione che possono essere applicate a un singolo utente senza influire sugli altri utenti di un client:</span><span class="sxs-lookup"><span data-stu-id="85200-138">The UserConfig file provides configuration settings that can be applied to a single user without affecting any other users on a client:</span></span>

-   <span data-ttu-id="85200-139">Estensioni che verranno integrate nel sistema nativo per utente:-scelte rapide, associazioni di tipi di file, protocolli URL, AppPaths, client software e COM</span><span class="sxs-lookup"><span data-stu-id="85200-139">Extensions that will be integrated into the native system per user:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

-   <span data-ttu-id="85200-140">Sottosistemi virtuali:-oggetti applicazione, variabili di ambiente, modifiche del registro di sistema, servizi e tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="85200-140">Virtual Subsystems:- Application Objects, Environment variables, Registry modifications, Services and Fonts</span></span>

-   <span data-ttu-id="85200-141">Script (solo contesto utente)</span><span class="sxs-lookup"><span data-stu-id="85200-141">Scripts (User context only)</span></span>

-   <span data-ttu-id="85200-142">Autorità di gestione (per controllare la coesistenza del pacchetto con l'App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="85200-142">Managing Authority (for controlling co-existence of package with App-V 4.6)</span></span>

<span data-ttu-id="85200-143">Il file DeploymentConfig fornisce le impostazioni di configurazione in due sezioni, uno relativo al contesto del computer e uno relativo al contesto utente che fornisce le stesse funzionalità elencate nell'elenco UserConfig precedente:</span><span class="sxs-lookup"><span data-stu-id="85200-143">The DeploymentConfig file provides configuration settings in two sections, one relative to the machine context and one relative to the user context providing the same capabilities listed in the UserConfig list above:</span></span>

-   <span data-ttu-id="85200-144">Tutte le impostazioni UserConfig sopra</span><span class="sxs-lookup"><span data-stu-id="85200-144">All UserConfig settings above</span></span>

-   <span data-ttu-id="85200-145">Estensioni che possono essere applicate solo a livello globale per tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="85200-145">Extensions that can only be applied globally for all users</span></span>

-   <span data-ttu-id="85200-146">Sottosistemi virtuali che possono essere configurati per le posizioni globali del computer, ad esempio il registro di sistema</span><span class="sxs-lookup"><span data-stu-id="85200-146">Virtual Subsystems that can be configured for global machine locations e.g. registry</span></span>

-   <span data-ttu-id="85200-147">URL origine prodotto</span><span class="sxs-lookup"><span data-stu-id="85200-147">Product Source URL</span></span>

-   <span data-ttu-id="85200-148">Script (solo contesto computer)</span><span class="sxs-lookup"><span data-stu-id="85200-148">Scripts (Machine context only)</span></span>

-   <span data-ttu-id="85200-149">Controlli per terminare i processi figlio</span><span class="sxs-lookup"><span data-stu-id="85200-149">Controls to Terminate Child Processes</span></span>

### <span data-ttu-id="85200-150">Struttura di file</span><span class="sxs-lookup"><span data-stu-id="85200-150">File structure</span></span>

<span data-ttu-id="85200-151">La struttura del file di configurazione dinamica App-V 5,0 è illustrata nella sezione seguente.</span><span class="sxs-lookup"><span data-stu-id="85200-151">The structure of the App-V 5.0 Dynamic Configuration file is explained in the following section.</span></span>

### <span data-ttu-id="85200-152">File di configurazione utente dinamico</span><span class="sxs-lookup"><span data-stu-id="85200-152">Dynamic User Configuration file</span></span>

<span data-ttu-id="85200-153">**Intestazione** : l'intestazione di un file di configurazione dell'utente dinamico è la seguente.</span><span class="sxs-lookup"><span data-stu-id="85200-153">**Header** - the header of a dynamic user configuration file is as follows:</span></span>

<span data-ttu-id="85200-154">&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="85200-154">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

<span data-ttu-id="85200-155">**PackageID** è lo stesso valore esistente nel file manifesto.</span><span class="sxs-lookup"><span data-stu-id="85200-155">The **PackageId** is the same value as exists in the Manifest file.</span></span>

<span data-ttu-id="85200-156">**Corpo** : il corpo del file di configurazione dell'utente dinamico può includere tutti i punti di estensione dell'app definiti nel file manifesto, nonché le informazioni per la configurazione delle applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="85200-156">**Body** - the body of the Dynamic User Configuration file can include all the app extension points that are defined in the Manifest file, as well as information to configure virtual applications.</span></span> <span data-ttu-id="85200-157">Nel corpo sono consentite quattro sottosezioni:</span><span class="sxs-lookup"><span data-stu-id="85200-157">There are four subsections allowed in the body:</span></span>

1. <span data-ttu-id="85200-158">**Applicazioni** -tutte le estensioni delle app contenute nel file manifesto all'interno di un pacchetto vengono assegnate con un ID applicazione, definito anche nel file manifesto.</span><span class="sxs-lookup"><span data-stu-id="85200-158">**Applications** - All app-extensions that are contained in the Manifest file within a package are assigned with an Application ID, which is also defined in the manifest file.</span></span> <span data-ttu-id="85200-159">In questo modo è possibile abilitare o disabilitare tutte le estensioni per una determinata applicazione all'interno di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="85200-159">This allows you to enable or disable all the extensions for a given application within a package.</span></span> <span data-ttu-id="85200-160">L' **ID applicazione** deve esistere nel file manifesto o verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="85200-160">The **Application ID** must exist in the Manifest file or it will be ignored.</span></span>

   <span data-ttu-id="85200-161">&lt;UserConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="85200-161">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="85200-162">&lt;Applicazioni&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-162">&lt;Applications&gt;</span></span>

   <span data-ttu-id="85200-163">&lt;!--Non è possibile definire una nuova applicazione in criteri.</span><span class="sxs-lookup"><span data-stu-id="85200-163">&lt;!-- No new application can be defined in policy.</span></span> <span data-ttu-id="85200-164">Il client AppV ignorerà qualsiasi ID applicazione che non sia anche nel file manifesto.&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-164">AppV Client will ignore any application ID that is not also in the Manifest file --&gt;</span></span>

   <span data-ttu-id="85200-165">&lt;ID applicazione = "{a56fa627-c35f-4A01-9e79-7d36aed8225a}" Enabled = "false"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-165">&lt;Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false"&gt;</span></span>

   <span data-ttu-id="85200-166">&lt;/Application&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-166">&lt;/Application&gt;</span></span>

   <span data-ttu-id="85200-167">&lt;/Applications&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-167">&lt;/Applications&gt;</span></span>

   <span data-ttu-id="85200-168">…</span><span class="sxs-lookup"><span data-stu-id="85200-168">…</span></span>

   <span data-ttu-id="85200-169">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-169">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="85200-170">**Sottosistemi** -AppExtensions e altri sottosistemi sono disposti come sottonodi sotto i &lt; sottosistemi &gt; :</span><span class="sxs-lookup"><span data-stu-id="85200-170">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under the &lt;Subsystems&gt;:</span></span>

   <span data-ttu-id="85200-171">&lt;UserConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="85200-171">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="85200-172">&lt;Sottosistemi&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-172">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="85200-173">..</span><span class="sxs-lookup"><span data-stu-id="85200-173">..</span></span>

   <span data-ttu-id="85200-174">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-174">&lt;/Subsystems&gt;</span></span>

   <span data-ttu-id="85200-175">..</span><span class="sxs-lookup"><span data-stu-id="85200-175">..</span></span>

   <span data-ttu-id="85200-176">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-176">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="85200-177">Ogni sottosistema può essere abilitato/disabilitato usando l'attributo "**Enabled**".</span><span class="sxs-lookup"><span data-stu-id="85200-177">Each subsystem can be enabled/disabled using the “**Enabled**” attribute.</span></span> <span data-ttu-id="85200-178">Di seguito sono riportati i vari sottosistemi e esempi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="85200-178">Below are the various subsystems and usage samples.</span></span>

   **<span data-ttu-id="85200-179">Estensioni</span><span class="sxs-lookup"><span data-stu-id="85200-179">Extensions:</span></span>**

   <span data-ttu-id="85200-180">Alcuni sottosistemi (sottosistemi di estensione) controllano le estensioni.</span><span class="sxs-lookup"><span data-stu-id="85200-180">Some subsystems (Extension Subsystems) control Extensions.</span></span> <span data-ttu-id="85200-181">Questi sottosistemi sono:-scelte rapide da tastiera, associazioni di tipi di file, protocolli URL, AppPaths, client software e COM</span><span class="sxs-lookup"><span data-stu-id="85200-181">Those subsystems are:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

   <span data-ttu-id="85200-182">I sottosistemi di estensione possono essere abilitati e disabilitati indipendentemente dal contenuto.</span><span class="sxs-lookup"><span data-stu-id="85200-182">Extension Subsystems can be enabled and disabled independently of the content.</span></span>  <span data-ttu-id="85200-183">In questo modo, se i tasti di scelta rapida sono abilitati, il client utilizzerà i collegamenti contenuti nel manifesto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="85200-183">Thus if Shortcuts are enabled, The client will use the shortcuts contained within the manifest by default.</span></span> <span data-ttu-id="85200-184">Ogni sottosistema di estensione può contenere &lt; un &gt; nodo Extensions.</span><span class="sxs-lookup"><span data-stu-id="85200-184">Each Extension Subsystem can contain an &lt;Extensions&gt; node.</span></span> <span data-ttu-id="85200-185">Se questo elemento figlio è presente, il client ignorerà il contenuto nel file manifesto per il sottosistema e userà solo il contenuto nel file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="85200-185">If this child element is present, the client will ignore the content in the Manifest file for that subsystem and only use the content in the configuration file.</span></span>

   <span data-ttu-id="85200-186">Esempio di utilizzo del sottosistema collegamenti:</span><span class="sxs-lookup"><span data-stu-id="85200-186">Example using the shortcuts subsystem:</span></span>

   1.  <span data-ttu-id="85200-187">Se l'utente ha definito questo contenuto nel file di configurazione dinamico o di distribuzione:</span><span class="sxs-lookup"><span data-stu-id="85200-187">If the user defined this in either the dynamic or deployment config file:</span></span>

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  <span data-ttu-id="85200-188">Se l'utente ha definito solo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="85200-188">If the user defined only the following:</span></span>

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  <span data-ttu-id="85200-189">Se l'utente definisce le operazioni seguenti</span><span class="sxs-lookup"><span data-stu-id="85200-189">If the user defines the following</span></span>

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   <span data-ttu-id="85200-190">Tutte le scelte rapide all'interno del manifesto verranno comunque ignorate.</span><span class="sxs-lookup"><span data-stu-id="85200-190">Then all the shortcuts within the manifest will still be ignored.</span></span> <span data-ttu-id="85200-191">Non ci saranno tasti di scelta rapida integrati.</span><span class="sxs-lookup"><span data-stu-id="85200-191">There will be no shortcuts integrated.</span></span>

   <span data-ttu-id="85200-192">I sottosistemi di estensione supportati sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="85200-192">The supported Extension Subsystems are:</span></span>

   <span data-ttu-id="85200-193">**Scelte rapide:** Questo controlla i tasti di scelta rapida che verranno integrati nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="85200-193">**Shortcuts:** This controls shortcuts that will be integrated into the local system.</span></span> <span data-ttu-id="85200-194">Di seguito è riportato un esempio con due scelte rapide:</span><span class="sxs-lookup"><span data-stu-id="85200-194">Below is a sample with 2 shortcuts:</span></span>

   <span data-ttu-id="85200-195">&lt;Sottosistemi&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-195">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="85200-196">&lt;Tasti di scelta rapida abilitati = "vero"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-196">&lt;Shortcuts Enabled="true"&gt;</span></span>

     <span data-ttu-id="85200-197">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-197">&lt;Extensions&gt;</span></span>

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     <span data-ttu-id="85200-198">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-198">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="85200-199">&lt;Extension Category = "AppV. Shortcut"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-199">&lt;Extension Category="AppV.Shortcut"&gt;</span></span>

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     <span data-ttu-id="85200-200">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-200">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="85200-201">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-201">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="85200-202">&lt;/Shortcuts&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-202">&lt;/Shortcuts&gt;</span></span>

   <span data-ttu-id="85200-203">**Associazioni di tipi di file:** Associa i tipi di file ai programmi da aprire per impostazione predefinita e imposta il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="85200-203">**File-Type Associations:** Associates File-types with programs to open by default as well as setup the context menu.</span></span> <span data-ttu-id="85200-204">I tipi MIME possono anche essere impostati tramite questo susbsystem.</span><span class="sxs-lookup"><span data-stu-id="85200-204">(MIME types can also be setup using this susbsystem).</span></span> <span data-ttu-id="85200-205">L'associazione di tipi di file di esempio è seguente:</span><span class="sxs-lookup"><span data-stu-id="85200-205">Sample File-type Association is below:</span></span>

   <span data-ttu-id="85200-206">&lt;FileTypeAssociations Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-206">&lt;FileTypeAssociations Enabled="true"&gt;</span></span>

   <span data-ttu-id="85200-207">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-207">&lt;Extensions&gt;</span></span>

     <span data-ttu-id="85200-208">&lt;Extension Category = "AppV. FileTypeAssociation"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-208">&lt;Extension Category="AppV.FileTypeAssociation"&gt;</span></span>

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      <span data-ttu-id="85200-209">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-209">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="85200-210">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-210">&lt;/Extensions&gt;</span></span>

     <span data-ttu-id="85200-211">&lt;/FileTypeAssociations&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-211">&lt;/FileTypeAssociations&gt;</span></span>

   <span data-ttu-id="85200-212">**Protocolli URL**: controlla i protocolli URL integrati nel registro di sistema locale del computer client, ad esempio "mailto:".</span><span class="sxs-lookup"><span data-stu-id="85200-212">**URL Protocols**: This controls the URL Protocols that are integrated into the local registry of the client machine e.g. “mailto:”.</span></span>

   <span data-ttu-id="85200-213">&lt;URLProtocols Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-213">&lt;URLProtocols Enabled="true"&gt;</span></span>

   <span data-ttu-id="85200-214">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-214">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="85200-215">&lt;Extension Category = "AppV. URLProtocol"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-215">&lt;Extension Category="AppV.URLProtocol"&gt;</span></span>

   <span data-ttu-id="85200-216">&lt;URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-216">&lt;URLProtocol&gt;</span></span>

     <span data-ttu-id="85200-217">&lt;Nome &gt; mailto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-217">&lt;Name&gt;mailto&lt;/Name&gt;</span></span>

     <span data-ttu-id="85200-218">&lt;ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-218">&lt;ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="85200-219">&lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-219">&lt;DefaultIcon&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403&lt;/DefaultIcon&gt;</span></span>

     <span data-ttu-id="85200-220">&lt;EditFlags &gt; 2 &lt; /EditFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-220">&lt;EditFlags&gt;2&lt;/EditFlags&gt;</span></span>

     <span data-ttu-id="85200-221">&lt;Descrizione&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-221">&lt;Description /&gt;</span></span>

     <span data-ttu-id="85200-222">&lt;AppUserModelID&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-222">&lt;AppUserModelId /&gt;</span></span>

     <span data-ttu-id="85200-223">&lt;FriendlyTypeName /&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-223">&lt;FriendlyTypeName /&gt;</span></span>

     <span data-ttu-id="85200-224">&lt;InfoTip&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-224">&lt;InfoTip /&gt;</span></span>

   <span data-ttu-id="85200-225">&lt;SourceFilter&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-225">&lt;SourceFilter /&gt;</span></span>

     <span data-ttu-id="85200-226">&lt;ShellFolder&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-226">&lt;ShellFolder /&gt;</span></span>

     <span data-ttu-id="85200-227">&lt;WebNavigableCLSID /&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-227">&lt;WebNavigableCLSID /&gt;</span></span>

     <span data-ttu-id="85200-228">&lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-228">&lt;ExplorerFlags&gt;2&lt;/ExplorerFlags&gt;</span></span>

     <span data-ttu-id="85200-229">&lt;CLSID&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-229">&lt;CLSID /&gt;</span></span>

     <span data-ttu-id="85200-230">&lt;ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-230">&lt;ShellCommands&gt;</span></span>

     <span data-ttu-id="85200-231">&lt;DefaultCommand &gt; Open &lt; /DefaultCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-231">&lt;DefaultCommand&gt;open&lt;/DefaultCommand&gt;</span></span>

     <span data-ttu-id="85200-232">&lt;ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-232">&lt;ShellCommand&gt;</span></span>

     <span data-ttu-id="85200-233">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-233">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="85200-234">&lt;Nome &gt; aperto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-234">&lt;Name&gt;open&lt;/Name&gt;</span></span>

     <span data-ttu-id="85200-235">&lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Nota/m "%1" &lt; /CommandLine&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-235">&lt;CommandLine&gt;\[{ProgramFilesX86}\\Microsoft Contoso\\Contoso\\contosomail.EXE" -c OEP.Note /m "%1"&lt;/CommandLine&gt;</span></span>

     <span data-ttu-id="85200-236">&lt;DropTargetClassId /&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-236">&lt;DropTargetClassId /&gt;</span></span>

     <span data-ttu-id="85200-237">&lt;FriendlyName&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-237">&lt;FriendlyName /&gt;</span></span>

     <span data-ttu-id="85200-238">&lt;Extended &gt; 0 &lt; /Extended&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-238">&lt;Extended&gt;0&lt;/Extended&gt;</span></span>

     <span data-ttu-id="85200-239">&lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-239">&lt;LegacyDisable&gt;0&lt;/LegacyDisable&gt;</span></span>

     <span data-ttu-id="85200-240">&lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-240">&lt;SuppressionPolicy&gt;2&lt;/SuppressionPolicy&gt;</span></span>

      <span data-ttu-id="85200-241">&lt;DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-241">&lt;DdeExec&gt;</span></span>

     <span data-ttu-id="85200-242">&lt;NoActivateHandler /&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-242">&lt;NoActivateHandler /&gt;</span></span>

     <span data-ttu-id="85200-243">&lt;Applicazione &gt; ContosoMail &lt; /Application&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-243">&lt;Application&gt;contosomail&lt;/Application&gt;</span></span>

     <span data-ttu-id="85200-244">&lt;Argomento &gt; ShellSystem &lt; /Topic&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-244">&lt;Topic&gt;ShellSystem&lt;/Topic&gt;</span></span>

     <span data-ttu-id="85200-245">&lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-245">&lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;</span></span>

     <span data-ttu-id="85200-246">&lt;DdeCommand &gt; \ [seforeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-246">&lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;</span></span>

     <span data-ttu-id="85200-247">&lt;/DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-247">&lt;/DdeExec&gt;</span></span>

     <span data-ttu-id="85200-248">&lt;/ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-248">&lt;/ShellCommand&gt;</span></span>

     <span data-ttu-id="85200-249">&lt;/ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-249">&lt;/ShellCommands&gt;</span></span>

     <span data-ttu-id="85200-250">&lt;/ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-250">&lt;/ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="85200-251">&lt;/URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-251">&lt;/URLProtocol&gt;</span></span>

     <span data-ttu-id="85200-252">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-252">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="85200-253">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-253">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="85200-254">&lt;/URLProtocols&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-254">&lt;/URLProtocols&gt;</span></span>

   <span data-ttu-id="85200-255">**Client software**: consente all'app di registrarsi come client di posta elettronica, lettore di News, lettore multimediale e rende visibile l'app nell'interfaccia utente imposta l'accesso al programma e il computer.</span><span class="sxs-lookup"><span data-stu-id="85200-255">**Software Clients**: Allows the app to register as an Email client, news reader, media player and makes the app visible in the Set Program Access and Computer Defaults UI.</span></span> <span data-ttu-id="85200-256">Nella maggior parte dei casi è necessario abilitarla e disabilitarla.</span><span class="sxs-lookup"><span data-stu-id="85200-256">In most cases you should only need to enable and disable it.</span></span> <span data-ttu-id="85200-257">Esiste anche un controllo che consente di abilitare e disabilitare il client di posta elettronica in modo specifico se si vuole che gli altri client siano ancora abilitati, ad eccezione del client.</span><span class="sxs-lookup"><span data-stu-id="85200-257">There is also a control to enable and disable the email client specifically if you want the other clients still enabled except for that client.</span></span>

   <span data-ttu-id="85200-258">&lt;SoftwareClients Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-258">&lt;SoftwareClients Enabled="true"&gt;</span></span>

     <span data-ttu-id="85200-259">&lt;ClientConfiguration EmailEnabled = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-259">&lt;ClientConfiguration EmailEnabled="false" /&gt;</span></span>

   <span data-ttu-id="85200-260">&lt;/SoftwareClients&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-260">&lt;/SoftwareClients&gt;</span></span>

   <span data-ttu-id="85200-261">AppPaths:-se un'applicazione ad esempio contoso.exe è registrata con un nome AppPath "MyApp", ti permette di digitare "MyApp" nel menu Esegui e si aprirà contoso.exe.</span><span class="sxs-lookup"><span data-stu-id="85200-261">AppPaths:- If an application for example contoso.exe is registered with an apppath name of “myapp”, it allows you type “myapp” under the run menu and it will open contoso.exe.</span></span>

   <span data-ttu-id="85200-262">&lt;AppPaths Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-262">&lt;AppPaths Enabled="true"&gt;</span></span>

   <span data-ttu-id="85200-263">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-263">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="85200-264">&lt;Extension Category = "AppV. AppPath"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-264">&lt;Extension Category="AppV.AppPath"&gt;</span></span>

   <span data-ttu-id="85200-265">&lt;AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-265">&lt;AppPath&gt;</span></span>

     <span data-ttu-id="85200-266">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-266">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="85200-267">&lt;Nome &gt;contosomail.exe&lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-267">&lt;Name&gt;contosomail.exe&lt;/Name&gt;</span></span>

     <span data-ttu-id="85200-268">&lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationPath&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-268">&lt;ApplicationPath&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationPath&gt;</span></span>

     <span data-ttu-id="85200-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span></span>

     <span data-ttu-id="85200-270">&lt;CanAcceptUrl &gt; false &lt; /CanAcceptUrl&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-270">&lt;CanAcceptUrl&gt;false&lt;/CanAcceptUrl&gt;</span></span>

     <span data-ttu-id="85200-271">&lt;SaveUrl /&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-271">&lt;SaveUrl /&gt;</span></span>

   <span data-ttu-id="85200-272">&lt;/AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-272">&lt;/AppPath&gt;</span></span>

   <span data-ttu-id="85200-273">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-273">&lt;/Extension&gt;</span></span>

   <span data-ttu-id="85200-274">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-274">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="85200-275">&lt;/AppPaths&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-275">&lt;/AppPaths&gt;</span></span>

   <span data-ttu-id="85200-276">**Com**: consente a un'applicazione di registrare server COM locali.</span><span class="sxs-lookup"><span data-stu-id="85200-276">**COM**: Allows an Application register Local COM servers.</span></span> <span data-ttu-id="85200-277">La modalità può essere integrazione, isolata o disinserita.</span><span class="sxs-lookup"><span data-stu-id="85200-277">Mode can be Integration, Isolated or Off.</span></span> <span data-ttu-id="85200-278">Quando isol.</span><span class="sxs-lookup"><span data-stu-id="85200-278">When Isol.</span></span>

   <span data-ttu-id="85200-279">&lt;Modalità COM = "isolata"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-279">&lt;COM Mode="Isolated"/&gt;</span></span>

   <span data-ttu-id="85200-280">**Altre impostazioni**:</span><span class="sxs-lookup"><span data-stu-id="85200-280">**Other Settings**:</span></span>

   <span data-ttu-id="85200-281">Oltre alle estensioni, gli altri sottosistemi possono essere abilitati/disabilitati e modificati:</span><span class="sxs-lookup"><span data-stu-id="85200-281">In addition to Extensions, other subsystems can be enabled/disabled and edited:</span></span>

   <span data-ttu-id="85200-282">**Oggetti kernel virtuali**:</span><span class="sxs-lookup"><span data-stu-id="85200-282">**Virtual Kernel Objects**:</span></span>

   <span data-ttu-id="85200-283">&lt;Oggetti abilitati = "falso"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-283">&lt;Objects Enabled="false" /&gt;</span></span>

   <span data-ttu-id="85200-284">**Registro**di sistema virtuale: usato se si vuole impostare un registro di sistema nel registro di sistema virtuale in HKCU</span><span class="sxs-lookup"><span data-stu-id="85200-284">**Virtual Registry**: Used if you want to set a registry in the Virtual Registry within HKCU</span></span>

   <span data-ttu-id="85200-285">&lt;Registro di sistema abilitato = "vero"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-285">&lt;Registry Enabled="true"&gt;</span></span>

   <span data-ttu-id="85200-286">&lt;Includono&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-286">&lt;Include&gt;</span></span>

   <span data-ttu-id="85200-287">&lt;Key path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-287">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\ABC"&gt;</span></span>

   <span data-ttu-id="85200-288">&lt;Valore Type = "REG \ _SZ" Name = "bar" data = "NewValue"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-288">&lt;Value Type="REG\_SZ" Name="Bar" Data="NewValue" /&gt;</span></span>

    <span data-ttu-id="85200-289">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-289">&lt;/Key&gt;</span></span>

     <span data-ttu-id="85200-290">&lt;Key path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-290">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\EmptyKey" /&gt;</span></span>

    <span data-ttu-id="85200-291">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-291">&lt;/Include&gt;</span></span>

   <span data-ttu-id="85200-292">&lt;Eliminare&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-292">&lt;Delete&gt;</span></span>

     <span data-ttu-id="85200-293">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-293">&lt;/Registry&gt;</span></span>

   **<span data-ttu-id="85200-294">File system virtuale</span><span class="sxs-lookup"><span data-stu-id="85200-294">Virtual File System</span></span>**

         &lt;FileSystem Enabled="true" /&gt;

   **<span data-ttu-id="85200-295">Tipi di carattere virtuali</span><span class="sxs-lookup"><span data-stu-id="85200-295">Virtual Fonts</span></span>**

         &lt;Fonts Enabled="false" /&gt;

   **<span data-ttu-id="85200-296">Variabili di ambiente virtuali</span><span class="sxs-lookup"><span data-stu-id="85200-296">Virtual Environment Variables</span></span>**

   <span data-ttu-id="85200-297">&lt;EnvironmentVariables Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-297">&lt;EnvironmentVariables Enabled="true"&gt;</span></span>

   <span data-ttu-id="85200-298">&lt;Includono&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-298">&lt;Include&gt;</span></span>

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **<span data-ttu-id="85200-299">Servizi virtuali</span><span class="sxs-lookup"><span data-stu-id="85200-299">Virtual services</span></span>**

         &lt;Services Enabled="false" /&gt;

3. <span data-ttu-id="85200-300">**Userscripts** -gli script possono essere usati per configurare o modificare l'ambiente virtuale, nonché per eseguire script in fase di distribuzione o rimozione, prima dell'esecuzione di un'applicazione oppure possono essere usati per "pulire" l'ambiente dopo la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85200-300">**UserScripts** – Scripts can be used to setup or alter the virtual environment as well as execute scripts at time of deployment or removal, before an application executes, or they can be used to “clean up” the environment after the application terminates.</span></span> <span data-ttu-id="85200-301">Fare riferimento a un file di configurazione dell'utente di esempio che viene restituito dal sequencer per visualizzare uno script di esempio.</span><span class="sxs-lookup"><span data-stu-id="85200-301">Please reference a sample User configuration file that is output by the sequencer to see a sample script.</span></span> <span data-ttu-id="85200-302">La sezione Scripts seguente fornisce altre informazioni sui vari trigger che possono essere usati.</span><span class="sxs-lookup"><span data-stu-id="85200-302">The Scripts section below provides more information on the various triggers that can be used.</span></span>

4. <span data-ttu-id="85200-303">**ManagingAuthority** -può essere usato quando due versioni del pacchetto sono coesistenti nello stesso computer, uno distribuito in App-v 4,6 e l'altro distribuito in App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="85200-303">**ManagingAuthority** – Can be used when 2 versions of your package are co-existing on the same machine, one deployed to App-V 4.6 and the other deployed on App-V 5.0.</span></span> <span data-ttu-id="85200-304">Per consentire a App-V vNext di assumere i punti di estensione App-V 4,6 per il pacchetto denominato, immettere quanto segue nel file UserConfig (dove PackageName è il GUID del pacchetto in App-V 4,6:</span><span class="sxs-lookup"><span data-stu-id="85200-304">To Allow App-V vNext to take over App-V 4.6 extension points for the named package enter the following in the UserConfig file (where PackageName is the Package GUID in App-V 4.6:</span></span>

   <span data-ttu-id="85200-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417C-acef-76fc5297fe81"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" /&gt;</span></span>

### <span data-ttu-id="85200-306">File di configurazione della distribuzione dinamica</span><span class="sxs-lookup"><span data-stu-id="85200-306">Dynamic Deployment Configuration file</span></span>

<span data-ttu-id="85200-307">**Intestazione** -l'intestazione di un file di configurazione della distribuzione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="85200-307">**Header** - The header of a Deployment Configuration file is as follows:</span></span>

<span data-ttu-id="85200-308">&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="85200-308">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="85200-309">**PackageID** è lo stesso valore esistente nel file manifesto.</span><span class="sxs-lookup"><span data-stu-id="85200-309">The **PackageId** is the same value as exists in the manifest file.</span></span>

<span data-ttu-id="85200-310">**Body** -il corpo del file di configurazione della distribuzione include due sezioni:</span><span class="sxs-lookup"><span data-stu-id="85200-310">**Body** - The body of the deployment configuration file includes two sections:</span></span>

-   <span data-ttu-id="85200-311">Sezione Configurazione utente: consente lo stesso contenuto del file di configurazione dell'utente descritto nella sezione precedente.</span><span class="sxs-lookup"><span data-stu-id="85200-311">User Configuration section –allows the same content as the User Configuration file described in the previous section.</span></span> <span data-ttu-id="85200-312">Quando il pacchetto viene pubblicato in un utente, tutte le impostazioni di configurazione di appextensions in questa sezione sovrascriveranno le impostazioni del manifesto all'interno del pacchetto, a meno che non venga fornito anche un file di configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="85200-312">When the package is published to a user, any appextensions configuration settings in this section will override corresponding settings in the Manifest within the package unless a user configuration file is also provided.</span></span> <span data-ttu-id="85200-313">Se viene fornito anche un file UserConfig, verrà usato al posto delle impostazioni utente nel file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="85200-313">If a UserConfig file is also provided, it will be used instead of the User settings in the deployment configuration file.</span></span> <span data-ttu-id="85200-314">Se il pacchetto viene pubblicato globalmente, in combinazione con il manifesto verrà usato solo il contenuto del file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="85200-314">If the package is published globally, then only the contents of the deployment configuration file will be used in combination with the manifest.</span></span>

-   <span data-ttu-id="85200-315">Sezione Configurazione computer: contiene informazioni che possono essere configurate solo per un intero computer, non per un utente specifico nel computer.</span><span class="sxs-lookup"><span data-stu-id="85200-315">Machine Configuration section–contains information that can be configured only for an entire machine, not for a specific user on the machine.</span></span> <span data-ttu-id="85200-316">Ad esempio, HKEY \ _LOCAL \ _MACHINE le chiavi del registro di sistema in VFS.</span><span class="sxs-lookup"><span data-stu-id="85200-316">For example, HKEY\_LOCAL\_MACHINE registry keys in the VFS.</span></span>

<span data-ttu-id="85200-317">&lt;DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="85200-317">&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="85200-318">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-318">&lt;UserConfiguration&gt;</span></span>

  <span data-ttu-id="85200-319">..</span><span class="sxs-lookup"><span data-stu-id="85200-319">..</span></span>

<span data-ttu-id="85200-320">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-320">&lt;/UserConfiguration&gt;</span></span>

<span data-ttu-id="85200-321">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-321">&lt;MachineConfiguration&gt;</span></span>

<span data-ttu-id="85200-322">..</span><span class="sxs-lookup"><span data-stu-id="85200-322">..</span></span>

<span data-ttu-id="85200-323">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-323">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="85200-324">..</span><span class="sxs-lookup"><span data-stu-id="85200-324">..</span></span>

<span data-ttu-id="85200-325">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-325">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="85200-326">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-326">&lt;/DeploymentConfiguration&gt;</span></span>

<span data-ttu-id="85200-327">**Configurazione utente** : usare la sezione **file di configurazione utente dinamico** precedente per informazioni sulle impostazioni disponibili nella sezione Configurazione utente del file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="85200-327">**User Configuration** - use the previous **Dynamic User Configuration file** section for information on settings that are provided in the user configuration section of the Deployment Configuration file.</span></span>

<span data-ttu-id="85200-328">Configurazione del computer: la sezione configurazione macchina del file di configurazione della distribuzione viene usata per configurare le informazioni che possono essere impostate solo per un intero computer, non per un utente specifico nel computer.</span><span class="sxs-lookup"><span data-stu-id="85200-328">Machine Configuration - the Machine configuration section of the Deployment Configuration File is used to configure information that can be set only for an entire machine, not for a specific user on the computer.</span></span> <span data-ttu-id="85200-329">Ad esempio, HKEY \ _LOCAL \ _MACHINE chiavi del registro di sistema nel registro di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="85200-329">For example, HKEY\_LOCAL\_MACHINE registry keys in the Virtual Registry.</span></span> <span data-ttu-id="85200-330">In questo elemento sono consentite quattro sottosezioni</span><span class="sxs-lookup"><span data-stu-id="85200-330">There are four subsections allowed in under this element</span></span>

1.  <span data-ttu-id="85200-331">**Sottosistemi** -AppExtensions e altri sottosistemi sono disposti come sottonodi in &lt; sottosistemi &gt; :</span><span class="sxs-lookup"><span data-stu-id="85200-331">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under &lt;Subsystems&gt;:</span></span>

    <span data-ttu-id="85200-332">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-332">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="85200-333">&lt;Sottosistemi&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-333">&lt;Subsystems&gt;</span></span>

      <span data-ttu-id="85200-334">..</span><span class="sxs-lookup"><span data-stu-id="85200-334">..</span></span>

      <span data-ttu-id="85200-335">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-335">&lt;/Subsystems&gt;</span></span>

    <span data-ttu-id="85200-336">..</span><span class="sxs-lookup"><span data-stu-id="85200-336">..</span></span>

    <span data-ttu-id="85200-337">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-337">&lt;/MachineConfiguration&gt;</span></span>

    <span data-ttu-id="85200-338">Nella sezione seguente vengono visualizzati i vari sottosistemi e gli esempi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="85200-338">The following section displays the various subsystems and usage samples.</span></span>

    <span data-ttu-id="85200-339">**Estensioni**:</span><span class="sxs-lookup"><span data-stu-id="85200-339">**Extensions**:</span></span>

    <span data-ttu-id="85200-340">Alcuni sottosistemi (sottosistemi di estensione) controllano le estensioni che possono essere applicate solo a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="85200-340">Some subsystems (Extension Subsystems) control Extensions which can only apply to all users.</span></span> <span data-ttu-id="85200-341">Il sottosistema è funzionalità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85200-341">The subsystem is application capabilities.</span></span> <span data-ttu-id="85200-342">Poiché questa operazione può essere applicata solo a tutti gli utenti, il pacchetto deve essere pubblicato globalmente in modo che questo tipo di estensione venga integrato nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="85200-342">Because this can only apply to all users, the package must be published globally in order for this type of extension to be integrated into the local system.</span></span> <span data-ttu-id="85200-343">Le stesse regole per i controlli e le impostazioni applicabili alle estensioni della configurazione utente si applicano anche a quelle nella sezione MachineConfiguration.</span><span class="sxs-lookup"><span data-stu-id="85200-343">The same rules for controls and settings that apply to the Extensions in the User Configuration also apply to those in the MachineConfiguration section.</span></span>

    <span data-ttu-id="85200-344">**Funzionalità delle applicazioni**: usate dai programmi predefiniti nell'interfaccia del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="85200-344">**Application Capabilities**: Used by default programs in windows operating system Interface.</span></span> <span data-ttu-id="85200-345">Consente a un'applicazione di registrarsi come in grado di aprire determinate estensioni di file, come contendente per lo slot del browser Internet del menu Start, in grado di aprire determinati tipi MIME di Windows.</span><span class="sxs-lookup"><span data-stu-id="85200-345">Allows an application to register itself as capable of opening certain file extensions, as a contender for the start menu internet browser slot, as capable of opening certain windows MIME types.</span></span><span data-ttu-id="85200-346">Questa estensione rende inoltre visibile l'applicazione virtuale nell'interfaccia utente imposta programmi predefiniti.:</span><span class="sxs-lookup"><span data-stu-id="85200-346"> This extension also makes the virtual application visible in the Set Default Programs UI.:</span></span>

    <span data-ttu-id="85200-347">&lt;ApplicationCapabilities Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-347">&lt;ApplicationCapabilities Enabled="true"&gt;</span></span>

      <span data-ttu-id="85200-348">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-348">&lt;Extensions&gt;</span></span>

       <span data-ttu-id="85200-349">&lt;Extension Category = "AppV. ApplicationCapabilities"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-349">&lt;Extension Category="AppV.ApplicationCapabilities"&gt;</span></span>

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       <span data-ttu-id="85200-350">&lt;CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-350">&lt;CapabilityGroup&gt;</span></span>

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      <span data-ttu-id="85200-351">&lt;/CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-351">&lt;/CapabilityGroup&gt;</span></span>

       <span data-ttu-id="85200-352">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-352">&lt;/ApplicationCapabilities&gt;</span></span>

      <span data-ttu-id="85200-353">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-353">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="85200-354">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-354">&lt;/Extensions&gt;</span></span>

    <span data-ttu-id="85200-355">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-355">&lt;/ApplicationCapabilities&gt;</span></span>

    <span data-ttu-id="85200-356">**Altre impostazioni**:</span><span class="sxs-lookup"><span data-stu-id="85200-356">**Other Settings**:</span></span>

    <span data-ttu-id="85200-357">Oltre alle estensioni, è possibile modificare altri sottosistemi:</span><span class="sxs-lookup"><span data-stu-id="85200-357">In addition to Extensions, other subsystems can be edited:</span></span>

    <span data-ttu-id="85200-358">**Registro**di sistema virtuale a livello di computer: usato quando si vuole impostare una chiave del registro di sistema nel registro di sistema virtuale in HKEY \ _Local \ _Machine</span><span class="sxs-lookup"><span data-stu-id="85200-358">**Machine Wide Virtual Registry**: Used when you want to set a registry key in the virtual registry within HKEY\_Local\_Machine</span></span>

    <span data-ttu-id="85200-359">&lt;Registro di sistema&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-359">&lt;Registry&gt;</span></span>

    <span data-ttu-id="85200-360">&lt;Includono&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-360">&lt;Include&gt;</span></span>

      <span data-ttu-id="85200-361">&lt;Key path = "\\REGISTRY\\Machine\\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-361">&lt;Key Path="\\REGISTRY\\Machine\\Software\\ABC"&gt;</span></span>

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       <span data-ttu-id="85200-362">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-362">&lt;/Key&gt;</span></span>

      <span data-ttu-id="85200-363">&lt;Key path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-363">&lt;Key Path="\\REGISTRY\\Machine\\Software\\EmptyKey" /&gt;</span></span>

     <span data-ttu-id="85200-364">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-364">&lt;/Include&gt;</span></span>

    <span data-ttu-id="85200-365">&lt;Eliminare&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-365">&lt;Delete&gt;</span></span>

    <span data-ttu-id="85200-366">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-366">&lt;/Registry&gt;</span></span>

    **<span data-ttu-id="85200-367">Oggetti kernel virtuali a livello di computer</span><span class="sxs-lookup"><span data-stu-id="85200-367">Machine Wide Virtual Kernel Objects</span></span>**

    <span data-ttu-id="85200-368">&lt;Oggetti&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-368">&lt;Objects&gt;</span></span>

    <span data-ttu-id="85200-369">&lt;NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-369">&lt;NotIsolate&gt;</span></span>

       <span data-ttu-id="85200-370">&lt;Object Name = "testObject"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-370">&lt;Object Name="testObject" /&gt;</span></span>

     <span data-ttu-id="85200-371">&lt;/NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-371">&lt;/NotIsolate&gt;</span></span>

    <span data-ttu-id="85200-372">&lt;/Objects&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-372">&lt;/Objects&gt;</span></span>

2.  <span data-ttu-id="85200-373">**ProductSourceURLOptOut**: indica se l'URL del pacchetto può essere modificato globalmente tramite PackageSourceRoot (per supportare scenari di succursale).</span><span class="sxs-lookup"><span data-stu-id="85200-373">**ProductSourceURLOptOut**: Indicates whether the URL for the package can be modified globally through PackageSourceRoot (to support branch office scenarios).</span></span> <span data-ttu-id="85200-374">Il valore predefinito è false e la modifica dell'impostazione diventa effettiva per il successivo avvio.</span><span class="sxs-lookup"><span data-stu-id="85200-374">Default is false and the setting change takes effect on the next launch.</span></span>  

    <span data-ttu-id="85200-375">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-375">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="85200-376">..</span><span class="sxs-lookup"><span data-stu-id="85200-376">..</span></span> 

      <span data-ttu-id="85200-377">&lt;ProductSourceURLOptOut Enabled = "true"/&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-377">&lt;ProductSourceURLOptOut Enabled="true" /&gt;</span></span>

      <span data-ttu-id="85200-378">..</span><span class="sxs-lookup"><span data-stu-id="85200-378">..</span></span>

    <span data-ttu-id="85200-379">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-379">&lt;/MachineConfiguration&gt;</span></span>

3.  <span data-ttu-id="85200-380">**MachineScripts** -il pacchetto può essere configurato per eseguire script in fase di distribuzione, pubblicazione o rimozione.</span><span class="sxs-lookup"><span data-stu-id="85200-380">**MachineScripts** – Package can be configured to execute scripts at time of deployment, publishing or removal.</span></span> <span data-ttu-id="85200-381">Fare riferimento a un file di configurazione della distribuzione di esempio generato dal sequencer per visualizzare uno script di esempio.</span><span class="sxs-lookup"><span data-stu-id="85200-381">Please reference a sample deployment configuration file that is generated by the sequencer to see a sample script.</span></span> <span data-ttu-id="85200-382">La sezione Scripts seguente fornisce altre informazioni sui vari trigger che possono essere usati</span><span class="sxs-lookup"><span data-stu-id="85200-382">The Scripts section below provides more information on the various triggers that can be used</span></span>

4.  <span data-ttu-id="85200-383">**TerminateChildProcess**:-è possibile specificare un file eseguibile dell'applicazione, i cui processi figlio verranno terminati quando il processo exe dell'applicazione viene terminato.</span><span class="sxs-lookup"><span data-stu-id="85200-383">**TerminateChildProcess**:- An application executable can be specified, whose child processes will be terminated when the application exe process is terminated.</span></span>

    <span data-ttu-id="85200-384">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-384">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="85200-385">..</span><span class="sxs-lookup"><span data-stu-id="85200-385">..</span></span>   

      <span data-ttu-id="85200-386">&lt;TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-386">&lt;TerminateChildProcesses&gt;</span></span>

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      <span data-ttu-id="85200-387">&lt;/TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-387">&lt;/TerminateChildProcesses&gt;</span></span>

      <span data-ttu-id="85200-388">..</span><span class="sxs-lookup"><span data-stu-id="85200-388">..</span></span>

    <span data-ttu-id="85200-389">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="85200-389">&lt;/MachineConfiguration&gt;</span></span>

### <span data-ttu-id="85200-390">Script</span><span class="sxs-lookup"><span data-stu-id="85200-390">Scripts</span></span>

<span data-ttu-id="85200-391">La tabella seguente descrive i vari eventi di script e il contesto in cui possono essere eseguiti.</span><span class="sxs-lookup"><span data-stu-id="85200-391">The following table describes the various script events and the context under which they can be run.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="85200-392">Tempo di esecuzione degli script</span><span class="sxs-lookup"><span data-stu-id="85200-392">Script Execution Time</span></span></th>
<th align="left"><span data-ttu-id="85200-393">Può essere specificato nella configurazione di distribuzione</span><span class="sxs-lookup"><span data-stu-id="85200-393">Can be specified in Deployment Configuration</span></span></th>
<th align="left"><span data-ttu-id="85200-394">Può essere specificato nella configurazione utente</span><span class="sxs-lookup"><span data-stu-id="85200-394">Can be specified in User Configuration</span></span></th>
<th align="left"><span data-ttu-id="85200-395">Può essere eseguito nell'ambiente virtuale del pacchetto</span><span class="sxs-lookup"><span data-stu-id="85200-395">Can run in the Virtual Environment of the package</span></span></th>
<th align="left"><span data-ttu-id="85200-396">Può essere eseguito nel contesto di un'applicazione specifica</span><span class="sxs-lookup"><span data-stu-id="85200-396">Can be run in the context of a specific application</span></span></th>
<th align="left"><span data-ttu-id="85200-397">Viene eseguito in contesto sistema/utente: (configurazione della distribuzione, configurazione utente)</span><span class="sxs-lookup"><span data-stu-id="85200-397">Runs in system/user context: (Deployment Configuration, User Configuration)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85200-398">AddPackage</span><span class="sxs-lookup"><span data-stu-id="85200-398">AddPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-399">X</span><span class="sxs-lookup"><span data-stu-id="85200-399">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85200-400">(SISTEMA, N/D)</span><span class="sxs-lookup"><span data-stu-id="85200-400">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85200-401">PublishPackage</span><span class="sxs-lookup"><span data-stu-id="85200-401">PublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-402">X</span><span class="sxs-lookup"><span data-stu-id="85200-402">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-403">X</span><span class="sxs-lookup"><span data-stu-id="85200-403">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85200-404">(Sistema; utente)</span><span class="sxs-lookup"><span data-stu-id="85200-404">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85200-405">UnpublishPackage</span><span class="sxs-lookup"><span data-stu-id="85200-405">UnpublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-406">X</span><span class="sxs-lookup"><span data-stu-id="85200-406">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-407">X</span><span class="sxs-lookup"><span data-stu-id="85200-407">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85200-408">(Sistema; utente)</span><span class="sxs-lookup"><span data-stu-id="85200-408">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85200-409">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="85200-409">RemovePackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-410">X</span><span class="sxs-lookup"><span data-stu-id="85200-410">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85200-411">(SISTEMA, N/D)</span><span class="sxs-lookup"><span data-stu-id="85200-411">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85200-412">StartProcess quale nome</span><span class="sxs-lookup"><span data-stu-id="85200-412">StartProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-413">X</span><span class="sxs-lookup"><span data-stu-id="85200-413">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-414">X</span><span class="sxs-lookup"><span data-stu-id="85200-414">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-415">X</span><span class="sxs-lookup"><span data-stu-id="85200-415">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-416">X</span><span class="sxs-lookup"><span data-stu-id="85200-416">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-417">(Utente, utente)</span><span class="sxs-lookup"><span data-stu-id="85200-417">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85200-418">ExitProcess</span><span class="sxs-lookup"><span data-stu-id="85200-418">ExitProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-419">X</span><span class="sxs-lookup"><span data-stu-id="85200-419">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-420">X</span><span class="sxs-lookup"><span data-stu-id="85200-420">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85200-421">X</span><span class="sxs-lookup"><span data-stu-id="85200-421">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-422">(Utente, utente)</span><span class="sxs-lookup"><span data-stu-id="85200-422">(User, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="85200-423">StartVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="85200-423">StartVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-424">X</span><span class="sxs-lookup"><span data-stu-id="85200-424">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-425">X</span><span class="sxs-lookup"><span data-stu-id="85200-425">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-426">X</span><span class="sxs-lookup"><span data-stu-id="85200-426">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85200-427">(Utente, utente)</span><span class="sxs-lookup"><span data-stu-id="85200-427">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="85200-428">TerminateVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="85200-428">TerminateVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-429">X</span><span class="sxs-lookup"><span data-stu-id="85200-429">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="85200-430">X</span><span class="sxs-lookup"><span data-stu-id="85200-430">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="85200-431">(Utente, utente)</span><span class="sxs-lookup"><span data-stu-id="85200-431">(User, User)</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="85200-432">Creare un file di configurazione dinamica usando un file manifesto di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="85200-432">Create a Dynamic Configuration file using an App-V 5.0 Manifest file</span></span>

<span data-ttu-id="85200-433">Puoi creare il file di configurazione dinamica usando uno dei tre metodi seguenti: manualmente, usando la console di gestione di App-V 5,0 o sequenziando un pacchetto, che verrà generato con due file di esempio.</span><span class="sxs-lookup"><span data-stu-id="85200-433">You can create the Dynamic Configuration file using one of three methods: either manually, using the App-V 5.0 Management Console or sequencing a package, which will be generated with 2 sample files.</span></span>

<span data-ttu-id="85200-434">Per altre informazioni su come creare il file usando la console di gestione di App-V 5,0, vedere [come creare un file di configurazione personalizzato usando la console di gestione di App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span><span class="sxs-lookup"><span data-stu-id="85200-434">For more information about how to create the file using the App-V 5.0 Management Console see, [How to Create a Custom Configuration File by Using the App-V 5.0 Management Console](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span></span>

<span data-ttu-id="85200-435">Per creare il file manualmente, è possibile combinare le informazioni di cui sopra nelle sezioni precedenti in un singolo file.</span><span class="sxs-lookup"><span data-stu-id="85200-435">To create the file manually, the information above in previous sections can be combined into a single file.</span></span> <span data-ttu-id="85200-436">Ti consigliamo di usare i file generati dal sequencer.</span><span class="sxs-lookup"><span data-stu-id="85200-436">We recommend you use files generated by the sequencer.</span></span>






## <span data-ttu-id="85200-437">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85200-437">Related topics</span></span>


[<span data-ttu-id="85200-438">Come applicare il file di configurazione della distribuzione con PowerShell</span><span class="sxs-lookup"><span data-stu-id="85200-438">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[<span data-ttu-id="85200-439">Come applicare il file di configurazione utente con PowerShell</span><span class="sxs-lookup"><span data-stu-id="85200-439">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[<span data-ttu-id="85200-440">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="85200-440">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





