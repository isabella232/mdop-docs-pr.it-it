---
title: Pianificazione della distribuzione del server App-V 5.1
description: Pianificazione della distribuzione del server App-V 5.1
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804977"
---
# Pianificazione della distribuzione del server App-V 5.1


L'infrastruttura server di Microsoft Application Virtualization (App-V) 5,1 è costituita da un set di caratteristiche specializzate che possono essere installate in uno o più computer server, in base ai requisiti dell'organizzazione.

## Pianificazione della distribuzione di App-V 5,1 server


Il server App-V 5,1 è costituito dalle caratteristiche seguenti:

-   Server di gestione: offre funzionalità di gestione complessive per l'infrastruttura App-V 5,1.

-   Database di gestione: consente di semplificare le predistribuzioni di database per la gestione di App-V 5,1.

-   Publishing Server: offre funzionalità di hosting e flusso per le applicazioni virtuali.

-   Reporting Server: offre app-V 5,1 Reporting Services.

-   Database delle relazioni: consente di semplificare le predistribuzioni di database per la creazione di report in App-V 5,1.

Nell'elenco seguente sono visualizzati i metodi consigliati per l'installazione dell'infrastruttura server App-V 5,1:

-   Installare il server App-V 5,1. Per altre informazioni, vedere [come distribuire il server App-V 5,1](how-to-deploy-the-app-v-51-server.md).

-   Installare le funzionalità di database, creazione di report e gestione in computer distinti. Per altre informazioni, vedere [come installare i database di gestione e Reporting in computer separati da gestione e Reporting Services](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md).

-   Usare Electronic Software Distribution (ESD). Per altre informazioni, Vedi [come distribuire pacchetti App-V 5,1 usando la distribuzione elettronica del software](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).

-   Installare tutte le funzionalità del server in un singolo computer.

## <a href="" id="---------app-v-5-1-server-interaction"></a> Interazione del server App-V 5,1


Questa sezione contiene informazioni sul modo in cui i vari ruoli del server App-V 5,1 interagiscono tra loro.

Il server di gestione di App-V 5,1 contiene il repository dei pacchetti e le relative configurazioni assegnate. Per i server di pubblicazione registrati con il server di gestione, i metadati associati vengono forniti ai server di pubblicazione per l'uso quando le richieste di aggiornamento della pubblicazione vengono ricevute dai computer che eseguono il client App-V 5,1. I server di pubblicazione App-V 5,1 gestiti da un singolo server di gestione possono servire diversi client e possono avere nomi di siti Web e binding di porta diversi. Inoltre, tutti i server di pubblicazione gestiti dallo stesso server di gestione sono repliche.

**Nota**  Il server di gestione non esegue alcun bilanciamento del carico. I metadati associati vengono semplicemente passati al server di pubblicazione per l'utilizzo durante l'elaborazione delle richieste client.

 

## Protocolli correlati al server e funzionalità esterne


Le informazioni seguenti visualizzano i protocolli relativi al server usati dai server App-V 5,1. La tabella include anche il meccanismo di creazione di report per ogni tipo di server.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di server</th>
<th align="left">Protocolli</th>
<th align="left">Caratteristiche esterne necessarie</th>
<th align="left">Creazione di rapporti</th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Server IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Questa combinazione di protocollo server richiede un meccanismo per sincronizzare il contenuto tra il server di gestione e il server di flusso. Quando si usa HTTP o HTTPS, usare un server IIS e un firewall per proteggere il server dall'esposizione a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p>File</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Questa combinazione di protocollo server richiede il supporto per sincronizzare il contenuto tra il server di gestione e il server di flusso. Usare un computer client con funzionalità di condivisione o flusso di file.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## Argomenti correlati


[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

[Distribuzione del server App-V 5.1](deploying-the-app-v-51-server.md)

 

 





