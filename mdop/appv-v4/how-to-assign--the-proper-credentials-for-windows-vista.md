---
title: Come assegnare le credenziali appropriate per Windows Vista
description: Come assegnare le credenziali appropriate per Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821366"
---
# Come assegnare le credenziali appropriate per Windows Vista


Usare la procedura seguente per configurare il client desktop di App-V per le credenziali di WindowsVista appropriate.

**Nota**  Questa procedura deve essere completata in ogni computer non appartenente a un dominio. A seconda del numero di computer non appartenenti a un dominio nell'ambiente, potrebbe trattarsi di un'operazione molto noiosa. Puoi usare gli script e l'interfaccia della riga di comando per Gestione credenziali per consentire agli amministratori di automatizzare questo processo.

 

**Per assegnare le credenziali appropriate per i client App-V che utilizzano Windows Vista**

1.  Con i privilegi di amministratore sul client Desktop App-V che utilizza Windows Vista, aprire il pannello di controllo **degli account utente** (pannello di controllo classico).

2.  Selezionare **Gestisci le password di rete** dagli **account utente** nel riquadro attività a sinistra.

3.  Selezionare **Aggiungi** nella schermata **archivia nomi utente e password** .

4.  Nella schermata **Proprietà credenziali archiviate** fornisci le informazioni per l'infrastruttura App-V:

    1.  **Accedere a:** Nome esterno del server di pubblicazione.

    2.  **Nome utente:** Nome utente per l'utente esterno nel formato Domain\\Username.

    3.  **Password:** Password per l'account utente immesso nel campo **nome utente** .

    4.  Uscire dal **tipo di credenziali** selezionato e fare clic su **OK**.

5.  Fai clic su **Chiudi**. Le credenziali sono archiviate nell'archivio credenziali per l'autenticazione corretta per l'infrastruttura App-V.

## Argomenti correlati


[Client aggiunti e non aggiunti a un dominio](domain-joined-and-non-domain-joined-clients.md)

[Come assegnare le credenziali appropriate per Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





