---
title: Come abilitare BitLocker usando MBAM come parte di una distribuzione di Windows
description: Come abilitare BitLocker usando MBAM come parte di una distribuzione di Windows
author: dansimp
ms.assetid: 7609ad7a-bb06-47be-b186-0a2db787c8a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: cd4086ca6bb2ea8d253ea3b743f4efe7efbbb6c1
ms.sourcegitcommit: 325c4b77f9a9df0f3de268457fed06184623bb94
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "11626183"
---
# <a name="how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deployment"></a>Come abilitare BitLocker usando MBAM come parte di una distribuzione di Windows

> [!IMPORTANT]
> Queste istruzioni non riguardano Gestione BitLocker di Configuration Manager. Lo `Invoke-MbamClientDeployment.ps1` script di PowerShell non è supportato per l'utilizzo con Gestione BitLocker in Configuration Manager. Ciò include la deposito delle chiavi di ripristino di BitLocker durante una sequenza di attività di Configuration Manager. Inoltre, a partire da Configuration Manager Current Branch 2103, Configuration Manager BitLocker Management non usa più il sito dei servizi di ripristino delle chiavi MBAM per depositare le chiavi. Se si tenta di utilizzare lo script di PowerShell con `Invoke-MbamClientDeployment.ps1` Configuration Manager Current Branch 2103 o versione più recente, possono verificarsi seri problemi con il sito di Configuration Manager. I problemi noti includono la creazione di una grande quantità di criteri destinati a tutti i dispositivi che possono causare tempeste di criteri. In questo modo si verifica una grave riduzione delle prestazioni in Configuration Manager principalmente in SQL e con i punti di gestione.

In questo argomento viene illustrato come abilitare BitLocker nel computer di un utente finale utilizzando MBAM come parte del processo Windows di creazione di immagini e distribuzione. Se viene visualizzata una schermata nera al riavvio (al termine della fase di installazione) che indica che l'unità non può essere sbloccata, vedere Le versioni precedenti di Windows non vengono avviate dopo il passaggio "Setup Windows and Configuration Manager" se viene utilizzato [Il pre-provisioning di BitLocker con Windows 10, versione 1511.](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo)

**Prerequisiti:**

-   Deve essere presente un processo di distribuzione di immagini Windows esistente, ovvero Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager o un altro strumento o processo di creazione di immagini.

-   Il TPM deve essere abilitato nel BIOS e visibile al sistema operativo

-   L'infrastruttura del server MBAM deve essere sul posto e accessibile

-   La partizione di sistema richiesta da BitLocker deve essere creata

-   Il computer deve essere aggiunto a un dominio durante l'acquisizione di immagini prima che MBAM a abilita completamente BitLocker

**Per abilitare BitLocker con MBAM 2.5 SP1 come parte di una Windows distribuzione**

