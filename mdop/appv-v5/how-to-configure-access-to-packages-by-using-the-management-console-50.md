---
title: Come configurare l'accesso ai pacchetti tramite la console di gestione
description: Come configurare l'accesso ai pacchetti tramite la console di gestione
author: dansimp
ms.assetid: 8f4c91e4-f4e6-48cf-aa94-6085a054e8f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0e1f5b51b118dc7b783a4a550e19fd39a61a0ab4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805715"
---
# Come configurare l'accesso ai pacchetti tramite la console di gestione


Prima di distribuire un pacchetto virtualizzato di App-V 5,0, è necessario configurare i gruppi di sicurezza di Active Directory Domain Services (AD DS) che saranno autorizzati ad accedere ed eseguire le applicazioni. I gruppi di sicurezza possono contenere computer o utenti. L'intitolazione di un pacchetto a un gruppo di computer pubblica il pacchetto a livello globale in tutti i computer del gruppo.

Usare la procedura seguente per configurare l'accesso ai pacchetti virtualizzati.

**Per concedere l'accesso a un pacchetto App-V 5,0**

1.  Trovare il pacchetto che si vuole configurare:

    1.  Aprire la console di gestione di App-V 5,0.

    2.  Per visualizzare la pagina di **accesso ad** , fare clic con il pulsante destro del mouse sul pacchetto da configurare e scegliere **modifica Active Directory Access**. In alternativa, selezionare il pacchetto e fare clic su **modifica** nel riquadro di **accesso ad** .

2.  Eseguire il provisioning di un gruppo di sicurezza per il pacchetto:

    1.  Accedere alla pagina **Trova nomi di Active Directory validi e Concedi accesso** .

    2.  Usando il formato del nome del **dominio**  \\  **groupname**, digitare il nome o una parte di un oggetto gruppo di Active Directory e fare clic su **Verifica**.

        **Nota**  Assicurati di specificare un nome di dominio associato per il gruppo che stai cercando.

         

3.  Per concedere l'accesso al pacchetto, selezionare il gruppo desiderato e fare clic su **Concedi accesso**. Il gruppo appena aggiunto viene visualizzato nel riquadro **ad entità con Access** .

4.  

    Per accettare le impostazioni di configurazione predefinite e chiudere la pagina di **accesso ad** , fare clic su **Chiudi**.

    Per personalizzare le configurazioni per un gruppo specifico, fare clic sull'elenco a discesa **Configurazioni assegnate** e selezionare **personalizzato**. Per configurare le configurazioni personalizzate, fare clic su **modifica**. Dopo aver concesso l'accesso, fare clic su **Chiudi**.

**Per rimuovere l'accesso a un pacchetto di App-V 5,0**

1.  Trovare il pacchetto che si vuole configurare:

    1.  Aprire la console di gestione di App-V 5,0.

    2.  Per visualizzare la pagina di **accesso ad** , fare clic con il pulsante destro del mouse sul pacchetto da configurare e scegliere **modifica Active Directory Access**. In alternativa, selezionare il pacchetto e fare clic su **modifica** nel riquadro di **accesso ad** .

2.  Selezionare il gruppo che si vuole rimuovere e fare clic su **Elimina**.

3.  Per chiudere la pagina di **accesso ad** , fare clic su **Chiudi**.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.0](operations-for-app-v-50.md)

 

 





