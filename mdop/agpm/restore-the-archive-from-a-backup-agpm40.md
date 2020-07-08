---
title: Ripristinare l'archivio da un backup
description: Ripristinare l'archivio da un backup
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818396"
---
# Ripristinare l'archivio da un backup


Se si verifica un problema di emergenza e l'archivio per Advanced Group Policy Management è danneggiato o distrutto, un amministratore della gestione avanzata Criteri di gruppo (controllo completo) può ripristinare l'archivio da una copia di backup preparata in anticipo e quindi importare dall'ambiente di produzione del dominio eventuali oggetti Criteri di gruppo che non sono presenti nell'archivio o per i quali la versione in produzione è più aggiornata di quella dell'archivio Per informazioni su come ripristinare un backup di archivio in un altro server, vedere [trasferire il server Advanced Group Policy Management e l'archivio](move-the-agpm-server-and-the-archive-agpm40.md).

Per completare questa procedura è necessario un account utente che abbia accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management) e alla cartella che contiene l'archivio.

**Per ripristinare l'archivio da un backup**

1.  Arrestare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).

2.  Rimuovere l'archivio esistente. Per impostazione predefinita, la cartella di archiviazione è%ProgramData%\\Microsoft\\AGPM, ma l'amministratore della gestione avanzata Criteri di gruppo che ha installato Microsoft Advanced Group Policy Management-Server potrebbe avere immesso una posizione diversa durante l'installazione.

3.  Creare nuovamente la cartella di archiviazione configurando il percorso di archiviazione, l'account del servizio Advanced Group Policy Management, il proprietario dell'archivio e la porta di ascolto. Non è necessario usare gli stessi valori usati durante l'installazione originale. Per altre informazioni, vedere [modificare il servizio Advanced Group Policy Management](modify-the-agpm-service-agpm40.md).

4.  Copiare il contenuto del backup dell'archivio nella cartella di archiviazione, copiando le sottocartelle e i file per verificare che tutte le sottocartelle e i file ereditino le autorizzazioni della cartella di archiviazione. Prestare attenzione a non sovrascrivere la cartella di archiviazione.

5.  Se non si è certi che un GPO nel backup dell'archivio sia più attuale della copia di tale oggetto in produzione, generare un report di differenza e confrontarne le impostazioni. Per altre informazioni, vedere [identificare le differenze tra GPO, versioni GPO o modelli](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).

6.  Riavviare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service-agpm40.md).

### Riferimenti aggiuntivi

-   [Eseguire il backup dell'archivio](back-up-the-archive-agpm40.md)

-   [Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo](move-the-agpm-server-and-the-archive-agpm40.md)

-   [Gestione dell'archivio](managing-the-archive-agpm40.md)

 

 





