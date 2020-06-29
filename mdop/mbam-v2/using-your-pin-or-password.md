---
title: Uso di PIN o password
description: Uso di PIN o password
author: dansimp
ms.assetid: 7fe2aef4-d3e0-49c8-877d-7fee13dc5b7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b8c4b894b8f3e14d2a5cfb39e744fa43874c6753
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823795"
---
# Uso di PIN o password


BitLocker consente di proteggere il computer richiedendo un PIN (Personal Identification Number) o una password per sbloccare le informazioni archiviate nel computer. I requisiti di PIN o password sono impostati dall'organizzazione e dipendono dal tipo di unità crittografata. I dati delle unità crittografate non possono essere visualizzati senza immettere il PIN o la password. Se l'hardware del computer include un TPM (Trusted Platform Module) abilitato, il chip TPM richiede il PIN prima dell'avvio di Windows nel computer.

## Informazioni sul PIN e le password di BitLocker


La tua azienda specifica la complessità necessaria per il PIN o la password. Questi requisiti per il PIN o la password vengono spiegati durante il processo di configurazione di BitLocker.

La password viene usata per sbloccare le unità nel computer che non contengono il sistema operativo. BitLocker richiederà la password dopo che il PIN è stato richiesto durante l'avvio. Ogni disco rigido protetto da BitLocker nel computer ha una password univoca. Non è possibile sbloccare un'unità protetta da BitLocker finché non si specifica la password.

**Nota**  Il tuo help desk può impostare le unità per l'apertura automatica. In questo articolo viene eliminata la necessità di specificare un PIN o una password per visualizzare le informazioni sulle unità.

 

## Sbloccare il computer se si dimentica il PIN o la password


Se si dimentica il PIN o la password, il proprio help desk può aiutarti a sbloccare le unità protette da BitLocker. Per sbloccare un'unità protetta con BitLocker, contattare il supporto tecnico se serve assistenza.

**Come sbloccare il computer se si dimentica il PIN o la password**

1.  Quando si contatta il proprio help desk, sarà necessario fornirle le informazioni seguenti:

    -   Nome utente

    -   Il dominio

    -   Le prime otto cifre dell'ID chiave di ripristino. Si tratta di un codice a 32 cifre che verrà visualizzato da BitLocker se si dimentica il PIN o la password.

        -   Se si dimentica il PIN, sarà necessario immettere le prime otto cifre dell'ID chiave di ripristino, che verrà visualizzato nella console di ripristino di BitLocker. La console di ripristino di BitLocker è una schermata precedente a Windows che verrà visualizzata se non si immette il PIN corretto.

        -   Se si dimentica la password, cercare l'ID chiave di ripristino nell'applicazione del pannello di controllo opzioni di crittografia BitLocker. Selezionare **Sblocca unità** e quindi fare clic su **non ricordo la password**. L'applicazione opzioni di crittografia BitLocker visualizzerà quindi un ID chiave di ripristino che fornisci per il supporto tecnico.

2.  Una volta che il tuo help desk riceve le informazioni necessarie, ti fornirà una chiave di ripristino tramite telefono o tramite posta elettronica.

    -   Se si è dimenticato il PIN, immettere il codice di ripristino nella console di ripristino di BitLocker per sbloccare il computer.

    -   Se si è dimenticata la password, immettere la chiave di ripristino nell'applicazione del pannello di controllo opzioni di crittografia BitLocker, nella stessa posizione in cui è stato trovato l'ID chiave di ripristino in precedenza. Verrà sbloccato il disco rigido protetto.

## Cambiare il PIN o la password


Prima di poter modificare la password in un'unità protetta da BitLocker, è necessario sbloccare l'unità. Se l'unità non è sbloccata, selezionare **Sblocca unità**e quindi immettere la password corrente. Non appena l'unità è sbloccata, è possibile selezionare **Gestisci la password** per cambiare la password corrente.

**Come cambiare il PIN o la password**

1.  Fare clic sul pulsante **Start**e quindi selezionare **Pannello di controllo**. Il pannello di controllo viene aperto in una nuova finestra.

2.  Selezionare **sistema e sicurezza**e quindi selezionare le **Opzioni di crittografia BitLocker**.

    -   Per cambiare il PIN, selezionare **Gestisci il pin**. Digitare il nuovo PIN in entrambi i campi e selezionare **Reimposta PIN**.

    -   Per cambiare la password, selezionare **Gestisci la password**. Immettere la nuova password in entrambi i campi e selezionare **Reimposta password**.

 

 





