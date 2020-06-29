---
title: Configurazione di MED-V per le reti remote
description: Configurazione di MED-V per le reti remote
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826725"
---
# Configurazione di MED-V per le reti remote


È possibile configurare MED-V in modo che funzioni all'interno di una rete, in remoto o sia dall'interno della rete che da remoto.

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**Per configurare MED-V per l'utilizzo all'interno di una rete**

-   Configurare un server MED-V e una distribuzione di immagini all'interno della rete.

**Per configurare MED-V per il lavoro in remoto**

1.  Configurare un server MED-V e un server di distribuzione delle immagini accessibile da Internet.

2.  Se necessario, configurare una rete perimetrale (detta anche DMZ) come proxy inverso.

3.  Impostare il metodo di autenticazione, nel file *ClientSettings.xml* , che si trova nella cartella **Servers\\Configuration Server\\** .

**Per configurare MED-V in modo che funzioni sia dall'interno di una rete che da remoto**

1.  Configurare un server MED-V e un server di distribuzione delle immagini all'interno della rete.

2.  Verificare che i server siano accessibili da Internet.

3.  Configurare la risoluzione DNS in modo che quando il client tenti di connettersi a un server, si connetta automaticamente al server corretto (all'interno della rete o tramite Internet) in base alla posizione del client.

4.  Se necessario, configurare un proxy inverso della rete perimetrale.

5.  Impostare il metodo di autenticazione, nel file *ClientSettings.xml* , che si trova nella cartella **Servers\\Configuration Server\\** .

**Nota**  Quando si applicano nuove impostazioni, il servizio deve essere riavviato.

 

-   È possibile modificare lo schema di autenticazione di IIS in una delle opzioni seguenti: BASIC, DIGEST, NTLM o NEGOTIATe. Il valore predefinito è NEGOTIATe e usa la voce seguente:

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## Argomenti correlati


[Progettazione e pianificazione dell'infrastruttura MED-V](med-v-infrastructure-planning-and-design.md)

 

 





