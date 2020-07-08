---
title: Pianificazione per la migrazione da una versione precedente di App-V
description: Pianificazione per la migrazione da una versione precedente di App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805001"
---
# Pianificazione per la migrazione da una versione precedente di App-V


Usare le informazioni seguenti per pianificare come eseguire la migrazione a Microsoft Application Virtualization (App-V) 5,1 dalle versioni precedenti di App-V.

## Requisiti di migrazione


Prima di iniziare gli aggiornamenti, esaminare i requisiti seguenti:

-   Se si esegue l'aggiornamento da una versione precedente a App-V 4,6 SP2, eseguire l'aggiornamento alla versione App-V 4,6 SP3 prima di eseguire l'aggiornamento a App-V 5,1 o versioni successive. In questo scenario aggiornare innanzitutto i client App-V e quindi aggiornare i componenti del server.
**Nota:** App-V 4,6 è uscito dal supporto mainstream.

-   App-V 5,1 supporta solo i pacchetti creati con App-V 5,0 o App-V 5,1 o i pacchetti che sono stati convertiti nel formato **appv** .

-   Se si sta aggiornando l'App-V Server da App-V 5,0 SP1, vedere [informazioni su App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) per istruzioni.

## Eseguire il client App-V 5,1 in concomitanza con l'App-V 4,6


Puoi eseguire il client App-V 5,1 contemporaneamente nello stesso computer con il client App-V 4.6 SP3.

Quando si eseguono i client App-V coesistenti, è possibile:

-   Convertire un pacchetto App-V 4,6 SP3 nel formato App-V 5,1 e pubblicare entrambi i pacchetti, quando sono in uso entrambi i client.

-   Definire i criteri di migrazione per il pacchetto convertito, che consente al pacchetto convertito App-V 5,1 di assumere le associazioni di tipi di file e le scelte rapide dal pacchetto App-V 4,6.

### Scenari di coesistenza supportati

La tabella seguente Mostra gli scenari di coesistenza di App-V supportati. È consigliabile installare gli aggiornamenti disponibili più recenti di una determinata versione quando si esegue client coesistenti.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo di client App-V 4,6</th>
<th align="left">Tipo di client App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,6 SP3</p></td>
<td align="left"><p>App-V 5.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 SP3 RDS</p></td>
<td align="left"><p>App-V 5,1 RDS</p></td>
</tr>
</tbody>
</table>

 

### Requisiti per l'uso di client coesistenti

Per eseguire i client coesistenti, è necessario:

-   Installare il client App-V 4.6 prima di installare il client App-V 5,1.

-   Abilitare l'impostazione attiva criteri di gruppo **modalità di migrazione** , che si trova nel nodo di coesistenza client **App-V** &gt; **Client Coexistence** . Per distribuire il modello con estensione ADMX, vedere [come scaricare e distribuire i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://technet.microsoft.com/library/dn659707.aspx).

**Nota**  I pacchetti App-V 5,1 possono essere eseguiti affiancati con i pacchetti App-V 4,6 Se si hanno installazioni coesistenti di App-V 5,1 e 4,6. Tuttavia, i pacchetti App-V 5,1 non possono interagire con i pacchetti App-V 4,6 nello stesso ambiente virtuale.

 

### Download e documentazione client

La tabella seguente fornisce collegamenti ai download client App-V 4,6 e alla documentazione di TechNet sulle versioni. I download includono i client App-V "regolari" e RDS. La documentazione di TechNet relativa al client App-V si applica a entrambi i client, se non diversamente specificato.

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versione App-V</th>
<th align="left">Collegamento alla documentazione di TechNet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)">Informazioni su Microsoft Application Virtualization 4.6 SP3</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)">Informazioni su Microsoft Application Virtualization 5,1</a></p></td>
</tr>
</tbody>
</table>

 

Per altre informazioni su come configurare la coesistenza client di App-V 5,1, vedere:

-   [Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [App-V 5,0 coesistenza e migrazione](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a>Conversione dei pacchetti "versione precedente" tramite il convertitore di pacchetti


Prima di eseguire la migrazione di un pacchetto, creato con app-4.6 SP2 o versioni precedenti, in App-V 5,1, esaminare i requisiti seguenti:

-   Devi convertire il pacchetto nel formato di file con **estensione appv** .

-   Il convertitore di pacchetti supporta solo la conversione diretta dei pacchetti creati usando App-V 4,5 e versioni successive. Per usare il convertitore di pacchetti in un pacchetto creato con una versione precedente, devi usare un'app-V 4.5 o una versione successiva del sequencer per aggiornare il pacchetto, quindi puoi eseguire la conversione del pacchetto.

Per altre informazioni sull'uso del convertitore di pacchetti per convertire un pacchetto, vedere [come convertire un pacchetto creato in una versione precedente di App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md). Dopo aver convertito il file, è possibile distribuirlo in computer di destinazione che eseguono il client App-V 5,1.






## Argomenti correlati


[Pianificazione della distribuzione di App-V](planning-to-deploy-app-v51.md)

 

 





