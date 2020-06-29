---
title: Informazioni sulle impostazioni di configurazione client
description: Informazioni sulle impostazioni di configurazione client
author: dansimp
ms.assetid: 18bb307a-7eda-4dd6-a83e-6afaefd99470
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fb547eedf63bf165b1e8f5fd024839b3c2af3e4c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806106"
---
# Informazioni sulle impostazioni di configurazione client


Il client di Microsoft Application Virtualization (App-V) 5,1 archivia la configurazione nel registro di sistema. Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client. È anche possibile configurare molte azioni client modificando le voci del registro di sistema. Questo argomento elenca le impostazioni di configurazione del client App-V 5,1 e spiega i loro usi. È possibile usare PowerShell per modificare le impostazioni di configurazione del client. Per altre informazioni sull'uso di PowerShell e App-V 5,1, vedere [amministrazione di App-v 5,1 tramite PowerShell](administering-app-v-51-by-using-powershell.md).

## <a href="" id="---------app-v-5-1-client-configuration-settings"></a> Impostazioni di configurazione client App-V 5,1


La tabella seguente mostra le informazioni sulle impostazioni di configurazione del client App-V 5,1:

|Nome dell'impostazione | Contrassegno imposta | Descrizione | Opzioni di impostazione | Valore della chiave del registro di sistema | Chiavi e valori di stato dei criteri disabilitati |
|-------------|------------|-------------|-----------------|--------------------|--------------------------------------|
| PackageInstallationRoot | PACKAGEINSTALLATIONROOT | Specifica la directory in cui verranno installate tutte le nuove applicazioni e gli aggiornamenti. | String | Streaming\PackageInstallationRoot | Valore criterio non scritto (uguale a non configurato) |
| PackageSourceRoot | PACKAGESOURCEROOT | Sostituisce la posizione di origine per scaricare il contenuto del pacchetto. | String | Streaming\PackageSourceRoot | Valore criterio non scritto (uguale a non configurato) |
| AllowHighCostLaunch | Non disponibile. |Questa impostazione controlla se le applicazioni virtualizzate vengono avviate in computer con Windows 10 collegati tramite una connessione di rete a consumo (ad esempio 4G). | True (abilitato); False (stato disabilitato) | Streaming\AllowHighCostLaunch | 0 |
| ReestablishmentRetries | Non disponibile. | Specifica il numero di tentativi di una sessione eliminata. | Numero intero (0-99) | Streaming\ReestablishmentRetries | Valore criterio non scritto (uguale a non configurato) |
| ReestablishmentInterval | Non disponibile. | Specifica il numero di secondi tra i tentativi di ristabilire una sessione eliminata. | Numero intero (0-3600) | Streaming\ReestablishmentInterval | Valore criterio non scritto (uguale a non configurato) |
| LocationProvider | Non disponibile. | Specifica il CLSID per un'implementazione compatibile dell'interfaccia IAppvPackageLocationProvider. | String | Streaming\LocationProvider | Valore criterio non scritto (uguale a non configurato) |
| CertFilterForClientSsl | Non disponibile. | Specifica il percorso di un certificato valido nell'archivio certificati. | String | Streaming\CertFilterForClientSsl | Valore criterio non scritto (uguale a non configurato) |
| VerifyCertificateRevocationList | Non disponibile. | Verifica lo stato di revoca del certificato del server prima della vaporizzazione tramite HTTPS. | True (abilitato); False (stato disabilitato) | Streaming\VerifyCertificateRevocationList | 0 |
| SharedContentStoreMode | SHAREDCONTENTSTOREMODE | Specifica che il contenuto del pacchetto in streaming non verrà salvato nel disco rigido locale. | True (abilitato); False (stato disabilitato) | Streaming\SharedContentStoreMode | 0 |
| Nome<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | PUBLISHINGSERVERNAME | Visualizza il nome del server di pubblicazione. | String | Publishing\Servers\ {serverId} \ FriendlyName | Valore criterio non scritto (uguale a non configurato) |
| URL<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | PUBLISHINGSERVERURL | Visualizza l'URL del server di pubblicazione. | String | Publishing\Servers\ {serverId} \ URL | Valore criterio non scritto (uguale a non configurato) |
| GlobalRefreshEnabled<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHENABLED | Abilita l'aggiornamento della pubblicazione globale (booleano) | True (abilitato); False (stato disabilitato) | Publishing\Servers\ {serverId} \ GlobalEnabled | False |
| GlobalRefreshOnLogon<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHONLOGON | Attiva un aggiornamento della pubblicazione globale all'accesso. Boolean | True (abilitato); False (stato disabilitato) | Publishing\Servers\ {serverId} \ GlobalLogonRefresh | False |
| GlobalRefreshInterval<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHINTERVAL | Specifica l'intervallo di aggiornamento della pubblicazione con GlobalRefreshIntervalUnit. Per disabilitare l'aggiornamento del pacchetto, selezionare 0. | Numero intero (0-744) | Publishing\Servers\ {serverId} \ GlobalPeriodicRefreshInterval | 0 |
| GlobalRefreshIntervalUnit <br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | GLOBALREFRESHINTERVALUNI | Specifica l'unità di intervallo (ora 0-23, giorno 0-31). | 0 per ora, 1 per giorno | Publishing\Servers\ {serverId} \ GlobalPeriodicRefreshIntervalUnit | 1 |
| UserRefreshEnabled<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | USERREFRESHENABLED | Abilita l'aggiornamento della pubblicazione degli utenti (Boolean) | True (abilitato); False (stato disabilitato) | Publishing\Servers\ {serverId} \ UserEnabled | False |
| UserRefreshOnLogon<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | USERREFRESHONLOGON | Attiva un aggiornamento della pubblicazione degli utenti ONLOGON. Boolean<br>Conteggio parole (con spazi): 60 | True (abilitato); False (stato disabilitato) | Publishing\Servers\ {serverId} \ UserLogonRefresh | False |
| UserRefreshInterval<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | USERREFRESHINTERVAL | Specifica l'intervallo di aggiornamento della pubblicazione con UserRefreshIntervalUnit. Per disabilitare l'aggiornamento del pacchetto, selezionare 0. | Conteggio parole (con spazi): 85<br>Numero intero (0-744 ore) | Publishing\Servers\ {serverId} \ UserPeriodicRefreshInterval | 0 |
| UserRefreshIntervalUnit<br>**Nota** Questa impostazione non può essere modificata usando il cmdLet **set-AppvclientConfiguration** . Devi usare il cmdlet **set-AppvPublishingServer** . | USERREFRESHINTERVALUNIT | Specifica l'unità di intervallo (ora 0-23, giorno 0-31). | 0 per ora, 1 per giorno | Publishing\Servers\ {serverId} \ UserPeriodicRefreshIntervalUnit | 1 |
| MigrationMode | MIGRATIONMODE | La modalità di migrazione consente al client App-V di modificare i tasti di scelta rapida e FTA per i pacchetti creati con una versione precedente di App-V. | True (stato abilitato); False (stato disabilitato) | Coexistence\MigrationMode | |
| CEIPOPTIN | CEIPOPTIN | Consente al computer che usa il client App-V 5,1 di raccogliere e restituire determinate informazioni sull'utilizzo per consentire di migliorare ulteriormente l'applicazione. | 0 per disabilitato; 1 per abilitato | SOFTWARE/Microsoft/AppV/analisi utilizzo software/CEIPEnable | 0 | 
| EnablePackageScripts | ENABLEPACKAGESCRIPTS | Abilita gli script definiti nel manifesto del pacchetto di file di configurazione che deve essere eseguito. | True (abilitato); False (stato disabilitato) | \Scripting\EnablePackageScripts | | 
| RoamingFileExclusions | ROAMINGFILEEXCLUSIONS | Specifica i percorsi di file relativi a% USERPROFILE% che non sono in roaming con il profilo di un utente. Esempio di utilizzo:/ROAMINGFILEEXCLUSIONS =' desktop; immagini personali ' | | | |
| RoamingRegistryExclusions | ROAMINGREGISTRYEXCLUSIONS | Specifica i percorsi del registro di sistema che non sono in roaming con un profilo utente. Esempio di utilizzo:/ROAMINGREGISTRYEXCLUSIONS = software\\classes; software\\clients | String | Integration\RoamingRegistryExclusions | Valore criterio non scritto (uguale a non configurato) |
| IntegrationRootUser | Non disponibile. | Specifica la posizione in cui creare collegamenti simbolici associati alla versione corrente di un pacchetto pubblicato per utente. tutte le estensioni delle applicazioni virtuali, ad esempio le scelte rapide da tastiera e le associazioni di tipi di file, puntano al percorso. Se non specifichi un percorso, i collegamenti simbolici non verranno usati quando pubblichi il pacchetto. Ad esempio:%localappdata%\Microsoft\AppV\Client\Integration.| String | Integration\IntegrationRootUser | Valore criterio non scritto (uguale a non configurato) |
|IntegrationRootGlobal | Non disponibile.| Specifica la posizione in cui creare collegamenti simbolici associati alla versione corrente di un pacchetto pubblicato globalmente. tutte le estensioni delle applicazioni virtuali, ad esempio le scelte rapide da tastiera e le associazioni di tipi di file, puntano al percorso. Se non specifichi un percorso, i collegamenti simbolici non verranno usati quando pubblichi il pacchetto. Ad esempio:%allusersprofile%\Microsoft\AppV\Client\Integration | String | Integration\IntegrationRootGlobal | Valore criterio non scritto (uguale a non configurato) |
| VirtualizableExtensions | Non disponibile. | Un elenco delimitato da virgole delle estensioni di file che possono essere usate per determinare se un'applicazione installata localmente può essere eseguita nell'ambiente virtuale.<br>Quando si creano tasti di scelta rapida, accordi e altri punti di estensione durante la pubblicazione, App-V confronterà l'estensione del nome file all'elenco se l'applicazione associata al punto di estensione è installata localmente. Se si trova l'estensione, verrà aggiunto il parametro della riga di comando **RunVirtual** e l'applicazione verrà eseguita virtualmente.<br>Per altre informazioni sul parametro **RunVirtual** , vedere [eseguire un'applicazione installata localmente in un ambiente virtuale con applicazioni virtualizzate](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications51.md). | String | Integration\VirtualizableExtensions | Valore criterio non scritto |
| ReportingEnabled | Non disponibile. | Consente al client di restituire informazioni a un server di report. | True (abilitato); False (stato disabilitato) | Reporting\EnableReporting | False |
| ReportingServerURL | Non disponibile. | Specifica la posizione nel server di report in cui vengono salvate le informazioni sul client. | String | Reporting\ReportingServer | Valore criterio non scritto (uguale a non configurato) |
| ReportingDataCacheLimit | Non disponibile. | Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report. Le dimensioni si applicano alla cache in memoria. Quando viene raggiunto il limite, il file di log verrà ribaltato. Imposta tra 0 e 1024. | Numero intero [0-1024] | Reporting\DataCacheLimit | Valore criterio non scritto (uguale a non configurato) |
| ReportingDataBlockSize| Non disponibile. | Specifica la dimensione massima in byte da trasmettere al server per la segnalazione delle richieste di caricamento. Ciò consente di evitare errori di trasmissione permanenti quando il log ha raggiunto una dimensione significativa. Impostato tra 1024 e illimitato. | Numero intero [1024-illimitato] | Reporting\DataBlockSize | Valore criterio non scritto (uguale a non configurato) |
| ReportingStartTime | Non disponibile. | Specifica il momento in cui avviare il client per inviare dati al server di report. È necessario specificare un numero intero valido compreso tra 0-23 corrispondente all'ora del giorno. Per impostazione predefinita, il **ReportingStartTime** inizierà il giorno corrente alle 10 P. M. o 22.<br>**Nota** Devi configurare questa impostazione in un momento in cui i computer che eseguono il client App-V 5,1 sono meno probabili di essere offline. | Numero intero (0-23) | Report \ StartTime | Valore criterio non scritto (uguale a non configurato) |
| ReportingInterval | Non disponibile. | Specifica l'intervallo di tentativi che il client userà per rinviare i dati al server di report. | Integer | Reporting\RetryInterval | Valore criterio non scritto (uguale a non configurato) |
| ReportingRandomDelay | Non disponibile. | Specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report. Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra 0 e **ReportingRandomDelay** e attenderà la durata specificata prima di inviare i dati. Questo può aiutare a prevenire collisioni nel server. | Numero intero [0-ReportingRandomDelay] | Reporting\RandomDelay | Valore criterio non scritto (uguale a non configurato) |
| EnableDynamicVirtualization<br>**Importante** Questa impostazione è disponibile solo con App-V 5,0 SP2 o versione successiva. | Non disponibile. | Abilita le estensioni della shell supportate, gli oggetti helper del browser e i controlli attivi X per essere virtualizzati ed eseguiti con le applicazioni virtuali. | 1 (abilitato), 0 (disabilitato) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization | |
| EnablePublishingRefreshUI<br>**Importante** Questa impostazione è disponibile solo con App-V 5,0 SP2. | Non disponibile. | Abilita la barra di stato dell'aggiornamento della pubblicazione per il computer in cui è in esecuzione il client App-V 5,1. | 1 (abilitato), 0 (disabilitato) | HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing | |
| HideUI<br>**Importante**  Questa impostazione è disponibile solo con App-V 5,0 SP2.| Non disponibile. | Nasconde la barra di stato dell'aggiornamento della pubblicazione. | 1 (abilitato), 0 (disabilitato) | | |
| ProcessesUsingVirtualComponents | Non disponibile. | Specifica un elenco di percorsi di processo (che possono contenere caratteri jolly), che sono candidati per l'uso della virtualizzazione dinamica (estensioni della shell supportate, oggetti helper del browser e controlli ActiveX). Solo i processi il cui percorso completo corrisponde a uno di questi elementi possono usare la virtualizzazione dinamica. | String | Virtualization\ProcessesUsingVirtualComponents | Stringa vuota. |






## Argomenti correlati


[Distribuzione di App-V 5.1 Sequencer e del client](deploying-the-app-v-51-sequencer-and-client.md)

[Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

[Come distribuire il client App-V](how-to-deploy-the-app-v-client-51gb18030.md)

 

 





