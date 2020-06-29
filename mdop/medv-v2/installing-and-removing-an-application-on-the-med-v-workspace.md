---
title: Installazione e rimozione di un'applicazione nell'area di lavoro MED-V
description: Installazione e rimozione di un'applicazione nell'area di lavoro MED-V
author: dansimp
ms.assetid: 24f32720-51ab-4385-adfe-4f5a65e45fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 22cb98c167b53b1b206b8b5be2ba18fc0fba4f06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827216"
---
# Installazione e rimozione di un'applicazione nell'area di lavoro MED-V


Le applicazioni che non sono compatibili con il sistema operativo host possono essere eseguite nell'area di lavoro MED-V e aperte nell'area di lavoro MED-V nello stesso modo in cui vengono aperte dal computer host, nel menu **Start** o usando un collegamento a localhost.

Dopo aver distribuito un'area di lavoro MED-V, sono disponibili diverse opzioni per l'installazione e la rimozione delle applicazioni nell'area di lavoro MED-V. Queste opzioni includono le seguenti:

-   [Uso di criteri di gruppo](#bkmk-grouppolicy)

-   [Uso di un sistema elettronico di distribuzione del software](#bkmk-esd)

-   [Uso della virtualizzazione delle applicazioni (APP-V)](#bkmk-appv)

-   [Aggiornamento dell'immagine di base](#bkmk-coreimage)

**Importante**  Per assicurarsi che un'applicazione installata venga pubblicata automaticamente nell'host, installare l'applicazione nella macchina virtuale per **tutti gli utenti**. Per altre informazioni sulla pubblicazione delle applicazioni, vedere [come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md).

 

**Suggerimento**  MED-V non supporta il reindirizzamento Guest-to-host per la gestione del contenuto, ad esempio fare doppio clic su un documento di Microsoft Word in Internet Explorer nell'area di lavoro MED-V. Di conseguenza, le applicazioni necessarie, ad esempio Microsoft Word, devono essere installate nell'area di lavoro MED-V per specificare le funzionalità di gestione del contenuto predefinite che un utente finale può aspettarsi.

 

## <a href="" id="bkmk-grouppolicy"></a> Aggiunta e rimozione di applicazioni tramite criteri di gruppo


Puoi usare gli oggetti Criteri di gruppo e criteri di gruppo per assegnare o pubblicare applicazioni in tutte le aree di lavoro di MED-V nell'organizzazione. Per le applicazioni assegnate, quando un utente finale accede al proprio computer, l'applicazione viene visualizzata nel menu **Start** . Quando si seleziona la nuova applicazione per la prima volta, l'applicazione viene installata ed è pronta per l'uso. Per le applicazioni pubblicate, l'applicazione non viene visualizzata nel menu **Start** . È disponibile solo per l'installazione da parte dell'utente finale utilizzando installazione **applicazioni** nel pannello di **controllo** o aprendo un file associato all'applicazione.

È anche possibile usare i criteri di gruppo e gli oggetti Criteri di gruppo allo stesso modo per rimuovere le applicazioni dall'area di lavoro MED-V.

Per altre informazioni su come aggiungere e rimuovere applicazioni tramite criteri di gruppo, vedere [installazione del software criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

## <a href="" id="bkmk-esd"></a> Aggiunta e rimozione di applicazioni tramite un sistema ESD


Un sistema ESD (Electronic Software Distribution) è progettato per distribuire efficacemente il software e altre informazioni a molti computer diversi tramite connessioni di rete. Se l'organizzazione usa un sistema ESD per distribuire il software, è possibile usarlo per aggiungere e rimuovere applicazioni nelle aree di lavoro MED-V così come si aggiungono e si rimuovono applicazioni in computer fisici.

## <a href="" id="bkmk-appv"></a> Aggiunta e rimozione di applicazioni tramite APP-V


Microsoft Application Virtualization (App-V) offre la funzionalità amministrativa per rendere le applicazioni disponibili per i computer degli utenti finali senza dover installare le applicazioni direttamente in tali computer. Potresti voler usare MED-V e App-V insieme se, ad esempio, l'organizzazione ha applicazioni sequenziate con App-V in Windows XP e la loro ripetizione sequenziale ritarderà la migrazione a Windows 7.

Puoi usare MED-V insieme a App-V per aggiungere e rimuovere applicazioni virtuali in un'area di lavoro MED-V distribuita. Per gestire le applicazioni in questo modo, devi prima installare l'agente App-V nel sistema operativo guest MED-V. Puoi quindi usare app-V nell'area di lavoro MED-V per aggiungere e rimuovere le applicazioni virtuali.

Per informazioni su come installare e usare app-V, vedere [virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .

**Importante**  Le applicazioni App-V pubblicate nell'area di lavoro MED-V hanno associazioni di tipi di file che non possono essere reindirizzate dal computer host alla macchina virtuale guest. Tuttavia, l'utente finale può comunque accedere a questi tipi di file facendo clic su **file**e quindi facendo clic su **Apri** nell'applicazione App-V pubblicata.

Per forzare il reindirizzamento delle associazioni di tipi di file, eseguire una query in App-V per le associazioni di tipi di file mappati digitando quanto segue al prompt dei comandi nella macchina virtuale Guest: **SFTMIME/query obj: Type**. Eseguire quindi il mapping delle associazioni di tipi di file nel computer host.

 

## <a href="" id="bkmk-coreimage"></a> Aggiunta e rimozione di applicazioni nell'immagine principale


Anche se non è considerata una procedura consigliata per MED-V, è possibile aggiungere e rimuovere applicazioni direttamente nell'immagine principale. Dopo aver aggiunto o rimosso un'applicazione, è possibile ridistribuire l'area di lavoro MED-V nell'organizzazione proprio come è stata distribuita in origine.

Per altre informazioni su come aggiungere o rimuovere applicazioni nell'immagine principale, vedere installazione di [applicazioni in un'immagine di Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md).

**Importante**  Questo metodo di gestione delle applicazioni non è consigliabile. Se si aggiungono o si rimuovono applicazioni nell'immagine principale e si ridistribuisce l'area di lavoro MED-V nell'organizzazione, è necessario eseguire di nuovo la configurazione per la prima volta e tutti i dati salvati nella macchina virtuale andranno perduti.

 

**Nota**  Anche se un'applicazione viene installata in un'area di lavoro MED-V, potrebbe essere necessario pubblicare l'applicazione anche prima che diventi disponibile per l'utente finale. Ad esempio, potrebbe essere necessario pubblicare un'applicazione installata se l'installazione non crea automaticamente un collegamento nel menu **Start** . Allo stesso modo, per annullare la pubblicazione di un'applicazione, potrebbe essere necessario rimuovere manualmente un collegamento dal menu **Start** .

Per impostazione predefinita, la maggior parte delle applicazioni viene pubblicata al momento dell'installazione, quando i tasti di scelta rapida vengono creati e abilitati automaticamente.

 

## Argomenti correlati


[Come verificare la pubblicazione delle applicazioni](how-to-test-application-publishing.md)

[Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