1. In MBAM 2.5 SP1, l'approccio consigliato per abilitare BitLocker durante una distribuzione di Windows consiste nell'usare lo `Invoke-MbamClientDeployment.ps1` script di PowerShell.

   -   Lo `Invoke-MbamClientDeployment.ps1` script emula BitLocker durante il processo di creazione di immagini. Se richiesto dai criteri di BitLocker, l'agente MBAM richiede immediatamente all'utente di dominio di creare un PIN o una password quando l'utente di dominio accede per la prima volta dopo la creazione di immagini.

   -   Facile da usare con MDT, System Center Configuration Manager o processi di creazione di immagini autonomi

   -   Compatibile con PowerShell 2.0 o versione successiva

   -   Crittografare il volume del sistema operativo con la protezione delle chiavi TPM

   -   Supporto completo del pre-provisioning di BitLocker

   -   Facoltativamente crittografare gli FDD

   -   Escrow TPM OwnerAuth Per Windows 7, MBAM deve essere proprietario del TPM perché la deposito si verifichi.
   Ad Windows 8.1, Windows 10 RTM e Windows 10 versione 1511, è supportata la deposito di TPM OwnerAuth.
   Ad Windows 10 versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton, Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per [ulteriori dettagli, vedere Password del proprietario del TPM.](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password)

   -   Chiavi di ripristino deposito e pacchetti di chiavi di ripristino

   -   Segnalare immediatamente lo stato di crittografia

   -   Nuovi provider WMI

   -   Registrazione dettagliata

   -   Gestione degli errori affidabile

   È possibile scaricare lo `Invoke-MbamClientDeployment.ps1` script [dall Microsoft.com Download Center.](https://www.microsoft.com/download/details.aspx?id=54439) Questo è lo script principale che il sistema di distribuzione chiamerà per configurare la crittografia dell'unità BitLocker e registrare le chiavi di ripristino con il server MBAM.

   **Metodi di distribuzione WMI per MBAM:** In MBAM 2.5 SP1 sono stati aggiunti i metodi WMI seguenti per supportare l'abilitazione di BitLocker tramite lo `Invoke-MbamClientDeployment.ps1` script di PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>**Classe WMI MBAM\_Machine** 
    **PrepareTpmAndEscrowOwnerAuth:** Legge il TPM OwnerAuth e lo invia al database di ripristino mbam utilizzando il servizio di ripristino MBAM. Se il TPM non è di proprietà e il provisioning automatico non è in corso, viene generato un TPM OwnerAuth e ne diventa la proprietà. Se non riesce, viene restituito un codice di errore per la risoluzione dei problemi.

   **Nota** Ad Windows 10 versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton, Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per [ulteriori dettagli, vedere Password del proprietario del TPM.](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password)

| Parametro | Descrizione |
| -------- | ----------- |
| RecoveryServiceEndPoint | Stringa che specifica l'endpoint del servizio di ripristino MBAM. |

Ecco un elenco di messaggi di errore comuni:

| Valori restituiti comuni | Messaggio di errore |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | Il metodo ha avuto esito positivo. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | Il TPM non è presente nel computer o è disabilitato nella configurazione del BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | Il TPM non è nello stato corretto (è consentita l'installazione abilitata, attivata e proprietaria). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM non può assumere la proprietà del TPM perché il provisioning automatico è in sospeso. Riprovare al termine del provisioning automatico. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM non è in grado di leggere il valore di autorizzazione del proprietario del TPM. Il valore potrebbe essere stato rimosso dopo un deposito corretto. In Windows 7, MBAM non è in grado di leggere il valore se il TPM è di proprietà di altri utenti. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | Il computer deve essere riavviato per impostare il TPM sullo stato corretto. Potrebbe essere necessario riavviare manualmente il computer. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | Per impostare il TPM sullo stato corretto, è necessario arrestare e rie spegnere il computer. Potrebbe essere necessario riavviare manualmente il computer. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Accesso negato dall'endpoint remoto. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | L'endpoint remoto non esiste o non è stato possibile individuarsi. |
| **WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | L'endpoint remoto non è in grado di elaborare la richiesta. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | L'endpoint remoto non è raggiungibile. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | È stato ricevuto un messaggio contenente un errore dall'endpoint remoto. Assicurarsi di connettersi all'endpoint del servizio corretto. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | L'URL dell'indirizzo dell'endpoint non è valido. L'URL deve iniziare con "http" o "https". |

   **ReportStatus:** Legge lo stato di conformità del volume e lo invia al database dello stato di conformità MBAM utilizzando il servizio di segnalazione dello stato mbam. Lo stato include la forza di crittografia, il tipo di protezione, lo stato del protettore e lo stato di crittografia. Se non riesce, viene restituito un codice di errore per la risoluzione dei problemi.

   | Parametro | Descrizione |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Stringa che specifica l'endpoint del servizio di segnalazione dello stato MBAM. |

   Ecco un elenco di messaggi di errore comuni:

   | Valori restituiti comuni | Messaggio di errore |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | Il metodo ha avuto esito positivo |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Accesso negato dall'endpoint remoto.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | L'endpoint remoto non esiste o non è stato possibile individuarsi. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | L'endpoint remoto non è in grado di elaborare la richiesta. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | L'endpoint remoto non è raggiungibile. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | È stato ricevuto un messaggio contenente un errore dall'endpoint remoto. Assicurarsi di connettersi all'endpoint del servizio corretto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | L'URL dell'indirizzo dell'endpoint non è valido. L'URL deve iniziare con "http" o "https". |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM\_Volume Classe WMI** **EscrowRecoveryKey:** legge la password numerica di ripristino e il pacchetto di chiavi del volume e le invia al database di ripristino MBAM utilizzando il servizio di ripristino MBAM. Se non riesce, viene restituito un codice di errore per la risoluzione dei problemi.

   | Parametro | Descrizione |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Stringa che specifica l'endpoint del servizio di ripristino MBAM. |

   Ecco un elenco di messaggi di errore comuni:

   | Valori restituiti comuni | Messaggio di errore |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | Il metodo ha avuto esito positivo |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | Il volume è bloccato. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Impossibile trovare una protezione con password numerica per il volume. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | Accesso negato dall'endpoint remoto. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | L'endpoint remoto non esiste o non è stato possibile individuarsi. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | L'endpoint remoto non è in grado di elaborare la richiesta. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | L'endpoint remoto non è raggiungibile. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | È stato ricevuto un messaggio contenente un errore dall'endpoint remoto. Assicurarsi di connettersi all'endpoint del servizio corretto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | L'URL dell'indirizzo dell'endpoint non è valido. L'URL deve iniziare con "http" o "https". |
     

2. **Distribuire MBAM tramite Microsoft Deployment Toolkit (MDT) e PowerShell**

   1.  In MDT crea una nuova condivisione di distribuzione o apri una condivisione di distribuzione esistente.

       **Nota**  
       Lo `Invoke-MbamClientDeployment.ps1` script di PowerShell può essere utilizzato con qualsiasi processo o strumento di creazione di immagini. Questa sezione illustra come integrarla tramite MDT, ma i passaggi sono simili all'integrazione con qualsiasi altro processo o strumento.

       **Attenzione**  
       Se si usa il pre-provisioning di BitLocker (WinPE) e si desidera mantenere il valore di autorizzazione del proprietario del TPM, è necessario aggiungere lo script in WinPE immediatamente prima del riavvio dell'installazione nel sistema operativo `SaveWinPETpmOwnerAuth.wsf` completo. **Se non si utilizza questo script, si perderà il valore di autorizzazione del proprietario del TPM al riavvio.**

   2.  Copia `Invoke-MbamClientDeployment.ps1` in ** &lt; DeploymentShare &gt; \\Scripts**. Se si utilizza il pre-provisioning, copiare il `SaveWinPETpmOwnerAuth.wsf` file in ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Aggiungere l'applicazione client MBAM 2.5 SP1 al nodo Applicazioni nella condivisione di distribuzione.

       1.  Nel nodo **Applicazioni** fare clic su **Nuova applicazione.**

       2.  Selezionare **Applicazione con file di origine**. Fai clic su **Avanti**.

       3.  In **Nome applicazione**digitare "MBAM 2.5 SP1 Client". Fai clic su **Avanti**.

       4.  Passare alla directory contenente `MBAMClientSetup-<Version>.msi` . Fai clic su **Avanti**.

       5.  Digitare "MBAM 2.5 SP1 Client" come directory da creare. Fai clic su **Avanti**.

       6.  Invio `msiexec /i MBAMClientSetup-<Version>.msi /quiet` alla riga di comando. Fai clic su **Avanti**.

       7.  Accettare le impostazioni predefinite rimanenti per completare la procedura guidata Nuova applicazione.

   4.  In MDT fai clic con il pulsante destro del mouse sul nome della condivisione di distribuzione e fai clic su **Proprietà.** Fare clic **sulla scheda** Regole. Aggiungere le righe seguenti:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Fare clic su OK per chiudere la finestra.

   5.  Nel nodo Sequenze di attività modificare una sequenza di attività esistente usata per Windows distribuzione. Se si desidera, è possibile creare una nuova sequenza di attività facendo clic con il pulsante destro del mouse sul nodo **Sequenze** di attività, selezionando **Nuova sequenza di**attività e completando la procedura guidata.

       Nella scheda **Sequenza di attività** della sequenza di attività selezionata eseguire la procedura seguente:

       1.  Nella cartella **Preinstalla** abilita l'attività facoltativa **Abilita BitLocker (offline)** se vuoi abilitare BitLocker in WinPE, che crittografa solo lo spazio usato.

       2.  Per mantenere TPM OwnerAuth quando si usa il pre-provisioning, consentendo a MBAM di depositarlo in un secondo momento, eseguire le operazioni seguenti:

           1.  Individuare il **passaggio Installa sistema** operativo

           2.  Aggiungere un nuovo **passaggio esegui riga di** comando dopo di esso

           3.  Assegnare al passaggio **il nome Persist TPM OwnerAuth**

           4.  Impostare la riga di comando su `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **Nota:** per Windows 10 versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton, Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per [ulteriori dettagli, vedere Password del proprietario del TPM.](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password)

       3.  Nella cartella **State Restore** eliminare l'attività **Enable BitLocker.**

       4.  Nella cartella **State Restore** in **Custom Tasks**crea una nuova attività Install **Application** e denotieni **Install MBAM Agent.** Fare clic **sul pulsante di opzione Installa** singola applicazione e passare all'applicazione client MBAM 2.5 SP1 creata in precedenza.

       5.  Nella cartella **State Restore** in **Custom Tasks**creare una nuova attività **Run PowerShell Script** (dopo il passaggio dell'applicazione client MBAM 2.5 SP1) con le impostazioni seguenti (aggiornare i parametri in base all'ambiente):

           -   Nome: Configurare BitLocker per MBAM

           -   Script di PowerShell: `Invoke-MbamClientDeployment.ps1`

           -   Parametri:

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p>-RecoveryServiceEndpoint</p></td>
               <td align="left"><p>Obbligatorio</p></td>
               <td align="left"><p>Endpoint del servizio di ripristino MBAM</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Facoltativo</p></td>
               <td align="left"><p>Endpoint del servizio di segnalazione dello stato MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Facoltativo</p></td>
               <td align="left"><p>Metodo di crittografia (impostazione predefinita: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare se crittografare i volumi di dati e le chiavi di ripristino del volume di dati di deposito</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare di attendere il completamento della crittografia</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare che lo script di distribuzione non riprenderà la crittografia sospesa</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specifica di ignorare l'errore di deposito proprietario-autenticazione TPM. Deve essere usato negli scenari in cui MBAM non è in grado di leggere l'autorizzazione del proprietario del TPM, ad esempio se il provisioning automatico TPM è abilitato</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specifica di ignorare l'errore di deposito chiave di ripristino del volume</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specifica di ignorare gli errori di segnalazione dello stato</p></td>
               </tr>
               </tbody>
               </table>

                 

**Per abilitare BitLocker con MBAM 2.5 o versioni precedenti come parte di una Windows distribuzione**

1.  Installare il client MBAM. Per istruzioni, vedere [Come distribuire il client MBAM tramite una riga di comando.](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

2.  Aggiungere il computer a un dominio (scelta consigliata).

    -   Se il computer non fa parte di un dominio, la password di ripristino non viene archiviata nel servizio di ripristino delle chiavi MBAM. Per impostazione predefinita, MBAM non consente la crittografia a meno che non sia possibile archiviare la chiave di ripristino.

    -   Se un computer viene avviato in modalità di ripristino prima che la chiave di ripristino sia archiviata nel server MBAM, non è disponibile alcun metodo di ripristino e il computer deve essere ricreato.

3.  Aprire un prompt dei comandi come amministratore e arrestare il servizio MBAM.

4.  Impostare il servizio su **Manuale** o **Su richiesta** digitando i comandi seguenti:

    **net stop mbamagent**

    **sc config mbamagent start= demand**

5.  Imposta i valori del Registro di sistema in modo che il client MBAM ignori le impostazioni di Criteri di gruppo e invece imposta la crittografia in modo da avviare l'Windows in quel computer client.

    **Attenzione**  
    Questo passaggio descrive come modificare il Registro di Windows registro. L'utilizzo non corretto dell'editor del Registro di sistema può causare seri problemi che possono richiedere la reinstallazione Windows. Non è possibile garantire che i problemi derivanti dall'utilizzo errato dell'editor del Registro di sistema possano essere risolti. Utilizzare l'editor del Registro di sistema a proprio rischio.

    1.  Impostare il TPM solo per la crittografia del sistema **operativo,** eseguire Regedit.exe e quindi importare il modello di chiave del Registro di sistema da C:\\Programmi\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  In Regedit.exe, passare a HKLM\\SOFTWARE\\Microsoft\\MBAM e configurare le impostazioni elencate nella tabella seguente.

        **Nota**  
        Puoi impostare le impostazioni di Criteri di gruppo o i valori del Registro di sistema correlati a MBAM qui. Queste impostazioni sovrascriveranno i valori impostati in precedenza.

        Voce del Registro di sistema Impostazioni di configurazione

        DeploymentTime

        0 = Disattivato

        1 = Utilizzare le impostazioni dei criteri tempo di distribuzione (impostazione predefinita): utilizzare questa impostazione per abilitare la crittografia al momento della distribuzione Windows nel computer client.

        UseKeyRecoveryService

        0 = Non utilizzare deposito chiavi (in questo caso non sono necessarie le due voci del Registro di sistema seguenti)

        1 = Usa deposito chiavi nel sistema di ripristino delle chiavi (impostazione predefinita)

        Questa è l'impostazione consigliata, che consente a MBAM di archiviare le chiavi di ripristino. Il computer deve essere in grado di comunicare con il servizio di ripristino delle chiavi MBAM. Verificare che il computer sia in grado di comunicare con il servizio prima di procedere.

        KeyRecoveryOptions

        0 = Carica solo chiave di ripristino

        1 = Carica la chiave di ripristino e il pacchetto di ripristino delle chiavi (impostazione predefinita)

        KeyRecoveryServiceEndPoint

        Impostare questo valore sull'URL del server che esegue il servizio di ripristino delle chiavi, ad esempio http:// &lt; nome computer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  Il client MBAM riavvierà il sistema durante la distribuzione del client MBAM. Quando si è pronti per il riavvio, eseguire il comando seguente al prompt dei comandi come amministratore:

    **net start mbamagent**

7.  Quando i computer vengono riavviati e viene richiesto il BIOS, accettare la modifica del TPM.

8.  Durante il processo di creazione di immagini del sistema operativo client di Windows, quando si è pronti per avviare **** la crittografia, aprire un prompt dei comandi come amministratore e digitare i comandi seguenti per impostare l'avvio su Automatico e riavviare l'agente client MBAM:

    **sc config mbamagent start= auto**

    **net start mbamagent**

9.  Per eliminare i valori bypass del Registro di sistema, eseguire Regedit.exe e passare alla voce del Registro di sistema HKLM\\SOFTWARE\\Microsoft. Fare clic con il pulsante destro del mouse sul nodo **MBAM** e quindi scegliere **Elimina**.

## <a name="related-topics"></a>Argomenti correlati

[Distribuzione del client di MBAM 2.5](deploying-the-mbam-25-client.md)

[Pianificazione della distribuzione del client di MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a name="got-a-suggestion-for-mbam"></a>Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi relativi a MBAM, utilizzare il [Forum TechNet di MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
