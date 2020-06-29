---
title: Configurazione dei criteri dell'area di lavoro MED-V
description: Configurazione dei criteri dell'area di lavoro MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824856"
---
# Configurazione dei criteri dell'area di lavoro MED-V


Un criterio di area di lavoro MED-V è un gruppo di impostazioni configurabili che definiscono l'esecuzione dell'ambiente virtualizzato e delle applicazioni nel computer host. Gli argomenti di questa sezione descrivono tutte le impostazioni configurabili nei criteri dell'area di lavoro MED-V e il modo in cui queste impostazioni influenzano l'area di lavoro MED-V.

Sono disponibili i tipi di area di lavoro MED-V seguenti:

-   **Persistente**: in un'area di lavoro MED-v persistente, tutte le modifiche e le aggiunte apportate dall'utente all'area di lavoro MED-v vengono salvate nell'area di lavoro MED-v tra le sessioni. Inoltre, un'area di lavoro MED-V persistente viene in genere usata in un ambiente di dominio.

-   **Revertible**-in un'area di lavoro di Revertible Med-v, al termine di ogni sessione (ovvero quando l'area di lavoro MED-v viene interrotta), l'area di lavoro MED-v ritorna allo stato originale durante la distribuzione. Nessuna modifica o aggiunta che l'utente ha eseguito viene salvata nell'area di lavoro MED-V tra le sessioni. Un'area di lavoro di revertible MED-V non può essere usata in un ambiente di dominio.

È importante decidere il tipo di area di lavoro MED-V che si sta creando prima di distribuire l'area di lavoro MED-V, perché non è consigliabile riconfigurare il tipo di area di lavoro MED-V dopo la distribuzione di un criterio agli utenti.

**Nota**  Quando si configura un criterio, accanto a campi obbligatori non compilati viene visualizzato un simbolo di avviso. Se non viene compilato un campo obbligatorio, anche il simbolo viene visualizzato nella scheda.

 

## In questa sezione


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[Come applicare le impostazioni generali a un'area di lavoro MED-V](how-to-apply-general-settings-to-a-med-v-workspace.md)  
Descrive le impostazioni generali di un'area di lavoro MED-V e come applicarle a un criterio.

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[Come applicare le impostazioni della macchina virtuale a un'area di lavoro MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
Descrive le impostazioni della macchina virtuale per un'area di lavoro MED-V e come applicarle a un criterio.

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[Come configurare un utente o un gruppo di dominio](how-to-configure-a-domain-user-or-groupmedvv2.md)  
Descrive come configurare gli utenti e i gruppi di dominio.

<a href="" id="how-to-configure-published-applications"></a>[Come configurare le applicazioni pubblicate](how-to-configure-published-applicationsmedvv2.md)  
Descrive le applicazioni e i menu pubblicati e come applicarli a un criterio.

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[Come configurare le impostazioni Web per un'area di lavoro MED-V](how-to-configure-web-settings-for-a-med-v-workspace.md)  
Descrive le impostazioni Web disponibili per un'area di lavoro MED-V e come applicarle a un criterio.

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[Come configurare la macchina virtuale per un'area di lavoro MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
Descrive la configurazione della macchina virtuale per un'area di lavoro MED-V e come applicarla a un criterio.

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[Come applicare le impostazioni di rete a un'area di lavoro MED-V](how-to-apply-network-settings-to-a-med-v-workspace.md)  
Descrive le impostazioni di rete di un'area di lavoro MED-V e come applicarle a un criterio.

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[Come applicare le impostazioni delle prestazioni a un'area di lavoro MED-V](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
Descrive le impostazioni delle prestazioni di un'area di lavoro MED-V e come applicarle a un criterio.

<a href="" id="how-to-import-and-export-a-policy"></a>[Come importare ed esportare un criterio](how-to-import-and-export-a-policy.md)  
Descrive come importare ed esportare un criterio.

 

 





