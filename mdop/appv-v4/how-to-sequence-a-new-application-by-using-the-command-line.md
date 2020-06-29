---
title: Come sequenziare una nuova applicazione con la riga di comando
description: Come sequenziare una nuova applicazione con la riga di comando
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816686"
---
# Come sequenziare una nuova applicazione con la riga di comando


Puoi usare una riga di comando per sequenziare una nuova applicazione. L'uso di una riga di comando è utile quando è necessario creare un numero elevato di applicazioni virtuali o quando è necessario creare applicazioni sequenziate su base periodica.

**Importante**  
La sequenziazione della riga di comando consente solo la sequenziazione predefinita. Se è necessario modificare le impostazioni di installazione predefinite per l'applicazione che si sta sequenziando, è necessario modificare manualmente l'applicazione virtuale o aggiornare l'applicazione virtuale tramite Application Virtualization (App-V) Sequencer. Per altre informazioni sull'aggiornamento di un'applicazione virtuale tramite App-V Sequencer, vedere [come aggiornare un'applicazione virtuale esistente](how-to-upgrade-an-existing-virtual-application.md).



Usare la procedura seguente per creare un'applicazione virtuale tramite la riga di comando.

**Per sequenziare un'applicazione usando la riga di comando**

1.  Nel computer in cui è in esecuzione l'App-V Sequencer aprire il prompt dei comandi selezionando **Start**, **Esegui**e quindi digitare **cmd**. Fai clic su **OK**.

2.  Usare il prompt dei comandi per specificare la posizione in cui è installato l'App-V Sequencer. Ad esempio, al prompt dei comandi digitare quanto segue: **CD C:\\Programmi \\Programmi\\microsoft Application Virtualization Sequencer**.

3.  Al prompt dei comandi digitare il comando seguente, sostituendo il testo tra virgolette con i valori seguenti:

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Nota**  
    Puoi specificare parametri aggiuntivi usando la riga di comando, a seconda della complessità dell'applicazione che stai sequenziando. Per un elenco completo dei parametri disponibili per l'uso con l'App-V Sequencer, Vedi [parametri della riga di comando sequencer](sequencer-command-line-parameters.md).



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
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Premere **invio**.

## Argomenti correlati


[Come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[Codici di errore della riga di comando di Sequencer](sequencer-command-line-error-codes.md)

[Parametri della riga di comando di Sequencer](sequencer-command-line-parameters.md)









