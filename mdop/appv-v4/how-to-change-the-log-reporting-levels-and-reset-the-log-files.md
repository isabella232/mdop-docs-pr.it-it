---
title: Come modificare i livelli del report di registro e azzerare i file di registro
description: Come modificare i livelli del report di registro e azzerare i file di registro
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818046"
---
# Come modificare i livelli del report di registro e azzerare i file di registro


È possibile usare la procedura seguente per modificare il livello di report del log dal nodo **Application Virtualization** in Application Virtualization Management Console. Quando il file di log raggiunge la dimensione massima (il valore predefinito è 256 MB), viene forzata una reimpostazione quando si verifica la successiva scrittura nel log. Un reset causa la creazione di un nuovo file di log e il vecchio file viene rinominato come backup.

**Per modificare il livello di report del log**

1.  Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.

2.  Nella scheda **generale** della finestra di dialogo **Proprietà** Selezionare il livello di log desiderato nell'elenco a discesa **livello log** .

    **Nota**  Se si sceglie **verbose** come livello di registrazione, i file di log si svilupperanno in modo molto rapido. Ciò potrebbe inibire le prestazioni del client, quindi è consigliabile usare questo livello di log solo per la diagnosi di problemi specifici.

     

3.  Nella scheda **generale** della finestra di dialogo **Proprietà** Selezionare il livello di log desiderato nell'elenco a discesa **livello registro di sistema** .

    **Nota**  L'impostazione **livello registro di sistema** controlla il livello di messaggi inviati al log eventi di sistema. I messaggi registrati sono identici ai messaggi che vengono registrati nel log eventi del client, ma archiviati in una posizione diversa.

     

4.  Fare clic su **OK** o su **applica** per modificare l'impostazione.

**Per reimpostare il file di log**

1.  Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.

2.  Nella scheda **generale** della finestra di dialogo **Proprietà** fare clic su **Reimposta log** per eseguire il backup del file di log corrente e avviare immediatamente un nuovo file di log. I file di log di backup sono archiviati nella stessa cartella.

3.  Fare clic su **OK** o su **applica** per modificare l'impostazione.

## Argomenti correlati


[Come configurare il client in Application Virtualization Client Management Console](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[Autorizzazioni di accesso utente in Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





