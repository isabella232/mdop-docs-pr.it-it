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
ms.openlocfilehash: 4b2cbf333c705088d0a068521fb65e99551bb1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826226"
---
# Come abilitare BitLocker usando MBAM come parte di una distribuzione di Windows


Questo argomento spiega come abilitare BitLocker nel computer di un utente finale usando MBAM nell'ambito del processo di creazione di immagini e distribuzione di Windows. Se viene visualizzata una schermata nera al riavvio (dopo la conclusione dell'installazione) che indica che l'unità non può essere sbloccata, vedere le [versioni precedenti di Windows non iniziano dopo il passaggio "configurazione di Windows e gestione configurazione" Se si usa BitLocker con Windows 10, versione 1511](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).

**Prerequisiti:**

-   Un processo di distribuzione di immagini Windows esistente: Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager o qualche altro strumento di imaging o processo, deve essere in posizione

-   Il TPM deve essere abilitato nel BIOS e visibile al sistema operativo

-   L'infrastruttura del server MBAM deve essere in posizione e accessibile

-   La partizione di sistema richiesta da BitLocker deve essere creata

-   La macchina deve essere collegata al dominio durante l'imaging prima che MBAM consenta completamente BitLocker

**Per abilitare BitLocker con MBAM 2,5 SP1 come parte di una distribuzione di Windows**

