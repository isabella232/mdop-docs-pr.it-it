---
title: Ripristinare l'archivio da un backup
description: Ripristinare l'archivio da un backup
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818365"
---
# Ripristinare l'archivio da un backup


Se si verifica un problema di emergenza e l'archivio per Advanced Group Policy Management è danneggiato o distrutto, un amministratore della gestione avanzata Criteri di gruppo (controllo completo) può ripristinare l'archivio da una copia di backup preparata in anticipo e quindi importare dall'ambiente di produzione eventuali oggetti Criteri di gruppo che non sono presenti nell'archivio o per i quali la versione in produzione è più aggiornata di quella dell'archivio. Per informazioni su come ripristinare un backup di archivio in un altro server, vedere [trasferire il server Advanced Group Policy Management e l'archivio](move-the-agpm-server-and-the-archive.md).

Per completare questa procedura è necessario un account utente che abbia accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management) e alla cartella che contiene l'archivio.

**Per ripristinare l'archivio da un backup**

1.  Arrestare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Rimuovere l'archivio esistente. Per impostazione predefinita, la cartella di archiviazione è%ProgramData%\\Microsoft\\AGPM, ma l'amministratore della gestione avanzata Criteri di gruppo che ha installato Microsoft Advanced Group Policy Management-Server potrebbe avere immesso una posizione diversa durante l'installazione.

3.  Creare nuovamente la cartella di archiviazione configurando il percorso di archiviazione, l'account del servizio Advanced Group Policy Management, il proprietario dell'archivio e la porta di ascolto. Non è necessario usare gli stessi valori usati durante l'installazione originale. Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm30ops.md).

4.  Copiare il contenuto del backup dell'archivio nella cartella di archiviazione, copiando le sottocartelle e i file per verificare che tutte le sottocartelle e i file ereditino le autorizzazioni della cartella di archiviazione. Prestare attenzione a non sovrascrivere la cartella di archiviazione.

5.  Se non si è certi che un GPO nel backup dell'archivio sia più attuale della copia di tale oggetto in produzione, generare un report di differenza e confrontarne le impostazioni. Per altre informazioni, vedere [identificare le differenze tra GPO, versioni GPO o modelli](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).

6.  Riavviare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm30ops.md).

### Riferimenti aggiuntivi

-   [Eseguire il backup dell'archivio](back-up-the-archive.md)

-   [Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo](move-the-agpm-server-and-the-archive.md)

-   [Gestione dell'archivio](managing-the-archive.md)

 

 





