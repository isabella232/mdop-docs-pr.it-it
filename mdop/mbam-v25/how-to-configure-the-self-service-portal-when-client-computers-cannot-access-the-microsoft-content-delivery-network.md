---
title: Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft
description: Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824495"
---
# Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft


Seguire queste istruzioni se i computer client dell'organizzazione non hanno accesso alla rete CDN (Microsoft AJAX Content Delivery Network).

**Perché è necessario configurare questo:**

I computer client devono accedere alla rete CDN, che fornisce al portale self-service l'accesso necessario a determinati file JavaScript. Se non si configura il portale self-service quando i computer client non riescono ad accedere alla rete CDN, verranno visualizzati solo il nome della società e l'account in cui l'utente finale accede. Nessun messaggio di errore verrà visualizzato.

**Nota**  In MBAM 2,5 SP1 i file JavaScript sono inclusi nel prodotto e non è necessario seguire le istruzioni in questa sezione per configurare il provider di servizi condivisi per supportare i client che non possono accedere a Internet.

 

**Come configurare il portale self-service quando i computer client non riescono ad accedere alla rete CDN**

1. Scaricare i seguenti file JavaScript dalla rete CDN:

   -   [jQuery-1.10.2.min.js](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [jQuery.validate.min.js](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [jQuery.validate.unobtrusive.min.js](https://go.microsoft.com/fwlink/?LinkID=390517)

2. Copiare i file JavaScript nella directory **Scripts** del portale self-service. Questa directory si trova in <em> &lt; mbam self-service install directory &gt; \\ </em> self service Website\\Scripts.

3. Aprire Gestione Internet Information Services (IIS).

4. Espandere i **siti** &gt; **di amministrazione e monitoraggio di Microsoft BitLocker**ed evidenziare **selfservice**.

   **Nota**  
   *Selfservice* è il nome della directory virtuale predefinita. Se si è scelto un nome diverso per questa directory durante la configurazione, ricordarsi di sostituire *selfservice* in queste istruzioni con il nome scelto.

     

5. Nel riquadro centrale fare doppio clic su **Impostazioni applicazione**.

6. Per ogni elemento dell'elenco seguente modificare le impostazioni dell'applicazione per fare riferimento alla nuova posizione sostituendo/ &lt; *directory virtuale* &gt; /con/selfservice/(o qualunque nome scelto durante la configurazione). Il percorso della directory virtuale, ad esempio, sarà simile a/selfservice/Scripts/jQuery-1.10.2.min.js.

   -   jQueryPath:/ &lt; *directory virtuale* &gt; /script/jQuery-1.10.2.min.js

   -   jQueryValidatePath:/ &lt; *directory virtuale* &gt; /script/jQuery.validate.min.js

   -   jQueryValidateUnobtrusivePath:/ &lt; *directory virtuale* &gt; /script/jQuery.validate.unobtrusive.min.js



## Argomenti correlati


[Come configurare le applicazioni Web di MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





