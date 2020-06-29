---
title: Come caricare un'immagine MED-V nel server
description: Come caricare un'immagine MED-V nel server
author: dansimp
ms.assetid: 0e70dfdf-3e3a-4860-970c-535806caa907
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6703eb24bc3542c280af41988a257a2f14643645
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825705"
---
# Come caricare un'immagine MED-V nel server


Dopo aver testato un'immagine MED-V, è possibile che venga imballata e quindi caricata nel server. Per informazioni sulla configurazione di un server di distribuzione Web delle immagini, vedere [come configurare il server di distribuzione Web Image](how-to-configure-the-image-web-distribution-server.md).

Una volta che un'immagine MED-V viene compressa e caricata nel server, può essere distribuita agli utenti usando un centro di distribuzione del software aziendale oppure può essere scaricata dagli utenti che usano un pacchetto di distribuzione. Per informazioni sulla distribuzione tramite un centro distribuzione software aziendale, vedere [distribuzione di un'area di lavoro MED-V tramite un sistema di distribuzione del software aziendale](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md). Per informazioni sulla distribuzione tramite un pacchetto, vedere [distribuzione di un'area di lavoro MED-V tramite un pacchetto di distribuzione](deploying-a-med-v-workspace-using-a-deployment-package.md).

**Nota**  
Prima di caricare un'immagine, verificare che un proxy Web non sia definito nelle impostazioni del browser e che Windows Update non sia attualmente in uso.



**Per caricare un'immagine MED-V nel server**

1.  Nel riquadro **Immagini locali imballati** selezionare l'immagine creata.

2.  Fare clic su **carica**.

    L'immagine viene caricata nel server. Potrebbe essere necessario un periodo di tempo considerevole.

    Le immagini nel server sono definite con le proprietà elencate nella tabella seguente.

**Immagini imballate sulle proprietà del server**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Proprietà</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nome immagine</p></td>
<td align="left"><p>Nome dell'immagine imballata come è stato definito quando l'amministratore ha creato l'immagine.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versione</p></td>
<td align="left"><p>La versione dell'immagine visualizzata.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Tutte le versioni precedenti vengono mantenute, a meno che non vengano eliminate.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Dimensioni file (compressi)</p></td>
<td align="left"><p>Dimensione compressa fisica dell'immagine.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Dimensioni immagine (non compresso)</p></td>
<td align="left"><p>Dimensioni non compresse fisiche dell'immagine.</p></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Come installare il client MED-V e MED-V Management Console](how-to-install-med-v-client-and-med-v-management-console.md)

[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'immagine Virtual PC per MED-V](creating-a-virtual-pc-image-for-med-v.md)

[Come comprimere un'immagine MED-V](how-to-pack-a-med-v-image.md)









