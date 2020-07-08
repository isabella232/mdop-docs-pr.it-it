---
title: Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5
description: Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804347"
---
# Modifica delle impostazioni dei Criteri di gruppo di MBAM 2.5


Per distribuire correttamente Microsoft BitLocker Administration and Monitoring (MBAM), è necessario:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Attività</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copiare i modelli dei criteri di gruppo di MBAM 2,5.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copia dei modelli dei Criteri di gruppo di MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Determinare gli oggetti Criteri di gruppo che si desidera utilizzare nell'implementazione di MBAM. In base alle esigenze dell'organizzazione, potrebbe essere necessario configurare altre impostazioni di criteri di gruppo.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Pianificazione per i requisiti di criteri di gruppo di MBAM 2,5 </a> -contiene le descrizioni dei GPO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Impostare le impostazioni dei criteri di gruppo per l'organizzazione.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Importante**  Non modificare le impostazioni dei criteri di gruppo nel nodo **crittografia unità BitLocker** oppure mbam non funzionerà correttamente. Quando si configurano le impostazioni dei criteri di gruppo nel nodo **MDOP mbam (BitLocker Management)** , mbam configura automaticamente le impostazioni di **crittografia unità BitLocker** .

 

**Per modificare le impostazioni dei criteri di gruppo di MBAM client**

1.  In un computer in cui sono installati i modelli di criteri di gruppo di MBAM verificare che i servizi MBAM siano abilitati.

2.  Usando la console Gestione criteri di gruppo (GPMC. msc) o il prodotto Microsoft Advanced Group Policy Management MDOP in un computer con i modelli di criteri di gruppo di mbam installati, selezionare criteri di **configurazione dei computer** &gt; **Policies** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (Gestione BitLocker)**.

3.  Modificare le impostazioni dei criteri di gruppo necessarie per abilitare i servizi client di MBAM nei computer client. Per ogni criterio nella tabella seguente selezionare **gruppo criteri**, fare clic sul **criterio** desiderato e quindi configurare le impostazioni.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Gruppo criteri</th>
    <th align="left">Criterio</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Gestione dei client</p></td>
    <td align="left"><p>Configurare i servizi MBAM</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unità del sistema operativo</p></td>
    <td align="left"><p>Impostazioni di crittografia unità del sistema operativo</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unità rimovibile</p></td>
    <td align="left"><p>Controllare l'uso di BitLocker su unità rimovibili</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unità fissa</p></td>
    <td align="left"><p>Controllare l'uso di BitLocker su unità fisse</p></td>
    </tr>
    </tbody>
    </table>

     

## Argomenti correlati


[Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)

[Copia dei modelli dei Criteri di gruppo di MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





