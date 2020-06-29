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
# Informazioni sulla configurazione dinamica di App-V 5.0


Puoi usare la configurazione dinamica per personalizzare un pacchetto di App-V 5,0 per un utente. Usare le informazioni seguenti per creare o modificare un file di configurazione dinamica esistente.

Quando si modifica il file di configurazione dinamica, viene personalizzato il modo in cui verrà eseguito un pacchetto di App-V 5,0 per un utente o un gruppo. Questo consente di fornire un metodo più comodo per la personalizzazione del pacchetto rimuovendo la necessità di risequenziare i pacchetti usando le impostazioni desiderate e offre un modo per rendere indipendente il contenuto del pacchetto e le impostazioni personalizzate.

## Avanzate: configurazione dinamica


I pacchetti di applicazioni virtuali contengono un manifesto che fornisce tutte le informazioni di base per il pacchetto. Queste informazioni includono i valori predefiniti per le impostazioni del pacchetto e determinano le impostazioni nella maschera più elementare (senza ulteriori personalizzazioni). Per modificare queste impostazioni predefinite per un utente o un gruppo specifico, è possibile creare e modificare i file seguenti:

-   File di configurazione utente

-   File di configurazione della distribuzione

I file XML precedenti specificano le impostazioni del pacchetto e consentono di personalizzare i pacchetti senza influire direttamente sui pacchetti. Quando viene creato un pacchetto, sequencer genera automaticamente file XML di distribuzione e configurazione utente usando i dati del manifesto del pacchetto. Di conseguenza, questi file di configurazione generati automaticamente riflettono semplicemente le impostazioni predefinite che il pacchetto innately come le cose sono state configurate durante la sequenziazione. Se si applicano questi file di configurazione a un pacchetto nella maschera generata dal sequencer, i pacchetti avranno le stesse impostazioni predefinite fornite dal manifesto. In questo articolo viene fornito un modello specifico del pacchetto per iniziare se è necessario modificare una delle impostazioni predefinite.

**Nota**  Le informazioni seguenti possono essere usate solo per modificare i file di configurazione generati da Sequencer per personalizzare i pacchetti in base a requisiti specifici per gli utenti o i gruppi.

 

### Contenuto del file di configurazione dinamica

Tutte le aggiunte, le eliminazioni e gli aggiornamenti nei file di configurazione devono essere eseguiti in relazione ai valori predefiniti specificati dalle informazioni del manifesto del pacchetto. Esaminare la tabella seguente:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>File Configuration. XML dell'utente</p></td>
</tr>
<tr class="even">
<td align="left"><p>File Configuration. XML di distribuzione</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Manifesto del pacchetto</p></td>
</tr>
</tbody>
</table>

 

La tabella precedente rappresenta il modo in cui verranno letti i file. La prima voce rappresenta quello che verrà letto per ultimo, quindi il suo contenuto avrà la precedenza. Di conseguenza, tutti i pacchetti contengono intrinsecamente e includono le impostazioni predefinite del manifesto del pacchetto. Se viene applicato un file Configuration. XML di distribuzione con impostazioni personalizzate, verranno ignorati i valori predefiniti del manifesto del pacchetto. Se prima di tutto viene applicato un file Configuration. XML con impostazioni personalizzate, l'utente eseguirà l'override sia della configurazione della distribuzione che dei valori predefiniti del manifesto del pacchetto.

Nell'elenco seguente vengono visualizzate altre informazioni sui due tipi di file:

-   **File di configurazione utente (userconfig)** : consente di specificare o modificare le impostazioni personalizzate per un pacchetto. Queste impostazioni verranno applicate a un utente specifico quando il pacchetto viene distribuito in un computer che gestisce il client App-V 5,0.

-   **File di configurazione della distribuzione (deploymentconfig)** : consente di specificare o modificare le impostazioni predefinite per un pacchetto. Queste impostazioni verranno applicate a tutti gli utenti quando un pacchetto viene distribuito in un computer che gestisce il client App-V 5,0.

