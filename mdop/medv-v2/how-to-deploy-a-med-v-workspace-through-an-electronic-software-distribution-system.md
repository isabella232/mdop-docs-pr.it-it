---
title: Come distribuire un'area di lavoro MED-V con un sistema di distribuzione elettronica del software
description: Come distribuire un'area di lavoro MED-V con un sistema di distribuzione elettronica del software
author: dansimp
ms.assetid: b5134c35-e1de-470c-93f8-ead6218d9dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56d21b0c2f010f63c04056d9fadd7763531bd9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804642"
---
# Come distribuire un'area di lavoro MED-V con un sistema di distribuzione elettronica del software


Un sistema di distribuzione elettronica del software è progettato per trasferire in modo efficiente il software a molti computer diversi tramite connessioni di rete lente o veloci. La sezione seguente contiene informazioni e istruzioni utili per distribuire l'area di lavoro MED-V in tutta l'organizzazione usando un sistema di distribuzione del software.

**Nota**  
Indipendentemente dalla soluzione di distribuzione del software che si usa, è necessario avere familiarità con i requisiti della soluzione specifica. Se si usa System Center Configuration Manager 2007 R2 o una versione successiva, vedere la [raccolta documenti di Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) nella raccolta tecnica Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .



**Importante**  
Se si usa System Center Configuration Manager 2007 SP2 e le aree di lavoro MED-V sono configurate per l'uso in modalità **NAT** , le macchine virtuali vengono classificate come client basati su Internet e non riescono a trovare i punti di distribuzione più vicini da cui scaricare il contenuto.

L' [hotfix per migliorare le funzionalità per le VM gestite da Med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) aggiunge nuove funzionalità alle macchine virtuali gestite da Med-v e configurate per l'uso in modalità **NAT** . La nuova funzionalità consente alle macchine virtuali di accedere ai punti di distribuzione più vicini. Di conseguenza, l'amministratore può gestire la macchina virtuale e il computer host nello stesso modo. Questo hotfix deve essere installato per primo nel server del sito e quindi nel client.

L'aggiornamento è pubblicamente disponibile. Tuttavia, potrebbe essere richiesto di accettare un contratto per i servizi Microsoft. Seguire le istruzioni sulle pagine Web successive per recuperare questo hotfix.



Puoi anche distribuire i componenti MED-V insieme usando un file batch, ma questo richiede un riavvio dopo l'installazione di Windows Virtual PC. Per ignorare questo requisito, è possibile specificare un singolo riavvio dopo l'installazione di tutti i componenti. Il riavvio singolo avvia anche automaticamente MED-V perché l'installazione dell'area di lavoro MED-V inserisce una voce in RUNKEY.

**Per distribuire un'area di lavoro MED-V usando un sistema di distribuzione del software**

1.  Definire un gruppo di computer e utenti nel sistema di distribuzione elettronica del software come set di destinazione di computer/utenti.

