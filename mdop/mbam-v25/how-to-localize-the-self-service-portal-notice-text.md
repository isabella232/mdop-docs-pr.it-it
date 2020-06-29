---
title: Come localizzare il testo dell'avviso nel portale self-service
description: Come localizzare il testo dell'avviso nel portale self-service
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826715"
---
# Come localizzare il testo dell'avviso nel portale self-service


È possibile configurare il testo dell'avviso localizzato per la visualizzazione agli utenti finali per impostazione predefinita nel portale self-service. Il file Notice.txt che Visualizza il testo dell'avviso si trova nella directory radice seguente:

&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self

Per visualizzare il testo dell'avviso localizzato, è possibile creare un file Notice.txt localizzato e salvarlo in una specifica cartella della lingua nella directory di esempio seguente:

&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self

**Nota**  Puoi configurare il percorso usando l'elemento **NoticeTextPath** nelle **impostazioni dell'applicazione**.

 

MBAM Visualizza il testo dell'avviso in base alle regole seguenti:

-   Se crei un file **Notice.txt** localizzato nella cartella della lingua appropriata, mbam visualizzerà il testo dell'avviso localizzato se il file di **Notice.txt** predefinito esiste. Se manca il file **Notice.txt** predefinito, viene visualizzato un messaggio che indica che il file predefinito non è presente.

-   Se MBAM non trova una versione localizzata del file Notice.txt, Visualizza il testo nel file Notice.txt predefinito.

-   Se MBAM non trova un file di Notice.txt predefinito, Visualizza il testo predefinito nel portale self-service.

**Nota**  Se il browser di un utente finale è impostato su una lingua che non ha una sottocartella o Notice.txt di lingua corrispondente, viene visualizzato il testo nel file Notice.txt nella directory radice seguente:

&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self

 

**Per creare un file Notice.txt localizzato**

1.  Nel server in cui è stato configurato il portale self-service creare una &lt; cartella della *lingua* &gt; nella directory di esempio seguente, dove &lt; *lingua* &gt; rappresenta il nome della lingua localizzata:

    &lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self

    **Nota**  Alcune cartelle di lingua esistono già, quindi potrebbe non essere necessario creare una cartella. Se è necessario creare una cartella della lingua, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) per un elenco dei nomi validi che è possibile usare per la cartella della &lt; *lingua* &gt; .

     

2.  Creare un file di Notice.txt contenente il testo dell'avviso localizzato.

3.  Salvare il file Notice.txt nella cartella della &lt; *lingua* &gt; . Ad esempio, per creare un file di Notice.txt localizzato in spagnolo, salvare il file Notice.txt localizzato nella directory di esempio seguente:

    &lt;Directory di installazione *di mbam self-service* &gt; Website\\Es-es servizio \\Self

    Il nome della cartella della lingua può essere anche il nome neutro della lingua **es** anziché **es-es**. Se il browser dell'utente finale è impostato su **es-es** e tale cartella non esiste, le impostazioni locali padre (come definito in .NET) vengono recuperate e controllate ricorsivamente, risolvendo &lt; la directory di installazione di mbam Self-Service &gt;\\SelfServiceWebsite\\es\\Notice.txt prima di diventare definitivamente il file di Notice.txt predefinito. Questo fallback ricorsivo simula le regole di caricamento delle risorse .NET.



## Argomenti correlati


[Personalizzazione del portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





