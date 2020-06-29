---
title: Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer
description: Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805529"
---
# Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer

**Nota:** App-V 4,6 è uscito dal supporto mainstream.

Usare le informazioni seguenti per installare il client di Microsoft Application Virtualization (App-V) 5,1 (preferibilmente con i Service Pack più recenti e gli hotfix) e il client App-V 4.6 SP2 o il client App-V 4.6 S3 nello stesso computer. Per le versioni supportate, i requisiti e altre informazioni sulla pianificazione, vedere [pianificazione della migrazione da una versione precedente di App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).

**Per distribuire client App-V 5,1 e client App-V 4,6 nello stesso computer**

1.  Installare la versione seguente del client App-V nel computer in cui è in esecuzione App-V 4,6.

    -   [Microsoft Application Virtualization 4,6 Service Pack 3](https://www.microsoft.com/download/details.aspx?id=41187)

2.  Installare il client App-V 5,1 nel computer in cui è in esecuzione la versione App-V 4,6 SP3 del client. Per ottenere risultati ottimali, è consigliabile installare tutti gli aggiornamenti disponibili per il client App-V 5,1.

3.  Convertire o rieseguire la sequenza graduale dei pacchetti.

    -   Per convertire i pacchetti, usa il convertitore di pacchetti App-V 5,1 e Converti i pacchetti necessari nel formato di file App-V 5,1 (**. AppV**).

    -   Per risequenziare i pacchetti, è consigliabile usare la versione più recente del sequencer per ottenere risultati ottimali.

    Per altre informazioni sulla pubblicazione di pacchetti, vedere [come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-51.md).

4.  Distribuire pacchetti ai computer client.

5.  Convertire i punti di estensione, in base alle esigenze. Per altre informazioni, vedi le risorse seguenti:

    -   [Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.1 convertito per tutti gli utenti in un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.1 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [Come convertire un pacchetto creato in una versione precedente di App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  Verificare che i pacchetti dell'App-V 5,1 abbiano esito positivo e quindi rimuovere i pacchetti 4,6. Per controllare lo stato dell'utente dei computer client, è consigliabile usare la [virtualizzazione dell'esperienza utente](https://technet.microsoft.com/library/dn458947.aspx) o un altro strumento di gestione dell'ambiente utente.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Pianificazione per la migrazione da una versione precedente di App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[Distribuzione di App-V 5.1 Sequencer e del client](deploying-the-app-v-51-sequencer-and-client.md)

 

 