1. In MBAM 2,5 SP1 l'approccio consigliato per abilitare BitLocker durante una distribuzione di Windows consiste nell'usare lo `Invoke-MbamClientDeployment.ps1` script di PowerShell.

   -   Lo `Invoke-MbamClientDeployment.ps1` script attiva BitLocker durante il processo di imaging. Quando necessario per i criteri di BitLocker, l'agente MBAM chiede immediatamente all'utente del dominio di creare un PIN o una password quando l'utente del dominio accede prima dopo l'imaging.

   -   Facile da usare con MDT, System Center Configuration Manager o processi di imaging autonomi

   -   Compatibile con PowerShell 2,0 o versioni successive

   -   Crittografare il volume del sistema operativo con il Protector Key TPM

   -   Supportare completamente BitLocker pre-provisioning

   -   Facoltativamente crittografare FDDs

   -   TPM OwnerAuth per Windows 7, MBAM deve essere proprietario del TPM per l'impegno.
   Per Windows 8,1, Windows 10 RTM e Windows 10 versione 1511 è supportato l'impegno di TPM OwnerAuth.
   Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per ulteriori informazioni, vedere [password del proprietario del TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

   -   Chiavi di ripristino escrow e pacchetti chiave di ripristino

   -   Segnalare immediatamente lo stato di crittografia

   -   Nuovi provider WMI

   -   Registrazione dettagliata

   -   Gestione degli errori affidabile

   È possibile scaricare lo `Invoke-MbamClientDeployment.ps1` script dall' [area download Microsoft.com](https://www.microsoft.com/download/details.aspx?id=54439). Questo è lo script principale che verrà chiamato dal sistema di distribuzione per configurare le chiavi di crittografia unità BitLocker e di ripristino record con il server MBAM.

   **Metodi di distribuzione WMI per mbam:** I metodi WMI seguenti sono stati aggiunti in MBAM 2,5 SP1 per supportare l'abilitazione di BitLocker tramite lo `Invoke-MbamClientDeployment.ps1` script di PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>**Mbam \ _Machine classe WMI** 
    **PrepareTpmAndEscrowOwnerAuth:** Legge il TPM OwnerAuth e lo invia al database di ripristino MBAM usando il servizio di ripristino MBAM. Se il TPM non è di proprietà e il provisioning automatico non è attivato, genera un OwnerAuth TPM e assume la proprietà. In caso di esito negativo, viene restituito un codice di errore per la risoluzione dei problemi.

   **Nota** Per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per ulteriori informazioni, vedere [password del proprietario del TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

| Parametro | Descrizione |
| -------- | ----------- |
| RecoveryServiceEndPoint | Stringa che specifica l'endpoint del servizio di ripristino MBAM. |

Ecco un elenco di messaggi di errore comuni:

| Valori restituiti comuni | Messaggio di errore |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | Il metodo ha avuto esito positivo. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | TPM non è presente nel computer o è disabilitato nella configurazione del BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | TPM non è nello stato corretto (abilitato, attivato e installazione del proprietario consentita). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM non può assumere la proprietà del TPM perché il provisioning automatico è in sospeso. Riprovare dopo il completamento del provisioning automatico. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM non può leggere il valore di autorizzazione del proprietario del TPM. Il valore potrebbe essere stato rimosso dopo un escrow riuscito. In Windows 7 MBAM non è in grado di leggere il valore se il TPM è di proprietà di altri utenti. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | Il computer deve essere riavviato per impostare TPM sullo stato corretto. Potrebbe essere necessario riavviare manualmente il computer. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | Il computer deve essere arrestato e riattivato per impostare TPM sullo stato corretto. Potrebbe essere necessario riavviare manualmente il computer. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L'accesso è stato negato dall'endpoint remoto. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | L'endpoint remoto non esiste o non è possibile trovarlo. |
| * * WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | L'endpoint remoto non ha potuto elaborare la richiesta. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | L'endpoint remoto non è raggiungibile. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un messaggio contenente un errore è stato ricevuto dall'endpoint remoto. Verificare di essere connessi all'endpoint di servizio corretto. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | L'URL dell'indirizzo endpoint non è valido. L'URL deve iniziare con "http" o "https". |

   **ReportStatus:** Legge lo stato di conformità del volume e lo invia al database di stato di conformità di MBAM usando il servizio di segnalazione dello stato di MBAM. Lo stato include la forza di cifratura, il tipo di protezione, lo stato di protezione e la crittografia. In caso di esito negativo, viene restituito un codice di errore per la risoluzione dei problemi.

   | Parametro | Descrizione |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Stringa che specifica l'endpoint del servizio Segnalazione stato di MBAM. |

   Ecco un elenco di messaggi di errore comuni:

   | Valori restituiti comuni | Messaggio di errore |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | Il metodo ha avuto esito positivo |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L'accesso è stato negato dall'endpoint remoto.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | L'endpoint remoto non esiste o non è possibile trovarlo. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | L'endpoint remoto non ha potuto elaborare la richiesta. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | L'endpoint remoto non è raggiungibile. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un messaggio contenente un errore è stato ricevuto dall'endpoint remoto. Verificare di essere connessi all'endpoint di servizio corretto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | L'URL dell'indirizzo endpoint non è valido. L'URL deve iniziare con "http" o "https". |

   <a href="" id="mbam-volume-wmi-class"></a>**Mbam \ _VOLUME WMI class** **EscrowRecoveryKey:** legge la password di ripristino numerico e il pacchetto di tasti del volume e li invia al database di ripristino MBAM usando il servizio di ripristino MBAM. In caso di esito negativo, viene restituito un codice di errore per la risoluzione dei problemi.

   | Parametro | Descrizione |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Stringa che specifica l'endpoint del servizio di ripristino MBAM. |

   Ecco un elenco di messaggi di errore comuni:

   | Valori restituiti comuni | Messaggio di errore |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | Il metodo ha avuto esito positivo |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | Il volume è bloccato. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | Non è stato trovato un Protector password numerico per il volume. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | L'accesso è stato negato dall'endpoint remoto. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | L'endpoint remoto non esiste o non è possibile trovarlo. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | L'endpoint remoto non ha potuto elaborare la richiesta. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | L'endpoint remoto non è raggiungibile. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Un messaggio contenente un errore è stato ricevuto dall'endpoint remoto. Verificare di essere connessi all'endpoint di servizio corretto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | L'URL dell'indirizzo endpoint non è valido. L'URL deve iniziare con "http" o "https". |
     

2. **Distribuire MBAM usando Microsoft Deployment Toolkit (MDT) e PowerShell**

   1.  In MDT creare una nuova condivisione di distribuzione o aprire una condivisione di distribuzione esistente.

       **Nota**  
       Lo `Invoke-MbamClientDeployment.ps1` script di PowerShell può essere usato con qualsiasi processo di imaging o strumento. Questa sezione illustra come integrarla usando MDT, ma i passaggi sono simili all'integrazione con qualsiasi altro processo o strumento.

       **Attenzione**  
       Se si usa BitLocker pre-provisioning (WinPE) e si vuole mantenere il valore di autorizzazione del proprietario del TPM, è necessario aggiungere lo `SaveWinPETpmOwnerAuth.wsf` script in WinPE immediatamente prima che l'installazione venga riavviata nel sistema operativo completo. **Se non si usa questo script, il valore di autorizzazione del proprietario del TPM verrà perso al riavvio.**

   2.  Copia `Invoke-MbamClientDeployment.ps1` in ** &lt; DeploymentShare &gt; \\Scripts**. Se si usa il provisioning preliminare, copiare il `SaveWinPETpmOwnerAuth.wsf` file in ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Aggiungere l'applicazione client MBAM 2,5 SP1 al nodo applicazioni della condivisione di distribuzione.

       1.  Nel nodo **applicazioni** fare clic su **nuova applicazione**.

       2.  Selezionare l' **applicazione con i file di origine**. Fai clic su **Avanti**.

       3.  In **nome applicazione**Digitare "MBAM 2,5 client SP1". Fai clic su **Avanti**.

       4.  Passare alla directory che contiene `MBAMClientSetup-<Version>.msi` . Fai clic su **Avanti**.

       5.  Digitare "MBAM 2,5 SP1 client" come directory da creare. Fai clic su **Avanti**.

       6.  Immettere `msiexec /i MBAMClientSetup-<Version>.msi /quiet` alla riga di comando. Fai clic su **Avanti**.

       7.  Accettare i valori predefiniti rimanenti per completare la procedura guidata nuova applicazione.

   4.  In MDT fare clic con il pulsante destro del mouse sul nome della condivisione di distribuzione e scegliere **Proprietà**. Fare clic sulla scheda **regole** . aggiungere le righe seguenti:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Fare clic su OK per chiudere la finestra.

   5.  Nel nodo sequenze attività modificare una sequenza di attività esistente usata per la distribuzione di Windows. Se si vuole, è possibile creare una nuova sequenza di attività facendo clic con il pulsante destro del mouse sul nodo **sequenze attività** , selezionando **nuova sequenza di attività**e completando la procedura guidata.

       Nella scheda **sequenza attività** della sequenza di attività selezionata eseguire questa procedura:

       1.  Nella cartella **Preinstall** abilitare l'attività facoltativa **abilitare BitLocker (offline)** se si vuole che BitLocker sia abilitato in WinPE, che esegue la crittografia solo dello spazio usato.

       2.  Per rendere persistente il TPM OwnerAuth quando si usa il pre-provisioning, per consentire a MBAM di escrowlo in seguito, eseguire le operazioni seguenti:

           1.  Trovare il passaggio per l' **installazione del sistema operativo**

           2.  Aggiungere un nuovo passaggio della **riga di comando Esegui**

           3.  Denominare il passaggio **persist TPM OwnerAuth**

           4.  Impostare la riga di comando su `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **Nota:** per Windows 10, versione 1607 o successiva, solo Windows può assumere la proprietà del TPM. In addiiton Windows non manterrà la password del proprietario del TPM durante il provisioning del TPM. Per ulteriori informazioni, vedere [password del proprietario del TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

       3.  Nella cartella **Ripristino stato** eliminare l'attività **Abilita BitLocker** .

       4.  Nella cartella **ripristino dello stato** in **attività personalizzate**creare una nuova attività di **installazione dell'applicazione** e denominarla **Install mbam Agent**. Fare clic sul pulsante di opzione **Installa singola applicazione** e passare all'applicazione client MBAM 2,5 SP1 creata in precedenza.

       5.  Nella cartella **ripristino dello stato** in **attività personalizzate**creare una nuova attività di **script di PowerShell** per l'esecuzione (dopo il passaggio di applicazione client MBAM 2,5 SP1) con le impostazioni seguenti (aggiornare i parametri come appropriato per l'ambiente):

           -   Nome: configurare BitLocker per MBAM

           -   Script di PowerShell: `Invoke-MbamClientDeployment.ps1`

           -   Parametri

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
               <td align="left"><p>Endpoint del servizio Reporting di stato MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Facoltativo</p></td>
               <td align="left"><p>Metodo di crittografia (impostazione predefinita: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare per crittografare i volumi di dati e i tasti di ripristino del volume di dati escrow</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare per attendere il completamento della crittografia</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare che lo script di distribuzione non riprende la crittografia sospesa</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare per ignorare l'errore di escrow Owner-auth. Dovrebbe essere usato negli scenari in cui MBAM non è in grado di leggere il TPM owner-auth, ad esempio se è abilitato il provisioning automatico TPM</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare per ignorare l'errore della chiave di recupero del volume</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Opzione</p></td>
               <td align="left"><p>Specificare per ignorare l'errore di segnalazione dello stato</p></td>
               </tr>
               </tbody>
               </table>

                 

**Per abilitare BitLocker con MBAM 2,5 o versioni precedenti come parte di una distribuzione di Windows**

1.  Installare il client MBAM. Per istruzioni, Vedi [come distribuire il client mbam usando una riga di comando](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Aggiungere il computer a un dominio (scelta consigliata).

    -   Se il computer non è collegato a un dominio, la password di ripristino non viene archiviata nel servizio di ripristino di chiave MBAM. Per impostazione predefinita, MBAM non consente la crittografia a meno che non sia possibile archiviare la chiave di ripristino.

    -   Se un computer viene avviato in modalità di ripristino prima che la chiave di ripristino sia archiviata nel server MBAM, non è disponibile alcun metodo di ripristino e il computer deve essere rielaborato.

3.  Aprire un prompt dei comandi come amministratore e arrestare il servizio MBAM.

4.  Impostare il servizio su **manuale** o **su richiesta** digitando i comandi seguenti:

    **NET STOP mbamagent**

    **sc config mbamagent start = demand**

5.  Imposta i valori del registro di sistema in modo che il client MBAM ignori le impostazioni dei criteri di gruppo e invece imposti la crittografia per avviare l'ora di distribuzione di Windows nel computer client.

    **Attenzione**  Questo passaggio descrive come modificare il registro di sistema di Windows. L'uso errato dell'editor del registro di sistema può causare seri problemi che possono richiedere la reinstallazione di Windows. Non è possibile garantire che i problemi risultanti dall'uso errato dell'editor del registro di sistema possano essere risolti. Usare l'editor del registro di sistema a proprio rischio.

    1.  Impostare il TPM per il **sistema operativo solo**per la crittografia, eseguire Regedit.exe e quindi importare il modello di chiave del registro di C:\\Programmi Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  In Regedit.exe accedere a HKLM\\SOFTWARE\\Microsoft\\MBAM e configurare le impostazioni elencate nella tabella seguente.

        **Nota**  Puoi impostare le impostazioni dei criteri di gruppo o i valori del registro di sistema correlati a MBAM qui. Queste impostazioni sovrascriveranno i valori impostati in precedenza.

        Impostazioni di configurazione della voce del registro di sistema

        DeploymentTime

        0 = disattivato

        1 = usare le impostazioni dei criteri per il tempo di distribuzione (impostazione predefinita): usare questa impostazione per abilitare la crittografia al momento della distribuzione di Windows nel computer client.

        UseKeyRecoveryService

        0 = non usare l'escrow Key (le due voci del registro di sistema successive non sono necessarie in questo caso)

        1 = usare l'escrow Key nel sistema di recupero chiavi (impostazione predefinita)

        Questa è l'impostazione consigliata, che consente a MBAM di archiviare le chiavi di ripristino. Il computer deve essere in grado di comunicare con il servizio di ripristino tramite MBAM Key. Verificare che il computer sia in grado di comunicare con il servizio prima di procedere.

        KeyRecoveryOptions

        0 = carica solo il tasto di ripristino

        1 = carica il tasto di ripristino e il pacchetto di ripristino della chiave (impostazione predefinita)

        KeyRecoveryServiceEndPoint

        Imposta questo valore sull'URL per il server che gestisce il servizio di recupero chiavi, ad esempio http:// &lt; nome computer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  Il client MBAM ricomincerà il sistema durante la distribuzione del client MBAM. Quando si è pronti per il riavvio, eseguire il comando seguente al prompt dei comandi come amministratore:

    **NET Start mbamagent**

7.  Quando il computer viene riavviato e il BIOS richiede di accettare la modifica del TPM.

8.  Durante il processo di imaging del sistema operativo client Windows, quando si è pronti per avviare la crittografia, aprire un prompt dei comandi come amministratore e digitare i comandi seguenti per impostare l'avvio **automatico** e riavviare l'agente client mbam:

    **sc config mbamagent Start = automatico**

    **NET Start mbamagent**

9.  Per eliminare i valori di bypass del registro di sistema, eseguire Regedit.exe e passare alla voce del registro di sistema HKLM\\SOFTWARE\\Microsoft. Fare clic con il pulsante destro del mouse sul nodo **mbam** e quindi scegliere **Elimina**.

## Argomenti correlati

[Distribuzione del client di MBAM 2.5](deploying-the-mbam-25-client.md)

[Pianificazione della distribuzione del client di MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
