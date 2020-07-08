---
title: Come distribuire il client MBAM come parte di una distribuzione di Windows
description: Come distribuire il client MBAM come parte di una distribuzione di Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824915"
---
# Come distribuire il client MBAM come parte di una distribuzione di Windows


Il client di amministrazione e monitoraggio (MBAM) di Microsoft BitLocker consente agli amministratori di applicare e monitorare la crittografia unità BitLocker nei computer dell'organizzazione. Il client BitLocker può essere integrato in un'organizzazione abilitando la gestione e la crittografia di BitLocker nei computer client durante il processo di distribuzione di immagini e Windows.

**Nota**  
Per esaminare i requisiti di sistema client di MBAM, vedere [configurazioni supportate di mbam 1,0](mbam-10-supported-configurations.md).



La crittografia dei computer client con BitLocker durante la fase di imaging iniziale di una distribuzione di Windows può ridurre il sovraccarico amministrativo per l'implementazione di MBAM. Questo approccio assicura inoltre che tutti i computer distribuiti abbiano già eseguito BitLocker e siano configurati correttamente.

**Warning**  
Questo argomento descrive come modificare il registro di sistema di Windows usando l'editor del registro di sistema. Se il registro di sistema di Windows non viene modificato correttamente, è possibile che si verifichino seri problemi che potrebbero richiedere la reinstallazione di Windows. Prima di modificare il registro di sistema, è consigliabile creare una copia di backup dei file del registro di stato (System. dat e User. dat). Microsoft non può garantire che i problemi che possono verificarsi quando si modifica il registro di sistema possano essere risolti. Cambiare il registro di sistema a proprio rischio.



**Per crittografare un computer come parte della distribuzione di Windows**

1.  Se l'organizzazione prevede di usare le opzioni di protezione TPM (Trusted Platform Module) o TPM + PIN Protector in BitLocker, è necessario attivare il chip TPM prima della distribuzione iniziale di MBAM. Quando si attiva il chip TPM, si evita un riavvio più avanti nel processo e si assicura che i chip TPM siano configurati correttamente in base ai requisiti dell'organizzazione. È necessario attivare manualmente il chip TPM nel BIOS del computer. Per altre informazioni su come configurare il chip TPM, vedere la documentazione del produttore.

2.  Installare l'agente client MBAM.

3.  Ti consigliamo di aggiungere il computer a un dominio...

    -   Se il computer non è collegato a un dominio, la password di ripristino non viene archiviata nel servizio di ripristino di chiave MBAM. Per impostazione predefinita, MBAM non consente la crittografia a meno che non sia possibile archiviare la chiave di ripristino.

    -   Se un computer viene avviato in modalità di ripristino prima che la chiave di ripristino sia archiviata nel server MBAM, è necessario che il computer venga rielaborato. Non è disponibile alcun metodo di ripristino.

4.  Aprire un prompt dei comandi come amministratore, arrestare il servizio MBAM e quindi impostare il servizio su **manuale** o **su richiesta**. Esegui quindi i comandi seguenti:

    **NET STOP mbamagent**

    **sc config mbamagent start = demand**

5.  Impostare le impostazioni del registro di sistema per l'agente di MBAM per ignorare i criteri di gruppo ed eseguire il TPM per la **crittografia solo per i sistemi operativi** , eseguire **Regedit**e quindi importare il modello della chiave del registro di c:\\Programmi Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  In regedit, passa a HKLM\\SOFTWARE\\Microsoft\\MBAM e configura le impostazioni elencate nella tabella seguente.

    Voce del registro di sistema

    Impostazioni di configurazione

    DeploymentTime

    0 = DISATTIVATO

    1 = usare le impostazioni dei criteri per il tempo di distribuzione (impostazione predefinita)

    UseKeyRecoveryService

    0 = non usare l'escrow Key (le due voci del registro di sistema successive non sono necessarie in questo caso).

    1 = usare l'escrow Key nel sistema di recupero chiavi (impostazione predefinita)

    Consigliato: il computer deve essere in grado di comunicare con il servizio di recupero chiavi. Verificare che il computer sia in grado di comunicare con il servizio prima di procedere.

    KeyRecoveryOptions

    0 = solo chiave di ripristino upload

    1 = carica chiave di ripristino e pacchetto di recupero tasti (impostazione predefinita)

    KeyRecoveryServiceEndPoint

    Imposta questo valore sull'URL del server Web di ripristino della chiave.

    Esempio: http:// &lt; nome computer &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. L'agente MBAM riavvia il sistema durante la distribuzione del client MBAM. Quando si è pronti per il riavvio, eseguire il comando seguente al prompt dei comandi come amministratore:

   **NET Start mbamagent**

8. Quando il computer viene riavviato e il BIOS chiede di accettare una modifica del TPM, accettare la modifica.

9. Durante il processo di imaging del sistema operativo client Windows, quando si è pronti per avviare la crittografia, riavviare il servizio di MBAM Agent. Per impostare l'avvio **automatico**, aprire un prompt dei comandi come amministratore ed eseguire i comandi seguenti:

   **sc config mbamagent Start = automatico**

   **NET Start mbamagent**

10. Rimuovere i valori di bypass del registro di sistema. A tale scopo, eseguire regedit, passare alla voce del registro di sistema HKLM\\SOFTWARE\\Microsoft, fare clic con il pulsante destro del mouse sul nodo **mbam** e quindi scegliere **Elimina**.

## Argomenti correlati


[Distribuzione del client MBAM 1.0](deploying-the-mbam-10-client.md)