Per personalizzare le impostazioni di un pacchetto per un set specifico di utenti in un computer o per apportare modifiche che verranno applicate alle posizioni degli utenti locali, ad esempio HKCU, deve essere usato il file UserConfig. Per modificare le impostazioni predefinite di un pacchetto per tutti gli utenti di un computer o per apportare modifiche che verranno applicate a posizioni globali come HKEY \ _LOCAL \ _MACHINE e la cartella tutti gli utenti, è necessario usare il file DeploymentConfig.

Il file UserConfig fornisce le impostazioni di configurazione che possono essere applicate a un singolo utente senza influire sugli altri utenti di un client:

-   Estensioni che verranno integrate nel sistema nativo per utente:-scelte rapide, associazioni di tipi di file, protocolli URL, AppPaths, client software e COM

-   Sottosistemi virtuali:-oggetti applicazione, variabili di ambiente, modifiche del registro di sistema, servizi e tipi di carattere

-   Script (solo contesto utente)

-   Autorità di gestione (per controllare la coesistenza del pacchetto con l'App-V 4,6)

Il file DeploymentConfig fornisce le impostazioni di configurazione in due sezioni, uno relativo al contesto del computer e uno relativo al contesto utente che fornisce le stesse funzionalità elencate nell'elenco UserConfig precedente:

-   Tutte le impostazioni UserConfig sopra

-   Estensioni che possono essere applicate solo a livello globale per tutti gli utenti

-   Sottosistemi virtuali che possono essere configurati per le posizioni globali del computer, ad esempio il registro di sistema

-   URL origine prodotto

-   Script (solo contesto computer)

-   Controlli per terminare i processi figlio

### Struttura di file

La struttura del file di configurazione dinamica App-V 5,0 è illustrata nella sezione seguente.

### File di configurazione utente dinamico

**Intestazione** : l'intestazione di un file di configurazione dell'utente dinamico è la seguente.

&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

**PackageID** è lo stesso valore esistente nel file manifesto.

**Corpo** : il corpo del file di configurazione dell'utente dinamico può includere tutti i punti di estensione dell'app definiti nel file manifesto, nonché le informazioni per la configurazione delle applicazioni virtuali. Nel corpo sono consentite quattro sottosezioni:

1. **Applicazioni** -tutte le estensioni delle app contenute nel file manifesto all'interno di un pacchetto vengono assegnate con un ID applicazione, definito anche nel file manifesto. In questo modo è possibile abilitare o disabilitare tutte le estensioni per una determinata applicazione all'interno di un pacchetto. L' **ID applicazione** deve esistere nel file manifesto o verrà ignorato.

   &lt;UserConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Applicazioni&gt;

   &lt;!--Non è possibile definire una nuova applicazione in criteri. Il client AppV ignorerà qualsiasi ID applicazione che non sia anche nel file manifesto.&gt;

   &lt;ID applicazione = "{a56fa627-c35f-4A01-9e79-7d36aed8225a}" Enabled = "false"&gt;

   &lt;/Application&gt;

   &lt;/Applications&gt;

   …

   &lt;/UserConfiguration&gt;

2. **Sottosistemi** -AppExtensions e altri sottosistemi sono disposti come sottonodi sotto i &lt; sottosistemi &gt; :

   &lt;UserConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;

   &lt;Sottosistemi&gt;

   ..

   &lt;/Subsystems&gt;

   ..

   &lt;/UserConfiguration&gt;

   Ogni sottosistema può essere abilitato/disabilitato usando l'attributo "**Enabled**". Di seguito sono riportati i vari sottosistemi e esempi di utilizzo.

   **Estensioni**

   Alcuni sottosistemi (sottosistemi di estensione) controllano le estensioni. Questi sottosistemi sono:-scelte rapide da tastiera, associazioni di tipi di file, protocolli URL, AppPaths, client software e COM

   I sottosistemi di estensione possono essere abilitati e disabilitati indipendentemente dal contenuto.  In questo modo, se i tasti di scelta rapida sono abilitati, il client utilizzerà i collegamenti contenuti nel manifesto per impostazione predefinita. Ogni sottosistema di estensione può contenere &lt; un &gt; nodo Extensions. Se questo elemento figlio è presente, il client ignorerà il contenuto nel file manifesto per il sottosistema e userà solo il contenuto nel file di configurazione.

   Esempio di utilizzo del sottosistema collegamenti:

   1.  Se l'utente ha definito questo contenuto nel file di configurazione dinamico o di distribuzione:

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  Se l'utente ha definito solo le operazioni seguenti:

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  Se l'utente definisce le operazioni seguenti

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   Tutte le scelte rapide all'interno del manifesto verranno comunque ignorate. Non ci saranno tasti di scelta rapida integrati.

   I sottosistemi di estensione supportati sono i seguenti:

   **Scelte rapide:** Questo controlla i tasti di scelta rapida che verranno integrati nel sistema locale. Di seguito è riportato un esempio con due scelte rapide:

   &lt;Sottosistemi&gt;

   &lt;Tasti di scelta rapida abilitati = "vero"&gt;

     &lt;Extensions&gt;

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

     &lt;/Extension&gt;

     &lt;Extension Category = "AppV. Shortcut"&gt;

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

     &lt;/Extension&gt;

    &lt;/Extensions&gt;

   &lt;/Shortcuts&gt;

   **Associazioni di tipi di file:** Associa i tipi di file ai programmi da aprire per impostazione predefinita e imposta il menu di scelta rapida. I tipi MIME possono anche essere impostati tramite questo susbsystem. L'associazione di tipi di file di esempio è seguente:

   &lt;FileTypeAssociations Enabled = "true"&gt;

   &lt;Extensions&gt;

     &lt;Extension Category = "AppV. FileTypeAssociation"&gt;

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

      &lt;/Extension&gt;

     &lt;/Extensions&gt;

     &lt;/FileTypeAssociations&gt;

   **Protocolli URL**: controlla i protocolli URL integrati nel registro di sistema locale del computer client, ad esempio "mailto:".

   &lt;URLProtocols Enabled = "true"&gt;

   &lt;Extensions&gt;

   &lt;Extension Category = "AppV. URLProtocol"&gt;

   &lt;URLProtocol&gt;

     &lt;Nome &gt; mailto &lt; /Name&gt;

     &lt;ApplicationURLProtocol&gt;

     &lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;

     &lt;EditFlags &gt; 2 &lt; /EditFlags&gt;

     &lt;Descrizione&gt;

     &lt;AppUserModelID&gt;

     &lt;FriendlyTypeName /&gt;

     &lt;InfoTip&gt;

   &lt;SourceFilter&gt;

     &lt;ShellFolder&gt;

     &lt;WebNavigableCLSID /&gt;

     &lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;

     &lt;CLSID&gt;

     &lt;ShellCommands&gt;

     &lt;DefaultCommand &gt; Open &lt; /DefaultCommand&gt;

     &lt;ShellCommand&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;

     &lt;Nome &gt; aperto &lt; /Name&gt;

     &lt;CommandLine &gt; \ [{ProgramFilesX86} \\Microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Nota/m "%1" &lt; /CommandLine&gt;

     &lt;DropTargetClassId /&gt;

     &lt;FriendlyName&gt;

     &lt;Extended &gt; 0 &lt; /Extended&gt;

     &lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;

     &lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;

      &lt;DdeExec&gt;

     &lt;NoActivateHandler /&gt;

     &lt;Applicazione &gt; ContosoMail &lt; /Application&gt;

     &lt;Argomento &gt; ShellSystem &lt; /Topic&gt;

     &lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;

     &lt;DdeCommand &gt; \ [seforeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;

     &lt;/DdeExec&gt;

     &lt;/ShellCommand&gt;

     &lt;/ShellCommands&gt;

     &lt;/ApplicationURLProtocol&gt;

     &lt;/URLProtocol&gt;

     &lt;/Extension&gt;

     &lt;/Extension&gt;

     &lt;/URLProtocols&gt;

   **Client software**: consente all'app di registrarsi come client di posta elettronica, lettore di News, lettore multimediale e rende visibile l'app nell'interfaccia utente imposta l'accesso al programma e il computer. Nella maggior parte dei casi è necessario abilitarla e disabilitarla. Esiste anche un controllo che consente di abilitare e disabilitare il client di posta elettronica in modo specifico se si vuole che gli altri client siano ancora abilitati, ad eccezione del client.

   &lt;SoftwareClients Enabled = "true"&gt;

     &lt;ClientConfiguration EmailEnabled = "false"/&gt;

   &lt;/SoftwareClients&gt;

   AppPaths:-se un'applicazione ad esempio contoso.exe è registrata con un nome AppPath "MyApp", ti permette di digitare "MyApp" nel menu Esegui e si aprirà contoso.exe.

   &lt;AppPaths Enabled = "true"&gt;

   &lt;Extensions&gt;

   &lt;Extension Category = "AppV. AppPath"&gt;

   &lt;AppPath&gt;

     &lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;

     &lt;Nome &gt;contosomail.exe&lt; /Name&gt;

     &lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\Microsoft Contoso\\Contoso\\contosomail.EXE&lt; /applicationPath&gt;

     &lt;PATHEnvironmentVariablePrefix /&gt;

     &lt;CanAcceptUrl &gt; false &lt; /CanAcceptUrl&gt;

     &lt;SaveUrl /&gt;

   &lt;/AppPath&gt;

   &lt;/Extension&gt;

   &lt;/Extensions&gt;

   &lt;/AppPaths&gt;

   **Com**: consente a un'applicazione di registrare server COM locali. La modalità può essere integrazione, isolata o disinserita. Quando isol.

   &lt;Modalità COM = "isolata"/&gt;

   **Altre impostazioni**:

   Oltre alle estensioni, gli altri sottosistemi possono essere abilitati/disabilitati e modificati:

   **Oggetti kernel virtuali**:

   &lt;Oggetti abilitati = "falso"/&gt;

   **Registro**di sistema virtuale: usato se si vuole impostare un registro di sistema nel registro di sistema virtuale in HKCU

   &lt;Registro di sistema abilitato = "vero"&gt;

   &lt;Includono&gt;

   &lt;Key path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;

   &lt;Valore Type = "REG \ _SZ" Name = "bar" data = "NewValue"/&gt;

    &lt;/Key&gt;

     &lt;Key path = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;

    &lt;/Include&gt;

   &lt;Eliminare&gt;

     &lt;/Registry&gt;

   **File system virtuale**

         &lt;FileSystem Enabled="true" /&gt;

   **Tipi di carattere virtuali**

         &lt;Fonts Enabled="false" /&gt;

   **Variabili di ambiente virtuali**

   &lt;EnvironmentVariables Enabled = "true"&gt;

   &lt;Includono&gt;

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **Servizi virtuali**

         &lt;Services Enabled="false" /&gt;

3. **Userscripts** -gli script possono essere usati per configurare o modificare l'ambiente virtuale, nonché per eseguire script in fase di distribuzione o rimozione, prima dell'esecuzione di un'applicazione oppure possono essere usati per "pulire" l'ambiente dopo la chiusura dell'applicazione. Fare riferimento a un file di configurazione dell'utente di esempio che viene restituito dal sequencer per visualizzare uno script di esempio. La sezione Scripts seguente fornisce altre informazioni sui vari trigger che possono essere usati.

4. **ManagingAuthority** -può essere usato quando due versioni del pacchetto sono coesistenti nello stesso computer, uno distribuito in App-v 4,6 e l'altro distribuito in App-v 5,0. Per consentire a App-V vNext di assumere i punti di estensione App-V 4,6 per il pacchetto denominato, immettere quanto segue nel file UserConfig (dove PackageName è il GUID del pacchetto in App-V 4,6:

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417C-acef-76fc5297fe81"/&gt;

### File di configurazione della distribuzione dinamica

**Intestazione** -l'intestazione di un file di configurazione della distribuzione è la seguente:

&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

**PackageID** è lo stesso valore esistente nel file manifesto.

**Body** -il corpo del file di configurazione della distribuzione include due sezioni:

-   Sezione Configurazione utente: consente lo stesso contenuto del file di configurazione dell'utente descritto nella sezione precedente. Quando il pacchetto viene pubblicato in un utente, tutte le impostazioni di configurazione di appextensions in questa sezione sovrascriveranno le impostazioni del manifesto all'interno del pacchetto, a meno che non venga fornito anche un file di configurazione dell'utente. Se viene fornito anche un file UserConfig, verrà usato al posto delle impostazioni utente nel file di configurazione della distribuzione. Se il pacchetto viene pubblicato globalmente, in combinazione con il manifesto verrà usato solo il contenuto del file di configurazione della distribuzione.

-   Sezione Configurazione computer: contiene informazioni che possono essere configurate solo per un intero computer, non per un utente specifico nel computer. Ad esempio, HKEY \ _LOCAL \ _MACHINE le chiavi del registro di sistema in VFS.

&lt;DeploymentConfiguration **PackageID**= "1F8488bf-2257-46b4-B27F-09c9dbaae707" DisplayName = "riservato" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;

&lt;UserConfiguration&gt;

  ..

&lt;/UserConfiguration&gt;

&lt;MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

..

&lt;/MachineConfiguration&gt;

&lt;/DeploymentConfiguration&gt;

**Configurazione utente** : usare la sezione **file di configurazione utente dinamico** precedente per informazioni sulle impostazioni disponibili nella sezione Configurazione utente del file di configurazione della distribuzione.

Configurazione del computer: la sezione configurazione macchina del file di configurazione della distribuzione viene usata per configurare le informazioni che possono essere impostate solo per un intero computer, non per un utente specifico nel computer. Ad esempio, HKEY \ _LOCAL \ _MACHINE chiavi del registro di sistema nel registro di sistema virtuale. In questo elemento sono consentite quattro sottosezioni

1.  **Sottosistemi** -AppExtensions e altri sottosistemi sono disposti come sottonodi in &lt; sottosistemi &gt; :

    &lt;MachineConfiguration&gt;

      &lt;Sottosistemi&gt;

      ..

      &lt;/Subsystems&gt;

    ..

    &lt;/MachineConfiguration&gt;

    Nella sezione seguente vengono visualizzati i vari sottosistemi e gli esempi di utilizzo.

    **Estensioni**:

    Alcuni sottosistemi (sottosistemi di estensione) controllano le estensioni che possono essere applicate solo a tutti gli utenti. Il sottosistema è funzionalità dell'applicazione. Poiché questa operazione può essere applicata solo a tutti gli utenti, il pacchetto deve essere pubblicato globalmente in modo che questo tipo di estensione venga integrato nel sistema locale. Le stesse regole per i controlli e le impostazioni applicabili alle estensioni della configurazione utente si applicano anche a quelle nella sezione MachineConfiguration.

    **Funzionalità delle applicazioni**: usate dai programmi predefiniti nell'interfaccia del sistema operativo Windows. Consente a un'applicazione di registrarsi come in grado di aprire determinate estensioni di file, come contendente per lo slot del browser Internet del menu Start, in grado di aprire determinati tipi MIME di Windows.Questa estensione rende inoltre visibile l'applicazione virtuale nell'interfaccia utente imposta programmi predefiniti.:

    &lt;ApplicationCapabilities Enabled = "true"&gt;

      &lt;Extensions&gt;

       &lt;Extension Category = "AppV. ApplicationCapabilities"&gt;

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       &lt;CapabilityGroup&gt;

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

      &lt;/CapabilityGroup&gt;

       &lt;/ApplicationCapabilities&gt;

      &lt;/Extension&gt;

    &lt;/Extensions&gt;

    &lt;/ApplicationCapabilities&gt;

    **Altre impostazioni**:

    Oltre alle estensioni, è possibile modificare altri sottosistemi:

    **Registro**di sistema virtuale a livello di computer: usato quando si vuole impostare una chiave del registro di sistema nel registro di sistema virtuale in HKEY \ _Local \ _Machine

    &lt;Registro di sistema&gt;

    &lt;Includono&gt;

      &lt;Key path = "\\REGISTRY\\Machine\\Software\\ABC"&gt;

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       &lt;/Key&gt;

      &lt;Key path = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;

     &lt;/Include&gt;

    &lt;Eliminare&gt;

    &lt;/Registry&gt;

    **Oggetti kernel virtuali a livello di computer**

    &lt;Oggetti&gt;

    &lt;NotIsolate&gt;

       &lt;Object Name = "testObject"/&gt;

     &lt;/NotIsolate&gt;

    &lt;/Objects&gt;

2.  **ProductSourceURLOptOut**: indica se l'URL del pacchetto può essere modificato globalmente tramite PackageSourceRoot (per supportare scenari di succursale). Il valore predefinito è false e la modifica dell'impostazione diventa effettiva per il successivo avvio.  

    &lt;MachineConfiguration&gt;

      .. 

      &lt;ProductSourceURLOptOut Enabled = "true"/&gt;

      ..

    &lt;/MachineConfiguration&gt;

3.  **MachineScripts** -il pacchetto può essere configurato per eseguire script in fase di distribuzione, pubblicazione o rimozione. Fare riferimento a un file di configurazione della distribuzione di esempio generato dal sequencer per visualizzare uno script di esempio. La sezione Scripts seguente fornisce altre informazioni sui vari trigger che possono essere usati

4.  **TerminateChildProcess**:-è possibile specificare un file eseguibile dell'applicazione, i cui processi figlio verranno terminati quando il processo exe dell'applicazione viene terminato.

    &lt;MachineConfiguration&gt;

      ..   

      &lt;TerminateChildProcesses&gt;

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      &lt;/TerminateChildProcesses&gt;

      ..

    &lt;/MachineConfiguration&gt;

### Script

La tabella seguente descrive i vari eventi di script e il contesto in cui possono essere eseguiti.

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
<th align="left">Tempo di esecuzione degli script</th>
<th align="left">Può essere specificato nella configurazione di distribuzione</th>
<th align="left">Può essere specificato nella configurazione utente</th>
<th align="left">Può essere eseguito nell'ambiente virtuale del pacchetto</th>
<th align="left">Può essere eseguito nel contesto di un'applicazione specifica</th>
<th align="left">Viene eseguito in contesto sistema/utente: (configurazione della distribuzione, configurazione utente)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>AddPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SISTEMA, N/D)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Sistema; utente)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UnpublishPackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Sistema; utente)</p></td>
</tr>
<tr class="even">
<td align="left"><p>RemovePackage</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(SISTEMA, N/D)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartProcess quale nome</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Utente, utente)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ExitProcess</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>(Utente, utente)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>StartVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Utente, utente)</p></td>
</tr>
<tr class="even">
<td align="left"><p>TerminateVirtualEnvironment</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p>X</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>(Utente, utente)</p></td>
</tr>
</tbody>
</table>

 

### Creare un file di configurazione dinamica usando un file manifesto di App-V 5,0

Puoi creare il file di configurazione dinamica usando uno dei tre metodi seguenti: manualmente, usando la console di gestione di App-V 5,0 o sequenziando un pacchetto, che verrà generato con due file di esempio.

Per altre informazioni su come creare il file usando la console di gestione di App-V 5,0, vedere [come creare un file di configurazione personalizzato usando la console di gestione di App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

Per creare il file manualmente, è possibile combinare le informazioni di cui sopra nelle sezioni precedenti in un singolo file. Ti consigliamo di usare i file generati dal sequencer.






## Argomenti correlati


[Come applicare il file di configurazione della distribuzione con PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[Come applicare il file di configurazione utente con PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





