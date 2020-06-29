---
title: Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1
description: Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1
author: dansimp
ms.assetid: f5ab426a-f49a-47b3-93f3-b9d60aada8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 282207b5424442950e88c40a372194e9def768cb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805643"
---
# Come creare un file di configurazione personalizzato usando la console di gestione di App-V 5.1


Puoi usare una configurazione dinamica per personalizzare un pacchetto di App-V 5,1 per un utente specifico. È tuttavia necessario prima di tutto creare il file di configurazione dinamica degli utenti o il file di configurazione della distribuzione dinamica prima di poter usare i file. La creazione del file è un'operazione manuale avanzata. Per informazioni generali sui file di configurazione dinamica degli utenti, vedere informazioni [sulla configurazione dinamica di App-V 5,1](about-app-v-51-dynamic-configuration.md).

Usare la procedura seguente per creare un file di configurazione utente dinamico usando la console di gestione di App-V 5,1.

**Per creare un file di configurazione utente dinamico**

1.  Fare clic con il pulsante destro del mouse sul nome del pacchetto che si desidera visualizzare e selezionare **modifica accesso Active Directory** per visualizzare la configurazione assegnata a un gruppo di utenti specificato. In alternativa, selezionare il pacchetto e fare clic su **modifica**.

2.  Usando l'elenco delle **entità pubblicitarie con Access**, selezionare il gruppo di annunci che si vuole personalizzare. Selezionare **personalizzato** nell'elenco a discesa, se non è già selezionato. Verrà visualizzato un collegamento denominato **modifica** .

3.  Fai clic su **Modifica**. Verrà visualizzata la configurazione utente dinamica assegnata al gruppo di annunci.

4.  Fare clic su **Avanzate**e quindi su **Esporta configurazione**. Digitare un nome di file e fare clic su **Salva**. A questo punto è possibile modificare il file per configurare un pacchetto per un utente.

    **Nota**  
    Per esportare una configurazione durante l'esecuzione in Windows Server, è necessario disabilitare "configurazione di sicurezza avanzata di IE". Se questa funzionalità è abilitata e impostata su blocca download, non è possibile scaricare nulla dal server App-V.



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)









