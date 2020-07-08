---
title: Informazioni sulle impostazioni di configurazione client
description: Informazioni sulle impostazioni di configurazione client
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806105"
---
# Informazioni sulle impostazioni di configurazione client


Il client di Microsoft Application Virtualization (App-V) 5,0 archivia la configurazione nel registro di sistema. Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client. È anche possibile configurare molte azioni client modificando le voci del registro di sistema. Questo argomento elenca le impostazioni di configurazione del client App-V 5,0 e spiega i loro usi. È possibile usare PowerShell per modificare le impostazioni di configurazione del client. Per altre informazioni sull'uso di PowerShell e App-V 5,0, vedere [amministrazione di App-v tramite PowerShell](administering-app-v-by-using-powershell.md).

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> Impostazioni di configurazione client App-V 5,0


La tabella seguente mostra le informazioni sulle impostazioni di configurazione del client App-V 5,0:

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
<th align="left">Impostazione del nome</th>
<th align="left">Contrassegno imposta</th>
<th align="left">Descrizione</th>
<th align="left">Opzioni di impostazione</th>
<th align="left">Valore della chiave del registro di sistema</th>
<th align="left">Chiavi e valori di stato dei criteri disabilitati</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageInstallationRoot</p></td>
<td align="left"><p>PACKAGEINSTALLATIONROOT</p></td>
<td align="left"><p>Specifica la directory in cui verranno installate tutte le nuove applicazioni e gli aggiornamenti.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\PackageInstallationRoot</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>PackageSourceRoot</p></td>
<td align="left"><p>PACKAGESOURCEROOT</p></td>
<td align="left"><p>Sostituisce la posizione di origine per scaricare il contenuto del pacchetto.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\PackageSourceRoot</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>AllowHighCostLaunch</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Questa impostazione controlla se le applicazioni virtualizzate vengono avviate in computer con Windows 8 collegati tramite una connessione di rete a consumo (ad esempio 4G).</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Streaming\AllowHighCostLaunch</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReestablishmentRetries</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica il numero di tentativi di una sessione eliminata.</p></td>
<td align="left"><p>Numero intero (0-99)</p></td>
<td align="left"><p>Streaming\ReestablishmentRetries</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReestablishmentInterval</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica il numero di secondi tra i tentativi di ristabilire una sessione eliminata.</p></td>
<td align="left"><p>Numero intero (0-3600)</p></td>
<td align="left"><p>Streaming\ReestablishmentInterval</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>AutoLoad</p></td>
<td align="left"><p>AUTOLOAD</p></td>
<td align="left"><p>Specifica il modo in cui i nuovi pacchetti devono essere caricati automaticamente da App-V in un computer specifico.</p></td>
<td align="left"><p>(0x0) None; (0x1) usato in precedenza; (0x2) tutti</p></td>
<td align="left"><p>Streaming\AutoLoad</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocationProvider</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica il CLSID per un'implementazione compatibile dell'interfaccia IAppvPackageLocationProvider.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\LocationProvider</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>CertFilterForClientSsl</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica il percorso di un certificato valido nell'archivio certificati.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Streaming\CertFilterForClientSsl</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VerifyCertificateRevocationList</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Verifica lo stato di revoca del certificato del server prima della vaporizzazione tramite HTTPS.</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Streaming\VerifyCertificateRevocationList</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>SharedContentStoreMode</p></td>
<td align="left"><p>SHAREDCONTENTSTOREMODE</p></td>
<td align="left"><p>Specifica che il contenuto del pacchetto in streaming non verrà salvato nel disco rigido locale.</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Streaming\SharedContentStoreMode</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nome</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERNAME</p></td>
<td align="left"><p>Visualizza il nome del server di pubblicazione.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ FriendlyName</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>PUBLISHINGSERVERURL</p></td>
<td align="left"><p>Visualizza l'URL del server di pubblicazione.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ URL</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshEnabled</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHENABLED</p></td>
<td align="left"><p>Abilita l'aggiornamento della pubblicazione globale (booleano)</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshOnLogon</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHONLOGON</p></td>
<td align="left"><p>Attiva un aggiornamento della pubblicazione globale all'accesso. Boolean</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>GlobalRefreshInterval</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVAL  </p></td>
<td align="left"><p>Specifica l'intervallo di aggiornamento della pubblicazione con GlobalRefreshIntervalUnit. Per disabilitare l'aggiornamento del pacchetto, selezionare 0.</p></td>
<td align="left"><p>Numero intero (0-744</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>GlobalRefreshIntervalUnit</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>GLOBALREFRESHINTERVALUNI</p></td>
<td align="left"><p>Specifica l'unità di intervallo (ora 0-23, giorno 0-31). </p></td>
<td align="left"><p>0 per ora, 1 per giorno</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ GlobalPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshEnabled</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHENABLED </p></td>
<td align="left"><p>Abilita l'aggiornamento della pubblicazione degli utenti (Boolean)</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserEnabled</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshOnLogon</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHONLOGON</p></td>
<td align="left"><p>Attiva un aggiornamento della pubblicazione degli utenti ONLOGON. Boolean</p>
<p>Conteggio parole (con spazi): 60</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserLogonRefresh</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="odd">
<td align="left"><p>UserRefreshInterval</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVAL     </p></td>
<td align="left"><p>Specifica l'intervallo di aggiornamento della pubblicazione con UserRefreshIntervalUnit. Per disabilitare l'aggiornamento del pacchetto, selezionare 0.</p>
<p>Conteggio parole (con spazi): 85</p></td>
<td align="left"><p>Numero intero (0-744 ore)</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserPeriodicRefreshInterval</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="even">
<td align="left"><p>UserRefreshIntervalUnit</p>
<div class="alert">
<strong>Nota</strong><br/><p>Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> . Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</p>
</div>
<div>

</div></td>
<td align="left"><p>USERREFRESHINTERVALUNIT  </p></td>
<td align="left"><p>Specifica l'unità di intervallo (ora 0-23, giorno 0-31). </p></td>
<td align="left"><p>0 per ora, 1 per giorno</p></td>
<td align="left"><p>Publishing\Servers {serverId} \ UserPeriodicRefreshIntervalUnit</p></td>
<td align="left"><p>1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MigrationMode</p></td>
<td align="left"><p>MIGRATIONMODE</p></td>
<td align="left"><p>La modalità di migrazione consente al client App-V di modificare i tasti di scelta rapida e FTA per i pacchetti creati con una versione precedente di App-V.</p></td>
<td align="left"><p>True (stato abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Coexistence\MigrationMode</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>CEIPOPTIN</p></td>
<td align="left"><p>Consente al computer che usa il client App-V 5,0 di raccogliere e restituire determinate informazioni sull'utilizzo per consentire di migliorare ulteriormente l'applicazione.</p></td>
<td align="left"><p>0 per disabilitato; 1 per abilitato</p></td>
<td align="left"><p>SOFTWARE/Microsoft/AppV/analisi utilizzo software/CEIPEnable</p></td>
<td align="left"><p>0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePackageScripts</p></td>
<td align="left"><p>ENABLEPACKAGESCRIPTS</p></td>
<td align="left"><p>Abilita gli script definiti nel manifesto del pacchetto di file di configurazione che deve essere eseguito.</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>\Scripting\EnablePackageScripts</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>RoamingFileExclusions</p></td>
<td align="left"><p>ROAMINGFILEEXCLUSIONS</p></td>
<td align="left"><p>Specifica i percorsi di file relativi a% USERPROFILE% che non sono in roaming con un profilo utente&#39;s. Esempio di utilizzo:/ROAMINGFILEEXCLUSIONS =&#39;desktop; immagini personali&#39;</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>RoamingRegistryExclusions</p></td>
<td align="left"><p>ROAMINGREGISTRYEXCLUSIONS</p></td>
<td align="left"><p>Specifica i percorsi del registro di sistema che non sono in roaming con un profilo utente. Esempio di utilizzo:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\RoamingRegistryExclusions</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>IntegrationRootUser</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica la posizione in cui creare collegamenti simbolici associati alla versione corrente di un pacchetto pubblicato per utente. tutte le estensioni delle applicazioni virtuali, ad esempio le scelte rapide da tastiera e le associazioni di tipi di file, puntano al percorso. Se non specifichi un percorso, i collegamenti simbolici non verranno usati quando pubblichi il pacchetto. Ad esempio:%localappdata%\Microsoft\AppV\Client\Integration.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\IntegrationRootUser</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IntegrationRootGlobal</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica la posizione in cui creare collegamenti simbolici associati alla versione corrente di un pacchetto pubblicato globalmente. tutte le estensioni delle applicazioni virtuali, ad esempio le scelte rapide da tastiera e le associazioni di tipi di file, puntano al percorso. Se non specifichi un percorso, i collegamenti simbolici non verranno usati quando pubblichi il pacchetto. Ad esempio:%allusersprofile%\Microsoft\AppV\Client\Integration</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\IntegrationRootGlobal</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>VirtualizableExtensions</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Un elenco delimitato da virgole delle estensioni di file che possono essere usate per determinare se un'applicazione installata localmente può essere eseguita nell'ambiente virtuale.</p>
<p>Quando si creano tasti di scelta rapida, accordi e altri punti di estensione durante la pubblicazione, App-V confronterà l'estensione del nome file all'elenco se l'applicazione associata al punto di estensione è installata localmente. Se si trova l'estensione, <strong> </strong> verrà aggiunto il parametro della riga di comando RunVirtual e l'applicazione verrà eseguita virtualmente.</p>
<p>Per altre informazioni sul <strong> parametro RunVirtual </strong> , vedere <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> eseguire un'applicazione installata localmente in un ambiente virtuale con applicazioni virtualizzate </a> .</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Integration\VirtualizableExtensions</p></td>
<td align="left"><p>Valore criterio non scritto</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingEnabled</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Consente al client di restituire informazioni a un server di report.</p></td>
<td align="left"><p>True (abilitato); False (stato disabilitato)</p></td>
<td align="left"><p>Reporting\EnableReporting</p></td>
<td align="left"><p>False</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingServerURL</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica la posizione nel server di report in cui vengono salvate le informazioni sul client.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Reporting\ReportingServer</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingDataCacheLimit</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report. Le dimensioni si applicano alla cache in memoria. Quando viene raggiunto il limite, il file di log verrà ribaltato. Imposta tra 0 e 1024.</p></td>
<td align="left"><p>Numero intero [0-1024]</p></td>
<td align="left"><p>Reporting\DataCacheLimit</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingDataBlockSize</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica la dimensione massima in byte da trasmettere al server per la segnalazione delle richieste di caricamento. Ciò consente di evitare errori di trasmissione permanenti quando il log ha raggiunto una dimensione significativa. Impostato tra 1024 e illimitato.</p></td>
<td align="left"><p>Numero intero [1024-illimitato]</p></td>
<td align="left"><p>Reporting\DataBlockSize</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingStartTime</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica il momento in cui avviare il client per inviare dati al server di report. È necessario specificare un numero intero valido compreso tra 0-23 corrispondente all'ora del giorno. Per impostazione predefinita, il ReportingStartTime inizierà <strong> </strong> il giorno corrente alle 10 P. M. o 22.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Devi configurare questa impostazione in un momento in cui i computer che eseguono il client App-V 5,0 sono meno probabili di essere offline.</p>
</div>
<div>

</div></td>
<td align="left"><p>Numero intero (0-23)</p></td>
<td align="left"><p>Report \ StartTime</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>ReportingInterval</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica l'intervallo di tentativi che il client userà per rinviare i dati al server di report.</p></td>
<td align="left"><p>Integer</p></td>
<td align="left"><p>Reporting\RetryInterval</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ReportingRandomDelay</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report. Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra 0 e <strong> ReportingRandomDelay </strong> e attenderà la durata specificata prima di inviare i dati. Questo può aiutare a prevenire collisioni nel server.</p></td>
<td align="left"><p>Numero intero [0-ReportingRandomDelay]</p></td>
<td align="left"><p>Reporting\RandomDelay</p></td>
<td align="left"><p>Valore criterio non scritto (uguale a non configurato)</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableDynamicVirtualization</p>
<div class="alert">
<strong>Importante</strong><br/><p>Questa impostazione è disponibile solo con App-V 5,0 SP2 o versione successiva.</p>
</div>
<div>

</div></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Abilita le estensioni della shell supportate, gli oggetti helper del browser e i controlli attivi X per essere virtualizzati ed eseguiti con le applicazioni virtuali.</p></td>
<td align="left"><p>1 (abilitato), 0 (disabilitato)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>EnablePublishingRefreshUI</p>
<div class="alert">
<strong>Importante</strong><br/><p>Questa impostazione è disponibile solo con App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Abilita la barra di stato dell'aggiornamento della pubblicazione per il computer in cui è in esecuzione il client App-V 5,0.</p></td>
<td align="left"><p>1 (abilitato), 0 (disabilitato)</p></td>
<td align="left"><p>HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>HideUI</p>
<div class="alert">
<strong>Importante</strong><br/><p>Questa impostazione è disponibile solo con App-V 5,0 SP2.</p>
</div>
<div>

</div></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Nasconde la barra di stato dell'aggiornamento della pubblicazione.</p></td>
<td align="left"><p>1 (abilitato), 0 (disabilitato)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Non disponibile.</p></td>
<td align="left"><p>Specifica un elenco di percorsi di processo (che possono contenere caratteri jolly), che sono candidati per l'uso della virtualizzazione dinamica (estensioni della shell supportate, oggetti helper del browser e controlli ActiveX). Solo i processi il cui percorso completo corrisponde a uno di questi elementi possono usare la virtualizzazione dinamica.</p></td>
<td align="left"><p>String</p></td>
<td align="left"><p>Virtualization\ProcessesUsingVirtualComponents</p></td>
<td align="left"><p>Stringa vuota.</p></td>
</tr>
</tbody>
</table>








## Argomenti correlati


[Distribuzione di App-V 5.0 Sequencer e del client](deploying-the-app-v-50-sequencer-and-client.md)

[Come modificare la configurazione del client App-V 5.0 usando il modello ADMX e Criteri di gruppo](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[Come distribuire il client App-V](how-to-deploy-the-app-v-client-gb18030.md)









