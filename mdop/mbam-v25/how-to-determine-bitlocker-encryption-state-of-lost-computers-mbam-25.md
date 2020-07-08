---
title: Come determinare lo stato della crittografia BitLocker nei computer smarriti
description: Come determinare lo stato della crittografia BitLocker nei computer smarriti
author: dansimp
ms.assetid: 4f4bec1b-df3e-40ee-b431-291440268d64
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95fb843b230804417e375946814a585d1d681634
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824475"
---
# Come determinare lo stato della crittografia BitLocker nei computer smarriti


Usare questa procedura con il sito Web amministrazione e monitoraggio per determinare quanto segue:

-   Ultimo stato di crittografia noto di BitLocker per i computer persi o rubati

-   Se i volumi di un computer smarrito o rubato sono stati crittografati

Per completare questa attività, è necessario accedere all'area **report** del sito Web amministrazione e monitoraggio. Per accedere a questa area, è necessario che il ruolo utenti del report MBAM venga assegnato. Quando sono stati creati, è possibile che siano stati assegnati nomi diversi a questi ruoli. Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

**Nota**  La conformità del dispositivo è determinata dai criteri di BitLocker distribuiti dall'organizzazione. Potrebbe essere necessario verificare i criteri distribuiti prima di provare a determinare lo stato di crittografia di BitLocker di un dispositivo.

 

**Per determinare l'ultimo stato di crittografia noto di BitLocker per i computer persi**

1.  Aprire un Web browser e passare al **sito Web di amministrazione e monitoraggio**.

2.  Nel riquadro sinistro selezionare **report** per aprire la pagina report.

3.  Selezionare il **report conformità computer**.

4.  Usare i campi filtro nel riquadro destro per restringere i risultati della ricerca e quindi fare clic su **Cerca**. I risultati vengono visualizzati nella query di ricerca.

5.  Eseguire l'azione appropriata, come determinato dai criteri per i dispositivi persi.



## Argomenti correlati


[Gestione di BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





