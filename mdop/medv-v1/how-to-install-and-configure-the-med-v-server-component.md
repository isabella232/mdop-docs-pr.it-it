---
title: Come installare e configurare il componente del server MED-V
description: Come installare e configurare il componente del server MED-V
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826976"
---
# <span data-ttu-id="6ee13-103">Come installare e configurare il componente del server MED-V</span><span class="sxs-lookup"><span data-stu-id="6ee13-103">How to Install and Configure the MED-V Server Component</span></span>


<span data-ttu-id="6ee13-104">Questa sezione spiega come [installare](#bkmk-howtoinstallthemedvserver) e [configurare](#bkmk-howtoconfigurethemedvserver) il server MED-V.</span><span class="sxs-lookup"><span data-stu-id="6ee13-104">This section explains how to [install](#bkmk-howtoinstallthemedvserver) and [configure](#bkmk-howtoconfigurethemedvserver) the MED-V server.</span></span>

## <a href="" id="bkmk-howtoinstallthemedvserver"></a><span data-ttu-id="6ee13-105">Come installare il server MED-V</span><span class="sxs-lookup"><span data-stu-id="6ee13-105">How to Install the MED-V Server</span></span>


**<span data-ttu-id="6ee13-106">Per installare il server MED-V</span><span class="sxs-lookup"><span data-stu-id="6ee13-106">To install the MED-V server</span></span>**

1.  <span data-ttu-id="6ee13-107">Installare il pacchetto server. msi MED-V.</span><span class="sxs-lookup"><span data-stu-id="6ee13-107">Install the MED-V Server .msi package.</span></span>

    <span data-ttu-id="6ee13-108">Il pacchetto MED-V Server. msi si chiama *MED-V\_Server\_x.msi*, dove x è il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="6ee13-108">The MED-V Server .msi package is called *MED-V\_Server\_x.msi*, where x is the version number.</span></span>

    <span data-ttu-id="6ee13-109">Ad esempio, *MED-V\_Server\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="6ee13-109">For example, *MED-V\_Server\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="6ee13-110">Quando viene visualizzata la schermata **iniziale della procedura guidata InstallShield** , fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-110">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

3.  <span data-ttu-id="6ee13-111">Nella schermata **contratto di licenza** leggere il contratto di licenza, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-111">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

    <span data-ttu-id="6ee13-112">Verrà visualizzata la schermata **cartella di destinazione** con la cartella di installazione predefinita visualizzata.</span><span class="sxs-lookup"><span data-stu-id="6ee13-112">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="6ee13-113">La cartella di installazione predefinita è *%SystemDrive%\\Program \\Programmi\\microsoft Enterprise Desktop Virtualization\\*.</span><span class="sxs-lookup"><span data-stu-id="6ee13-113">The default installation folder is *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span></span>

    -   <span data-ttu-id="6ee13-114">Per modificare la cartella in cui deve essere installato MED-V, fare clic su **Cambia** e selezionare una cartella esistente.</span><span class="sxs-lookup"><span data-stu-id="6ee13-114">To change the folder where MED-V should be installed, click **Change** and browse to an existing folder.</span></span>

4.  <span data-ttu-id="6ee13-115">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-115">Click **Next**.</span></span>

5.  <span data-ttu-id="6ee13-116">Nella schermata **pronto per l'installazione** fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-116">On the **Ready to Install the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="6ee13-117">Viene avviata l'installazione del server MED-V.</span><span class="sxs-lookup"><span data-stu-id="6ee13-117">The MED-V server installation starts.</span></span> <span data-ttu-id="6ee13-118">Questo può richiedere diversi minuti e la schermata potrebbe non visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="6ee13-118">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="6ee13-119">Durante l'installazione vengono visualizzate diverse schermate di stato.</span><span class="sxs-lookup"><span data-stu-id="6ee13-119">During installation, several progress screens appear.</span></span> <span data-ttu-id="6ee13-120">Se viene visualizzato un messaggio, seguire le istruzioni fornite.</span><span class="sxs-lookup"><span data-stu-id="6ee13-120">If a message appears, follow the instructions provided.</span></span>

6.  <span data-ttu-id="6ee13-121">Quando viene visualizzata la schermata **completamento guidata InstallShield** , fare clic su **fine** per completare la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="6ee13-121">When the **InstallShield Wizard Completed** screen appears, click **Finish** to complete the wizard.</span></span>

**<span data-ttu-id="6ee13-122">Nota</span><span class="sxs-lookup"><span data-stu-id="6ee13-122">Note</span></span>**  
<span data-ttu-id="6ee13-123">Se si sta installando il server MED-V tramite Desktop remoto Microsoft, usare la sintassi seguente: **mstsc/admin**. Verificare che la sessione RDP sia rivolta alla console.</span><span class="sxs-lookup"><span data-stu-id="6ee13-123">If you are installing the MED-V server via Microsoft Remote Desktop, use the following syntax: **mstsc/admin**. Ensure that your RDP session is directed to the console.</span></span>



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a><span data-ttu-id="6ee13-124">Come configurare il server MED-V</span><span class="sxs-lookup"><span data-stu-id="6ee13-124">How to Configure the MED-V Server</span></span>


<span data-ttu-id="6ee13-125">Le impostazioni del server seguenti possono essere configurate:</span><span class="sxs-lookup"><span data-stu-id="6ee13-125">The following server settings can be configured:</span></span>

-   [<span data-ttu-id="6ee13-126">Connessioni</span><span class="sxs-lookup"><span data-stu-id="6ee13-126">Connections</span></span>](#bkmk-configuringconnections)

-   [<span data-ttu-id="6ee13-127">Immagini</span><span class="sxs-lookup"><span data-stu-id="6ee13-127">Images</span></span>](#bkmk-configuringimages)

-   [<span data-ttu-id="6ee13-128">Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="6ee13-128">Permissions</span></span>](#bkmk-configuringpermissions)

-   [<span data-ttu-id="6ee13-129">Rapporti</span><span class="sxs-lookup"><span data-stu-id="6ee13-129">Reports</span></span>](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a><span data-ttu-id="6ee13-130">Configurazione delle connessioni</span><span class="sxs-lookup"><span data-stu-id="6ee13-130">Configuring Connections</span></span>

**<span data-ttu-id="6ee13-131">Per configurare le connessioni</span><span class="sxs-lookup"><span data-stu-id="6ee13-131">To configure connections</span></span>**

1.  <span data-ttu-id="6ee13-132">Nel menu Start di Windows selezionare **tutti i programmi &gt; Med-v &gt; Med-v Server Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-132">On the Windows Start menu, select **All Programs &gt; MED-V &gt; MED-V Server Configuration Manager**.</span></span>

    **<span data-ttu-id="6ee13-133">Nota</span><span class="sxs-lookup"><span data-stu-id="6ee13-133">Note</span></span>**  
    <span data-ttu-id="6ee13-134">Nota: se è stata selezionata la casella di controllo **Avvia Gestione configurazione server MED-v** durante l'installazione del server, la gestione configurazione di Med-v Server viene avviata automaticamente dopo il completamento dell'installazione del server.</span><span class="sxs-lookup"><span data-stu-id="6ee13-134">Note: If you selected the **Launch MED-V Server Configuration Manager** check box during the server installation, the MED-V server configuration manager starts automatically after the server installation is complete.</span></span>



~~~
The MED-V Server Configuration Manager appears.
~~~

2. <span data-ttu-id="6ee13-135">Nella scheda **connessioni** configurare le impostazioni di connessione client seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ee13-135">On the **Connections** tab, configure the following client connections settings:</span></span>

   -   <span data-ttu-id="6ee13-136">**Abilitare le connessioni non crittografate (http), tramite la porta**, selezionare questa casella di controllo per abilitare le connessioni non crittografate con una porta specificata.</span><span class="sxs-lookup"><span data-stu-id="6ee13-136">**Enable unencrypted connections (http), using port**—Select this check box to enable unencrypted connections using a specified port.</span></span> <span data-ttu-id="6ee13-137">Nella casella porta immettere la porta del server in cui accettare connessioni non crittografate (http).</span><span class="sxs-lookup"><span data-stu-id="6ee13-137">In the port box, enter the server port on which to accept unencrypted connections (http).</span></span>

   -   <span data-ttu-id="6ee13-138">**Abilitare le connessioni crittografate (HTTPS) tramite la porta**: selezionare questa casella di controllo per abilitare le connessioni crittografate con una porta specificata.</span><span class="sxs-lookup"><span data-stu-id="6ee13-138">**Enable encrypted connections (https), using port**—Select this check box to enable encrypted connections using a specified port.</span></span> <span data-ttu-id="6ee13-139">Nella casella porta immettere la porta del server in cui accettare connessioni crittografate (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="6ee13-139">In the port box, enter the server port on which to accept encrypted connections (https).</span></span>

       <span data-ttu-id="6ee13-140">HTTPS è una configurazione facoltativa che può essere impostata per garantire transazioni sicure tra il server MED-V e i client MED-V.</span><span class="sxs-lookup"><span data-stu-id="6ee13-140">Https is an optional configuration which can be set to ensure secure transactions between the MED-V server and MED-V clients.</span></span> <span data-ttu-id="6ee13-141">Per configurare HTTPS, è necessario eseguire le procedure seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ee13-141">To configure https, you must perform the following procedures:</span></span>

       -   <span data-ttu-id="6ee13-142">Configurare un certificato nel server.</span><span class="sxs-lookup"><span data-stu-id="6ee13-142">Configure a certificate on the server.</span></span>

       -   <span data-ttu-id="6ee13-143">Associa il certificato del server alla porta specificata usando netsh.</span><span class="sxs-lookup"><span data-stu-id="6ee13-143">Associate the server certificate with the port specified using netsh.</span></span> <span data-ttu-id="6ee13-144">Per informazioni, vedere le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ee13-144">For information, see the following:</span></span>

           -   [<span data-ttu-id="6ee13-145">Comandi Netsh per HTTP (Hypertext Transfer Protocol)</span><span class="sxs-lookup"><span data-stu-id="6ee13-145">Netsh Commands for Hypertext Transfer Protocol (HTTP)</span></span>](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [<span data-ttu-id="6ee13-146">Procedura: configurare una porta con un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="6ee13-146">How to: Configure a Port with an SSL Certificate</span></span>](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [<span data-ttu-id="6ee13-147">Procedura: configurare una porta con un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="6ee13-147">How to: Configure a Port with an SSL Certificate</span></span>](https://msdn.microsoft.com/library/ms733791.aspx)

3. <span data-ttu-id="6ee13-148">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-148">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringimages"></a><span data-ttu-id="6ee13-149">Configurazione di immagini</span><span class="sxs-lookup"><span data-stu-id="6ee13-149">Configuring Images</span></span>

**<span data-ttu-id="6ee13-150">Per configurare le immagini</span><span class="sxs-lookup"><span data-stu-id="6ee13-150">To configure images</span></span>**

1.  <span data-ttu-id="6ee13-151">Fare clic sulla scheda **Immagini** .</span><span class="sxs-lookup"><span data-stu-id="6ee13-151">Click the **Images** tab.</span></span>

2.  <span data-ttu-id="6ee13-152">Configurare le impostazioni di gestione delle immagini seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ee13-152">Configure the following image management settings:</span></span>

    -   <span data-ttu-id="6ee13-153">**Directory VMS**: directory della macchina virtuale (directory in cui sono archiviate le immagini).</span><span class="sxs-lookup"><span data-stu-id="6ee13-153">**VMs Directory**—The virtual machine directory (the directory where the images are stored).</span></span> <span data-ttu-id="6ee13-154">Questo campo contiene un percorso UNC della directory delle immagini nel server di distribuzione delle immagini che dovrebbe essere accessibile dal server MED-V.</span><span class="sxs-lookup"><span data-stu-id="6ee13-154">This field contains a UNC path to the image directory on the image distribution server that should be accessible from the MED-V server.</span></span>

    -   <span data-ttu-id="6ee13-155">**URL VMS**: la posizione del server in cui sono archiviate le immagini.</span><span class="sxs-lookup"><span data-stu-id="6ee13-155">**VMs URL**—The location of the server where the images are stored.</span></span>

3.  <span data-ttu-id="6ee13-156">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-156">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringpermissions"></a><span data-ttu-id="6ee13-157">Configurazione delle autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="6ee13-157">Configuring Permissions</span></span>

**<span data-ttu-id="6ee13-158">Per configurare le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="6ee13-158">To configure permissions</span></span>**

1.  <span data-ttu-id="6ee13-159">Fare clic sulla scheda **autorizzazioni** .</span><span class="sxs-lookup"><span data-stu-id="6ee13-159">Click the **Permissions** tab.</span></span>

2.  <span data-ttu-id="6ee13-160">È disponibile un elenco di tutti gli utenti che possono eseguire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6ee13-160">A list of all users who can log in is provided.</span></span> <span data-ttu-id="6ee13-161">Per applicare le autorizzazioni di lettura e scrittura a un utente, selezionare la casella di controllo accanto all'utente.</span><span class="sxs-lookup"><span data-stu-id="6ee13-161">To apply read and write permissions to a user, select the check box next to the user.</span></span> <span data-ttu-id="6ee13-162">Per applicare le autorizzazioni di sola lettura a un utente, deselezionare la casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="6ee13-162">To apply read-only permissions to a user, clear the check box.</span></span>

3.  <span data-ttu-id="6ee13-163">Per aggiungere utenti o gruppi di dominio, fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-163">To add domain users or groups, click **Add**.</span></span>

    <span data-ttu-id="6ee13-164">Verrà visualizzata la finestra di dialogo **Immetti nomi utente o di gruppo** .</span><span class="sxs-lookup"><span data-stu-id="6ee13-164">The **Enter User or Group names** dialog box appears.</span></span>

    1.  <span data-ttu-id="6ee13-165">Selezionare utenti o gruppi di dominio eseguendo una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ee13-165">Select domain users or groups by doing one of the following:</span></span>

        -   <span data-ttu-id="6ee13-166">Nel campo **Immetti nomi utente o gruppo** Digitare un utente o un gruppo esistente nel dominio oppure esistere come utente o gruppo locale nel computer.</span><span class="sxs-lookup"><span data-stu-id="6ee13-166">In the **Enter User or Group names** field, type a user or group that exists in the domain or exists as a local user or group on the computer.</span></span> <span data-ttu-id="6ee13-167">Quindi fare clic su **Controlla nomi** per risolverlo con il nome completo esistente.</span><span class="sxs-lookup"><span data-stu-id="6ee13-167">Then click **Check Names** to resolve it to the full existent name.</span></span>

        -   <span data-ttu-id="6ee13-168">Fare clic su **trova** per aprire la finestra di dialogo standard **Seleziona utenti o gruppi** .</span><span class="sxs-lookup"><span data-stu-id="6ee13-168">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="6ee13-169">Quindi Seleziona utenti o gruppi di dominio.</span><span class="sxs-lookup"><span data-stu-id="6ee13-169">Then select domain users or groups.</span></span>

    2.  <span data-ttu-id="6ee13-170">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-170">Click **OK**.</span></span>

4.  <span data-ttu-id="6ee13-171">Per rimuovere utenti o gruppi di dominio, selezionare un utente o un gruppo e fare clic su **Rimuovi**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-171">To remove domain users or groups, select a user or group and click **Remove**.</span></span>

5.  <span data-ttu-id="6ee13-172">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-172">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringreports"></a><span data-ttu-id="6ee13-173">Configurazione di report</span><span class="sxs-lookup"><span data-stu-id="6ee13-173">Configuring Reports</span></span>

**<span data-ttu-id="6ee13-174">Per configurare i report</span><span class="sxs-lookup"><span data-stu-id="6ee13-174">To configure reports</span></span>**

1.  <span data-ttu-id="6ee13-175">Fare clic sulla scheda **report** .</span><span class="sxs-lookup"><span data-stu-id="6ee13-175">Click the **Reports** tab.</span></span>

2.  <span data-ttu-id="6ee13-176">Per supportare i report, selezionare **Abilita report**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-176">To support reports, select **Enable reports**.</span></span>

3.  <span data-ttu-id="6ee13-177">Nella casella **stringa di connessione** immettere una stringa di connessione per il database MSSQL.</span><span class="sxs-lookup"><span data-stu-id="6ee13-177">In the **Connection String** box, enter a connection string for the MSSQL database.</span></span>

    -   <span data-ttu-id="6ee13-178">Quando SQL Server è installato in un server remoto, usare la stringa di connessione seguente:</span><span class="sxs-lookup"><span data-stu-id="6ee13-178">When SQL Server is installed on a remote server, use the following connection string:</span></span>

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **<span data-ttu-id="6ee13-179">Nota</span><span class="sxs-lookup"><span data-stu-id="6ee13-179">Note</span></span>**  
        <span data-ttu-id="6ee13-180">Nota: per connettersi a SQL Express, usare:</span><span class="sxs-lookup"><span data-stu-id="6ee13-180">Note: To connect to SQL Express, use:</span></span> `Data Source=<ServerName>\sqlexpress.`



4.  <span data-ttu-id="6ee13-181">Per creare il database, fare clic su **Crea database**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-181">To create the database, click **Create Database**.</span></span>

5.  <span data-ttu-id="6ee13-182">Per verificare la connessione, fare clic su **Test connessione**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-182">To test the connection, click **Test Connection**.</span></span>

6.  <span data-ttu-id="6ee13-183">Per configurare le opzioni di cancellazione del database, fare clic su **Cancella opzioni**.</span><span class="sxs-lookup"><span data-stu-id="6ee13-183">To configure database clearing options, click **Clear Options**.</span></span>

    <span data-ttu-id="6ee13-184">Verrà visualizzata la finestra di dialogo **Cancella Opzioni database** .</span><span class="sxs-lookup"><span data-stu-id="6ee13-184">The **Clear Database Options** dialog box appears.</span></span>

    1.  <span data-ttu-id="6ee13-185">Scegliere una delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ee13-185">Choose one of the following options:</span></span>

        -   <span data-ttu-id="6ee13-186">**Cancellare i dati antecedenti**: cancellare tutti i dati antecedenti al numero di giorni specificato; nella casella numero immettere un numero di giorni.</span><span class="sxs-lookup"><span data-stu-id="6ee13-186">**Clear data older than**—Clear all data older than the number of days specified; in the number box, enter a number of days.</span></span>

        -   <span data-ttu-id="6ee13-187">**Cancellare tutti i dati da database**: cancellare tutti i dati esistenti nel database.</span><span class="sxs-lookup"><span data-stu-id="6ee13-187">**Clear all data from database**—Clear all existent data in the database.</span></span>

        -   <span data-ttu-id="6ee13-188">**Drop database**: eliminare il database.</span><span class="sxs-lookup"><span data-stu-id="6ee13-188">**Drop database**—Delete the database.</span></span>

    2.  <span data-ttu-id="6ee13-189">Fare clic su **OK** per applicare le modifiche e chiudere la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6ee13-189">Click **OK** to apply changes and close the dialog box.</span></span>

7.  <span data-ttu-id="6ee13-190">Fare clic su **OK** per salvare le modifiche oppure su **Annulla** per chiudere la finestra di dialogo senza salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="6ee13-190">Click **OK** to save the changes, or click **Cancel** to close the dialog box without saving changes.</span></span>

8.  <span data-ttu-id="6ee13-191">Se richiesto, riavviare il servizio server MED-V per applicare le modifiche alle impostazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="6ee13-191">If prompted, restart the MED-V server service to apply changes to the network settings.</span></span>

## <span data-ttu-id="6ee13-192">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ee13-192">Related topics</span></span>


[<span data-ttu-id="6ee13-193">Configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="6ee13-193">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="6ee13-194">Progettare l'infrastruttura del server MED-V</span><span class="sxs-lookup"><span data-stu-id="6ee13-194">Design the MED-V Server Infrastructure</span></span>](design-the-med-v-server-infrastructure.md)









