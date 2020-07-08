---
title: Come importare un'applicazione
description: Come importare un'applicazione
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817405"
---
# Come importare un'applicazione


In genere si importano le applicazioni per renderle disponibili per lo streaming da un Application Virtualization Management Server. È anche possibile aggiungere manualmente un'applicazione, ma è necessario specificare informazioni precise e dettagliate sull'applicazione. Per altre informazioni, vedere [come aggiungere manualmente un'applicazione](how-to-manually-add-an-application.md).

**Nota**  Per importare un'applicazione, è necessario che il file OSD (Open Software Descriptor) sequenziato o il file di progetto sequencer (SPRJ) sia disponibile nel server.

 

Quando si importa un'applicazione, è necessario assicurarsi che il server sia configurato con un valore nel campo **percorso di contenuto predefinito** nella scheda **generale** della finestra di dialogo **Opzioni di sistema** (accessibile facendo clic con il pulsante destro del mouse sul nodo **Application Virtualization System** nella console App-V Server). Il valore predefinito del percorso di contenuto definisce la posizione in cui verranno importate le applicazioni e durante il processo di importazione questo valore viene usato per modificare i percorsi definiti nel file OSD per il file SFT e per le scelte rapide da icona. Nel file OSD, il percorso del file SFT viene specificato nella voce CODEBASE HREF e il percorso per le icone viene specificato nella voce di tasti di scelta rapida.

Durante il processo di importazione, il protocollo, il server e, se presente, la porta specificata in questi due percorsi nel file OSD verranno sostituiti con il valore del percorso di contenuto predefinito. La tabella seguente contiene un esempio di come verrà influenzato il percorso di importazione.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Percorso di contenuto predefinito</th>
<th align="left">File OSD CODEBASE HREF</th>
<th align="left">Valore risultante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\server\content &lt; /p&gt;</td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p>\server\content\myFolder\package.sft</p></td>
</tr>
</tbody>
</table>

 

**Per importare un'applicazione**

1.  Fare clic con il pulsante destro del mouse sul nodo **applicazioni** nel riquadro sinistro e scegliere **Importa applicazioni**.

2.  Nella finestra di dialogo **Apri** passare al file SPRJ o OSD dell'applicazione. Evidenziare il file e fare clic su **Apri**.

3.  Nella **creazione guidata nuova applicazione**verificare che la casella **abilitato** sia selezionata per le applicazioni che si desidera eseguire il flusso. È anche possibile immettere una descrizione e verificare il server e i percorsi dei file. Inoltre, se è stata configurata la licenza e i gruppi di server, è possibile selezionarli.

4.  Fai clic su **Avanti**.

5.  Nella schermata **collegamenti pubblicati** selezionare le caselle relative alle posizioni in cui si desidera visualizzare i tasti di scelta rapida dell'applicazione nei computer client.

6.  Fai clic su **Avanti**.

7.  Nella schermata **associazioni di file** è possibile aggiungere nuove associazioni di file a questa applicazione. A tale scopo, fare clic su **Aggiungi**, immettere l'estensione (senza un punto precedente), immettere una descrizione e fare clic su **OK**.

    **Nota**  Le applicazioni sequenziate con sequencer 4,0 popolano la finestra di dialogo **associazioni di file** quando vengono importate o create tramite la console di gestione. Le applicazioni con i pacchetti di versioni precedenti di Sequencer non lo fanno.

     

8.  Fai clic su **Avanti**.

9.  Nella schermata **autorizzazioni di accesso** fare clic su **Aggiungi**.

10. Completare la finestra di dialogo **Seleziona gruppi** . Al termine, fare clic su **OK**.

11. Fai clic su **Avanti**.

12. Nella schermata **Riepilogo** è possibile rivedere le impostazioni di importazione. Fare clic su **fine**oppure su **Torna** per cambiare l'importazione o fare clic su **Annulla** per annullare l'importazione.

## Argomenti correlati


[Come gestire i gruppi di applicazioni in Server Management Console](how-to-manage-application-groups-in-the-server-management-console.md)

[Come gestire le applicazioni in Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

[Come aggiungere manualmente un'applicazione](how-to-manually-add-an-application.md)

 

 





