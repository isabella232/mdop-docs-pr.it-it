---
title: Come gestire la compatibilità hardware
description: Come gestire la compatibilità hardware
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804636"
---
# Come gestire la compatibilità hardware


Microsoft BitLocker Administration and Monitoring (MBAM) può raccogliere informazioni sul produttore e sul modello di computer client dopo la distribuzione dei criteri di gruppo Verifica compatibilità hardware. Se si configura questo criterio, l'agente di MBAM riporta il computer e le informazioni sul modello al server MBAM quando il client MBAM viene distribuito in un computer client.

La funzionalità compatibilità hardware è utile quando l'organizzazione ha hardware o computer meno recenti che non supportano i chip TPM (Trusted Platform Module). In questi casi, è possibile usare la caratteristica compatibilità hardware per verificare che la crittografia BitLocker venga applicata solo ai modelli di computer che la supportano. Se tutti i computer dell'organizzazione supportano BitLocker, non è necessario usare la funzionalità compatibilità hardware.

**Nota**  Per impostazione predefinita, la caratteristica compatibilità hardware di MBAM non è abilitata. Per abilitarlo, selezionare la caratteristica **compatibilità hardware** sotto la caratteristica di **amministrazione e monitoraggio del server** durante l'installazione. Per altre informazioni su come impostare e configurare la compatibilità hardware, vedere [distribuzione dell'infrastruttura del server MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).

 

La funzionalità compatibilità hardware funziona nel modo seguente.

****

1.  L'agente client MBAM individua le informazioni di base sul computer, come produttore, modello, BIOS Maker, versione del BIOS, creatore TPM e versione TPM, quindi passa queste informazioni al server MBAM.

2.  Il server MBAM genera un elenco di modelli di computer client che consente di distinguere tra quelli che possono o non possono supportare BitLocker

3.  Gli agenti client MBAM distribuiti nell'organizzazione aggiornano automaticamente questo elenco con tutte le nuove funzionalità e i modelli di computer individuati con uno stato **sconosciuto**. Un amministratore può quindi usare il sito Web di amministrazione di MBAM per modificare le voci di elenco in modo da specificare un determinato tipo di computer e modello come **compatibile** o **incompatibile**.

4.  Prima che l'agente client MBAM inizi a crittografare un'unità, l'agente verifica prima di tutto la compatibilità con crittografia BitLocker dell'hardware in cui è in esecuzione.

    -   Se l'hardware è contrassegnato come compatibile, viene avviato il processo di crittografia BitLocker. MBAM riverificherà anche lo stato di compatibilità hardware del computer una volta al giorno.

    -   Se l'hardware è contrassegnato come non compatibile, l'agente registra un evento e passa uno stato "esonerato dall'hardware" come parte del report di conformità. L'agente controlla ogni sette giorni per verificare se lo stato è stato modificato in "compatibile".

    -   Se l'hardware è contrassegnato come sconosciuto, il processo di crittografia di BitLocker non inizierà. L'agente client MBAM verificherà nuovamente lo stato di compatibilità hardware del computer una volta al giorno.

**Avviso**  Se l'agente client MBAM prova a crittografare un computer che non supporta la crittografia unità BitLocker, è possibile che il computer venga danneggiato. Verificare che la funzionalità compatibilità hardware sia configurata correttamente quando l'organizzazione ha un hardware meno recente che non supporta BitLocker.

 

**Per gestire la compatibilità hardware**

1.  Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio di Microsoft BitLocker. Selezionare **hardware** nella barra dei menu a sinistra.

2.  Nel riquadro destro fare clic su **ricerca avanzata**e quindi filtrare per visualizzare un elenco di tutti i modelli di computer con uno **Capability** stato di funzionalità **sconosciuto**. Viene visualizzato un elenco di modelli di computer corrispondenti ai criteri di ricerca. Gli amministratori possono aggiungere, modificare o rimuovere nuovi tipi di computer da questa pagina.

3.  Esaminare ogni configurazione hardware sconosciuta per determinare se la configurazione deve essere impostata su **compatibile** o non **compatibile**.

4.  Selezionare una o più righe e quindi fare clic su **imposta compatibile** o **imposta non compatibile** per impostare la compatibilità di BitLocker, in base alle esigenze, per i modelli di computer selezionati. Se impostato su **compatible**, BitLocker cerca di applicare i criteri di crittografia unità nei computer che corrispondono al modello supportato. Se impostato su non **compatibile**, BitLocker non applica i criteri di crittografia unità in tali computer.

    **Nota**  Dopo aver impostato un modello di computer come compatibile, possono essere necessarie più di ventiquattro ore perché il client MBAM inizi la crittografia BitLocker nei computer che corrispondono al modello hardware.

     

5.  Gli amministratori dovrebbero monitorare regolarmente l'elenco compatibilità hardware per esaminare i nuovi modelli scoperti dall'agente MBAM e quindi aggiornare l'impostazione di compatibilità in modo che sia **compatibile** o non **compatibile** .

## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 1.0](administering-mbam-10-features.md)

 

 





