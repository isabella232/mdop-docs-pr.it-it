---
title: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0
description: Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824086"
---
# Come modificare le impostazioni degli oggetti Criteri di gruppo per MBAM 2.0


Per distribuire correttamente l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è necessario prima di tutto determinare i criteri di gruppo che verranno usati nell'implementazione dell'amministrazione e del monitoraggio di Microsoft BitLocker. Per altre informazioni sui diversi criteri disponibili, vedere [pianificazione dei requisiti di criteri di gruppo per MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) . Dopo aver determinato i criteri che si intende usare, è necessario modificare uno o più oggetti Criteri di gruppo che includono le impostazioni dei criteri per MBAM.

È possibile usare la procedura seguente per configurare le impostazioni di GPO di base consigliate per consentire a MBAM di gestire la crittografia BitLocker per i computer client dell'organizzazione.

**Per modificare le impostazioni del GPO client MBAM**

1.  In un computer in cui è installato il modello di criteri di gruppo di MBAM verificare che i servizi MBAM siano abilitati.

2.  Usando la console Gestione criteri di gruppo (GPMC. msc) o il prodotto MDOP Advanced Group Policy Management in un computer in cui è installato il modello di criteri di gruppo di MBAM, selezionare **Configurazione computer**, scegliere **criteri**, **modelli amministrativi**, **componenti di Windows**e quindi fare clic su **MDOP mbam (Gestione BitLocker)**.

3.  Modificare le impostazioni degli oggetti Criteri di gruppo necessarie per abilitare i servizi client di MBAM nei computer client. Per ogni criterio nella tabella seguente selezionare **gruppo criteri**, fare clic sul **criterio**e quindi configurare l' **impostazione**:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Gruppo criteri</th>
    <th align="left">Criterio</th>
    <th align="left">Impostazione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Gestione dei client</p></td>
    <td align="left"><p>Configurare i servizi MBAM</p></td>
    <td align="left"><p>Abilitata. Impostare l' <strong> endpoint del servizio hardware e ripristino </strong> di mbam e <strong> selezionare informazioni di ripristino di BitLocker da archiviare </strong> . Impostare l' <strong> endpoint del servizio </strong> di conformità mbam e immettere la frequenza del rapporto di stato in (minuti).</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unità del sistema operativo</p></td>
    <td align="left"><p>Impostazioni di crittografia unità del sistema operativo</p></td>
    <td align="left"><p>Abilitata. Impostare <strong> Seleziona protezione per l'unità del sistema operativo </strong> . Necessario per salvare i dati dell'unità del sistema operativo nel server di ripristino MBAMKey.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unità rimovibile</p></td>
    <td align="left"><p>Controllare l'uso di BitLocker su unità rimovibili</p></td>
    <td align="left"><p>Abilitata. Obbligatorio se MBAM Salva i dati dell'unità rimovibili nel server di ripristino di chiave di MBAM.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unità fissa</p></td>
    <td align="left"><p>Controllare l'uso di BitLocker su unità fisse</p></td>
    <td align="left"><p>Abilitata. Obbligatorio se MBAM Salva i dati di unità fissati nel server di ripristino della chiave di MBAM.</p>
    <p>Impostare <strong> scegliere il modo in cui le unità protette da BitLocker possono essere recuperate </strong> e <strong> consentire l'agente di recupero dati </strong> .</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Argomenti correlati


[Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)









