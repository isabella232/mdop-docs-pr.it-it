---
title: Come configurare le applicazioni pubblicate
description: Come configurare le applicazioni pubblicate
author: dansimp
ms.assetid: 43a59ff7-5d4e-49dc-84e5-1082bc4dd8f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cb5736382f03e818ef10aa814a8e61044ca2b73a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824315"
---
# Come configurare le applicazioni pubblicate


Le applicazioni che non sono compatibili con il sistema operativo host possono essere eseguite all'interno dell'area di lavoro MED-V e avviate dall'area di lavoro MED-V nello stesso modo in cui vengono avviate dal desktop, dal menu Start o da un collegamento a un host locale. Le applicazioni selezionate e definite sono denominate applicazioni pubblicate. Le procedure descritte in questa sezione illustrano come aggiungere e rimuovere le applicazioni pubblicate.

Un'applicazione può essere pubblicata in uno dei modi seguenti:

-   Come applicazione: selezionare un'applicazione specifica digitando la riga di comando per l'applicazione. Viene pubblicata solo l'applicazione selezionata.

-   Come menu: selezionare una cartella contenente più applicazioni. Tutte le applicazioni all'interno della cartella vengono pubblicate e visualizzate come menu.

## <a href="" id="bkmk-addingapublishedapplication"></a>Come aggiungere un'applicazione pubblicata a un'area di lavoro MED-V


**Per aggiungere un'applicazione all'area di lavoro MED-V**

1.  Fare clic sull'area di lavoro MED-V per configurare.

2.  Nella sezione **applicazioni pubblicate** del riquadro **applicazioni** fare clic su **Aggiungi** per aggiungere una nuova applicazione.

3.  Configurare le proprietà dell'applicazione come descritto nella tabella seguente.

4.  Nel menu **criteri** selezionare **commit**.

    **Nota**  
    Se si imposta Internet Explorer come applicazione pubblicata per verificare che il reindirizzamento del Web funzioni correttamente, verificare che i parametri non siano racchiusi tra parentesi.



**Proprietà delle applicazioni pubblicate**

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
<td align="left"><p>Abilitato</p></td>
<td align="left"><p>Selezionare questa casella di controllo per abilitare l'applicazione pubblicata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome visualizzato</p></td>
<td align="left"><p>Il nome del collegamento nel menu Start di Windows dell'utente&#39;.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Il nome visualizzato non è distinzione tra maiuscole e <strong> </strong> minuscole.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione dell'applicazione pubblicata, che viene visualizzata come descrizione comando quando l'utente&#39;il puntatore del mouse sul collegamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Riga di comando</p></td>
<td align="left"><p>Comando usato per eseguire l'applicazione dall'interno dell'area di lavoro MED-V. Il percorso completo è obbligatorio e i parametri possono essere passati all'applicazione in modo simile a qualsiasi altro comando Windows.</p>
<p>In un'area di lavoro di revertible MED-V è possibile eseguire il mapping di un'unità di rete con la sintassi MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; drive &gt; &lt; path, &gt; </em> &quot; ad esempio &quot; <em> MapNetworkDrive t: \tux\date </em> &quot; .</p>
<p>Ad esempio, per pubblicare Esplora risorse, usare la sintassi seguente: &quot; <em> c: &lt; /em &gt; &quot; o &quot; <em> c:\Windows </em> .&quot;</p>
<div class="alert">
<strong>Nota</strong><br/><p>Per avere una risoluzione del nome, è necessario eseguire una delle operazioni seguenti:</p>
</div>
<div>

</div>
<ul>
<li><p>Configurare il DNS nell'immagine dell'area di lavoro base MED-V.</p></li>
<li><p>Verificare che la risoluzione DNS sia definita nell'host e configurarla per l'uso dell'host DNS.</p></li>
<li><p>Usare l'IP per definire l'unità di rete.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Se il percorso include spazi, l'intero percorso deve essere racchiuso tra virgolette.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Nota</strong><br/><p>Il percorso non deve terminare con una barra rovesciata ().</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Menu Start</p></td>
<td align="left"><p>Selezionare questa casella di controllo per creare un collegamento per l'applicazione nel menu Start di Windows dell'utente&#39;.</p></td>
</tr>
</tbody>
</table>



