---
title: Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo
description: Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 13cb83c4-bb42-4e81-8660-5b7540f473d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6ae5ba9c2346caf81f5aff9f57f6b9dc97127ad1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822516"
---
# Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo


Se si sostituisce il server Advanced Group Policy Management e il server in cui è ospitato l'archivio, è necessario trasferire il servizio Advanced Group Policy Management e l'archivio. Se si preferisce, è possibile trasferire il servizio Advanced Group Policy Management e l'archivio separatamente.

**Nota**  
-   Il server Advanced Group Policy Management è il computer che ospita il servizio Advanced Policy Management e il computer in cui è installato Microsoft Advanced Group Policy Management-Server.

-   Per impostazione predefinita, l'archivio è ospitato nel server Advanced Group Policy Management, ma è possibile specificare un percorso di archiviazione per ospitarlo in un altro server.

 

Per completare questa procedura è necessario un account utente che sia membro del gruppo Domain Admins e che abbia accesso ai nuovi server Advanced Group Policy Management. È inoltre necessario specificare le credenziali per l'account del servizio Advanced Group Policy Management che verrà usato dal nuovo server Advanced Group Policy Management per completare questa procedura.

**Per trasferire il servizio Advanced Group Policy Management e l'archivio in un server o server diverso**

1.  Eseguire il backup dell'archivio. Per altre informazioni, vedere [eseguire il backup dell'archivio](back-up-the-archive.md).

2.  Trasferire il servizio Advanced Group Policy Management:

    1.  Arrestare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm30ops.md).

    2.  Installare Microsoft Advanced Group Policy Management-Server nel nuovo server che ospiterà il servizio Advanced Group Policy Manager. Durante questo processo, devi specificare il nuovo percorso di archiviazione, la posizione dell'archivio in relazione al server Advanced Group Policy Management. Per altre informazioni, vedere Guida dettagliata per Microsoft Advanced Group Policy Management 3,0 ( <https://go.microsoft.com/fwlink/?LinkId=132706> ) e guida alla pianificazione per Microsoft Advanced Group Policy Management ( <https://go.microsoft.com/fwlink/?LinkId=141871> ).

    3.  Un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) deve configurare la connessione al server Advanced Group Policy Management per tutti gli amministratori dei criteri di gruppo che utilizzeranno il nuovo server Advanced Group Policy Management e rimuovere la connessione per il vecchio server Advanced Group Policy Management oppure ogni amministratore di criteri di gruppo deve configurare manualmente la nuova connessione al server Advanced Group Policy Management per lo snap-in del computer. Per altre informazioni, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm30ops.md).

        **Nota**  Come procedura consigliata, è consigliabile disinstallare Microsoft Advanced Group Policy Management-Server dal server Advanced Group Policy Management. In questo modo, il servizio Advanced Group Policy Management non può essere riavviato involontariamente sul server e potrebbe causare confusione se le connessioni del server Advanced Group Policy Management restano.

         

3.  Copiare l'archivio dal backup al nuovo server che ospiterà l'archivio. Per altre informazioni, vedere [ripristinare l'archivio da un backup](restore-the-archive-from-a-backup.md).

    **Importante**  Se l'archivio è stato spostato senza spostare contemporaneamente il servizio Advanced Group Policy Management:

    1.  È necessario modificare il percorso di archiviazione in base al nuovo percorso dell'archivio in relazione al server Advanced Group Policy Management. Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm30ops.md).

    2.  È necessario immettere di nuovo e confermare la password nella scheda **delega del dominio** . Per altre informazioni, vedere [configurare la notifica tramite posta elettronica](configure-e-mail-notification-agpm30ops.md).

     

### Riferimenti aggiuntivi

-   [Eseguire il backup dell'archivio](back-up-the-archive.md)

-   [Ripristinare l'archivio da un backup](restore-the-archive-from-a-backup.md)

-   [Configurare le connessioni server di Gestione avanzata Criteri di gruppo](configure-agpm-server-connections-agpm30ops.md)

-   [Modificare il servizio Gestione avanzata Criteri di gruppo](modify-the-agpm-service-agpm30ops.md)

-   Guida dettagliata per Microsoft Advanced Group Policy Management 3,0 ( <https://go.microsoft.com/fwlink/?LinkId=132706> )

-   Guida alla pianificazione per Microsoft Advanced Group Policy Management ( <https://go.microsoft.com/fwlink/?LinkId=141871> )

-   [Attività di amministrazione per Gestione avanzata Criteri di gruppo](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





