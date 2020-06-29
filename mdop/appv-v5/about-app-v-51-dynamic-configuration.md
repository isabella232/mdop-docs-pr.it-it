---
title: Informazioni sulla configurazione dinamica di App-V 5,1
description: Puoi usare la configurazione dinamica per personalizzare un pacchetto di App-V 5,1 per un utente. Usare le informazioni seguenti per creare o modificare un file di configurazione dinamica esistente.
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/28/2018
ms.author: dansimp
ms.openlocfilehash: ec8a25da6e139ac329810b1e04f7097cadaa6ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814965"
---
# Informazioni sulla configurazione dinamica di App-V 5,1 
Con la configurazione dinamica, è possibile modificare il file di configurazione dinamica per personalizzare il modo in cui viene eseguito un pacchetto di App-V 5,1 per un utente o un gruppo. La personalizzazione del pacchetto Elimina la necessità di risequenziare i pacchetti usando le impostazioni desiderate.  Offre anche un modo per proteggere il contenuto del pacchetto e le impostazioni personalizzate indipendentemente.

I pacchetti di applicazioni virtuali contengono un manifesto che fornisce tutte le informazioni di base per il pacchetto. Queste informazioni includono i valori predefiniti per le impostazioni del pacchetto e determinano le impostazioni nella maschera più elementare (senza ulteriori personalizzazioni). 

Quando viene creato un pacchetto, il sequencer genera automaticamente i file XML di distribuzione e configurazione utente usando i dati del manifesto del pacchetto. Di conseguenza, questi file generati riflettono le impostazioni predefinite configurate durante la sequenziazione. Se si applicano questi file a un pacchetto nella maschera generata dal sequencer, i pacchetti hanno le stesse impostazioni predefinite fornite dal manifesto. 

Usa questi file generati per apportare modifiche, se necessario, che non influiscono direttamente sul pacchetto. Se si vogliono aggiungere, eliminare o aggiornare i file di configurazione, apportare le modifiche relative ai valori predefiniti nelle informazioni del manifesto.

>[!TIP]
>Ordine in cui i file sono letti:<ul><li>UserConfig.xml</li><li>DeploymentConfig.xml</li><li>Manifesto</li></ul><p>La prima voce rappresenta ciò che viene letto per ultimo. Di conseguenza, il suo contenuto ha la precedenza e tutti i pacchetti contengono intrinsecamente e includono le impostazioni predefinite del manifesto del pacchetto.<ol><li> Se si Personalizza il file DeploymentConfig.xml e si applicano le impostazioni personalizzate, le impostazioni predefinite nel manifesto del pacchetto vengono ignorate. </li><li> Se si Personalizza la UserConfig.xml e si applicano le impostazioni personalizzate, le impostazioni predefinite per la configurazione della distribuzione e il manifesto del pacchetto vengono ignorate. </li></ol>

## Contenuto del file di configurazione utente (UserConfig.xml)
Il file UserConfig fornisce le impostazioni di configurazione che vengono applicate a un utente specifico quando si distribuisce il pacchetto in un computer che esegue il client App-V 5,1.  Queste impostazioni non influiscono sugli altri utenti del client.

Usare il file UserConfig per specificare o modificare le impostazioni personalizzate per un pacchetto:

