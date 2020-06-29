---
title: Come aggiungere o aggiornare pacchetti tramite la console di gestione
description: Come aggiungere o aggiornare pacchetti tramite la console di gestione
author: dansimp
ms.assetid: 62417b63-06b2-437c-8584-523e1dea97c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4ac458a5e33b83e19d72fee39cf837aa6bd57bc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805763"
---
# Come aggiungere o aggiornare pacchetti tramite la console di gestione


È possibile eseguire la procedura seguente per aggiungere o aggiornare un pacchetto alla console di gestione di App-V 5,1. Per aggiornare un pacchetto già esistente nella console di gestione, eseguire la procedura seguente e importare il pacchetto aggiornato usando lo stesso **nome**del pacchetto.

**Per aggiungere un pacchetto alla console di gestione**

1.  Fare clic sulla scheda **pacchetti** nel riquadro di spostamento della visualizzazione della console di gestione.

    Nella console viene visualizzato l'elenco dei pacchetti che sono stati aggiunti al server insieme alle informazioni sullo stato di ogni pacchetto. Quando si seleziona un pacchetto, nel riquadro **pacchetti** vengono visualizzate informazioni dettagliate sul pacchetto.

    Fare clic sulla casella di riepilogo a discesa non **raggruppata** e specificare la modalità di visualizzazione dei pacchetti nella console. È anche possibile fare clic sull'intestazione di colonna associata per ordinare i pacchetti.

2.  Per specificare il pacchetto che si vuole aggiungere, fare clic su **Aggiungi o Aggiorna pacchetti**.

3.  Digitare il percorso completo del pacchetto che si vuole aggiungere. Usare il formato percorso UNC o HTTP, ad esempio **\\\\servername\\sharename\\foldername\\packagename.AppV** o **http://server.1234/file.appv** , e quindi fare clic su **Aggiungi**.

    **Importante**  Devi selezionare un pacchetto con l'estensione di file **appv** .

     

4.  Nella pagina viene visualizzato il messaggio di stato che **aggiunge &lt; PackageName &gt; **. Fare clic su **Importa stato** per controllare lo stato di un pacchetto importato.

    Fare clic su **OK** per aggiungere il pacchetto e chiudere la pagina **Aggiungi pacchetto** . Se durante l'importazione si è verificato un errore, fare clic su **Dettagli** nella pagina **importazione pacchetto** per altre informazioni. Il pacchetto appena aggiunto è ora disponibile nel riquadro **pacchetti** .

5.  Fare clic su **Chiudi** per chiudere la pagina **Add o upgrade packages** .

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





