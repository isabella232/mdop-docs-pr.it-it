---
title: Come applicare le impostazioni generali a un'area di lavoro MED-V
description: Come applicare le impostazioni generali a un'area di lavoro MED-V
author: dansimp
ms.assetid: 6152dced-e301-4fa2-bfa0-aecf3c23f23a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 176564ae1d22b27a24625d988f46c9746b291748
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826536"
---
# Come applicare le impostazioni generali a un'area di lavoro MED-V


Le impostazioni generali consentono di configurare l'esperienza utente di base quando si lavora con un'area di lavoro MED-V, definendo se l'area di lavoro MED-V verrà visualizzata in modalità di integrazione completa o desktop completo. L'integrazione perfetta include le applicazioni legacy nel desktop host in modo che vengano visualizzate come se fossero installate direttamente nell'host. Desktop completo presenta il desktop del sistema operativo MED-V Workspace in una finestra separata dell'host.

Tutte le impostazioni generali sono configurate nel modulo **criteri** , nella scheda **generale** .

**Per applicare le impostazioni generali a un'area di lavoro MED-V**

1.  Fare clic sull'area di lavoro MED-V per configurare.

2.  Configurare le proprietà generali come descritto nella tabella seguente.

3.  Nel menu **criteri** selezionare **commit**.

**Proprietà generali dell'area di lavoro**

Proprietà dell' *area di lavoro* Descrizione proprietà

Nome

Nome dell'area di lavoro MED-V.

**Avviso**  Non rinominare un'area di lavoro MED-V esistente mentre è in esecuzione in un computer client.

 

Descrizione

Descrizione dell'area di lavoro MED-V, che può includere il contenuto o lo stato dell'area di lavoro MED-V e tutte le altre informazioni utili.

**Nota**  La descrizione è per l'uso di amministratore e non ha alcun impatto sui criteri.

 

Info di contatto supporto tecnico

Le informazioni di contatto per il supporto tecnico. Le informazioni immesse verranno visualizzate nella schermata informazioni contatto di supporto a cui è possibile accedere dall'area di notifica del client MED-V.

*Interfaccia utente dell'area di lavoro*

Integrazione perfetta

Selezionare questa opzione per le icone dell'area di lavoro MED-V, della barra delle applicazioni e delle aree di notifica per integrarsi perfettamente nel desktop host.

Disegnare un fotogramma intorno a ogni finestra dell'area di lavoro

Quando si usa l'integrazione senza problemi, selezionare questa opzione per creare un bordo colorato intorno a tutte le applicazioni in uso nell'area di lavoro MED-V e uno sfondo colorato per tutte le icone del pulsante della barra delle applicazioni. Nel campo **colore cornice** selezionare il colore.

Desktop completo

Selezionare questa opzione per visualizzare l'area di lavoro MED-V come intero desktop, senza l'integrazione con l'host.

*Verifica host*

Riga di comando

Digitare una riga di comando da eseguire nell'host prima di avviare l'area di lavoro MED-V.

Non avviare l'area di lavoro se la verifica non riesce (il codice di uscita non è' 0')

Selezionare questa casella di controllo se si usa una riga di comando e si vuole avviare l'area di lavoro MED-V solo se lo script viene completato correttamente.

 

Una riga di comando può essere eseguita nell'host prima di avviare l'area di lavoro MED-V.

**Per eseguire una riga di comando prima di avviare un'area di lavoro MED-V**

1.  Nel campo **riga di comando** immettere una riga di comando.

2.  Per avviare l'area di lavoro MED-V solo se la riga di comando è stata eseguita correttamente, selezionare la casella di controllo non **avviare l'area di lavoro se la verifica non riesce** .

## Argomenti correlati


[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





