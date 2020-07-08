---
title: Come rimuovere un pacchetto con la riga di comando
description: Come rimuovere un pacchetto con la riga di comando
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816825"
---
# Come rimuovere un pacchetto con la riga di comando


È possibile usare le procedure della riga di comando seguenti per eliminare un pacchetto di applicazione virtuale dal client Application Virtualization (App-V) in un computer specifico.

**Per eliminare un pacchetto di applicazione virtuale per tutti gli utenti**

-   Se il pacchetto è stato aggiunto in precedenza per tutti gli utenti usando l'opzione/GLOBAL, usare il comando seguente per eliminare il pacchetto e i tipi di file e i tasti di scelta rapida globali. Sono necessari i diritti di amministratore. L'opzione/GLOBAL non è necessaria in questo caso perché il comando esegue sempre un'eliminazione globale del pacchetto.

    `SFTMIME DELETE PACKAGE:”name”`

**Per eliminare un pacchetto aggiunto in precedenza per singoli utenti**

1.  Se il pacchetto è stato aggiunto in precedenza per singoli utenti, sono disponibili diverse opzioni.

    Eseguire il comando seguente una volta sotto l'account utente di ogni persona a cui è stato pubblicato il pacchetto. In questo caso l'accesso dell'utente alle applicazioni viene negato se si spostano in un altro computer. Elimina le impostazioni, i collegamenti e i tipi di file specifici dell'utente dal profilo e arresta i carichi in background nel contesto dell'utente.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  In alternativa, eseguire il comando seguente sotto l'account utente di ogni persona a cui è stato pubblicato il pacchetto.

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    Esegui quindi questo comando per il pacchetto.

    `SFTMIME DELETE PACKAGE:”name”`

    Questo rimuove completamente il pacchetto e Elimina tutte le impostazioni utente, i tasti di scelta rapida e i tipi di file dai relativi profili. Se il pacchetto viene successivamente aggiunto nuovamente, gli utenti dovranno specificare di nuovo le relative impostazioni. Per eseguire questo comando è necessaria solo l'autorizzazione "Elimina applicazioni" (**Deleteapp**).

3.  Come terza alternativa, è possibile eseguire semplicemente il comando **Elimina pacchetto** senza usare il comando Annulla **pubblicazione pacchetto** . In questo caso, i tipi di file e i tasti di scelta rapida per ogni utente sono nascosti anziché eliminati e le impostazioni utente vengono mantenute. Questo significa che se il pacchetto viene successivamente aggiunto di nuovo per l'utente, i tipi di file e i collegamenti vengono ripristinati e le impostazioni utente vengono riapplicate.

## Argomenti correlati


[Come aggiungere un pacchetto con la riga di comando](how-to-add-a-package-by-using-the-command-line.md)

[Come eliminare tutte le applicazioni virtuali usando la riga di comando](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





