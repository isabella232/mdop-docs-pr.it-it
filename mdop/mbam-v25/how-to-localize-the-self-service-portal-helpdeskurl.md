---
title: Come localizzare il portale self-service "HelpdeskURL"
description: Come localizzare il portale self-service "HelpdeskURL"
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826706"
---
# Come localizzare il portale self-service "HelpdeskURL"


Puoi configurare una versione localizzata dell'URL del portale self-service da visualizzare agli utenti finali per impostazione predefinita. L'URL del portale self-service è rappresentato dal parametro **HelpdeskURL**.

Se si crea una versione localizzata, come descritto nelle istruzioni seguenti, Microsoft BitLocker Administration and Monitoring (MBAM) trova e visualizza la versione localizzata. Se MBAM non trova una versione localizzata, Visualizza l'URL configurato per il parametro **HelpDeskURL**.

**Nota**  Nelle istruzioni seguenti, *selfservice* è il nome della directory virtuale predefinita per il portale self-service. Quando hai configurato il portale self-service, potresti aver usato un nome diverso.

 

**Per localizzare l'URL del portale self-service**

1.  Nel server in cui è stato configurato il portale self-service individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni delle applicazioni**di Microsoft BitLocker selfservice.

2.  Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .

3.  Nel campo **nome** Digitare **HelpdeskURL**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per l'URL.

    Ad esempio, per creare una versione localizzata del `HelpdeskURL` valore in spagnolo, denominare il parametro **HelpdeskURL \ _es-es**.

    Il nome della cartella della lingua può essere anche il nome neutro della lingua **es** anziché **es-es**. Se il browser dell'utente finale è impostato su **es-es** e tale cartella non esiste, le impostazioni locali padre (come definito in .NET) vengono recuperate e controllate ricorsivamente, risolvendo &lt; la directory di installazione di mbam Self-Service &gt;\\SelfServiceWebsite\\es\\Notice.txt prima di diventare definitivamente il file di Notice.txt predefinito. Questo fallback ricorsivo simula le regole di caricamento delle risorse .NET.

    Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Nel campo **valore** Digitare la versione localizzata del `HelpdeskURL` valore che si desidera visualizzare per gli utenti finali.



## Argomenti correlati


[Personalizzazione del portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md)

 

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




