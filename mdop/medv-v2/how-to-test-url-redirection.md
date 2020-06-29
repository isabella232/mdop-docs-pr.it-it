---
title: Come verificare il reindirizzamento URL
description: Come verificare il reindirizzamento URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824446"
---
# Come verificare il reindirizzamento URL


Dopo l'esecuzione del test della configurazione prima volta, è possibile verificare che la funzionalità di reindirizzamento degli URL funzioni come previsto eseguendo le attività seguenti.

**Importante**  L'agente host MED-V deve essere in funzione in modo che il reindirizzamento degli URL funzioni correttamente.

<a href="" id="bkmk-urlredir"></a>**Per testare il reindirizzamento degli URL**

1.  Aprire un browser Internet Explorer nel computer host e immettere un URL specificato per il reindirizzamento.

2.  Verificare che la pagina Web sia aperta in Internet Explorer nella macchina virtuale guest.

3.  Ripetere questa procedura per ogni URL che si vuole testare.

**Per verificare che sia possibile aggiungere o rimuovere un URL**

1.  Aggiungere o rimuovere un URL dall'area di lavoro MED-V.

    Per informazioni su come aggiungere e rimuovere URL per il reindirizzamento in un'area di lavoro MED-V, vedere [gestire il reindirizzamento degli URL di Med-v](manage-med-v-url-redirection.md).

2.  Se è stato aggiunto un URL all'elenco di reindirizzamento, ripetere i passaggi [per testare il reindirizzamento degli URL](#bkmk-urlredir) per verificare che il nuovo URL venga reindirizzato come previsto.

3.  Se è stato rimosso un URL dall'elenco di reindirizzamento, verificare che venga rimosso eseguendo la procedura seguente:

    1.  Aprire un browser Internet Explorer nel computer host e immettere l'URL rimosso dall'elenco di reindirizzamento.

    2.  Verificare che la pagina Web sia aperta in Internet Explorer nel computer host anziché nella macchina virtuale guest.

        **Nota**  Può essere necessario attendere alcuni secondi prima che le modifiche al reindirizzamento degli URL avvengano.

**Nota**  In caso di problemi durante la verifica delle impostazioni di reindirizzamento degli URL, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).

Dopo aver completato i test di reindirizzamento degli URL nell'area di lavoro MED-V, è possibile testare altre configurazioni per verificare che funzionino come previsto.

Dopo aver completato il test del pacchetto dell'area di lavoro MED-V e aver verificato che funzioni come previsto, è possibile distribuire l'area di lavoro MED-V alla propria organizzazione.

## Argomenti correlati

[Come verificare la pubblicazione delle applicazioni](how-to-test-application-publishing.md)

[Come verificare le impostazioni della prima configurazione](how-to-verify-first-time-setup-settings.md)

[Distribuzione del pacchetto nell'area di lavoro MED-V](deploying-the-med-v-workspace-package.md)

 

 





