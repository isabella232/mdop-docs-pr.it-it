---
title: Note sulla versione per App-V 5.0
description: Note sulla versione per App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804888"
---
# Note sulla versione per App-V 5.0


**Per cercare un problema specifico in queste note sulla versione, premere CTRL + F.**

Leggere accuratamente queste note sulla versione prima di installare App-V 5,0.

Queste note sulla versione contengono informazioni necessarie per installare correttamente App-V 5,0. Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V 5,0, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Informazioni sulla documentazione del prodotto


Per informazioni sulla documentazione di App-V 5,0, vedere la Home page di App-V 5,0 in Microsoft TechNet.

## Inviare commenti e suggerimenti


Siamo interessati a ricevere commenti e suggerimenti su App-V 5,0. È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .

**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future nella documentazione e nei rilasci del prodotto.

 

Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemi noti di App-V 5,0


Questa sezione contiene note sulla versione sui problemi noti di App-V 5,0.

### Non è possibile terminare l'aggiunta di pacchetti quando si usano i cmdlet di PowerShell per server

Quando si aggiunge un pacchetto con PowerShell, non esiste alcun metodo per uscire dall'aggiunta di nuovi pacchetti.

SOLUZIONE alternativa: per interrompere l'aggiunta di pacchetti, premere **invio** dopo aver aggiunto il pacchetto finale.

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> Il client App-V 5,0 rifiuta i pacchetti dai server il cui certificato SSL è stato revocato

Quando si usa il protocollo HTTPS, per impostazione predefinita il client App-V 5,0 rifiuterà i pacchetti da server il cui certificato SSL è stato revocato. Questo comportamento può essere disattivato tramite la configurazione modificando l'impostazione **VerifyCertificateRevocationList** . L'applicazione di una nuova configurazione per questa impostazione non avrà effetto finché non viene riavviato il servizio App-V 5,0.

SOLUZIONE alternativa: riavviare il servizio App-V 5,0.

## Informazioni sul copyright delle note sulla versione


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società. Tutti gli altri marchi sono proprietà dei rispettivi proprietari.








## Argomenti correlati


[Informazioni su App-V 5.0](about-app-v-50.md)

 

 





