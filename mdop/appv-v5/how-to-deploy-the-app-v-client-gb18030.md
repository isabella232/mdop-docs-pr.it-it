---
title: Come distribuire il client App-V
description: Come distribuire il client App-V
ms.author: dansimp
author: dansimp
ms.assetid: 9c4e67ae-ddaf-4e23-8c16-72d029a74a27
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/05/2018
ms.openlocfilehash: 4e246e13bf59f167eade77200afd866c6a3c41fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805488"
---
# Come distribuire il client App-V


Usare la procedura seguente per installare il client di Microsoft Application Virtualization (App-V) 5,0 e il client di Servizi Desktop remoto. È necessario installare la versione del client che corrisponde al sistema operativo del computer di destinazione.

<a href="" id="bkmk-clt-install-prereqs"></a>**Operazioni da eseguire prima di iniziare**

1. Rivedere e installare i prerequisiti software:

   Installare il software prerequisito che corrisponde alla versione di App-V che si sta installando:

   - [Informazioni su App-V 5.0 SP3](about-app-v-50-sp3.md)

   - App-V 5,0 SP1 e App-V 5,0 SP2: nessun nuovo requisito in queste versioni

   - [Prerequisiti di App-V 5.0](app-v-50-prerequisites.md)

2. Esaminare gli scenari di coesistenza client e non supportati, in applicazione dell'installazione:


   |                                               |                                                                                                                            |
   |-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
   |      Distribuzione di client App-V coesistenti       | [Pianificazione della distribuzione di App-V 5.0 Sequencer e del client](planning-for-the-app-v-50-sequencer-and-client-deployment.md) |
   | Scenari di installazione non supportati o limitati |                         [Configurazioni supportate di App-V 5.0](app-v-50-supported-configurations.md)                         |

   ---

3. Esaminare le posizioni per informazioni sul Registro di sistema, il log e la risoluzione dei problemi del client:

#### Informazioni sul Registro di sistema client
<ul><li>Per impostazione predefinita, dopo l'installazione del client App-V 5,0, le informazioni sul client sono archiviate nel registro di sistema nella chiave del registro di sistema seguente:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\APPV\CLIENT</code></li><li>Quando si distribuisce un pacchetto virtualizzato in un computer che sta eseguendo il client App-V, i dati del pacchetto associati vengono archiviati nella posizione seguente:<p><p><code>C:\ProgramData\App-V</code><p><p>È tuttavia possibile riconfigurare la posizione con la chiave del registro di sistema seguente:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\SOFTWARE\MICROSOFT\APPV\CLIENT\STREAMING\PACKAGEINSTALLATIONROOT</code></li></ul>

