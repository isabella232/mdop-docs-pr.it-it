---
title: Come aggiungere manualmente un'applicazione
description: Come aggiungere manualmente un'applicazione
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817096"
---
# Come aggiungere manualmente un'applicazione


Quando si aggiunge un'applicazione all'Application Virtualization Management Server, è consigliabile importarla. È possibile aggiungere manualmente un'applicazione, ma è necessario specificare le informazioni precise e dettagliate sull'applicazione richiesta in questa sezione.

**Per aggiungere manualmente una nuova applicazione**

1.  Nel riquadro sinistro fare clic con il pulsante destro del mouse sul nodo **applicazioni** e scegliere **nuova applicazione**.

2.  Nella **procedura guidata nuova applicazione**completare la finestra di dialogo **informazioni generali** :

    1.  **Nome applicazione**: digitare il nome che si desidera venga visualizzato dagli utenti.

    2.  **Versione**: digitare la versione dell'applicazione.

    3.  **Enabled**: questa casella deve essere selezionata per eseguire il flusso dell'applicazione dopo averla creata.

    4.  **Descrizione**: digitare una descrizione facoltativa per l'uso amministrativo.

    5.  **Percorso OSD**: esplorare la rete in un file OSD (Open Software Descriptor) dell'applicazione. Questo file deve trovarsi in una cartella di rete condivisa.

    6.  **Percorso icona**: individuare il file ico dell'applicazione.

    7.  **Gruppo di licenze applicative**: se sono stati configurati gruppi di licenze, è possibile assegnare l'applicazione a uno selezionandolo nell'elenco a discesa.

    8.  **Gruppo Server**: se si hanno più server di virtualizzazione delle applicazioni, è possibile assegnarlo a uno selezionando l'applicazione nell'elenco a discesa.

3.  Fai clic su **Avanti**.

4.  Nella finestra di dialogo **Seleziona pacchetto** selezionare il pacchetto correlato e fare clic su **Avanti**.

5.  Nella schermata **collegamenti pubblicati** selezionare le caselle relative alle posizioni in cui si desidera visualizzare i tasti di scelta rapida dell'applicazione nei computer client e fare clic su **Avanti**.

6.  Nella schermata **associazioni di file** è possibile aggiungere nuove associazioni di tipi di file a questa applicazione. A tale scopo, fare clic su **Aggiungi**, immettere l'estensione (senza un punto precedente), immettere una descrizione e fare clic su **OK**.

7.  Fai clic su **Avanti**.

8.  Nella finestra di dialogo **autorizzazioni di accesso** fare clic su **Aggiungi**.

9.  Nella finestra di dialogo **Aggiungi/modifica gruppo utenti** passare al gruppo utenti. È anche possibile immettere il dominio e il gruppo digitando le informazioni nei rispettivi campi. Al termine, fare clic su **OK**. È possibile aggiungere altri gruppi con le stesse pagine.

10. Fai clic su **Avanti**.

11. Nella schermata **Riepilogo** è possibile rivedere le impostazioni di importazione. Fare clic su **fine** per aggiungere l'applicazione, fare clic su **Torna** per modificare le informazioni o su **Annulla**.

## Argomenti correlati


[Come gestire le applicazioni in Server Management Console](how-to-manage-applications-in-the-server-management-console.md)

 

 





