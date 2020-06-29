---
title: Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0
description: Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826635"
---
# Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0


I modelli di posizione delle impostazioni personalizzate possono essere archiviati in un percorso di cartella nei computer Microsoft User Experience Virtualization (UE-V) o in una condivisione di rete SMB (Server Message Block). Un'attività pianificata nel computer verifica la ricerca di modelli nuovi o aggiornati da questa posizione. L'attività controlla questa posizione una volta al giorno e aggiorna il comportamento di sincronizzazione in base ai modelli presenti nella cartella. I modelli aggiunti o aggiornati in questa cartella dall'ultimo controllo vengono registrati dall'agente UE-V. L'agente UE-V Annulla la registrazione dei modelli rimossi dalla cartella. L'attività pianificata viene eseguita come SYSTEM. La condivisione di rete deve almeno concedere le autorizzazioni per il gruppo Domain Computers. Concedere inoltre le autorizzazioni di accesso per la cartella di condivisione di rete agli amministratori che gestiscono i modelli archiviati. Per altre informazioni sui modelli di posizione delle impostazioni personalizzate, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

**Per configurare il catalogo dei modelli di impostazioni per UE-V**

1.  Creare una nuova cartella nel computer in cui verrà memorizzato il catalogo dei modelli di impostazioni UE-V.

2.  Impostare le seguenti autorizzazioni SMB per la cartella del catalogo dei modelli di impostazioni.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Account utente</strong></th>
    <th align="left"><strong>Consigliare le autorizzazioni</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tutti</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computer di dominio</p></td>
    <td align="left"><p>Livelli di autorizzazione di lettura</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Livelli di autorizzazione di lettura/scrittura</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Impostare le autorizzazioni NTFS seguenti per la cartella del catalogo dei modelli di impostazioni.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Account utente</th>
    <th align="left">Autorizzazioni consigliate</th>
    <th align="left">Applica a</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creatore/proprietario</p></td>
    <td align="left"><p>Controllo completo</p></td>
    <td align="left"><p>Questa cartella, le sottocartelle e i file</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Computer di dominio</p></td>
    <td align="left"><p>Contenuto della cartella di elenco e lettura</p></td>
    <td align="left"><p>Questa cartella, le sottocartelle e i file</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Tutti</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    <td align="left"><p>Nessuna autorizzazione</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Controllo completo</p></td>
    <td align="left"><p>Questa cartella, le sottocartelle e i file</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Fare clic su **OK** per chiudere le finestre di dialogo.

## Argomenti correlati


[Distribuzione di UE-V 1.0](deploying-ue-v-10.md)

[Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





