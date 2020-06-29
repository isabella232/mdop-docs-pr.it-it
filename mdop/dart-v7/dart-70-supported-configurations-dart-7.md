---
title: Configurazioni supportate di DaRT 7.0
description: Configurazioni supportate di DaRT 7.0
author: dansimp
ms.assetid: e9ee87b0-3254-4625-b178-17b2f5b8f8c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b074a061c402f86769e42d873e0119ac54080c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804419"
---
# Configurazioni supportate di DaRT 7.0


L'ambiente può già soddisfare i requisiti di configurazione forniti in questo articolo in modo da poter installare ed eseguire Microsoft Diagnostics and Recovery Toolset (DaRT) 7. Questi includono i requisiti seguenti per l'immagine di ripristino e lo spazio su disco.

## Requisiti per l'immagine di ripristino DaRT 7


Non è supportata la creazione di immagini di ripristino multipiattaforma. Nella tabella seguente viene specificato il tipo di immagine di ripristino che è necessario creare e distribuire nell'organizzazione:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Piattaforma e versione DaRT</th>
<th align="left">Requisiti per l'immagine di ripristino</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>64 bit DaRT 7,0</p></td>
<td align="left"><p>Creare e usare un'immagine di ripristino delle freccette di 64 bit.</p></td>
</tr>
<tr class="even">
<td align="left"><p>32 bit DaRT 7,0</p></td>
<td align="left"><p>Creare e usare un'immagine di ripristino delle freccette di 32 bit.</p></td>
</tr>
</tbody>
</table>

 

## Requisiti per i computer degli utenti finali di DaRT 7


La finestra del **set di strumenti di diagnostica e ripristino** in DART richiede che il computer di destinazione usi uno dei sistemi operativi seguenti insieme alla quantità specificata di memoria di sistema disponibile per DART:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Requisiti di sistema per DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7 64 bit (2GB)</p></td>
<td align="left"><p>2,5 GB di memoria di sistema</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7 32 bit (1GB)</p></td>
<td align="left"><p>1.5 GB di memoria di sistema</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 (512MB)</p></td>
<td align="left"><p>1GB di memoria di sistema</p></td>
</tr>
</tbody>
</table>

 

DaRT offre anche i requisiti hardware minimi seguenti:

-   Un'unità CD o DVD o una porta USB

    Questa operazione è obbligatoria se si distribuisce un dardo nell'organizzazione usando un CD, un DVD o un dispositivo USB.

-   Supporto del BIOS per avviare il computer da un CD o DVD, da un'unità flash USB o da una partizione remota o di ripristino

## Argomenti correlati


[Pianificazione della distribuzione di DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





