---
title: Come installare il client MED-V e MED-V Management Console
description: Come installare il client MED-V e MED-V Management Console
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826985"
---
# Come installare il client MED-V e MED-V Management Console


I componenti MED-V seguenti sono inclusi nel pacchetto client. msi:

-   Client MED-V: il software MED-V che deve essere installato nei computer client per l'uso delle aree di lavoro MED-V.

-   MED-V Management Console: lo strumento di amministrazione che gli amministratori possono usare per creare e gestire le immagini, le aree di lavoro MED-V e i criteri.

La console di gestione MED-V e il client MED-V sono entrambi installati dal pacchetto client. msi di MED-V. Il client MED-V, tuttavia, può essere installato in modo indipendente senza la console di gestione MED-V deselezionando la casella di controllo **installa l'applicazione di gestione MED-** v durante l'installazione.

**Nota**  
Il client MED-V e la console di gestione MED-V possono essere installati solo nei computer basati su Windows 7, Windows Vista e Windows XP. Non è possibile installare i prodotti server.



**Nota**  
Non installare il client MED-V usando il comando Windows **RunAs** .



**Per installare il client MED-V**

1.  Accedere come utente con i diritti di amministratore locale nel computer locale.

2.  Eseguire il pacchetto MED-V. msi.

    Il pacchetto MED-V. msi si chiama *MED-V\_x.msi*, dove *x* corrisponde al numero di versione.

    Ad esempio, *MED-V\_1.0.65.msi*.

3.  Quando viene visualizzata la schermata **iniziale della procedura guidata InstallShield** , fare clic su **Avanti**.

4.  Nella schermata **contratto di licenza** leggere il contratto di licenza, fare clic su **Accetto i termini del contratto di licenza**e quindi fare clic su **Avanti**.

    Verrà visualizzata la schermata **cartella di destinazione** con la cartella di installazione predefinita visualizzata.

    La cartella di installazione predefinita è la directory in cui è installato il sistema operativo.

    -   Per modificare la cartella in cui deve essere installato MED-V, fare clic su **Cambia**e selezionare una cartella esistente.

5.  Fai clic su **Avanti**.

6.  Nella schermata **Impostazioni Med-v** configurare l'installazione di Med-v come indicato di seguito:

    -   Selezionare la casella di controllo **installa l'applicazione di gestione MED-V** per includere il componente di gestione nell'installazione.

        **Nota**  
        Gli amministratori di virtualizzazione desktop aziendale devono installare l'applicazione di gestione MED-V. Questa applicazione è necessaria per la configurazione di immagini desktop e aree di lavoro MED-V.



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. Fai clic su **Avanti**.

8. Nella schermata **pronto per l'installazione** fare clic su **Installa**.

   Viene avviata l'installazione del client MED-V. Questo può richiedere diversi minuti e la schermata potrebbe non visualizzare il testo. Durante l'installazione vengono visualizzate diverse schermate di stato. Se viene visualizzato un messaggio, seguire le istruzioni fornite.

   Una volta completata l'installazione, viene visualizzata la schermata **completamento configurazione guidata InstallShield** .

9. Fare clic su **fine** per chiudere la procedura guidata.

## Argomenti correlati


[Configurazioni supportate](supported-configurationsmedv-orientation.md)

[Elenchi di controllo per l'installazione e l'aggiornamento](installation-and-upgrade-checklists.md)









