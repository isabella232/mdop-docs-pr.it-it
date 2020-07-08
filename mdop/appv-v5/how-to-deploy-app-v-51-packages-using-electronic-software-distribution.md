---
title: Come distribuire pacchetti App-V 5.1 usando una soluzione di distribuzione elettronica del software
description: Come distribuire pacchetti App-V 5.1 usando una soluzione di distribuzione elettronica del software
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805536"
---
# Come distribuire pacchetti App-V 5.1 usando una soluzione di distribuzione elettronica del software


Puoi usare un sistema ESD (Electronic Software Distribution) per distribuire le applicazioni virtuali App-V 5,1 ai client App-V. Per informazioni dettagliate, vedere la documentazione disponibile con l'ESD in uso.

Per i requisiti e le opzioni per i componenti per l'uso di un ESD per distribuire pacchetti App-V, vedere Pianificazione della distribuzione [di App-v 5,1 con un sistema di distribuzione elettronica del software](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).

Usa uno dei metodi seguenti per pubblicare i pacchetti in computer client App-V con un ESD:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Metodo</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Funzionalità fornite da un ESD di terze parti</p></td>
<td align="left"><p>Usare la funzionalità in un ESD di terze parti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Installer autonomo</p></td>
<td align="left"><p>Installare l'applicazione nel computer client di destinazione usando il file di Windows Installer (MSI) associato creato quando si sequenzia inizialmente un'applicazione. Il file di Windows Installer contiene le informazioni relative ai file del pacchetto App-V 5,1 usate per configurare un pacchetto e copia i file di pacchetto necessari nel client.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Usare i cmdlet di PowerShell per distribuire applicazioni virtualizzate. Per altre informazioni sull'uso di PowerShell e App-V 5,1, vedere <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> amministrazione di App-v 5,1 tramite PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

**Per distribuire i pacchetti App-V 5,1 usando un ESD**

1.  Installare il sequencer App-V 5,1 in un computer nell'ambiente. Per altre informazioni sull'installazione del sequencer, vedere [come installare Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Usare il sequencer App-V 5,1 per creare un'applicazione virtuale. Per informazioni sulla creazione di un'applicazione virtuale, vedere [creazione e gestione di applicazioni virtualizzate App-V 5,1](creating-and-managing-app-v-51-virtualized-applications.md).

3.  Dopo aver creato l'applicazione virtuale, distribuire il pacchetto usando la soluzione ESD.

    Se si usa System Center Configuration Manager, iniziare rivedendo [Introduzione alla gestione delle applicazioni in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) per informazioni sull'uso di App-V 5,1 e System Center2012 Configuration Manager.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





