---
title: Come localizzare l'istruzione "HelpdeskText" che indirizza gli utenti verso altre informazioni nel portale self-service
description: Come localizzare l'istruzione "HelpdeskText" che indirizza gli utenti verso altre informazioni nel portale self-service
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823425"
---
# Come localizzare l'istruzione "HelpdeskText" che indirizza gli utenti verso altre informazioni nel portale self-service


È possibile configurare una versione localizzata dell'istruzione Self-Service Portal "HelpdeskText", che informa gli utenti finali su come ottenere assistenza aggiuntiva quando usano il portale self-service. Se si configura il testo localizzato per l'istruzione, come descritto nelle istruzioni seguenti, MBAM Visualizza la versione localizzata. Se MBAM non trova la versione localizzata, Visualizza il valore che si trova nel parametro **HelpdeskText** .

**Nota**  Nelle istruzioni seguenti, *selfservice* è il nome della directory virtuale predefinita per il portale self-service. Quando hai configurato il portale self-service, potresti aver usato un nome diverso.

 

**Per visualizzare una versione localizzata dell'istruzione HelpdeskText**

1.  Nel server in cui è stato configurato il portale self-service individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni delle applicazioni**di Microsoft BitLocker selfservice.

2.  Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .

3.  Nel campo **nome** Digitare **HelpdeskText**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per il testo.

    Ad esempio, per creare un'istruzione HelpdeskText localizzata in spagnolo, denominare il parametro **HelpdeskText \ _es-es**.

    Il nome della cartella della lingua può essere anche il nome neutro della lingua **es** anziché **es-es**. Se il browser dell'utente finale è impostato su **es-es** e tale cartella non esiste, le impostazioni locali padre (come definito in .NET) vengono recuperate e controllate ricorsivamente, risolvendo &lt; la directory di installazione di mbam Self-Service &gt;\\SelfServiceWebsite\\es\\Notice.txt prima di diventare definitivamente il file di Notice.txt predefinito. Questo fallback ricorsivo simula le regole di caricamento delle risorse .NET.

    Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Nel campo **valore** Digitare il testo localizzato che si vuole visualizzare per gli utenti finali.



## Argomenti correlati


[Personalizzazione del portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md)

 

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