Tutte le applicazioni pubblicate vengono visualizzate come tasti di scelta rapida nel menu **Start** di Windows (**Start &gt; All &gt; Applications programs MED-V**).

## Come rimuovere un'applicazione pubblicata da un'area di lavoro MED-V


**Per rimuovere un'applicazione dall'area di lavoro MED-V**

1.  Fare clic su un'area di lavoro MED-V.

2.  Nella sezione **applicazioni pubblicate** del riquadro **applicazioni** selezionare un'applicazione da rimuovere.

3.  Fare clic su **Rimuovi**.

    L'applicazione viene rimossa dall'elenco delle applicazioni pubblicate.

4.  Nel menu **criteri** selezionare **commit**.

## Come aggiungere un menu pubblicato a un'area di lavoro MED-V


**Per aggiungere un menu pubblicato all'area di lavoro MED-V**

1.  Fare clic sull'area di lavoro MED-V per configurare.

2.  Nella sezione **menu pubblicati** del riquadro **applicazioni** fare clic su **Aggiungi** per aggiungere un nuovo menu.

3.  Configurare le proprietà del menu come descritto nella tabella seguente.

4.  Nel menu **criteri** selezionare **commit**.

**Proprietà del menu pubblicato**

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
<td align="left"><p>Abilitato</p></td>
<td align="left"><p>Selezionare questa casella di controllo per abilitare il menu pubblicato.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Nome visualizzato</p></td>
<td align="left"><p>Il nome del collegamento nel menu Start di Windows dell'utente&#39;.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione, che viene visualizzata come descrizione comando quando l'utente&#39;il puntatore del mouse sul collegamento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cartella nell'area di lavoro</p></td>
<td align="left"><p>Selezionare la cartella da pubblicare come menu contenente tutte le applicazioni all'interno della cartella.</p>
<p>Il testo visualizzato è un percorso relativo dalla cartella programmi.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se lasciato vuoto, tutti i programmi nell'host verranno pubblicati come menu.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Tutti i menu pubblicati vengono visualizzati come tasti di scelta rapida nel menu **Start** di Windows (**avviare &gt; tutte &gt; le applicazioni programmi MED-V**). È possibile modificare il nome del collegamento nel campo della **cartella scelte rapide dal menu Start** .

**Nota**  
Quando si configurano due aree di lavoro MED-V, è consigliabile configurare un nome diverso per la cartella collegamenti al menu Start.



## Come rimuovere un menu pubblicato da un'area di lavoro MED-V


**Per rimuovere un menu pubblicato da un'area di lavoro MED-V**

1.  Fare clic su un'area di lavoro MED-V.

2.  Nella sezione **menu pubblicati** del riquadro **applicazioni** selezionare un menu da rimuovere.

3.  Fare clic su **Rimuovi**.

    Il menu viene rimosso dall'elenco dei menu pubblicati.

4.  Nel menu **criteri** selezionare **commit**.

## Eseguire un'applicazione pubblicata da una riga di comando nel client


L'amministratore può eseguire le applicazioni pubblicate da qualsiasi posizione, ad esempio un collegamento sul desktop, usando il comando seguente:

``` syntax
"<Install path>\Manager\KidaroCommands.exe" /run "<published application name>" "<MED-V workspace name>"
```

**Nota**  
L'area di lavoro MED-V in cui è definita l'applicazione pubblicata deve essere in corso.



## Argomenti correlati


[Come modificare un'applicazione pubblicata con le impostazioni avanzate](how-to-edit-a-published-application-with-advanced-settings.md)

[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

[Creazione di un'area di lavoro MED-V](creating-a-med-v-workspacemedv-10-sp1.md)









