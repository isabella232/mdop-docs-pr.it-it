---
title: Creare un pacchetto nell'area di lavoro MED-V
description: Creare un pacchetto nell'area di lavoro MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823265"
---
# Creare un pacchetto nell'area di lavoro MED-V


Un'area di lavoro MED-V è l'ambiente desktop Windows XP in cui gli utenti finali interagiscono con la macchina virtuale fornita da MED-V. L'amministratore crea e Personalizza l'area di lavoro MED-V. L'area di lavoro è costituita da un'immagine e da criteri di gruppo che definiscono le regole e le funzionalità dell'area di lavoro MED-V.

È possibile creare più aree di lavoro MED-V, ognuna personalizzata con la propria configurazione, le impostazioni e le regole. Un utente, un gruppo o più utenti o gruppi può essere associato a ogni area di lavoro MED-V. La personalizzazione rende disponibile l'area di lavoro MED-V solo per l'utente o il gruppo.

USA **Packager area di lavoro MED-v** per creare aree di lavoro MED-v. Il **Packager area di lavoro MED-V** è suddiviso in due sezioni principali:

-   Pannello principale che include tre pulsanti che si usano per creare e gestire aree di lavoro MED-V. Il pulsante **Crea un pacchetto di area di lavoro MED-v** apre la **procedura guidata Crea pacchetto area di lavoro MED-v** che si usa per creare le aree di lavoro MED-v.

-   **Centro assistenza** sul lato destro della finestra che fornisce informazioni e indicazioni utili per creare, testare e gestire le aree di lavoro MED-V.

**Importante**  
Prima di poter usare **Packager area di lavoro MED-V**, devi prima di tutto verificare che il criterio di esecuzione di Windows PowerShell sia impostato su senza restrizioni.

`Set-ExecutionPolicy Unrestricted`

Inoltre, il criterio SAN per il computer in cui viene eseguito il **Packager area di lavoro MED-V** deve essere impostato su "online All". Per controllare l'impostazione del criterio SAN, eseguire i comandi seguenti in un prompt dei comandi con credenziali amministrative:

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

Se necessario, modificare i criteri di SAN in "online All" digitando i comandi seguenti al prompt dei comandi con le credenziali amministrative:

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**Importante**  
Se nel computer che si usa per montare il disco rigido virtuale e creare il pacchetto di area di lavoro MED-V è installato il software di crittografia automatica del disco, è necessario disabilitare il software prima di iniziare. In caso contrario, non è possibile usare l'area di lavoro MED-V in un altro computer.



Le informazioni fornite in questo articolo consentono di creare il pacchetto di distribuzione dell'area di lavoro MED-V.

## <a href="" id="bkmk-prereq"></a>Prerequisiti


Prima di iniziare a creare il pacchetto di distribuzione dell'area di lavoro MED-V, verificare di avere accesso agli elementi seguenti:

-   **Immagine di Windows XP preparata**

    Per altre informazioni su come creare un'immagine di Windows XP da usare con MED-V, vedere [preparare un'immagine MED-v](prepare-a-med-v-image.md).

-   **Un file di testo o un elenco che contiene informazioni sul reindirizzamento degli URL**

    Il file di testo o l'elenco di reindirizzamento degli URL contiene gli URL che vuoi reindirizzare dal computer host a Internet Explorer nell'area di lavoro MED-V. Quando si usa la creazione guidata pacchetti per creare l'area di lavoro MED-V, è possibile importare, digitare o copiare e incollare queste informazioni di reindirizzamento come uno dei passaggi del processo di creazione del pacchetto.

    **Nota**  
    Il reindirizzamento degli URL in MED-V supporta solo i protocolli HTTP e HTTPS. MED-V non offre il supporto per FTP o altri protocolli.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## Creazione di un'area di lavoro MED-V per una lingua diversa da quella del computer Packager dell'area di lavoro MED-V


Per impostazione predefinita, l'area di lavoro MED-V supporta i caratteri sia nella lingua del computer che in inglese. Per creare un'area di lavoro MED-V per una lingua diversa da quella installata nel computer, specificare **-loc \ [locale \]** nello script di PowerShell (. ps1) dopo il nome dell'area di lavoro MED-v.

