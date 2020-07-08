---
title: Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione
description: Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827275"
---
# Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione


Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 supportano le applicazioni Microsoft Application Virtualization (App-V) senza apportare modifiche necessarie al pacchetto App-V o al modello UE-V. Tuttavia, è necessario un passaggio aggiuntivo perché non è possibile eseguire il generatore UE-V direttamente in un'applicazione App-V virtualizzata. È invece necessario installare l'applicazione localmente, generare il modello e quindi applicare il modello all'applicazione virtualizzata. UE-V supporta i pacchetti App-V 4,5, App-V 4,6 e App-V 5,0.

## Sincronizzazione delle impostazioni di UE-V per le applicazioni App-V


UE-V monitora quando un'applicazione si apre con il nome del programma e, facoltativamente, per i numeri di versione del file e i numeri di versione del prodotto, indipendentemente dal fatto che l'applicazione sia installata localmente o virtualmente usando App-V. Quando l'applicazione viene avviata, la UE-V monitora il processo App-V, applica tutte le impostazioni archiviate nel percorso di archiviazione delle impostazioni dell'utente e quindi consente l'avvio normale dell'applicazione. UE-V monitora le applicazioni App-V e traduce automaticamente i percorsi di file e del registro di sistema pertinenti nella posizione virtualizzata rispetto alla posizione fisica esterna all'ambiente di elaborazione di App-V.

 **Per implementare la sincronizzazione delle impostazioni per un'applicazione virtualizzata**

1.  Eseguire il generatore di UE-V per raccogliere le impostazioni dell'applicazione installata localmente di cui si vuole sincronizzare i computer. Questo processo crea un modello di posizione delle impostazioni. Se si usa un modello predefinito, ad esempio il modello Microsoft Office 2010, ignorare questo passaggio. Per altre informazioni sull'uso del generatore UE-V, vedere [distribuire UE-v 2. x per le applicazioni personalizzate](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).

2.  Installare il pacchetto dell'applicazione App-V se non è già stato fatto.

3.  Pubblicare il modello nella posizione del catalogo del modello di impostazioni o installare manualmente il modello usando il `Register-UEVTemplate` cmdlet di Windows PowerShell.

    **Nota**  Se pubblichi il modello appena creato nel catalogo dei modelli di impostazioni, il client non riceverà il modello fino a quando il provider di sincronizzazione non aggiornerà le impostazioni. Per avviare manualmente il processo, aprire **utilità di pianificazione**, espandere **la raccolta**utilità di pianificazione, espandere **Microsoft**ed espandere **UE-V**. Nel riquadro risultati fare clic con il pulsante destro del mouse su **aggiornamento automatico modelli**e quindi scegliere **Esegui**.

     

4.  Avviare il pacchetto App-V.






## Argomenti correlati


[Amministrazione di UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





