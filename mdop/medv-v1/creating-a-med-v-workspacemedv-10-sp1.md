---
title: Creazione di un'area di lavoro MED-V
description: Creazione di un'area di lavoro MED-V
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824865"
---
# Creazione di un'area di lavoro MED-V


Un'area di lavoro MED-V è l'ambiente desktop in cui gli utenti finali interagiscono con la macchina virtuale fornita da MED-V. L'area di lavoro MED-V viene creata e personalizzata dall'amministratore. È costituito da un'immagine e dal criterio, che definisce le regole e le funzionalità dell'area di lavoro MED-V. È possibile creare più aree di lavoro MED-V, ognuna personalizzata con la propria configurazione, le impostazioni e le regole. Un utente, un gruppo o più utenti o gruppi può essere associato a ogni area di lavoro MED-V, rendendo così disponibile l'area di lavoro MED-V solo per i computer dell'utente o del gruppo associato.

## Come aggiungere un'area di lavoro MED-V


**Per aggiungere un'area di lavoro MED-V**

1.  Fare clic sul pulsante Gestione **criteri** per aprire il modulo dei **criteri** .

    Il modulo dei **criteri** è costituito dal menu **aree di lavoro** a sinistra e dalle schede **generale**, **macchina virtuale**, **distribuzione**, **applicazioni**, **Web**, **configurazione VM**, **rete**e **prestazioni** .

2.  Nel menu **criteri** selezionare **nuova area di lavoro**oppure fare clic su **Aggiungi** per creare una nuova area di lavoro MED-V.

3.  Nel campo **nome** della scheda **generale** immettere il nome dell'area di lavoro MED-V.

4.  Nel campo **Descrizione** immettere una descrizione per l'area di lavoro MED-V.

5.  Nel campo **informazioni contatto di supporto** immettere le informazioni di contatto per il supporto tecnico.

    Per altre informazioni sulla configurazione di un'area di lavoro MED-V, vedere [configurazione dei criteri di area di lavoro MED-v](configuring-med-v-workspace-policies.md).

## Come clonare un'area di lavoro MED-V


Un'area di lavoro MED-V può essere clonata in modo da poter creare un'area di lavoro MED-V identica a un'area di lavoro MED-V esistente.

**Per clonare un'area di lavoro MED-V**

1.  Fare clic sull'area di lavoro MED-V per clonare.

2.  Nel menu **criteri** selezionare **clona area di lavoro**.

    Viene creata una nuova area di lavoro MED-V con il nome &lt; area di lavoro originale Med-v &gt; -2.

## Come eliminare un'area di lavoro MED-V


**Per eliminare un'area di lavoro MED-V**

-   Nel modulo **criteri** , mentre il riquadro area di lavoro è in stato di attivazione, fare clic su **Rimuovi**.

## Argomenti correlati


[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

 

 