Per creare un pacchetto di area di lavoro MED-V in una lingua diversa da quella predefinita del computer Packager area di lavoro MED-V, genera uno script nella lingua predefinita eseguendo il Packager area di lavoro MED-V e quindi modificando lo script di output come richiesto per le impostazioni locali. Lo script si trova nella directory di output dell'area di lavoro MED-V specificata durante l'imballaggio. I nomi delle impostazioni locali si trovano in. File di WXL nella directory seguente:

C:\\Programmi \\Programmi\\microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale

## Creazione di un pacchetto di area di lavoro MED-V


Per creare un pacchetto di area di lavoro MED-V, eseguire le operazioni seguenti:

****

1.  Per aprire **Packager area di lavoro MED-v**, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **virtualizzazione desktop Microsoft Enterprise**e quindi fare clic su **Packager area di lavoro MED-v**.

2.  Nel pannello principale di Packager **area di lavoro MED-v** fare clic su **Crea un pacchetto area di lavoro MED-v**.

    Viene visualizzata la **creazione guidata pacchetto area di lavoro MED-v create Med-v** . La procedura guidata è composta dalle pagine seguenti:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Informazioni sul pacchetto</strong></p></td>
    <td align="left"><p>Specificare un nome per l'area di lavoro MED-V e selezionare una cartella in cui vengono salvati i file del pacchetto dell'area di lavoro MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Selezionare l'immagine di Windows XP</strong></p></td>
    <td align="left"><p>Specifica l'immagine del PC virtuale di Windows XP preparata.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Configurazione per la prima volta</strong></p></td>
    <td align="left"><p>Specificare il processo di configurazione che MED-V segue durante la configurazione per la prima volta.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Messaggi di MED-V</strong></p></td>
    <td align="left"><p>Specificare i messaggi e l'URL facoltativo per le informazioni della guida che l'utente finale Visualizza durante la configurazione per la prima volta.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Denominazione dei computer</strong></p></td>
    <td align="left"><p>Specificare la modalità di denominazione della macchina virtuale MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Copiare le impostazioni dall'host</strong></p></td>
    <td align="left"><p>Specificare la modalità di definizione delle impostazioni per l'area di lavoro MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Avvio e networking</strong></p></td>
    <td align="left"><p>Specificare le impostazioni per l'avvio dell'area di lavoro MED-V, della rete e delle credenziali utente.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Reindirizzamento Web</strong></p></td>
    <td align="left"><p>Specificare un file di testo o un elenco degli URL che si vuole reindirizzare a Internet Explorer nell'area di lavoro MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Riepilogo</strong></p></td>
    <td align="left"><p>Verificare le impostazioni dell'area di lavoro MED-V e iniziare a creare il pacchetto di distribuzione dell'area di lavoro MED-V.</p></td>
    </tr>
    </tbody>
    </table>



3.  Nella pagina **informazioni pacchetto** immettere un nome per l'area di lavoro MED-v e selezionare una cartella in cui vengono salvati i file del pacchetto dell'area di lavoro MED-v.

    **Warning**  
    È necessario assegnare un nome all'area di lavoro MED-V e specificare una cartella per continuare.



~~~
After you have finished, click **Next**.
~~~

4. Nella pagina **selezionare l'immagine di Windows XP** specificare la posizione dell'immagine PC virtuale di Windows XP preparata (file con estensione VHD).

   **Warning**  
   Per continuare, devi specificare un'immagine VHD di Windows XP.



~~~
After you have finished, click **Next**.
~~~

