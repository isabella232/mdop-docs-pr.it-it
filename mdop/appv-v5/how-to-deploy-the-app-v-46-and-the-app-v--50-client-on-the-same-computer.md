---
title: Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer
description: Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805535"
---
# Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer

**Nota:** App-V 4,6 è uscito dal supporto mainstream. Il seguente presuppone che il client App-V 4,6 SP3 sia già installato.

Usare le informazioni seguenti per installare il client App-V 5,0 (preferibilmente con i Service Pack più recenti e gli hotfix) e il client App-V 4.6 SP3 nello stesso computer. Per le versioni supportate, i requisiti e altre informazioni sulla pianificazione, vedere [pianificazione della migrazione da una versione precedente di App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**Per distribuire client App-V 5,0 e client App-V 4,6 nello stesso computer**

1.  Installare il client App-V 5,0 SP3 nel computer in cui è in esecuzione la versione App-V 4,6 del client. Per ottenere risultati ottimali, è consigliabile installare tutti gli aggiornamenti disponibili per il client App-V 5,0 SP3.

2.  Convertire o rieseguire la sequenza graduale dei pacchetti.

    -   Per convertire i pacchetti, usa il convertitore di pacchetti App-V 5,0 e Converti i pacchetti necessari nel formato di file App-V 5,0 (**. AppV**).

    -   Per risequenziare i pacchetti, è consigliabile usare la versione più recente del sequencer per ottenere risultati ottimali.

    Per altre informazioni sulla pubblicazione di pacchetti, vedere [come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-50.md).

3.  Distribuire pacchetti ai computer client.

4.  Convertire i punti di estensione, in base alle esigenze. Per altre informazioni, vedi le risorse seguenti:

    -   [Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Come convertire un pacchetto creato in una versione precedente di App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Verificare che i pacchetti dell'App-V 5,0 abbiano esito positivo e quindi rimuovere i pacchetti 4,6. Per controllare lo stato dell'utente dei computer client, è consigliabile usare la [virtualizzazione dell'esperienza utente](https://technet.microsoft.com/library/dn458947.aspx) o un altro strumento di gestione dell'ambiente utente.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Pianificazione per la migrazione da una versione precedente di App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Distribuzione di App-V 5.0 Sequencer e del client](deploying-the-app-v-50-sequencer-and-client.md)

 

 