#### File di log client                  
<ul><li>Per informazioni sul file di log associato al client App-V 5,0, eseguire una ricerca nel log seguente:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV</code></li><li>In App-V 5,0 SP3 alcuni registri sono stati consolidati e spostati nella posizione seguente:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</code><p><p>Per un elenco dei registri spostati, vedere [informazioni su App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</li><li>I pacchetti attualmente archiviati nei computer che eseguono il client App-V 5,0 vengono salvati nella posizione seguente:<p><p><code>C:\ProgramData\App-V\<<em>package id</em>>\<<em>version id</em>></code></li></ul>

#### Informazioni sulla risoluzione dei problemi di installazione client
- Vedere il log degli errori nella cartella **% Temp%** . 
- Per rivedere i file di log, fare clic sul pulsante **Start**, digitare **% Temp%** e quindi cercare il **log appv_**. 

## Per installare il client App-V 5,0

1. Copiare il file di installazione del client App-V 5,0 nel computer in cui verrà installato.<p><p>Scegliere tra i tipi di client seguenti:


   |                  Tipo di client                  |          File da usare          |
   |-----------------------------------------------|-------------------------------|
   |        Versione standard del client         |   **appv_client_setup.exe**   |
   | Versione Servizi Desktop remoto del client | **appv_client_setup_rds.exe** |

   ---

2. Fare doppio clic sul file di installazione e fare clic su **Installa**. Prima che l'installazione venga avviata, il programma di installazione controlla il computer per tutti i [prerequisiti di App-V 5,0](app-v-50-prerequisites.md)mancanti.

3. Rivedere e accettare le condizioni di licenza software, scegliere se usare Microsoft Update e se partecipare al programma Microsoft Customer Experience Improvement e fare clic su **Installa**.

4. Nella pagina **installazione completata** fare clic su **Chiudi**.

   L'installazione crea le voci seguenti per il client App-V nei **programmi**:

   -   **.exe**

   -   **.msi**

   -   **Language Pack**

   >[!NOTE]
   >Dopo l'installazione, è possibile disinstallare solo il file exe.


## Per installare il client App-V 5,0 con uno script

1. Installare tutti i prerequisiti software necessari nei computer di destinazione. Vedere [cosa fare prima di iniziare](#bkmk-clt-install-prereqs). Se si installa il client usando un file con estensione msi, l'installazione non riuscirà se mancano i prerequisiti.

2. Per usare uno script per installare il client App-V 5,0, usare i parametri seguenti con **appv\_client\_setup.exe**.

   >[!NOTE]
   >Il client Windows Installer (con estensione msi) supporta lo stesso set di opzioni, fatta eccezione per il parametro **/log** .

   |                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   |----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |           /INSTALLDIR            |                                                                                                                                                               Specifica la directory di installazione. Esempio d'uso:<p><p>**/INSTALLDIR = C:\Program Files\AppV client**                                                                                                                                                                |
   |            /CEIPOPTIN            |                                                                                                                                                          Consente la partecipazione al programma Analisi utilizzo software. Esempio d'uso:<p><p>**/CEIPOPTIN = [0 \ | 1 \]**                                                                                                                                                           |
   |             /MUOPTIN             |                                                                                                                                                                                 Abilita Microsoft Update. Esempio d'uso:<p><p>**/MUOPTIN = [0 \ | 1 \]**                                                                                                                                                                                  |
   |     /PACKAGEINSTALLATIONROOT     |                                                                                                                                         Specifica la directory in cui installare tutte le nuove applicazioni e gli aggiornamenti. Esempio d'uso: <p><p>**/PACKAGEINSTALLATIONROOT =' pacchetti C:\App-V '**                                                                                                                                         |
   |        /PACKAGESOURCEROOT        |                                                                                                                                                  Sostituisce la posizione di origine per il download del contenuto del pacchetto. Esempio d'uso:<p><p>**/PACKAGESOURCEROOT =' <http://packageStore> '**                                                                                                                                                  |
   |            /AUTOLOAD             |                                                                                           Specifica il modo in cui i nuovi pacchetti verranno caricati da App-V 5,0 in un computer specifico. Le opzioni seguenti sono abilitate: [1]; caricare automaticamente tutti i pacchetti [2]; o caricare automaticamente nessun pacchetto [0]. Esempio d'uso:<p><p>**/AUTOLOAD = [0 \ | 1 \ | 2 \]**                                                                                           |
   |     /SHAREDCONTENTSTOREMODE      |                                                                                                                                           Specifica che il contenuto del pacchetto in streaming non verrà salvato nel disco rigido locale. Esempio d'uso: <p><p>**/SHAREDCONTENTSTOREMODE = [0 \ | 1 \]**                                                                                                                                            |
   |          /MIGRATIONMODE          |                                                                                                                     Consente al client App-V 5,0 di modificare i tasti di scelta rapida e i accordi associati ai pacchetti creati con una versione precedente. Esempio d'uso:<p><p>**/MIGRATIONMODE = [0 \ | 1 \]**                                                                                                                     |
   |      /ENABLEPACKAGESCRIPTS       |                                                                                                                                   Abilita gli script definiti nel file manifesto del pacchetto o nei file di configurazione che devono essere eseguiti. Esempio d'uso:<p><p>**/ENABLEPACKAGESCRIPTS = [0 \ | 1 \]**                                                                                                                                   |
   |    /ROAMINGREGISTRYEXCLUSIONS    |                                                                                                                                      Specifica i percorsi del registro di sistema che non andranno in roaming con un profilo utente. Esempio d'uso:<p><p>**/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients**                                                                                                                                      |
   |      /ROAMINGFILEEXCLUSIONS      |                                                                                                                                  Specifica i percorsi di file relativi a% USERPROFILE% che non sono in roaming con il profilo di un utente. Esempio d'uso: <p><p>**/ROAMINGFILEEXCLUSIONS ' desktop; immagini personali '**                                                                                                                                   |
   |   /S [1-5] PUBLISHINGSERVERNAME    |                                                                                                                                                           Visualizza il nome del server di pubblicazione. Esempio d'uso:<p><p>**/S2PUBLISHINGSERVERNAME = MyPublishingServer**                                                                                                                                                            |
   |    /S [1-5] PUBLISHINGSERVERURL    |                                                                                                                                                                Visualizza l'URL del server di pubblicazione. Esempio d'uso:<p><p>**/S2PUBLISHINGSERVERURL = \\pubserver**                                                                                                                                                                |
   |   /S [1-5] GLOBALREFRESHENABLED    |                                                                                                                                                                    Abilita un aggiornamento globale della pubblicazione. Esempio d'uso:<p><p>**/S2GLOBALREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                     |
   |   /S [1-5] GLOBALREFRESHONLOGON    |                                                                                                                                                             Avvia un aggiornamento della pubblicazione globale quando un utente esegue l'accesso. Esempio d'uso:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                              |
   |   /S [1-5] GLOBALREFRESHINTERVAL   |                                                                                                                                         Specifica l'intervallo di aggiornamento della pubblicazione, dove **0** indica che non viene aggiornato periodicamente. Esempio di utilizzo: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   | /S [1-5] GLOBALREFRESHINTERVALUNIT |                                                                                                                                                            Specifica l'unità di intervallo (ore [0], giorni [1]). Esempio d'uso:<p><p>**/S2GLOBALREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                            |
   |    /S [1-5] USERREFRESHENABLED     |                                                                                                                                                                          Consente di aggiornare la pubblicazione degli utenti. Esempio di utilizzo: **/S2USERREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                          |
   |    /S [1-5] USERREFRESHONLOGON     |                                                                                                                                                              Avvia un aggiornamento della pubblicazione degli utenti quando un utente esegue l'accesso. Esempio d'uso:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                               |
   |    /S [1-5] USERREFRESHINTERVAL    |                                                                                                                                         Specifica l'intervallo di aggiornamento della pubblicazione, dove **0** indica che non viene aggiornato periodicamente. Esempio di utilizzo: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   |  /S [1-5] USERREFRESHINTERVALUNIT  |                                                                                                                                                             Specifica l'unità di intervallo (ore [0], giorni [1]). Esempio d'uso:<p><p>**/S2USERREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                             |
   |               /Log               |                                                                                                                                                Specifica un percorso in cui vengono salvate le informazioni sul log. La posizione predefinita è% Temp%. Esempio d'uso:<p><p>**/log C:\logs\log.log**                                                                                                                                                |
   |                /nocancel/q                |                                                                                                                                                                                                Specifica un'installazione automatica.                                                                                                                                                                                                |
   |             /REPAIR              |                                                                                                                                                                                               Ripristina un'installazione precedente del client.                                                                                                                                                                                               |
   |            /NORESTART            | Impedisce il riavvio del computer dopo l'installazione del client.<p><p>Il parametro impedisce il riavvio del computer per gli utenti finali dopo l'installazione di ogni aggiornamento e consente di programmare la reinstallazione in base alle proprie esigenze. Ad esempio, è possibile installare App-V 5,0 SPX e quindi installare il pacchetto di hotfix Y senza riavviare il sistema dopo l'installazione del Service Pack. Dopo l'installazione, è necessario riavviare prima di iniziare a usare app-V. |
   |            /UNINSTALL            |                                                                                                                                                                                                       Disinstalla il client.                                                                                                                                                                                                        |
   |           /ACCEPTEULA            |                                                                                                                                              Accetta il contratto di licenza. Questa operazione è necessaria per un'installazione automatica. Esempio d'uso:<p><p>**/AcceptEula** o **/ACCEPTEULA = 1**                                                                                                                                               |
   |             /LAYOUT              |                                                                                                                               Specifica l'azione di layout associata. Estrae anche Windows Installer (. msi) e i file di script in una cartella senza installare App-V 5,0. Nessun valore previsto.                                                                                                                                |
   |            /LAYOUTDIR            |                                                                                                                                                 Specifica la directory del layout. Richiede un valore stringa. Esempio d'uso:<p><p>**/LAYOUTDIR = "client di virtualizzazione C:\Application"**                                                                                                                                                  |
   |          /?,/h,/Help           |                                                                                                                                                                                      Richiede informazioni sui parametri di installazione precedenti.                                                                                                                                                                                      |

   ---

## Per installare il client App-V 5,0 usando il file di Windows Installer (con estensione msi)

1. Installare i prerequisiti necessari nei computer di destinazione. Vedere [cosa fare prima di iniziare](#bkmk-clt-install-prereqs). Se i prerequisiti non sono soddisfatti, l'installazione avrà esito negativo.

2. Assicurarsi che i computer di destinazione non abbiano un riavvio in sospeso prima di installare il client con i file di Windows Installer (MSI) di App-V 5,0. I file di Windows Installer non contrassegnano un riavvio in sospeso.

3. Distribuire uno dei file di Windows Installer seguenti nel computer di destinazione. Il file specificato deve corrispondere alla configurazione del computer di destinazione.


   |                       Tipo di distribuzione                        |      Distribuire il file       |
   |-----------------------------------------------------------------|-----------------------------|
   | Il computer sta usando un sistema operativo Microsoft Windows a 32 bit |   appv_client_MSI_x86.msi   |
   | Il computer sta usando un sistema operativo Microsoft Windows a 64 bit |   appv_client_MSI_x64.msi   |
   | Si sta distribuendo il client Servizi Desktop remoto App-V 5,0  | appv_client_rds_MSI_x64.msi |

   ---

4. Usando le informazioni nella tabella seguente, selezionare il Language Pack **. msi** appropriato da installare, in base alla lingua desiderata per il computer di destinazione. Il **xxxx** nella tabella fa riferimento alle impostazioni locali di destinazione del Language Pack.

   **Informazioni da conoscere prima di iniziare:** 

   -  I Language Pack sono comuni sia al client standard App-V 5,0 che alla versione Servizi Desktop remoto del client App-V 5,0.

   -  Se si installa il client App-V 5,0 usando il **. exe**, il programma di installazione distribuirà solo il Language Pack che corrisponde al sistema operativo in uso nel computer di destinazione.

   -  Per distribuire altri Language Pack in un computer di destinazione, usare la procedura **per installare il client App-V 5,0 usando il file di Windows Installer (con estensione msi)**.

   |                       Tipo di distribuzione                        |       Distribuire il file       |
   |-----------------------------------------------------------------|------------------------------|
   | Il computer sta usando un sistema operativo Microsoft Windows a 32 bit | appv_client_LP_xxxx_ x86.msi |
   | Il computer sta usando un sistema operativo Microsoft Windows a 64 bit | appv_client_LP_xxxx_ x64.msi |

   ---

   **Hai un suggerimento per App-V**? Aggiungere o votare [suggerimenti](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). <p><p>**Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Distribuzione di App-V 5.0](deploying-app-v-50.md)

[Informazioni sulle impostazioni di configurazione client](about-client-configuration-settings.md)

[Come disinstallare il client App-V 5.0](how-to-uninstall-the-app-v-50-client.md)
