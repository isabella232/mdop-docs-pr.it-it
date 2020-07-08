---
title: Come pubblicare un pacchetto tramite la console di gestione
description: Come pubblicare un pacchetto tramite la console di gestione
author: dansimp
ms.assetid: 7c6930fc-5c89-4519-a901-512dae155fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 832dd95edbb0f4cd6b6ae242a81859141ebcb279
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805236"
---
# Come pubblicare un pacchetto tramite la console di gestione


Usare la procedura seguente per pubblicare un pacchetto App-V 5,0. Dopo aver pubblicato un pacchetto, i computer che eseguono il client App-V 5,0 possono accedere ed eseguire le applicazioni in tale pacchetto.

**Nota**  La possibilità di abilitare solo gli amministratori per la pubblicazione o l'annullamento della pubblicazione di pacchetti (descritti di seguito) è supportata a partire da App-V 5,0 SP3.

 

**Per pubblicare un pacchetto di App-V 5,0**

1.  Nella console di gestione di App-V 5,0. fare clic con il pulsante destro del mouse sul nome del pacchetto da pubblicare e scegliere **pubblica**.

2.  Esaminare la colonna **stato** per verificare che il pacchetto sia stato pubblicato ed è ora disponibile. Se il pacchetto è disponibile, viene visualizzato lo stato **pubblicato** .

    Se il pacchetto non viene pubblicato correttamente, viene visualizzato lo stato non **pubblicato** , insieme al testo dell'errore che spiega perché il pacchetto non è disponibile.

**Per consentire solo agli amministratori di pubblicare o annullare la pubblicazione di pacchetti**

1.  Passare al nodo oggetto Criteri di gruppo seguente:

    **Configurazione &gt; computer Criteri &gt; amministrativi modelli &gt; &gt; di sistema App-V &gt; Publishing**.

2.  Abilitare l'impostazione Richiedi i criteri **di gruppo pubblica come amministratore** .

    Per usare in alternativa PowerShell per impostare questo elemento, vedere [come gestire i pacchetti App-V 5,0 in uso in un computer autonomo usando PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs).

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

[Come configurare l'accesso ai pacchetti tramite la console di gestione](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

 

 





