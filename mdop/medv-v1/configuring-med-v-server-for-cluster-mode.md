---
title: Configurazione del server MED-V per la modalità cluster
description: Configurazione del server MED-V per la modalità cluster
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826716"
---
# Configurazione del server MED-V per la modalità cluster


È possibile configurare il server MED-V in modalità cluster. In modalità cluster vengono usati due server e tutti i file identificati come reciproci per entrambi i server vengono posizionati in un file System. Il server accede ai file dal file System anziché archiviare localmente i file.

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**Per configurare il server MED-V in modalità cluster**

1.  Installare e configurare MED-V in uno dei server.

2.  Creare una rete condivisa in una posizione centrale in cui tutti i server possono accedervi.

3.  Copiare il contenuto della cartella * &lt; INSTALLDIR &gt; /Servers/ConfigurationServer* nella rete condivisa.

4.  Installare il server MED-V in tutti i server designati.

5.  Nella rete condivisa assegnare l'accesso completo a tutti gli account di sistema di MED-V Server.

6.  In ogni server eseguire le operazioni seguenti:

    1.  Nel file * &lt; InstallDir &gt; /Servers/ServerConfiguration.xml* impostare il valore di * &lt; PercorsoArchivio &gt; * sul percorso di rete condiviso.

    2.  Copiare il file di * &lt; &gt; KeyPair.xml/Servers/InstsallDir* dal server originale a tutti i server MED-V.

    3.  Riavviare il servizio MED-V.

**Nota**  Se tutti i server hanno le stesse impostazioni locali, ad esempio le porte in attesa, il server IIS, le autorizzazioni di gestione, il database del report e così via, la * &lt; &gt; ServerSettings.xmlInstallDir/Servers/* può essere condivisa anche da tutti i server.

 

## Argomenti correlati


[Progettazione e pianificazione dell'infrastruttura MED-V](med-v-infrastructure-planning-and-design.md)

 

 





