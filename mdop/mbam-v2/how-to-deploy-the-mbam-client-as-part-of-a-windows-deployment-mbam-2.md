---
title: Come distribuire il client MBAM come parte di una distribuzione di Windows
description: Come distribuire il client MBAM come parte di una distribuzione di Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824625"
---
# Come distribuire il client MBAM come parte di una distribuzione di Windows


Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Se i computer con un chip TPM (Trusted Platform Module), il client BitLocker può essere integrato in un'organizzazione abilitando la gestione e la crittografia di BitLocker nei computer client come parte del processo di distribuzione di immagini e Windows.

**Nota**  
Per esaminare i requisiti di sistema per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [configurazioni supportate di MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



La crittografia dei computer client con BitLocker durante la fase di imaging iniziale di una distribuzione di Windows può ridurre il sovraccarico amministrativo necessario per l'implementazione di MBAM in un'organizzazione. Assicura inoltre che tutti i computer distribuiti abbiano già eseguito BitLocker e siano configurati correttamente.

**Nota**  
La procedura descritta in questo argomento descrive la modifica del registro di sistema di Windows. L'uso errato dell'editor del registro di sistema può causare seri problemi che potrebbero richiedere la reinstallazione di Windows. Microsoft non può garantire che i problemi causati dall'uso errato dell'editor del registro di sistema possano essere risolti. Usare l'editor del registro di sistema a proprio rischio.



**Per crittografare un computer come parte della distribuzione di Windows**

1.  Se l'organizzazione prevede di usare le opzioni di protezione TPM (Trusted Platform Module) o TPM + PIN Protector in BitLocker, è necessario attivare il chip TPM prima della distribuzione iniziale di MBAM. Quando si attiva il chip TPM, si evita un riavvio più avanti nel processo e si assicura che i chip TPM siano configurati correttamente in base ai requisiti dell'organizzazione. È necessario attivare manualmente il chip TPM nel BIOS del computer.

    **Nota**  
    Alcuni fornitori includono gli strumenti per attivare e attivare il chip TPM nel BIOS dall'interno del sistema operativo. Per altre informazioni su come configurare il chip TPM, vedere la documentazione del produttore.



2.  Installare l'agente client di amministrazione e monitoraggio di Microsoft BitLocker.

3.  Aggiungere il computer a un dominio (scelta consigliata).

    -   Se il computer non è collegato al dominio, la password di ripristino non viene archiviata nel servizio di ripristino di chiave di MBAM. Per impostazione predefinita, MBAM non consente la crittografia a meno che non sia possibile archiviare la chiave di ripristino.

    -   Se un computer viene avviato in modalità di ripristino prima che la chiave di ripristino sia archiviata nel server MBAM, è necessario che il computer venga rielaborato. Non è disponibile alcun metodo di ripristino.

4.  Eseguire il prompt dei comandi come amministratore, arrestare il servizio MBAM e quindi impostare il servizio su **manuale** o **su richiesta**e quindi iniziare digitando i comandi seguenti:

    **NET STOP mbamagent**

    **sc config mbamagent start = demand**

5.  Impostare le impostazioni del registro di sistema per l'agente MBAM per ignorare i criteri di gruppo ed eseguire il TPM solo per la **crittografia dei sistemi operativi** eseguendo **Regedit**e quindi importando il modello di chiave del registro di c:\\Programmi Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  In regedit, passa a HKLM\\SOFTWARE\\Microsoft\\MBAM e configura le impostazioni elencate nella tabella seguente.

    Voce del registro di sistema

    Impostazioni di configurazione

    DeploymentTime

    0 = DISATTIVATO

    1 = usare le impostazioni dei criteri per il tempo di distribuzione (impostazione predefinita)

    UseKeyRecoveryService

    0 = non usare l'escrow Key (le due voci del registro di sistema successive non sono necessarie in questo caso)

    1 = usare l'escrow Key nel sistema di recupero chiavi (impostazione predefinita)

    Consigliato: il computer deve essere in grado di comunicare con il servizio di recupero chiavi. Verificare che il computer sia in grado di comunicare con il servizio prima di procedere.

    KeyRecoveryOptions

    0 = carica solo il tasto di ripristino

    1 = carica il tasto di ripristino e il pacchetto di ripristino della chiave (impostazione predefinita)

    KeyRecoveryServiceEndPoint

    Imposta questo valore sull'URL per il server Web di ripristino chiave, ad esempio http:// &lt; nome computer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. L'agente MBAM riavvia il sistema durante la distribuzione del client MBAM. Quando si è pronti per il riavvio, eseguire il comando seguente al prompt dei comandi come amministratore:

   **NET Start mbamagent**

8. Quando il computer viene riavviato e il BIOS chiede di accettare una modifica del TPM, accettare la modifica.

9. Durante il processo di imaging del sistema operativo client Windows, quando si è pronti per avviare la crittografia, riavviare il servizio di MBAM Agent e impostare Start su **automatico** eseguendo un prompt dei comandi come amministratore e digitando i comandi seguenti:

   **sc config mbamagent Start = automatico**

   **NET Start mbamagent**

10. Rimuovere i valori di bypass del registro di sistema eseguendo regedit e passando alla voce del registro di sistema HKLM\\SOFTWARE\\Microsoft. Per eliminare il nodo **mbam** , fare clic con il pulsante destro del mouse sul nodo e scegliere **Elimina**.

## Argomenti correlati


[Distribuzione del client MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)









