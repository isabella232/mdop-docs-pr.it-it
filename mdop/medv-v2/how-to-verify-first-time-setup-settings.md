---
title: Come verificare le impostazioni della prima configurazione
description: Come verificare le impostazioni della prima configurazione
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804666"
---
# Come verificare le impostazioni della prima configurazione


Durante l'esecuzione del test di configurazione per la prima volta o dopo il completamento, è possibile verificare le impostazioni configurate nell'area di lavoro MED-V eseguendo le attività seguenti.

**Nota**  Per informazioni su come monitorare il completamento della configurazione per la prima volta in tutta l'organizzazione dopo la distribuzione, vedere [monitoraggio delle distribuzioni dell'area di lavoro MED-V](monitoring-med-v-workspace-deployments.md).

 

**Per verificare le impostazioni durante la configurazione per la prima volta**

1.  Durante l'esecuzione della configurazione per la prima volta, verificare quanto segue:

    Se è stata specificata la modalità **automatica** , verificare che la macchina virtuale non venga visualizzata quando viene eseguita la configurazione per la prima volta.

    Se è stata specificata la modalità assistita, verificare che la macchina virtuale venga visualizzata e che siano visualizzati tutti i campi che richiedono l'input dell'utente.

2.  È anche possibile monitorare la procedura di configurazione completa per la prima volta visualizzando la macchina virtuale quando è in esecuzione la configurazione per la prima volta. A tale scopo, effettua quanto segue:

    1.  Aprire la console PC virtuale Windows.

        Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**e quindi fare clic su **Virtual PC Windows**.

    2.  Avviare MED-V se non è già in uso.

        Se non è già presente, in breve tempo viene visualizzata una macchina virtuale con il nome dell'area di lavoro MED-V distribuita nell'elenco delle macchine virtuali.

    3.  Fare doppio clic sulla macchina virtuale MED-V per aprirla.

        È possibile osservare la macchina virtuale MED-V quando è in fase di configurazione ed è possibile risolvere i problemi della procedura di configurazione minima. Verificare le informazioni nelle diverse schermate, ad esempio la configurazione delle impostazioni di rete, le informazioni di join del dominio del computer, la configurazione dell'agente guest, l'impostazione delle impostazioni personali e l'arresto.

    4.  La macchina virtuale si chiude automaticamente al termine della configurazione per la prima volta.

        **Nota**  È possibile chiudere la finestra della macchina virtuale in qualsiasi momento e la configurazione della prima volta continua.

         

**Per verificare le impostazioni al termine della configurazione per la prima volta**

1.  Verificare che la configurazione per la prima volta sia stata completata correttamente.

2.  Verificare che l'area di lavoro MED-V sia configurata correttamente.

    1.  Aprire la console PC virtuale Windows.

        Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Windows Virtual PC**e quindi fare clic su **Virtual PC Windows**.

    2.  Fare doppio clic sull'area di lavoro MED-V installata.

        Se l'area di lavoro MED-V è già in uso, potrebbe essere richiesto di chiudere l'applicazione prima di poter aprire la macchina virtuale.

    3.  Nell'area di lavoro MED-V fare clic con il pulsante destro del mouse su **risorse del computer**e quindi scegliere **Proprietà**.

    4.  Verificare che l'area di lavoro MED-V sia stata aggiunta al dominio corretto. Se applicabile per l'organizzazione, provare a partecipare al dominio specificando due diversi domini per verificare che il dominio guest venga sottoposto a override dal dominio host.

    5.  Verificare che l'area di lavoro MED-V sia stata aggiunta all'unità organizzativa del dominio specificata.

    6.  Se è stata specificata la maschera nome computer, verificare che il nome del nuovo computer corrisponda a quello specificato.

3.  Verificare che le impostazioni locali specificate siano corrette.

    1.  Nell'area di lavoro MED-V fare clic su **Start** e quindi su **Pannello di controllo**.

    2.  Verificare le impostazioni di configurazione specificate, ad esempio **data e ora** , **internazionali e della lingua**.

**Nota**  In caso di problemi durante la verifica delle impostazioni di configurazione per la prima volta, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).

 

Dopo avere verificato che le impostazioni di configurazione per la prima volta sono corrette, è possibile verificare altre configurazioni dell'area di lavoro MED-V per verificarne il funzionamento, ad esempio la pubblicazione di applicazioni e il reindirizzamento degli URL.

Dopo aver completato tutti i test del pacchetto dell'area di lavoro MED-V e aver verificato che funzioni come previsto, è possibile distribuire l'area di lavoro MED-V alla propria organizzazione.

## Argomenti correlati


[Come verificare la pubblicazione delle applicazioni](how-to-test-application-publishing.md)

[Come verificare il reindirizzamento URL](how-to-test-url-redirection.md)

[Distribuzione del pacchetto nell'area di lavoro MED-V](deploying-the-med-v-workspace-package.md)

[Gestire le impostazioni dell'area di lavoro MED-V](manage-med-v-workspace-settings.md)

 

 





