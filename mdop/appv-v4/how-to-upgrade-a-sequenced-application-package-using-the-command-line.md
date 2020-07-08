---
title: Come aggiornare un pacchetto di applicazione sequenziata usando la riga di comando
description: Come aggiornare un pacchetto di applicazione sequenziata usando la riga di comando
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816486"
---
# Come aggiornare un pacchetto di applicazione sequenziata usando la riga di comando


Usare la procedura seguente per aggiornare un'applicazione virtuale tramite una riga di comando. Quando si aggiorna un pacchetto di applicazione virtuale esistente tramite la riga di comando, la versione originale del file SFT viene eliminata. È consigliabile eseguire il backup del file SFT associato prima di aggiornare il pacchetto tramite la riga di comando.

**Per aggiornare un'applicazione virtuale**

1.  Nel computer in cui è in esecuzione Application Virtualization (App-V) Sequencer, per aprire il prompt dei comandi, selezionare **Start**, **Esegui**e digitare **cmd**. Fai clic su **OK**.

2.  Al prompt dei comandi specificare il percorso in cui è installato App-V Sequencer. Ad esempio, al prompt dei comandi digitare quanto segue: **CD C:\\Programmi \\Programmi\\microsoft Application Virtualization Sequencer**.

3.  Al prompt dei comandi digitare il comando seguente, sostituendo il testo tra virgolette con i valori seguenti:

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Nota**  
    Puoi specificare parametri aggiuntivi usando la riga di comando, a seconda della complessità dell'applicazione che stai aggiornando. Per un elenco completo dei parametri disponibili per l'uso con l'App-V Sequencer, Vedi [parametri della riga di comando](command-line-parameters.md).



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Premere **invio**.

## Argomenti correlati


[Come gestire le applicazioni virtuali usando la riga di comando](how-to-manage-virtual-applications-using-the-command-line.md)









