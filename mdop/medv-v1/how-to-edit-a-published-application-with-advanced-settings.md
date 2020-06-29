---
title: Come modificare un'applicazione pubblicata con le impostazioni avanzate
description: Come modificare un'applicazione pubblicata con le impostazioni avanzate
author: dansimp
ms.assetid: 06a79049-9ce9-490f-aad7-fd4fdf185590
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 843aebb38f54959f209e742b398e3979acac3334
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826996"
---
# Come modificare un'applicazione pubblicata con le impostazioni avanzate


Dopo che un'applicazione pubblicata è stata aggiunta e configurata, è possibile modificare l'applicazione pubblicata e configurare altre impostazioni avanzate.

**Per modificare un'applicazione pubblicata con impostazioni avanzate**

1.  Nel riquadro **applicazioni** aggiungere e configurare un'applicazione pubblicata.

2.  Selezionare l'applicazione pubblicata da modificare.

3.  Fai clic su **Modifica**.

4.  Nella finestra di dialogo **applicazione pubblicata** configurare i parametri come descritto nella tabella seguente.

5.  Fai clic su **OK**.

6.  Nel menu **criteri** selezionare **commit**.

**Modifica delle proprietà dell'applicazione pubblicate**

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
<td align="left"><p>Nome visualizzato</p></td>
<td align="left"><p>Il nome del collegamento nel menu Start di Windows dell'utente&#39;.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Il nome visualizzato non è distinzione tra maiuscole e <strong> </strong> minuscole.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Descrizione</p></td>
<td align="left"><p>Descrizione del menu pubblicato.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Inizio pagina</p></td>
<td align="left"><p>Directory da cui avviare l'applicazione.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Il percorso non deve includere le virgolette.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Riga di comando</p></td>
<td align="left"><p>Comando con cui eseguire l'applicazione all'interno dell'area di lavoro MED-V.</p>
<p>Il percorso completo è obbligatorio e i parametri possono essere passati all'applicazione in modo simile a qualsiasi altro comando Windows.</p>
<p>In una configurazione di dominio un'unità condivisa esiste in genere nel server in cui sono mappati tutti i computer del dominio. La directory deve essere mappata qui e, se si tratta di una cartella che richiede l'autenticazione dell'utente, è <strong> necessario selezionare la casella di controllo Usa credenziali MED-V per eseguire questa applicazione </strong> .</p>
<p>In un'area di lavoro di revertible MED-V è possibile eseguire il mapping di un'unità di rete con la sintassi MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; drive &gt; &lt; path, &gt; </em> &quot; ad esempio &quot; <em> MapNetworkDrive t: \tux\data </em> &quot; .</p>
<p>Ad esempio, per pubblicare Esplora risorse, usare la sintassi seguente: &quot; <em> c: &amp; quot; o &quot; c:\Windows </em> &quot; .</p>
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
<td align="left"><p>Aggiungere un collegamento nel menu Start di Windows host</p></td>
<td align="left"><p>Selezionare questa casella di controllo per creare un collegamento per l'applicazione nel menu Start di Windows dell'utente&#39;.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Avviare l'applicazione quando l'area di lavoro viene avviata</p></td>
<td align="left"><p>Selezionare questa casella di controllo per eseguire automaticamente l'applicazione quando si avvia l'area di lavoro MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usare le credenziali di MED-V per eseguire l'applicazione</p></td>
<td align="left"><p>Selezionare questa casella di controllo per autenticare le applicazioni che richiedono un nome utente e una password usando le credenziali MED-V anziché le credenziali impostate per l'applicazione.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Quando si usa SSO, la riga di comando deve essere <strong>C:\Windows\Explorer.exe &quot; percorso cartella &quot; </strong> . Quando non si usa SSO, la riga di comando deve essere &quot; <strong> percorso cartella </strong> &quot; .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Argomenti correlati


[Come configurare le applicazioni pubblicate](how-to-configure-published-applicationsmedvv2.md)









