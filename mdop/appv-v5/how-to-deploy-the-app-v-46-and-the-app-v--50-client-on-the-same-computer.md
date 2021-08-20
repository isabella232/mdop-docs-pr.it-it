---
title: Come distribuire App-V 4.6 e il client App-V 5.0 nello stesso computer
description: Come distribuire App-V 4.6 e il client App-V 5.0 nello stesso computer
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.prod: w10
ms.openlocfilehash: f10f3d159c4724f3b486215b1169825bb029316d
ms.sourcegitcommit: 0132cd232b9c030820d95d91b71c4def0184400a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "11907229"
---
# <a name="how-to-deploy-the-app-v-46-and-the-app-v-50-client-on-the-same-computer"></a>Come distribuire App-V 4.6 e il client App-V 5.0 nello stesso computer

**Nota:** App-V 4.6 ha terminato il supporto Mainstream. L'esempio seguente presuppone che il client App-V 4.6 SP3 sia già installato.

Utilizzare le informazioni seguenti per installare il client App-V 5.0 (preferibilmente con i Service Pack e gli hotfix più recenti) e il client App-V 4.6 SP3 nello stesso computer. Per le versioni supportate, i requisiti e altre informazioni sulla pianificazione, vedere [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**Per distribuire il client App-V 5.0 e il client App-V 4.6 nello stesso computer**

1.  Installare il client App-V 5.0 SP3 nel computer che esegue la versione App-V 4.6 del client. Per ottenere risultati ottimali, è consigliabile installare tutti gli aggiornamenti disponibili nel client App-V 5.0 SP3.

2.  Convertire o ri-sequenziare gradualmente i pacchetti.

    -   Per convertire i pacchetti, usa il convertitore di pacchetti App-V 5.0 e converti i pacchetti necessari nel formato di file App-V 5.0 (**appv).**

    -   Per ri-sequenziare i pacchetti, valuta la possibilità di usare la versione più recente di Sequencer per ottenere risultati ottimali.

    Per ulteriori informazioni sulla pubblicazione di pacchetti, vedere [Come pubblicare un pacchetto tramite la console di gestione.](how-to-publish-a-package-by-using-the-management-console-50.md)

3.  Distribuire pacchetti nei computer client.

4.  Convertire i punti di estensione, in base alle esigenze. Per ulteriori informazioni, vedere le risorse seguenti:

    -   [Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Come convertire un pacchetto creato in una versione precedente di App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Verifica che i pacchetti App-V 5.0 siano stati evasi correttamente e quindi rimuovi i pacchetti 4.6. Per controllare lo stato utente dei computer client, è consigliabile utilizzare [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) o un altro strumento di gestione dell'ambiente utente.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema di App-V?** Usare il [Forum TechNet di App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## <a name="related-topics"></a>Argomenti correlati


[Pianificazione per la migrazione da una versione precedente di App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Distribuzione di App-V 5.0 Sequencer e del client](deploying-the-app-v-50-sequencer-and-client.md)

 

 





