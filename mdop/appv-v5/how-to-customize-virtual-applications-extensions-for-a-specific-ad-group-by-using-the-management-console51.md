---
title: Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione
description: Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione
author: dansimp
ms.assetid: dd71df05-512f-4eb4-a55f-e5b93601323d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bf086da3fbb6938a4fc602af5ab63adb1621532
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805590"
---
# Come personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory specifico tramite la console di gestione


Usare la procedura seguente per personalizzare le estensioni delle applicazioni virtuali per un gruppo Active Directory (AD).

**Per personalizzare le estensioni delle applicazioni virtuali per un gruppo di annunci**

1.  Per visualizzare il pacchetto che si vuole configurare, aprire la console di gestione di App-V 5,1. Per visualizzare la configurazione assegnata a un gruppo di utenti specifico, selezionare il pacchetto e fare clic con il pulsante destro del mouse sul nome del pacchetto e scegliere **modifica Active Directory Access**. In alternativa, selezionare il pacchetto e fare clic su **modifica** nel riquadro di **accesso ad** .

2.  Per personalizzare un gruppo di annunci, puoi trovare il gruppo nell'elenco delle **entità pubblicitarie con Access**. Quindi, usando la casella di menu a discesa nel riquadro **configurazione assegnata** , selezionare **personalizzato**e quindi fare clic su **modifica**.

3.  Per disabilitare tutte le estensioni per una determinata applicazione, deselezionare **Abilita**.

    Per aggiungere un nuovo collegamento per l'applicazione selezionata, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Aggiungi nuovo collegamento**. Per rimuovere un collegamento, fare clic con il pulsante destro del mouse sull'applicazione nel riquadro **collegamenti** e scegliere **Rimuovi collegamento**. Per modificare un collegamento esistente, fare clic con il pulsante destro del mouse sull'applicazione e scegliere **Modifica collegamento**.

4.  Per visualizzare le altre estensioni dell'applicazione, fare clic su **Avanzate**e quindi su **Esporta configurazione**. Digitare un nome di file e fare clic su **Salva**. Puoi visualizzare tutte le estensioni dell'applicazione associate al pacchetto usando il file di configurazione.

5.  Per modificare altre estensioni dell'applicazione, modificare il file di configurazione e fare clic su **Importa e Sovrascrivi questa configurazione**. Selezionare il file modificato e fare clic su **Apri**. Nella finestra di dialogo fare clic su **Sovrascrivi** per completare il processo.

    **Hai un suggerimento per App-V**? Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Hai un problema con l'App-V?** Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Argomenti correlati


[Operazioni per App-V 5.1](operations-for-app-v-51.md)

 

 





