---
title: Come installare il client MED-V
description: Come installare il client MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827195"
---
# Come installare il client MED-V


In uno scenario basato su un pacchetto di distribuzione, l'installazione del client MED-V è inclusa nel pacchetto di distribuzione e viene installata direttamente dal pacchetto.

**Importante**  
Quando si usa un pacchetto di distribuzione che non include un'immagine, assicurarsi che l'immagine venga caricata sul Web o inserita nella cartella pre-stage prima di installare il pacchetto di distribuzione.



**Per installare un pacchetto di distribuzione**

1.  Effettua una delle seguenti operazioni:

    -   Scaricare il pacchetto MED-V dal Web.

    -   Inserire la distribuzione USB o DVD nell'unità host.

2.  Se MED-V non viene avviato automaticamente, fare doppio clic su MED-VAutoInstaller.exe.

    Verrà visualizzata una finestra di dialogo in cui sono elencati i componenti già installati e quelli attualmente installati.

    **Nota**  
    Se nel computer host è presente una versione di Microsoft Virtual PC che non è supportata, verrà visualizzato un messaggio che indica di disinstallare la versione esistente ed eseguire di nuovo il programma di installazione.



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. Se necessario, riavviare il computer.

   Al termine dell'installazione, viene avviato MED-V e viene visualizzato un messaggio che informa che l'installazione è stata completata.

4. Accedere a MED-V usando il nome utente e la password seguenti:

   -   Digitare il nome di dominio e il nome utente seguiti dalla password dell'utente di dominio autorizzato a usare MED-V.

       Esempio: "Domain \ _name \\user\ _name", "password"

## Argomenti correlati


[Come configurare un pacchetto di distribuzione](how-to-configure-a-deployment-package.md)

[Come caricare un'immagine MED-V nel server](how-to-upload-a-med-v-image-to-the-server.md)

[Riferimento della riga di comando dell'installazione client](client-installation-command-line-reference.md)









