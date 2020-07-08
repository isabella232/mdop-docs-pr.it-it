---
title: Eseguire il backup dell'archivio
description: Eseguire il backup dell'archivio
author: dansimp
ms.assetid: 400176da-3518-4475-ad19-c96cda6ca7ba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a75099e7a6624850ee0511cf65feddf63909a0c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819206"
---
# Eseguire il backup dell'archivio


Per agevolare il ripristino dell'archivio per Advanced Group Policy Management (gestione avanzata Criteri di gruppo) in caso di emergenza, un amministratore della Advanced Group Policy (controllo completo) deve eseguire il backup dell'archivio di frequente. Per impostazione predefinita, l'archivio viene creato in%ProgramData%\\Microsoft\\AGPM. Tuttavia, è possibile specificare un percorso diverso durante la configurazione di Microsoft Advanced Group Policy Management-Server.

Un account utente che ha accesso sia al server Advanced Group Policy Management, il computer in cui è installato il servizio Advanced Group Policy Management, sia alla cartella che contiene l'archivio è necessario per completare questa procedura.

**Per eseguire il backup dell'archivio**

1.  Arrestare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Eseguire il backup della cartella di archiviazione usando Esplora risorse, xcopy, Windows Server® backup o un altro strumento di backup. Assicurarsi di eseguire il backup dei file nascosti, di sistema e di sola lettura.

3.  Archiviare il backup dell'archivio in una posizione sicura.

4.  Riavviare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm30ops.md).

**Nota**  Se un amministratore Advanced Group Policy Management fa eseguire il backup dell'archivio in modo non frequente, gli oggetti Criteri di gruppo nel backup dell'archivio non saranno correnti. Per fare in modo che il backup dell'archivio sia aggiornato, eseguire il backup dell'archivio nell'ambito della strategia di backup giornaliera dell'organizzazione.

 

### Riferimenti aggiuntivi

-   [Ripristinare l'archivio da un backup](restore-the-archive-from-a-backup.md)

-   [Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo](move-the-agpm-server-and-the-archive.md)

-   [Gestione dell'archivio](managing-the-archive.md)

 

 





