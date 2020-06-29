---
title: Tecnologia TrimTransfer di MED-V
description: Tecnologia TrimTransfer di MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826186"
---
# Tecnologia TrimTransfer di MED-V


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


La tecnologia di deduplicazione Advanced Trim Transfer MED-V consente di velocizzare il download delle immagini delle macchine virtuali iniziali e aggiornate tramite la rete LAN o WAN, riducendo così la larghezza di banda necessaria per il trasporto di una macchina virtuale dell'area di lavoro MED-V a più utenti finali.

Questa tecnologia rivoluzionaria usa i dati locali esistenti per creare l'immagine della macchina virtuale, sfruttando il fatto che in molti casi, la maggior parte della macchina virtuale, ad esempio i file di sistema e applicazione, esiste già nel disco dell'utente finale. Ad esempio, se una macchina virtuale contenente WindowsXP viene recapitata a un client che gestisce una copia locale di WindowsXP, MED-V rimuoverà automaticamente gli elementi di WindowsXP ridondanti dal trasferimento. Per garantire un'area di lavoro valida e funzionale, il client MED-V verifica in modo crittografico l'integrità dei dati locali prima che venga utilizzata, garantendo che i blocchi di dati locali siano identici per bit a quelli nell'immagine della macchina virtuale desiderata. I blocchi che non corrispondono non vengono usati.

Il processo è efficiente per la larghezza di banda e trasparente e i trasferimenti vengono eseguiti in background, usando risorse di rete e CPU inutilizzate.

Quando si esegue l'aggiornamento a una nuova versione di immagine, ad esempio quando gli amministratori desiderano distribuire una nuova applicazione o patch, vengono scaricati solo gli elementi che sono stati modificati ("Delta") e non l'intera macchina virtuale, riducendo in modo significativo la larghezza di banda e il tempo di consegna della rete necessari.

Puoi configurare le cartelle indicizzate nell'host come parte del protocollo di trasferimento trim, in base al sistema operativo host. Queste impostazioni sono configurate nel file *ClientSettings.xml* , che si trova nella cartella **Servers\\Configuration Server\\** .

Quando si applicano nuove impostazioni, il servizio deve essere riavviato.

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





