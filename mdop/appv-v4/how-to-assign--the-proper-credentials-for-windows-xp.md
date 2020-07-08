---
title: Come assegnare le credenziali appropriate per Windows XP
description: Come assegnare le credenziali appropriate per Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819325"
---
# Come assegnare le credenziali appropriate per Windows XP


Usare la procedura seguente per configurare il client Desktop App-V per le credenziali WindowsXP appropriate.

**Nota**  Dopo aver completato questa procedura, il client non collegato al dominio può eseguire un aggiornamento della pubblicazione senza essere associato a un dominio.

 

**Per assegnare le credenziali appropriate per i client App-V in cui è in uso WindowsXP**

1.  Con i privilegi di amministratore nel client App-V in cui è in uso WindowsXP, aprire il pannello di controllo **degli account utente** (pannello di controllo classico).

2.  Fare clic sulla **scheda Avanzate**e selezionare **Gestisci password**.

3.  Nella schermata **archiviazione nomi utente e password** fare clic su **Aggiungi**.

4.  Nella schermata **Proprietà informazioni di accesso** compilare i campi seguenti con le informazioni dell'infrastruttura App-V:

    1.  **Server:** Nome del nome del server di pubblicazione esterno.

    2.  **Nome utente:** Nome utente per utenti esterni nel modulo Domain\\username.

    3.  **Password:** Password per l'account utente immesso nel campo **nome utente** .

5.  Fai clic su **OK**. Le credenziali verranno archiviate nel client.

## Argomenti correlati


[Client aggiunti e non aggiunti a un dominio](domain-joined-and-non-domain-joined-clients.md)

[Come assegnare le credenziali appropriate per Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





