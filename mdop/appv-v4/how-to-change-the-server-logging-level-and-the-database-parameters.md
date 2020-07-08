---
title: Come modificare il livello di registrazione del server e i parametri del database
description: Come modificare il livello di registrazione del server e i parametri del database
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818035"
---
# Come modificare il livello di registrazione del server e i parametri del database


È possibile usare le procedure seguenti per modificare il livello di registrazione e i parametri del log del database dalla console di gestione di Application Virtualization Server.

Sono disponibili i livelli di registrazione seguenti:

-   Solo transazione

-   Errori irreversibili

-   Errori

-   Avvisi/errori

-   Info/avvisi/errori

-   Dettagliata

**Nota**  A causa delle dimensioni del file di log prodotto quando si usa la modalità **verbose** , si consiglia di non eseguire server di produzione con questo livello di set di registrazione.

 

I parametri di registrazione del database determinano il tipo di driver di database, le credenziali di accesso e la posizione del database di registrazione.

**Per modificare il livello di registrazione per i server di gestione**

1.  Fare clic sul nodo **gruppi di server** per visualizzare i gruppi di server.

2.  Fare clic con il pulsante destro del mouse sul gruppo Server e scegliere **Proprietà**.

3.  Nella finestra di dialogo **Proprietà** selezionare la scheda **registrazione** .

4.  Nella finestra di dialogo **Proprietà gruppo Server** selezionare il server e quindi fare clic su **modifica**.

5.  Nella finestra di dialogo **Aggiungi/modifica modulo log** selezionare il livello di registrazione nell'elenco a discesa **tipo di evento** .

6.  Fai clic su **OK**.

7.  Nella finestra di dialogo **Proprietà gruppo Server** fare clic su **OK** o su **applica**.

**Per modificare il livello di registrazione per i server di flusso**

1.  Modificare il valore della chiave del registro di sistema seguente per modificare il livello di registrazione:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel

2.  Selezionare uno dei valori seguenti per impostare il livello di registrazione.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Value</th>
    <th align="left">Livello di registrazione</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>0</p></td>
    <td align="left"><p>Solo transazioni</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>1</p></td>
    <td align="left"><p>Errori irreversibili</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>2</p></td>
    <td align="left"><p>Errori</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>3</p></td>
    <td align="left"><p>Avvisi/errori</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>4</p></td>
    <td align="left"><p>Informazioni/avvisi/errori</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>5</p></td>
    <td align="left"><p>Dettagliata</p></td>
    </tr>
    </tbody>
    </table>

     

**Per modificare i parametri del log del database**

1.  Fare clic sul nodo **gruppi di server** per visualizzare i gruppi di server.

2.  Fare clic con il pulsante destro del mouse sul gruppo Server e scegliere **Proprietà**.

3.  Nella finestra di dialogo **Proprietà** selezionare la scheda **registrazione** .

4.  Nella finestra di dialogo **Proprietà gruppo Server** selezionare il server e quindi fare clic su **modifica**.

5.  Nella finestra di dialogo **Aggiungi/modifica modulo log** selezionare un driver di database dall'elenco a discesa **driver del database** .

6.  Immettere un **nome host DNS**.

7.  Fare clic sulla casella di controllo **determina dinamicamente la porta** o immettere un numero di porta nel campo della **porta** .

8.  Immettere il **nome** di un servizio nel campo corrispondente.

9.  Fai clic su **OK**.

10. Nella finestra di dialogo **Proprietà gruppo Server** fare clic su **OK** o su **applica**.

## Argomenti correlati


[Come personalizzare un sistema di Application Virtualization in Server Management Console](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