5. Nella pagina **configurazione per la prima volta** , selezionare se si vuole che venga eseguita la configurazione prima volta durante la fase di partecipazione o automatica e se si vuole che l'area di lavoro MED-V venga usata separatamente o usata da tutti gli utenti finali in un computer condiviso.

   Se si seleziona **configurazione automatica, senza alcuna notifica**, l'utente finale non viene informato prima dell'esecuzione della configurazione iniziale e la macchina virtuale non viene visualizzata all'utente finale durante la configurazione del primo tempo. Inoltre, la pagina **messaggi MED-V** della procedura guidata è nascosta perché non è necessario alcun messaggio se la configurazione iniziale viene eseguita in modalità completamente automatica.

   Se selezioni la **configurazione automatica, ma avvisa gli utenti finali prima che inizi la configurazione iniziale**, l'utente finale viene informato prima che venga eseguita la configurazione per la prima volta. Tuttavia, la macchina virtuale non viene visualizzata all'utente finale durante la configurazione per la prima volta.

   Selezionare **configurazione assistita** se l'utente finale deve immettere le informazioni durante la configurazione per la prima volta.

   Il comportamento predefinito è la **configurazione automatica, ma avvisa gli utenti finali prima**dell'inizio della configurazione iniziale.

   **Attenzione**  
   Se è stato creato il file Sysprep. inf in modo che la configurazione minima richiedesse l'input dell'utente per il completamento, è necessario selezionare **configurazione assistita** o potrebbero verificarsi problemi durante la configurazione per la prima volta.



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. Nella pagina **messaggi MED-V** specificare i messaggi seguenti che l'utente finale vedrà durante la configurazione per la prima volta:

   -   Messaggio visualizzato dall'utente finale al momento dell'avvio della configurazione iniziale.

   -   Messaggio che viene visualizzato dall'utente finale se la configurazione per la prima volta non riesce o si verifica un errore.

   **Nota**  
   La pagina **messaggi MED-V** della procedura guidata è nascosta se è stata selezionata l'opzione **installazione automatica, senza alcuna notifica** nella **prima** pagina di configurazione.



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. Nella pagina **Naming Computers** è possibile specificare se la denominazione del computer è gestita da MED-V o da uno strumento di gestione del sistema, ad esempio Sysprep. L'impostazione predefinita è che la denominazione dei computer è gestita da uno strumento di gestione del sistema.

   Se specifichi che la denominazione del computer è gestita da MED-V, seleziona una convenzione di denominazione del computer (mask) predefinita nell'elenco a discesa. Verrà visualizzata un'anteprima di un nome di computer di esempio basato sul computer in uso per compilare il pacchetto dell'area di lavoro MED-V.

   Se si seleziona una delle convenzioni di denominazione personalizzate, i campi che è possibile specificare sono limitati ai caratteri seguenti:

   -   I campi prefisso e suffisso sono limitati ai caratteri a-Z, a-z, 0-9 e ai caratteri speciali. @ \ # $% ^ & ()-\ _' {}. e ~.

   -   I campi hostname e username sono limitati alle cifre da 0 a 9.

   **Importante**  
   I nomi dei computer devono essere univoci e limitati a un massimo di 15 caratteri. Quando si decide il metodo di denominazione del computer, considerare gli utenti finali che hanno più computer o che condividono un computer ed evitare di usare maschere di nomi di computer che potrebbero causare una collisione in rete.



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. Nella pagina **Copia impostazioni da host** è possibile selezionare le impostazioni seguenti per specificare il modo in cui è configurata l'area di lavoro MED-V:

   **Attenzione**  
   Le impostazioni specificate in questa pagina che vengono copiate dal computer host all'area di lavoro MED-V eseguono l'override di quelle specificate nel file di risposte Sysprep. inf.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. Nella pagina **avvio e networking** è possibile modificare il comportamento predefinito per le impostazioni seguenti:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Avviare l'area di lavoro MED-V</strong></p></td>
   <td align="left"><p>Scegliere se avviare l'area di lavoro MED-V all'accesso dell'utente, al primo utilizzo o per consentire all'utente finale di decidere quando viene avviata l'area di lavoro MED-v.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>L'area di lavoro MED-V viene avviata in uno dei due modi seguenti: quando l'utente finale accede o quando avvia un'azione che richiede MED-V, ad esempio l'apertura di un'applicazione pubblicata o l'immissione di un URL che richiede il reindirizzamento.</p>
   <p>Puoi definire questa impostazione per l'utente finale o lasciare che l'utente finale controlli l'avvio di MED-V.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Se specifichi che l'utente finale decide, il comportamento predefinito che provano è che l'area di lavoro MED-V viene avviata quando si collegano. Possono modificare l'impostazione predefinita facendo clic con il pulsante destro del mouse sull'icona MED-V nell'area di notifica e selezionando <strong> impostazioni utente Med-v </strong> . Se si definisce questa impostazione per l'utente finale, non è possibile modificare la modalità di avvio di MED-V.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Reti</strong></p></td>
   <td align="left"><p>Selezionare <strong> condivisi </strong> o <strong> Bridged </strong> per l'impostazione di rete. Il valore predefinito è <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Condivisa </strong> - l'area di lavoro MED-V USA NAT (Network Address Translation) per condividere l'host&#39;s IP per il traffico in uscita.</p>
   <p><strong>Bridged </strong> - l'area di lavoro MED-V ha un proprio indirizzo di rete, in genere ottenuto tramite DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Credenziali dello Store</strong></p></td>
   <td align="left"><p>Scegliere se si desidera archiviare le credenziali dell'utente finale.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Il comportamento predefinito è che l'archiviazione delle credenziali è disabilitata in modo che l'utente finale debba essere autenticato ogni volta che accede.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Anche se la memorizzazione nella cache delle credenziali dell'utente finale offre la migliore esperienza utente, dovresti essere consapevole dei rischi.</p>
   <p>Le credenziali di dominio dell'utente finale sono archiviate in un formato reversibile in Gestione credenziali di Windows. Di conseguenza, un utente malintenzionato potrebbe scrivere un programma che recupera la password e potrebbe avere accesso alle credenziali dell'utente. È possibile ridurre questo rischio solo disabilitando l'archiviazione delle credenziali degli utenti finali.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. Nella pagina di Reindirizzamento **Web** è possibile immettere, incollare o importare un elenco degli URL reindirizzati a Internet Explorer nell'area di lavoro MED-V. Per altre informazioni su come configurare le informazioni di reindirizzamento degli URL, vedere [prerequisiti](#bkmk-prereq).

   È anche possibile specificare la modalità di configurazione di Internet Explorer nell'area di lavoro MED-V per gli utenti finali. Per impostazione predefinita, il livello di sicurezza dell'area Internet è impostato su elevato. Vengono inoltre rimosse alcune funzionalità di esplorazione predefinite, ad esempio la barra degli indirizzi. Questa configurazione predefinita di Internet Explorer nell'area di lavoro MED-V offre un ambiente di esplorazione più sicuro per gli utenti finali.

   **Attenzione**  
   Modificando le impostazioni predefinite, è possibile personalizzare Internet Explorer nell'area di lavoro MED-V. Tuttavia, renditi conto che se modifichi le impostazioni predefinite per renderle meno sicure, puoi esporre l'organizzazione a questi rischi per la sicurezza presenti nelle versioni precedenti di Internet Explorer. Per altre informazioni, vedere [procedure consigliate per la sicurezza per le operazioni MED-V](security-best-practices-for-med-v-operations.md).



~~~
After you have finished, click **Next**.
~~~

11. Nella pagina di **Riepilogo** è possibile esaminare le impostazioni di creazione di pacchetti per l'area di lavoro MED-V. Se si vogliono modificare le impostazioni, fare clic sul pulsante **precedente** per tornare alla pagina pertinente. Dopo aver completato la revisione delle impostazioni, fare clic su **Crea**.

   Verrà visualizzata la pagina **completamento** della **procedura guidata Crea pacchetto area di lavoro MED-V** per mostrare lo stato di avanzamento della creazione del pacchetto.

   **Nota**  
   Il processo di creazione del pacchetto dell'area di lavoro MED-V potrebbe richiedere diversi minuti per il completamento, a seconda delle dimensioni del VHD specificato.



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. Fare clic su **Chiudi** per chiudere la creazione guidata pacchetti e tornare al **Packager area di lavoro MED-V**.

Il pacchetto dell'area di lavoro MED-V è ora pronto per il test prima della distribuzione.

## Argomenti correlati


[Configurazione delle impostazioni avanzate con Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md)

[Test del pacchetto nell'area di lavoro MED-V](testing-the-med-v-workspace-package.md)

[Creare un'immagine MED-V](prepare-a-med-v-image.md)