2.  Creare pacchetti per ogni file di installazione di Microsoft che deve essere distribuito. Di seguito sono riportati i file necessari e l'ordine in cui devono essere installati:

    1.  **Windows Virtual PC** -se non è già installato (è necessario riavviare il computer). Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

    2.  **Aggiunte e aggiornamenti di Windows Virtual PC** , se non sono già installati. Per altre informazioni, vedere [configurare i prerequisiti di installazione](configure-installation-prerequisites.md).

    3.  **File di installazione dell'agente host MED-v** : installa l'agente host (MED-v \ _HostAgent \ _setup file di installazione). Per altre informazioni, vedere [come installare manualmente l'agente host MED-V](how-to-manually-install-the-med-v-host-agent.md).

        **Warning**  
        Chiudere Internet Explorer prima di installare l'agente host MED-V, in caso contrario i conflitti possono verificarsi in seguito con il reindirizzamento degli URL. Questa operazione può essere eseguita anche specificando il riavvio del computer durante una distribuzione.



    4.  **Programma di installazione dell'area di lavoro MED-v, VHD e configurazione eseguibile** -creato nel **Packager area di lavoro MED-v**. Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).

        **Importante**  
        Il file del disco rigido virtuale compresso (con estensione MEDV) e il programma eseguibile di installazione (setup.exe) devono trovarsi nella stessa cartella della versione di installazione dell'area di lavoro MED-V. Installare quindi il programma di installazione dell'area di lavoro MED-V eseguendo setup.exe.



~~~
    **Tip**  
    Because problems can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



3. Configurare i pacchetti da eseguire in modalità silenziosa (non è necessaria alcuna interazione con l'utente).

   L'uso della modalità silenziosa Elimina il prompt per chiudere Internet Explorer se è in corso e il prompt per avviare l'agente host MED-V. Entrambe le azioni vengono eseguite quando il computer viene riavviato.

   **Nota**  
   L'installazione di Windows Virtual PC richiede di riavviare il computer. È possibile creare un singolo processo di installazione e installare tutti i componenti contemporaneamente se si elimina il riavvio e si ignorano i prerequisiti necessari per l'installazione di MED-V. Puoi eseguire questa operazione anche usando gli argomenti della riga di comando. Per un esempio di questi argomenti, vedere [come distribuire i componenti MED-V tramite un sistema di distribuzione elettronica del software](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md#bkmk-batch). MED-V viene avviato automaticamente all'avvio del computer.



4. Installare MED-V e i relativi componenti prima di installare Windows Virtual PC. Vedere il file batch di esempio più avanti in questo argomento.

   **Importante**  
   Selezionare l'opzione **Ignore \ _PREREQUISITES** come illustrato nel file batch di esempio in modo che i componenti MED-V possano essere installati prima dei componenti di VPC necessari. Installare i componenti MED-V in questo ordine per consentire il riavvio singolo.



5. Identificare eventuali altri requisiti necessari per l'installazione e per il sistema di distribuzione del software, ad esempio piattaforme di destinazione e spazio su disco gratuito.

6. Assegnare i pacchetti al set di destinazione di computer/utenti.

   Man mano che i computer sono in funzione, il client del sistema di distribuzione del software riconosce che sono disponibili nuovi pacchetti e inizia a installare i pacchetti per la definizione e i requisiti. Le installazioni devono essere eseguite in sequenza in modo silenzioso. È consigliabile eseguire questa operazione come singolo processo che non richiede un riavvio fino a quando non vengono installati tutti i pacchetti.

7. Una volta completate le installazioni, riavviare i computer aggiornati.

   A seconda del sistema di distribuzione del software, è possibile pianificare il riavvio del computer o gli utenti finali possono riavviare i computer manualmente durante il normale lavoro. Dopo il riavvio del computer, MED-V viene avviato automaticamente dopo l'accesso di un utente finale. Quando si avvia MED-V per la prima volta, viene eseguita la configurazione per la prima volta.

La prima volta che viene avviata la configurazione e potrebbero essere necessari alcuni minuti per terminare, a seconda delle dimensioni del disco rigido virtuale specificato e del numero di criteri applicati all'area di lavoro MED-V all'avvio. L'utente finale può tenere traccia dello stato di avanzamento guardando l'icona MED-V nell'area di notifica. Per altre informazioni sulla configurazione per la prima volta, vedere [Panoramica della distribuzione di MED-V 2,0](med-v-20-deployment-overview.md).

**Per installare l'area di lavoro MED-V usando un file batch**

1.  Eseguire l'installazione in un prompt dei comandi con credenziali amministrative.

2.  Distribuire ogni componente in una singola directory. Se viene eseguito da una condivisione di rete, è necessario un tempo più lungo per decomprimere il file con estensione MEDV.

3.  Come procedura consigliata, specificare che Windows Virtual PC e Windows Virtual PC hotfix vengono installati dopo l'agente host MED-V e i file del pacchetto dell'area di lavoro MED-V. Questo significa che Windows Update non causerà interferenze con il processo di installazione richiedendo un riavvio.

4.  Riavviare il computer dopo il completamento del file batch.

Dopo il riavvio, all'utente viene richiesto di eseguire la configurazione per la prima volta e completare la configurazione di MED-V.

L'esempio seguente, con gli argomenti specificati, Mostra come installare i componenti MED-V di 64 bit in un singolo processo:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Argomento</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/norestart</p></td>
<td align="left"><p>Impedisce l'installazione di Windows Virtual PC e dell'aggiornamento di Windows Virtual PC da riavviare il computer host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/quiet</p></td>
<td align="left"><p>Installa i componenti MED-V in modalità non interattiva senza interazione dell'utente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Qn</p></td>
<td align="left"><p>Installa i componenti MED-V senza un'interfaccia utente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>IGNORE_PREREQUISITES</p></td>
<td align="left"><p>Viene installata senza controllare Windows Virtual PC.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Specificare questo argomento solo se si sta installando Windows Virtual PC come parte di questa installazione.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>OVERWRITEVHD</p></td>
<td align="left"><p>Impone l'installazione dell'area di lavoro MED-V e impedisce eventuali richieste che potrebbero generare.</p></td>
</tr>
</tbody>
</table>



## Esempio


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## Argomenti correlati


[Panoramica della distribuzione di MED-V 2.0](med-v-20-deployment-overview.md)

[Come distribuire un'area di lavoro MED-V in un'immagine di Windows 7](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)









