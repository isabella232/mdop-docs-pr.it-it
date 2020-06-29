---
title: Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo
description: Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820486"
---
# Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo


Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione. Per impostazione predefinita, il servizio Advanced Policy Management è in ascolto sulla porta 4600. È possibile modificare la porta modificando il file di indice dell'archivio di Advanced Group Policy Management (avanzata) per ogni archivio.

**Nota**  Prima di modificare la porta in cui è in ascolto il servizio Advanced Group Policy Management, è consigliabile eseguire il backup del file di indice dell'Archivio Advanced Group Policy Management (gpostate.xml). Questo file si trova nella cartella immessa come percorso di archiviazione durante l'installazione di Advanced Group Policy Management-Server. Per impostazione predefinita, questa posizione di questo file è% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml nel server Advanced Group Policy Management. Se non si conosce il computer che ospita l'archivio, è possibile seguire la procedura per modificare il percorso di archiviazione per visualizzare il percorso di archiviazione corrente. Per altre informazioni, vedere [modificare il percorso di archiviazione](modify-the-archive-path.md).

 

Un account utente con accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management) e il file di indice di archivio è necessario per completare questa procedura.

**Per modificare la porta in cui è in ascolto il servizio Advanced Group Policy Management**

1.  Nel computer che ospita l'archivio aprire il file di indice di archivio (gpostate.xml) in un editor di testo.

2.  Nel file cercare **Advanced Group Policy Management: Port = "4600"**.

3.  Sostituire **4600** con la porta in cui deve essere ascoltata il servizio Advanced Group Policy Management. quindi, Salva e Chiudi il file.

4.  Nel server Advanced Group Policy Management riavviare il servizio Advanced Group Policy Management. Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service.md).

5.  Modificare la porta nella connessione del server Advanced Group Policy Management per ogni amministratore di criteri di gruppo. Per altre informazioni, vedere [configurare la connessione al server Advanced Group Policy Management](configure-the-agpm-server-connection.md).

6.  Ripetere la procedura per ogni server di archiviazione e Advanced Group Policy Management.

### Riferimenti aggiuntivi

-   [Gestione del servizio Gestione avanzata Criteri di gruppo](managing-the-agpm-service.md)

 

 