-   Estensioni integrate nel sistema nativo per utente: scelte rapide, associazioni di tipi di file, protocolli URL, AppPaths, client software e COM
-   Sottosistemi virtuali: oggetti applicazione, variabili di ambiente, modifiche del registro di sistema, servizi e tipi di carattere
-   Script (solo contesto utente)
-   Autorità di gestione (per controllare la coesistenza del pacchetto con l'App-V 4,6)

### Intestazione

L'intestazione di un file di configurazione utente dinamico ha un aspetto simile al seguente:

```xml
<?xml version="1.0" encoding="utf-8"?><UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">
```

**PackageID** è lo stesso valore esistente nel file manifesto.


### Corpo

Il corpo del file di configurazione dell'utente dinamico può includere tutti i punti di estensione dell'app definiti nel file manifesto, oltre a informazioni per configurare le applicazioni virtuali. Nel corpo sono consentite quattro sottosezioni:

1.  **[Applicazioni](#applications)** 
2.  **[Sottosistemi](#subsystems)**
3.  **[UserScripts](#userscripts)**
4.  **[ManagingAuthority](#managingauthority)**

#### Applicazioni

Tutte le estensioni delle app contenute nel file manifesto all'interno di un pacchetto hanno un ID applicazione assegnato, che si trova nel file manifesto. L'ID applicazione consente di abilitare o disabilitare tutte le estensioni per una determinata applicazione all'interno di un pacchetto. L'ID applicazione deve esistere nel file manifesto o viene ignorato.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved"  xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Applications>

<!--No new application can be defined in policy. AppV Client will ignore any application ID that is not also in the Manifest file-->

<Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false">

</Application>

</Applications>

..

</UserConfiguration>
```

#### Sottosistemi

AppExtensions e altri sottosistemi disposti come sottonodi.

```XML
<UserConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/userconfiguration">

<Subsystems>

..

</Subsystems>

..

</UserConfiguration>
```

Puoi abilitare o disabilitare ogni sottosistema usando l'attributo **Enabled** .

**Extensions** 

Alcuni sottosistemi (sottosistemi di estensione) controllano le estensioni. Questi sottosistemi sono collegamenti, associazioni di tipi di file, protocolli URL, AppPaths, client software e COM.

I sottosistemi di estensione possono essere abilitati e disabilitati indipendentemente dal contenuto. Ad esempio, se attivi i tasti di scelta rapida, il client usa i tasti di scelta rapida contenuti nel manifesto per impostazione predefinita. Ogni sottosistema di estensione può contenere un \<Extensions\> nodo. Se questo elemento figlio è presente, il client ignora il contenuto nel file manifesto per il sottosistema e usa solo il contenuto nel file di configurazione. 

_**Esempi:**_ 

- Se si definisce questa opzione nel file di configurazione dell'utente o della distribuzione, il contenuto del manifesto viene ignorato.

  ```XML

  <Shortcuts  Enabled="true"\>

  <Extensions>

  ...

  </Extensions>

  </Shortcuts>
  ```
- Se si definiscono solo le operazioni seguenti, il contenuto del manifesto viene integrato durante la pubblicazione.

  ```XML

  <Shortcuts  Enabled="true"/>
  ```

- Se si definiscono le operazioni seguenti, tutti i tasti di scelta rapida all'interno del manifesto vengono ignorati. In altre parole, le scelte rapide non vengono integrate.

  ```XML

  <Shortcuts  Enabled="true">

     <Extensions/>

  </Shortcuts>
  ```

_**Sottosistemi di estensione supportati:**_ 

Il sottosistema delle estensioni di **tasti di scelta rapida** controlla quali scelte rapide vengono integrate nel sistema locale.  

```XML

<Subsystems>

<Shortcuts Enabled="true">

  <Extensions>

    <Extension Category="AppV.Shortcut">

      <Shortcut>

        <File>[{Common Programs}]\Microsoft Contoso\Microsoft ContosoApp Filler 2010.lnk</File>

        <Target>[{PackageRoot}]\Contoso\ContosoApp.EXE</Target>


      <Icon>[{Windows}]\Installer\{90140000-0011-0000-0000-0000000FF1CE}\inficon.exe</Icon>

        <Arguments />

        <WorkingDirectory />

        <AppUserModelId>ContosoApp.Filler.3</AppUserModelId>

        <Description>Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.</Description>

        <Hotkey>0</Hotkey>

        <ShowCommand>1</ShowCommand>

      <ApplicationId>[{PackageRoot}]\Contoso\ContosoApp.EXE</ApplicationId>

      </Shortcut>

  </Extension>

  <Extension Category="AppV.Shortcut">

    <Shortcut>

    <File>[{AppData}]\Microsoft\Contoso\Recent\Templates.LNK</File>

      <Target>[{AppData}]\Microsoft\Templates</Target>

      <Icon />

      <Arguments />

      <WorkingDirectory />

      <AppUserModelId />

      <Description />

      <Hotkey>0</Hotkey>

      <ShowCommand>1</ShowCommand>

      <!-- Note the ApplicationId is optional -->

    </Shortcut>

  </Extension>

 </Extensions>

</Shortcuts>
```

**File-Type Associates** Extension Subsystem associa i tipi di file ai programmi da aprire per impostazione predefinita, nonché la configurazione del menu di scelta rapida. 

>[!TIP]
>Puoi configurare il sottosistema con i tipi MIME.

```XML

<FileTypeAssociations Enabled="true">

<Extensions>

  <Extension Category="AppV.FileTypeAssociation">

    <FileTypeAssociation>

      <FileExtension MimeAssociation="true">

      <Name>.docm</Name>

      <ProgId>contosowordpad.DocumentMacroEnabled.12</ProgId>

      <PerceivedType>document</PerceivedType>

    <ContentType>application/vnd.ms-contosowordpad.document.macroEnabled.12</ContentType>

      <OpenWithList>

        <ApplicationName>wincontosowordpad.exe</ApplicationName>

      </OpenWithList>

     <OpenWithProgIds>

        <ProgId>contosowordpad.8</ProgId>

      </OpenWithProgIds>

      <ShellNew>

        <Command />

        <DataBinary />

        <DataText />

        <FileName />

        <NullFile>true</NullFile>

        <ItemName />

        <IconPath />

        <MenuText />

        <Handler />

      </ShellNew>

    </FileExtension>

    <ProgId>

       <Name>contosowordpad.DocumentMacroEnabled.12</Name>

      <DefaultIcon\>[{Windows}]\Installer\{90140000-0011-0000-0000-000000FF1CE}\contosowordpadicon.exe,15</DefaultIcon>

        <Description>Blah Blah Blah</Description>

        <FriendlyTypeName>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,9182</FriendlyTypeName>

        <InfoTip>[{FOLDERID_ProgramFilesX86}]\Microsoft Contoso 14\res.dll,1424</InfoTip>

        <EditFlags>0</EditFlags>

        <ShellCommands>

          <DefaultCommand>Open</DefaultCommand>

          <ShellCommand>

           <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

             <Name>Edit</Name>

             <FriendlyName>&Edit</FriendlyName>

           <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /vu "%1"</CommandLine>

          </ShellCommand>

          </ShellCommand>

          <ApplicationId>{e56fa627-c35f-4a01-9e79-7d36aed8225a}</ApplicationId>

            <Name>Open</Name>

            <FriendlyName>&Open</FriendlyName>

            <CommandLine>"[{PackageRoot}]\Contoso\WINcontosowordpad.EXE" /n "%1"</CommandLine>

            <DropTargetClassId />

            <DdeExec>

              <Application>mscontosowordpad</Application>

              <Topic>ShellSystem</Topic>

              <IfExec>[SHELLNOOP]</IfExec>

              <DdeCommand>[SetForeground][ShellNewDatabase"%1"]</DdeCommand>

            </DdeExec>

          </ShellCommand>

        </ShellCommands>

      </ProgId>

     </FileTypeAssociation>

   </Extension>

  </Extensions>

  </FileTypeAssociations>
```

Il sottosistema estensioni **protocolli URL** controlla i protocolli URL integrati nel registro locale del computer client, ad esempio _mailto:_. 

```XML

<URLProtocols Enabled="true">

<Extensions>

<Extension Category="AppV.URLProtocol">

<URLProtocol>

  <Name>mailto</Name>

  <ApplicationURLProtocol>

  <DefaultIcon>[{ProgramFilesX86}]\MicrosoftContoso\Contoso\contosomail.EXE,-9403</DefaultIcon>

  <EditFlags>2</EditFlags>

  <Description />

  <AppUserModelId />

  <FriendlyTypeName />

  <InfoTip />

<SourceFilter />

  <ShellFolder />

  <WebNavigableCLSID />

  <ExplorerFlags>2</ExplorerFlags>

  <CLSID />

  <ShellCommands>

  <DefaultCommand>open</DefaultCommand>

  <ShellCommand>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>open</Name>

  <CommandLine>[{ProgramFilesX86}\Microsoft Contoso\Contoso\contosomail.EXE" -c OEP.Note /m "%1"</CommandLine>

  <DropTargetClassId />

  <FriendlyName />

  <Extended>0</Extended>

  <LegacyDisable>0</LegacyDisable>

  <SuppressionPolicy>2</SuppressionPolicy>

   <DdeExec>

  <NoActivateHandler />

  <Application>contosomail</Application>

  <Topic>ShellSystem</Topic>

  <IfExec>[SHELLNOOP]</IfExec>

  <DdeCommand>[SetForeground][ShellNewDatabase "%1"]</DdeCommand>

  </DdeExec>

  </ShellCommand>

  </ShellCommands>

  </ApplicationURLProtocol>

  </URLProtocol>

  </Extension>

  </Extension>

  </URLProtocols>
```

Il sottosistema estensione **client software** consente all'app di registrarsi come client di posta elettronica, lettore di notizie, lettore multimediale e rende visibile l'app nell'interfaccia utente imposta l'accesso e il computer. Nella maggior parte dei casi devi solo abilitarlo e disabilitarlo. Esiste anche un controllo che consente di abilitare e disabilitare il client di posta elettronica in modo specifico se si vuole che gli altri client siano ancora abilitati, ad eccezione del client.

```XML

<SoftwareClients Enabled="true">

  <ClientConfiguration EmailEnabled="false" />

</SoftwareClients>
```

Il sottosistema di estensione **AppPaths** apre le app registrate con un percorso applicazione. Ad esempio, se contoso.exe ha un nome AppPath di _MyApp_, gli utenti possono digitare _MyApp_ dal menu Esegui, aprendo contoso.exe.

```XML

<AppPaths Enabled="true">

<Extensions>

<Extension Category="AppV.AppPath">

<AppPath>

  <ApplicationId>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationId>

  <Name>contosomail.exe</Name>

  <ApplicationPath>[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE</ApplicationPath>

  <PATHEnvironmentVariablePrefix />

  <CanAcceptUrl>false</CanAcceptUrl>

  <SaveUrl />

</AppPath>

</Extension>

</Extensions>

</AppPaths>
```

Il sottosistema delle estensioni **com** consente un'applicazione registrata nei server COM locali. La modalità può essere:

-   Integrazione
-   Isolato 
-   Disattivato

```XML

<COM Mode="Isolated"/>
```

**Oggetti kernel virtuali**

```XML

<Objects Enabled="false" />
```

Il registro di sistema **virtuale** imposta un registro di sistema nel registro di sistema virtuale in HKCU.

```XML

<Registry Enabled="true">

<Include>

<Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\ABC">

<Value Type="REG_SZ" Name="Bar" Data="NewValue" />

 </Key>

  <Key Path="\REGISTRY\USER\[{AppVCurrentUserSID}]\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**File system virtuale**

```XML

    <FileSystem Enabled="true" />
```

**Tipi di carattere virtuali**

```XML

      <Fonts Enabled="false" />
```

**Variabili di ambiente virtuali**

```XML

<EnvironmentVariables Enabled="true">

<Include>

       <Variable Name="UserPath" Value="%path%;%UserProfile%" />

       <Variable Name="UserLib" Value="%UserProfile%\ABC" />

       </Include>

      <Delete>

       <Variable Name="lib" />

        </Delete>

        </EnvironmentVariables>
```

**Servizi virtuali**

```XML

      <Services Enabled="false" />
```

#### UserScripts

Usare UserScripts per configurare o modificare l'ambiente virtuale.  È anche possibile eseguire script al momento della distribuzione o per pulire l'ambiente dopo la chiusura dell'applicazione. Per visualizzare uno script di esempio, fare riferimento al file di configurazione dell'utente generato dal sequencer. La sezione Scripts seguente fornisce altre informazioni sui vari trigger che possono essere usati.

#### ManagingAuthority

USA ManagingAuthority quando due versioni del pacchetto coesistono nello stesso computer, uno distribuito in App-V 4,6 e un altro distribuito in App-V 5,0. Per consentire a App-V vNext di assumere i punti di estensione App-V 4,6 per il pacchetto denominato, immettere quanto segue nel file UserConfig (dove PackageName è il GUID del pacchetto in App-V 4,6:

```XML

<ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" />
```

## File di configurazione della distribuzione (DeploymentConfig.xml)

Il file DeploymentConfig fornisce le impostazioni di configurazione per il contesto di computer e il contesto utente, fornendo le stesse funzionalità elencate nel file UserConfig. L'impostazione viene applicata quando si distribuisce il pacchetto in un computer che esegue il client App-V 5,1.

Usare il file DeploymentConfig per specificare o modificare le impostazioni personalizzate per un pacchetto:

- Tutte le impostazioni di UserConfig
- Estensioni che possono essere applicate solo a livello globale per tutti gli utenti
- Sottosistemi virtuali per le posizioni globali del computer, ad esempio il registro di sistema
- URL origine prodotto
- Script (solo contesto computer)
- Controlli per terminare i processi figlio

### Intestazione

L'intestazione di un file di configurazione della distribuzione dinamica ha un aspetto simile al seguente:

```XML
<?xml version="1.0" encoding="utf-8"?><DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">
```

**PackageID** è lo stesso valore esistente nel file manifesto.

### Corpo

Il corpo del file di configurazione della distribuzione dinamica include due sezioni:

- **UserConfiguration:** consente lo stesso contenuto del file di configurazione dell'utente descritto nella sezione precedente.  Quando si pubblica il pacchetto in un utente, tutte le impostazioni di configurazione di appextensions in questa sezione eseguono l'override delle impostazioni corrispondenti nel manifesto all'interno del pacchetto, a meno che non venga fornito un file di configurazione utente. Se viene fornito anche un file UserConfig, viene usato al posto delle impostazioni utente nel file di configurazione della distribuzione. Se si pubblica il pacchetto globalmente, solo il contenuto del file di configurazione della distribuzione viene usato in combinazione con il manifesto. Per altre informazioni, Vedi [contenuto del file di configurazione utente (UserConfig.xml)](#user-configuration-file-contents-userconfigxml).

- **MachineConfiguration:** contiene informazioni che possono essere configurate solo per un intero computer, non per un utente specifico nel computer. Ad esempio, HKEY_LOCAL_MACHINE le chiavi del registro di sistema nel VFS.

```XML

<DeploymentConfiguration PackageId="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="http://schemas.microsoft.com/appv/2010/deploymentconfiguration">

<UserConfiguration>

...

</UserConfiguration>

<MachineConfiguration>

...

</MachineConfiguration>

...

</MachineConfiguration>

</DeploymentConfiguration>
```

### UserConfiguration

Fare riferimento al [contenuto del file di configurazione utente (UserConfig.xml)](#user-configuration-file-contents-userconfigxml) per informazioni sulle impostazioni disponibili per questa sezione. 

### MachineConfiguration

Usare la sezione MachineConfiguration per configurare le informazioni per un'intera macchina; non per un utente specifico nel computer. Ad esempio, HKEY_LOCAL_MACHINE le chiavi del registro di sistema nel registro di sistema virtuale. In questo elemento sono consentite quattro sottosezioni:

1.  **[Sottosistemi](#subsystems-1)**
2.  **[ProductSourceURLOptOut](#productsourceurloptout)**
3.  **[MachineScripts](#machinescripts)**
4.  **[TerminateChildProcess](#terminatechildprocess)**

#### Sottosistemi

AppExtensions e altri sottosistemi disposti come sottonodi.

```XML

<MachineConfiguration>

  <Subsystems>

  …

  </Subsystems>

…

</MachineConfiguration>
```

Puoi abilitare o disabilitare ogni sottosistema usando l'attributo **Enabled** .

**Extensions** 

Alcuni sottosistemi (sottosistemi di estensione) controllano le estensioni. Il sottosistema è funzionalità delle applicazioni usate dai programmi predefiniti. Per questo tipo di estensione, il pacchetto deve essere pubblicato globalmente per l'integrazione nel sistema locale. Le stesse regole per i controlli e le impostazioni applicabili alle estensioni della configurazione utente si applicano anche a quelle nella sezione MachineConfiguration.

**Funzionalità delle applicazioni**: usate dai programmi predefiniti che consentono a un'applicazione di registrarsi come segue:

- In grado di aprire specifiche estensioni di file
- Un concorrente per lo slot del browser Internet del menu Start
- In grado di aprire specifici tipi MIME di Windows

Questa estensione rende inoltre visibile l'applicazione virtuale nell'interfaccia utente imposta programmi predefiniti.

```XML

<ApplicationCapabilities Enabled="true">

  <Extensions>

   <Extension Category="AppV.ApplicationCapabilities">

    <ApplicationCapabilities>


   <ApplicationId>[{PackageRoot}]\LitView\LitViewBrowser.exe</ApplicationId>

     <Reference>

      <Name>LitView Browser</Name>

      <Path>SOFTWARE\LitView\Browser\Capabilities</Path>

     </Reference>

   <CapabilityGroup>

    <Capabilities>


   <Name>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12345</Name>


   <Description>@[{ProgramFilesX86}]\LitView\LitViewBrowser.exe,-12346</Description>

     <Hidden>0</Hidden>

     <EMailSoftwareClient>Lit View E-Mail Client</EMailSoftwareClient>

     <FileAssociationList>

      <FileAssociation Extension=".htm" ProgID="LitViewHTML" />

      <FileAssociation Extension=".html" ProgID="LitViewHTML" />

      <FileAssociation Extension=".shtml" ProgID="LitViewHTML" />

     </FileAssociationList>

     <MIMEAssociationList>

      <MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" />

      <MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" />

     </MIMEAssociationList>

    <URLAssociationList>

      <URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" />

     </URLAssociationList>

     </Capabilities>

  </CapabilityGroup>

   </ApplicationCapabilities>

  </Extension>

</Extensions>

</ApplicationCapabilities>
```

_**Sottosistemi di estensione supportati:**_ 

Il sottosistema di estensione **del registro virtuale di computer wide** imposta una chiave di registro nel registro virtuale all'interno di HKEY_LOCAL_MACHINE.

```XML

<Registry>

<Include>

  <Key Path="\REGISTRY\\Machine\Software\ABC">

    <Value Type="REG_SZ" Name="Bar" Data="Baz" />

   </Key>

  <Key Path="\REGISTRY\Machine\Software\EmptyKey" />

 </Include>

<Delete>

</Registry>
```

**Oggetti kernel virtuali a livello di computer**

```XML

<Objects>

<NotIsolate>

   <Object Name="testObject" />

 </NotIsolate>

</Objects>
```

#### ProductSourceURLOptOut

USA ProductSourceURLOptOut per indicare che l'URL del pacchetto può essere modificato globalmente tramite _PackageSourceRoot_ (per supportare gli scenari di filiale). Le modifiche hanno effetto sul prossimo avvio. 

```XML

<MachineConfiguration>

  ... 

  <ProductSourceURLOptOut Enabled="true" />

  ...

</MachineConfiguration>
```

#### MachineScripts

Il pacchetto può essere configurato per eseguire script in fase di distribuzione, pubblicazione o rimozione. Per visualizzare uno script di esempio, vedere il file di configurazione della distribuzione generato dal sequencer. 

La sezione Scripts seguente fornisce altre informazioni sui vari trigger che possono essere usati.

#### TerminateChildProcess

È possibile specificare un file eseguibile dell'applicazione, i cui processi figlio vengono terminati al termine del processo exe dell'applicazione.

```XML

<MachineConfiguration>

  ...   

  <TerminateChildProcesses>

    <Application Path="[{PackageRoot}]\Contoso\ContosoApp.EXE" />

    <Application Path="[{PackageRoot}]\LitView\LitViewBrowser.exe" />

    <Application Path="[{ProgramFilesX86}]\Microsoft Contoso\Contoso\contosomail.EXE" />

  </TerminateChildProcesses>

  ...

</MachineConfiguration>
```



## Script

La tabella seguente descrive i vari eventi di script e il contesto in cui possono essere eseguiti.

| Tempo di esecuzione degli script       | Può essere specificato nella configurazione di distribuzione | Può essere specificato nella configurazione utente | Può essere eseguito nell'ambiente virtuale del pacchetto | Può essere eseguito nel contesto di un'applicazione specifica | Viene eseguito in contesto sistema/utente: (configurazione della distribuzione, configurazione utente) |
|-----------------------------|----------------------------------------------|----------------------------------------|---------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------|
| AddPackage                  | X                                            |                                        |                                                   |                                                     | (SISTEMA, N/D)                                                               |
| PublishPackage              | X                                            | X                                      |                                                   |                                                     | (Sistema; utente)                                                              |
| UnpublishPackage            | X                                            | X                                      |                                                   |                                                     | (Sistema; utente)                                                              |
| RemovePackage               | X                                            |                                        |                                                   |                                                     | (SISTEMA, N/D)                                                               |
| StartProcess quale nome                | X                                            | X                                      | X                                                 | X                                                   | (Utente, utente)                                                                |
| ExitProcess                 | X                                            | X                                      |                                                   | X                                                   | (Utente, utente)                                                                |
| StartVirtualEnvironment     | X                                            | X                                      | X                                                 |                                                     | (Utente, utente)                                                                |
| TerminateVirtualEnvironment | X                                            | X                                      |                                                   |                                                     | (Utente, utente)                                                                |

### Uso di più script in un singolo trigger di evento

App-V 5,1 supporta l'uso di più script in un singolo trigger di evento per i pacchetti App-V, inclusi i pacchetti convertiti da App-V 4,6 in App-V 5,0 o versioni successive. Per abilitare l'uso di più script, App-V 5,1 usa un'applicazione di avvio di script, denominata ScriptRunner.exe, che viene installata come parte dell'installazione del client App-V.

### Come usare più script in un singolo trigger di evento

Per ogni script che si vuole eseguire, passare lo script come argomento all'applicazione ScriptRunner.exe. L'applicazione esegue quindi ogni script separatamente, insieme agli argomenti specificati per ogni script. Usare un solo script (ScriptRunner.exe) per trigger.

> [!NOTE]
> 
> È consigliabile eseguire prima di tutto la riga di script da un prompt dei comandi per verificare che tutti gli argomenti vengano generati correttamente prima di aggiungerli al file di configurazione della distribuzione.

### Esempio di script e descrizioni di parametri

Usando il file e la tabella di esempio seguenti, modificare il file di configurazione della distribuzione o dell'utente per aggiungere gli script che si desidera eseguire.

```XML
<MachineScripts>
 <AddPackage>
   <Path>ScriptRunner.exe</Path>
   <Arguments>
   -appvscript script1.exe arg1 arg2 –appvscriptrunnerparameters –wait –timeout=10
   -appvscript script2.vbs arg1 arg2
   -appvscript script3.bat arg1 arg2 –appvscriptrunnerparameters –wait –timeout=30 –rollbackonerror
   </Arguments>
   <Wait timeout=”40” RollbackOnError=”true”/>
 </AddPackage>
</MachineScripts>
```


**I parametri nel file di esempio includono:**

#### \<AddPackage\>

Nome del trigger dell'evento per cui si esegue uno script, ad esempio l'aggiunta di un pacchetto o la pubblicazione di un pacchetto.

#### \<Path\>ScriptRunner.exe\</Path\>

L'applicazione di avvio script installata come parte dell'installazione del client App-V.

> [!NOTE]
> 
> Anche se ScriptRunner.exe viene installato come parte del client App-V, la posizione del client App-V deve essere in% path% o ScriptRunner non verrà eseguito. ScriptRunner.exe si trova in genere in C:FilesApplication Virtualizationfolder.

#### \<Arguments\>

`-appvscript` -Token che rappresenta lo script effettivo che si vuole eseguire.

`script1.exe` : Nome dello script che si vuole eseguire.

`arg1 arg2` -Argomenti per lo script che si vuole eseguire.

`-appvscriptrunnerparameters` -Token che rappresenta le opzioni di esecuzione per script1.exe.

`-wait` -Token che informa ScriptRunner di attendere il completamento dell'esecuzione di script1.exe prima di procedere con lo script successivo.

`-timeout=x` -Token che informa ScriptRunner di interrompere l'esecuzione dello script corrente dopo il numero di secondi x. Vengono ancora eseguiti tutti gli altri script specificati.

`-rollbackonerror` -Token che informa ScriptRunner di interrompere l'esecuzione di tutti gli script che non sono ancora stati eseguiti e di ripristinare un errore nel client App-V.

#### \<Wait timeout=”40” RollbackOnError=”true”/\>

Attende il completamento complessivo della ScriptRunner.exe.

Imposta il valore di timeout per il partecipante globale in modo che sia maggiore o uguale alla somma dei valori di timeout per i singoli script.

Se un singolo script ha segnalato un errore e rollbackonerror è stato impostato su true, ScriptRunner segnala l'errore al client App-V.

ScriptRunner esegue qualsiasi script il cui tipo di file sia associato a un'applicazione installata nel computer. Se l'applicazione associata è mancante o il tipo di file dello script non è associato a nessuna applicazione nel computer, lo script non viene eseguito.

### Creare un file di configurazione dinamica usando un file manifesto di App-V 5,1

Puoi creare il file di configurazione dinamica usando uno dei tre metodi seguenti: manualmente, usando la console di gestione di App-V 5,1 o sequenziando un pacchetto, che genera due file di esempio. Per altre informazioni su come creare il file usando la console di gestione di App-V 5,1, vedere [come creare un file di configurazione personalizzato usando la console di gestione di App-v 5,1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md).

Per creare il file manualmente, è possibile combinare le informazioni di cui sopra nelle sezioni precedenti in un singolo file. Ti consigliamo di usare i file generati dal sequencer.



- Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).
- Per i problemi di App-V, usa il [Forum di App-v TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati

- [Come applicare il file di configurazione della distribuzione con PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

- [Come applicare il file di configurazione utente con PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

- [Operazioni per App-V 5.1](operations-for-app-v-51.md)

---
