---
title: Come verificare la pubblicazione delle applicazioni
description: Come verificare la pubblicazione delle applicazioni
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826915"
---
# Come verificare la pubblicazione delle applicazioni


Dopo la fine del test di configurazione per la prima volta, è possibile verificare che la funzionalità di pubblicazione dell'applicazione funzioni come previsto eseguendo le attività seguenti.

<a href="" id="bkmk-apppub"></a>**Per testare la pubblicazione delle applicazioni**

1.  Verificare che le applicazioni specificate per la pubblicazione siano visibili.

    Fare clic sul pulsante **Start** e quindi scegliere **tutti i programmi** e cercare le applicazioni specificate.

    In alcuni casi è possibile che la stessa applicazione sia installata due volte, una sola volta nel computer host e una sola volta nel guest. Se un'applicazione pubblicata con lo stesso nome viene pubblicata nella stessa posizione nel menu **Start** dell'host, si distingue dal collegamento all'applicazione host aggiungendo il nome della macchina virtuale al nome del collegamento. Ad esempio, per una macchina virtuale denominata "MEDVHost1", un'applicazione host potrebbe essere "Notepad" e un'applicazione pubblicata potrebbe essere "Notepad (MEDVHost1)".

2.  Verificare che le applicazioni funzionino come previsto.

    Nel computer host avviare le applicazioni pubblicate e verificare che vengano aperte in Windows XP SP3 per l'ospite. L'applicazione deve essere visualizzata in una finestra in stile Windows XP nel desktop del computer host.

3.  Se applicabile, verificare che il reindirizzamento dei documenti funzioni come previsto.

    Se un'applicazione pubblicata per l'ospite deve aprire una cartella nell'unità host System, verificare che sia possibile aprire la cartella specificata.

    **Importante**  Dato che Windows Virtual PC non supporta la creazione di una condivisione da una cartella già condivisa, il reindirizzamento non si verifica per i documenti che si aprono da una cartella condivisa, ad esempio una cartella documenti che si trova nella rete. Per altre informazioni, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).

Dopo avere verificato che le applicazioni pubblicate sono installate e funzionanti correttamente, è possibile verificare se le applicazioni possono essere aggiunte o rimosse dall'area di lavoro MED-V.

**Per verificare che un'applicazione possa essere aggiunta o rimossa**

1.  Aggiungere o rimuovere un'applicazione dall'area di lavoro MED-V.

    Per informazioni su come aggiungere e rimuovere applicazioni da un'area di lavoro MED-V, vedere [gestione delle applicazioni distribuite nelle aree di lavoro MED-v](managing-applications-deployed-to-med-v-workspaces.md).

2.  Se è stata aggiunta un'applicazione, ripetere i passaggi [per testare la pubblicazione dell'applicazione](#bkmk-apppub) per verificare che la nuova applicazione funzioni come previsto.

3.  Se è stata rimossa un'applicazione, fare clic su **Start** e quindi su **tutti i programmi** e verificare che le applicazioni rimosse non siano più elencate.

**Nota**  In caso di problemi durante la verifica delle impostazioni di pubblicazione delle applicazioni, vedere [risoluzione dei problemi relativi alle operazioni](operations-troubleshooting-medv2.md).

Dopo aver completato il test di pubblicazione delle applicazioni, è possibile testare altre configurazioni dell'area di lavoro MED-V per verificare che funzionino come previsto.

Dopo aver completato il test del pacchetto dell'area di lavoro MED-V e aver verificato che funzioni come previsto, è possibile distribuire l'area di lavoro MED-V alla propria organizzazione.

## Argomenti correlati

[Come verificare il reindirizzamento URL](how-to-test-url-redirection.md)

[Come verificare le impostazioni della prima configurazione](how-to-verify-first-time-setup-settings.md)

[Distribuzione del pacchetto nell'area di lavoro MED-V](deploying-the-med-v-workspace-package.md)

 

 





